---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 7dd42948073b56a33c1d00f9b4292d1cc3416470
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 66%

---

# Aktuelle Adobe Analytics-Versionshinweise (September 2024)


**Letzte Aktualisierung**: Donnerstag, 11. September 2024

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom 11. September 2024 bis Anfang Oktober. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
|--- | --- | --- | --- |
| **Zusätzliche Informationen in der Spalte „Verwendet in“ im Manager für berechnete Metriken und im Segment-Manager** | Die Spalte „Verwendet in“ im Manager für berechnete Metriken und im Segment-Manager enthält die folgenden neuen Reporting-Bereiche:<ul><li>**Report Builder**: Zeigt die Anzahl der berechneten Metriken oder Segmente an, die im Report Builder verwendet werden.</li><li>**Ad-hoc-Komponenten**: Zeigt die Anzahl der berechneten Ad-hoc-Metriken oder Ad-hoc-Segmente an, die in Projekten verwendet werden. Diese berechneten Ad-hoc-Metriken und -Segmente (auch als „schnell berechnete Metriken“ und „Schnellsegmente“ bezeichnet) können nur in dem Projekt verwendet werden, in dem sie erstellt wurden. Daher werden sie getrennt vom Reporting-Bereich „Projekt“ in der Spalte „Verwendet in“ aufgeführt.</li></ul>Weitere Informationen finden Sie unter [Manager für berechnete Metriken](https://experienceleague.adobe.com/en/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-manager) und [Segment-Manager](https://experienceleague.adobe.com/en/docs/analytics/components/segmentation/segmentation-workflow/seg-manage). |  | 11. September 2024 |
| **Activity Map v3-Erweiterung** | Die Activity Map v3-Erweiterung ist jetzt verfügbar. Wenn Sie die v2-Erweiterung installiert haben, deinstallieren Sie sie, bevor Sie die v3-Erweiterung installieren. Navigieren Sie zu **[!UICONTROL Tools]** > **[!UICONTROL Activity Map]** , um die neueste Version der Erweiterung zu erhalten. |  | 3. September 2024 |


## Fehlerbehebungen in Adobe Analytics

A4T: AN-355736
Activity Map: AN-353779
Analysis Workspace: AN-348485; AN-349693; AN-357247
Analytics Mobile App: AN-352645
Klassifizierungen: AN-355636; AN-355651; AN-355753; AN-356005; AN-356439; AN-356540; AN-35657; AN-356622
Geräteübergreifende Analyse: AN-355138
Datenfeeds: AN-356258; AN-357133
Data Warehouse: AN-339292; AN-353807
Exportstandorte: AN-356912
Datenschutz-API: AN-352420
Report Builder: AN-352555; AN-354316
Geplante Projekte: AN-355971
Segmentierung: AN-352095;
Zielberichte: AN-355748

Weitere Fehlerbehebungen: AN-349698; AN-349880; AN-354860; AN-355355; AN-356289;

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Datum hinzugefügt oder aktualisiert | Beschreibung |
| ----------- | ---------- | ---------- |
| **13-monatige Gültigkeit für gespeicherte`cust_visids`** | 20. August 2024 | Die Version der Analytics-Trefferverarbeitungs-Engine vom **20. August 2024** setzt eine 13-monatige Gültigkeit für gespeicherte `cust_visids` durch. Wenn in der Report Suite „Besucherzuordnung aktivieren“ aktiviert ist, wird diese Einstellung zum Suchen der `cust_visid` für einen `visid_high/visid_low value` ohne `cust_visid` für den Treffer verwendet. Bisher war die Gültigkeit der Zuordnung eines `cust_visid` für einen `visid_high/visid_low` nicht eingeschränkt. Mit dieser Version endet die Gültigkeit der Zuordnung, wenn 13 Monate oder mehr vergangen sind, seit `visid_high/visid_low` eine `cust_visid` für einen Treffer hatte. |
| **Zusätzliche Implementierungsdetails XDM-Felder, die automatisch zugeordnet werden** | 11. September 2024 | Wenn Sie das Adobe Experience Platform-Edge Network zum Senden von Daten an Adobe Analytics verwenden, werden die XDM-Felder `xdm.implementationdetails.name` und `xdm.implementationdetails.environment` jetzt immer den Kontextdatenvariablen `c.a.x.implementationdetails.name` und `c.a.x.implementationdetails.environment` zugeordnet. In früheren Szenarien wurde verhindert, dass diese Werte ausgefüllt werden. Passen Sie die relevanten Verarbeitungsregeln an, um die Verfügbarkeit dieser Werte zu berücksichtigen. |

{style="table-layout:auto"}

## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Ende der Nutzungsdauer für Adobe Analytics-API (Version 1.4)** | 17. Juli 2024 | Ab **12. August 2026** werden die folgenden veralteten Analytics-API-Dienste nicht mehr unterstützt und beendet. Aktuelle Integrationen, die mit diesen Diensten erstellt wurden, funktionieren nicht mehr:<ul><li>Adobe Analytics-API (Version 1.4)</li><li>WSSE-Authentifizierung von Adobe Analytics </li></ul><p>Integrationen, die die Adobe Analytics-API (Version 1.4) verwenden, müssen zur [Adobe Analytics 2.0-API](https://developer.adobe.com/analytics-apis/docs/2.0/) migrieren, während WSSE-Integrationen zu einem OAuth-basierten Authentifizierungsprotokoll in der [Adobe Developer Console](https://developer.adobe.com/console) migrieren müssen.</p><p>Antworten auf häufig gestellte Fragen und weitere Anleitungen finden Sie in den [häufig gestellten Fragen zum Ende der Nutzungsdauer der Adobe Analytics 1.4-API](/help/admin/c-admin-api/c-admin-14-api-eol.md).</p> |
| **Migration auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O** | 11. Mai 2023 | Kundinnen und Kunden von Adobe Analytics-API und Livestream, die JWT-Anmeldeinformationen für Adobe I/O verwenden, müssen bis zum **1. Januar 2025** auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O migrieren. Adobe I/O lässt die Erstellung neuer JWT-Anmeldeinformationen ab dem 1. Mai 2024 nicht mehr zu. Kunden und Kundinnen, die JWT verwenden, müssen neue OAuth Server-zu-Server-Anmeldeinformationen erstellen oder ihre bestehende JWT-Anmeldeinformationen zu OAuth Server-zu-Server-Anmeldeinformationen migrieren. Kunden und Kundinnen müssen außerdem ihre Client-Anwendungen aktualisieren, um die neuen OAuth Server-to-Server-Anmeldeinformationen zu verwenden. <ul><li>[Migration von Dienstkonto-Anmeldeinformationen (JWT)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementierungshandbuch für neue und alte Programme mit OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[Verwenden der neuen OAuth Server-zu-Server-Anmeldeinformationen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Häufig gestellte Fragen (FAQ)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}

## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.26.0) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2024](/help/release-notes/2024.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zum Add-on für Streaming-Mediensammlungen](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
