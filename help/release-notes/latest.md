---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: a7a80fc9845382eaa5b15dc6c325015de0a0cd9e
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 99%

---

# Aktuelle Adobe Analytics-Versionshinweise (Version März 2025)

**Zuletzt aktualisiert**: 12. März 2025

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom 5. März bis Mai 2025. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Aktualisierung des Analytics-Kontextdatenfelds`a.locale`** | Durch diese Aktualisierung ändert sich die Art und Weise, wie das Analytics-Kontextdatenfeld `a.locale` bei der Datenerfassung über Experience Edge festgelegt wird. Wenn Daten mit Experience Edge an Adobe Analytics gesendet werden, werden Analytics-Felder basierend auf einer Zuordnung von XDM-Feldern ausgefüllt. Die Zuordnung für `c.a.locale` verweist auf ein nicht standardmäßiges XDM-Feld (`xdm.environment.language`). Dieses Feld wird aktualisiert, um auf das richtige Feld (`xdm.environment._dc.language`) zu verweisen.<p>Aus Gründen der Abwärtskompatibilität verweist die Zuordnung weiterhin auf `xdm.environment.language`. Um die Kontinuität sicherzustellen, hat `xdm.environment.language` Vorrang, falls beide Felder festgelegt sind. Die vollständige Liste der Zuordnungen von XDM zu standardmäßigen Analytics-Feldern finden Sie [hier](https://experienceleague.adobe.com/de/docs/analytics/implementation/aep-edge/xdm-var-mapping). | | 5. März 2025 |
| **Leitfaden für das Upgrade auf Customer Journey Analytics** | Ermöglicht die Erstellung eines schrittweisen Leitfadens für das Upgrade von Adobe Analytics auf Customer Journey Analytics. Dieser Leitfaden ist auf Ihre Organisation zugeschnitten und berücksichtigt Ihre aktuelle Adobe Analytics-Umgebung, die vorgesehenen Verwendungszwecke für Customer Journey Analytics und alle zeitsparenden Kompromisse, die Ihre Organisation eingehen möchte.<p>Um mit der Erstellung Ihres benutzerdefinierten Leitfadens zu beginnen, melden Sie sich bei [!DNL Customer Journey Analytics] an und wählen Sie dann auf der Registerkarte **[!UICONTROL Arbeitsbereich]** die Option **[!UICONTROL Upgrade auf Customer Journey Analytics]** aus.<p>[Weitere Informationen](https://experienceleague.adobe.com/de/docs/analytics-platform/using/compare-aa-cja/upgrade-to-cja/cja-upgrade-recommendations#recommended-upgrade-steps-for-most-organizations) |  | 11. März 2025 |
| **„Nur Data Warehouse“-Dimensionen** | Ab Mai 2025 beginnt Adobe, Dimensionen (benutzerdefinierte Variablen wie eVars und Props) festzulegen, die eine extrem hohe Kardinalität vom Typ „Nur Data Warehouse“ aufweisen. Variablen mit hoher Kardinalität haben viele verschiedene Werte. Beispiele dafür sind Zeitstempel oder UUIDs. Diese Dimensionen werden nicht mehr für das Reporting in Analysis Workspace verfügbar sein.<p>Für diese Änderung infrage kommen Dimensionen, die die Grenzwerte für geringen Traffic zu einem sehr frühen Zeitpunkt im Monat überschreiten. Bei diesen Dimensionstypen sind Berichte in Analysis Workspace, die auf dieser Dimension basieren, nicht hilfreich, da die berichtsfähigen Daten nur einen sehr kleinen Teil der erfassten Ausgangswerte darstellen.<p>Da Data Warehouse keine Grenzwerte für geringen Traffic vorsieht, können Sie trotzdem nützliche Berichte oder Segmente auf Grundlage dieser Dimensionstypen erstellen. | | Mai 2025 |


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

Die neuesten Aktualisierungen zu AppMeasurement-Versionen finden Sie in den Versionshinweisen zu [AppMeasurement für JavaScript](https://github.com/adobe/appmeasurement/releases).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2025](/help/release-notes/2025.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zur Streaming-Mediensammlung](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
