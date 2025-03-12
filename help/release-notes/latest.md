---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 2b13f649d286e9eb707f2dd22c068b9742c51c70
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 54%

---

# Aktuelle Versionshinweise zu Adobe Analytics (Version März 2025)

**Zuletzt aktualisiert**: Donnerstag, 12. März 2025

Diese Versionshinweise decken den Veröffentlichungszeitraum vom 5. März bis Mai 2025 ab. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Aktualisierung des Analytics-Kontextdatenfelds`a.locale`** | Diese Aktualisierung ändert die Art und Weise, wie das Analytics-Kontextdatenfeld `a.locale` bei der Datenerfassung über Experience Edge festgelegt wird. Wenn Daten mit Experience Edge an Adobe Analytics gesendet werden, werden Analytics-Felder basierend auf einer Zuordnung von XDM-Feldern ausgefüllt. Die Zuordnung für `c.a.locale` verweist auf ein nicht standardmäßiges XDM-Feld (`xdm.environment.language`). Dieses Feld wird aktualisiert, um auf das richtige Feld (`xdm.environment._dc.language`) zu verweisen.<p>Aus Gründen der Abwärtskompatibilität verweist die Zuordnung weiterhin auf `xdm.environment.language`. Wenn beide Felder festgelegt sind, hat für die Kontinuität der Wert &quot;`xdm.environment.language`&quot; Vorrang. Die vollständige Liste der Zuordnungen von XDM zu standardmäßigen Analytics-Feldern finden Sie [hier](https://experienceleague.adobe.com/de/docs/analytics/implementation/aep-edge/xdm-var-mapping). | | 5. März 2025 |
| **Customer Journey Analytics-Aktualisierungshandbuch** | Ermöglicht die Erstellung einer schrittweisen Anleitung für die Aktualisierung von Adobe Analytics auf Customer Journey Analytics. Dieser Leitfaden ist auf Ihr Unternehmen zugeschnitten und berücksichtigt Ihre aktuelle Adobe Analytics-Umgebung, Ihre Verwendungszwecke für Customer Journey Analytics und alle zeitsparenden Kompromisse, die Ihr Unternehmen erzielen möchte.<p>Um mit der Erstellung Ihres benutzerdefinierten Handbuchs zu beginnen, melden Sie sich bei [!DNL Customer Journey Analytics] an und wählen Sie dann **[!UICONTROL Upgrade auf Customer Journey Analytics]** auf der Registerkarte **[!UICONTROL Workspace]** aus.<p>[Weitere Informationen](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/upgrade-to-cja/cja-upgrade-recommendations#recommended-upgrade-steps-for-most-organizations) |  | Mittwoch, 11. März 2025 |
| **Dimensionen, die nur Data Warehouse betreffen** | Ab Mai 2025 beginnt Adobe mit dem Festlegen von Dimensionen (benutzerdefinierte Variablen wie eVars und Props), die eine extrem hohe Kardinalität auf „nur Data Warehouse&quot; aufweisen. Variablen mit hoher Kardinalität haben viele verschiedene Werte. Beispiele sind Zeitstempel oder UUIDs. Diese Dimensionen werden nicht mehr für das Reporting in Analysis Workspace verfügbar sein.<p>Kandidaten für diese Änderung sind Dimensionen, die die niedrigen Traffic-Grenzwerte sehr früh im Monat überschreiten. Bei diesen Dimensionstypen sind Berichte in Analysis Workspace, die auf dieser Dimension basieren, nicht hilfreich, da die berichtspflichtigen Daten nur einen dünnen Abschnitt der erfassten Ausgangswerte darstellen.<p>Da Data Warehouse keine niedrigen Traffic-Beschränkungen vorsieht, können Sie dennoch nützliche Berichte oder Segmente basierend auf diesen Dimensionstypen erstellen. | | Mai 2025 |


## Fehlerbehebungen in Adobe Analytics

**Activity Map**: AN-361038
**Admin Tools**: AN-362178; AN-369483
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

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.27.0) finden Sie in den Versionshinweisen zu [AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2025](/help/release-notes/2025.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zur Streaming-Mediensammlung](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
