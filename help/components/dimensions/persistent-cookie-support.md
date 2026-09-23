---
title: Unterstützung persistenter Cookies
description: Bestimmt, ob der Besucher persistente Cookies unterstützen kann.
feature: Dimensions
exl-id: ced69e41-d992-4c5a-8541-920aeb7186ae
TQID: https://experienceleague.adobe.com/QmbTee9NoWeTmiRdFI3p24idNhzEzK66xb5RY-KKnQ4
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
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
source-wordcount: '243'
ht-degree: 67%
---
# Unterstützung persistenter Cookies

Die Dimension „Unterstützung persistenter Cookies[ zeigt an](overview.md) ob der Treffer eine Besucherkennung verwendet hat, die von einer persistenten Quelle stammt. Die häufigste persistente Quelle ist ein Cookie, aber auch mobile Header und andere Quellen sind möglich.

## Diese Dimension mit Daten füllen

Adobe bestimmt diese Dimension Server-seitig anhand dessen, ob die Besucherkennung des Treffers aus einer Quelle stammt, die persistent ist (z. B. einem Cookie). Es gibt keine Variable zum Festlegen und die Konfiguration ist bei allen Implementierungen sofort einsatzbereit.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (Server-seitig abgeleitet) |
| **Feld Web SDK/XDM** | Keine (Server-seitig abgeleitet) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | nicht angegeben |

## Dimensionselemente

* **`Enabled`**: Die Besucher-ID des Treffers stammt aus einer Quelle, die persistent ist. Die häufigsten Beispiele sind die Abfragezeichenfolgenparameter `aid`, `fid` oder `mid`, da diese ihre Werte von einem Cookie beziehen.
* **`Disabled`**: Die Besucher-ID des Treffers stammt aus einer Quelle, die von Adobe nicht als persistent erachtet wird, z. B. IP + Benutzeragenten-Zeichenfolge. Dieses Dimensionselement enthält auch benutzerdefinierte Besucher-IDs, die die Variable [`visitorID`](/help/implement/vars/config-vars/visitorid.md) verwenden.

## Unterschied zwischen „Cookie-Unterstützung“ und „Unterstützung persistenter Cookies“

* **Unterstützung von Cookies**: AppMeasurement versucht, ein generisches Cookie zu setzen. Das Dimensionselement basiert darauf, ob das Cookie erfolgreich festgelegt wurde.
* **Unterstützung persistenter Cookies**: Das Dimensionselement basiert darauf, ob die Kennung des Treffers von einer persistenten Quelle wie einem Cookie stammt.
