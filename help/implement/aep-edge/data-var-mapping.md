---
title: Datenobjekt-Feldzuordnung zu Adobe Analytics
description: Erfahren Sie, welche Datenobjektfelder in Experience Platform Edge automatisch Analytics-Variablen zugeordnet werden.
feature: Implementation Basics
role: Admin, Developer
exl-id: 45b2fbbc-73ca-40b3-9484-b406ae99fdad
source-git-commit: b3546e67cccc37cbdb89db2e80b3b34b2dbe417b
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 77%

---

# Datenobjekt-Feldzuordnung zu Adobe Analytics

Die folgende Tabelle zeigt das Datenobjektfeld, das Adobe Experience Platform Edge Network automatisch Adobe Analytics zuordnet. Wenn Sie diese Datenobjektfeldpfade verwenden, ist keine zusätzliche Konfiguration erforderlich, um Daten an Adobe Analytics zu senden.

Die Verwendung dieser Felder wird empfohlen, wenn Sie in Zukunft Customer Journey Analytics verwenden möchten. Diese Implementierungsmethode ermöglicht es Ihrer Organisation, Daten mithilfe von Web SDK an Adobe zu senden, ohne einem XDM-Schema zu entsprechen. Wenn Ihre Organisation bereit ist, Daten an Adobe Experience Platform zu senden, können Sie [Datenstromzuordnung](https://experienceleague.adobe.com/de/docs/experience-platform/datastreams/data-prep#mapping) verwenden, um Datenobjektfelder den entsprechenden XDM-Feldern zuzuordnen.

## Wertprioritäten

Die meisten Datenobjektfelder in dieser Tabelle entsprechen einem [zugeordneten XDM-Feld](xdm-var-mapping.md). Während der Adobe Analytics-Aufnahme werden Werte zunächst von XDM Analytics-Variablen zugeordnet. Erkannte Datenobjektfelder werden dann zugeordnet und überschreiben alle zuvor festgelegten Werte, wenn sie derselben Analytics-Variablen zugeordnet werden. Wenn beispielsweise `data.__adobe.analytics.events` vorhanden ist, ersetzt sie den gesamten Satz von Ereignissen, die andernfalls von XDM abgeleitet würden. Ereignisse werden nicht über beide Quellen hinweg kombiniert. Eine leere Zeichenfolge (`""`) in einem Datenobjektfeld blendet die zugeordnete Analytics-Variable für den Treffer aus, auch wenn das entsprechende XDM-Feld einen Wert enthält.

Einige Datenobjektfelder unterstützen auch den jeweiligen [Abfrageparameterwert](../validate/query-parameters.md) als Kurzschreibweise. Sie können standardmäßige Datenobjektfelder und Datenobjektfelder in Kurzschreibweise austauschbar verwenden, solange diese jeweils für eindeutige Variablen stehen. Vermeiden Sie es, gleichzeitig ein standardmäßiges Datenobjektfeld und das entsprechende Datenobjektfeld in Kurzschreibweise festzulegen. Adobe kann nicht garantieren, welches Feld Priorität hat.

## Zuordnen von Datenobjektfeldern

Vorherige Aktualisierungen dieser Tabelle finden Sie auf der Seite [Commit-Verlauf auf GitHub](https://github.com/AdobeDocs/analytics.de-DE/commits/main/help/implement/aep-edge/data-var-mapping.md). Ähnlich wie bei AppMeasurement-Variablen wird auch bei allen Datenobjektfeldern zwischen Groß- und Kleinschreibung unterschieden.

| Datenobjektfeldpfade | Analytics-Variable und Beschreibung |
| --- | --- |
| `data.__adobe.analytics.browserHeight` | Die Dimension [Browser-Höhe](../../components/dimensions/browser-height.md). Die Kurzschreibweise `data.__adobe.analytics.bh` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.browserWidth` | Die Dimension [Browser-Breite](../../components/dimensions/browser-width.md). Die Kurzschreibweise `data.__adobe.analytics.bw` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.campaign` | Die Dimension [Trackingcode](../../components/dimensions/tracking-code.md). Die Kurzschreibweise `data.__adobe.analytics.v0` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.channel` | Die Dimension [Site-Bereich](../../components/dimensions/site-section.md). Die Kurzschreibweise `data.__adobe.analytics.ch` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.colorDepth` | Die Dimension [Farbtiefe](../../components/dimensions/color-depth.md). Die Kurzschreibweise `data.__adobe.analytics.c` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.connectionType` | Die Dimension [Verbindungstyp](../../components/dimensions/connection-type.md). Die Kurzschreibweise `data.__adobe.analytics.ct` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.contextData` | [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md). |
| `data.__adobe.analytics.cookiesEnabled` | Die Dimension [Cookie-Unterstützung](../../components/dimensions/cookie-support.md). Die Kurzschreibweise `data.__adobe.analytics.k` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.currencyCode` | Implementierungsvariable [`currencyCode`](../vars/config-vars/currencycode.md). Die Kurzschreibweise `data.__adobe.analytics.cc` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.dynamicVariablePrefix` | Implementierungsvariable [`dynamicVariablePrefix`](../vars/config-vars/dynamicvariableprefix.md). |
| `data.__adobe.analytics.eVar1` – `data.__adobe.analytics.eVar250` | [eVar](../../components/dimensions/evar.md)-Dimensionen. Die Kurzschreibweise `data.__adobe.analytics.v1` - `data.__adobe.analytics.v250` werden ebenfalls unterstützt. |
| `data.__adobe.analytics.events` | [Benutzerdefinierte Ereignisse](../../components/metrics/custom-events.md). Formatieren Sie dieses Feld ähnlich wie die Implementierungsvariable [`events`](../vars/page-vars/events/events-overview.md). |
| `data.__adobe.analytics.javaEnabled` | Die Dimension [Java aktiviert](../../components/dimensions/java-enabled.md). Die Kurzschreibweise `data.__adobe.analytics.v` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.latitude` | Ermöglicht die Definition der Mobile-Lebenszyklusdimensionen [Speicherort](../../components/dimensions/lifecycle-dimensions.md). Die Kurzschreibweise `data.__adobe.analytics.lat` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.linkName` | Die Dimension [Benutzerspezifischer Link](../../components/dimensions/custom-link.md), [Download-Link](../../components/dimensions/download-link.md) oder [Exit-Link](../../components/dimensions/exit-link.md), je nach Wert in `data.__adobe.analytics.linkType`. Die Kurzschreibweise `data.__adobe.analytics.pev2` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.linkURL` | Implementierungsvariable [`linkURL`](../vars/config-vars/linkurl.md). Die Kurzschreibweise `data.__adobe.analytics.pev1` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.linkType` | Bestimmt den Typ des angeklickten Links. Gültige Werte sind `o` (benutzerspezifische Links), `d` (Download-Links) und `e` (Exit-Links). Die Kurzschreibweise `data.__adobe.analytics.pe` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.list1` – `data.__adobe.analytics.list3` | Implementierungsvariablen [`list`](/help/implement/vars/page-vars/list.md). Die Kurzschreibweisen `data.__adobe.analytics.l1` - `data.__adobe.analytics.list3` werden ebenfalls unterstützt. |
| `data.__adobe.analytics.longitude` | Hilft beim Festlegen der Mobile-Lebenszyklusdimensionen [Standort](../../components/dimensions/lifecycle-dimensions.md). Die Kurzschreibweise `data.__adobe.analytics.lon` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.pageName` | Die Dimension [Seite](/help/components/dimensions/page.md). |
| `data.__adobe.analytics.pageURL` | Die Dimension [Seiten-URL](/help/components/dimensions/page-url.md). Die Kurzschreibweise `data.__adobe.analytics.g` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.pageType` | Implementierungsvariable [`pageType`](../vars/page-vars/pagetype.md). |
| `data.__adobe.analytics.prop1` – `data.__adobe.analytics.prop75` | Die Dimension [Prop](../../components/dimensions/prop.md). Die Kurzschreibweisen `data.__adobe.analytics.c1` - `data.__adobe.analytics.c75` werden ebenfalls unterstützt. |
| `data.__adobe.analytics.purchaseID` | Implementierungsvariable [`purchaseID`](../vars/page-vars/purchaseid.md). |
| `data.__adobe.analytics.products` | Die Implementierungsvariable [`products`](../vars/page-vars/products.md) folgt einer ähnlichen Formatierung. |
| `data.__adobe.analytics.referrer` | Die Dimension [Referrer](/help/components/dimensions/referrer.md). |
| `data.__adobe.analytics.resolution` | Die Dimension [Bildschirmauflösung](../../components/dimensions/monitor-resolution.md). Die Kurzschreibweise `data.__adobe.analytics.s` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.server` | Die Dimension [Server](/help/components/dimensions/server.md). |
| `data.__adobe.analytics.transactionID` | Implementierungsvariable [`transactionID`](../vars/page-vars/transactionid.md). Die Kurzschreibweise `data.__adobe.analytics.xact` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.zip` | Die Dimension [Postleitzahl](../../components/dimensions/zip-code.md). |

{style="table-layout:auto"}
