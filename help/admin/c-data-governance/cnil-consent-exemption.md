---
description: Informieren Sie sich über die Richtlinien und Empfehlungen für die Zustimmung der Benutzer zum Speichern oder Lesen von nicht erforderlichen Cookies auf Geräten oder Browsern.
title: Was sind die CNIL-Richtlinien für Cookies und die Zustimmung der Benutzer?
feature: Data Governance
exl-id: 04179e58-dbba-45e2-ba57-7fe5fdedc483
source-git-commit: ac9e4934cee0178fb00e4201cc3444d333a74052
workflow-type: ht
source-wordcount: '732'
ht-degree: 100%

---

# CNIL-Zustimmungsfreistellung

Am 1. Oktober 2020 veröffentlichte die französische Datenschutzbehörde (im Folgenden „CNIL“) eine überarbeitete Fassung ihrer Cookie-Leitlinien (im Folgenden „Leitlinien“) und ihrer abschließenden Empfehlungen zur Einholung der Zustimmung der Benutzer zum Speichern oder Lesen nicht unerlässlicher Cookies und ähnlicher Technologien auf Geräten oder Browsern der Benutzer (im Folgenden „Empfehlungen“).

Die Leitlinien sehen eine begrenzte Freistellung von der Zustimmungspflicht vor („Zustimmungsfreistellung“). Die Zustimmungsfreistellung gilt für Analytics-Cookies, deren Zweck nur auf die Messung der Zielgruppe der Site oder Mobile App im Auftrag des Web-Herausgebers beschränkt ist. Die Leitlinien sehen vor, dass für die Anwendung der Zustimmungsfreistellung die folgenden Bedingungen erfüllt sein müssen:

* Maximale Datenaufbewahrung über 25 Monate.  Sie können Ihre aktuellen Einstellungen für die Datenaufbewahrung unter „Analytics“ > „Admin“ > „Datenverwaltung“ überprüfen.  [Datenaufbewahrung](https://experienceleague.adobe.com/docs/analytics/technotes/data-retention.html?lang=de)
* Deaktivieren Sie Drittanbieter-Cookies in Experience Cloud Identifier. [disableThirdPartyCalls](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/configurations/disablethirdpartycalls.html?lang=de#id-service-api), [disableThirdPartyCookies](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/configurations/disable-cookies.html?lang=de#id-service-api) und [disableIdSyncs](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/configurations/disableidsync.html?lang=de#id-service-api)
* Cookie-Beschränkung auf 13 Monate. Mit der Variablen `cookieLifetime` können Sie den Ablauf Ihres Analytics-Cookies überschreiben. Experience Cloud-Cookies, einschließlich Analytics und ECID, verlängern das Cookie-Ablaufdatum mit jedem Besuch. Um einen statischen, nicht rollierenden Cookie-Ablauf festzulegen, haben Sie folgende Möglichkeiten: (1) Schreiben Sie benutzerdefinierten Code, um ein Datum festzulegen, an dem das Cookie gelöscht werden soll, oder (2) verwenden Sie Ihre CMP, um das Zurücksetzdatum des Cookies zu steuern. [cookieLifetime](https://experienceleague.adobe.com/docs/analytics/implementation/vars/config-vars/cookielifetime.html?lang=de) und [Experience Cloud-Cookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-privacy.html?lang=de#ec-cookies)
* Eingeschränkter Umfang. Der Umfang des Cookies muss auf eine einzelne Site oder Anwendung beschränkt sein. [Browsercookies](https://experienceleague.adobe.com/docs/analytics/technotes/cookies.html?lang=de#third-party-cookie-implementations)
* Anonymisierung. Anonymisieren des letzten Oktetts der IP-Adresse. [Allgemeine Kontoeinstellungen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/general-acct-settings-admin.html?lang=de)
* Besucher-ID aus Berichten ausblenden.  Die Besucher-IDs sind in Adobe Workspace und Adobe Reports &amp; Analytics standardmäßig nicht sichtbar.  Besucher-IDs stehen in Daten-Feeds und Data Warehouse zur Verfügung.  Der Zugriff auf Daten-Feeds und Data Warehouse kann durch [Zugriffsberechtigungen in Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=de#task_040673FE3E3E429B9531FBCB8B6A4391) beschränkt werden  und durch [Referenz zur Daten-Feed-Spalte](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html?lang=de#columns%2C-descriptions%2C-and-data-types)
* Geopositionsparameter. Die Geoposition darf nicht präziser sein als Postleitzahlen. [Zip-Option](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/zip.html?lang=de#zip-in-adobe-experience-platform-launch) und [Allgemeine Kontoeinstellungen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/general-acct-settings-admin.html?lang=de#admin-tools)
* Legen Sie die Opt-in-Optionen fest.  Mit dem Opt-in-Service können Sie Besucherprotokolle einrichten, um zu bestimmen, ob Sie ein Cookie auf dem Gerät oder Browser des Benutzers erstellen können, wenn dieser Ihre Site besucht. [Opt-in-Service](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html?lang=de)
* Datenfreigabe verhindern.  Um die Datenfreigabe für Adobe Audience Manager auszuschließen, verwenden Sie die Kontextvariable `opt.dmp` für [Privacy Reporting](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/consent-variables.html?lang=de#variables), um zu verhindern, dass Treffer freigegeben werden.
* Zugriffs- und Löschmöglichkeit. Verwenden Sie den Privacy Service für Zugriffs- und Löschanforderungen. [Analytics &amp; Privacy Service](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/an-gdpr-overview.html?lang=de)

## Zusätzliche Überlegungen zur Datenerfassung

Es gelten zusätzlich folgende Überlegungen:

* Adobe Analytics betreibt Datenverarbeitungszentren in den USA, Großbritannien und Singapur, um allen Kunden Flexibilität bei der Erfassung, Verarbeitung und Speicherung ihrer Daten auf regionaler Ebene zu bieten. Bei der Konfiguration der erstmaligen Einrichtung von Adobe Analytics wählen Kunden den gewünschten Standort des Datenverarbeitungszentrums aus. Die Kundendaten werden letztendlich in ihrer ausgewählten Region für das Analytics-Hauptprodukt gespeichert.
* Ziehen Sie in Erwägung, den Opt-in-Status in einer Analytics-Variablen zu erfassen, um Opt-in-Daten und Opt-out-Daten bei der Segmentierung oder bei Virtual Report Suites zu trennen oder zu separaten Endpunkten weiterzuleiten.
* Keine Messung außerhalb der Site oder App ohne vorherige Zustimmung, z. B. keine Offsite-Kampagnen, E-Mail-Kampagnen oder iFrames.
* Die Erfassung personenbezogener Daten in Variablen ist ohne Zustimmung nicht gestattet. [Experience Cloud-Aktivitäten auf Basis des Benutzereinverständnisses steuern](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/use-opt-in-to-control-experience-cloud-activities-based-on-user-consent.html?lang=de%22%20\l%20%22implementation#implementation)
* Daten dürfen nur zur Erstellung anonymer Statistiken verwendet werden, wobei sie nicht mit anderen Daten kombiniert werden dürfen.
* Die Daten werden nicht für Querverweisaktionen verwendet.
* GPS-Geopositionsdaten werden nicht erfasst.
* Wenn die Endbenutzer-Einwilligung erteilt wurde, können die oben genannten Einstellungen geändert und die Einschränkungen gelockert werden.

Weitere Informationen finden Sie auf der Website [CNIL Cookie Exemption](https://www.cnil.fr/en/sheet-ndeg16-use-analytics-your-websites-and-applications).
