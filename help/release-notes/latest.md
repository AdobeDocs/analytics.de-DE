---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 91a17aa9ae7a0a6c6b7a1fd8d5ffe5d7d2efb294
workflow-type: tm+mt
source-wordcount: '1072'
ht-degree: 94%

---

# Aktuelle Adobe Analytics-Versionshinweise (Version Juni 2025)

**Letzte Aktualisierung**: Dienstag, 7. Juli 2025

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom 18. Juni bis zum 15. Juli 2025. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Livestream-TNT-Felder mit Algorithmen** | Livestream wird derzeit aktualisiert, um sicherzustellen, dass die Technologie weiterhin modern und stabil ist. Im Rahmen dieser Aktualisierung beginnen wir mit der Integration des TNT-Felds in die Livestream-Ausgabe, wenn Ihr TNT-Feld einen Algorithmus enthält. Dies umfasst jedoch nur die zuvor unterstützten Elemente: `campaignId`, `recipeId`, `trafficType`, `actionId` und `actionName`. Das gesamte TNT-Schema für Livestream bleibt unverändert. |   | Juli 7,2025 |
| **Unterstützung für sichere Cloud-Ziele im neuen Report Builder** | Das JavaScript-Add-in Report Builder unterstützt jetzt den Export von Berichten in die folgenden Cloud-Speicherziele:<ul><li>Amazon S3 Role ARN</li><li>Google Cloud Platform</li><li>Azure SAS</li><li>Azure RBAC</li></ul><p>Zuvor waren nur FTP und E-Mail als Ziele verfügbar. FTP wird aufgrund von Sicherheitsbedenken nicht mehr unterstützt.</p><p>Weitere Informationen finden Sie unter [Planen von Arbeitsmappen durch den Export in Cloud-Ziele](/help/analyze/report-builder/report-builder-export.md).</p><p>Zusätzlich zu diesen Änderungen bietet das Feld „Verwenden mit“ beim Erstellen eines Speicherorts in Adobe Analytics jetzt die Möglichkeit, den Speicherort mit Report Builder zu verwenden, wie in [Konfigurieren von Cloud-Import- und -Exportspeicherorten](/help/components/locations/configure-import-locations.md) beschrieben.</p> |  | 19. Juni 2025 (ursprünglich 18. Juni) |
| **Neues Vorschauerlebnis** | Der Vorschaubereich, der beim Erstellen eines Segments oder beim Konfigurieren der Einstellungen einer Datenansicht verwendet wird, nutzt jetzt eine Darstellung mit horizontalen Balken anstelle einer Darstellung mit Ringdiagrammen. |  | 18. Juni 2025 |
| **Geändertes Dialogfeld für Attributionsmodelle** | Sie können nun den Container und den Zeitraum separat im Dialogfeld für Attributionsmodelle definieren. |  | 18. Juni 2025 |
| **Aktualisierte Navigation zur Benutzeroberfläche für Kundenattribute** | Die Benutzeroberfläche für Kundenattribute ist jetzt direkt über die App-Auswahl in Adobe Experience Cloud zugänglich. |  | TBD |
| **Streaming-Medien: Unterstützung von Zeitplandaten** | Sie können jetzt Zeitplandaten von früheren Live-Inhalten von Streaming-Medien hochladen, um die Zuschauerzahlen einfacher und genauer zu verfolgen. Im Folgenden finden Sie Beispiele für Live-Inhalte, die mit dem Upload von Zeitplandaten unterstützt werden:<ul><li>FAST-Plattformen (Free Ad Supported TV)</li><li>Lokale Datenströme</li><li>Live-Sportübertragungen</li></ul>Durch das Hochladen von Zeitplandaten können Sie die Zuschauerzahlen für einzelne Programme verfolgen, die in dem von Ihnen in der Upload-Datei angegebenen Zeitraum gelaufen sind. Sie können sogar Zuschauerzahlen zu bestimmten Themen oder Programmsegmenten erfassen. Diese Funktionen sind unabhängig davon verfügbar, wie Sie die Erfassung von Streaming-Medien implementiert haben.<p>Zuvor war es bei der Analyse von Live-Inhalten schwierig, eine bestimmte Sitzung genau mit bestimmten Programmen zu verknüpfen, und es war nicht möglich, eine bestimmte Sitzung mit einzelnen Themen oder Programmsegmenten zu verknüpfen. Weitere Informationen |  | 15. August 2025 (ursprünglich 25. Juni 2025) |

## Fehlerbehebungen in Adobe Analytics

**A4T**: AN-379045
**Advertising Analytics**: AN-377338
**Warnhinweise**: AN-377229
**Analysis Workspace**: AN-378891; AN-379589; AN-379604; AN-381270; AN-382264; AN-382414;
**API  1.4**: AN-380188
**API  2.0**: AN-373078; AN-379006; AN-381248
**Klassifizierungen**: AN-379209; AN-379315; AN-379567; AN-379573; AN-379749; AN-379764; AN-379818; AN-380433; AN-381670; AN-381751; AN-381994; AN-382055; AN-382682; AN-383059; AN-383409
**Beitragsanalyse**: AN-369822
**Daten-Feeds** AN-365552; AN-367158; AN-378288; AN-379754; AN-380433; AN-380855; AN-380959; AN-381115; AN-381657; AN-381931
**Data Warehouse**: AN-379244
**Plattform**: AN-375847
**Verarbeitungsregeln**: AN-375157
**Report Builder**: AN-371395; AN-372174; AN-373815; AN-383194
**Server-Aufrufe**: AN-380930
**Nutzungs- und Zugriffsprotokolle**: AN-372130; AN-382123
**Virtual Report Suites**: AN-382010


## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Vorgängerversion von Report Builder** | 18. Juni 2025 | Die Vorgängerversion des Report Builder-Add-ins wird im Juni 2026 eingestellt. Alle Benutzenden sollten mit dem Upgrade ihrer Arbeitsmappen der Vorgängerversion auf den [neuen Report Builder](https://experienceleague.adobe.com/de/docs/analytics/analyze/report-builder/rb-overview) beginnen. Der neue Report Builder ist sowohl für Adobe Analytics- als auch für Customer Journey Analytics-Kundschaft verfügbar. Er bietet [nahezu die gleichen Funktionen](https://experienceleague.adobe.com/de/docs/analytics/analyze/report-builder/convert-workbooks#unsupported) sowie viele neue, praktische Funktionen und Verbesserungen der Benutzeroberfläche. Um den Upgrade-Prozess zu vereinfachen, enthält der neue Report Builder eine Funktion zur einfachen Arbeitsmappenkonvertierung. Der neue Report Builder ist nur als Add-in über den Microsoft Store verfügbar. Viele Organisationen benötigen einen internen Genehmigungsprozess, bevor das Add-in Benutzenden zur Verfügung gestellt werden kann. Planen Sie Zeit für diesen Prozess ein und arbeiten Sie jetzt mit Ihrer Organisation, um vor dem Ende der Nutzungsdauer genügend Zeit für ein Upgrade Ihrer Arbeitsmappen zu haben. |
| **Zugriff über Legacy-Domains oder Legacy-SSO** | 10. April 2025 | Adobe plant, die Art und Weise zu aktualisieren, wie Benutzende auf Adobe Analytics zugreifen, um die Sicherheit zu erhöhen und das Anmeldeerlebnis zu optimieren. Im Rahmen dieser Bemühungen wird der Zugriff über Legacy-Domains oder Legacy-SSO, einschließlich `my.omniture.com`, am **2. Januar 2026** dauerhaft eingestellt. Nach diesem Datum funktionieren die alten Anmeldedaten bzw. die alte SSO-Methode nicht mehr. Alle Benutzenden müssen sich über `experience.adobe.com` mit ihren Adobe Experience Cloud-IDs anmelden. Wenn Sie Hilfe im Zusammenhang mit Ihrer Experience Cloud-ID benötigen, wenden Sie sich an das Adobe Analytics-Admin-Team Ihrer Organisation oder an die [Adobe-Kundenunterstützung](https://helpx.adobe.com/de/contact.html). |
| **Migration auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O** | &#x200B;17. Januar 2025 | Kundinnen und Kunden von Adobe Analytics-API und -Livestream, die JWT-Anmeldeinformationen für Adobe I/O verwenden, müssen bis zum **30. Juni 2025** auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O migrieren. Adobe I/O lässt die Erstellung neuer JWT-Anmeldeinformationen ab dem 1. Mai 2024 nicht mehr zu. Kunden und Kundinnen, die JWT verwenden, müssen neue OAuth Server-zu-Server-Anmeldeinformationen erstellen oder ihre bestehende JWT-Anmeldeinformationen zu OAuth Server-zu-Server-Anmeldeinformationen migrieren. Kunden und Kundinnen müssen außerdem ihre Client-Anwendungen aktualisieren, um die neuen OAuth Server-to-Server-Anmeldeinformationen zu verwenden. <ul><li>[Migration von Dienstkonto-Anmeldeinformationen (JWT)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration)</li><li>[Implementierungshandbuch für neue und alte Programme mit OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation)<li>[Verwenden der neuen OAuth Server-zu-Server-Anmeldeinformationen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation)</li><li>[Häufig gestellte Fragen (FAQ)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs)</li></ul> |
| **Adobe Analytics-API (Version 1.4)** | 17. Juli 2024 | Ab **12. August 2026** werden die folgenden veralteten Analytics-API-Dienste nicht mehr unterstützt und beendet. Aktuelle Integrationen, die mit diesen Diensten erstellt wurden, funktionieren dann nicht mehr:<ul><li>Adobe Analytics-API (Version 1.4)</li><li>WSSE-Authentifizierung von Adobe Analytics </li></ul><p>Integrationen, die die Adobe Analytics-API (Version 1.4) verwenden, müssen zur [Adobe Analytics 2.0-API](https://developer.adobe.com/analytics-apis/docs/2.0/) migrieren, während WSSE-Integrationen zu einem OAuth-basierten Authentifizierungsprotokoll in der [Adobe Developer Console](https://developer.adobe.com/console) migrieren müssen.</p><p>Antworten auf häufig gestellte Fragen und weitere Anleitungen finden Sie in den [häufig gestellten Fragen zum Ende der Nutzungsdauer der Adobe Analytics 1.4-API](/help/admin/c-admin-api/c-admin-14-api-eol.md).</p> |



## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen finden Sie in den [Versionshinweisen zu AppMeasurement](https://github.com/adobe/appmeasurement/releases).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2025](/help/release-notes/2025.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zur Streaming-Mediensammlung](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
