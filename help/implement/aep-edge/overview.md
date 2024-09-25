---
title: Implementieren von Adobe Analytics mit Adobe Experience Platform Edge
description: Übersicht über die Verwendung von XDM-Daten aus Experience Platform in Adobe Analytics
exl-id: 7d8de761-86e3-499a-932c-eb27edd5f1a3
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: 4453c2aa2ea70ef4d00b2bc657285287f3250c65
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 85%

---

# Implementieren von Adobe Analytics mit dem Adobe Experience Platform Edge Network

Mit Adobe Experience Platform Edge Network können Sie Daten, die für mehrere Produkte bestimmt sind, an einen zentralen Ort senden. Edge Network leitet die entsprechenden Informationen an die gewünschten Produkte weiter. Mit diesem Konzept können Sie Implementierungsaufgaben zusammenfassen, insbesondere, wenn mehrere Datenlösungen vorhanden sind.

Adobe bietet drei Methoden zum Senden von Daten an Edge Network:

* **[Adobe Experience Platform Web SDK](web-sdk/overview.md)**: Verwenden Sie die Web SDK-Erweiterung in der Datenerfassung von Adobe Experience Platform, um Daten an Edge zu senden.
* **[Adobe Experience Platform Mobile SDK](mobile-sdk/overview.md)**: Verwenden Sie die Mobile SDK-Erweiterung in der Datenerfassung von Adobe Experience Platform, um Daten an Edge zu senden.
* **[Adobe Experience Platform Edge Network Server-API](server-api/overview.md)**: Senden Sie Daten mithilfe einer API direkt an Edge.



## Verarbeiten von Edge Network-Daten durch Adobe Analytics

An Adobe Experience Platform Edge Network gesendete Daten können zwei Formate aufweisen:

* XDM-Objekt: Entsprechen Schemas, die auf [XDM (Experience-Datenmodell)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de) basieren.  Mit XDM können Sie flexibel bestimmen, welche Felder als Teil von Ereignissen definiert werden. Wenn Ereignisse Adobe Analytics erreichen, werden sie in ein Format übersetzt, das Adobe Analytics verarbeiten kann.
* Datenobjekt: Senden Sie Daten mithilfe bestimmter, Adobe Analytics zugewiesener Felder an Edge Network. Edge Network erkennt das Vorhandensein dieser Felder und leitet sie an Adobe Analytics weiter, ohne dass sie einem Schema entsprechen müssen.

Das Edge Network verwendet die folgende Logik, um Adobe Analytics-Seitenansichten und Verknüpfungsereignisse zu bestimmen:

| XDM-Payload enthält … | Adobe Analytics … |
|---|---|
| `xdm.web.webPageDetails.name` oder `xdm.web.webPageDetails.URL` und nicht `xdm.web.webInteraction.type` | betrachtet Payload als eine **Seitenansicht** |
| `xdm.web.webInteraction.type` und (`xdm.web.webInteraction.name` oder `xdm.web.webInteraction.url`) | betrachtet Payload als ein **Link-Ereignis** |
| `web.webInteraction.type` und (`web.webPageDetails.name` oder `web.webPageDetails.url`) | betrachtet Payload als ein **Link-Ereignis** <br/>`web.webPageDetails.name` und `web.webPageDetails.URL` sind auf `null` gesetzt |
| kein `web.webInteraction.type` und (kein `webPageDetails.name` und kein `web.webPageDetails.URL`) | entfernt die Payload und ignoriert die Daten |
| `xdm.eventType = display` oder <br/>`xdm.eventType = decisioning.propositionDisplay` oder <br/>`xdm.eventType = personalization.request` oder <br/>`xdm.eventType = decisioning.propositionFetch` und `xdm._experience.decisioning` | berücksichtigt Nutzlast einen **A4T** -Aufruf. |
| `xdm.eventType = display` oder <br/>`xdm.eventType = decisioning.propositionDisplay` oder <br/>`xdm.eventType = personalization.request` oder <br/>`xdm.eventType = decisioning.propositionFetch` und keine `xdm._experience.decisioning` | entfernt die Payload und ignoriert die Daten |
| `xdm.eventType = click` oder `xdm.eventType = decisioning.propositionInteract` und `xdm._experience.decisioning` und keine `web.webInteraction.type` | berücksichtigt Nutzlast einen **A4T** -Aufruf. |
| `xdm.eventType = click` oder `xdm.eventType = decisioning.propositionInteract` und keine `xdm._experience.decisioning` und keine `web.webInteraction.type` | speichert die Payload und ignoriert die Daten. |

{style="table-layout:auto"}

Weitere Informationen finden Sie unter [Adobe Analytics ExperienceEvent Full Extension-Schema-Feldgruppe](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/event/analytics-full-extension.html).
