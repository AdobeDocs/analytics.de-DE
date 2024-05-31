---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 47893ea714f0a0baaccce66578c9f9175c59511f
workflow-type: tm+mt
source-wordcount: '1144'
ht-degree: 99%

---

# Aktuelle Adobe Analytics-Versionshinweise (Mai 2024)

**Letzte Aktualisierung:**: 22. Mai 2024

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom 15. Mai 2024 bis Juni 2024. Die Versionen von Adobe Analytics basieren auf einem [kontinuierlichen Bereitstellungsmodell](releases.md), das eine besser skalierbare, schrittweise Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Neue Dokumentation für die Aktualisierung von Adobe Analytics auf Customer Journey Analytics** | Für Organisationen, die von Adobe Analytics auf Customer Journey Analytics umsteigen möchten, gibt es mehrere Aktualisierungsoptionen und viele Überlegungen, die abhängig von der aktuellen Adobe Analytics-Implementierung und den langfristigen Zielen der Organisation berücksichtigt werden sollten. Es stehen nun neue Dokumentationsressourcen zur Verfügung, die Ihnen helfen, Folgendes besser zu verstehen:<ul><li>Die verschiedenen vorhandenen Aktualisierungspfade</li><li>Welche Aktualisierungspfade auf der Grundlage der aktuellen Adobe Analytics-Implementierung einer Organisation verfügbar sind</li><li>Die Vor- und Nachteile jedes Aktualisierungspfads</li><li>Eine schrittweise Anleitung für jeden Aktualisierungspfad</li><li>Überlegungen zum Umgang mit historischen Daten</li></ul>[Erste Schritte mit dem Upgrade auf Customer Journey Analytics](https://experienceleague.adobe.com/de/docs/analytics-platform/using/compare-aa-cja/upgrade-to-cja/cja-upgrade-getstarted) | | Jetzt verfügbar |
| **Festlegen von `contextData`-Feldern über XDM** | Kundinnen und Kunden, die Daten über das Experience Edge Network an Adobe Analytics senden, können [Kontextdatenwerte](https://experienceleague.adobe.com/de/docs/analytics/implementation/vars/page-vars/contextdata) direkt entweder in XDM oder in den „Daten“-Teilen der Payload festlegen. |  | Jetzt verfügbar |
| **Analytics Real-time-Reporting-API 2.0** | Die neue Real-time-Reporting-API 2.0 in Adobe Analytics verbessert die Kundenintegration und liefert schnelle Reporting-Ergebnisse. Diese Ergebnisse können programmgesteuert für die Arbeit mit einfachen, Trend- und Detailberichten verwendet werden. [Weitere Informationen](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/reports/real-time/) | | 30. Mai 2024 |
| **Streaming-Medien: Senden von Web-Daten mit dem Web SDK an Adobe Experience Platform Edge Network** | Sie können jetzt das Adobe Experience Platform Web SDK verwenden, um Web-Daten zu Streaming-Medien an Adobe Experience Platform Edge Network zu senden. Diese Verbesserung ermöglicht die Erstellung stärker personalisierter Kampagnen und die Bereitstellung stärker personalisierter Inhalte, was zu mehr Tracking-Daten für die Berichterstellung führt.<p>Diese Änderung bietet eine einheitliche Erfassungsmethode für Web-Implementierungen über alle Plattformlösungen hinweg, wie Customer Journey Analytics, Adobe Real-time CDP, Adobe Journey Optimizer und Ereignisweiterleitung. Zuvor bestand die einzige Möglichkeit, Web-Daten zu Streaming-Medien an Edge Network zu senden, in der Verwendung der Media Edge-API. <p>[Weitere Informationen](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/edge-recommended/media-edge-sdk/edge-web-sdk)</p> | | Donnerstag, 29. Mai 2024 |
| **Anhebung der standardmäßigen Schwellenwerte für geringeren Traffic** | **Mitte April 2024** beginnt Adobe mit der Erhöhung der standardmäßigen Report Suite-Schwellenwerte für geringen Traffic wie folgt: ![Schwellenwerte für geringen Traffic](assets/thresholds.png) Dies wirkt sich nur auf Variablen aus, die derzeit unter den neuen Schwellenwerten liegen. Diese Änderungen werden schrittweise vorgenommen und wir gehen davon aus, dass sie bis **Ende Mai** abgeschlossen sind. Wenn diese Erhöhungen eingeführt werden, werden Sie möglicherweise Änderungen bei Variablen mit hoher Kardinalität bemerken:<ul><li>Es können mehr Dimensionswerte für das Reporting verfügbar sein.</li><li>Segmente und berechnete Metriken können weitere Daten enthalten.</li><li>Virtual Report Suites, die auf Segmenten basieren, können mehr Daten enthalten.</li><li>Klassifizierungs-Exporte können mehr Daten enthalten.</li></ul> | Mitte April 2024 | 31. Mai 2024 |
| **Administratoreinstellungen zum Steuern der Konten und Speicherorte, die für den Export und Import verwendet werden** | Eine neue Registerkarte „Admin-Einstellungen“ im Speicherorte-Manager gibt Admins die Kontrolle darüber, ob Benutzende Konten und Speicherorte erstellen und bearbeiten können. Diese Einstellungen gelten, wenn Benutzende Cloud-Import- und -Exportkonten und Cloud-Import- und -Exportspeicherorte konfigurieren. <p>Admins können auch die Kontotypen (Google Cloud Platform, Azure RBAC, Amazon S3 usw.) einschränken, die Benutzende erstellen und verwenden können.</p><p>Zuvor konnten alle Benutzenden Konten und Speicherorte für beliebige Kontotypen erstellen, bearbeiten und verwenden.</p><p>(Link zur aktualisierten Dokumentation folgt)</p> | Donnerstag, 12. Juni 2024 | Montag, 30. Juni 2024 |
| **Freigeben von Konten und Speicherorten, die für den Export und Import verwendet werden** | Benutzende können nun die von ihnen erstellten Konten und Speicherorte allen Benutzenden in ihrer Organisation zur Verfügung stellen. Nur die Personen, denen Konten bzw. Speicherorte gehören, und System-Admins können Konten und Speicherorte bearbeiten und löschen.<p>Zuvor konnten Konten und Speicherorte nur von der Person verwendet werden, die sie erstellt hat.</p><p>Diese Einstellungen sind verfügbar, wenn Benutzende Cloud-Import- und -Exportkonten und Cloud-Import- und -Exportspeicherorte konfigurieren. </p> <p>(Link zur aktualisierten Dokumentation folgt)</p> | Donnerstag, 12. Juni 2024 | Montag, 30. Juni 2024 |
| **Activity Map, um weniger Server-Aufrufe für Web SDK zu verwenden** | Derzeit werden Activity Map-Link-Ereignisse als eigene Ereignisse gezählt und verursachen zusätzliche Kosten. Durch diese Verbesserung werden einige Link-Ereignisse aufgenommen und in den nächsten Treffer gepackt, ähnlich wie bei der Verarbeitung durch AppMeasurement. <p>(Link zur aktualisierten Dokumentation folgt)</p> | Die Beta beginnt am 31. Mai 2024 | TBD |

{style="table-layout:auto"}

## Fehlerbehebungen in Adobe Analytics

* Es wurden folgende Klassifizierungsprobleme behoben: AN-343186; AN-344711; AN-344856; AN-345094; AN-345179; AN-346265; AN-345288; AN-346339; AN-346560; AN-347572; AN-347681; AN-347768; AN-348024
* Die folgenden Data Warehouse-Probleme wurden behoben: AN-346789; AN-347031; AN-347568;
* Die folgenden Data Feeds-Probleme wurden behoben: AN-343616; AN-345831; AN-345988; AN-346124; AN-346232; AN-346972; AN-347680; AN-347755; AN-347954
* Das folgende Datenquellen-Problem wurde behoben: AN-347890;
* Die folgenden Analysis Workspace-Probleme wurden behoben: AN-321503; AN-343103; AN-343471; AN-345171; AN-345223; AN-345912; AN-346026; AN-346330; AN-346839; AN-347679
* Das folgende A4T-Problem wurde behoben: AN-345118;

### Weitere behobene Fehler in Analytics

AN-327749; AN-332949; AN-342881; AN-343171; AN-343708; AN-344034; AN-345559; AN-346023; AN-346230; AN-346330; AN-346469; AN-346606; AN-346750; AN-346973; AN-347026; AN-347110; AN-347439;

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Datum hinzugefügt oder aktualisiert | Beschreibung |
| ----------- | ---------- | ---------- |
| **13-monatige Gültigkeit für gespeicherte`cust_visids`** | 22. Mai 2024 | Eine bevorstehende Version der Analytics-Trefferverarbeitungs-Engine, **deren Freigabe für Juli 2024 geplant ist**, wird damit beginnen, eine 13-monatige Gültigkeit für gespeicherte `cust_visids` durchzusetzen. Wenn „Besucherzuordnung aktivieren“ in der Report Suite aktiviert ist, wird diese Einstellung zum Suchen der `cust_visid` für einen `visid_high/visid_low value` ohne `cust_visid` für den Treffer verwendet. Derzeit gibt es keine Gültigkeit der Zuordnung eines `cust_visid` für einen `visid_high/visid_low`. Mit dieser Version endet die Gültigkeit der Zuordnung, wenn 13 Monate oder mehr vergangen sind, seit `visid_high/visid_low` eine `cust_visid` für einen Treffer hatte. |
| **Aktualisierungen der ISO-Region** | 10. Mai 2024 | Am 7. Juni 2024 wird Adobe die Aktualisierung der ISO-Region 2024 durchführen. Nach dieser Veröffentlichung sind kleinere Aktualisierungen der Geoinformationen (Region) zu erwarten. |

{style="table-layout:auto"}

## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Migration auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O** | 11. Mai 2023 | Kundinnen und Kunden von Adobe Analytics-API und Livestream, die JWT-Anmeldeinformationen für Adobe I/O verwenden, müssen bis zum **1. Januar 2025** auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O migrieren. Adobe I/O lässt die Erstellung neuer JWT-Anmeldeinformationen ab dem 1. Mai 2024 nicht mehr zu. Kunden und Kundinnen, die JWT verwenden, müssen neue OAuth Server-zu-Server-Anmeldeinformationen erstellen oder ihre bestehende JWT-Anmeldeinformationen zu OAuth Server-zu-Server-Anmeldeinformationen migrieren. Kunden und Kundinnen müssen außerdem ihre Client-Anwendungen aktualisieren, um die neuen OAuth Server-to-Server-Anmeldeinformationen zu verwenden. <ul><li>[Migration von Dienstkonto-Anmeldeinformationen (JWT)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementierungshandbuch für neue und alte Programme mit OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[Verwenden der neuen OAuth Server-zu-Server-Anmeldeinformationen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Häufig gestellte Fragen (FAQ)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}

## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.26.0) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2023](/help/release-notes/2023.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
