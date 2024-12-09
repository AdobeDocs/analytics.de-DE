---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 2a766fc06cab81c2b1d4b8a4de2c88dae42bf907
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 97%

---

# Aktuelle Adobe Analytics-Versionshinweise (Version vom 23. Oktober 2024)

**Letztes Update**: Dienstag, 9. Dezember 2024

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom 16. Oktober 2024 bis Ende 2024. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Neuer Report Builder für Adobe Analytics** | Die neue Anwendung Report Builder bietet eine umfassende Aktualisierung für Adobe Analytics, beispielsweise verbesserte Leistung, eine optimierte Benutzeroberfläche, Unterstützung für 2.0 API und Unterstützung für Microsoft Excel unter Mac, Windows und in Webbrowsern. Diese Anwendung kann zusammen mit der Vorgängeranwendung verwendet werden, jedoch nicht in derselben Datei. Mit einer Aktualisierungsfunktion können ältere Arbeitsmappen auf die neue Anwendung aktualisiert werden. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/analytics/analyze/report-builder/report-buider-overview) |  | 16. Oktober 2024 |
| **JSON-Export für die Migration der Tag-Implementierung zu Web SDK-Tags** | Diese Aktualisierung der Analytics-Tag-Erweiterung bezieht sich auf die Migration zu Web SDK. Sie können dieses Update für die Adobe Analytics-Erweiterung als Teil Ihres Workflows verwenden, um Ihre Erweiterungskonfigurationen mit der Web SDK-Erweiterung neu zu erstellen. In der Adobe Analytics-Tag-Erweiterung können Sie eVars-, Props- und Ereigniseinstellungen als JSON anzeigen, die zur Bearbeitung exportiert und in die Web SDK-Erweiterung aufgenommen werden können. |  | 31. Oktober 2024 |
| **Neue Informationen zu Anfragefaktoren bei der Leistung von Analysis Workspace** | Bei der Leistungsanalyse in Analysis Workspace ist jetzt ein neuer Abschnitt „Anfragefaktoren“ verfügbar. Weitere Informationen zur Verarbeitung von Anfragen und zu den verschiedenen Faktoren, die die Verarbeitungszeiten beeinflussen, finden Sie unter „Anfragefaktoren“ unter [Optimieren der Analysis Workspace-Leistung](https://experienceleague.adobe.com/de/docs/analytics/analyze/analysis-workspace/workspace-faq/optimizing-performance). |  | 1. Oktober 2024 |
| **Aufbewahrungszeitraum der Transaktions-ID** | Die `transactionID`-Variable identifiziert eine Transaktion eindeutig, sodass der Treffer mit Daten verknüpft werden kann, die über Data Sources hochgeladen wurden. Der standardmäßige Aufbewahrungszeitraum der ID von 90 Tagen wird im Januar 2025 auf 25 Monate verlängert. |  | Donnerstag, 22. Januar 2025 |

## Fehlerbehebungen in Adobe Analytics

Analysis Workspace: AN-356287; AN-358435; AN-359456; AN-359826; AN-360215
Admin-Tools: AN-342485; AN-347931; AN-348704; AN-357723; AN-358453; AN-358717; AN-359548; AN-360136
Klassifizierungen: AN-359025; AN-359283; AN-359368; AN-359710; AN-359752; AN-359759; AN-359799; AN-359887; AN-360543; AN-360566; AN-360612; AN-360741; AN-360942; AN-360952
Geräteübergreifende Analyse: AN-359210
Kundenattribute: AN-357897
Datenerfassung: AN-351131; AN-351309; AN-355678; AN-359856
Daten-Feeds: AN-359699
Datenreparatur-API: AN-360256
Datenquellen: AN-359290
Data Warehouse: AN-359820
Überlastungs-Warnhinweise: AN-358132

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Datum hinzugefügt oder aktualisiert | Beschreibung |
| ----------- | ---------- | ---------- |
| **Kundinnen und Kunden ohne Adobe Campaign verlieren den Zugriff auf Trigger** | 16. Oktober 2023 | Am 30. Januar 2025 verlieren Adobe Analytics-Kundinnen und -Kunden, die keine Adobe Campaign-Lizenz haben, den Zugriff auf die Möglichkeit, Trigger zu konfigurieren und zu nutzen. Kundinnen und Kunden müssen entweder Campaign erwerben, die Nutzung von Triggern in Zukunft einstellen oder sich andere Adobe-Tools ansehen, die Trigger-Funktionen bieten. |
| **Automatische Zuordnung von XDM-Feldern mit zusätzlichen Implementierungsdetails** | 11. September 2024 | Wenn Sie Adobe Experience Platform Edge Network zum Senden von Daten an Adobe Analytics verwenden, werden die XDM-Felder `xdm.implementationdetails.name` und `xdm.implementationdetails.environment` nun immer den Kontextdatenvariablen `c.a.x.implementationdetails.name` und `c.a.x.implementationdetails.environment` zugeordnet. Früher wurde bei bestimmten Szenarien verhindert, dass diese Werte ausgefüllt werden. Passen Sie die relevanten Verarbeitungsregeln an, damit diese Werte verfügbar sind. |

## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Ende der Nutzungsdauer für Adobe Analytics-API (Version 1.4)** | 17. Juli 2024 | Ab **12. August 2026** werden die folgenden veralteten Analytics-API-Dienste nicht mehr unterstützt und beendet. Aktuelle Integrationen, die mit diesen Diensten erstellt wurden, funktionieren dann nicht mehr:<ul><li>Adobe Analytics-API (Version 1.4)</li><li>WSSE-Authentifizierung von Adobe Analytics </li></ul><p>Integrationen, die die Adobe Analytics-API (Version 1.4) verwenden, müssen zur [Adobe Analytics 2.0-API](https://developer.adobe.com/analytics-apis/docs/2.0/) migrieren, während WSSE-Integrationen zu einem OAuth-basierten Authentifizierungsprotokoll in der [Adobe Developer Console](https://developer.adobe.com/console) migrieren müssen.</p><p>Antworten auf häufig gestellte Fragen und weitere Anleitungen finden Sie in den [häufig gestellten Fragen zum Ende der Nutzungsdauer der Adobe Analytics 1.4-API](/help/admin/c-admin-api/c-admin-14-api-eol.md).</p> |
| **Migration auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O** | 11. Mai 2023 | Kundinnen und Kunden von Adobe Analytics-API und Livestream, die JWT-Anmeldeinformationen für Adobe I/O verwenden, müssen bis zum **1. Januar 2025** auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O migrieren. Adobe I/O lässt die Erstellung neuer JWT-Anmeldeinformationen ab dem 1. Mai 2024 nicht mehr zu. Kunden und Kundinnen, die JWT verwenden, müssen neue OAuth Server-zu-Server-Anmeldeinformationen erstellen oder ihre bestehende JWT-Anmeldeinformationen zu OAuth Server-zu-Server-Anmeldeinformationen migrieren. Kunden und Kundinnen müssen außerdem ihre Client-Anwendungen aktualisieren, um die neuen OAuth Server-to-Server-Anmeldeinformationen zu verwenden. <ul><li>[Migration von Dienstkonto-Anmeldeinformationen (JWT)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementierungshandbuch für neue und alte Programme mit OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[Verwenden der neuen OAuth Server-zu-Server-Anmeldeinformationen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Häufig gestellte Fragen (FAQ)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |


## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.26.0) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2024](/help/release-notes/2024.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zum Add-on für Streaming-Mediensammlungen](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
