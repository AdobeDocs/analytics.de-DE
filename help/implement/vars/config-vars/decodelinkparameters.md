---
title: decodeLinkParameters
description: Aktivieren oder deaktivieren Sie die AppMeasurement-Doppelkodierung von Linktracking-Variablen.
exl-id: 329c521a-b965-4114-93ce-f45f159d4a20
feature: Variables
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 8%

---

# decodeLinkParameters

Die Variable `decodeLinkParameters` ist ein boolescher Wert, der bestimmt, ob Linktracking-Variablen einmal kodiert werden (bei `true`) oder zweimal (bei `false`). Dies wirkt sich nur auf `linkName` (Teil der [`tl()`](../functions/tl-method.md) -Methode) und [`linkURL`](linkurl.md) aus. Es ist AppMeasurement v2.24.0 oder höher erforderlich. Der Standardwert dieser Variablen ist `false`.

In Versionen von AppMeasurement vor Version 2.24.0 waren Linktracking-Variablen immer zweimal URL-kodiert. Bei Implementierungen, die normalerweise auf Einzelbyte-Zeichen angewiesen sind, stellt die Doppelkodierung zwar kein Problem dar, sie hat aber falsch kodierte Werte für Multibytezeichen in Berichten erstellt. Wenn Sie diese Variable auf `true` setzen, werden die Linktracking-Werte einmal kodiert, was normalerweise das gewünschte Verhalten ist.

* Wenn Ihre Implementierung Multi-Byte-Zeichen verwendet und Linktracking-Variablen URL-dekodiert sind, um die doppelte Codierung von AppMeasurement zu versetzen, setzen Sie diese Variable auf `false`. Dieser Wert behält bestehende AppMeasurement-Funktionen bei.
* Wenn Ihre Implementierung Multibyte-Zeichen verwendet und Sie keine URL-Dekodierung von Linktracking-Werten vornehmen, empfiehlt Adobe, diese Variable auf `true` festzulegen.
* Wenn Ihre Implementierung keine Multibytezeichen verwendet, ist diese Variable nicht erforderlich. Adobe empfiehlt jedoch, diese Variable auf `true` festzulegen, wenn Multibytezeichen gesendet werden.

## Doppelkodieren von Link-Parametern mit dem Web SDK

Diese Variable ist spezifisch für AppMeasurement und wird in keiner Web SDK-Implementierung benötigt.

## Doppelkodieren von Link-Parametern mit der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.decodeLinkParameters in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die Variable `s.decodeLinkParameters` ist ein boolescher Wert, der bestimmt, ob Linktracking-Werte doppelt kodiert werden. Wenn diese Variable nicht definiert ist, ist ihr Standardwert `false`, um die Funktionalität für vorhandene Implementierungen beizubehalten. Adobe empfiehlt, diesen Wert für alle neuen Implementierungen auf `true` festzulegen, insbesondere wenn in Linktracking-Berichten URL-kodierte Werte angezeigt werden.

```js
s.decodeLinkParameters = true;
```
