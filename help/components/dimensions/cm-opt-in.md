---
title: Einverständnisverwaltungs-Opt-in
description: Ermitteln Sie, zu welchen Datenschutzeinstellungen sich ein Besucher bzw. eine Besucherin angemeldet hat.
exl-id: b2768180-b763-41fb-8cba-665fac047e29
feature: Dimensions
TQID: https://experienceleague.adobe.com/hvtKcglMPFz4FbInpuSs9haS5SwGNQpVWXn12M1x658
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 188
ht-degree: 90%

---

# Einverständnisverwaltungs-Opt-in

Die Dimension „Einverständnisverwaltungs-Opt[ zeigt an](overview.md) welche Datenschutzeinstellungen ein Besucher bzw. eine Besucherin akzeptiert hat. Sie können diese Dimension verwenden, um Daten basierend auf Datenschutzeinstellungen zu filtern oder die häufigsten Gründe für ein Datenschutz-Opt-in anzuzeigen.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst Daten aus den folgenden [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md):

* `contextData.['opt.dmp']`, wenn auf `Y` gesetzt. Wenn `opt.dmp` gleich `N` ist, wird stattdessen die Dimension [Einverständnisverwaltungs-Opt-out](cm-opt-out.md) ausgefüllt.
* `contextData.['opt.sell']`, wenn auf `Y` gesetzt. Wenn `opt.sell` gleich `N` ist, wird stattdessen die Dimension [Einverständnisverwaltungs-Opt-out](cm-opt-out.md) ausgefüllt.

Ihr Unternehmen bestimmt die Logik zur Implementierung dieser Kontextdatenvariablen. Sie bleiben nicht über den Treffer hinaus erhalten, für den sie festgelegt wurden. Daher müssen Sie jede Kontextdatenvariable auf jeder Seite festlegen.

## Dimensionselemente

Zu den Dimensionselementen gehören die folgenden zwei Werte:

* **`DMP`**: Der Besucher bzw. die Besucherin hat sich für die Freigabe für Datenverwaltungsplattformen entschieden. Dieses Dimensionselement ist vorhanden, wenn die Kontextdatenvariable `opt.dmp` gleich `Y` ist.
* **`SELL`**: Der Besucher bzw. die Besucherin akzeptierte die Freigabe oder den Verkauf der Daten an Dritte. Diese Dimension ist vorhanden, wenn die Kontextdatenvariable `opt.sell` gleich `Y` ist.
