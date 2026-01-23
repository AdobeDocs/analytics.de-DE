---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 58098a24e826161bbd7aadb98abe050fd944791e
workflow-type: tm+mt
source-wordcount: '1221'
ht-degree: 49%

---

# Aktuelle Adobe Analytics-Versionshinweise (Januar 2026)

**Letzte Aktualisierung:** Donnerstag, 14. Januar 2026

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom Januar 2026. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Rule Builder für Klassifizierungssätze** | [Rule Builder](/help/components/classifications/sets/manage/rules.md) Funktion ist jetzt in Klassifizierungssätzen verfügbar. Sie definieren Regeln im Kontext eines Klassifizierungssatzes. Regeln werden (wenn aktiviert) auf alle Report Suite- und Schlüssel-Dimensionskombinationen angewendet, die für den Klassifizierungssatz abonniert wurden.</p> |  | Samstag, 23. Januar 2026 |
| **Verbesserte Daten-Feeds** | Die folgenden Verbesserungen sind jetzt für Daten-Feeds verfügbar:<ul><li>Verbessertes Benutzererlebnis.</li><li>Neues Erlebnis zum Erstellen und Verwalten von Spaltenvorlagen.</li><li>Sie können jetzt auswählen, wann eine Spaltenvorlage für die Wiederverwendung in zukünftigen Daten-Feeds erstellt werden soll. Sie können Vorlagen auch löschen, bearbeiten und kopieren.<br/>Zuvor führte jeder erstellte Daten-Feed zu einer neuen Spaltenvorlage, was dazu führte, dass eine große Anzahl nicht verwendeter Spaltenvorlagen vorhanden war und es keine Möglichkeit gab, sie zu löschen oder zu verwalten.</li><li>Hinzufügen und Filtern nach Tags.</li><li>Anzeigen des Verlaufs von Daten-Feed-Aufträgen. (Beginn und Ende des Anfragezeitraums usw.)</li><li>Daten-Feeds erneut senden oder verarbeiten. (Auf der Seite Vorgangsverlauf )</li><li>Verspätete Treffer zulassen. Sie können jetzt Daten einbeziehen, die nach Abschluss der Verarbeitung von Daten durch den Daten-Feed innerhalb der festgelegten Reporting-Häufigkeit eingegangen sind.</li><li>Bei der Auswahl eines Enddatums für einen Daten-Feed wird das von Ihnen gewählte Enddatum als letzter Tag des Daten-Feeds eingeschlossen.<br/>Zuvor wurde das Enddatum aus dem Daten-Feed ausgeschlossen.</li><li>Eine Exportfrequenz von 15 Minuten ist jetzt möglich, aber standardmäßig nicht verfügbar. Damit diese Option in Ihrer Umgebung verfügbar wird, müssen Sie sich zunächst an die Adobe-Kundenunterstützung wenden und anfordern, dass Ihre Report Suite für die Unterstützung von 15-Minuten-Exporten konfiguriert ist.</li></ul><p>**Hinweis:** Mit diesen Verbesserungen werden auch die URLs zu Daten-Feed-Seiten in Adobe Analytics aktualisiert. Bitte aktualisieren Sie alle vorhandenen Lesezeichen, um bis zum 30. April 2026 auf die neuen Daten-Feeds-Seiten zu verweisen.</p>(Link zur Dokumentation folgt.)</p> | Mittwoch, 20. Januar 2026 | Mittwoch, 10. Februar 2026 |
| **Sortieren von Tabellen nach mehreren Spalten** | Sie können jetzt die Daten einer Freiformtabelle in Analysis Workspace nach mehreren Spalten sortieren, unabhängig davon, ob es sich um Dimensionen oder Metriken handelt.<p>Wenn Sie Daten für mehrere Spalten sortieren, werden die Daten nach der Priorität sortiert, die Sie jeder Spalte zuweisen. Die Prioritätsnummerierung wird neben dem Sortiersymbol angezeigt.</p><p>(Link zur Dokumentation folgt.)<!-- For more information, see "Filter and sort freeform tables". (need to move info to this article from "Include multiple dimension columns in a freeform table") --></p> | Donnerstag, 28. Januar 2026 | Donnerstag, 18. Februar 2026 |
| **Streaming-Mediendienste: Unterstützung von Zeitplandaten** | Sie können jetzt Zeitplandaten von früheren Live-Inhalten von Streaming-Medien hochladen, um die Zuschauerzahlen einfacher und genauer zu verfolgen.<p>Im Folgenden finden Sie Beispiele für Live-Inhalte, die mit dem Upload von Zeitplandaten unterstützt werden:</p><ul><li>FAST-Plattformen (Free Ad Supported TV)</li><li>Lokale Datenströme</li><li>Live-Sportübertragungen</li></ul><p>Durch das Hochladen von Zeitplandaten können Sie die Zuschauerzahlen für einzelne Programme verfolgen, die in dem von Ihnen in der Upload-Datei angegebenen Zeitraum gelaufen sind. Sie können sogar Zuschauerzahlen für bestimmte Themen oder Programmsegmente erfassen.</p><p>Diese Funktionen sind unabhängig davon verfügbar, wie Sie die Erfassung von Streaming-Medien implementiert haben.</p><p>Zuvor war es bei der Analyse von Live-Inhalten schwierig, eine bestimmte Sitzung genau mit bestimmten Programmen zu verknüpfen, und es war nicht möglich, eine bestimmte Sitzung mit einzelnen Themen oder Programmsegmenten zu verknüpfen.</p><p>Weitere Informationen finden Sie unter [Hochladen von Zeitplandaten zum Nachverfolgen von Live-Inhalten](https://experienceleague.adobe.com/de/docs/media-analytics/using/media-use-cases/track-schedule-data)</p> | &#x200B;29. Oktober 2025 | Erstes Halbjahr 2026<p>(Veröffentlichung ursprünglich für den 29. Oktober 2025 geplant)</p> |

## Fehlerbehebungen in Adobe Analytics

**Activity Map**:
**Analysis Workspace**: AN-423389, AN-422636, AN-422482, AN-422027, AN-421134, AN-420187, AN-406271, AN-406188, AN-405997, AN-405983, AN-405796, AN-404893, AN-404871, AN-404842, AN-404713, AN-404502, AN-404353, AN-405033, AN-404352, AN-404048, AN-402523, AN-396149, AN-390990, AN-390728, AN-390646, AN-383484, AN-376980, AN-371729, AN-347570, AN-
**Classifications**: AN-423985, AN-423092, AN-423067, AN-422913, AN-422908, AN-422793, AN-422785, AN-422745, AN-422705, AN-422422, AN-422077, AN-422058, AN-421999, AN-421698, AN-421351, AN-422126, AN-406583, AN-422098, AN-406295, AN-406123, AN-406052, AN-AN-404743 404372, AN-ALL
**Datenerfassung**: AN-422488
**Daten-Feeds und Data Warehouse**: AN-423186, AN-422789, AN-422239, AN-421552, AN-421393, AN-421339, AN-421231, AN-420149, AN-406345, AN-406217, AN-405073, AN-404822, AN-404774, AN-389691
**Datenschutz**:
**Report Builder**: AN-422120, AN-421937, AN-406296, AN-402951, AN-399748
**Reporting**:
**Terminierte Berichte**: AN-423087, AN-422686
**Segmentvergleich**:
**Sonstige**: AN-423401, AN-422819, AN-422775, AN-422626, AN-422238, AN-422160, AN-422071, AN-421687, AN-420045, AN-404891, AN-404608, AN-390912


## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Verbesserungen bei der Livestream-Verarbeitung** | Donnerstag, 14. Januar 2026 | Adobe plant Verbesserungen und Änderungen an der Formatierung von LiveStream-Payloads. Diese Aktualisierungen bieten eine bessere Parität zwischen LiveStream und anderen Adobe Analytics-Funktionen wie Analysis Workspace. Es ist ein Vorschau-Endpunkt verfügbar, mit dem Sie die geplanten Änderungen testen können. Siehe [LiveStream-Versionshinweise] für die vollständige Liste der Änderungen und Details zum Vorschau-Endpunkt. Adobe plant für den 13. April 2026 eine feste Umstellung auf das aktualisierte Payload-Format. |
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
