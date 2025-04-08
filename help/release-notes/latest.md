---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: bf6a811aac7d881517944c8308fd97e719791cc0
workflow-type: tm+mt
source-wordcount: '980'
ht-degree: 94%

---

# Aktuelle Adobe Analytics-Versionshinweise (Version März 2025)

**Letzte Aktualisierung**: Samstag, 4. April 2025

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom 5. März bis Mai 2025. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Analytics-Inventar** | Der Analytics-Bestand bietet einen umfassenden Überblick über Ihre Adobe Analytics-Umgebung, einschließlich der Anzahl der Projekte und Komponenten, Report Suites, Benutzer und mehr. Durch die Automatisierung des Inventarprozesses können Sie den Aufwand für den Wechsel von Adobe Analytics zu Customer Journey Analytics schnell verstehen. Dies erleichtert und beschleunigt den Übergang. [Weitere Informationen](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/analytics-inventory) |  | 26. März 2025 |
| **Aktualisierung des Analytics-Kontextdatenfelds`a.locale`** | Durch diese Aktualisierung ändert sich die Art und Weise, wie das Analytics-Kontextdatenfeld `a.locale` bei der Datenerfassung über Experience Edge festgelegt wird. Wenn Daten mit Experience Edge an Adobe Analytics gesendet werden, werden Analytics-Felder basierend auf einer Zuordnung von XDM-Feldern ausgefüllt. Die Zuordnung für `c.a.locale` verweist auf ein nicht standardmäßiges XDM-Feld (`xdm.environment.language`). Dieses Feld wird aktualisiert, um auf das richtige Feld (`xdm.environment._dc.language`) zu verweisen.<p>Aus Gründen der Abwärtskompatibilität verweist die Zuordnung weiterhin auf `xdm.environment.language`. Um die Kontinuität sicherzustellen, hat `xdm.environment.language` Vorrang, falls beide Felder festgelegt sind. Die vollständige Liste der Zuordnungen von XDM zu standardmäßigen Analytics-Feldern finden Sie [hier](https://experienceleague.adobe.com/de/docs/analytics/implementation/aep-edge/xdm-var-mapping). | | 5. März 2025 |
| **Leitfaden für das Upgrade auf Customer Journey Analytics** | Ermöglicht die Erstellung eines schrittweisen Leitfadens für das Upgrade von Adobe Analytics auf Customer Journey Analytics. Dieser Leitfaden ist auf Ihre Organisation zugeschnitten und berücksichtigt Ihre aktuelle Adobe Analytics-Umgebung, die vorgesehenen Verwendungszwecke für Customer Journey Analytics und alle zeitsparenden Kompromisse, die Ihre Organisation eingehen möchte.<p>Um mit der Erstellung Ihres benutzerdefinierten Leitfadens zu beginnen, melden Sie sich bei [!DNL Customer Journey Analytics] an und wählen Sie dann auf der Registerkarte **[!UICONTROL Arbeitsbereich]** die Option **[!UICONTROL Upgrade auf Customer Journey Analytics]** aus.<p>[Weitere Informationen](https://experienceleague.adobe.com/de/docs/analytics-platform/using/compare-aa-cja/upgrade-to-cja/cja-upgrade-recommendations#recommended-upgrade-steps-for-most-organizations) |  | 11. März 2025 |
| **„Nur Data Warehouse“-Dimensionen** | Ab Mai 2025 beginnt Adobe, bestimmte Dimensionen (benutzerdefinierte Variablen wie eVars und Props) als „Nur Data Warehouse“ festzulegen. Dies gilt für Dimensionen mit den folgenden Eigenschaften:<ul><li> Über einen Zeitraum von mehreren Monaten erreicht die Variable innerhalb der ersten Tage des Monats das Limit für geringen Traffic.</li><li>> 90 % der übergebenen Werte werden nur einmal im Monat angezeigt.</li></ul>Beispiele sind Dimensionen mit Zeitstempeln, UUIDs oder anderen Daten, die eine extrem hohe Kardinalität aufweisen und bei denen eindeutige neue Werte für fast jeden Treffer (oder fast jeden Besuch oder fast jede besuchende Person) im Laufe des Monats übergeben werden. Diese Dimensionen überschreiten normalerweise sehr schnell die Limits für geringen Traffic und nur für einen sehr kleinen Teil der Werte können in Analysis Workspace Berichte erstellt werden. Berichte, die diese Dimensionen verwenden, sind dadurch verwirrend, da sie keine nützlichen oder genauen Informationen enthalten. Diese Dimensionen entsprechen nicht dem Zweck der Funktion des geringen Traffics bzw. profitieren nicht von dieser Funktion, die eine Möglichkeit bieten soll, Berichte zu Werten zu erstellen, die „beliebt“ werden, nachdem die Dimension die Limits für geringen Traffic im Laufe des Monats überschritten hat. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/analytics/technotes/low-traffic)<p>Dimensionen, die als „Nur Data Warehouse“ gekennzeichnet sind, sind in Analysis Workspace nicht für Berichte verfügbar. Sie stehen jedoch weiterhin für Berichte über Data Warehouse zur Verfügung, da Limits für geringen Traffics hier nicht gelten.<p>Dies bedeutet nicht, dass jede Dimension, die die Limits für geringen Traffic erreicht hat, als „Nur Data Warehouse“ gekennzeichnet werden kann. Die meisten Dimensionen, die die Limits für geringen Traffic erreichen, erfüllen tatsächlich die Absicht der Funktionalität für geringen Traffic:<ul><li>Die meisten übergebenen Werte sind nicht eindeutig.</li><li>Allgemeine Werte kommen weiter an, nachdem die Limits für geringen Traffic im Laufe des Monats erreicht wurden.</li><li>Neue „beliebte“ Werte können weiterhin auftreten.</li></ul>Nur die Dimensionen, in denen fast alle übergebenen Werte neu und eindeutig sind, werden als „Nur Data Warehouse“ gekennzeichnet. Angesichts der Eindeutigkeit der in diesen Situationen erfassten Daten ist die Erhöhung der Limits für geringen Traffic keine Lösung. | | Mai 2025 |


## Fehlerbehebungen in Adobe Analytics

**Activity Map**: AN-361038
**Admin-Tools**: AN-362178; AN-369483
**Analytics-API 1.4**: AN-369615
**Analysis Workspace**: AN-353491; AN-363403; AN-367230; AN-367313; AN-368582; AN-369821; AN-370227;
**Klassifizierungen**: AN-369848; AN-370196; AN-370226; AN-370437
**Daten-Feeds**: AN-366162; AN-368906; AN-369066; AN-369087; AN-369225; AN-369798
**Data Governance**: AN-365157
**Datenquellen**: AN-367550
**Platform**: AN-363931
**Report Builder**: AN-367460; AN-368975

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Datum hinzugefügt oder aktualisiert | Beschreibung |
| ----------- | ---------- | ---------- |
| -/- |  |  |

## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Migration auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O** | 17. Januar 2025 | Kundinnen und Kunden von Adobe Analytics-API und -Livestream, die JWT-Anmeldeinformationen für Adobe I/O verwenden, müssen bis zum **30. Juni 2025** auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O migrieren. Adobe I/O lässt die Erstellung neuer JWT-Anmeldeinformationen ab dem 1. Mai 2024 nicht mehr zu. Kunden und Kundinnen, die JWT verwenden, müssen neue OAuth Server-zu-Server-Anmeldeinformationen erstellen oder ihre bestehende JWT-Anmeldeinformationen zu OAuth Server-zu-Server-Anmeldeinformationen migrieren. Kunden und Kundinnen müssen außerdem ihre Client-Anwendungen aktualisieren, um die neuen OAuth Server-to-Server-Anmeldeinformationen zu verwenden. <ul><li>[Migration von Dienstkonto-Anmeldeinformationen (JWT)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementierungshandbuch für neue und alte Programme mit OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[Verwenden der neuen OAuth Server-zu-Server-Anmeldeinformationen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Häufig gestellte Fragen (FAQ)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **Ende der Nutzungsdauer für Adobe Analytics-API (Version 1.4)** | 17. Juli 2024 | Ab **12. August 2026** werden die folgenden veralteten Analytics-API-Dienste nicht mehr unterstützt und beendet. Aktuelle Integrationen, die mit diesen Diensten erstellt wurden, funktionieren dann nicht mehr:<ul><li>Adobe Analytics-API (Version 1.4)</li><li>WSSE-Authentifizierung von Adobe Analytics </li></ul><p>Integrationen, die die Adobe Analytics-API (Version 1.4) verwenden, müssen zur [Adobe Analytics 2.0-API](https://developer.adobe.com/analytics-apis/docs/2.0/) migrieren, während WSSE-Integrationen zu einem OAuth-basierten Authentifizierungsprotokoll in der [Adobe Developer Console](https://developer.adobe.com/console) migrieren müssen.</p><p>Antworten auf häufig gestellte Fragen und weitere Anleitungen finden Sie in den [häufig gestellten Fragen zum Ende der Nutzungsdauer der Adobe Analytics 1.4-API](/help/admin/c-admin-api/c-admin-14-api-eol.md).</p> |


## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen finden Sie in den [Versionshinweisen zu AppMeasurement](https://github.com/adobe/appmeasurement/releases).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2025](/help/release-notes/2025.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zur Streaming-Mediensammlung](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
