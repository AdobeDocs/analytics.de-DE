---
title: Letztkontakt-Kanaldetail
description: Details zum neuesten Marketing-Kanal innerhalb des Interaktionsablaufs des Besuchers.
feature: Dimensions
exl-id: def03267-f3e5-4772-a707-5678c45eba6d
TQID: https://experienceleague.adobe.com/bVZVCTQQ1tZVB0qF9fxeCU1Ec6bjcspymoyOY-AQATU
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
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
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 70%
---
# Letztkontakt-Kanaldetail

Die Dimension „Detail des Letztkontaktkanals[ zeigt Details zum ](overview.md) Marketing-Kanal an, dem ein Besucher während des Interaktionszeitraums dieses Besuchers entspricht (standardmäßig 30 Tage). Diese Dimension ist nützlich, um zu verstehen, was dazu beigetragen hat, dass der Treffer einem Marketing-Kanal entsprach. Wenn beispielsweise ein Besucher zu Ihrer Site gelangt ist und mit dem Marketing-Kanal „Paid Search“ übereinstimmt, können Sie anhand des Kanaldetails sehen, welche Suchmaschine verwendet wurde oder nach welchem Schlüsselwort er gesucht hat.

## Füllen dieser Dimension mit Daten

Diese Dimension wird von Marketing-Kanal-Verarbeitungsregeln abgeleitet, die Werte aus anderen Variablen kopieren. Die verwendete Variable referenziert den Kanalwert in jeder [Marketing-Kanalverarbeitungsregel](/help/admin/tools/manage-rs/edit-settings/marketing-channels/mc-proc-rules.md). Wenn ein Treffer mit einer Marketing-Kanalverarbeitungsregel übereinstimmt, wird die Dimension [Letztkontakt-Kanal](last-touch-channel.md) auf den Kanalnamen festgelegt und diese Dimension auf den in der Regel festgelegten Kanalwert gesetzt. Es gibt keine Variable zum Festlegen.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (abgeleitet von Marketing-Kanal-Verarbeitungsregeln) |
| **Feld Web SDK/XDM** | Keine (abgeleitet von Marketing-Kanal-Verarbeitungsregeln) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | k. A. |

Führen Sie die folgenden Schritte aus, um diese Dimension auf einen bestimmten Wert zu setzen:

* Achten Sie darauf, dass sich das gewünschte Dimensionselement in einem Trefferattribut oder einer benutzerdefinierten Variable befindet.
* Legen Sie eine Marketing-Kanalverarbeitungsregel fest, die die gewünschten Kriterien für den Treffer enthält.
* Wählen Sie in der Marketing-Kanal[!UICONTROL Verarbeitungsregel den gewünschten Dropdown-Wert unter ]Kanalwert festlegen) aus.
* Der Treffer des Besuchers auf Ihrer Site muss den Kriterien entsprechen, die in der Marketing-Kanalverarbeitungsregel beschrieben sind.

## Dimensionselemente

Dimension-Elemente hängen vom Kanalwert ab, der in der Dropdown-Liste für die entsprechende Marketing-Kanal-Verarbeitungsregel aufgeführt ist. Wenn Sie beispielsweise den Wert des Kanals auf „Seiten-URL“ setzen, umfassen die Dimensionselemente die Seiten-URLs auf Ihrer Site. Wenn Sie den Wert des Kanals auf „Referrer-Domäne“ setzen, umfassen die Dimensionselemente die Domänen, auf die Besucher geklickt haben, um zu Ihrer Site zu gelangen. Diese Dimension aggregiert alle Detaildimensionselemente, unabhängig davon, auf welchem Kanal sie sich befinden.

Adobe empfiehlt, Kanalwerte für den Marketing-Kanal festzulegen, um Einblick in die Kanaldetails zu erhalten.
