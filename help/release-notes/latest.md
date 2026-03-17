---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: d61dc175eed0737ce8fc43506712dedf5341367c
workflow-type: tm+mt
source-wordcount: '1291'
ht-degree: 52%

---

# Aktuelle Adobe Analytics-Versionshinweise (Märzi 2026)

**Letztes Update**: Donnerstag, 11. März 2026

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom März 2026. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals monatlich aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion und Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ---- |
| **Sortieren von Tabellen nach mehreren Spalten** <br/>Sie können jetzt die Daten einer Freiformtabelle in Analysis Workspace nach mehreren Spalten sortieren, unabhängig davon, ob es sich um Dimensionen oder Metriken handelt.<p>Wenn Sie Daten für mehrere Spalten sortieren, werden die Daten nach der Priorität sortiert, die Sie jeder Spalte zuweisen. Die Prioritätsnummerierung wird neben dem Sortiersymbol angezeigt.</p><p>Weitere Informationen finden Sie unter [Filtern und Sortieren von Freiformtabellen](/help/analyze/analysis-workspace/visualizations/freeform-table/filter-and-sort.md).</p> | Donnerstag, 28. Januar 2026 | Donnerstag, 4. März 2026 <p>(Ursprünglich für den 18. Februar 2026 geplant)</p> |
| **Report Builder: Administratorsichtbarkeit für alle geplanten Arbeitsmappen**<br/> Das Report Builder Excel-Add-in enthält eine neue Filteroption, mit der Administratoren alle geplanten Arbeitsmappen für eine bestimmte Organisation anzeigen können, unabhängig davon, wer sie geplant hat. Diese Filteroption ist nur für Analytics-Admins verfügbar. Er ist sowohl auf der Registerkarte „Arbeitsmappe“ als auch auf der Registerkarte „Legacy“ verfügbar, wenn geplante Arbeitsmappen angezeigt werden.<p>Die Möglichkeit, alle geplanten Arbeitsmappen anzuzeigen, ist besonders bei der Migration von Arbeitsmappen über verteilte Teams hinweg nützlich, da Admins dadurch alle alten Arbeitsmappen vor der Migration leicht finden können.</p><p>Zuvor konnten Admins nur die von ihnen geplanten Arbeitsmappen sehen, nicht die von anderen Benutzern geplanten.</p><p>Weitere Informationen finden Sie unter [Verwaltete geplante Arbeitsmappen](/help/analyze/report-builder/manage-schedules-reportbuilder.md).</p> | | Mittwoch, 10. März 2026 |
| **Aktualisierung zur Funktion „Ungefährer Distinct Count**<br/> Der HLL-probabilistische Algorithmus, der in der Funktion „Ungefährer Distinct Count“ verwendet wird, wird bald aktualisiert. Die resultierende Ausgabe für Zahlen, die diese Funktion verwenden, kann sich wie folgt geringfügig von historischen Zahlen unterscheiden:</p><ul><li>Beim Zählen sehr kleiner Mengen eindeutiger Werte werden die Ergebnisse dahingehend verbessert, dass genaue Zählungen anstelle von Schätzungen verwendet werden.</li><li>Wenn Sie etwas Größeres zählen, behalten Zählschätzungen dieselbe Genauigkeit wie vor dieser Aktualisierung bei (Schätzungen sind innerhalb von 5 Prozent der exakten Zahl genau, 95 Prozent der Zeit).</li></ul><p>Weitere Informationen zur Funktion Ungefährer Distinct Count finden Sie unter [Ungefährer Distinct Count](/help/components/calculated-metrics/cm-reference/cm-adv-functions.md#approximate-count-distinct) unter [Erweiterte Funktionen](/help/components/calculated-metrics/cm-reference/cm-adv-functions.md)</p> | | Mittwoch, 10. März 2026 |
| **Praktisches Tutorial für Analysis Workspace**<br/> Ein neues praktisches Tutorial, das neue Benutzende durch die Grundlagen der Verwendung von Bedienfeldern, Visualisierungen und Komponenten in Analysis Workspace führt, ist jetzt verfügbar. <p>Weitere Informationen finden Sie unter [Adobe Analytics-Landingpage](/help/analyze/landing.md).</p> | | Donnerstag, 18. März 2026 |
| **Aufschlüsselung auf ein Bedienfeld anwenden**<br/> Sie können jetzt eine Aufschlüsselung auf ein Bedienfeld anwenden. Wenn Sie eine Aufschlüsselung auf Bedienfeldebene anwenden, wird die Aufschlüsselung auf alle Spalten in allen Freiformtabellen innerhalb des Bedienfelds angewendet. | März 2026 | Mai 2026 |
| **Streaming-Medien-Services: Unterstützung von Zeitplandaten** <br/>Sie können jetzt geplante Daten vergangener Live-Streaming-Medien-Inhalte hochladen, um die Zuschauerzahlen einfacher und genauer zu verfolgen.<p>Im Folgenden finden Sie Beispiele für Live-Inhalte, die mit dem Upload von Zeitplandaten unterstützt werden:</p><ul><li>FAST-Plattformen (Free Ad Supported TV)</li><li>Lokale Datenströme</li><li>Live-Sportübertragungen</li></ul><p>Durch das Hochladen von Zeitplandaten können Sie die Zuschauerzahlen für einzelne Programme verfolgen, die in dem von Ihnen in der Upload-Datei angegebenen Zeitraum gelaufen sind. Sie können sogar Zuschauerzahlen für bestimmte Themen oder Programmsegmente erfassen.</p><p>Diese Funktionen sind unabhängig davon verfügbar, wie Sie die Erfassung von Streaming-Medien implementiert haben.</p><p>Zuvor war es bei der Analyse von Live-Inhalten schwierig, eine bestimmte Sitzung genau mit bestimmten Programmen zu verknüpfen, und es war nicht möglich, eine bestimmte Sitzung mit einzelnen Themen oder Programmsegmenten zu verknüpfen.</p><p>Weitere Informationen finden Sie unter [Hochladen von Zeitplandaten zum Nachverfolgen von Live-Inhalten](https://experienceleague.adobe.com/de/docs/media-analytics/using/media-use-cases/track-schedule-data)</p> | &#x200B;29. Oktober 2025 | Erstes Halbjahr 2026<p>(Veröffentlichung ursprünglich für den 29. Oktober 2025 geplant)</p> |

## Fehlerbehebungen in Adobe Analytics

**Activity Map**:
**Analysis Workspace**: AN-440336, AN-440216, AN-440121, AN-438445, AN-438216, AN-437856, AN-437776, AN-437765, AN-437365, AN-432793, AN-431557, AN-431200, AN-429621, AN-429424, AN-432094, AN-427973, AN-426089, AN-425883, AN-424359
**Klassifizierungen**: AN-440143, AN-439891, AN-439844, AN-438994, AN-438057, AN-438052, AN-437986, AN-437896, AN-435387, AN-435335, AN-435150, AN-433050, AN-432062, AN-431873, AN-429642
**Daten-Feeds und Data Warehouse**: AN-439441, AN-437086, AN-433064, AN-432121, AN-431755, AN-428239, AN-427049, AN-425036, AN-424972, AN-423509, AN-335417, AN-283958, AN-256948
**Migration**:
**Exporte**: AN-432030
**Report Builder**: AN-437895, AN-437083, AN-434288, AN-434209, AN-433224, AN-430622
**Reporting**: AN-434545, AN-431206, AN-428043
**Terminierte Berichte**:
**Segmentierung**:
**Sonstige**: AN-440076, AN-434783, AN-434542, AN-434233, AN-433368, AN-432138, AN-431322, AN-431012, AN-429067, AN-423285


## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Verbesserungen bei der Livestream-Verarbeitung** | Donnerstag, 14. Januar 2026 | Adobe plant Verbesserungen und Änderungen an der Formatierung von LiveStream-Payloads. Diese Aktualisierungen bieten eine bessere Parität zwischen LiveStream und anderen Adobe Analytics-Funktionen wie Analysis Workspace. Es ist ein Vorschauendpunkt verfügbar, mit dem Sie die geplanten Änderungen testen können. Die vollständige Liste der Änderungen und Details zum Vorschauendpunkt finden Sie unter [LiveStream-Versionshinweise](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/livestream/release-notes/). Adobe plant die feste Umstellung auf das aktualisierte Payload-Format für den 13. April 2026. |
| **Entfernung von TLS 1.2 Cipher Suites** | Donnerstag, 11. Februar 2026 | Hinweis für Administratoren: Adobe plant, die Unterstützung für die folgenden TLS 1.2-Chiffrier-Suites von den Adobe-Datenerfassungs-Servern am 27. Mai 2026 einzustellen.<ul><li>`TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA`</li><li>`TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA`</li><li>`TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA`</li><li>`TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA`</li><li>`TLS_RSA_WITH_AES_128_CBC_SHA`</li><li>`TLS_RSA_WITH_AES_256_CBC_SHA`</li></ul><p>Bei den meisten Implementierungen ist keine Kundenaktion erforderlich. Diese Änderung betrifft in erster Linie Analytics-Daten, die von veralteten nativen Programmen gesendet werden, die veraltete TLS-Bibliotheken verwenden, sowie eine geringe Anzahl von Web-Besuchern in veralteten Browsern oder Betriebssystemen. Die Aufhebung der Unterstützung für diese Chiffrier-Suites erhöht die Sicherheit und stimmt Adobe mit modernen Verschlüsselungsstandards ab. Weniger als 0,1 % des Datenerfassungs-Traffics beruht derzeit auf diesen Chiffrier-Suites.</p> |
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
