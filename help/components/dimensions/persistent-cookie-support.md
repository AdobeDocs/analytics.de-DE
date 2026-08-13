---
title: Unterstützung persistenter Cookies
description: Bestimmt, ob der Besucher persistente Cookies unterstützen kann.
feature: Dimensions
exl-id: ced69e41-d992-4c5a-8541-920aeb7186ae
TQID: https://experienceleague.adobe.com/QmbTee9NoWeTmiRdFI3p24idNhzEzK66xb5RY-KKnQ4
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 207
ht-degree: 90%

---

# Unterstützung persistenter Cookies

Die Dimension „Unterstützung persistenter Cookies[ zeigt an](overview.md) ob der Treffer eine Besucherkennung verwendet hat, die von einer persistenten Quelle stammt. Die häufigste persistente Quelle ist ein Cookie, aber auch mobile Header und andere Quellen sind möglich.

## Diese Dimension mit Daten füllen

Adobe bestimmt den Wert dieser Dimension Server-seitig anhand der Quelle der Trefferkennung. Es gibt keine Möglichkeit, ihn direkt festzulegen. Dies ist bei allen Implementierungen vorkonfiguriert.

## Dimensionselemente

* **`Enabled`**: Die Besucher-ID des Treffers stammt aus einer Quelle, die persistent ist. Die häufigsten Beispiele sind die Abfragezeichenfolgenparameter `aid`, `fid` oder `mid`, da diese ihre Werte von einem Cookie beziehen.
* **`Disabled`**: Die Besucher-ID des Treffers stammt aus einer Quelle, die von Adobe nicht als persistent erachtet wird, z. B. IP + Benutzeragenten-Zeichenfolge. Dieses Dimensionselement enthält auch benutzerdefinierte Besucher-IDs, die die Variable [`visitorID`](/help/implement/vars/config-vars/visitorid.md) verwenden.

## Unterschied zwischen „Unterstützung von Cookies“ und „Unterstützung persistenter Cookies“

* **Unterstützung von Cookies**: AppMeasurement versucht, ein generisches Cookie zu setzen. Das Dimensionselement basiert auf dem erfolgreichen Setzen des Cookies.
* **Unterstützung persistenter Cookies**: Das Dimensionselement basiert darauf, ob die Kennung des Treffers von einer persistenten Quelle wie einem Cookie stammt.
