---
title: Prop
description: Eine benutzerdefinierte Dimension, die Sie in Berichten verwenden können.
feature: Dimensions
exl-id: cf8ad65b-bc54-473e-bcfc-9c981d23e782
TQID: https://experienceleague.adobe.com/2WMG5X3GNmogf-9Bbapq78pjVg5ibQQw7Bgb0qNpF1E
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2:
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 475
ht-degree: 93%

---

# Prop

*Auf dieser Hilfeseite wird beschrieben, wie Props als [-Dimension &#x200B;](overview.md). Weitere Informationen zur Implementierung von Props finden Sie unter [Props](/help/implement/vars/page-vars/prop.md) im Benutzerhandbuch zu Implementierungen.*

Props sind benutzerdefinierte Variablen, die Sie beliebig verwenden können. Sie bleiben nicht über den von ihnen festgelegten Treffer hinaus bestehen.

>[!TIP]
>
>Adobe empfiehlt in den meisten Fällen die Verwendung von [eVars](evar.md). In früheren Versionen von Adobe Analytics hatten Props und eVars Vorteile und Nachteile. Adobe hat eVars jedoch dahingehend verbessert, dass sie fast alle Anwendungsfälle für Props erfüllen.

Wenn Sie über ein [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) verfügen, können Sie diese benutzerspezifischen Dimensionen den unternehmensspezifischen Werten zuordnen. Die Anzahl der verfügbaren Props hängt von Ihrem Vertrag mit Adobe ab. Es sind bis zu 75 Props verfügbar, wenn Ihr Vertrag mit Adobe dies unterstützt.

## Füllen von Props mit Daten

Jede Prop erfasst Daten aus der [`c1` – `c75`-Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in den Bildanforderungen. Beispielsweise erfasst der Abfragezeichenfolgenparameter `c1` Daten für prop1, während der Abfragezeichenfolgenparameter `c68` Daten für prop68 erfasst.

AppMeasurement, das JavaScript-Variablen in eine Bildanforderung für die Datenerfassung kompiliert, verwendet die Variablen `prop1` – `prop75`. Die Implementierungsrichtlinien finden Sie unter [Prop](/help/implement/vars/page-vars/prop.md) im Benutzerhandbuch zu Implementierungen.

## Dimensionselemente

Da Props benutzerdefinierte Zeichenfolgen in Ihrer Implementierung enthalten, bestimmt Ihr Unternehmen, welche Dimensionselemente für jede Prop gelten. Stellen Sie sicher, dass Sie den Zweck jeder Prop und die typischen Dimensionselemente in einem [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) aufzeichnen.

## Groß-/Kleinschreibung

Bei Props wird standardmäßig nicht zwischen Groß- und Kleinschreibung unterschieden. Wenn Sie denselben Wert mit verschiedenen Groß- und Kleinschreibungen senden (z. B. `"DOG"` und `"Dog"`), gruppiert Analysis Workspace ihn in demselben Dimensionselement. Es wird die erste Groß- und Kleinschreibung verwendet, die zu Beginn des Berichtsmonats vorkam. Data Warehouse zeigt den ersten aufgefundenen Wert innerhalb des Anforderungszeitraums an.

Sie können bei allen Props die Groß-/Kleinschreibung beachten. Sie können auch die Groß-/Kleinschreibung für jede Prop deaktivieren, sobald sie aktiviert ist. Wenden Sie sich an die Adobe-Kundenunterstützung mit der Report Suite-ID und den gewünschten Variablen, um die Groß-/Kleinschreibung zu ändern.

>[!WARNING]
>
>Beim Umschalten der Groß-/Kleinschreibung können Dimensionselemente abgeschnitten werden, unerwartete Ergebnisse bei Segmenten hervorgerufen werden und Probleme mit Filtern auftreten. Adobe empfiehlt dringend, diese Einstellung zwischen zwei Hauptzeiträumen umzuschalten, z. B. am Anfang eines Monats oder Jahres.

## Wert von Props gegenüber eVars

Adobe empfiehlt in den meisten Fällen die Verwendung von eVars. Ausnahmen von dieser Aussage sind:

* Sie können Props in Echtzeitberichten verwenden. Bei eVars dauert es mindestens 30 Minuten, bis die Daten im Reporting angezeigt werden.
* Props können zu Listen-Props werden, die mehrere Werte im selben Treffer akzeptieren. Listenvariablen sind eine separate Variable, und es sind nur drei Listenvariablen verfügbar.
* Wenn Sie Pfade für eine Prop aktivieren, stehen die Dimensionen [Einstieg](entry-dimensions.md) und [Ausstieg](exit-dimensions.md) sofort zur Verfügung. Wenn Sie Eingangs- und Ausgangsdimensionen für eVars wünschen, können Sie manuell ein Segment erstellen.

Weitere Vergleiche zwischen Props und eVars finden Sie unter [eVar](evar.md).
