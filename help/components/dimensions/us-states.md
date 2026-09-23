---
title: US-Staaten
description: Der US-Bundesstaat des Besuchers.
feature: Dimensions
exl-id: d4506e59-c1ff-4348-912d-c1ad73278f56
TQID: https://experienceleague.adobe.com/YLZIz1-J-LVvases2X1AgNxQR1eTtqoeDoxFVCg2MV4
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
subfeature_v2:
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
    internal-label: Appmeasurement implementation
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
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 64%
---
# US-Bundesstaat

Die Dimension „US[Bundesstaat](overview.md) zeigt den Status des Besuchers in den Vereinigten Staaten von Amerika an. Sie ähnelt der Dimension [Regionen](regions.md), allerdings ist diese Dimension spezifisch für die USA. Die Verwendung dieser Dimension ist hilfreich, wenn Sie Einblicke wünschen, die detaillierter sind als [Länder](countries.md), aber nicht so detailliert wie [Städte](cities.md).

## Füllen dieser Dimension mit Daten

Adobe leitet diese Dimension Server-seitig von der IP-Adresse des Besuchers ab und ordnet sie einer internen Lookup-Tabelle zu. Adobe arbeitet mit [Digital Element](https://www.digitalelement.com/) zusammen, um Suchen zwischen IP-Adressen und dem US-Bundesstaat zu verwalten. Es gibt keine Variable zum Festlegen.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (abgeleitet von der IP-Adresse des Besuchers) |
| **Feld Web SDK/XDM** | Keine (abgeleitet von der IP-Adresse des Besuchers) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | k. A. |

* Bei AppMeasurement-Implementierungen ist diese Dimension vorkonfiguriert.
* Aktivieren Sie für Web SDK-Implementierungen [!UICONTROL Geo-Suche] beim [Konfigurieren eines Datenstroms](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de).

## Dimensionselemente

Zu den Dimensionselementen gehören Regionen und das Land, in dem sich die Region befindet. Zu den Beispielwerten gehören `"California"`, `"Texas"` oder `"Virginia"`. Das Dimensionselement `"Unspecified"` umfasst den gesamten internationalen Traffic außerhalb der Vereinigten Staaten.

Diese Dimension kann `"AOL"`, einen DFÜ-Dienstleister umfassen. Abonnenten dieses Dienstes wird ein Zugangspunkt zugewiesen. AOL-Benutzer verwenden die IP-Adresse dieses Zugriffspunkts. Da diese Dimension auf der IP-Adresse basiert, wird die Geolokalisierung des Zugangspunkts anstelle des tatsächlichen Standorts der Besucherin bzw. des Besuchers verwendet.

## Unterschiede zwischen gemeldetem und tatsächlichem Standort

Da diese Dimension auf der IP-Adresse basiert, kann in einigen Szenarien ein Unterschied zwischen dem gemeldeten und dem tatsächlichen Standort angezeigt werden:

* **IP-Adressen, die Unternehmensproxys darstellen**: Diese Besucher können als Traffic erscheinen, der über das Unternehmensnetzwerk des Benutzers kommt. Dies kann ein anderer Standort sein, wenn der Benutzer remote arbeitet.
* **Mobile IP-Adressen**: Die mobile IP-Zielerfassung funktioniert auf unterschiedlichen Ebenen, je nach Standort und Netzwerk. Einige Fluggesellschaften befördern den IP-Verkehr über zentrale oder regionale Anlaufstellen.
* **Satelliten-ISP-Benutzer**: Es ist schwierig, den spezifischen Standort dieser Benutzer zu identifizieren, da sie in der Regel vom Uplink-Standort zu stammen scheinen.
* **Militärische und staatliche IPs**: Die Mitarbeiter sind weltweit unterwegs und der Zugriff erfolgt eher über ihren Heimatstandort als von der Basis oder der Behörde aus, in der sie gegenwärtig beschäftigt sind.
* **Proxys, die IP-Adressen aus Datenschutzgründen verdecken**: Services wie das Private Relay von Apple verbergen die wahre IP-Adresse, indem sie zufällig Daten über einen Vermittler oder Proxy senden. Dieser Proxy ersetzt dann eine andere IP-Adresse, bevor er an Adobe weitergeleitet wird.
