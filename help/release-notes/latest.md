---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 0f05faf76c26000f714e95ed2469ff13b7e3b72e
workflow-type: tm+mt
source-wordcount: '841'
ht-degree: 85%

---

# Aktuelle Adobe Analytics-Versionshinweise (August 2024)

**Letzte Aktualisierung**: Dienstag, 9. September 2024

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom 14. August 2024 bis September 2024. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Zusätzliche Informationen in der Spalte &quot;Verwendet in&quot;im Manager für berechnete Metriken und im Segment-Manager** | Die Spalte &quot;Verwendet in&quot;im Manager für berechnete Metriken und im Segment-Manager enthält die folgenden neuen Berichtsbereiche:<ul><li>**Report Builder:** Zeigt die Anzahl der berechneten Metriken oder Segmente an, die im Report Builder verwendet werden.</li><li>**Ad-hoc-Komponenten:** Zeigt die Anzahl der berechneten Ad-hoc-Metriken oder Ad-hoc-Segmente an, die in Projekten verwendet werden. Diese errechneten Ad-hoc-Metriken und Segmente (auch als &quot;schnell berechnete Metriken&quot;und &quot;Schnellsegmente&quot;bezeichnet) können nur in dem Projekt verwendet werden, in dem sie erstellt wurden. Daher werden sie getrennt vom Berichtsbereich &quot;Projekt&quot;in der Spalte &quot;Verwendet in&quot;gemeldet.</li></ul><p>(Nachfolgende Links der Dokumentation wurden aktualisiert.)</p> | -/- | Donnerstag, 11. September 2024 |
| **Web SDK-Verbesserungen für das Linktracking** | In der neuesten Version des Web SDK sind mehrere wichtige Verbesserungen bezüglich des Linktrackings verfügbar, wovon Activity Map direkt profitiert. Diese neuen Funktionen sind sowohl in der Web SDK-JavaScript-Bibliothek als auch in der Web SDK-Tag-Erweiterung verfügbar.<ul><li>Ereignisgruppierung: Wenn eine Besucherin oder ein Besucher auf einen internen Link klickt, können Sie sich dafür entscheiden, Ereignisdaten auf der nächsten Seite gruppieren, anstatt einen separaten Ereignisaufruf für das Linktracking auszulösen. Diese Verbesserung reduziert die Anzahl der Ereignisse, die das Web SDK im Rahmen Ihres vertraglichen Limits verwendet!.</li><li>Klickeigenschaften filtern: Ein neuer Rückruf, der `OnBeforeLinkClickSend` ersetzt. Sie können diesen Rückruf verwenden, um verknüpfungsbezogene Daten zu filtern oder zu verschleiern, bevor Sie sie an Adobe senden.</li></ul><p>Weitere Informationen finden Sie unter [clickCollection](https://experienceleague.adobe.com/de/docs/experience-platform/web-sdk/commands/configure/clickcollection) im Web SDK-Benutzerhandbuch.</p> | Open Beta begann am 10. Juli 2024 | 18. Juli 2024 |

{style="table-layout:auto"}

## Fehlerbehebungen in Adobe Analytics

* Es wurde ein Problem behoben, bei dem mehrere unbekannte Werte in Workspace angezeigt wurden (AN-353632).
* Es wurde ein Problem behoben, bei dem die Benachrichtigungs-E-Mail nach dem Hinzufügen neuer Kundinnen und Kunden oder neuer Analytics-Produktprofile in der Admin Console nicht gesendet wurde (AN-350930).

### Weitere behobene Fehler in Analytics

AN-354361; AN-354248; AN-354211; AN-354324; AN-351532; AN-349808; AN-347831; AN-353777; AN-354092; AN-354064; AN-354202; AN-354006; AN-354097; AN-352548; AN-353819; AN-353818; AN-353628; AN-353747; AN-353527; AN-353490; AN-352647; AN-352656; AN-351274; AN-352135; AN-351519; AN-344906; AN-353697; AN-354499; AN-354402; AN-354062; AN-353905; AN-353932; AN-354142; AN-354194; AN-354182; AN-353758; AN-353039; AN-353612; AN-350799; AN-354414; AN-354636; AN-354249; AN-353637; AN-350949; AN-349402; AN-355103; AN-354174; AN-353823; AN-354819; AN-354215; AN-354219; AN-354040; AN-354763; AN-354597; AN-354478; AN-354528; AN-354335

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Datum hinzugefügt oder aktualisiert | Beschreibung |
| ----------- | ---------- | ---------- |
| **13-monatige Gültigkeit für gespeicherte`cust_visids`** | 20. August 2024 | Die Version der Analytics-Trefferverarbeitungs-Engine vom **20. August 2024** setzt eine 13-monatige Gültigkeit für gespeicherte `cust_visids` durch. Wenn in der Report Suite „Besucherzuordnung aktivieren“ aktiviert ist, wird diese Einstellung zum Suchen der `cust_visid` für einen `visid_high/visid_low value` ohne `cust_visid` für den Treffer verwendet. Bisher war die Gültigkeit der Zuordnung eines `cust_visid` für einen `visid_high/visid_low` nicht eingeschränkt. Mit dieser Version endet die Gültigkeit der Zuordnung, wenn 13 Monate oder mehr vergangen sind, seit `visid_high/visid_low` eine `cust_visid` für einen Treffer hatte. |

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
