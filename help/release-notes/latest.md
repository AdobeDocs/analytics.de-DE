---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: ace906a4b5acf1ab667529af33dd5be1618863f2
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 97%

---

# Aktuelle Versionshinweise zu Adobe Analytics (Version Februar 2025)

**Letzte Aktualisierung**: 21. Februar 2025

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom 11. Februar bis Mitte März 2025. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Aufbewahrungszeitraum der Transaktions-ID** | Der Aufbewahrungszeitraum der Transaktions-ID von 90 Tagen wurde auf 25 Monate verlängert. Die Variable `transactionID` identifiziert eine Transaktion eindeutig, sodass der Treffer mit Daten verknüpft werden kann, die über Datenquellen hochgeladen wurden. Weitere Informationen finden Sie [hier](https://experienceleague.adobe.com/de/docs/analytics/implementation/vars/page-vars/transactionid) und [hier](https://experienceleague.adobe.com/de/docs/analytics/import/data-sources/transactionid). |  | 20. Februar 2025 |
| **Referenz zur Daten-Feeds-API** | Die [Referenz](https://adobedocs.github.io/analytics-2.0-apis/?urls.primaryName=Data%20Feeds%20APIs) zur Daten-Feeds-API ist jetzt verfügbar. |  | 30. Januar 2025 |
| **Livestream-API – Client-Implementierung** | Verwenden Sie die Livestream-Client-Implementierung, um Livestream-Daten zu nutzen. [Weitere Informationen](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/livestream/clientcode/) |  | 18. Februar 2025 |
| **Aktualisierung der Klassifizierungs-API** | Sie können jetzt einzelne Klassifizierungsfelder oder -schlüssel vom Server entfernen. Dies bietet eine Alternative zum Löschen eines gesamten Klassifizierungsdatensatzes mit der DELETE-Methode. [Weitere Informationen](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/classifications/remove-values/) |  | 18. Februar 2025 |
| **Aktualisierung des Analytics-Kontextdatenfelds`a.locale`** | Durch eine geplante Aktualisierung ändert sich die Art und Weise, wie das Analytics-Kontextdatenfeld `a.locale` bei der Datenerfassung über Experience Edge festgelegt wird. Wenn Daten mit Experience Edge an Adobe Analytics gesendet werden, werden Analytics-Felder basierend auf einer Zuordnung von XDM-Feldern ausgefüllt. Die Zuordnung für `c.a.locale` verweist auf ein nicht standardmäßiges XDM-Feld (`xdm.environment.language`). Dieses Feld wird aktualisiert, um auf das richtige Feld (`xdm.environment._dc.language`) zu verweisen.<p>Aus Gründen der Abwärtskompatibilität verweist die Zuordnung weiterhin auf `xdm.environment.language`. Um eine Kontinuität sicherzustellen, hat `xdm.environment.language` Vorrang, wenn beide Felder festgelegt sind. Die vollständige Liste der Zuordnungen von XDM zu standardmäßigen Analytics-Feldern finden Sie [hier](https://experienceleague.adobe.com/de/docs/analytics/implementation/aep-edge/xdm-var-mapping). | | 5. März 2025 |


## Fehlerbehebungen in Adobe Analytics

**Analysis Workspace**: AN-359974; AN-366212; AN-368460
**Klassifizierungen**: AN-367186; AN-367328; AN-368548
**Komponentenmigration** AN-364529; AN-366398; AN-367509;
**Daten-Feeds**: AN-365685; AN-366745; AN-367256; AN-367349; AN-368363
**Data Warehouse**: AN-368178; AN-368331;
**App**: AN-367137
**Platform**: AN-351924; AN-365540; AN-365866; AN-366898; AN-367856; AN-367933
**Report Builder**: AN-366456; AN-366655;
**Virtual Report Suites**: AN-367411
**VISTA-Regeln**: AN-365331

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Datum hinzugefügt oder aktualisiert | Beschreibung |
| ----------- | ---------- | ---------- |
| **Kundinnen und Kunden ohne Adobe Campaign verlieren den Zugriff auf Trigger** | 16. Oktober 2023 | Seit 30. Januar 2025 haben Adobe Analytics-Kundinnen und -Kunden, die keine Adobe Campaign-Lizenz haben, nicht mehr die Möglichkeit, [Trigger](https://experienceleague.adobe.com/de/docs/core-services/interface/services/triggers) zu konfigurieren und zu nutzen. Kundinnen und Kunden müssen entweder Campaign erwerben, die Nutzung von Triggers in Zukunft einstellen oder sich mit anderen Adobe-Tools befassen, die Funktionen von Triggers bieten. |

## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Migration auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O** | 17. Januar 2025 | Kundinnen und Kunden von Adobe Analytics-API und -Livestream, die JWT-Anmeldeinformationen für Adobe I/O verwenden, müssen bis zum **30. Juni 2025** auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O migrieren. Adobe I/O lässt die Erstellung neuer JWT-Anmeldeinformationen ab dem 1. Mai 2024 nicht mehr zu. Kunden und Kundinnen, die JWT verwenden, müssen neue OAuth Server-zu-Server-Anmeldeinformationen erstellen oder ihre bestehende JWT-Anmeldeinformationen zu OAuth Server-zu-Server-Anmeldeinformationen migrieren. Kunden und Kundinnen müssen außerdem ihre Client-Anwendungen aktualisieren, um die neuen OAuth Server-to-Server-Anmeldeinformationen zu verwenden. <ul><li>[Migration von Dienstkonto-Anmeldeinformationen (JWT)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementierungshandbuch für neue und alte Programme mit OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[Verwenden der neuen OAuth Server-zu-Server-Anmeldeinformationen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Häufig gestellte Fragen (FAQ)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **Ende der Nutzungsdauer für Adobe Analytics-API (Version 1.4)** | 17. Juli 2024 | Ab **12. August 2026** werden die folgenden veralteten Analytics-API-Dienste nicht mehr unterstützt und beendet. Aktuelle Integrationen, die mit diesen Diensten erstellt wurden, funktionieren dann nicht mehr:<ul><li>Adobe Analytics-API (Version 1.4)</li><li>WSSE-Authentifizierung von Adobe Analytics </li></ul><p>Integrationen, die die Adobe Analytics-API (Version 1.4) verwenden, müssen zur [Adobe Analytics 2.0-API](https://developer.adobe.com/analytics-apis/docs/2.0/) migrieren, während WSSE-Integrationen zu einem OAuth-basierten Authentifizierungsprotokoll in der [Adobe Developer Console](https://developer.adobe.com/console) migrieren müssen.</p><p>Antworten auf häufig gestellte Fragen und weitere Anleitungen finden Sie in den [häufig gestellten Fragen zum Ende der Nutzungsdauer der Adobe Analytics 1.4-API](/help/admin/c-admin-api/c-admin-14-api-eol.md).</p> |


## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.27.0) finden Sie in den Versionshinweisen zu [AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2024](/help/release-notes/2024.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zur Streaming-Mediensammlung](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
