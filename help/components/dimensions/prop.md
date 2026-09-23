---
title: Prop
description: Eine benutzerdefinierte Dimension, die Sie in Berichten verwenden können.
feature: Dimensions
exl-id: cf8ad65b-bc54-473e-bcfc-9c981d23e782
TQID: https://experienceleague.adobe.com/2WMG5X3GNmogf-9Bbapq78pjVg5ibQQw7Bgb0qNpF1E
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
    internal-label: Analysis Workspace
subfeature_v2:
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
    internal-label: Components
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 82%
---
# Prop

>[!BEGINSHADEBOX]

*Auf dieser Hilfeseite wird beschrieben, wie Props als [-Dimension ](overview.md). Weitere Informationen zur Implementierung von Props finden Sie unter [Props](/help/implement/vars/page-vars/prop.md) im Benutzerhandbuch zu Implementierungen.*

>[!ENDSHADEBOX]

Props sind benutzerdefinierte Variablen, die Sie beliebig verwenden können. Sie bleiben nur für den Treffer bestehen, in dem sie festgelegt werden.

>[!TIP]
>
>Adobe empfiehlt in den meisten Fällen die Verwendung von [eVars](evar.md). In früheren Versionen von Adobe Analytics hatten Props und eVars Vorteile und Nachteile. Adobe hat eVars jedoch so verbessert, dass sie fast alle Anwendungsfälle für Props erfüllen.

Wenn Sie über ein [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) verfügen, können Sie diese benutzerspezifischen Dimensionen den unternehmensspezifischen Werten zuordnen. Die Anzahl der verfügbaren Props hängt von Ihrem Vertrag mit Adobe ab. Es sind bis zu 75 Props verfügbar, wenn Ihr Vertrag mit Adobe dies unterstützt.

## Füllen von Props mit Daten

Jede Prop erfasst Daten mit der entsprechenden [`prop1` - `prop75`](/help/implement/vars/page-vars/prop.md) Variable in AppMeasurement. Beispielsweise füllt die Variable `prop1` die Dimension prop1, während die Variable `prop68` die Dimension prop68 ausfüllt.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | [`prop1` - `prop75`](/help/implement/vars/page-vars/prop.md) |
| **Feld Web SDK/XDM** | [`_experience.analytics.customDimensions.props.prop1` - `prop75`](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/field-groups/event/analytics-full-extension) |
| **Abfrageparameter** | [`c1` - `c75`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<prop1>` - `<prop75>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Byte-Grenze** | 100 Byte |
| **Persistenz** | Treffer |

## Dimensionselemente

Da Props benutzerdefinierte Zeichenfolgen in Ihrer Implementierung enthalten, bestimmt Ihr Unternehmen, welche Dimensionselemente für jede Prop gelten. Stellen Sie sicher, dass Sie den Zweck jeder Prop und die typischen Dimensionselemente in einem [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) aufzeichnen.

## Groß-/Kleinschreibung

Bei Props wird standardmäßig nicht zwischen Groß- und Kleinschreibung unterschieden. Wenn Sie denselben Wert mit verschiedenen Groß- und Kleinschreibungen senden (z. B. `"DOG"` und `"Dog"`), gruppiert Analysis Workspace ihn in demselben Dimensionselement. Es wird die erste Groß- und Kleinschreibung verwendet, die zu Beginn des Berichtsmonats vorkam. Data Warehouse zeigt den ersten aufgefundenen Wert innerhalb des Anforderungszeitraums an.

Sie können bei allen Props die Groß-/Kleinschreibung beachten. Sie können auch die Abhängigkeit von der Schreibweise für jede Prop deaktivieren, sobald sie aktiviert ist. Wenden Sie sich mit der Report Suite-ID und den gewünschten Variablen an die Adobe-Kundenunterstützung, um die Abhängigkeit von der Schreibweise zu aktivieren oder zu deaktivieren.

>[!WARNING]
>
>Beim Umschalten der Groß-/Kleinschreibung können Dimensionselemente abgeschnitten werden, unerwartete Ergebnisse bei Segmenten hervorgerufen werden und Probleme mit Filtern auftreten. Adobe empfiehlt dringend, diese Einstellung zwischen zwei größeren Zeiträumen umzuschalten, z. B. am Anfang eines Monats oder Jahres.

## Wert von Props gegenüber eVars

Adobe empfiehlt in den meisten Fällen die Verwendung von eVars. Ausnahmen von dieser Aussage sind:

* Sie können Props in Echtzeitberichten verwenden. Bei eVars dauert es mindestens 30 Minuten, bis die Daten im Reporting angezeigt werden.
* Props können zu Listen-Props werden, die mehrere Werte im selben Treffer akzeptieren. Listenvariablen sind eine separate Variable, und es sind nur drei Listenvariablen verfügbar.
* Wenn Sie Pfade für eine Prop aktivieren, stehen die Dimensionen [Einstieg](entry-dimensions.md) und [Ausstieg](exit-dimensions.md) sofort zur Verfügung. Wenn Sie Eingangs- und Ausgangsdimensionen für eVars wünschen, können Sie manuell ein Segment erstellen.

Weitere Vergleiche zwischen Props und eVars finden Sie unter [eVar](evar.md).
