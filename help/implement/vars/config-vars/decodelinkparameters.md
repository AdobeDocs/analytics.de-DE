---
title: decodeLinkParameters
description: Aktivieren oder deaktivieren Sie die doppelte Kodierung von Linktracking-Variablen in AppMeasurement.
exl-id: 329c521a-b965-4114-93ce-f45f159d4a20
feature: Appmeasurement Implementation
role: Admin, Developer
TQID: https://experienceleague.adobe.com/YzBsuWvpzof1f8qqJO5j8wuWvHSWdPomxowisPbkg7E
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: c069c44e-5426-4c1a-accc-8028662f2fdeid: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 310
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
