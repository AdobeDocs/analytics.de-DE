---
title: Zuordnung von Datenobjektvariablen zu Adobe Analytics
description: Zeigen Sie an, welche Datenobjektfelder Experience Platform Edge automatisch Analytics-Variablen zugeordnet.
feature: Implementation Basics
role: Admin, Developer
exl-id: 45b2fbbc-73ca-40b3-9484-b406ae99fdad
source-git-commit: 59d9dd8055a13046d05ac4c3b5261a6c5a919b5c
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 2%

---

# Zuordnung von Datenobjektvariablen zu Adobe Analytics

Die folgende Tabelle zeigt die Datenobjektvariablen, die das Adobe Experience Platform-Edge Network automatisch Adobe Analytics zuordnet. Wenn Sie diese Datenobjektfeldpfade verwenden, ist keine zusätzliche Konfiguration erforderlich, um Daten an Adobe Analytics zu senden.

Die Verwendung dieser Felder wird empfohlen, wenn Sie in Zukunft Customer Journey Analytics verwenden möchten. Mit dieser Implementierungsmethode kann Ihr Unternehmen Daten mit dem Web SDK an Adobe senden, ohne ein XDM-Schema zu erfüllen. Wenn Ihr Unternehmen bereit ist, Daten an Adobe Experience Platform zu senden, können Sie die [Datenasterzuordnung](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/data-prep#mapping) verwenden, um Datenobjektfelder auf ihre jeweiligen XDM-Felder zu verweisen.

## Wertprioritäten

Die meisten Datenobjektfelder in dieser Tabelle entsprechen einem [zugeordneten XDM-Feld](xdm-var-mapping.md). Wenn Sie sowohl ein bestimmtes Datenobjektfeld als auch das entsprechende XDM-Feld festlegen, hat das Datenobjektfeld Priorität. Wenn beispielsweise das Feld `data.__adobe.analytics.events` vorhanden ist, werden alle ereignisbezogenen XDM-Objektfelder überschrieben.

Einige Datenobjektfelder unterstützen auch ihren jeweiligen [Abfrageparameterwert](../validate/query-parameters.md) als Kurzwerte. Sie können standardmäßige Datenobjektfelder und kurze Datenobjektfelder synonym verwenden, sofern sie jeweils für eindeutige Variablen gelten. Vermeiden Sie es, gleichzeitig ein standardmäßiges Datenobjektfeld und das entsprechende Kurzdatenobjektfeld festzulegen. Adobe kann nicht garantieren, welches Feld Priorität hat.

## Datenobjektfeldzuordnung

Vorherige Aktualisierungen dieser Tabelle finden Sie im [Commitverlauf dieser Seite auf GitHub](https://github.com/AdobeDocs/analytics.en/commits/main/help/implement/aep-edge/data-var-mapping.md). Ähnlich wie bei AppMeasurement-Variablen wird bei allen Datenobjektfeldern zwischen Groß- und Kleinschreibung unterschieden.

| Datenobjektfeldpfad | Analytics-Variable und -Beschreibung |
| --- | --- |
| `data.__adobe.analytics.browserHeight` | Die Dimension [Browserhöhe](../../components/dimensions/browser-height.md) . Das Kurzfeld `data.__adobe.analytics.bh` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.browserWidth` | Die Dimension [Browserbreite](../../components/dimensions/browser-width.md) . Das Kurzfeld `data.__adobe.analytics.bw` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.campaign` | Die Dimension [Trackingcode](../../components/dimensions/tracking-code.md) . Das Kurzfeld `data.__adobe.analytics.v0` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.channel` | Die Dimension [Site-Abschnitt](../../components/dimensions/site-section.md) . Das Kurzfeld `data.__adobe.analytics.ch` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.colorDepth` | Die Dimension [Farbtiefe](../../components/dimensions/color-depth.md) . Das Kurzfeld `data.__adobe.analytics.c` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.connectionType` | Die Dimension [Verbindungstyp](../../components/dimensions/connection-type.md) . Das Kurzfeld `data.__adobe.analytics.ct` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.contextData` | [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md). |
| `data.__adobe.analytics.cookiesEnabled` | Die Dimension [Cookie-Unterstützung](../../components/dimensions/cookie-support.md) . Das Kurzfeld `data.__adobe.analytics.k` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.currencyCode` | Die Implementierungsvariable [`currencyCode`](../vars/config-vars/currencycode.md). Das Kurzfeld `data.__adobe.analytics.cc` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.dynamicVariablePrefix` | Die Implementierungsvariable [`dynamicVariablePrefix`](../vars/config-vars/dynamicvariableprefix.md). |
| `data.__adobe.analytics.eVar1` - `data.__adobe.analytics.eVar250` | [eVar](../../components/dimensions/evar.md) -Dimensionen. Die Kurzfelder `data.__adobe.analytics.v1` - `data.__adobe.analytics.v250` werden ebenfalls unterstützt. |
| `data.__adobe.analytics.events` | [Benutzerspezifische Ereignisse](../../components/metrics/custom-events.md). Formatieren Sie dieses Feld ähnlich wie die Implementierungsvariable [`events`](../vars/page-vars/events/events-overview.md). |
| `data.__adobe.analytics.javaEnabled` | Die Dimension [Java aktiviert](../../components/dimensions/java-enabled.md) . Das Kurzfeld `data.__adobe.analytics.v` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.latitude` | Hilft bei der Festlegung der Mobile-Lebenszyklusdimensionen für [Position](../../components/dimensions/lifecycle-dimensions.md). Das Kurzfeld `data.__adobe.analytics.lat` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.linkName` | Die Dimension [Benutzerspezifischer Link](../../components/dimensions/custom-link.md), [Downloadlink](../../components/dimensions/download-link.md) oder [Exitlink](../../components/dimensions/exit-link.md) , je nach Wert in `data.__adobe.analytics.linkType`. Das Kurzfeld `data.__adobe.analytics.pev2` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.linkURL` | Die Implementierungsvariable [`linkURL`](../vars/config-vars/linkurl.md). Das Kurzfeld `data.__adobe.analytics.pev1` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.linkType` | Bestimmt den Typ des angeklickten Links. Gültige Werte sind `o` (benutzerspezifische Links), `d` (Downloadlinks) und `e` (Exitlinks). Das Kurzfeld `data.__adobe.analytics.pe` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.list1` - `data.__adobe.analytics.list3` | [`list`](/help/implement/vars/page-vars/list.md) Implementierungsvariablen. Die Kurzfelder `data.__adobe.analytics.l1` - `data.__adobe.analytics.list3` werden ebenfalls unterstützt. |
| `data.__adobe.analytics.longitude` | Helfen Sie bei der Festlegung der Dimensionen für den mobilen Lebenszyklus von [Standort](../../components/dimensions/lifecycle-dimensions.md) . Das Kurzfeld `data.__adobe.analytics.lon` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.pageName` | Die Dimension [Seite](/help/components/dimensions/page.md). |
| `data.__adobe.analytics.pageURL` | Die Dimension [Seiten-URL](/help/components/dimensions/page-url.md) . Das Kurzfeld `data.__adobe.analytics.g` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.pageType` | Die Implementierungsvariable [`pageType`](../vars/page-vars/pagetype.md). |
| `data.__adobe.analytics.prop1` - `data.__adobe.analytics.prop75` | [Prop](../../components/dimensions/prop.md) -Dimensionen. Die Kurzfelder `data.__adobe.analytics.c1` - `data.__adobe.analytics.c75` werden ebenfalls unterstützt. |
| `data.__adobe.analytics.purchaseID` | Die Implementierungsvariable [`purchaseID`](../vars/page-vars/purchaseid.md). |
| `data.__adobe.analytics.products` | Die Implementierungsvariable [`products`](../vars/page-vars/products.md) , die ähnlich formatiert ist. |
| `data.__adobe.analytics.referrer` | Die Dimension [Referrer](/help/components/dimensions/referrer.md). |
| `data.__adobe.analytics.resolution` | Die Dimension [Bildschirmauflösung](../../components/dimensions/monitor-resolution.md) . Das Kurzfeld `data.__adobe.analytics.s` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.server` | Die Dimension [Server](/help/components/dimensions/server.md). |
| `data.__adobe.analytics.transactionID` | Die Implementierungsvariable [`transactionID`](../vars/page-vars/transactionid.md). Das Kurzfeld `data.__adobe.analytics.xact` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.zip` | Die Dimension [Postleitzahl](../../components/dimensions/zip-code.md) . |

{style="table-layout:auto"}
