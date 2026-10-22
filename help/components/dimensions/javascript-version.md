---
title: JavaScript-Version
description: Die vom Browser des Besuchers unterstützte JavaScript-Version.
feature: Dimensions
source-git-commit: a68e13c9232ef8d975fd1256168a0addf677f5ac
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 10%
---
# JavaScript-Version

Die Dimension &quot;JavaScript[Version](overview.md) zeigt die JavaScript-Version an, die vom Browser des Besuchers unterstützt wird. Es zeigt keine Version der AppMeasurement-Bibliothek an.

>[!IMPORTANT]
>
>Diese Dimension ist nur in Data Warehouse verfügbar. Wenn Sie die JavaScript-Version in anderen Analytics-Lösungen verwenden möchten, kopieren Sie den Wert bei jedem [&#128279;](evar.md) in eine eVar.

## Füllen dieser Dimension mit Daten

AppMeasurement erkennt JavaScript-Funktionen im Browser automatisch und sendet im `j` Abfragezeichenfolgenparameter einen Versionswert. Es gibt keine festzulegende Implementierungsvariable. Bei dieser Erkennung werden ältere JavaScript-Versionskennzeichnungen verwendet. Es handelt sich hierbei nicht um ein umfassendes Maß für die Unterstützung moderner ECMAScript-Funktionen.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (automatisch erfasst) |
| **Feld Web SDK/XDM** | [`environment.browserDetails.javaScriptVersion`](/help/implement/aep-edge/xdm-var-mapping.md) |
| **Abfrageparameter** | [`j`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<javaScriptVersion>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Bulk Data Insertion-API-Spalte** | [`javaScriptVersion`](https://developer.adobe.com/analytics-collection-apis/methods/bulk-data-insertion/column-reference) |
| **Byte-Grenze** | 5 Byte |
| **Persistenz** | Treffer |

## Dimensionselemente

Dimension-Elemente enthalten die JavaScript-Versionswerte, die von Besucherbrowsern wie `1.5` und `1.6` erfasst wurden.
