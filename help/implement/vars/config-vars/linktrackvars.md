---
title: linkTrackVars
description: Geben Sie an, welche Variablen in Bildanforderungen zum Linktracking einbezogen werden sollen.
feature: Variables
exl-id: b884f6e9-45d9-49f0-ac74-ea6f4f01020a
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 62%

---

# linkTrackVars

Einige Implementierungen möchten nicht alle Variablen in alle Bildanforderungen zum Linktracking einbeziehen. Verwenden Sie die Variablen `linkTrackVars` und [`linkTrackEvents`](linktrackevents.md), um Dimensionen und Metriken selektiv in [`tl()`](../functions/tl-method.md)-Aufrufe einzubeziehen.

Diese Variable wird nicht für Seitenansichtsaufrufe ([`t()`](../functions/t-method.md)-Methode) verwendet.

## Bestimmen Sie mithilfe der Web-SDK, welche Variablen in ein XDM-Ereignis eingeschlossen werden sollen

Web SDK schließt bestimmte Felder für Linktracking-Aufrufe nicht aus. Sie können jedoch den `onBeforeEventSend`-Callback verwenden, um die gewünschten Felder zu löschen oder festzulegen, bevor Daten an den Adobe gesendet werden. Weitere Informationen [ Sie in der ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html?lang=de#modifying-events-globally) zu Web SDK unter „Globales Ändern von Ereignissen“.

## Variablen in Linktracking-Aufrufen mit der Adobe Analytics-Erweiterung

Diese Variable wird automatisch im Backend auf der Grundlage der in der -Schnittstelle festgelegten Variablen gefüllt, sodass sie in Implementierungen, die die Adobe Analytics-Erweiterung verwenden, immer festgelegt wird.

>[!IMPORTANT]
>
>Wenn Sie Variablen mit dem Editor für benutzerspezifischen Code festlegen, müssen Sie die Variablen auch in `linkTrackVars` unter Verwendung von benutzerdefiniertem Code einbeziehen.

## s.linkTrackVars auf AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.linkTrackVars`-Variable ist eine Zeichenfolge, die eine kommagetrennte Liste von Variablen enthält, die Sie in Bildanforderungen zum Linktracking einbeziehen möchten (`tl()`-Methode). Die folgenden beiden Kriterien müssen erfüllt sein, um Dimensionen in Linktracking-Treffer einzubeziehen:

* Legen Sie den gewünschten Variablenwert fest. Beispiel: `s.eVar1 = "Example value";`.
* Legen Sie die gewünschte Variable in der `linkTrackVars`-Variablen fest. Beispiel: `s.linkTrackVars = "eVar1";`.

```js
s.linkTrackVars = "eVar1,eVar2,events,channel,products";
```

Der Standardwert für diese Variable ist eine leere Zeichenfolge. Adobe hat jedoch AppMeasurement-Code im Code-Manager bereitgestellt, wobei diese Variable auf `"None"` gesetzt ist. Gültige Werte sind alle Variablen auf Seitenebene, die eine Dimension ausfüllen.

* Wenn diese Variable nicht definiert oder auf eine leere Zeichenfolge festgelegt ist, werden *alle* Variablen in Bildanforderungen zum Linktracking einbezogen.
* Wenn diese Variable auf `"None"` festgelegt ist, werden in Bildanforderungen zum Linktracking *keine* Variablen einbezogen.

>[!TIP]
>
>Vermeiden Sie die Verwendung der Analytics-Objektkennung (`s.`) bei der Angabe von Variablen in dieser Variablen. Zum Beispiel ist `s.linkTrackVars = "eVar1";` korrekt, während `s.linkTrackVars = "s.eVar1";` nicht korrekt ist.

## Beispiel

Die folgende Linktracking-Funktion enthält nur `eVar1` (nicht `eVar2`) in der Bildanforderung, die an Adobe gesendet wird:

```js
s.eVar1 = "Example value 1";
s.eVar2 = "Example value 2";
s.linkTrackVars = "eVar1";
s.tl(this,"o","Example Custom Link");
```
