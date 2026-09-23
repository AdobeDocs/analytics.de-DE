---
title: Betriebssystemtypen
description: Das Betriebssystem unabhängig von der Version.
feature: Dimensions
exl-id: 0afd5261-98e8-4247-865a-1b8844c53ff4
TQID: https://experienceleague.adobe.com/onZ7Wt7A44gd42hqmjqYHL7OF6VtBke1NDgu1tsnMIg
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
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
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 40%
---
# Betriebssystemtypen

Die Dimension „Betriebssystemtypen[&#x200B; zeigt das übergeordnete Betriebssystem an](overview.md) das der Besucher verwendet hat, unabhängig von bestimmten Versionen. Diese Dimension ist nützlich, um nicht nur zu verstehen, welches spezifische Betriebssystem und welche Version am häufigsten verwendet werden, sondern auch, welche typische Betriebssystemplattform Besuchende verwenden.

## Füllen dieser Dimension mit Daten

Adobe leitet diese Dimension vom `User-Agent`-HTTP-Header ab und ordnet sie einer internen Lookup-Tabelle zu, die Adobe in Zusammenarbeit mit [DeviceAtlas](https://deviceatlas.com/) verwaltet. Es gibt keine Variable zum Festlegen.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (vom Benutzeragenten abgeleitet) |
| **Feld Web SDK/XDM** | Keine (vom Benutzeragenten abgeleitet) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | k. A. |

* Bei AppMeasurement-Implementierungen ist diese Dimension vorkonfiguriert.
* Aktivieren Sie für Web SDK-Implementierungen [!UICONTROL Gerätesuche] beim [Konfigurieren eines Datenstroms](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de).

## Dimensionselemente

Dimension-Elemente umfassen den Typ des verwendeten Betriebssystems. Beispiele sind `"Microsoft Windows"`, `"Apple Macintosh"`, `"Google Android"` und `"Apple iOS"`.
