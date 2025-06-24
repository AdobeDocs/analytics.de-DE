---
title: decodeLinkParameters
description: Aktivieren oder deaktivieren Sie die doppelte Kodierung von Linktracking-Variablen in AppMeasurement.
exl-id: 329c521a-b965-4114-93ce-f45f159d4a20
feature: Appmeasurement Implementation
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 8%

---

# decodeLinkParameters

Die Variable `decodeLinkParameters` ist ein boolescher Wert, der bestimmt, ob Linktracking-Variablen einmal (bei Festlegung auf `true`) oder zweimal (bei Festlegung auf `false`) kodiert werden. Sie wirkt sich nur auf `linkName` (Teil der [`tl()`](../functions/tl-method.md)) und [`linkURL`](linkurl.md) aus. Hierfür ist AppMeasurement v2.24.0 oder höher erforderlich. Der Standardwert dieser Variablen ist `false`.

In Versionen von AppMeasurement vor Version 2.24.0 wurden Linktracking-Variablen immer zweimal URL-kodiert. Bei Implementierungen, die in der Regel auf Einzelbyte-Zeichen angewiesen sind, stellt die Doppelcodierung zwar kein Problem dar, es werden jedoch falsch codierte Werte für Multibyte-Zeichen in Berichten erstellt. Wenn Sie diese Variable auf setzen, werden Linktracking-Werte `true` einmal kodiert, was normalerweise das gewünschte Verhalten ist.

* Wenn Ihre Implementierung Multi-Byte-Zeichen verwendet und Linktracking-Variablen URL-decodiert sind, um die doppelte Codierung von AppMeasurement zu versetzen, setzen Sie diese Variable auf `false`. Dieser Wert behält bestehende AppMeasurement-Funktionen bei.
* Wenn Ihre Implementierung Multi-Byte-Zeichen verwendet und Sie keine URL-Decodierung von Linktracking-Werten vornehmen, empfiehlt Adobe, diese Variable auf `true` festzulegen.
* Wenn Ihre Implementierung keine Multi-Byte-Zeichen verwendet, ist diese Variable nicht erforderlich. Adobe empfiehlt jedoch, diese Variable in Fällen, in denen Multibyte-Zeichen gesendet werden können, auf `true` festzulegen.

## Doppelte Kodierung von Link-Parametern mithilfe der Web-SDK

Diese Variable ist spezifisch für AppMeasurement und wird in keiner Implementierung von Web SDK benötigt.

## Doppelte Kodierung von Link-Parametern mithilfe der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.decodeLinkParameters in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die Variable `s.decodeLinkParameters` ist ein boolescher Wert, der bestimmt, ob Linktracking-Werte doppelt kodiert werden. Wenn diese Variable nicht definiert ist, wird ihr Standardwert `false`, um die Funktionalität für vorhandene Implementierungen beizubehalten. Adobe empfiehlt, diesen Wert für alle neuen Implementierungen auf `true` zu setzen, insbesondere wenn in Linktracking-Berichten URL-codierte Werte angezeigt werden.

```js
s.decodeLinkParameters = true;
```
