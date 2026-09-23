---
title: Cookie-Unterstützung
description: Stellt fest, ob der Browser Cookies unterstützt.
feature: Dimensions
exl-id: 07d4fe12-0d60-469d-98b1-e93ce5a0fd21
TQID: https://experienceleague.adobe.com/axOR-Ut8kkRSCTYPescoSCa44g25E8xxp4gg-yQlyYw
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
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
source-wordcount: '211'
ht-degree: 38%
---
# Cookie-Unterstützung

Die Dimension „Cookie-Unterstützung[&#x200B; gibt &#x200B;](overview.md), ob der Browser Cookies für einen bestimmten Treffer unterstützt. Es ist nützlich, den Anteil der Besucher zu ermitteln, die Browser verwenden, die Cookies unterstützen, und diejenigen, die sie absichtlich deaktivieren.

## Füllen dieser Dimension mit Daten

Die Cookie-Unterstützung wird automatisch Client-seitig erfasst: AppMeasurement versucht, ein Cookie mit dem Namen `s_cc` festzulegen, und meldet dann, ob es vorhanden ist - `Y` ob der Browser Cookies unterstützt und aktiviert hat oder `N` ob Cookies deaktiviert sind. Dies funktioniert standardmäßig in jeder AppMeasurement- oder Web SDK (Tags)-Implementierung - es gibt keine Variable zum Festlegen. Wenn Sie Daten außerhalb von AppMeasurement oder der Web-SDK erfassen (z. B. über die API), senden Sie bei jedem Treffer `Y` oder `N`.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (automatisch erfasst) |
| **Feld Web SDK/XDM** | Keine (automatisch erfasst) |
| **Abfrageparameter** | [`k`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<cookiesEnabled>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Byte-Grenze** | 1 Byte |
| **Persistenz** | nicht angegeben |

## Dimensionselemente

Zu den Dimensionselementen gehören `Enabled`, `Disabled` und `Unknown`.

* **`Enabled`**: Der Browser unterstützt Cookies und hat diese aktiviert.
* **`Disabled`**: Cookies werden vom Browser nicht unterstützt oder sie wurden vom Besucher deaktiviert.
* **`Unknown`**: AppMeasurement konnte die Cookie-Unterstützung nicht ermitteln. Die Abfragezeichenfolge `k` war in der Bildanforderung nicht vorhanden.
