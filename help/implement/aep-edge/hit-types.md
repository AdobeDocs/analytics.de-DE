---
title: Edge Network-Ereignistypen in Adobe Analytics
description: Interpretieren der von Edge Network empfangenen Ereignisse durch Adobe Analytics.
feature: Implementation Basics
role: Admin, Developer
exl-id: 31085025-9c38-4375-8dfb-4fded6542ca7
source-git-commit: 0096a53505b3b1bc925c813c2c6c11ee3c7ee0c0
workflow-type: ht
source-wordcount: '425'
ht-degree: 100%

---

# Edge Network-Ereignistypen in Adobe Analytics

Adobe Analytics behandelt Treffer unterschiedlich, je nachdem, welche Funktionen Sie in AppMeasurement aufrufen. Beispielsweise schließen [`s.t`](/help/implement/vars/functions/t-method.md) und [`s.tl`](/help/implement/vars/functions/tl-method.md) bestimmte Dimensionen ein oder lassen sie aus und inkrementieren [Seitenansichten](/help/components/metrics/page-views.md) auf unterschiedliche Weise. Adobe Experience Platform enthält nur den Befehl [`sendEvent`](https://experienceleague.adobe.com/de/docs/experience-platform/collection/js/commands/sendevent/overview). Spezifische Eigenschaften in der Payload [`xdm`](https://experienceleague.adobe.com/de/docs/experience-platform/collection/js/commands/sendevent/xdm) oder [`data`](https://experienceleague.adobe.com/de/docs/experience-platform/collection/js/commands/sendevent/data) bestimmen, wie diese Daten in Adobe Analytics interpretiert werden.

Das Edge Network verwendet die folgende Logik, um die [Seitenansichten](/help/components/metrics/page-views.md) und [Link-Ereignisse](/help/components/metrics/page-events.md) in Adobe Analytics zu bestimmen:

## Seitenansichten und Verknüpfen von Ereignissen mithilfe des Objekts `xdm`

| XDM-Payload enthält … | Adobe Analytics … |
|---|---|
| `xdm.web.webPageDetails.name` oder `xdm.web.webPageDetails.URL` und nicht `xdm.web.webInteraction.type` | betrachtet Payload als eine **Seitenansicht** |
| `xdm.eventType = web.webpagedetails.pageViews` | betrachtet Payload als eine **Seitenansicht** |
| `xdm.web.webInteraction.type` und (`xdm.web.webPageDetails.name` oder `xdm.web.webPageDetails.URL`) | betrachtet Payload als ein **Link-Ereignis** <br/>setzt außerdem `xdm.web.webPageDetails.name` und `xdm.web.webPageDetails.URL` auf `null` |
| `xdm.web.webInteraction.type` und (`xdm.web.webInteraction.name` oder `xdm.web.webInteraction.URL`) | betrachtet Payload als ein **Link-Ereignis** <br/>setzt außerdem `xdm.web.webPageDetails.name` und `xdm.web.webPageDetails.URL` auf `null`, falls vorhanden |
| kein `xdm.web.webInteraction.type` und kein `xdm.web.webPageDetails.name` und kein `xdm.web.webPageDetails.URL` | entfernt die Payload und ignoriert die Daten |

>[!TIP]
>
>Bei XDM-Feldnamen in der Payload wird zwischen Groß- und Kleinschreibung unterschieden (z. B. `webPageDetails.URL`). Das Feld `xdm.eventType` ist ein Zeichenfolgenwert mit einem eigenen Satz zulässiger Werte. Die Groß-/Kleinschreibung in diesen Werten stimmt möglicherweise nicht mit den XDM-Feldnamen überein. Zulässige Werte finden Sie im Feld `eventType` in der [XDM ExperienceEvent-Klasse](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/classes/experienceevent#eventType).

+++Minimale Seitenansicht mit den Feldern `xdm`

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

+++Minimales Link-Ereignis mit empfohlenen Feldern

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

## Seitenansichten und Verknüpfen von Ereignissen mithilfe des Objekts `data`

| Datenobjekt-Payload enthält … | Adobe Analytics … |
|---|---|
| `data.__adobe.analytics.pageName` oder `data.__adobe.analytics.pageURL` und nicht `data.__adobe.analytics.linkType` | betrachtet Payload als eine **Seitenansicht** |
| `data.__adobe.analytics.linkType` und (`data.__adobe.analytics.linkName` oder `data.__adobe.analytics.linkURL`) | betrachtet Payload als ein **Link-Ereignis** <br/>setzt außerdem `data.__adobe.analytics.pageName` und `data.__adobe.analytics.pageURL` auf `null` |
| kein `data.__adobe.analytics.linkType` und kein `data.__adobe.analytics.pageName` und kein `data.__adobe.analytics.pageURL` | entfernt die Payload und ignoriert die Daten |

+++Minimale Seitenansicht mit den Feldern `data`

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

+++Minimales Link-Ereignis mit den Feldern `data`

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
>Wenn Sie sowohl ein Objekt `xdm` und ein Objekt `data` in dieselbe Payload einbeziehen, prüft Adobe Analytics beide Objekte auf die jeweiligen Felder.

## A4T- und entscheidungsbezogene Ereignisse

Zusätzlich zur Unterscheidung zwischen Seitenansichten und Link-Ereignissen bestimmt die folgende Logik, ob bestimmte Entscheidungsereignisse als A4T kategorisiert oder verworfen werden.

| XDM-Payload enthält … | Adobe Analytics … |
|---|---|
| `xdm.eventType = decisioning.propositionDisplay` und `xdm._experience.decisioning` | betrachtet Payload als einen **A4T**-Aufruf. |
| `xdm.eventType = decisioning.propositionDisplay` und kein `xdm._experience.decisioning` | entfernt die Payload und ignoriert die Daten |
| `xdm.eventType = decisioning.propositionInteract` und `xdm._experience.decisioning` und nicht `xdm.web.webInteraction.type` | betrachtet Payload als einen **A4T**-Aufruf. |
| `xdm.eventType = decisioning.propositionInteract` und kein `xdm._experience.decisioning` und kein `xdm.web.webInteraction.type` | entfernt die Payload und ignoriert die Daten. |
| `xdm.eventType = decisioning.propositionFetch` | entfernt die Payload und ignoriert die Daten |

>[!TIP]
>
>Die folgenden Werte `eventType` sind veraltet: Beachten Sie, dass diese Werte die Logik auf die gleiche Weise beeinflussen wie ihre aktuellen Gegenstücke:
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
