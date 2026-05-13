---
description: Report Builder verwendet den benutzerdefinierten Analytics-Kalender. Sie können den Kalender verwenden, um den ersten Wochentag und das erste Jahr zu definieren, oder einen anderen Einzelhandelskalenderstil verwenden. Die Kalenderformate werden für verschiedene Zwecke verwendet, einschließlich Verkaufsvergleich und Prognosestandardisierung, Lohnkostenanalyse oder Regulierung der Inventuranzahl.
title: Benutzerdefinierter Kalender
feature: Report Builder
role: User, Admin
exl-id: e65cb6c8-8bb0-4dcd-a3a3-d22adcd024fa
TQID: https://experienceleague.adobe.com/At3YiOPV0jx5WXwe-VvA05n3yIEmiAJIRzoOoeISeA4
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 409
ht-degree: 15%

---

# Benutzerdefinierter Kalender

{{legacy-arb}}

Report Builder verwendet den benutzerdefinierten Analytics-Kalender. Sie können den Kalender verwenden, um den ersten Wochentag und das erste Jahr zu definieren, oder einen anderen Einzelhandelskalenderstil verwenden. Die Kalenderformate werden für verschiedene Zwecke verwendet, einschließlich Verkaufsvergleich und Prognosestandardisierung, Lohnkostenanalyse oder Regulierung der Inventuranzahl.

Nachfolgend werden die einzelnen Kalenderformate beschrieben.

<table id="table_E609632569EB499184E56618C2CEF742"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Kalender </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Gregorianischer Kalender </p> </td> 
   <td colname="col2"> <p> Verwendet das herkömmliche Kalenderformat (Januar bis Dezember, mit 30 oder 31 Tagen und einer variablen Anzahl von Wochen pro Monat). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Modifizierter gregorianischer Kalender </p> </td> 
   <td colname="col2"> <p> Verwendet den traditionellen gregorianischen Kalender, ermöglicht jedoch die Auswahl des ersten Monats des Jahres und des ersten Wochentags. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4-5-4 Einzelhandelskalender </p> </td> 
   <td colname="col2"> <p> Schlüsselt jeden Monat nach der Anzahl der Wochen im Monat auf. Der Januar hat also vier Wochen und so weiter. Die National Retail Federation verwendet das Kalenderformat 4-5-4. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Benutzerdefinierter Kalender </p> </td> 
   <td colname="col2"> <p> Bietet drei Formate, die auf der Anzahl der Wochen in jedem Monat basieren. Die Anzahl der Wochen in jedem Monat hängt vom ausgewählten ersten Tag des Jahres ab. </p> <p>Ein Jahr hat 52 Wochen. Teilen Sie das auf 4 Quartale auf und Sie bekommen 13 Wochen pro Quartal. Aber es gibt drei Monate in einem Quartal. Die Zahl 13 ist nicht durch 3 teilbar. Folglich muss die restliche Woche aus Konsistenzgründen zu einem der Monate hinzugefügt werden. 5/4/4 bedeutet, dass der 1. Monat des Quartals die zusätzliche Woche hat. 4/5/4 bedeutet, dass der 2. Monat die zusätzliche Woche hat usw. Im Kalender 5-4-4 wird die 53. Woche zum letzten Quartal des Jahres hinzugefügt. </p> 
    <ul id="ul_1579FD106A47419486B03E248A5E6ED5"> 
     <li id="li_E9B9E8F03E324DBDA9139C2D0D599092"><b>4-5-</b>:Januar hat vier Wochen, Februar hat fünf Wochen, März hat vier Wochen usw. </li> 
     <li id="li_D0675DBDEC4641D2A8645B5CDFC565AB"><b>4-4-</b>: Januar hat vier Wochen, Februar hat vier Wochen, März hat fünf Wochen usw. </li> 
     <li id="li_6743BBB9AC9A4CFEAA0CBCE51052BC29"><b>5-5-</b>: Januar hat fünf Wochen, Februar hat fünf Wochen, März hat vier Wochen usw. </li> 
    </ul> <p>Hinweis: Diese Kalenderoption wird in allen Adobe Analytics-Tools unterstützt: Analysis Workspace, Report Builder und Activity Map. Die Ausnahme ist Data Warehouse, wo benutzerdefinierte Kalender nicht unterstützt werden. </p> </td> 
  </tr> 
 </tbody> 
</table>
