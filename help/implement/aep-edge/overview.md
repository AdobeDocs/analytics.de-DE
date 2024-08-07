---
title: Implementieren von Adobe Analytics mit Adobe Experience Platform Edge
description: Übersicht über die Verwendung von XDM-Daten aus Experience Platform in Adobe Analytics
exl-id: 7d8de761-86e3-499a-932c-eb27edd5f1a3
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: 914b822aae659d1d0f0b8a98480090ead99e102a
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 100%

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


Edge Network verwendet die folgende Logik, um die Seitenansichten und Verknüpfungsereignisse in Adobe Analytics zu bestimmen.

| XDM-Payload enthält … | Adobe Analytics … |
|---|---|
| `web.webPageDetails.name` oder `web.webPageDetails.URL` und nicht `web.webInteraction.type` | betrachtet Payload als eine **Seitenansicht** |
| `web.webInteraction.type` und (`web.webInteraction.name` oder `web.webInteraction.url`) | betrachtet Payload als ein **Link-Ereignis** |
| `web.webInteraction.type` und (`web.webPageDetails.name` oder `web.webPageDetails.url`) | betrachtet Payload als ein **Link-Ereignis** <br/>`web.webPageDetails.name` und `web.webPageDetails.URL` sind auf `null` gesetzt |
| kein `web.webInteraction.type` und (kein `webPageDetails.name` und kein `web.webPageDetails.URL`) | entfernt die Payload und ignoriert die Daten |

{style="table-layout:auto"}

Weitere Informationen finden Sie unter [Adobe Analytics ExperienceEvent Full Extension-Schema-Feldgruppe](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/event/analytics-full-extension.html).
