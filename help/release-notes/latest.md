---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: ae03f0d9e5f22c8e8ff6550a33a6f9d18432f46f
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 86%

---

# Aktuelle Adobe Analytics-Versionshinweise (Oktober 2024)

**Letztes Update**: Freitag, 17. Oktober 2024

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom 2. Oktober 2024 bis zum 22. Oktober 2024. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| Neuer Report Builder für Adobe Analytics | Die neue Report Builder-Anwendung bietet aktualisierte Funktionen wie verbesserte Leistung, optimierte Benutzeroberfläche, 2.0-API-Unterstützung und Unterstützung für Microsoft Excel unter Mac, Windows und Webbrowsern. [Weitere Informationen](https://experienceleague.adobe.com/en/docs/analytics/analyze/report-builder/report-buider-overview) |  | Donnerstag, 16. Oktober 2024 |

## Fehlerbehebungen in Adobe Analytics

Analysis Workspace: AN-343611; AN-355870; AN-357100; AN-358364; AN-358756; AN-359269
Analytics-App: AN-354085
Klassifizierungen: AN-353074; AN-357533; AN-358308; AN-358350; AN-358732; AN-358925; AN-359249
Geräteübergreifende Analyse: AN-357968
Daten-Feeds: AN-358489; AN-358542
Data Warehouse: AN-352181; AN-356701; AN-356802; AN-356804; AN-359162

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Datum hinzugefügt oder aktualisiert | Beschreibung |
| ----------- | ---------- | ---------- |
| **Automatische Zuordnung von XDM-Feldern mit zusätzlichen Implementierungsdetails** | 11. September 2024 | Wenn Sie Adobe Experience Platform Edge Network zum Senden von Daten an Adobe Analytics verwenden, werden die XDM-Felder `xdm.implementationdetails.name` und `xdm.implementationdetails.environment` nun immer den Kontextdatenvariablen `c.a.x.implementationdetails.name` und `c.a.x.implementationdetails.environment` zugeordnet. Früher wurde bei bestimmten Szenarien verhindert, dass diese Werte ausgefüllt werden. Passen Sie die relevanten Verarbeitungsregeln an, damit diese Werte verfügbar sind. |

{style="table-layout:auto"}

## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Ende der Nutzungsdauer für Adobe Analytics-API (Version 1.4)** | 17. Juli 2024 | Am **12. August 2026** erreichen die folgenden Analytics Legacy-API-Dienste ihr Lebenszyklusende und werden beendet. Aktuelle Integrationen, die mit diesen Diensten erstellt wurden, funktionieren nicht mehr:<ul><li>Adobe Analytics-API (Version 1.4)</li><li>WSSE-Authentifizierung von Adobe Analytics </li></ul><p>Integrationen, die die Adobe Analytics-API (Version 1.4) verwenden, müssen zur [Adobe Analytics 2.0-API](https://developer.adobe.com/analytics-apis/docs/2.0/) migrieren, während WSSE-Integrationen zu einem OAuth-basierten Authentifizierungsprotokoll in der [Adobe Developer Console](https://developer.adobe.com/console) migrieren müssen.</p><p>Antworten auf häufig gestellte Fragen und weitere Anleitungen finden Sie in den [häufig gestellten Fragen zum Ende der Nutzungsdauer der Adobe Analytics 1.4-API](/help/admin/c-admin-api/c-admin-14-api-eol.md).</p> |
| **Migration auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O** | 11. Mai 2023 | Kundinnen und Kunden von Adobe Analytics-API und Livestream, die JWT-Anmeldeinformationen für Adobe I/O verwenden, müssen bis zum **1. Januar 2025** auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O migrieren. Adobe I/O lässt die Erstellung neuer JWT-Anmeldeinformationen ab dem 1. Mai 2024 nicht mehr zu. Kunden und Kundinnen, die JWT verwenden, müssen neue OAuth Server-zu-Server-Anmeldeinformationen erstellen oder ihre bestehende JWT-Anmeldeinformationen zu OAuth Server-zu-Server-Anmeldeinformationen migrieren. Kunden und Kundinnen müssen außerdem ihre Client-Anwendungen aktualisieren, um die neuen OAuth Server-to-Server-Anmeldeinformationen zu verwenden. <ul><li>[Migration von Dienstkonto-Anmeldeinformationen (JWT)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementierungshandbuch für neue und alte Programme mit OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[Verwenden der neuen OAuth Server-zu-Server-Anmeldeinformationen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Häufig gestellte Fragen (FAQ)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}

## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.26.0) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2024](/help/release-notes/2024.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zum Add-on für Streaming-Mediensammlungen](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
