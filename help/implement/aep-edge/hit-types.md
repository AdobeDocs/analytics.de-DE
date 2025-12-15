---
title: Edge Network-Ereignistypen in Adobe Analytics
description: Interpretation der von Edge Network empfangenen Ereignisse durch Adobe Analytics
feature: Implementation Basics
role: Admin, Developer
exl-id: 31085025-9c38-4375-8dfb-4fded6542ca7
source-git-commit: 0096a53505b3b1bc925c813c2c6c11ee3c7ee0c0
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 20%

---

# Edge Network-Ereignistypen in Adobe Analytics

In Adobe Analytics werden Treffer je nachdem, welche Funktionen Sie in AppMeasurement aufrufen, unterschiedlich behandelt. Beispielsweise schließen [`s.t`](/help/implement/vars/functions/t-method.md) und [`s.tl`](/help/implement/vars/functions/tl-method.md) bestimmte Dimensionen ein oder lassen sie aus und erhöhen [Seitenansichten](/help/components/metrics/page-views.md) unterschiedlich. Adobe Experience Platform enthält nur den [`sendEvent`](https://experienceleague.adobe.com/de/docs/experience-platform/collection/js/commands/sendevent/overview). Spezifische Eigenschaften innerhalb der [`xdm`](https://experienceleague.adobe.com/de/docs/experience-platform/collection/js/commands/sendevent/xdm)- oder [`data`](https://experienceleague.adobe.com/de/docs/experience-platform/collection/js/commands/sendevent/data)-Payload bestimmen, wie diese Daten in Adobe Analytics interpretiert werden.

Die Edge Network verwendet die folgende Logik, um Adobe Analytics-[&#x200B; (Seitenansichten](/help/components/metrics/page-views.md) und [Link-Ereignisse](/help/components/metrics/page-events.md) zu bestimmen:

## Seitenansichten und Verknüpfen von Ereignissen mithilfe des `xdm`

| XDM-Payload enthält … | Adobe Analytics … |
|---|---|
| `xdm.web.webPageDetails.name` oder `xdm.web.webPageDetails.URL` und nicht `xdm.web.webInteraction.type` | betrachtet Payload als eine **Seitenansicht** |
| `xdm.eventType = web.webpagedetails.pageViews` | betrachtet Payload als eine **Seitenansicht** |
| `xdm.web.webInteraction.type` und (`xdm.web.webPageDetails.name` oder `xdm.web.webPageDetails.URL`) | betrachtet die Payload als **Link-Ereignis** <br/>setzt außerdem `xdm.web.webPageDetails.name` und `xdm.web.webPageDetails.URL` auf `null` |
| `xdm.web.webInteraction.type` und (`xdm.web.webInteraction.name` oder `xdm.web.webInteraction.URL`) | Nutzlast als **Link-Ereignis** betrachtet <br/>setzt `xdm.web.webPageDetails.name` und `xdm.web.webPageDetails.URL` auch auf `null`, falls vorhanden |
| Keine `xdm.web.webInteraction.type` und keine `xdm.web.webPageDetails.name` und keine `xdm.web.webPageDetails.URL` | entfernt die Payload und ignoriert die Daten |

>[!TIP]
>
>Bei XDM-Feldnamen in der Payload wird zwischen Groß- und Kleinschreibung unterschieden (z. B. `webPageDetails.URL`). Das `xdm.eventType` ist ein Zeichenfolgenwert mit einem eigenen Satz akzeptierter Werte. Die Groß-/Kleinschreibung in diesen Werten stimmt möglicherweise nicht mit den XDM-Feldnamen überein. Akzeptierte Werte finden Sie im `eventType` in der [XDM ExperienceEvent-Klasse](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/classes/experienceevent#eventType).

+++Minimale Seitenansicht mit `xdm` Feldern

```json
{
  "xdm": {
    "web": {
      "webPageDetails": {
        "name": "Example page",
        "URL": "https://example.com/page"
      }
    }
  }
}
```

+++

+++Minimale Seitenansicht mit `xdm.eventType`

```json
{
  "xdm": {
    "eventType": "web.webpagedetails.pageViews"
  }
}
```

+++

+++Minimales Verknüpfungsereignis mit empfohlenen Feldern

```json
{
  "xdm": {
    "web": {
      "webInteraction": {
        "type": "other",
        "name": "Header nav: Pricing",
        "URL": "https://example.com/pricing"
      }
    }
  }
}
```

+++

## Seitenansichten und Verknüpfen von Ereignissen mithilfe des `data`

| Datenobjekt-Payload enthält… | Adobe Analytics … |
|---|---|
| `data.__adobe.analytics.pageName` oder `data.__adobe.analytics.pageURL` und nicht `data.__adobe.analytics.linkType` | betrachtet Payload als eine **Seitenansicht** |
| `data.__adobe.analytics.linkType` und (`data.__adobe.analytics.linkName` oder `data.__adobe.analytics.linkURL`) | betrachtet die Payload als **Link-Ereignis** <br/>setzt außerdem `data.__adobe.analytics.pageName` und `data.__adobe.analytics.pageURL` auf `null` |
| Keine `data.__adobe.analytics.linkType` und keine `data.__adobe.analytics.pageName` und keine `data.__adobe.analytics.pageURL` | entfernt die Payload und ignoriert die Daten |

+++Minimale Seitenansicht mit `data` Feldern

```json
{
  "data": {
    "__adobe": {
      "analytics": {
        "pageName": "Example page",
        "pageURL": "https://example.com/page"
      }
    }
  }
}
```

+++

+++Minimales Verknüpfungsereignis mit `data` Feldern

```json
{
  "data": {
    "__adobe": {
      "analytics": {
        "linkType": "o",
        "linkName": "Header nav: Pricing",
        "linkURL": "https://example.com/pricing"
      }
    }
  }
}
```

+++

>[!NOTE]
>
>Wenn Sie sowohl ein `xdm` als auch ein `data` Objekt in dieselbe Payload einbeziehen, prüft Adobe Analytics beide Objekte auf die entsprechenden Felder.

## A4T- und entscheidungsbezogene Ereignisse

Neben der Unterscheidung von Seitenansichten und Link-Ereignissen bestimmt die folgende Logik, ob bestimmte Entscheidungsereignisse als A4T kategorisiert oder verworfen werden.

| XDM-Payload enthält … | Adobe Analytics … |
|---|---|
| `xdm.eventType = decisioning.propositionDisplay` und `xdm._experience.decisioning` | Nutzlast wird als **A4T**-Aufruf betrachtet. |
| `xdm.eventType = decisioning.propositionDisplay` und keine `xdm._experience.decisioning` | entfernt die Payload und ignoriert die Daten |
| `xdm.eventType = decisioning.propositionInteract` und `xdm._experience.decisioning` und keine `xdm.web.webInteraction.type` | Nutzlast wird als **A4T**-Aufruf betrachtet. |
| `xdm.eventType = decisioning.propositionInteract` und keine `xdm._experience.decisioning` und keine `xdm.web.webInteraction.type` | Löscht die Payload und ignoriert die Daten. |
| `xdm.eventType = decisioning.propositionFetch` | entfernt die Payload und ignoriert die Daten |

>[!TIP]
>
>Die folgenden `eventType` werden nicht mehr unterstützt. Beachten Sie, dass sich diese Werte auf die gleiche Weise auf die Logik auswirken wie ihre aktuellen Gegenstücke:
>
>* Der Ereignistyp `display` ist veraltet. Verwenden Sie stattdessen `decisioning.propositionDisplay`.
>* Der Ereignistyp `click` ist veraltet. Verwenden Sie stattdessen `decisioning.propositionInteract`.
>* Der Ereignistyp `personalization.request` ist veraltet. Verwenden Sie stattdessen `decisioning.propositionFetch`.

+++Minimale A4T-Anzeige

```json
{
  "xdm": {
    "eventType": "decisioning.propositionDisplay",
    "_experience": {
      "decisioning": {
        "propositions": [
          {
            "id": "example-proposition-id",
            "scope": "example-scope",
            "scopeDetails": { "decisionProvider": "AJO" }
          }
        ],
        "propositionEventType": { "display": 1 }
      }
    }
  }
}
```

+++

+++Minimale A4T-Interaktion

```json
{
  "xdm": {
    "eventType": "decisioning.propositionInteract",
    "_experience": {
      "decisioning": {
        "propositions": [
          {
            "id": "example-proposition-id",
            "scope": "example-scope",
            "scopeDetails": { "decisionProvider": "AJO" }
          }
        ],
        "propositionEventType": { "interact": 1 }
      }
    }
  }
}
```

+++

Weitere Informationen finden Sie unter [Adobe Analytics ExperienceEvent Full Extension-Schema-Feldgruppe](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/field-groups/event/analytics-full-extension).
