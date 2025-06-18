---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 987638b1a5601a4c5713611b463e4ec77479ed8d
workflow-type: tm+mt
source-wordcount: '968'
ht-degree: 45%

---

# Aktuelle Versionshinweise zu Adobe Analytics (Version Juni 2025)

**Letzte Aktualisierung**: Donnerstag, 18. Juni 2025

Diese Versionshinweise decken den Veröffentlichungszeitraum vom 18. Juni bis zum 15. Juli 2025 ab. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Unterstützung für sichere Ziele in der neuen Report Builder** | Dem Report Builder-Add-in wurden neue Exportziele hinzugefügt. Die folgenden Cloud-Speicher-Ziele werden unterstützt: <ul><li>Amazon S3 Role ARN</li><li>Google Cloud Platform</li><li>Azure SAS</li><li>Azure RBAC</li></ul> FTP wird aus Sicherheitsgründen nicht mehr unterstützt. (Link zur Dokumentation folgt) |  | Juni 18,2025 |
| **Neues Vorschauerlebnis** | Im Vorschaubereich, in dem Segmente, berechnete Metriken usw. in der Vorschau angezeigt werden, wird jetzt eine horizontale Balkenvisualisierung anstelle einer Ringvisualisierung verwendet. |  | 18. Juni 2025 |
| **Dialogfeld „Geändertes Attributionsmodell“** | Sie können jetzt den Container und den Zeitraum im Dialogfeld Attributionsmodell separat definieren. |  | Juni 18,2025 |
| **Die Navigation zur Benutzeroberfläche für Kundenattribute wurde aktualisiert** | Die Benutzeroberfläche Kundenattribute kann jetzt direkt über den App-Selektor in Adobe Experience Cloud aufgerufen werden. |  | TBD |
| **Streaming-Medien: Unterstützung von Zeitplandaten** | Sie können jetzt geplante Daten vergangener Live-Streaming-Medieninhalte hochladen, um die Zuschauerzahlen einfacher und genauer verfolgen zu können. Im Folgenden finden Sie Beispiele für Live-Inhalte, die beim Hochladen von Zeitplandaten unterstützt werden:<ul><li>FAST-Plattformen (Free and Supported TV)</li><li>Lokale Streams</li><li>Live-Sport</li></ul>Durch das Hochladen von Zeitplandaten können Sie die Daten der Zuschauer für einzelne Programme verfolgen, die während der von Ihnen in der Upload-Datei festgelegten Zeit ausgeführt wurden. Sie können sogar Zuschauerzahlen zu bestimmten Themen oder Programmsegmenten erfassen. Diese Funktionen sind unabhängig davon verfügbar, wie Sie die Streaming-Mediensammlung implementiert haben.<p>Zuvor war es bei der Analyse von Live-Inhalten schwierig, eine bestimmte Sitzung genau mit bestimmten Programmen zu verknüpfen, und es war nicht möglich, eine bestimmte Sitzung mit einzelnen Themen oder Programmsegmenten zu verknüpfen. Weitere Informationen |  | &#x200B;25. Juni 2025 |
| **Unterstützung für das Chrome-Pre-Rendering** | Steuern, wie sich Datenerfassungsbibliotheken verhalten, wenn Chrome eine Seite vorab rendert. (Link zur Dokumentation folgt) |  | Dienstag, 30. Juni 2025 |

## Fehlerbehebungen in Adobe Analytics

**A4T**: AN-379045
**Advertising Analytics**: AN-377338
**Warnhinweise**: AN-377229
**Analysis Workspace**: AN-378891; AN-379589; AN-379604; AN-381270; AN-382264; AN-382414;
**API 1.4**: AN-380188
**API 2.0**: AN-373078; AN-379006; AN-381248
**EINSTUFUNGEN**: AN-379209; AN-379315; AN-379567; AN-379573; AN-379749; AN-379764; AN-379818; AN-380433; AN-381670; AN-381751; AN-381994; AN-382055; AN-382682; AN-383059; AN-383409
**Beitragsanalyse**: AN-369822
**Daten-Feeds** AN-365552; AN-367158; AN-378288; AN-379754; AN-380433; AN-380855; AN-380959; AN-381115; AN-381657; AN-381931
**Data Warehouse**: AN-379244
**Platform**: AN-375847
**Verarbeitungsregeln**: AN-375157
**Report Builder**: AN-371395; AN-372174; AN-373815; AN-383194
**Server-Aufrufe**: AN-380930
**Nutzungs- und Zugriffsprotokolle**: AN-372130; AN-382123
**Virtual Report Suites**: AN-382010


## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Vorgängerversion von Report Builder** | 18. Juni 2025 | Das alte Report Builder-Add-in wird im Juni 2026 eingestellt. Alle Benutzer sollten mit dem Upgrade ihrer alten Arbeitsmappen auf die [neue Report Builder](https://experienceleague.adobe.com/de/docs/analytics/analyze/report-builder/rb-overview) beginnen. Die neue Report Builder ist sowohl für Adobe Analytics- als auch für Customer Journey Analytics-Kunden verfügbar. Es bietet [nahezu gleiche Funktionen](https://experienceleague.adobe.com/en/docs/analytics/analyze/report-builder/convert-workbooks#unsupported) sowie viele neue, praktische Funktionen und Benutzeroberflächenverbesserungen. Um den Upgrade-Prozess zu vereinfachen, enthält die neue Report Builder eine Funktion zur einfachen Arbeitsmappen-Konvertierung. Die neue Report Builder ist nur als Add-in über den Microsoft Store verfügbar. Viele Organisationen benötigen einen internen Genehmigungsprozess, bevor das Add-In Benutzern zur Verfügung gestellt werden kann. Planen Sie Zeit für diesen Prozess ein und beginnen Sie jetzt mit Ihrer Organisation, um vor dem Ende der Nutzungsdauer genügend Zeit für ein Upgrade Ihrer Arbeitsmappen zu haben. |
| **Zugriff über Legacy-Domains oder Legacy-SSO** | 10. April 2025 | Adobe plant, die Art und Weise zu aktualisieren, wie Benutzende auf Adobe Analytics zugreifen, um die Sicherheit zu erhöhen und das Anmeldeerlebnis zu optimieren. Im Rahmen dieser Bemühungen wird der Zugriff über Legacy-Domains oder Legacy-SSO, einschließlich `my.omniture.com`, am **2. Januar 2026** dauerhaft eingestellt. Nach diesem Datum funktionieren die alten Anmeldedaten bzw. die alte SSO-Methode nicht mehr. Alle Benutzenden müssen sich über `experience.adobe.com` mit ihren Adobe Experience Cloud-IDs anmelden. Wenn Sie Hilfe im Zusammenhang mit Ihrer Experience Cloud-ID benötigen, wenden Sie sich an das Adobe Analytics-Admin-Team Ihrer Organisation oder an die [Adobe-Kundenunterstützung](https://helpx.adobe.com/de/contact.html). |
| **Migration auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O** | &#x200B;17. Januar 2025 | Kundinnen und Kunden von Adobe Analytics-API und -Livestream, die JWT-Anmeldeinformationen für Adobe I/O verwenden, müssen bis zum **30. Juni 2025** auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O migrieren. Adobe I/O lässt die Erstellung neuer JWT-Anmeldeinformationen ab dem 1. Mai 2024 nicht mehr zu. Kunden und Kundinnen, die JWT verwenden, müssen neue OAuth Server-zu-Server-Anmeldeinformationen erstellen oder ihre bestehende JWT-Anmeldeinformationen zu OAuth Server-zu-Server-Anmeldeinformationen migrieren. Kunden und Kundinnen müssen außerdem ihre Client-Anwendungen aktualisieren, um die neuen OAuth Server-to-Server-Anmeldeinformationen zu verwenden. <ul><li>[Migration von Dienstkonto-Anmeldeinformationen (JWT)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration)</li><li>[Implementierungshandbuch für neue und alte Programme mit OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation)<li>[Verwenden der neuen OAuth Server-zu-Server-Anmeldeinformationen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation)</li><li>[Häufig gestellte Fragen (FAQ)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs)</li></ul> |
| **Adobe Analytics-API (Version 1.4)** | 17. Juli 2024 | Ab **12. August 2026** werden die folgenden veralteten Analytics-API-Dienste nicht mehr unterstützt und beendet. Aktuelle Integrationen, die mit diesen Diensten erstellt wurden, funktionieren dann nicht mehr:<ul><li>Adobe Analytics-API (Version 1.4)</li><li>WSSE-Authentifizierung von Adobe Analytics </li></ul><p>Integrationen, die die Adobe Analytics-API (Version 1.4) verwenden, müssen zur [Adobe Analytics 2.0-API](https://developer.adobe.com/analytics-apis/docs/2.0/) migrieren, während WSSE-Integrationen zu einem OAuth-basierten Authentifizierungsprotokoll in der [Adobe Developer Console](https://developer.adobe.com/console) migrieren müssen.</p><p>Antworten auf häufig gestellte Fragen und weitere Anleitungen finden Sie in den [häufig gestellten Fragen zum Ende der Nutzungsdauer der Adobe Analytics 1.4-API](/help/admin/c-admin-api/c-admin-14-api-eol.md).</p> |



## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen finden Sie in den [Versionshinweisen zu AppMeasurement](https://github.com/adobe/appmeasurement/releases).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2025](/help/release-notes/2025.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zur Streaming-Mediensammlung](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
