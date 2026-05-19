---
description: Es gibt Besuchermetriken in Adobe Analytics und Adobe Audience Manager, die ähnliche Definitionen haben, die sich aber aus verschiedenen Gründen nicht zu 100 % entsprechen.
title: Unterschiede in der Besucherzahl
feature: Audience Analytics
exl-id: be5a935a-c3a2-4ab4-8cd7-ed54a37932c8
TQID: https://experienceleague.adobe.com/ksfYYDZ6G9vH7WEZVh-JsN93Rl-jsZTe9-CQADSwnfI
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 312
ht-degree: 50%

---

# Unterschiede in der Besucherzahl

Es gibt Besuchermetriken in Adobe Analytics und Adobe Audience Manager, die ähnliche Definitionen haben, die sich aber aus verschiedenen Gründen nicht zu 100 % entsprechen.

Die Besuchermetriken sind:

<table id="table_F9FE107A89934C3B854C55D7D76AC6E8"> 
 <thead> 
  <tr> 
   <th colname="col2" class="entry"> Metrik </th> 
   <th colname="col3" class="entry"> Definition </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col2"> <p><a href="https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder-data.html?lang=de"  > Adobe Audience Manager: Gesamte Segmentpopulation</a> </p> </td> 
   <td colname="col3"> <p>Anzahl der Geräte (Experience Cloud IDs), die während des Lookback-Zeitraums Teil Ihres Segments waren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><a href="https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder-data.html?lang=de"  > Adobe Audience Manager: Echtzeit-Segmentpopulation</a> </p> </td> 
   <td colname="col3"> <p>Anzahl der Geräte (Experience Cloud-IDs), die Mitglied Ihres Segments waren und während des Lookback-Zeitraums Ihre Eigenschaften erreicht haben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Analytics: Unique Visitors </p> </td> 
   <td colname="col3"> <p>Zeigt die Anzahl der Unique Visitors, die Ihre Eigenschaften während des Berichtszeitraums erreicht haben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Analytics: Besucher mit Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>Zeigt die Anzahl der Unique Visitors mit einer Experience Cloud ID an, die Ihre Eigenschaften während des Berichtszeitraums erreicht haben. </p> </td> 
  </tr> 
 </tbody> 
</table>

Am ähnlichsten sind Adobe Audience Manager Real-time Segment Population und Analytics Visitors mit Experience Cloud ID, die in Audience Analytics-Berichten verwendet werden. In der nächsten Zeit gibt es dabei jedoch aufgrund verschiedener Faktoren leichte Diskrepanzen. Folgende Faktoren tragen dazu bei:

<table id="table_A391B37CC077456F8BB83BAA3C640EF6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Faktor </th> 
   <th colname="col2" class="entry"> Adobe Audience Manager: Echtzeit-Segmentpopulation </th> 
   <th colname="col3" class="entry"> Analytics: Besucher mit Experience Cloud ID </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Zeitzone </p> </td> 
   <td colname="col2"> <p>UTC (Coordinated Universal Time) </p> </td> 
   <td colname="col3"> <p>Angegeben pro Report Suite </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Benutzerdefinierte Filter </p> </td> 
   <td colname="col2"> <p>Nein </p> </td> 
   <td colname="col3"> <p>Ja, z. B. IP-Filter, Bot-Filter </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Limit von 150 Segmenten </p> </td> 
   <td colname="col2"> <p>Nein </p> </td> 
   <td colname="col3"> <p>Ja - Analytics-Zahlen können bis zu 5 % von dem Limit für die 150-Segment-Integration betroffen sein. „Zielgruppenlimit erreicht“ wird in der Dimension „Zielgruppenname“ angezeigt, wenn es zu einer Kürzung kam. </p> </td> 
  </tr> 
 </tbody> 
</table>

Siehe [Segmente in Analytics und Audience Manager – Grundlagen](/help/integrate/c-audience-analytics/aam-analytics-segments.md) für zusätzliche Erklärungen zu den Nuancen zwischen Daten und der Segmentierung zwischen Analytics und Audience Manager.
