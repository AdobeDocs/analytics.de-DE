---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 9fcebd7a8fb3a3d98eebef53a748c8ac585cbcd1
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 96%

---

# Aktuelle Adobe Analytics-Versionshinweise (Juni 2024)

**Letzte Aktualisierung**: 13. Juni 2024

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom 12. Juni 2024 bis Juli 2024. Die Versionen von Adobe Analytics basieren auf einem [kontinuierlichen Bereitstellungsmodell](releases.md), das eine besser skalierbare, schrittweise Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Auswählen mehrerer Felder in einem Dropdown-Filter** | Wenn einem Dropdown-Filter mehrere Felder hinzugefügt wurden, können Benutzende jetzt mehrere Felder gleichzeitig auswählen. Das Panel wird gefiltert, um eines der ausgewählten Felder einzuschließen. <p>Zuvor konnte in einem Dropdown-Filter jeweils nur ein Feld ausgewählt werden.</p><p>Weitere Informationen finden Sie unter [Statische Dropdown-Segmente](/help/analyze/analysis-workspace/c-panels/panels.md#static-drop-down-segments) in [Bedienfelder - Übersicht](/help/analyze/analysis-workspace/c-panels/panels.md).</p> |  | 19. Juni 2024 |
| **Inhaltsverzeichnis für Workspace-Projekte** | Für Projekte ist jetzt ein neues Inhaltsverzeichnis verfügbar. Das Inhaltsverzeichnis enthält Links, über die Benutzende schnell zu Panels und Visualisierungen innerhalb des Projekts springen können. Das Inhaltsverzeichnis kann für einzelne Projekte oder für alle Projekte einer bestimmten Person aktiviert werden.<p>Weitere Informationen finden Sie unter [Inhaltsverzeichnis des Projekts](/help/analyze/analysis-workspace/build-workspace-project/project-table-of-contents.md).</p> |  | 19. Juni 2024 |
| **Erstellen von Hyperlinks für Dimensionselemente in einer Freiformtabelle** | Sie können Hyperlinks für ein oder mehrere Dimensionselemente erstellen, damit sie in einer Freiformtabelle in Analysis Workspace angeklickt werden können. <p>Sie können Hyperlinks für Dimensionselemente erstellen, die URL-Werte aufweisen, oder Sie können benutzerdefinierte URLs für Dimensionselemente erstellen, die Nicht-URL-Werte haben.</p><p>Sie können dynamische, benutzerdefinierte URLs für mehrere Dimensionselemente mithilfe von Variablen erstellen. Variablen können auf den Wert eines Dimensionselements oder auf die Aufschlüsselungsdimension verweisen.</p><p>Weitere Informationen finden Sie unter [Erstellen von Hyperlinks für Dimensionen in einer Freiformtabelle](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table-hyperlinks.md).</p> |  | 19. Juni 2024 |
| **Administratoreinstellungen zum Steuern der Konten und Speicherorte, die für den Export und Import verwendet werden** | Eine neue Registerkarte [„Admin-Einstellungen“ im Speicherorte-Manager](/help/components/locations/locations-manager.md#configure-company-wide-settings-administrators-only) gibt Admins die Kontrolle darüber, ob Benutzende Konten und Speicherorte erstellen und bearbeiten können. Diese Einstellungen gelten, wenn Benutzende [Konten für den Cloud-Import und -Export](/help/components/locations/configure-import-accounts.md) und [Speicherorte für den Cloud-Import und -Export](/help/components/locations/configure-import-locations.md) konfigurieren. <p>Admins können auch die Kontotypen (Google Cloud Platform, Azure RBAC, Amazon S3 usw.) einschränken, die Benutzende erstellen und verwenden können.</p><p>Zuvor konnten alle Benutzenden Konten und Speicherorte für beliebige Kontotypen erstellen, bearbeiten und verwenden.</p> | 12. Juni 2024 | 30. Juni 2024 |
| **Freigeben von Konten und Speicherorten, die für den Export und Import verwendet werden** | Benutzende können nun die von ihnen erstellten Konten und Speicherorte allen Benutzenden in ihrer Organisation zur Verfügung stellen. Nur die Personen, denen Konten bzw. Speicherorte gehören, und System-Admins können Konten und Speicherorte bearbeiten und löschen.<p>Zuvor konnten Konten und Speicherorte nur von der Person verwendet werden, die sie erstellt hat.</p><p>Diese Einstellungen sind verfügbar, wenn Benutzende [Konten für den Cloud-Import und -Export](https://experienceleague.adobe.com/de/docs/analytics/components/locations/configure-import-accounts) und [Speicherorte für den Cloud-Import und -Export](https://experienceleague.adobe.com/de/docs/analytics/components/locations/configure-import-locations) konfigurieren. </p> | 12. Juni 2024 | 30. Juni 2024 |
| **Activity Map, um weniger Server-Aufrufe für Web SDK zu verwenden** | Derzeit werden Activity Map-Link-Ereignisse als eigene Ereignisse gezählt und verursachen zusätzliche Kosten. Durch diese Verbesserung werden einige Link-Ereignisse aufgenommen und in den nächsten Treffer gepackt, ähnlich wie bei der Verarbeitung durch AppMeasurement. <p>(Link zur aktualisierten Dokumentation folgt)</p> | Open Beta beginnt am 19. Juni 2024 | TBD |

{style="table-layout:auto"}

## Fehlerbehebungen in Adobe Analytics

* Es wurden folgende Klassifizierungsprobleme behoben: AN-347682; AN-348396; AN-348625; AN-348668; AN-348926; AN-348936; AN-349040; AN-349191; AN-349195; AN-349443; AN-349697; AN-349758; AN-349862; AN-350051; AN-350054; AN-350208; AN-350497; AN-350525; AN-351067
* Es wurden die folgenden Data Warehouse-Probleme behoben: AN-346862; AN-349409; AN-349926; AN-350629; AN-350996
* Es wurden die folgenden Probleme mit Daten-Feeds behoben: AN-346727; AN-348282; AN-348334; AN-348725; AN-348726; AN-348823; AN-349081; AN-349207; AN-349307; AN-349539; AN-349710; AN-349729; AN-349742; AN-349878; AN-349943; AN-350527
* Es wurde das folgende Problem mit Datenquellen behoben: AN-350038.
* Es wurden die folgenden Probleme mit Analysis Workspace behoben: AN-342953; AN-346346; AN-349590; AN-349717; AN-350057; AN-350697; AN-350904
* Es wurden die folgenden Report Builder-Probleme behoben: AN-348903; AN-350691
* Es wurden die folgenden A4T-Probleme behoben: AN-347690, AN-350853.

### Weitere behobene Fehler in Analytics

AN-346470; AN-346850; AN-347227; AN-348145; AN-348564; AN-349001; AN-349008; AN-349211; AN-349719; AN-350523

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

* [Frühere Versionshinweise für 2024](/help/release-notes/2024.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
