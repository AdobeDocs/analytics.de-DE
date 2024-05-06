---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 7468463e2fe1de16221b4528919b6abd6c8aedcb
workflow-type: ht
source-wordcount: '1445'
ht-degree: 100%

---

# Aktuelle Adobe Analytics-Versionshinweise (April 2024)

**Letzte Aktualisierung**: 17. April 2024

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom 17. April 2024 bis Mai 2024. Die Versionen von Adobe Analytics basieren auf einem [kontinuierlichen Bereitstellungsmodell](releases.md), das eine besser skalierbare, schrittweise Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Streaming-Medien: Senden von Roku-Daten an Adobe Experience Platform Edge Network** | Bei der [Installation von Media Analytics mit Experience Platform Edge](https://experienceleague.adobe.com/de/docs/media-analytics/using/implementation/edge-recommended/media-edge-sdk/implementation-edge) können Sie jetzt das Adobe Experience Platform Roku SDK verwenden, um Streaming-Medien-Daten an Adobe Experience Platform zu senden. |  | 12. April 2024 |
| **Verbesserter Workflow für die Web SDK-Migration** | Bei Datenströmen werden nun automatisch Felder aus dem Web SDK-Datenobjekt direkt Adobe Analytics zugeordnet. Die [Datenobjektzuordnung](/help/implement/aep-edge/data-var-mapping.md) ähnelt der [XDM-Objektzuordnung](/help/implement/aep-edge/xdm-var-mapping.md), erfordert jedoch kein XDM-Schema. Dieser verbesserte Workflow bietet folgende Vorteile:<ul><li>Die Verwendung eines Schemas wird so lange verzögert, bis Sie bereit sind, Daten an Adobe Experience Platform zu senden. Wenn in dieser Phase der Implementierungsmigration ein Schema erforderlich war, mussten Sie ein Schema verwenden, das auf Adobe Analytics-Feldern basiert. Adobe Experience Platform-Dienste wie Customer Journey Analytics haben kein Props- oder eVars-Konzept. Ein Analytics-orientiertes Schema kann Probleme verursachen, wenn Ihre Organisation in Zukunft ein eigenes Schema verwenden möchte.</li><li>Nachdem Sie die Implementierungsänderungen am Web SDK vorgenommen haben, ist Ihre Organisation besser in der Lage, von Adobe Analytics zu Customer Journey Analytics zu migrieren. Wenn Sie Daten mit dem Web SDK an Adobe Analytics senden, müssen Sie für den Datenversand an Adobe Experience Platform keine zusätzlichen Implementierungsänderungen vornehmen. Stattdessen können Sie mittels Datenvorbereitung Datenobjektfelder Ihrem XDM-Schema zuordnen.</li></ul>Weitere Informationen finden Sie unter [Migrieren von der Adobe Analytics-Tag-Erweiterung zur Web SDK-Tag-Erweiterung](/help/implement/aep-edge/web-sdk/analytics-extension-to-web-sdk.md) und [Migrieren von AppMeasurement zum Web SDK](../implement/aep-edge/web-sdk/appmeasurement-to-web-sdk.md). |  | April 2024 |
| **Erweiterung der Berechtigungen für projektspezifische [!UICONTROL Arbeitsbereich]-Komponenten** | Wenn eine Benutzerin oder ein Benutzer (Person A) zuvor ein Projekt für eine andere Benutzerin bzw. einen anderen Benutzer (Person B) freigegeben und Person B Bearbeitungszugriff auf das Projekt gewährt hat, konnte Person B das Projekt bearbeiten. Person B war jedoch nicht in der Lage, die im Projekt eingebetteten [!UICONTROL Schnellsegmente] zu bearbeiten. Diese Einschränkung ist nun aufgehoben - Person B kann nun [!UICONTROL Schnellsegmente] und andere projektspezifische Komponenten bearbeiten, die in das freigegebene Projekt eingebettet sind. |  | 17. April 2024 |
| **Verwenden derselben Cloud-Konten für [!UICONTROL Daten-Feeds], [!UICONTROL Data Warehouse] und [!UICONTROL Klassifizierungssätze]** | Von Ihnen erstellte Cloud-Konten und -Speicherorte können nun zum Exportieren von Daten (mit [!UICONTROL Daten-Feeds] und [!UICONTROL Data Warehouse]) und zum Importieren von Daten (mit [!UICONTROL Klassifizierungssätzen]) verwendet werden.<p> **Änderungen beim Konfigurieren von Konten**: Benutzende können [Cloud-Import- und -Exportkonten konfigurieren](https://experienceleague.adobe.com/de/docs/analytics/components/locations/configure-import-accounts) und [Cloud-Import- und -Exportspeicherorte konfigurieren](https://experienceleague.adobe.com/de/docs/analytics/components/locations/configure-import-locations), die für einen der folgenden Zwecke verwendet werden können:<ul><li>Importieren von Daten mit [!UICONTROL Klassifizierungssätzen]</li><li>Exportieren von Daten mit [!UICONTROL Daten-Feeds]</li><li>Exportieren von Daten mit [!UICONTROL Data Warehouse]</li></ul><p>**Änderungen bei der Verwaltung von Konten und Speicherorten über die Seite [!UICONTROL Speicherorte]**: Benutzende können die Seite [Speicherorte](https://experienceleague.adobe.com/de/docs/analytics/components/locations/locations-manager) (unter [!UICONTROL Komponenten] > Speicherorte) verwenden, um alle von ihnen erstellten Konten und Speicherorte anzuzeigen und zu verwalten, unabhängig davon, wo sie erstellt wurden. <p>Zuvor galt die Seite [!UICONTROL Speicherorte] nur für Konten, die zum Importieren von Daten mit [!UICONTROL Klassifizierungssätzen] erstellt wurden.</p>**Änderungen bei der Verwaltung von Speicherorten über [!UICONTROL Data Warehouse] oder [!UICONTROL Klassifizierungssätze]**<p>Bei der Verwaltung von Speicherorten innerhalb eines bestimmten Anwendungsbereichs ([!UICONTROL Data Warehouse] oder [!UICONTROL Klassifizierungssätze]) sind nur die in diesem spezifischen Anwendungsbereich erstellten Speicherorte verfügbar. Bei Anzeige des Anwendungsbereichs [!UICONTROL Data Warehouse] sind beispielsweise nur [!UICONTROL Data Warehouse]-Speicherorte verfügbar. Alle Konten sind weiterhin in jedem Anwendungsbereich verfügbar, unabhängig vom Anwendungsbereich, in dem sie erstellt wurden. Bislang waren alle Konten und Speicherorte in jedem Anwendungsbereich verfügbar, unabhängig vom Anwendungsbereich, in dem sie erstellt wurden. Dies gilt auch bei der Anzeige des Anwendungsbereichs [!UICONTROL Daten-Feeds]. | | 17. April 2024 |
| **Verwaltung aller Speicherorte und Konten in der Organisation durch Admins** | Eine neue Option auf der Registerkarte „Speicherorte“ (auf der Seite „Komponenten“ > „Speicherorte“) ermöglicht es Admins, alle Speicherorte in der Organisation anzuzeigen und zu verwalten.<p>Eine neue Option auf der Registerkarte [Speicherort-Konten](https://experienceleague.adobe.com/de/docs/analytics/components/locations/locations-manager) (auf der Seite „Komponenten“ > „Speicherorte“) ermöglicht es Admins, alle Konten in der Organisation anzuzeigen und zu verwalten.</p> <p>Bislang konnten Admins nur von ihnen selbst erstellte Speicherorte und Konten anzeigen und verwalten.</p> |  | 17. April 2024 |
| **Anhebung der standardmäßigen Schwellenwerte für geringeren Traffic** | **Mitte April 2024** beginnt Adobe mit der Erhöhung der standardmäßigen Report Suite-Schwellenwerte für geringen Traffic wie folgt: ![Schwellenwerte für geringen Traffic](assets/thresholds.png) Dies wirkt sich nur auf Variablen aus, die derzeit unter den neuen Schwellenwerten liegen. Diese Änderungen werden schrittweise vorgenommen und wir gehen davon aus, dass sie bis **Ende Mai** abgeschlossen sind. Wenn diese Erhöhungen eingeführt werden, werden Sie möglicherweise Änderungen bei Variablen mit hoher Kardinalität bemerken:<ul><li>Es können mehr Dimensionswerte für das Reporting verfügbar sein.</li><li>Segmente und berechnete Metriken können weitere Daten enthalten.</li><li>Virtual Report Suites, die auf Segmenten basieren, können mehr Daten enthalten.</li><li>Klassifizierungs-Exporte können mehr Daten enthalten.</li></ul> | Mitte April 2024 | 31. Mai 2024 |
| **Activity Map verwendet weniger Server-Aufrufe für Web SDK** | Derzeit werden Activity Map-Link-Ereignisse als eigene Ereignisse gezählt und verursachen zusätzliche Kosten. <p>Durch diese Verbesserung werden einige Link-Ereignisse aufgenommen und in den nächsten Treffer gepackt, ähnlich wie bei der Verarbeitung durch AppMeasurement.</p> |  | 31. Mai 2024 |

{style="table-layout:auto"}

## Fehlerbehebungen in Adobe Analytics

* Es wurden die folgenden Klassifizierungsprobleme behoben: AN-343439, AN-343503, AN-343504, AN-343986, AN-344262, AN-344564, AN-345204, AN-345234.
* Es wurden die folgenden Classifications Rule Builder-Probleme behoben: AN-341488, AN-342501, AN-345751.
* Es wurde das folgende Problem mit intelligenten Warnhinweisen behoben: AN-343466.
* Es wurden die folgenden Probleme mit der Segmentierung behoben: AN-342313
* Es wurde das folgende Data Warehouse-Problem behoben: AN-339323.
* Es wurden die folgenden Probleme mit Daten-Feeds behoben: AN-339545, AN-340092, AN-342124, AN-342862, AN-343737, AN-344035, AN-344329, AN-344703, AN-344721, AN-344940, AN-345180, AN-345196, AN-345225, AN-345236, AN-345326, AN-345631, AN-345659.
* Es wurde das folgende Problem mit Datenquellen behoben: AN-343541.
* Es wurden die folgenden Analysis Workspace-Probleme behoben: AN-336303, AN-336472, AN-338422, AN-338556, AN-339718, AN-340147, AN-340301, AN-340421, AN-340951, AN-341172, AN-342905, AN-342909, AN-343448, AN-343570, AN-344050, AN-344182, AN-344763, AN-344768,
* Es wurden die folgenden Analytics-Admin-Probleme behoben: AN-342519, AN-342523, AN-343623, AN-343882, AN-344237, AN-344829, AN-345235.
* Es wurden die folgenden A4T-Probleme behoben: AN-341619, AN-344402.
* Es wurde das folgende Mobile-App-Problem behoben: AN-342010.

### Weitere behobene Fehler in Analytics

AN-336099, AN-337474, AN-337993, AN-339718, AN-339901, AN-340014, AN-341356, AN-343021, AN-343102, AN-343353, AN-343416, AN-340014, AN-344037, AN-344525, AN-345737

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Datum hinzugefügt oder aktualisiert | Beschreibung |
| ----------- | ---------- | ---------- |
| **13-monatige Gültigkeit für gespeicherte`cust_visids`** | 20. März 2024 | Eine bevorstehende Version der Analytics-Trefferverarbeitungs-Engine, deren Freigabe für April oder Mai geplant ist, wird damit beginnen, eine 13-monatige Gültigkeit für gespeicherte `cust_visids` durchzusetzen. Wenn „Besucherzuordnung aktivieren“ in der Report Suite aktiviert ist, wird diese Einstellung zum Suchen der `cust_visid` für einen `visid_high/visid_low value` ohne `cust_visid` für den Treffer verwendet. Derzeit gibt es keine Gültigkeit der Zuordnung eines `cust_visid` für einen `visid_high/visid_low`. Mit dieser Version endet die Gültigkeit der Zuordnung, wenn 13 Monate oder mehr vergangen sind, seit `visid_high/visid_low` einen `cust_visid` für einen Treffer hatte. |
| **Adobe-API-Objektmitgliederergänzungen** | 17. Januar 2024 | Adobe kann jederzeit ohne Ankündigung oder Versionsänderung optionale Anfrage- und Antwortmitglieder (Name/Wert-Paare) zu bestehenden API-Objekten hinzufügen. Adobe empfiehlt, in der API-Dokumentation jedes Drittanbieter-Tools, das Sie in unsere API integrieren, nachzuschlagen, damit solche Ergänzungen bei der Verarbeitung ignoriert werden, wenn sie nicht verstanden werden. Bei ordnungsgemäßer Implementierung stellen diese Ergänzungen keine einschneidenden Änderungen für Ihre Implementierung dar. Adobe entfernt keine Parameter und fügt keine erforderlichen Parameter hinzu, ohne zuvor durch Versionshinweise eine Standardbenachrichtigung bereitzustellen. |

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
