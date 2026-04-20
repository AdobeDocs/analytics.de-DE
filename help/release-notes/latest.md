---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 7a245e2c24e8763c93150aa5b9f3ac2d197f6f1f
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 100%

---

# Aktuelle Adobe Analytics-Versionshinweise (April 2026)

**Letztes Update**: Freitag, 9. April 2026

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom April 2026. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion und Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ---- |
| **MCP-Server für Adobe Analytics** <br/>Sie können Adobe Analytics jetzt mithilfe von MCP (Model Context Protocol) in Ihre bestehenden Agent-basierten Workflows einbinden. Sie können Berichte und Erkenntnisse in natürlicher Sprache anfordern.<p>(Link zur Dokumentation folgt.)</p> | | Ende April 2026 |
| **Streaming-Mediendienste: Unterstützung von Zeitplandaten** <br/>Sie können jetzt Zeitplandaten von früheren Live-Inhalten von Streaming-Medien hochladen, um Zuschauerzahlen einfacher und genauer zu verfolgen.<p>Im Folgenden finden Sie Beispiele für Live-Inhalte, die mit dem Upload von Zeitplandaten unterstützt werden:</p><ul><li>FAST-Plattformen (Free Ad Supported TV)</li><li>Lokale Datenströme</li><li>Live-Sportübertragungen</li></ul><p>Durch das Hochladen von Zeitplandaten können Sie die Zuschauerzahlen für einzelne Programme verfolgen, die in dem von Ihnen in der Upload-Datei angegebenen Zeitraum gelaufen sind. Sie können sogar Zuschauerzahlen für bestimmte Themen oder Programmsegmente erfassen.</p><p>Diese Funktionen sind unabhängig davon verfügbar, wie Sie die Erfassung von Streaming-Medien implementiert haben.</p><p>Zuvor war es bei der Analyse von Live-Inhalten schwierig, eine bestimmte Sitzung genau mit bestimmten Programmen zu verknüpfen, und es war nicht möglich, eine bestimmte Sitzung mit einzelnen Themen oder Programmsegmenten zu verknüpfen.</p><p>Weitere Informationen finden Sie unter [Hochladen von Zeitplandaten zum Nachverfolgen von Live-Inhalten](https://experienceleague.adobe.com/de/docs/media-analytics/using/media-use-cases/track-schedule-data)</p> | &#x200B;29. Oktober 2025 | Erstes Halbjahr 2026<p>(Veröffentlichung ursprünglich für den 29. Oktober 2025 geplant)</p> |
| **Zusätzliche API-Datumsbereichsformatierung**<br/> Für die Angabe von Datumsbereichen in Analytics 2.0-API-Berichtsanfragen werden jetzt zwei neue Formate unterstützt. Dazu gehören eine Datumsformel und ein gemischtes Format. [Weitere Informationen](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/reports/#date-range-field--supported-formats) | | März 2026 |
| **Optionale Dimension in API-Berichtsanfragen**<br/> Ein Dimensionsobjekt ist in API-Berichtsanfragen nicht erforderlich. Wenn keine Dimension angegeben ist, werden in der Antwort Daten für einen Bericht mit Gesamtwerten angezeigt. [Weitere Informationen](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/reports/#using-dimension-in-report-payload-requests) | | März 2026 |
| **Erweiterter API-Bericht mit Datumstrends**<br/> Neuer erweiterter Bericht mit Datumstrends für die Adobe Analytics 2.0 API. Erstellen Sie erweiterte API-Berichte mit Datumstrends mithilfe von Datumsbereichsvergleichen und Segmenten. [Weitere Informationen](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/reports/advanced/) | | März 2026 |

## Fehlerbehebungen in Adobe Analytics

**Activity Map**:
**Analysis Workspace**: AN-442813, AN-442410, AN-441943, AN-441717, AN-434855, AN-431409, AN-429777, AN-429048, AN-428892, AN-428189, AN-425215
**Klassifizierungen**: AN-443453, AN-443275, AN-443148, AN-442906, AN-442232, AN-442207, AN-442148, AN-442133, AN-441937, AN-441901, AN-441807, AN-441671, AN-441333, AN-441302, AN-441149, AN-441132, AN-441085, AN-441048, AN-440846, AN-440727, AN-440716, AN-440511, AN-440496, AN-432100
**Daten-Feeds und Data Warehouse**: AN-442211, AN-441719, AN-441183, AN-441011, AN-440625, AN-438953
**Migration**: AN-442467, AN-440380, AN-440357
**Exporte**:
**Report Builder**: AN-441136, AN-438147, AN-425150
**Reporting**: AN-441506, AN-440919, AN-440545, AN-440300
**Report Suites**: AN-439429, AN-439423, AN-430988
**Terminierte Berichte**:
**Segmentierung**:
**Sonstige**: AN-423359, AN-406242, AN-397985


## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Verbesserungen bei der Livestream-Verarbeitung** | Donnerstag, 14. Januar 2026 | Adobe plant Verbesserungen und Änderungen an der Formatierung von LiveStream-Payloads. Diese Aktualisierungen bieten eine bessere Parität zwischen LiveStream und anderen Adobe Analytics-Funktionen wie Analysis Workspace. Es ist ein Vorschauendpunkt verfügbar, mit dem Sie die geplanten Änderungen testen können. Die vollständige Liste der Änderungen und Details zum Vorschauendpunkt finden Sie unter [LiveStream-Versionshinweise](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/livestream/release-notes/). Adobe plant die feste Umstellung auf das aktualisierte Payload-Format für den 13. April 2026. |
| **Entfernung von TLS 1.2 Cipher Suites** | &#x200B;11. Februar 2026 | Hinweis für Admins: Adobe plant, am 27. Mai 2026 die Unterstützung für die folgenden TLS 1.2 Cipher Suites von den Adobe-Datenerfassungs-Servern zu entfernen.<ul><li>`TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA`</li><li>`TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA`</li><li>`TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA`</li><li>`TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA`</li><li>`TLS_RSA_WITH_AES_128_CBC_SHA`</li><li>`TLS_RSA_WITH_AES_256_CBC_SHA`</li><li>`TLS_RSA_WITH_AES_128_GCM_SHA256`</li><li>`TLS_RSA_WITH_AES_256_GCM_SHA384`</li></ul><p>Bei den meisten Implementierungen ist keine Kundenaktion erforderlich. Diese Änderung betrifft in erster Linie Analytics-Daten, die von veralteten nativen Anwendungen gesendet werden, die veraltete TLS-Bibliotheken verwenden, sowie eine geringe Anzahl von Web-Besucherinnen und -Besuchern mit veralteten Browsern oder Betriebssystemen. Das Entfernen der Unterstützung für diese Cipher Suites erhöht die Sicherheit und sorgt dafür, dass Adobe moderne Verschlüsselungsstandards einsetzt. Weniger als 0,1 % des Datenerfassungs-Traffics beruht derzeit auf diesen Cipher Suites.</p> |
| **Vorgängerversion von Report Builder** | 18. Juni 2025 | Die Vorgängerversion des Report Builder-Add-ins wird im Juni 2026 eingestellt. Alle Benutzenden sollten mit dem Upgrade ihrer Arbeitsmappen der Vorgängerversion auf den [neuen Report Builder](/help/analyze/report-builder/rb-overview.md) beginnen. Der neue Report Builder ist sowohl für Adobe Analytics- als auch für Customer Journey Analytics-Kundschaft verfügbar. Er bietet [nahezu die gleichen Funktionen](/help/analyze/report-builder/convert-workbooks.md#unsupported) sowie viele neue, praktische Funktionen und Verbesserungen der Benutzeroberfläche. Um den Upgrade-Prozess zu vereinfachen, enthält der neue Report Builder eine Funktion zur einfachen Arbeitsmappenkonvertierung. Der neue Report Builder ist nur als Add-in über den Microsoft Store verfügbar. Viele Organisationen benötigen einen internen Genehmigungsprozess, bevor das Add-in Benutzenden zur Verfügung gestellt werden kann. Planen Sie Zeit für diesen Prozess ein und arbeiten Sie jetzt mit Ihrer Organisation, um vor dem Ende der Nutzungsdauer genügend Zeit für ein Upgrade Ihrer Arbeitsmappen zu haben. |
| **Zugriff über Legacy-Domains oder Legacy-SSO** | 10. April 2025 | Adobe plant, die Art und Weise zu aktualisieren, wie Benutzende auf Adobe Analytics zugreifen, um die Sicherheit zu erhöhen und das Anmeldeerlebnis zu optimieren. Im Rahmen dieser Bemühungen wird der Zugriff über Legacy-Domains oder Legacy-SSO, einschließlich `my.omniture.com`, am **2. Januar 2026** dauerhaft eingestellt. Nach diesem Datum funktionieren die alten Anmeldedaten bzw. die alte SSO-Methode nicht mehr. Alle Benutzenden müssen sich über `experience.adobe.com` mit ihren Adobe Experience Cloud-IDs anmelden. Wenn Sie Hilfe im Zusammenhang mit Ihrer Experience Cloud-ID benötigen, wenden Sie sich an das Adobe Analytics-Admin-Team Ihrer Organisation oder an die [Adobe-Kundenunterstützung](https://helpx.adobe.com/de/contact.html). |
| **Adobe Analytics-API (Version 1.4)** | 17. Juli 2024 | Ab **12. August 2026** werden die folgenden veralteten Analytics-API-Dienste nicht mehr unterstützt und beendet. Aktuelle Integrationen, die mit diesen Diensten erstellt wurden, funktionieren dann nicht mehr:<ul><li>Adobe Analytics-API (Version 1.4)</li><li>WSSE-Authentifizierung von Adobe Analytics</li></ul><p>Integrationen, die die Adobe Analytics-API (Version 1.4) verwenden, müssen zur [Adobe Analytics 2.0-API](https://developer.adobe.com/analytics-apis/docs/2.0/) migrieren, während WSSE-Integrationen zu einem OAuth-basierten Authentifizierungsprotokoll in der [Adobe Developer Console](https://developer.adobe.com/console) migrieren müssen.</p><p>Antworten auf häufig gestellte Fragen und weitere Anleitungen finden Sie in den [häufig gestellten Fragen zum Ende der Nutzungsdauer der Adobe Analytics 1.4-API](https://developer.adobe.com/analytics-apis/docs/1.4/guides/eol/).</p> |


## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen finden Sie in den [Versionshinweisen zu AppMeasurement](https://github.com/adobe/appmeasurement/releases).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2025](/help/release-notes/2025.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Streaming-Mediendiensten](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
