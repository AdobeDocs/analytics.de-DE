---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: e2e387f20d5e5732ec1d7eb67a0c81df95e07a55
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 62%

---

# Aktuelle Adobe Analytics-Versionshinweise (Version April 2025)

**Letzte Aktualisierung**: Donnerstag, 16. April 2025

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom 26. März bis Mai 2025. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Analytics-Inventar** | Das Analytics-Inventar bietet einen umfassenden Überblick über Ihre Adobe Analytics-Umgebung, einschließlich der Anzahl der Projekte und Komponenten, Report Suites, Benutzenden und mehr. Durch die Automatisierung des Inventarprozesses können Sie den Aufwand für den Wechsel von Adobe Analytics zu Customer Journey Analytics schnell verstehen. Dies erleichtert und beschleunigt den Übergang. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/analytics/admin/admin-tools/analytics-inventory) |  | 26. März 2025 |
| **„Nur Data Warehouse“-Dimensionen** | Aufgrund des Feedbacks unserer Kunden haben wir beschlossen, eine Neubewertung vorzunehmen. Die Funktion „Nur Data Warehouse-Dimensionen“ wird nicht wie angekündigt veröffentlicht. | | TBD |

## Fehlerbehebungen in Adobe Analytics

**A4T**: AN-370625; AN-371279; AN-371351
**Admin Tools**: AN-365072; AN-371303
**Analysis Workspace**: AN-363831; AN-369554
**EINSTUFUNGEN**: AN-370519; AN-370727; AN-370827; AN-370941; AN-370995; AN-371377; AN-371597; AN-371868; AN-371869; AN-372510; AN-372650; AN-373164; AN-373300; AN-373308; AN-373592
**Datenerfassung**: AN-371877
**Daten-Feeds** AN-368676; AN-370225; AN-370514; AN-370521; AN-370687; AN-370761; AN-370911; AN-371047; AN-371542; AN-371627; AN-371746; AN-372708; AN-373068; AN-373179
**Data Warehouse**: AN-366649; AN-369817; AN-370705; AN-371127; AN-371995; AN-372596; AN-372940
**Marketing-**: AN-372308
**Mobile App**: AN-370287; AN-371335; AN-371374
**PLATTFORM**: AN-369510; AN-370435; AN-372150
**Report Builder**: AN-369830; AN-371395; AN-372983

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Datum hinzugefügt oder aktualisiert | Beschreibung |
| ----------- | ---------- | ---------- |
| k. A. |  |  |

## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Zugriff über ältere Domains oder über ältere SSO** | Freitag, 10. April 2025 | Adobe plant, die Art und Weise, wie Benutzende auf Adobe Analytics zugreifen, zu aktualisieren, um die Sicherheit zu erhöhen und die Anmeldung zu optimieren. Im Rahmen dieser Bemühungen wird der Zugriff über veraltete Domains oder über veraltete SSO, einschließlich `my.omniture.com`, am (2. **2026)**. Nach diesem Datum funktionieren die bisherigen Anmeldedaten und das alte SSO nicht mehr. Alle Benutzer müssen sich über `experience.adobe.com` mit ihrer Adobe Experience Cloud ID anmelden. Wenn Sie Hilfe bei Ihrer Experience Cloud ID benötigen, wenden Sie sich an den Adobe Analytics-Administrator Ihres Unternehmens oder an die [Adobe-Kundenunterstützung](https://helpx.adobe.com/de/contact.html). |
| **Migration auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O** | 17. Januar 2025 | Kundinnen und Kunden von Adobe Analytics-API und -Livestream, die JWT-Anmeldeinformationen für Adobe I/O verwenden, müssen bis zum **30. Juni 2025** auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O migrieren. Adobe I/O lässt die Erstellung neuer JWT-Anmeldeinformationen ab dem 1. Mai 2024 nicht mehr zu. Kunden und Kundinnen, die JWT verwenden, müssen neue OAuth Server-zu-Server-Anmeldeinformationen erstellen oder ihre bestehende JWT-Anmeldeinformationen zu OAuth Server-zu-Server-Anmeldeinformationen migrieren. Kunden und Kundinnen müssen außerdem ihre Client-Anwendungen aktualisieren, um die neuen OAuth Server-to-Server-Anmeldeinformationen zu verwenden. <ul><li>[Migration von Dienstkonto-Anmeldeinformationen (JWT)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementierungshandbuch für neue und alte Programme mit OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[Verwenden der neuen OAuth Server-zu-Server-Anmeldeinformationen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Häufig gestellte Fragen (FAQ)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **Ende der Nutzungsdauer für Adobe Analytics-API (Version 1.4)** | 17. Juli 2024 | Ab **12. August 2026** werden die folgenden veralteten Analytics-API-Dienste nicht mehr unterstützt und beendet. Aktuelle Integrationen, die mit diesen Diensten erstellt wurden, funktionieren dann nicht mehr:<ul><li>Adobe Analytics-API (Version 1.4)</li><li>WSSE-Authentifizierung von Adobe Analytics </li></ul><p>Integrationen, die die Adobe Analytics-API (Version 1.4) verwenden, müssen zur [Adobe Analytics 2.0-API](https://developer.adobe.com/analytics-apis/docs/2.0/) migrieren, während WSSE-Integrationen zu einem OAuth-basierten Authentifizierungsprotokoll in der [Adobe Developer Console](https://developer.adobe.com/console) migrieren müssen.</p><p>Antworten auf häufig gestellte Fragen und weitere Anleitungen finden Sie in den [häufig gestellten Fragen zum Ende der Nutzungsdauer der Adobe Analytics 1.4-API](/help/admin/c-admin-api/c-admin-14-api-eol.md).</p> |


## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen finden Sie in den [Versionshinweisen zu AppMeasurement](https://github.com/adobe/appmeasurement/releases).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2025](/help/release-notes/2025.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zur Streaming-Mediensammlung](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
