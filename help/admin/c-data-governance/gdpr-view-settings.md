---
description: Über das Data-Governance-Dialogfeld in den Admin Tools können Sie einsehen, welche Report Suites für Data Governance konfiguriert wurden, ob sie einer Experience Cloud-Organisation zugeordnet wurden und ob für die entsprechende Report Suite eine Richtlinie zur Datenaufbewahrung vorhanden ist.
title: Data-Governance-Einstellungen von Report Suites anzeigen/verwalten
feature: Data Governance
exl-id: 87b0be42-1098-4e72-8eb8-0c1bb56791f8
source-git-commit: f6199620033af9c8e304bd0f537d4e0b052ed64d
workflow-type: ht
source-wordcount: '486'
ht-degree: 100%

---

# Data-Governance-Einstellungen von Report Suites anzeigen/verwalten

Über das Data-Governance-Dialogfeld in den Admin Tools können Sie einsehen, welche Report Suites für Data Governance konfiguriert wurden, ob sie einer Experience Cloud-Organisation zugeordnet wurden und ob für die entsprechende Report Suite eine Richtlinie zur Datenaufbewahrung vorhanden ist.

1. Melden Sie sich bei Adobe Experience Cloud an.
1. Öffnen Sie **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Data Governance]**.

   Hier werden Ihnen die Report Suites des Anmeldeunternehmens angezeigt:

   ![](assets/privacy_setup_an.png)

<table id="table_448292730FF0475E9DCB731882F9A29B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Einstellung </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Report Suites </p> </td> 
   <td colname="col2"> <p>Die erste Zeile enthält den Anzeigenamen der Report Suite. Die zweite Zeile enthält den internen Namen der Report Suite. Wenn Sie Beschriftungen für eine Report Suite festlegen dürfen, befindet sich in der ersten Zeile ein Link, auf den Sie klicken können und über den Sie zur Beschriftungsseite gelangen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Organisationszuordnung </p> </td> 
   <td colname="col2"> 
    <ul id="ul_EF8F613B0C5E42D19DB60BD0C89C114B"> 
     <li id="li_B35EE88555F547EFBF55ADE9D0C9EC3B"><b>Zugeordnet</b>: Diese Report Suite wurde bereits derselben Experience Cloud-Organisation wie das Analytics-Anmeldeunternehmen zugeordnet, bei dem Sie angemeldet sind. Es können nur Report Suites mit dieser Einstellung beschriftet werden. </li>
     <li id="li_FF825A65D089487BBF5FCB0D74D41CD7"><b>Einer anderen Organisation zugeordnet</b>: Diese Report Suite wurde bereits einer anderen Experience Cloud-Organisation zugeordnet. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Richtlinie zur Datenaufbewahrung </p> </td> 
   <td colname="col2"> <p>Für die Datenschutzimplementierung in Analytics müssen Sie eine Richtlinie zur Datenaufbewahrung erstellen. </p> <p>Diese Einstellung zeigt: </p> 
    <ul> 
     <li>ob eine Richtlinie zur Datenaufbewahrung für die entsprechende Report Suite vorhanden ist und </li> 
     <li>wie lange die Daten von Adobe aufbewahrt werden, bis sie gelöscht werden. Standardmäßig beträgt der Aufbewahrungszeitraum 25 Monate. </li> 
    </ul> <p>Hinweis: Adobe Analytics kann Sie bei der Verarbeitung von Anfragen an die Datenschutz-API – also bei der Verarbeitung von Zugriffs- oder Löschanfragen, die Sie von Ihren Endbenutzern erhalten – nicht unterstützen, wenn kein Zeitraum zur Datenaufbewahrung festgelegt wurde. Wenden Sie sich an Ihren Customer Success Manager, um den Zeitraum der Datenaufbewahrung festzulegen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gruppen </p> </td> 
   <td colname="col2"> <p>Die Gruppierungsfunktionalität ist derzeit nicht implementiert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Linke Sidebar </p> </td> 
   <td colname="col2"> <p>Klicken Sie auf das Trichtersymbol, um die Sidebar zu öffnen oder zu schließen. </p> <p>Im Bereich „Organisationszuordnung“ wird die Anzahl Report Suites angezeigt, die in die einzelnen beschriebenen Kategorien fallen. </p> <p>Im Bereich „Richtlinie zur Datenaufbewahrung“ werden die eindeutige momentan für Ihre Organisation verwendete Datenaufbewahrungsrichtlinie sowie die Anzahl Report Suites angezeigt, die dieser Aufbewahrungsrichtlinie zugeordnet wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>In CSV exportieren </p> </td> 
   <td colname="col2"> <p>Wenn Sie das Kontrollkästchen neben einer oder mehreren Report Suites aktivieren, wird die Option <span class="uicontrol">In CSV exportieren</span> angezeigt. Mithilfe dieser Option können Sie eine CSV-Datei mit allen aktuellen Beschriftungsdefinitionen für sämtliche Variablen aller ausgewählten Report Suites herunterladen. </p> <p>Es wird empfohlen, dass Ihre Rechtsabteilung die Beschriftungseinstellungen überprüft. Diese Überprüfung wird mithilfe dieser Option vereinfacht. Statt die Überprüfung durchführen zu müssen, während Sie bei der Data-Governance-Benutzeroberfläche angemeldet sind, können Sie einfach die CSV-Datei weitergeben. </p> <p><img placement="break"  src="assets/export_csv.png" width="300px" id="image_5FE821B2D07B402D8E0F6FE53D6FC52E" /> </p> </td> 
  </tr> 
 </tbody> 
</table>
