---
title: linkTrackEvents
description: Bestimmen Sie, welche Ereignisse in Bildanforderungen zum Linktracking einbezogen werden sollen.
feature: Appmeasurement Implementation
exl-id: 53c9e122-425c-4ec3-8a32-96e4d112f348
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 68%

---

# linkTrackEvents

Einige Implementierungen möchten nicht alle Variablen in alle Bildanforderungen zum Linktracking einbeziehen. Verwenden Sie die Variablen [`linkTrackVars`](linktrackvars.md) und `linkTrackEvents`, um Dimensionen und Metriken selektiv in [`tl()`](../functions/tl-method.md)-Aufrufe einzubeziehen.

Diese Variable wird nicht für Seitenansichtsaufrufe ([`t()`](../functions/t-method.md)-Methode) verwendet.

## Bestimmen Sie mithilfe der Web-SDK, welche Analytics-Ereignisse in ein XDM-Ereignis eingeschlossen werden sollen

Web SDK schließt bestimmte Felder für Linktracking-Aufrufe nicht aus. Sie können jedoch den `onBeforeEventSend`-Callback verwenden, um die gewünschten Felder zu löschen oder festzulegen, bevor Daten an Adobe gesendet werden. Weitere Informationen [ Sie in der ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html?lang=de#modifying-events-globally) zu Web SDK unter „Globales Ändern von Ereignissen“.

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
