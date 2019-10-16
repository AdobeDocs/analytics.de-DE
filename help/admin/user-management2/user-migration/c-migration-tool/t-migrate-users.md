---
description: Migrieren Sie Benutzer aus dem vormaligen Analytics User Management-System in die Adobe Admin Console.
seo-description: Migrieren Sie Benutzer aus dem vormaligen Analytics User Management-System in die Adobe Admin Console.
seo-title: Migrieren von Analytics-Benutzerkonten für Adobe IDs
title: Migrieren von Analytics-Benutzerkonten für Adobe IDs
uuid: 734e9f14-ef8d-44de-8ff3-3ee6dfe0a214
translation-type: tm+mt
source-git-commit: 45e3330adb562ec795d287ae1c1fa6b03a2b2a31

---


# Migrieren von Analytics-Benutzerkonten für Adobe IDs{#migrate-analytics-user-accounts-for-adobe-ids}

Migrieren Sie Benutzer aus dem vormaligen Analytics User Management-System in die Adobe Admin Console.

## Migrieren von Analytics-Benutzerkonten für Adobe IDs {#task-f3355f3b14a340feae58cfa04c0ba1c9}

Migrieren Sie Benutzer aus dem vormaligen Analytics User Management-System in die Adobe Admin Console.

>[!NOTE]
>
>Wenn ein Administrator, der nicht über Experience Cloud angemeldet ist, versucht, auf das Tool zur Migration von Benutzer-IDs zuzugreifen, wird er zur Experience Cloud-Anmeldeseite weitergeleitet.

**Migration von Analytics-Benutzern**

1. Navigieren Sie zu **Analytics** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Benutzer-ID-Migration]**.

   ![](assets/migration-progress.png)

   Die Seite zur Migration von Benutzer-IDs besteht aus zwei Abschnitten: *Migrationsprozess* und *Benutzerdaten*.

   **Migrationsprozess**

<table id="table_F9F1CFF762C745E198CB075A02BA2DDA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Phase </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Migration abgeschlossen </p> </td> 
   <td colname="col2"> <p>Die Benutzer haben die Einladung angenommen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bisherige Anmeldedaten deaktiviert </p> </td> 
   <td colname="col2"> <p>Die bisherigen Anmeldedaten mit Unternehmens-ID wurden deaktiviert. Benutzer greifen nun mit ihrer Adobe ID oder Enterprise ID auf die Experience Cloud zu. Wenn alle Ihre Benutzer diese Phase erreicht haben, ist die Migration abgeschlossen. </p> <p>Bei der Migration ist die Legacy-Anmeldung deaktiviert. Benutzer werden zu " <span class="filepath"> experiencecloud.adobe.com</span> "umgeleitet und müssen sich mit der Adobe ID oder Enterprise ID anmelden. </p> <p>See <a href="/help/admin/user-management2/user-migration/c-migration-tool/t-disable-legacy-login.md" format="dita" scope="local"> Disable Legacy Logins</a> for more information. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Benutzerdaten**

Die Benutzerdaten zeigen die Benutzer in Ihrer Organisation an, getrennt durch den Domänennamen.

<table id="table_3822E27AF81E4A188562FEB5131548A5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Domäne </p> </td> 
   <td colname="col2"> <p>Domänen beziehen sich auf die E-Mail-IDs der aktuellen Analytics-Benutzerbasis. Eine Domäne kann nur von einem einzigen Unternehmen und nur durch Systemadministratoren in Anspruch genommen werden. Weitere Informationen finden Sie unter <a href="https://helpx.adobe.com/enterprise/help/request-access-to-claimed-domain.html" format="html" scope="external">Zugriff auf eine beanspruchte Domäne anfordern</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Domäne angefordert </p> </td> 
   <td colname="col2"> <p>Wenn Sie Benutzer als Enterprise- oder Federated IDs migrieren möchten, müssen Sie Systemadministrator sein und eine verfügbare Domäne über die Admin Console anfordern, bevor Sie Benutzer migrieren können. <a href="https://helpx.adobe.com/enterprise/help/identity.html" format="html" scope="external">Weitere Informationen</a>. </p> <p>Wenn Sie keine Domänen für Enterprise- oder Federated IDs anfordern möchten, überspringen Sie diesen Schritt und migrieren Sie Benutzer als Adobe IDs. Erfahren Sie <a href="https://helpx.adobe.com/enterprise/help/identity.html" format="html" scope="external">hier</a> mehr über ID-Arten. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Locate the domain containing the user IDs you want to migrate, then, under **[!UICONTROL Requiring Migration]**, click **[!UICONTROL Select Users]**.
1. On the [!DNL Users] page, select the users you want to migrate, then click **[!UICONTROL Migrate]**.

   When you click **[!UICONTROL Migrate]**, users receive an invitation (Migration Initiated) and must accept it. Dadurch wird die Benutzer-ID in die Kategorie „Migration abgeschlossen“ verschoben. Sie können die bisherigen [!DNL my.omniture.com]-Anmeldedaten dann deaktivieren.

   ![](assets/user-info.png)

1. Geben Sie die Art der ID an, die Sie für die Migration der Benutzer verwenden möchten ([Adobe ID oder Enterprise ID](https://helpx.adobe.com/enterprise/help/identity.html)).

   After migrating users, the status under the column Migration Status changes from *`Not Initiated`* to *`Migrated`*.

   If *`Failed`* displays, hover over the icon for a description about why the migration failed.
