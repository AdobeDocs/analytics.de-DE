---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: d7beee25af3551426eb905f0e727545de068b2d9
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 45%

---

# Aktuelle Versionshinweise zu Adobe Analytics (Version Januar 2025)

**Letzte Aktualisierung:** Dienstag, 22. Januar 2024

Diese Versionshinweise decken den Veröffentlichungszeitraum vom 15. Januar bis Mitte Februar 2025 ab. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Planung im neuen Report Builder** | Mit der Zeitplanung können Sie nicht nur Ihre neuen Report Builder-Arbeitsmappen planen. Darüber hinaus können Sie beim Konvertieren veralteter Arbeitsmappen die Metadaten für alte geplante Aufgaben abrufen. Auf diese Weise senden Sie Ihre alten Arbeitsmappen, wenn Sie sie in neue Arbeitsmappen konvertieren und planen, an dieselben E-Mails und mit derselben Kadenz wie die alten Arbeitsmappen. [Weitere Informationen](/help/analyze/report-builder/schedule-reportbuilder.md) |  | 22. Januar 2025 |
| **Verbesserungen an Berichten (auch als Vorlagen bezeichnet) in Analysis Workspace** | Für Berichte (auch als Vorlagen bezeichnet) sind jetzt verschiedene Verbesserungen verfügbar:<ul><li>Jetzt [!UICONTROL Vorlagen] (nicht mehr als &quot;[!UICONTROL &quot; ]).</li><li>Verbessertes Benutzererlebnis zum Anzeigen und Suchen von Vorlagen, einschließlich der Option zum Anzeigen von Vorlagen in einer Spaltenansicht oder Kartenansicht.</li><li>Neuer, intuitiverer Speicherort für Unternehmensvorlagen (unter **[!UICONTROL Workspace]** > **[!UICONTROL Templates]**).</li><li>Zuvor wurde beim Erstellen eines Projekts über das Dialogfeld auf Unternehmensvorlagen zugegriffen.</li><li>Zusätzliche vordefinierte Vorlagen sind verfügbar.</li></ul>[Weitere Informationen](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/templates/use-templates).<p>Administratoren können Vorlagen erstellen und für andere Benutzer in ihrem angemeldeten Unternehmen speichern, um sie zu verwenden. [Weitere Informationen](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/templates/create-templates) | Donnerstag, 15. Januar 2025 | Freitag, 30. Januar 2025 |
| **Aufbewahrungszeitraum der Transaktions-ID** | Die Aufbewahrungsfrist für Transaktions-IDs von 90 Tagen wird im Februar 2025 auf 25 Monate verlängert. Die `transactionID`-Variable identifiziert eine Transaktion eindeutig, sodass der Treffer mit Daten verknüpft werden kann, die über Datenquellen hochgeladen wurden. (Links zur Dokumentation folgen) |  | Mittwoch, 11. Februar 2025 |

## Fehlerbehebungen in Adobe Analytics

**A4T**: AN-355602; AN-365988
**Activity Map**: AN-365320
**Admin Console**: AN-363884
**Admin Tools**: AN-356747; AN-358776
**Advertising Analytics**: AN-355488
**Analysis Workspace**: AN-345318; AN-354801; AN-357052; AN-358975; AN-362886; AN-363831; AN-364124; AN-365257; AN-365319; AN-365462; AN-366194
**Analytics 1.4-API**: AN-358059
**CLASSIFICATIONS** AN-360049; AN-360745; AN-362345; AN-362560; AN-362633; AN-362653; AN-362762; AN-362885; AN-360424; AN-363343; AN-363860; AN-362208; AN-362576; AN-AN; AN-AN-AN; AN-362815; AN-362881; AN-362973; AN-363558; AN-364239; AN-364480; AN-364451; AN-364528; AN-364548; AN-364552; AN-364585; AN-364598; AN-364643; AN-364715; AN-364912; AN-AN; AN-364997; AN-365081 365189 365197 365203 365431 365647 365794 366546
**Komponentenmigration**: AN-362236; AN-365429
**Beitragsanalyse**: AN-360146
**Datenfeeds** AN-356997; AN-362470; AN-362498; AN-362775; AN-363323; AN-363413; AN-363569; AN-364063; AN-364142; AN-364294; AN-364367; AN-364594; AN-364995; AN-365127; AN-365519; AN-365272; AN-364298; AN-364325; AN-365760; AN-366152; AN-; AN-; AN-NV;
**Data Repair API**: AN-362773; AN-362874
**Datenquellen**: AN-360745; AN-362202; AN-364566
**Data Warehouse**: AN-361447; AN-362616; AN-364524; AN-365108
**Mobile App**: AN-362856; AN-365270
**Überlastungs**-Warnhinweise: AN-355594; AN-364547
**PLATTFORM**: AN-358914; AN-360205; AN-362990; AN-364550; AN-365454; AN-365485
**Report Builder**: AN-363478; AN-364433; AN-365610
**Reporting Activity Manager**: AN-362440
**Segmentierung**: AN-359921
**VISTA-**: AN-362927

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Datum hinzugefügt oder aktualisiert | Beschreibung |
| ----------- | ---------- | ---------- |
| **Kundinnen und Kunden ohne Adobe Campaign verlieren den Zugriff auf Trigger** | 16. Oktober 2023 | Am 30. Januar 2025 verlieren Adobe Analytics-Kunden ohne Adobe Campaign-Lizenz den Zugriff auf die Möglichkeit, [Trigger zu konfigurieren und zu nutzen](https://experienceleague.adobe.com/en/docs/core-services/interface/services/triggers). Kundinnen und Kunden müssen entweder Campaign erwerben, die Nutzung von Triggern in Zukunft einstellen oder sich andere Adobe-Tools ansehen, die Trigger-Funktionen bieten. |

## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Migration auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O** | Samstag, 17. Januar 2025 | Kundinnen und Kunden von Adobe Analytics-API und Livestream, die JWT-Anmeldeinformationen für Adobe I/O verwenden, müssen bis zum **Dienstag, 30. Juni 2025** auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O migrieren. Adobe I/O lässt die Erstellung neuer JWT-Anmeldeinformationen ab dem 1. Mai 2024 nicht mehr zu. Kunden und Kundinnen, die JWT verwenden, müssen neue OAuth Server-zu-Server-Anmeldeinformationen erstellen oder ihre bestehende JWT-Anmeldeinformationen zu OAuth Server-zu-Server-Anmeldeinformationen migrieren. Kunden und Kundinnen müssen außerdem ihre Client-Anwendungen aktualisieren, um die neuen OAuth Server-to-Server-Anmeldeinformationen zu verwenden. <ul><li>[Migration von Dienstkonto-Anmeldeinformationen (JWT)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementierungshandbuch für neue und alte Programme mit OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[Verwenden der neuen OAuth Server-zu-Server-Anmeldeinformationen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Häufig gestellte Fragen (FAQ)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **Ende der Nutzungsdauer für Adobe Analytics-API (Version 1.4)** | 17. Juli 2024 | Ab **12. August 2026** werden die folgenden veralteten Analytics-API-Dienste nicht mehr unterstützt und beendet. Aktuelle Integrationen, die mit diesen Diensten erstellt wurden, funktionieren dann nicht mehr:<ul><li>Adobe Analytics-API (Version 1.4)</li><li>WSSE-Authentifizierung von Adobe Analytics </li></ul><p>Integrationen, die die Adobe Analytics-API (Version 1.4) verwenden, müssen zur [Adobe Analytics 2.0-API](https://developer.adobe.com/analytics-apis/docs/2.0/) migrieren, während WSSE-Integrationen zu einem OAuth-basierten Authentifizierungsprotokoll in der [Adobe Developer Console](https://developer.adobe.com/console) migrieren müssen.</p><p>Antworten auf häufig gestellte Fragen und weitere Anleitungen finden Sie in den [häufig gestellten Fragen zum Ende der Nutzungsdauer der Adobe Analytics 1.4-API](/help/admin/c-admin-api/c-admin-14-api-eol.md).</p> |


## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.26.0) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2024](/help/release-notes/2024.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zur Streaming-Mediensammlung](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
