---
title: Einverständnisverwaltungs-Opt-in
description: Ermitteln Sie, zu welchen Datenschutzeinstellungen sich ein Besucher bzw. eine Besucherin angemeldet hat.
exl-id: b2768180-b763-41fb-8cba-665fac047e29
feature: Dimensions
TQID: https://experienceleague.adobe.com/hvtKcglMPFz4FbInpuSs9haS5SwGNQpVWXn12M1x658
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
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
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 78%
---
# Einverständnisverwaltungs-Opt-in

Die Dimension „Einverständnisverwaltungs-Opt[ zeigt an](overview.md) welche Datenschutzeinstellungen ein Besucher bzw. eine Besucherin akzeptiert hat. Sie können diese Dimension verwenden, um Daten basierend auf Datenschutzeinstellungen zu filtern oder die häufigsten Gründe für ein Datenschutz-Opt-in anzuzeigen.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst Daten aus den folgenden [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md):

* `contextData.['opt.dmp']`, wenn auf `Y` gesetzt. Wenn `opt.dmp` gleich `N` ist, wird stattdessen die Dimension [Einverständnisverwaltungs-Opt-out](cm-opt-out.md) ausgefüllt.
* `contextData.['opt.sell']`, wenn auf `Y` gesetzt. Wenn `opt.sell` gleich `N` ist, wird stattdessen die Dimension [Einverständnisverwaltungs-Opt-out](cm-opt-out.md) ausgefüllt.

Ihr Unternehmen bestimmt die Logik zur Implementierung dieser Kontextdatenvariablen. Legen Sie jede Kontextdatenvariable auf jeder Seite fest.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (über Einverständnissignale eingestellt) |
| **Feld Web SDK/XDM** | Keine |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | 100 Byte |
| **Persistenz** | Treffer |

## Dimensionselemente

Zu den Dimensionselementen gehören die folgenden zwei Werte:

* **`DMP`**: Der Besucher bzw. die Besucherin hat sich für die Freigabe für Datenverwaltungsplattformen entschieden. Dieses Dimensionselement ist vorhanden, wenn die Kontextdatenvariable `opt.dmp` gleich `Y` ist.
* **`SELL`**: Der Besucher bzw. die Besucherin akzeptierte die Freigabe oder den Verkauf der Daten an Dritte. Diese Dimension ist vorhanden, wenn die Kontextdatenvariable `opt.sell` gleich `Y` ist.
