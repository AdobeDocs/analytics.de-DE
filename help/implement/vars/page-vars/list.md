---
title: list
description: Benutzerdefinierte Variablen, die mehrere Werte im selben Treffer enthalten.
feature: Variables
exl-id: 612f6f10-6b68-402d-abb8-beb6f44ca6ff
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 85%

---

# Liste

Listenvariablen sind benutzerspezifische Variablen, die Sie beliebig verwenden können. Sie funktionieren ähnlich wie eVars, allerdings können sie mehrere Werte im selben Treffer enthalten. Listenvariablen haben keine Zeichenbeschränkung.

Vergewissern Sie sich, dass Sie die Verwendung der einzelnen Listenvariablen und deren Logik in Ihrem [Lösungsdesigndokument](../../prepare/solution-design.md) aufzeichnen.

>[!NOTE]
>
>Listenvariablen speichern die letzten 250 Werte pro Besucher. Wenn mehr als 250 eindeutige Werte für einen bestimmten Besucher vorhanden sind, werden die ältesten Werte nicht den Metriken zugeordnet.

## Einrichten von Listenvariablen in den Report Suite-Einstellungen

Stellen Sie sicher, dass Sie jede Listenvariable in den Report Suite-Einstellungen konfigurieren, bevor Sie sie in Ihrer Implementierung verwenden. Weitere Informationen finden Sie im Admin-Handbuch unter [Konversionsvariablen](/help/admin/admin/conversion-var-admin/list-var-admin.md).

## Listenvariablen mit dem Web SDK

Listenvariablen sind [für Adobe Analytics zugeordnet](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) unter den XDM-Feldern `_experience.analytics.customDimensions.lists.list1` nach `_experience.analytics.customDimensions.lists.list3`.

## Listenvariablen mit der Adobe Analytics-Erweiterung

Es gibt kein spezielles Feld in der Adobe Analytics-Erweiterung, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.list1 - s.list3 in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Jede Listenvariable ist eine Zeichenfolge, die für Ihr Unternehmen spezifische benutzerdefinierte Werte enthält. Sie haben keine maximale Byte-Anzahl; jeder einzelne Wert hat jedoch ein Maximum von 255 Byte. Das Trennzeichen, das Sie verwenden, wird beim Einrichten der Variablen in den Report Suite-Einstellungen festgelegt. Verwenden Sie keine Leerzeichen, wenn Sie mehrere Elemente trennen.

```js
// A list variable configured with a comma as a delimiter
s.list1 = "Example value 1,Example value 2,Example value 3";
```

>[!TIP]
>
>Wenn Sie im selben Treffer doppelte Werte festlegen, dedupliziert Adobe alle Instanzen dieser Werte. Wenn Sie z. B. `s.list1 = "Example,Example";` festlegen, wird eine Instanz in Berichten gezählt.

## Vergleich von Listen-Props mit Listenvariablen

Listen-Props und Listenvariablen können beide im selben Treffer mehrere Werte enthalten. Zwischen diesen beiden Variablentypen gibt es jedoch einige wichtige Unterschiede.

* Jede Prop kann eine Listen-Prop werden. Sie können bis zu 75 Listen-Props haben, wenn jede Prop eine Listen-Prop ist. Es sind nur 3 Listenvariablen verfügbar.
* Listen-Props haben eine 100-Byte-Grenze für die gesamte Variable. Listenvariablen haben eine 255-Byte-Grenze pro Wert und keine Gesamt-Byte-Grenze.
* Listen-Props bleiben nicht über den festgelegten Treffer hinaus erhalten. Für Listenvariablen gelten die gewünschten Gültigkeitseinstellungen. Bei der [Berichtszeitverarbeitung](/help/components/vrs/vrs-report-time-processing.md) können Sie jedoch sowohl auf Listen-Props als auch auf Listenvariablen eine benutzerdefinierte Attribution anwenden.
