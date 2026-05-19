---
description: Migrieren Sie Benutzer aus dem vormaligen Analytics User Management-System in die Admin Console.
title: Migrieren von Analytics-Benutzerkonten für Adobe IDs
feature: Admin Tools
exl-id: 198367a1-8156-4cc3-af8a-d92c61699eda
role: Admin
TQID: https://experienceleague.adobe.com/bD-qiEI3KbDBNe4aO01-MqzjoZ-OMcGAnd9vnMTBmZs
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
subfeature_v2:
  - id: d124af73-4061-4b84-9063-ae2b60f2c1f3
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: c2ae876122715b4fa6367326dc23479dd9648021
workflow-type: tm+mt
source-wordcount: 405
ht-degree: 72%

---

# Migrieren von Analytics-Benutzerkonten für Adobe IDs

Migrieren Sie Benutzer aus dem vormaligen Analytics User Management-System in die Admin Console.

>[!NOTE]
>
>Wenn ein Administrator, der nicht bei CX Enterprise angemeldet ist, versucht, auf das Tool für die Benutzer-ID-Migration zuzugreifen, wird er zur Anmeldeseite von CX Enterprise weitergeleitet.

1. Navigieren Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Benutzer-ID-Migration]**.

   ![](/help/admin/tools/user-management/user-migration/assets/migration-progress.png)

   Die Seite „Benutzer-ID-Migration“ *zwei Abschnitte:* und *Benutzerinformationen*.

## Migrationsfortschritt

<table id="table_F9F1CFF762C745E198CB075A02BA2DDA"> 
   <thead> 
   <tr> 
      <th colname="col1" class="entry"> Phase </th> 
      <th colname="col2" class="entry"> Beschreibung </th> 
   </tr>
   </thead>
   <tbody> 
   <tr> 
      <td colname="col1"> <p>Migrationen abgeschlossen </p> </td> 
      <td colname="col2"> <p>Die Benutzer haben die Einladung angenommen. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>Legacy-Anmeldung deaktiviert </p> </td> 
      <td colname="col2"> <p>Ältere Anmeldedaten mit einer Unternehmens-ID sind deaktiviert. Anwender greifen jetzt über ihre Adobe ID oder Enterprise ID auf CX Enterprise zu. Wenn alle Benutzer diese Phase erreicht haben, ist die Migration abgeschlossen. </p> <p>Bei der Migration ist die bisherige Anmeldung deaktiviert. Benutzer werden zu <span class="filepath">experiencecloud.adobe.com</span> umgeleitet und müssen sich mit der Adobe ID oder Enterprise ID anmelden. </p> </td> 
   </tr> 
   </tbody> 
   </table>

## Benutzerinformationen

In den Benutzerinformationen werden die Benutzer in Ihrer Organisation, getrennt nach Domain-Namen, aufgeführt.

<table id="table_3822E27AF81E4A188562FEB5131548A5"> 
<thead> 
<tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
</tr>
</thead>
<tbody> 
<tr> 
   <td colname="col1"> <p>Domain </p> </td> 
   <td colname="col2"> <p>Domains sind spezifisch für die E-Mail-IDs der aktuellen Analytics-Benutzerbasis. Eine Domain kann nur von einem einzigen Unternehmen und nur durch Systemadministratoren in Anspruch genommen werden. Weitere Informationen finden Sie unter <a href="https://helpx.adobe.com/de/enterprise/help/request-access-to-claimed-domain.html">Anfordern des Zugriffs auf eine beanspruchte Domain</a>. </p> </td> 
</tr> 
<tr> 
   <td colname="col1"> <p>Domain angefordert </p> </td> 
   <td colname="col2"> <p>Wenn Sie Benutzende als Enterprise- oder Federated IDs migrieren möchten, müssen Sie Systemadministrator bzw. Systemadministratorin sein und eine verfügbare Domain über die Adobe Admin Console anfordern, bevor Sie Benutzende migrieren können. <a href="https://helpx.adobe.com/de/enterprise/help/identity.html">Weitere Informationen</a>. </p> <p>Wenn Sie keine Domänen für Enterprise- oder Federated IDs anfordern möchten, überspringen Sie diesen Schritt und migrieren Sie Benutzer als Adobe IDs. Erfahren Sie <a href="https://helpx.adobe.com/de/enterprise/help/identity.html">hier</a> mehr über ID-Typen. </p> </td> 
</tr> 
</tbody> 
</table>

1. Suchen Sie nach der Domain, die die zu migrierenden Benutzer-IDs enthält, und klicken Sie dann unter **[!UICONTROL Migration erforderlich]** auf **[!UICONTROL Benutzer auswählen]**.
1. Wählen Sie auf der Seite „[!DNL Users]“ die Benutzer aus, die Sie migrieren möchten, und klicken Sie dann auf **[!UICONTROL Migrieren]**.

   Wenn Sie auf **[!UICONTROL Migrieren]** klicken, erhalten Benutzer eine Einladung (die Migration wird initiiert) und müssen diese annehmen. Dadurch wird die Benutzer-ID in die Kategorie „Migration abgeschlossen“ verschoben. Sie können dann die bisherigen `[!DNL my.omniture.com].`-Anmeldedaten deaktivieren

   ![](/help/admin/tools/user-management/user-migration/assets/user-info.png)

1. Geben Sie den Typ der ID an, die Sie für die Migration der Benutzer verwenden möchten (Adobe ID oder Enterprise ID)

   Nach der Migration von Benutzern ändert sich der Wert in der Spalte „Migrationsstatus“ von *`Not Initiated`* auf *`Migrated`*.

   Wenn *`Failed`* angezeigt wird, fahren Sie mit dem Maus über das Symbol, um den Grund für das Fehlschlagen der Migration anzuzeigen.
