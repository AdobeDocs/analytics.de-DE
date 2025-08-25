---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 7609ecb3c34fb0bc8293fc1ecd409cfabb327295
workflow-type: tm+mt
source-wordcount: '1147'
ht-degree: 90%

---

# Aktuelle Adobe Analytics-Versionshinweise (Version August 2025)

**Letzte Aktualisierung**: 13. August 2025

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom 13. August bis 16. September 2025. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Analysieren von KI-Traffic mit einem neuen Dimensionselement vom Referrer-Typ** | Im Oktober wird ein neues Dimensionselement vom Referrer-Typ zur Verfügung stehen, um den von KI-Tools stammenden Traffic zu analysieren. <p>Dieses neue Dimensionselement vom Referrer-Typ namens Conversational AI-Tools gruppiert verweisende Domains der wichtigsten KI-Tools und ermöglicht es Ihnen, Trends für die Gruppe als Ganzes zu betrachten. Die anfängliche Liste der verweisenden Domains in dieser neuen Kategorie umfasst (ist jedoch nicht auf beschränkt auf):</p><ul><li>chatgpt.com</li><li>claude.ai</li><li>m365.cloud.microsoft</li><li>grok.com</li><li>gemini.google.com</li><li>perplexity.ai</li></ul><p>Das neue Dimensionselement ist in allen Adobe Analytics-bezogenen Tools verfügbar, einschließlich Analysis Workspace, Report Builder, Data Warehouse, Daten-Feeds usw.</p><p>Beachten Sie bei der Verwendung dieses neuen Dimensionselements Folgendes:</p><ul><li>Es ist nicht immer möglich, den Referrer-Traffic, der aus den Ergebnissen im „KI-Modus” einer Suchmaschine stammt, von dem Traffic zu unterscheiden, der aus Klicks auf herkömmliche Suchergebnisse stammt.</li><li>Das neue Dimensionselement der Conversational AI-Tools konzentriert sich auf die wichtigsten Anbieter mit dem meisten Traffic. Ein neuer Trend zeigt eine steigende Anzahl von imitierenden Sites mit Domains, die denen großer Anbieter von KI-Tools ähneln. Das liegt wahrscheinlich daran, dass einzelne Personen oder Gruppen sehr einfach eigene KI-Tools erstellen und im Internet hosten können. Da sich dieser Bereich schnell weiterentwickelt, wenden Sie sich an das Adobe-Support-Team, wenn Ihnen auffällt, dass eine beliebte Website nicht enthalten ist.</li><li>Die Dimension vom Referrer-Typ, einschließlich des neuen Dimensionselements „Conversational AI-Tools“, ist nur bei Daten verfügbar, die von Adobe Analytics verarbeitet werden. </li></ul><p>(Link zur Dokumentation folgt.)</p> |   | Oktober 2025 |
| **Als PDF heruntergeladene Projekte werden auf Ihre Workstation heruntergeladen** | Beim Herunterladen eines Projekts als PDF wird die PDF-Datei in den Ordner „Downloads“ auf Ihrer Workstation heruntergeladen. <p>Bisher wurde die PDF-Datei in einem neuen Browser-Tab mit einer eindeutigen URL geöffnet, wenn Sie ein Projekt als PDF heruntergeladen haben. </p><p>Weitere Informationen finden Sie unter [Herunterladen von Projekten und Daten](/help/analyze/analysis-workspace/curate-share/download-send.md)</p> |  | &#x200B;25. August 2025 |
| **Gelöschte Projekte sind sofort danach nicht mehr über ihre URL verfügbar und werden aus terminierten Bereitstellungen gelöscht** | Gelöschte Projekte werden sofort aus den terminierten Bereitstellungen gelöscht und sind über ihre URL nicht mehr zugänglich.<p>Zuvor waren Projekte in terminierte Bereitstellungen eingeschlossen und konnten nach dem Löschen noch 60 Tage lang über ihre URL aufgerufen werden.</p><p>Weitere Informationen zum Löschen von Projekten finden Sie unter [Überblick über Projekte](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md).</p> | | Ende August 2025 |
| **Streaming-Mediendienste: Aktualisierte XDM-Felder zum Erfassen von Streaming-Mediendaten in Adobe Experience Platform** | Beim Erfassen von Streaming-Mediendaten in Adobe Experience Platform sollten die XDM-Feldpfade, die unter der Überschrift „XDM-Feldpfad“ der Dokumentation zu Streaming-Medienparametern angezeigt werden, nicht mehr verwendet werden. Stattdessen müssen Kundinnen und Kunden, die den Analytics-Quell-Connector implementiert haben, um Streaming-Mediendaten in Platform vor dem 9. Mai 2025 zu erfassen, ihre vorhandenen Konfigurationen in die mediaReporting-Feldpfade migrieren, wie unter der Überschrift „XDM-Feldpfad für Berichterstellung“ der Dokumentation zu Streaming-Medienparametern gezeigt.<p> Diese Feldpfade befinden sich auf den folgenden Seiten und sind als „veraltet“ gekennzeichnet: [Audio- und Videoparameter](https://experienceleague.adobe.com/de/docs/media-analytics/using/implementation/variables/audio-video-parameters), [Anzeigenparameter](https://experienceleague.adobe.com/de/docs/media-analytics/using/implementation/variables/ad-parameters), [Kapitelparameter](https://experienceleague.adobe.com/de/docs/media-analytics/using/implementation/variables/chapter-parameters), [Player-Statusparameter](https://experienceleague.adobe.com/de/docs/media-analytics/using/implementation/variables/player-state-parameters) und [Qualitätsparameter](https://experienceleague.adobe.com/de/docs/media-analytics/using/implementation/variables/quality-parameters). (Bei Kundinnen und Kunden, die den Analytics-Quell-Connector nach dem 9. Mai 2025 implementiert haben und bereits nur XDM-Pfade für mediaReporting verwenden, ist keine Aktion erforderlich.)</p><p>Die Datenaufnahme über die veralteten XDM-Feldpfade wird noch bis Ende Oktober 2025 fortgesetzt. Danach werden die veralteten Felder vollständig entfernt und nicht mehr in der Schema-Benutzeroberfläche von Adobe Experience Platform angezeigt. Daten werden nur mithilfe der mediaReporting-Feldpfade gesendet.</p><p>Weitere Informationen finden Sie unter [Migrieren einer Analytics Source Connector-Implementierung in aktualisierte XDM Streaming Media-Felder](https://experienceleague.adobe.com/de/docs/media-analytics/using/media-use-cases/xdm-updates/updated-xdm-fields).</p><p>Wenden Sie sich an Ihren Adobe Consulting-Dienst oder Ihr Konto-Team, um Unterstützung bei der Migration zu erhalten.  </p> |  | Oktober 2025 |

## Fehlerbehebungen in Adobe Analytics

**Activity Map**: AN-389205; AN-384186
**Analysis Workspace**: AN-390102; AN-389066; AN-388841; AN-388687; AN-388478; AN-387089; AN-387044; AN-384560; AN-379213; AN-351639
**Klassifizierungen** AN-390442; AN-390385; AN-389953; AN-389703; AN-389321; AN-389116; AN-388833; AN-388717; AN-387987; AN-383329
**Datenerfassung**: AN-389320
**Daten-Feeds und Data Warehouse**: AN-389702; AN-388136; AN-387779; AN-384369; AN-383075; AN-380307
**Datenschutz**:
**Report Builder**: AN-389336; AN-382775
**Reporting**: AN-390398
**Terminierte Berichte**:
**Segmentvergleich**:
**Sonstige**: AN-388180; AN-383164; AN-366532


## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Vorgängerversion von Report Builder** | 18. Juni 2025 | Die Vorgängerversion des Report Builder-Add-ins wird im Juni 2026 eingestellt. Alle Benutzenden sollten mit dem Upgrade ihrer Arbeitsmappen der Vorgängerversion auf den [neuen Report Builder](https://experienceleague.adobe.com/de/docs/analytics/analyze/report-builder/rb-overview) beginnen. Der neue Report Builder ist sowohl für Adobe Analytics- als auch für Customer Journey Analytics-Kundschaft verfügbar. Er bietet [nahezu die gleichen Funktionen](https://experienceleague.adobe.com/de/docs/analytics/analyze/report-builder/convert-workbooks#unsupported) sowie viele neue, praktische Funktionen und Verbesserungen der Benutzeroberfläche. Um den Upgrade-Prozess zu vereinfachen, enthält der neue Report Builder eine Funktion zur einfachen Arbeitsmappenkonvertierung. Der neue Report Builder ist nur als Add-in über den Microsoft Store verfügbar. Viele Organisationen benötigen einen internen Genehmigungsprozess, bevor das Add-in Benutzenden zur Verfügung gestellt werden kann. Planen Sie Zeit für diesen Prozess ein und arbeiten Sie jetzt mit Ihrer Organisation, um vor dem Ende der Nutzungsdauer genügend Zeit für ein Upgrade Ihrer Arbeitsmappen zu haben. |
| **Zugriff über Legacy-Domains oder Legacy-SSO** | 10. April 2025 | Adobe plant, die Art und Weise zu aktualisieren, wie Benutzende auf Adobe Analytics zugreifen, um die Sicherheit zu erhöhen und das Anmeldeerlebnis zu optimieren. Im Rahmen dieser Bemühungen wird der Zugriff über Legacy-Domains oder Legacy-SSO, einschließlich `my.omniture.com`, am **2. Januar 2026** dauerhaft eingestellt. Nach diesem Datum funktionieren die alten Anmeldedaten bzw. die alte SSO-Methode nicht mehr. Alle Benutzenden müssen sich über `experience.adobe.com` mit ihren Adobe Experience Cloud-IDs anmelden. Wenn Sie Hilfe im Zusammenhang mit Ihrer Experience Cloud-ID benötigen, wenden Sie sich an das Adobe Analytics-Admin-Team Ihrer Organisation oder an die [Adobe-Kundenunterstützung](https://helpx.adobe.com/de/contact.html). |
| **Adobe Analytics-API (Version 1.4)** | 17. Juli 2024 | Ab **12. August 2026** werden die folgenden veralteten Analytics-API-Dienste nicht mehr unterstützt und beendet. Aktuelle Integrationen, die mit diesen Diensten erstellt wurden, funktionieren dann nicht mehr:<ul><li>Adobe Analytics-API (Version 1.4)</li><li>WSSE-Authentifizierung von Adobe Analytics </li></ul><p>Integrationen, die die Adobe Analytics-API (Version 1.4) verwenden, müssen zur [Adobe Analytics 2.0-API](https://developer.adobe.com/analytics-apis/docs/2.0/) migrieren, während WSSE-Integrationen zu einem OAuth-basierten Authentifizierungsprotokoll in der [Adobe Developer Console](https://developer.adobe.com/console) migrieren müssen.</p><p>Antworten auf häufig gestellte Fragen und weitere Anleitungen finden Sie in den [häufig gestellten Fragen zum Ende der Nutzungsdauer der Adobe Analytics 1.4-API](/help/admin/c-admin-api/c-admin-14-api-eol.md).</p> |


## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen finden Sie in den [Versionshinweisen zu AppMeasurement](https://github.com/adobe/appmeasurement/releases).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2025](/help/release-notes/2025.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Streaming Media Services](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
