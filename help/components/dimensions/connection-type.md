---
title: Verbindungstyp
description: Wie sich der Besucher mit dem Internet verbindet.
feature: Dimensions
exl-id: 149b2353-6128-4e0c-a73a-bc5a37c66b52
TQID: https://experienceleague.adobe.com/5kdDrW5vGzc4EKpLOF4VWzXish439t-aGp6q-XcK3Fs
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
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 76%
---
# Verbindungstyp

Der „Verbindungstyp“ (Dimension[&#x200B; gibt &#x200B;](overview.md), wie der Besucher eine Internetverbindung hergestellt hat. Diese Dimension ist nützlich, um festzustellen, wie Besucher eine Internetverbindung herstellen, um auf Ihrer Site zu surfen. Damit können Sie den Site-Inhalt entsprechend der Verbindungsgeschwindigkeit der Besucher optimieren.

## Füllen dieser Dimension mit Daten

Diese Dimension wird durch eine Kombination aus erfassten Daten und Server-seitiger Adobe-Logik bestimmt, nicht durch eine von Ihnen festgelegte Variable.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine |
| **Feld Web SDK/XDM** | Keine |
| **Abfrageparameter** | [`ct`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<connectionType>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Byte-Grenze** | k. A. |
| **Persistenz** | k. A. |

Adobe setzt die folgenden Regeln ein, um den Wert der Dimension zu bestimmen:

1. Wenn die `ct` Abfragezeichenfolge `"modem"` entspricht, setze das Dimensionselement auf `"Modem"`. AppMeasurement erfasst diese Daten nur in nicht unterstützten Internet Explorer-Browsern, wodurch dieses Dimensionselement nicht oft vorkommt.
1. Überprüfen Sie die IP-Adresse des Treffers und referenzieren Sie sie auf eine Adobe-interne Nachschlagetabelle. Wenn die IP-Adresse von einem Mobilnetzbetreiber stammt, setze das Dimensionselement auf `"Mobile Carrier"`.
1. Wenn die `ct` Abfragezeichenfolge `"lan"` entspricht, setze das Dimensionselement auf `"LAN/Wifi"`.
1. Wenn der Treffer von einer [Datenquelle](/help/import/data-sources/overview.md) stammt oder anderweitig als spezieller Treffertyp gilt, setze das Dimensionselement auf `"Not specified"`.
1. Wenn keine der oben genannten Regeln erfüllt ist, verwende als Standard den Wert `"LAN/Wifi"`.

## Dimensionselemente

Zu den Dimensionselementen gehören `LAN/Wifi`, `Mobile Carrier`, `Modem` und `Not Specified`.

* **`LAN/Wifi`**: Besucher, die über das Festnetz oder einen WLAN-Hotspot mit dem Internet verbunden sind.
* **`Mobile Carrier`**: Besucher, die über einen Mobilnetzbetreiber mit dem Internet verbunden sind.
* **`Modem`**: Besucher, die über ein Modem über den nicht unterstützten Internet Explorer-Browser mit dem Internet verbunden sind.
* **`Not Specified`**: Der Treffer hatte keinen Verbindungstyp.
