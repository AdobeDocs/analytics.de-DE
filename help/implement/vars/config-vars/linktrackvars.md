---
title: linkTrackVars
description: Geben Sie an, welche Variablen in Bildanforderungen zum Linktracking einbezogen werden sollen.
feature: Appmeasurement Implementation
exl-id: b884f6e9-45d9-49f0-ac74-ea6f4f01020a
role: Admin, Developer
TQID: https://experienceleague.adobe.com/B3So-VtGCz2klaFJT2a1zA3-AzSPaM9R-0jafXNsrVE
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: c069c44e-5426-4c1a-accc-8028662f2fde
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 344
ht-degree: 60%

---

# linkTrackVars

Einige Implementierungen möchten nicht alle Variablen in alle Bildanforderungen zum Linktracking einbeziehen. Verwenden Sie die Variablen `linkTrackVars` und [`linkTrackEvents`](linktrackevents.md), um Dimensionen und Metriken selektiv in [`tl()`](../functions/tl-method.md)-Aufrufe einzubeziehen.

Diese Variable wird nicht für Seitenansichtsaufrufe ([`t()`](../functions/t-method.md)-Methode) verwendet.

## Bestimmen Sie mithilfe der Web-SDK, welche Variablen in ein XDM-Ereignis eingeschlossen werden sollen

Web SDK schließt bestimmte Felder für Linktracking-Aufrufe nicht aus. Sie können jedoch den `onBeforeEventSend`-Callback verwenden, um die gewünschten Felder zu löschen oder festzulegen, bevor Daten an Adobe gesendet werden. Weitere Informationen [&#x200B; Sie in der &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) zu Web SDK unter „Globales Ändern von Ereignissen“.

## Variablen in Linktracking-Aufrufen mit der Adobe Analytics-Erweiterung

Diese Variable wird automatisch im Backend auf der Grundlage der in der -Schnittstelle festgelegten Variablen gefüllt, sodass sie in Implementierungen, die die Adobe Analytics-Erweiterung verwenden, immer festgelegt wird.

>[!IMPORTANT]
>
>Wenn Sie Variablen mit dem Editor für benutzerspezifischen Code festlegen, müssen Sie die Variablen auch in `linkTrackVars` unter Verwendung von benutzerdefiniertem Code einbeziehen.

## s.linkTrackVars in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

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
