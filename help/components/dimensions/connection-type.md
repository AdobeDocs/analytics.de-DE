---
title: Verbindungstyp
description: Wie sich der Besucher mit dem Internet verbindet.
feature: Dimensions
exl-id: 149b2353-6128-4e0c-a73a-bc5a37c66b52
TQID: https://experienceleague.adobe.com/5kdDrW5vGzc4EKpLOF4VWzXish439t-aGp6q-XcK3Fs
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 236
ht-degree: 94%

---

# Verbindungstyp

Der „Verbindungstyp“ (Dimension[ gibt ](overview.md), wie der Besucher eine Internetverbindung hergestellt hat. Diese Dimension ist nützlich, um festzustellen, wie Besucher eine Internetverbindung herstellen, um auf Ihrer Site zu surfen. Damit können Sie den Site-Inhalt entsprechend der Verbindungsgeschwindigkeit der Besucher optimieren.

## Füllen dieser Dimension mit Daten

Diese Dimension verwendet eine Kombination aus der [`ct` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) und der Server-seitigen Logik von Adobe. Adobe setzt die folgenden Regeln ein, um den Wert der Dimension zu bestimmen:

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
