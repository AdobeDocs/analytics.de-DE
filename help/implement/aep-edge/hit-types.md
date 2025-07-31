---
title: Edge Network-Ereignistypen in Adobe Analytics
description: Interpretation der von Edge Network empfangenen Ereignisse durch Adobe Analytics
feature: Implementation Basics
role: Admin, Developer
source-git-commit: 8d369bd3be3ae9c075e490e108666728a2cff5dc
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 28%

---

# Edge Network-Ereignistypen in Adobe Analytics

In Adobe Analytics werden Treffer je nachdem, welche Funktionen Sie in AppMeasurement aufrufen, unterschiedlich behandelt. [`s.t`](/help/implement/vars/functions/t-method.md) und [`s.tl`](/help/implement/vars/functions/tl-method.md) beispielsweise bestimmte Dimensionen ein- oder auslassen und Seitenansichten unterschiedlich inkrementieren. Adobe Experience Platform enthält nur den `sendEvent`. Spezifische Eigenschaften innerhalb der `xdm` Payload bestimmen, wie diese Daten in Adobe Analytics interpretiert werden.

Die Edge Network verwendet die folgende Logik, um Adobe Analytics-Seitenansichten und Link-Ereignisse zu bestimmen:

| XDM-Payload enthält … | Adobe Analytics … |
|---|---|
| `xdm.web.webPageDetails.name` oder `xdm.web.webPageDetails.URL` und nicht `xdm.web.webInteraction.type` | betrachtet Payload als eine **Seitenansicht** |
| `xdm.eventType = web.webPageDetails.pageViews` | betrachtet Payload als eine **Seitenansicht** |
| `xdm.web.webInteraction.type` und (`xdm.web.webInteraction.name` oder `xdm.web.webInteraction.url`) | betrachtet Payload als ein **Link-Ereignis** |
| `xdm.web.webInteraction.type` und (`xdm.web.webPageDetails.name` oder `xdm.web.webPageDetails.url`) | betrachtet die Payload als **Link-Ereignis** <br/>setzt außerdem `xdm.web.webPageDetails.name` und `xdm.web.webPageDetails.URL` auf `null` |
| kein `xdm.web.webInteraction.type` und (kein `xdm.webPageDetails.name` und kein `xdm.web.webPageDetails.URL`) | entfernt die Payload und ignoriert die Daten |

Neben der Unterscheidung von Seitenansichten und Link-Klicks gibt es die folgende Logik, die bestimmt, ob bestimmte Ereignisse als A4T kategorisiert oder verworfen werden.

| XDM-Payload enthält … | Adobe Analytics … |
| --- | --- |
| `xdm.eventType = display` oder <br/>`xdm.eventType = decisioning.propositionDisplay` oder <br/>`xdm.eventType = personalization.request` oder <br/>`xdm.eventType = decisioning.propositionFetch` und `xdm._experience.decisioning` | Nutzlast wird als **A4T**-Aufruf betrachtet. |
| `xdm.eventType = display` oder <br/>`xdm.eventType = decisioning.propositionDisplay` oder <br/>`xdm.eventType = personalization.request` oder <br/>`xdm.eventType = decisioning.propositionFetch` und keine `xdm._experience.decisioning` | entfernt die Payload und ignoriert die Daten |
| `xdm.eventType = click` oder `xdm.eventType = decisioning.propositionInteract` und `xdm._experience.decisioning` und keine `web.webInteraction.type` | Nutzlast wird als **A4T**-Aufruf betrachtet. |
| `xdm.eventType = click` oder `xdm.eventType = decisioning.propositionInteract` und keine `xdm._experience.decisioning` und keine `web.webInteraction.type` | Löscht die Payload und ignoriert die Daten. |

Weitere Informationen finden Sie unter [Adobe Analytics ExperienceEvent Full Extension-Schema-Feldgruppe](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/field-groups/event/analytics-full-extension).
