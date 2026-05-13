---
description: Erfahren Sie, warum nicht alle in Segment Builder erstellten Segmente mit Data Warehouse kompatibel sind. Erfahren Sie, welche Funktionen unterstützt werden.
title: Data Warehouse-Segmentkompatibilität
feature: Segmentation
exl-id: 66b86226-ef4c-4a1a-abe1-3c3accf419e5
TQID: https://experienceleague.adobe.com/7CrArNYD-8ZXVpfO86d1l42ySkTuv8V04PWJFeNWx3s
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2: id: a544b409-2610-410d-a842-474ac1d0d54eid: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 345
ht-degree: 55%

---

# Data Warehouse-Segmentkompatibilität

Nicht alle in Segment Builder erstellten Segmente sind mit [!DNL Data Warehouse] kompatibel. Diese Tabelle listet die unterstützten Funktionen auf.

<table> 
 <thead> 
  <tr> 
   <th> </th> 
   <th> Analysis Workspace, Reports &amp; Analytics </th> 
   <th> Data Warehouse </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td > <b>Container ausschließen</b> </td> 
   <td> Auf beliebiger Ebene unterstützt </td> 
   <td> Wird nur in Sonderfällen auf der obersten Ebene unterstützt </td> 
  </tr> 
  <tr> 
   <td> <b>Sequenzielle Segmente</b> </td> 
   <td> Unterstützt </td> 
   <td> Nicht unterstützt </td> 
  </tr> 
  <tr> 
   <td> <b>AND und OR können uneingeschränkt kombiniert werden</b> </td> 
   <td> Unterstützt </td> 
   <td> Einige Einschränkungen. Siehe *Hinweis* unter der Tabelle. </td> 
  </tr> 
  <tr> 
   <td> <b>Verschachtelte Container</b> </td> 
   <td> Unterstützt </td> 
   <td> Einige Einschränkungen (sie müssen im Umfang abnehmen, z. B. können Besucher Treffer enthalten, aber nicht umgekehrt) </td> 
  </tr> 
  <tr> 
   <td> <b>Dimensionen</b> </td> 
   <td>Ziehen Sie eine Dimension per Drag-and-Drop in das Feld <span class="uicontrol">-Definitionen </span> Segment Builders, um mehr über die Produktkompatibilität zu erfahren. Beispielsweise werden diese Dimensionen nur in Analysis Workspace und Reports &amp; Analytics unterstützt: 
    <ul> 
     <li>Entryserver </li> 
     <li>Eingabekategorie </li> 
     <li>Eingabedatum </li> 
     <li>Rangansicht aller Suchseiten </li> 
    </ul> </td> 
   <td> Ziehen Sie eine Dimension per Drag-and-Drop in das Feld <span class="uicontrol">-Definitionen </span> Segment Builders, um mehr über die Produktkompatibilität zu erfahren. Beispielsweise werden diese Dimensionen nur in Data Warehouse unterstützt: 
    <ul> 
     <li>IP-Adresse </li> 
     <li>Seiten-URL </li> 
     <li>Besucher-ID </li> 
     <li>Experience Cloud-Besucher-ID </li> 
    </ul> <p>Die folgenden Dimensionen <b>können nicht </b>in Data Warehouse-Segmenten verwendet werden: </p> 
    <ul> 
     <li>Rangansicht aller Suchseiten </li> 
     <li>Vormittag/Nachmittag </li> 
     <li>Tag des Monats </li> 
     <li>Wochentag </li> 
     <li>Tag des Jahres </li> 
     <li>Geschäftseinheit Eintritt </li> 
     <li>Eingabe (Alle Dimensionen, die mit Eingabe beginnen, außer Einstiegsseite) </li> 
     <li>Exit (Alle Dimensionen, die mit Exit beginnen, außer Exitlink und Exitpage) </li> 
     <li>Hierarchie (alle Dimensionen, die mit Hierarchie beginnen) </li> 
     <li>Treffertiefe </li> 
     <li>Treffertyp </li> 
     <li>Stunde Tag </li> 
     <li>Monat des Jahres </li> 
     <li>Seiten nicht gefunden </li> 
     <li>Paid Search </li> 
     <li>Quartal des Jahres </li> 
     <li>Rückkehrhäufigkeit </li> 
     <li>Einzelseitenbesuche </li> 
     <li>Zeit vor Ereignis </li> 
     <li>Besuchszeit pro Seite – zusammengefasst </li> 
     <li>Zeit pro Besuch – zusammengefasst </li> 
     <li>Nachverfolgen des Abmeldegrunds </li> 
     <li>US-Staaten </li> 
     <li>Wochentag/Wochenende </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <b>Segmentstapelung</b> </td> 
   <td> Unterstützt </td> 
   <td> Unterstützt </td> 
  </tr>
  <tr>
    <td><b>Operatoren „entspricht beliebigen von“ und „entspricht keinem von“</b></td>
    <td>Unterstützt</td>
    <td>Nicht unterstützt</td>
  </tr>
 </tbody> 
</table>

*Hinweis: Data Warehouse unterstützt nicht alle Fälle der Verwendung eines `exclusion`- oder eines `without`-Containers bei der Verwendung von `AND/OR`. Bei Verwendung einer solchen Kombination werden in Data Warehouse nur Segmente unterstützt, die als `A AND NOT B` neu geschrieben werden können (oder **dieses Merkmal einbeziehen** und **dieses Merkmal ausschließen**).*
