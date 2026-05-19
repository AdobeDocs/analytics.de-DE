---
description: Was Sie über die Migration der Analytics-Benutzer-ID zum Admin Console in Adobe CX Enterprise wissen müssen.
title: Analytics-Benutzermigration zur Admin Console
feature: Admin Tools
exl-id: f4bc0e92-af53-40db-8138-44d29e4b25fe
role: Admin
TQID: https://experienceleague.adobe.com/bCf6DWIpIVALcGPAi3tL8zlZ5V8lzPR-9XNCm4HuFnY
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7id: fd307ce7-56f5-4ee3-af68-a7833ff6e85eid: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
subfeature_v2: id: ac8a38fa-dec3-4581-8f64-178fde9f64e8id: d124af73-4061-4b84-9063-ae2b60f2c1f3id: e499b847-6dc4-408a-9f0b-70d35ce9b711id: ef60b66e-5984-4336-ba72-6d978b1b6f87id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 9e2c89f4188c723b4623a6e7859b74ede15e155b
workflow-type: tm+mt
source-wordcount: 2960
ht-degree: 52%

---

# Analytics-Benutzermigration zur Adobe Admin Console{#analytics-user-migration-to-the-admin-console}

Was Sie über die Migration der Analytics-Benutzer-ID zum Adobe Admin Console in Adobe CX Enterprise wissen müssen.

Generelle Hilfestellung zu Adobe Admin Console-Themen (nicht in Bezug auf die Analytics-Migration) finden Sie im [Admin Console-Benutzerhandbuch](https://helpx.adobe.com/de/enterprise/administering/user-guide.html).

Nach der Migration können Sie [CX Enterprise-Benutzer und -Produkte](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=de) in der Adobe Admin Console verwalten.

## Was ist die Migration der Analytics-Benutzer-ID? {#section-adbe49aba10c4e62afa836a97894107c}

Die Migration der Analytics-Benutzer-ID ermöglicht es Admins, Benutzerkonten einfach vom Analytics User Management zur Adobe Admin Console zu migrieren. Nachdem Ihre Benutzer migriert wurden, haben sie Zugriff auf die Lösungen und zentralen Services, die in CX Enterprise verfügbar sind. Die Migration wird schrittweise für Kunden eingeführt.

Vorteile der Verwendung der Adobe Admin Console sind unter anderem:

<table id="table_E4465796E224474680D750CAC5434ED3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Vorteil </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Single Sign-on </p> </td> 
   <td colname="col2"> <p>Analytics-Anwender können sich mit ihrem Adobe ID oder Enterprise ID bei CX Enterprise und allen Lösungen anmelden. Diese Anmeldung ermöglicht den Zugriff auf integrierte Lösungen und zentrale Services in CX Enterprise. </p> <p>Nach der Migration werden Benutzer, die versuchen, sich über die bisherigen Anmeldedaten anzumelden (<span class="filepath">my.omniture.com</span> und <span class="filepath">sc.omniture.com</span>), an <span class="filepath">experiencecloud.adobe.com</span> weitergeleitet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Benutzeridentität und -berechtigungen verwalten </p> </td> 
   <td colname="col2"> <p>Analytics-Administratoren können Benutzer und Berechtigungen ausschließlich in der <a href="https://adminconsole.adobe.com/enterprise/">Admin Console</a> verwalten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Produkte und zentrale Services verwalten </p> </td> 
   <td colname="col2"> 
    <ul id="ul_01043FEF271E4B27BF34980D629D1932"> 
     <li id="li_DC31AE8BAAB843F39A7CC9EB047265D5">Neue Benutzer einladen </li> 
     <li id="li_73724DD7D79E41F8A1D58C74E37674BA">Anlegen von Produktprofilen </li> 
     <li id="li_7E75FC68E0F84873A9A211D2707B6DE7">Gewähren von Benutzerberechtigungen für bestimmte Produkte und Services </li> 
     <li id="li_9C8A340A7C9A45A98EC0BD4AF9E100FF">Zugriff auf <a href="https://experienceleague.adobe.com/docs/core-services/interface/experience-cloud.html?lang=de"> lösungsübergreifende Core Services, </a> in Adobe CX Enterprise verfügbar sind </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Was man vor der Migration von Benutzer-IDs wissen (und tun) sollte (Häufig gestellte Fragen) {#section-b0fc7f0bbd4b488e95b0c8e77ff077a9}

Antworten auf Fragen, die Sie vielleicht vor der Migration haben.

<table id="table_36FD7EF1DAB44D359F4FC186D93147E5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Frage/Aufgabe </th> 
   <th colname="col2" class="entry"> Antwort </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Ich bin Analytics-Admin und habe eine E-Mail vor der Migration erhalten. Was muss ich zuerst tun? </p> </td> 
   <td colname="col2"> <p>Stellen Sie sicher, dass Sie über eine Adobe ID verfügen und auf die <a href="https://adminconsole.adobe.com/enterprise/"> CX Enterprise Admin Console</a> zugreifen können. </p> <p>Wenden Sie sich andernfalls an die <a href="https://helpx.adobe.com/de/marketing-cloud/contact-support.html">Adobe-Kundenunterstützung</a>. (Sie sollten sich zunächst an Ihren System- oder Produktadministrator wenden, um eine Einladung zur entsprechenden Organisation zu erhalten.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>AEM-Integrationen mit Analytics </p> </td> 
   <td colname="col2"> <p> AEM-Benutzer mit einer Analytics-Integration müssen ihre Konfiguration ändern, um das gemeinsame Analytics-Geheimnis anstelle des Kennworts zu verwenden. </p> <p> Sie sollten dies tun, bevor die Migration aktiviert wird. Sobald die Migration deaktiviert ist, ist das ursprünglich konfigurierte Kennwort nicht mehr gültig. </p> <p><b>Abrufen des gemeinsamen Geheimnisses in Analytics</b> </p> <p> Der gemeinsam genutzte geheime Schlüssel kann von Analytics (<span class="uicontrol">Analytics</span> &gt; <span class="uicontrol">Benutzerverwaltung</span>) bezogen werden und ist für jeden Benutzer unterschiedlich. </p> <p><b>Aktualisieren Ihrer AEM-Konfiguration mit dem gemeinsam genutzten geheimen Schlüssel</b> </p> <p>Sehen Sie <a href="https://helpx.adobe.com/de/experience-manager/6-3/sites/administering/using/adobeanalytics-connect.html">Verbinden mit Adobe Analytics und Erstellen von Frameworks</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Report Builder aktualisieren </p> </td> 
   <td colname="col2"> <p> <p>Wichtig: Aktualisieren Sie Ihre Installation von <a href="/help/analyze/report-builder/report-builder-setup.md">Report Builder</a> auf die neueste Version. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wann beginnt die Migration? </p> </td> 
   <td colname="col2"> <p>Adobe benachrichtigt Analytics-Administratoren per E-Mail mit Anweisungen, wann die Migration beginnen wird. </p> <p>Migrationen zur Adobe Admin Console werden in Schüben durchgeführt. Am Tag der Migration benachrichtigt Adobe Analytics-Administratoren und gewährt ihnen Zugriff auf das Migrations-Tool. Nachdem ein Anmeldeunternehmen die für jede Migrationswelle definierten Kriterien erfüllt, wird Adobe: </p> 
    <ul id="ul_D7DDC62A08AB4407B122985EDEA6ABD1"> 
     <li id="li_BA0AD50DCDC14C90ADD513DEF6F78180">Legen Sie das Start- und Enddatum für die Migration des Unternehmens fest. </li> 
     <li id="li_C048A5C64FAA46C4BB41EF24F1CEDF62">Senden Sie ca. 30 Tage vor der Migration eine E-Mail-Benachrichtigung an die aktuellen Analytics-Administratoren des Unternehmens. </li> 
     <li id="li_476265B24CE2404B995201170C75D674">Zeigen Sie eine Benachrichtigung im Produkt an, die Admins über das Startdatum der Migration informiert. </li> 
    </ul> <p> Am Tag der Migration werden Ihre vorherigen Berechtigungsgruppen automatisch in die Adobe Admin Console kopiert. Sie können dann in den Analytics Admin Tools keine Benutzer mehr einladen und keine neuen Gruppen mehr erstellen. </p> <p>Nach der Migration: </p> 
    <ul id="ul_4639963EB08F407F8C18ACE2B3D30223"> 
     <li id="li_7F24A3FC900146C3B2E988D399C859EA">Administrierende verwenden die Adobe Admin Console zur Verwaltung der Analytics-Benutzenden und -Berechtigungen. (Sie verwenden nicht mehr die Benutzeroberfläche zur Benutzerverwaltung unter Analytics &gt; Admin &gt; User Management.) </li> 
     <li id="li_5B5234D4F94A4B96A8920F6A5831A64C">Anwender können über CX Enterprise auf Analytics zugreifen, indem sie ihre Adobe oder Enterprise ID anstelle von my.omniture.com <span class="filepath"></span>. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Was geschieht am Startdatum der Migration? </p> </td> 
   <td colname="col2"> <p>Um 10:00 Uhr UTC am Startdatum der Migration: </p> 
    <ul id="ul_25D1DBDF5C804D048E741F31550FF5F3"> 
     <li id="li_418476105FE341229CE146E730AAB33D">Ihre in Analytics vorhandenen Berechtigungsgruppen werden automatisch in der Adobe Admin Console als Produktprofile repliziert, inklusive ihrer Beschreibungen und granularen Berechtigungen in verschiedenen Report Suites, Metriken, Analytics und Report Suite-Werkzeugen. </li> 
     <li id="li_412F88C454B0455A8F3BC8016226855C">Wurden aktuelle Analytics-Besuchende in der Adobe Admin Console erstellt (also mit verknüpfter Adobe/Enterprise ID), werden sie den entsprechenden Produktprofilen in der Adobe Admin Console hinzugefügt. </li> 
     <li id="li_8A05137EC05C4FD5910E73FE58300DCB">Der Abschnitt „User Management“ auf der Registerkarte „Admin“ in Analytics wird auf <span class="term"> Schreibgeschützt festgelegt</span>. Sie werden nicht mehr in der Lage sein, neue Benutzende oder Berechtigungsgruppen hier zu erstellen, und müssen diese Funktionen über die Adobe Admin Console nutzen. Weitere Informationen dazu finden Sie unter <a href="/help/admin/tools/user-management/user-migration/c-migration-tool.md#section-928ffba27a0446e0af575b720434ef56">Nicht unterstützte Analytics-Funktionen in der Adobe Admin Console</a>. </li> 
     <li id="li_2742DE69E9B547198A58E1F33E908361">Als Administrator erhalten Sie Zugriff auf das Werkzeug zur <a href="/help/admin/tools/user-management/user-migration/c-migration-tool.md">Benutzer-ID-Migration</a>. Außerdem erscheint im Produkt selbst eine Benachrichtigung, die das Enddatum der Migration (in der Regel 60 Tage später) sowie Links zu Hilfeinhalten und FAQs enthält. </li> 
     <li id="li_095D42E3A3544FC59A60A8C8F94C971B">Sie erhalten Zugriff auf die Registerkarte „Berechtigungen“ in der Adobe Admin Console, über die Sie Produktprofile mit all den granularen Optionen erstellen können, die Sie von Analytics kennen. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wie funktioniert die Migration von Benutzer-IDs? </p> </td> 
   <td colname="col2"> <p> Klicken Sie auf der Admin-Seite unter „User Management“ auf <a href="/help/admin/tools/user-management/user-migration/t-migrate-users.md#task-f3355f3b14a340feae58cfa04c0ba1c9">Benutzer-IDs migrieren</a>. Verwenden Sie das Tool, um Benutzende zu Produktprofilen in der Adobe Admin Console hinzuzufügen (repliziert aus Berechtigungsgruppen in Analytics). Sie können Benutzer-IDs in Ihrem eigenen Tempo migrieren. </p> <p>Es sind Administratorrechte erforderlich. Nach Abschluss der Migration kann diese nicht mehr rückgängig gemacht werden. </p> <p>Am Enddatum der Migration wird der Zugriff auf <span class="filepath">my.omniture.com</span> für Benutzer innerhalb ihres angemeldeten Unternehmens deaktiviert. Benutzer (einschließlich derjenigen, die noch migriert werden müssen) werden über die neue CX Enterprise-URL zur Anmeldung weitergeleitet (<span class="filepath"> experiencecloud.adobe.com</span>) </p> <p>Hinweis: Adobe empfiehlt, vor der Migration die Gelegenheit für eine Prüfung Ihrer Benutzer und Gruppen zu nutzen. Löschen Sie alte und nicht verwendete Konten sowie solche, die keinen Zugriff mehr auf das Produkt haben sollten (z. B. Mitarbeiter, die nicht mehr im Unternehmen arbeiten). </p> <p>Verwandtes Thema: <a href="/help/admin/tools/user-management/user-migration/migrate-enterprise.md">Migrieren von Analytics-Benutzerkonten für Enterprise und Federated IDs</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wirkt sich die Migration auf meine Analytics-Implementierung aus oder auf die Art und Weise, wie Daten erfasst werden? </p> </td> 
   <td colname="col2"> <p>Nein. </p> <p>Das Migrations-Tool unterstützt Sie beim Übergang von Benutzer-IDs und Berechtigungen von Analytics User Management auf die <a href="https://adminconsole.adobe.com/enterprise/"> CX Enterprise Admin Console</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wie lange dauert der Migrationsprozess? </p> </td> 
   <td colname="col2"> <p>Alle aktuellen Analytics-Administratoren erhalten vier Wochen vor der Migration eine E-Mail mit einer Benachrichtigung zur Vorabmigration. (Das tatsächliche Startdatum wird in der Analytics-Benutzeroberfläche angezeigt.) </p> <p>Zu Beginn der Migration haben Administratoren 60 Tage Zeit, um den Prozess abzuschließen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kann ich meine Migration beschleunigen? </p> </td> 
   <td colname="col2"> <p>Ja. Adobe empfiehlt jedoch, die Zeit zu verwenden, bevor die Migration beginnt: </p> 
    <ul id="ul_52C7EC44A5534975BFD7A6F37A829C25"> 
     <li id="li_8CFFF72877E8456DAC3241143AD648AD">Stellen Sie sicher, dass Sie ein Analytics-Produktadministrator bzw. eine Analytics-Produktadministratorin in der Adobe Admin Console sind. </li> 
     <li id="li_25DAA8D1EEDA45A0B5B59472BD8896C4">Kommunizieren Sie Ihrer Benutzerbasis, dass sich ihr Anmeldeerlebnis ändern wird, wenn die Migration beginnt. </li> 
     <li id="li_5B50F942F6A8483FAFA500AFF428702C">Überprüfen Sie Ihre aktuellen Benutzer und Berechtigungen und führen Sie Bereinigungsaktivitäten durch. </li> 
    </ul> <p>Um Ihre Migration zu beschleunigen, wenden Sie sich an Ihr Adobe-Account-Team bei <a href="https://helpx.adobe.com/de/marketing-cloud/contact-support.html"> Adobe-</a> und fordern Sie ein früheres Startdatum an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Ich bin ein Analytics-Administrator bzw. eine Analytics-Administratorin ohne Zugriff auf die Adobe Admin Console. Wie erhalte ich Zugriff darauf? </p> </td> 
   <td colname="col2"> <p>Alle System- oder Produktadministrierenden, die Zugriff auf die Adobe Admin Console Ihrer Organisation haben, können Ihnen Zugriff gewähren. Wenn Sie sich nicht sicher sind, wer in Ihrer Organisation über Administratorberechtigungen in der Konsole verfügt, wenden Sie sich an die <a href="https://helpx.adobe.com/de/marketing-cloud/contact-support.html">Adobe-Kundenunterstützung</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kann ich das Startdatum der Migration verschieben? </p> </td> 
   <td colname="col2"> <p>Ja. Wenden Sie sich an die <a href="https://helpx.adobe.com/de/marketing-cloud/contact-support.html">Adobe-Kundenunterstützung</a>. </p><p>Im Folgenden finden Sie eine Beschreibung der Änderungen an Ihrer Analytics-Benutzer- und -Berechtigungsverwaltung am Startdatum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Mein Unternehmen migriert nun zur Adobe Admin Console. Wo erstelle ich jetzt Benutzende und Berechtigungsgruppen vor dem Start der Migration? </p> </td> 
   <td colname="col2"> <p>Vor dem Startdatum der Migration können Sie Benutzende in der Adobe Admin Console oder unter Analytics &gt; User Management erstellen. </p> <p>Nach Beginn der Migration können Sie Benutzende und Berechtigungsgruppen nur noch in der Adobe Admin Console erstellen. </p><p>Weitere Informationen dazu, was am Startdatum der Migration geschieht, finden Sie im Abschnitt „Migration“ weiter unten. </p>
   </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Wann kann ich Single Sign-on mit Federated IDs implementieren? </p> </td> 
   <td colname="col2"> <p> In Kürze wird in der Adobe Admin Console ein Werkzeug zur Verfügung stehen, mit dem Sie ID-Typen von Adobe IDs in Federated IDs ändern können. Während der Migration können Benutzer nicht als Federated IDs migriert werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Informationen während der Migration (FAQ) {#section-d394524aa6d046d79025bbd7499792bc}

Wichtige Informationen zum Migrationsprozess und dessen Auswirkungen auf die aktuelle Benutzerverwaltung.

<table id="table_0E37BB1DEA6143F0B5F4E861FCFA7189"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Frage </th> 
   <th colname="col2" class="entry"> Antwort </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Wie werden Berechtigungsgruppen in der Adobe Admin Console repliziert? Was geschieht mit meinen Benutzenden? </p> </td> 
   <td colname="col2"> <p>Eine migrierte Analytics-Gruppe wird in der Adobe Admin Console <i>Produktprofil</i> genannt. Die Berechtigungseinstellungen für die ursprüngliche Gruppe werden bei der Migration beibehalten. Die der Gruppe zugewiesenen Benutzer werden jedoch nicht migriert. Wenn ein Benutzer, der zu dieser Gruppe gehört, mithilfe des Migrations-Tools migriert wird, wird dieser Benutzer diesem Produktprofil zugewiesen. </p> <p>Beispielsweise wird eine Berechtigungsgruppe für Operationen an der Westküste, die ihre Mitglieder zu Report Builder und Analysis Workspace berechtigt (mit bestimmten Report Suites, Metriken, Dimensionen), zu einem Produktprofil für Operationen an der Westküste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kann ich den Migrationsaufwand an einen anderen Administrator delegieren? </p> </td> 
   <td colname="col2"> <p>Nach Beginn der Migration kann jeder Administrator, der über CX Enterprise auf Ihre Analytics-Instanz zugreift, das Migrations-Tool verwenden, um die Migration von Benutzern zu starten (oder fortzusetzen). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kann ich die Zugehörigkeit zu einer Berechtigungsgruppe für nicht migrierte Benutzer aktualisieren? </p> </td> 
   <td colname="col2"> <p>Ja. Sie können die Gruppenmitgliedschaft nicht migrierter Benutzer über den Abschnitt Analytics User Management ändern. </p><p>In Erwartung einer Klarstellung von Ashok darüber, wo das geschieht. </p>
   </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kann ich nach Beginn der Migration Benutzende und Berechtigungsgruppen in Analytics erstellen und sie dann mit dem Migrationswerkzeug in die Adobe Admin Console migrieren? </p> </td> 
   <td colname="col2"> <p> Nein. Nach dem Beginn der Migration müssen alle Benutzenden und Berechtigungsgruppen („Produktprofile“ in der Adobe Admin Console) in der Adobe Admin Console erstellt werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Würden Benutzern, die ich mit dem Migrations-Tool migriere, die gleichen Berechtigungen zugewiesen, die sie in Analytics hatten? </p> </td> 
   <td colname="col2"> <p>Ja. Benutzern, die mit dem Tool migriert wurden, werden die Berechtigungen gewährt, die sie derzeit in Analytics haben. Darüber hinaus behalten sie den Zugriff auf ihre Analytics-Assets (z. B. Segmente, Projekte, berechnete Metriken usw.), wenn sie über CX Enterprise auf Analytics zugreifen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Haben Benutzende, die ich in die Adobe Admin Console migriere, weiterhin Zugriff auf Analytics über <span class="filepath">my.omniture.com</span>? </p> </td> 
   <td colname="col2"> <p>Ja. Migrierte Benutzer können bis zum Enddatum der Migration mit ihrem bisherigen Benutzernamen und Passwort über <span class="filepath">my.omniture.com</span> auf Analytics zugreifen, außer Sie deaktivieren den Zugriff mit den bisherigen Anmeldedaten über das Migrationswerkzeug. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zwei oder mehr meiner Benutzer haben dieselbe E-Mail-ID in ihrem Analytics-Datensatz. Was passiert, wenn ich sie migriere? </p> </td> 
   <td colname="col2"> <p>Da für Benutzerkonten in der Adobe Admin Console eindeutige E-Mail-IDs erforderlich sind, wird der Fehler „Doppelte E-Mail-ID“ ausgegeben, wenn Sie mehr als einen dieser Benutzenden migrieren. Sie können die E-Mail-IDs nicht migrierter Benutzer im Abschnitt „Benutzerverwaltung (veraltet)“ aktualisieren, bevor Sie die Migration erneut versuchen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Was mache ich nach der Migration meiner Benutzer? </p> </td> 
   <td colname="col2"> <p>Deaktivieren Sie den Zugriff mit den bisherigen Anmeldedaten für <span class="filepath">my.omniture.com</span>. Sie können ältere Anmeldedaten nur deaktivieren, wenn sie migriert wurden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kann ich den Migrationsprozess verfolgen? </p> </td> 
   <td colname="col2"> <p>Das Migrationswerkzeug enthält ein Dashboard, das anzeigt, wie viele Ihrer Benutzer erfolgreich migriert wurden und wie viele von ihnen ihre bisherigen Anmeldedaten deaktiviert haben. </p> <p> Sie haben Ihr angemeldetes Unternehmen erfolgreich in die Adobe Admin Console migriert, wenn die Migration für 100 % Ihrer Benutzenden abgeschlossen wurde und deren bisherigen Anmeldedaten deaktiviert wurden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ich muss während der Migration eine Benutzer- und Berechtigungsverwaltung durchführen. Mit welchem Tool kann ich diese Aufgabe durchführen? </p> </td> 
   <td colname="col2"> <p>Nach dem Beginn der Migration verwenden Sie die Adobe Admin Console zur Erstellung und Verwaltung neuer Benutzender und Produktprofile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Was erleben meine Benutzer, wenn ich sie mithilfe des Tools migriere? </p> </td> 
   <td colname="col2"> <p>Sie erhalten eine Begrüßungs-E-Mail an die E-Mail-ID in ihrem Analytics-Benutzerdatensatz, in der sie über ihre neue Methode für den Zugriff auf Analytics über CX Enterprise informiert werden. Wenn er noch keine Adobe ID hat, wird er aufgefordert, eine zu erstellen, nach der er über seine Adobe ID auf die Lösung zugreifen kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kann ich APIs verwenden, um meine Benutzer zu migrieren, anstatt das Migrations-Tool zu verwenden? </p> </td> 
   <td colname="col2"> <p>Nein. Sie müssen das Migrationswerkzeug verwenden, um sicherzustellen, dass alle Ihre vorhandenen Benutzenden in die Adobe Admin Console migriert werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Welche Analytics-Funktionen zum User Management sind in der Adobe Admin Console nicht verfügbar? </p> </td> 
   <td colname="col2"> 
    <ul id="ul_3F3747D4C1D3420699F7D28EC0CA1AA0"> 
     <li id="li_BD943B3245FF47E7A0DDA6107EA1EF89">Asset-Übertragung </li> 
     <li id="li_2DF7004D67ED4C6CB40461EEFB038A5A">User Expiration </li> 
     <li id="li_980E3F5B98F344A492B0EBAD7F1DA60C">Benutzerprotokolle </li> 
    </ul> <p>Diese bleiben für Sie in der Analytics-Benutzerverwaltung verfügbar. </p> <p>Weitere Informationen dazu finden Sie unter <a href="/help/admin/tools/user-management/user-migration/c-migration-tool.md">Nicht unterstützte Analytics-Funktionen in der Adobe Admin Console</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wir haben verschiedene Konfigurationen in der Adobe Admin Console erstellt und sie Analytics-Berechtigungsgruppen zugeordnet. Was geschieht bei Migrationsbeginn mit diesen Konfigurationen? </p> </td> 
   <td colname="col2"> <p>Analytics-Berechtigungsgruppen werden in der Adobe Admin Console als Produktprofile wiederhergestellt, ebenso wie alle anderen Gruppen. Daher werden Ihnen in der Konsole zwei Produktprofile angezeigt, die im Grunde doppelte Berechtigungen aufweisen. Sie können doppelte Produktprofile über die Adobe Admin Console löschen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Was ist der nächste Schritt nach der Migration von Benutzenden? </p> </td> 
   <td colname="col2"> <p>Wenn Sie einen Benutzer oder einen Benutzersatz migriert haben, besteht der nächste Schritt in der Deaktivierung der bisherigen Anmeldedaten über <span class="filepath">my.omniture.com</span>. Wählen Sie dazu die entsprechenden Benutzenden im Migrationswerkzeug aus und klicken Sie auf die Kontextoption „Bisherige Anmeldedaten deaktivieren“, die oben im Fenster erscheint. Diese Option wird nur angezeigt, wenn Sie einen Benutzer bzw. eine Benutzerin oder eine Benutzergruppe auswählen, die erfolgreich in die Adobe Admin Console migriert wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Was geschieht am Enddatum der Migration? </p> </td> 
   <td colname="col2"> <p>Nach dem Enddatum der Migration (60 Tage nach Migrationsbeginn) werden alle Benutzer in Ihrem Anmeldeunternehmen über die CX Enterprise-Anmeldeseite mit ihren Adobe-IDs zur Anmeldung weitergeleitet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ich konnte bis zum Enddatum der Migration nicht alle meine Benutzer migrieren. Würden nicht migrierte Benutzer ihren Zugriff auf Analytics verlieren? </p> </td> 
   <td colname="col2"> <p>Benutzer, die bis zum Enddatum noch nicht migriert wurden, werden zur Anmeldeseite von CX Enterprise (experiencecloud.adobe.com) weitergeleitet und können nicht auf Analytics zugreifen. Allerdings haben Sie weiterhin Zugriff auf das Migrationswerkzeug. So können Sie die entsprechenden Benutzer finden und ihren Zugriff wiederherstellen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Informationen nach der Migration (FAQ) {#section-9681baa01b8c41cdb9659b73b70b50ff}

<table id="table_F48CC9DFE3424AC9AD76A16882701C8F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Frage/Problem </th> 
   <th colname="col2" class="entry"> Antworten </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Löschen von Benutzenden aus der Adobe Admin Console </p> </td> 
   <td colname="col2"> <p> In Analytics wird ein gelöschter Benutzer als <span class="term"> abgelaufen festgelegt</span> aber das Konto existiert weiterhin. Das Beibehalten des Kontos ermöglicht die Übertragung von Assets wie Segmenten, berechneten Metriken, terminierten Berichten, Projekten usw. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kontoablauf </p> </td> 
   <td colname="col2"> <p> Sie können in Analytics in den Admin Tools manuell ein Ablaufdatum für das Konto festlegen. Sobald das Ablaufdatum erreicht ist, kann der Benutzer nicht mehr auf Analytics zugreifen, sondern auf sein tatsächliches CX Enterprise-Benutzerkonto (z. B. Adobe ID, Enterprise ID, Federated ID usw.) Läuft nicht ab. Sie können sich weiterhin bei CX Enterprise anmelden, können sich aber nicht in Analytics einloggen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Nicht unterstützte Analytics-Funktionen in der Adobe Admin Console {#section-928ffba27a0446e0af575b720434ef56}

>[!IMPORTANT]
>
>Lernen Sie über die folgenden Probleme, die während der Migration bei Ihnen auftreten können.

<table id="table_88E2FA03D5F241B79AB54D12F64B51DA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Frage/Problem </th> 
   <th colname="col2" class="entry"> Antworten </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Anmelden als </p> </td> 
   <td colname="col2"> <p> Administrierende, die zur Adobe Admin Console migrieren, können die Funktion „Anmeldung als“ nicht mehr für den Zugriff auf Nicht-Admin-Benutzerkonten verwenden, die in die Adobe Admin Console migriert wurden. Diese Funktion wurde eingestellt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Benutzerablauf und Asset-Übertragung </p> </td> 
   <td colname="col2"> <p> In der Adobe Admin Console werden Benutzergültigkeit und Asset-Übertragung nicht unterstützt. Administratoren verwenden für beide Funktionen den Abschnitt „Analytics-Benutzer und Assets" unter „Admin-Tools“ in Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Letzter Zugriff (letzte Anmeldung) </p> </td> 
   <td colname="col2"> <p> Details zum letzten Anmeldezeitpunkt von Benutzenden sind unter dem Link „Analytics-Benutzer und Assets“ und nicht in der Adobe Admin Console verfügbar. Das Datum der letzten Anmeldung in Analytics bezieht sich darauf, wann Benutzer tatsächlich von CX Enterprise aus auf Analytics zugegriffen haben. Es gibt nicht das Datum und die Uhrzeit der Anmeldung bei CX Enterprise wieder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>User Management-APIs – <a href="https://helpx.adobe.com/de/enterprise/help/identity.html">von Adobe unterstützte Identitätstypen</a> </p> </td> 
   <td colname="col2"> <p> Admins, die zur Adobe Admin Console migrieren, sollten die auf Adobe Developer angebotenen User Management-APIs konfigurieren, um programmgesteuerten Zugriff auf Benutzerkonten in der Adobe Admin Console zu erhalten. </p> <p>Die Analytics-Berechtigungs-APIs werden deaktiviert, wenn Sie für die Migration aktiviert sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Web-Service-Zugriffsberechtigungen </p> </td> 
   <td colname="col2"> <p> Die Web-Service-Anmeldeinformationen für Benutzende (und ihr gemeinsam genutzter geheimer Schlüssel) sind nicht in der Adobe Admin Console verfügbar. Auf sie kann durch Klicken auf die spezifischen Benutzenden im Abschnitt „Analytics-Benutzer und Assets“ zugegriffen werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Single Sign-on </p> </td> 
   <td colname="col2"> <p> Die Analytics-Konfigurationen für einmaliges Anmelden werden entfernt, wenn Sie die Migration abgeschlossen haben. Sie bleiben während der Migration aktiv. Kunden, die Analytics Single Sign-on verwenden, sollten ein Upgrade auf <a href="https://helpx.adobe.com/de/enterprise/help/identity.html">Adobe Federated ID</a> durchführen. </p> <p>Analytics empfiehlt, die Benutzerinnen und Benutzer zunächst als Adobe IDs zu migrieren, um auf einfache Weise die CX Enterprise-Konten zu erstellen, und diese Konten dann in Federated Single Sign-Benutzerinnen und -Benutzer zu konvertieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Herunterladen von Berechtigungsgruppen </p> </td> 
   <td colname="col2"> <p> Das Herunterladen von Informationen zu Berechtigungsgruppen wird weder in den Analytics Admin Tools noch in der Adobe Admin Console mehr unterstützt. Kunden sollten die User Management-APIs von adobe.io verwenden, um Informationen zu Berechtigungsgruppen massenweise abzurufen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Erstellungsdatum des Kontos </p> </td> 
   <td colname="col2"> <p>Informationen zum Datum der Kontoerstellung werden weder in den Analytics Admin Tools noch in der Adobe Admin Console mehr unterstützt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Massen-E-Mail </p> </td> 
   <td colname="col2"> <p>Massen-E-Mails an Benutzende werden weder in den Analytics Admin-Tools noch in der Adobe Admin Console weiter unterstützt. Kunden können Benutzer-E-Mail-Adressen per Massenexport aus der Adobe Admin Console exportieren und E-Mails anhand eines beliebigen E-Mail-Clients senden. </p> </td> 
  </tr> 
 </tbody> 
</table>
