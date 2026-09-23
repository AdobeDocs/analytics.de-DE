---
title: Domain
description: Die Organisation oder der ISP, die bzw. den der Besucher für den Internetzugang verwendet.
feature: Dimensions
exl-id: 292dc256-e9e7-47be-8586-774f1c047011
TQID: https://experienceleague.adobe.com/D-qRVSeU1Gx9YMDXvcDYLbSo9tCcR-0mUiD-2KsN3g4
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
  - id: c8add8f2-4250-4fd9-9cde-9707036c567d
    internal-label: Methods
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
source-wordcount: '199'
ht-degree: 31%
---
# Domain

Die Dimension „Domain[ ](overview.md) zeigt die Zugriffspunkte an, die Besucherinnen und Besucher für den Internetzugang verwenden.

>[!NOTE]
>
>Data Warehouse enthält die Dimension &quot;[!UICONTROL Domains“ ]Plural), die ähnliche Informationen ausgibt. Adobe empfiehlt, diese Dimension &quot;[!UICONTROL Domain] (Singular)“ zu verwenden, um Konsistenz zu gewährleisten.

## Füllen dieser Dimension mit Daten

Adobe leitet diese Dimension Server-seitig von der IP-Adresse des Besuchers ab und verwendet dabei mehrere Methoden, einschließlich Reverse-DNS-Lookup, um die Zugriffspunkt-Domain zu ermitteln. Adobe arbeitet mit [Digital Element](https://www.digitalelement.com/) zusammen, um diese Suche beizubehalten. Es gibt keine Variable zum Festlegen.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (abgeleitet von der IP-Adresse des Besuchers) |
| **Feld Web SDK/XDM** | Keine (abgeleitet von der IP-Adresse des Besuchers) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | k. A. |

* Bei AppMeasurement-Implementierungen ist diese Dimension vorkonfiguriert.
* Aktivieren Sie bei Web SDK-Implementierungen [!UICONTROL Netzwerksuche] beim [Konfigurieren eines Datenstroms](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de).

## Dimensionselemente

Beispiele für Dimensionselemente sind `comcast.net`, `rr.com`, `sbcglobal.net` und `amazonaws.com`. Bei diesen Domains handelt es sich um Zugriffspunkte, und nicht unbedingt um die Domain, die einen ISP oder eine Organisation repräsentiert.

Dimensionswerte von `None` bedeuten, dass der Inhaber der IP-Adresse des Zugriffspunkts keine Domain angegeben hat.
