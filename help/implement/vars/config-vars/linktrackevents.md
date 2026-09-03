---
title: linkTrackEvents
description: Bestimmen Sie, welche Ereignisse in Bildanforderungen zum Linktracking einbezogen werden sollen.
feature: Appmeasurement Implementation
exl-id: 53c9e122-425c-4ec3-8a32-96e4d112f348
role: Admin, Developer
TQID: https://experienceleague.adobe.com/7BKaDxchTRu39doWzm8f32DOemgpvj1s-4uzfjJkOEA
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: c069c44e-5426-4c1a-accc-8028662f2fdeid: df312454-73c4-43f6-a90e-18f5043f074cid: e7d92df1-c5ba-4e93-85df-f83171b889beid: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 325
ht-degree: 66%

---

# linkTrackEvents

Einige Implementierungen möchten nicht alle Variablen in alle Bildanforderungen zum Linktracking einbeziehen. Verwenden Sie die Variablen [`linkTrackVars`](linktrackvars.md) und `linkTrackEvents`, um Dimensionen und Metriken selektiv in [`tl()`](../functions/tl-method.md)-Aufrufe einzubeziehen.

Diese Variable wird nicht für Seitenansichtsaufrufe ([`t()`](../functions/t-method.md)-Methode) verwendet.

## Bestimmen Sie mithilfe der Web-SDK, welche Analytics-Ereignisse in ein XDM-Ereignis eingeschlossen werden sollen

Web SDK schließt bestimmte Felder für Linktracking-Aufrufe nicht aus. Sie können jedoch den `onBeforeEventSend`-Callback verwenden, um die gewünschten Felder zu löschen oder festzulegen, bevor Daten an Adobe gesendet werden. Weitere Informationen [ Sie in der ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) zu Web SDK unter „Globales Ändern von Ereignissen“.

## Ereignisse in Linktracking-Aufrufen mit der Adobe Analytics-Erweiterung

Adobe Experience Platform schließt definierte Ereignisse automatisch in Linktracking-Treffern ein, wenn Sie keinen benutzerspezifischen Code verwenden.

>[!IMPORTANT]
>
>Wenn Sie Ereignisse im benutzerdefinierten Code-Editor der Analytics-Erweiterung festlegen, müssen Sie das Ereignis auch in `linkTrackEvents` einbeziehen, indem Sie benutzerdefinierten Code verwenden.

## s.linkTrackEvents in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.linkTrackEvents`-Variable ist eine Zeichenfolge, die eine kommagetrennte Liste von Ereignissen enthält, die Sie in Bildanforderungen zum Linktracking einbeziehen möchten (`tl()`-Methode). Die folgenden drei Kriterien müssen erfüllt sein, um Metriken in Linktracking-Treffer einzubeziehen:

* Legen Sie das gewünschte Ereignis in der [`events`](../page-vars/events/events-overview.md)-Variablen fest. Beispiel: `s.events = "event1";`.
* Setzen Sie die `events`-Variable in `linkTrackVars`. Beispiel: `s.linkTrackVars = "events";`.
* Legen Sie das gewünschte Ereignis in der `linkTrackEvents`-Variablen fest. Beispiel: `s.linkTrackEvents = "event1";`.

```js
s.linkTrackEvents = "event1,event2,event3,purchase";
```

Der Standardwert für diese Variable ist eine leere Zeichenfolge. Wenn diese Variable nicht definiert ist, werden alle Ereignisse in Bildanforderungen zum Linktracking einbezogen. Beachten Sie, dass die Datenerfassung diese Variable automatisch basierend auf den in der Benutzeroberfläche festgelegten Ereignissen füllt. Daher ist sie immer für Implementierungen eingerichtet, die Tags in Adobe Experience Platform verwenden.

>[!TIP]
>
>Vermeiden Sie die Verwendung der Analytics-Objektkennung (`s.`) bei der Angabe von Ereignissen in dieser Variablen. Zum Beispiel ist `s.linkTrackEvents = "event1";` korrekt, während `s.linkTrackEvents = "s.event1";` nicht korrekt ist.

## Beispiel

Die folgende Linktracking-Funktion enthält nur `event1` (nicht `event2`) in der Bildanforderung, die an Adobe gesendet wird:

```js
s.events = "event1,event2";
s.linkTrackVars = "events";
s.linkTrackEvents = "event1";
s.tl(this,"o","Example Custom Link");
```
