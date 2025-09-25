---
title: Edge Network-Ereignistypen in Adobe Analytics
description: Interpretation der von Edge Network empfangenen Ereignisse durch Adobe Analytics
feature: Implementation Basics
role: Admin, Developer
exl-id: 31085025-9c38-4375-8dfb-4fded6542ca7
source-git-commit: 6e500007e10086c0ff8108856a3563d7702f1130
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 25%

---

# Edge Network-Ereignistypen in Adobe Analytics

In Adobe Analytics werden Treffer je nachdem, welche Funktionen Sie in AppMeasurement aufrufen, unterschiedlich behandelt. [`s.t`](/help/implement/vars/functions/t-method.md) und [`s.tl`](/help/implement/vars/functions/tl-method.md) beispielsweise bestimmte Dimensionen ein- oder auslassen und Seitenansichten unterschiedlich inkrementieren. Adobe Experience Platform enthält nur den `sendEvent`. Spezifische Eigenschaften innerhalb der `xdm` Payload bestimmen, wie diese Daten in Adobe Analytics interpretiert werden.

Die Edge Network verwendet die folgende Logik, um Adobe Analytics-Seitenansichten und Link-Ereignisse zu bestimmen:

| XDM-Payload enthält … | Adobe Analytics … |
|---|---|
| `xdm.web.webPageDetails.name` oder `xdm.web.webPageDetails.URL` und nicht `xdm.web.webInteraction.type` | betrachtet Payload als eine **Seitenansicht** |
| `xdm.eventType = web.webPageDetails.pageViews` | betrachtet Payload als eine **Seitenansicht** |
| `xdm.web.webInteraction.type` und (`xdm.web.webPageDetails.name` oder `xdm.web.webPageDetails.url`) | betrachtet die Payload als **Link-Ereignis** <br/>setzt außerdem `xdm.web.webPageDetails.name` und `xdm.web.webPageDetails.URL` auf `null` |
| Keine `xdm.web.webInteraction.type` und keine `xdm.webPageDetails.name` und keine `xdm.web.webPageDetails.URL` | entfernt die Payload und ignoriert die Daten |

| Datenobjekt-Payload enthält… | Adobe Analytics … |
|---|---|
| `data.__adobe.analytics.pageName` oder `data.__adobe.analytics.pageURL` und nicht `data.__adobe.analytics.linkType` | betrachtet Payload als eine **Seitenansicht** |
| `data.__adobe.analytics.linkType` und (`data.__adobe.analytics.linkName` oder `data.__adobe.analytics.linkURL`) | betrachtet die Payload als **Link-Ereignis** <br/>setzt außerdem `data.__adobe.analytics.pageName` und `data.__adobe.analytics.pageURL` auf `null` |
| Keine `data.__adobe.analytics.linkType` und keine `data.__adobe.analytics.pageName` und keine `data.__adobe.analytics.pageURL` | entfernt die Payload und ignoriert die Daten |

>[!NOTE]
>
>Wenn Sie sowohl ein `xdm` als auch ein `data` Objekt in dieselbe Payload einbeziehen, prüft Adobe Analytics beide Objekte auf die entsprechenden Felder.

Neben der Unterscheidung von Seitenansichten und Link-Klicks gibt es die folgende Logik, die bestimmt, ob bestimmte Ereignisse als A4T kategorisiert oder verworfen werden.

| XDM-Payload enthält … | Adobe Analytics … |
|---|---|
| `xdm.eventType = display` oder <br/>`xdm.eventType = decisioning.propositionDisplay` oder <br/>`xdm.eventType = personalization.request` oder <br/>`xdm.eventType = decisioning.propositionFetch` und `xdm._experience.decisioning` | Nutzlast wird als **A4T**-Aufruf betrachtet. |
| `xdm.eventType = display` oder <br/>`xdm.eventType = decisioning.propositionDisplay` oder <br/>`xdm.eventType = personalization.request` oder <br/>`xdm.eventType = decisioning.propositionFetch` und keine `xdm._experience.decisioning` | entfernt die Payload und ignoriert die Daten |
| `xdm.eventType = click` oder `xdm.eventType = decisioning.propositionInteract` und `xdm._experience.decisioning` und keine `web.webInteraction.type` | Nutzlast wird als **A4T**-Aufruf betrachtet. |
| `xdm.eventType = click` oder `xdm.eventType = decisioning.propositionInteract` und keine `xdm._experience.decisioning` und keine `web.webInteraction.type` | Löscht die Payload und ignoriert die Daten. |

Weitere Informationen finden Sie unter [Adobe Analytics ExperienceEvent Full Extension-Schema-Feldgruppe](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/field-groups/event/analytics-full-extension).
