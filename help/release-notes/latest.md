---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: cb0eab15dac6d679e9f912010045e6be2e47df4a
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 46%

---

# Aktuelle Adobe Analytics-Versionshinweise (Juli 2024)

**Letzte Aktualisierung**: Donnerstag, 17. Juli 2024

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom 17. Juli 2024 bis August 2024. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Web SDK-Verbesserungen für das Linktracking** | In der neuesten Version des Web SDK sind einige wichtige Verbesserungen bezüglich des Linktrackings verfügbar, wovon Activity Map direkt profitiert. Diese neuen Funktionen sind sowohl in der Web SDK JavaScript-Bibliothek als auch in der Web SDK-Tag-Erweiterung verfügbar.<ul><li>Ereignisgruppierung: Wenn ein Besucher auf einen internen Link klickt, können Sie Ereignisdaten auf der nächsten Seite gruppieren, anstatt einen separaten Ereignisaufruf für die Linktracking auszulösen. Diese Verbesserung reduziert die Anzahl der Ereignisse, die das Web SDK gegen Ihr vertragliches Limit verwendet.</li><li>Klickeigenschaften filtern: Ein neuer Rückruf, der `OnBeforeLinkClickSend` ersetzt. Sie können diesen Rückruf verwenden, um verknüpfungsbezogene Daten zu filtern oder zu verschleiern, bevor Sie sie an Adobe senden.</li></ul><p>Weitere Informationen finden Sie unter [clickCollection](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollection) im Web SDK-Benutzerhandbuch.</p> | Öffnen Sie Beta ab dem 10. Juli 2024 | TBD |

{style="table-layout:auto"}

## Fehlerbehebungen in Adobe Analytics

* Es wurde ein Problem behoben, das die Anmeldung von Benutzern bei der Analytics-Benutzeroberfläche verhinderte (AN-352953).
* Es wurde ein Problem behoben, durch das Benutzer sich nicht bei der mobilen Analytics-App anmelden konnten (AN-352463).
* Es wurde ein Problem behoben, das das Herunterladen des Projekts als PDF verhinderte (AN-352680).
* Es wurde ein Problem behoben, bei dem Classifications nicht importiert wurden (AN-352178).

### Weitere behobene Fehler in Analytics

AN-352905; AN-352902; AN-352693; AN-352659; AN-352619;
AN-352577; AN-352575; AN-352572; AN-352571; AN-352549; AN-352501; AN-35249; AN 352478; AN-352466; AN-352437; AN-352378; AN-352355; AN-352341; AN-352318; AN-3 52297; AN-352272; AN-352267; AN-352263; AN-352088; AN-352019; AN-352018; AN-35 1978; AN-351908; AN-351809; AN-351750; AN-351689; AN-351624; AN-351564; AN-351 524; AN-351507; AN-351416; AN-351414; AN-351405; AN-351299; AN-351283; AN-3512 31; AN-350710; AN-349912; AN-349786; AN-348300; AN-348061; AN-347865; AN-3476 6; AN-347478; AN-343611; AN-343114; AN-334124

## Wichtige Hinweise für Adobe Analytics-Administratoren {#admin}

| Hinweis | Datum hinzugefügt oder aktualisiert | Beschreibung |
| ----------- | ---------- | ---------- |
| **13-monatige Gültigkeit für gespeicherte`cust_visids`** | 22. Mai 2024 | Eine bevorstehende Version der Analytics-Trefferverarbeitungs-Engine, **deren Freigabe für Juli 2024 geplant ist**, wird damit beginnen, eine 13-monatige Gültigkeit für gespeicherte `cust_visids` durchzusetzen. Wenn „Besucherzuordnung aktivieren“ in der Report Suite aktiviert ist, wird diese Einstellung zum Suchen der `cust_visid` für einen `visid_high/visid_low value` ohne `cust_visid` für den Treffer verwendet. Derzeit gibt es keine Gültigkeit der Zuordnung eines `cust_visid` für einen `visid_high/visid_low`. Mit dieser Version endet die Gültigkeit der Zuordnung, wenn 13 Monate oder mehr vergangen sind, seit `visid_high/visid_low` eine `cust_visid` für einen Treffer hatte. |

{style="table-layout:auto"}

## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **EOL für Adobe Analytics-API (Version 1.4)** | Donnerstag, 17. Juli 2024 | Am **12. August 2026** erreichen die folgenden Analytics Legacy-API-Dienste ihr Lebenszyklusende und werden beendet. Aktuelle Integrationen, die mit diesen Diensten erstellt wurden, funktionieren nicht mehr:<ul><li>Adobe Analytics-API (Version 1.4)</li><li>Adobe Analytics WSSE-Authentifizierung</li></ul><p>Integrationen, die die Adobe Analytics-API (Version 1.4) verwenden, müssen zur [Adobe Analytics 2.0-API](https://developer.adobe.com/analytics-apis/docs/2.0/) migrieren, während WSSE-Integrationen in der [Adobe Developer Console](https://developer.adobe.com/console) zu einem OAuth-basierten Authentifizierungsprotokoll migrieren müssen.</p><p>Antworten auf häufig gestellte Fragen und weitere Anleitungen finden Sie in den [Häufig gestellten Fragen zur Adobe Analytics 1.4 API EOL](/help/admin/c-admin-api/c-admin-14-api-eol.md) .</p> |
| **Migration auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O** | 11. Mai 2023 | Kundinnen und Kunden von Adobe Analytics-API und Livestream, die JWT-Anmeldeinformationen für Adobe I/O verwenden, müssen bis zum **1. Januar 2025** auf OAuth Server-zu-Server-Anmeldeinformationen für Adobe I/O migrieren. Adobe I/O lässt die Erstellung neuer JWT-Anmeldeinformationen ab dem 1. Mai 2024 nicht mehr zu. Kunden und Kundinnen, die JWT verwenden, müssen neue OAuth Server-zu-Server-Anmeldeinformationen erstellen oder ihre bestehende JWT-Anmeldeinformationen zu OAuth Server-zu-Server-Anmeldeinformationen migrieren. Kunden und Kundinnen müssen außerdem ihre Client-Anwendungen aktualisieren, um die neuen OAuth Server-to-Server-Anmeldeinformationen zu verwenden. <ul><li>[Migration von Dienstkonto-Anmeldeinformationen (JWT)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementierungshandbuch für neue und alte Programme mit OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[Verwenden der neuen OAuth Server-zu-Server-Anmeldeinformationen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Häufig gestellte Fragen (FAQ)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}

## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.26.0) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2024](/help/release-notes/2024.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zum Add-on für Streaming-Mediensammlungen](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
