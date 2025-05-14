---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 9c6da2c1ed5bc2c016da16a5bb821f0064e1ae4f
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 48%

---

# Aktuelle Versionshinweise zu Adobe Analytics (Version vom Mai 2025)

**Letzte Aktualisierung:**: Donnerstag, 14. Mai 2025

Diese Versionshinweise decken den Veröffentlichungszeitraum vom XX. April bis zum 18. Juni 2025 ab. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Das linke Bedienfeld von Analysis Workspace wird beim Bewegen des Mauszeigers nicht mehr geöffnet und geschlossen** | Das linke Bedienfeld in Analysis Workspace wird verwendet, um Ihrem Projekt Elemente wie Komponenten, Bedienfelder und Visualisierungen hinzuzufügen. Die Option zum vorübergehenden Öffnen des linken Bedienfelds durch Bewegen des Mauszeigers über eines der Symbole ganz links ist nicht mehr verfügbar. Klicken Sie stattdessen einfach auf eines dieser Symbole, um das Bedienfeld offen zu lassen, und klicken Sie dann auf dasselbe Symbol, um es zu schließen. |  | Freitag, 29. Mai 2025 |


## Fehlerbehebungen in Adobe Analytics

**Warnhinweise**: AN-378351
**Analysis Workspace**: AN-363521; AN-367366; AN-373575; AN-374238; AN-374295; AN-374382; AN-376938; AN-377176; AN-377467; AN-377942
**Asset-Übertragung**: AN-373381
**Klassifizierungen**: AN-373166; AN-373479; AN-376074; AN-377337; AN-377505
**Komponenten**: AN-314468
**Daten-Feeds**: AN-370241; AN-375267; AN-376940
**Datenquellen**: AN-375259
**Data Warehouse**: AN-370415; AN-372090;
**PLATTFORM**: AN-365681; AN-372306; AN-372616;
**Echtzeit-Reporting**: AN-365681
**Report Builder**: AN-371395
**Segmentierung**: AN-373576; AN-375858
**Virtual Report Suites**: AN-377948; AN-377952
**VISTA-Regeln**: AN-373292

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Datum hinzugefügt oder aktualisiert | Beschreibung |
| ----------- | ---------- | ---------- |
| **Das linke Bedienfeld von Analysis Workspace wird beim Bewegen des Mauszeigers nicht mehr geöffnet und geschlossen** | Das linke Bedienfeld in Analysis Workspace wird verwendet, um Ihrem Projekt Elemente wie Komponenten, Bedienfelder und Visualisierungen hinzuzufügen. Die Option zum vorübergehenden Öffnen des linken Bedienfelds durch Bewegen des Mauszeigers über eines der Symbole ganz links ist nicht mehr verfügbar. Klicken Sie stattdessen einfach auf eines dieser Symbole, um das Bedienfeld offen zu lassen, und klicken Sie dann auf dasselbe Symbol, um es zu schließen. |  | Freitag, 29. Mai 2025 |


## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Zugriff über ältere Domains oder über ältere SSO** | Freitag, 10. April 2025 | Adobe plant, die Art und Weise, wie Benutzende auf Adobe Analytics zugreifen, zu aktualisieren, um die Sicherheit zu erhöhen und die Anmeldung zu optimieren. Im Rahmen dieser Bemühungen wird der Zugriff über veraltete Domains oder über veraltete SSO, einschließlich `my.omniture.com`, am (2. **2026)**. Nach diesem Datum funktionieren die bisherigen Anmeldedaten und das alte SSO nicht mehr. Alle Benutzer müssen sich über `experience.adobe.com` mit ihrer Adobe Experience Cloud ID anmelden. Wenn Sie Hilfe bei Ihrer Experience Cloud ID benötigen, wenden Sie sich an den Adobe Analytics-Administrator Ihres Unternehmens oder an die [Adobe-Kundenunterstützung](https://helpx.adobe.com/de/contact.html). |
| **Migration auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O** | 17. Januar 2025 | Kundinnen und Kunden von Adobe Analytics-API und -Livestream, die JWT-Anmeldeinformationen für Adobe I/O verwenden, müssen bis zum **30. Juni 2025** auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O migrieren. Adobe I/O lässt die Erstellung neuer JWT-Anmeldeinformationen ab dem 1. Mai 2024 nicht mehr zu. Kunden und Kundinnen, die JWT verwenden, müssen neue OAuth Server-zu-Server-Anmeldeinformationen erstellen oder ihre bestehende JWT-Anmeldeinformationen zu OAuth Server-zu-Server-Anmeldeinformationen migrieren. Kunden und Kundinnen müssen außerdem ihre Client-Anwendungen aktualisieren, um die neuen OAuth Server-to-Server-Anmeldeinformationen zu verwenden. <ul><li>[Migration von Dienstkonto-Anmeldeinformationen (JWT)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration)</li><li>[Implementierungshandbuch für neue und alte Programme mit OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation)<li>[Verwenden der neuen OAuth Server-zu-Server-Anmeldeinformationen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation)</li><li>[Häufig gestellte Fragen (FAQ)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs)</li></ul> |
| **Ende der Nutzungsdauer für Adobe Analytics-API (Version 1.4)** | 17. Juli 2024 | Ab **12. August 2026** werden die folgenden veralteten Analytics-API-Dienste nicht mehr unterstützt und beendet. Aktuelle Integrationen, die mit diesen Diensten erstellt wurden, funktionieren dann nicht mehr:<ul><li>Adobe Analytics-API (Version 1.4)</li><li>WSSE-Authentifizierung von Adobe Analytics </li></ul><p>Integrationen, die die Adobe Analytics-API (Version 1.4) verwenden, müssen zur [Adobe Analytics 2.0-API](https://developer.adobe.com/analytics-apis/docs/2.0/) migrieren, während WSSE-Integrationen zu einem OAuth-basierten Authentifizierungsprotokoll in der [Adobe Developer Console](https://developer.adobe.com/console) migrieren müssen.</p><p>Antworten auf häufig gestellte Fragen und weitere Anleitungen finden Sie in den [häufig gestellten Fragen zum Ende der Nutzungsdauer der Adobe Analytics 1.4-API](/help/admin/c-admin-api/c-admin-14-api-eol.md).</p> |


## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen finden Sie in den [Versionshinweisen zu AppMeasurement](https://github.com/adobe/appmeasurement/releases).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2025](/help/release-notes/2025.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zur Streaming-Mediensammlung](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
