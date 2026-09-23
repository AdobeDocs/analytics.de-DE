---
title: Java aktiviert
description: Bestimmt, ob Java im Browser aktiviert ist.
feature: Dimensions
exl-id: 2d4b4ea2-65ba-4d39-a040-f989b5eddc6e
TQID: https://experienceleague.adobe.com/EjiqmqpByH-q9AL-934s5HXAv78JTXpEJZ1Bwk-y5MI
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 51%
---
# Java aktiviert

Die Dimension „Java aktiviert[ bestimmt](overview.md) ob Java im Browser aktiviert ist. Das ist hilfreich, wenn Sie Java-basierte Funktionen auf Ihrer Site einführen und wissen möchten, wie viele Besucher Java bereits aktiviert haben. Für diejenigen, die Java deaktiviert haben, können Sie eine Alternative oder Anweisungen zur Aktivierung bereitstellen.

## Füllen dieser Dimension mit Daten

Java aktiviert wird automatisch Client-seitig erfasst: AppMeasurement erkennt, ob Java im Browser aktiviert ist, und meldet „Y“ oder „N“. Dies funktioniert standardmäßig in jeder AppMeasurement- oder Web SDK (Tags)-Implementierung - es gibt keine Variable zum Festlegen. Wenn Sie Daten außerhalb von AppMeasurement oder der Web-SDK erfassen (z. B. über die API), senden Sie „Y“ oder „N“, um diese Dimension zu verwenden.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (automatisch erfasst) |
| **Feld Web SDK/XDM** | Keine (automatisch erfasst) |
| **Abfrageparameter** | [`v`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<javaEnabled>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Byte-Grenze** | 1 Byte |
| **Persistenz** | nicht angegeben |

## Dimensionselemente

Zu den Dimensionselementen gehören „Aktiviert“, „Deaktiviert“ und „Nicht bekannt“.

* **Aktiviert**: Java ist im Browser aktiviert. Die Abfragezeichenfolge `v` enthielt den Wert „Y“.
* **Deaktiviert**: Java ist im Browser deaktiviert oder unterstützt Java anderweitig nicht. Die Abfragezeichenfolge `v` enthielt den Wert „N“.
* **Nicht bekannt**: AppMeasurement konnte die Java-Unterstützung nicht ermitteln. Die Abfragezeichenfolge `v` war in der Bildanforderung nicht vorhanden.
