---
title: IP-Adresse
description: Die IP-Adresse, von der jeder Treffer gesendet wurde, verfügbar in Data Warehouse.
feature: Dimensions
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
source-wordcount: '153'
ht-degree: 16%
---
# IP-Adresse

Die Dimension „IP[Adresse](overview.md) listet die IP-Adresse auf, von der jeder Treffer gesendet wurde.

>[!IMPORTANT]
>
>Diese Dimension ist nur in Data Warehouse verfügbar.

## Füllen dieser Dimension mit Daten

AppMeasurement erfasst die IP-Adresse automatisch aus dem HTTP-Header jeder Bildanforderung. Dies entspricht der `ip` Spalte in Daten-Feeds. Siehe [Datenspaltenreferenz](../../export/analytics-data-feed/c-df-contents/datafeeds-reference.md) für weitere Informationen.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (aus der HTTP-Anfrage) |
| **Feld Web SDK/XDM** | Keine (aus der HTTP-Anfrage) |
| **Abfrageparameter** | Keine (aus der HTTP-Anfrage) |
| **XML-Tag** | [`<ipAddress>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Byte-Grenze** | k. A. |
| **Persistenz** | k. A. |

Wenn [!UICONTROL IP-Verschleierung] in den allgemeinen Kontoeinstellungen [&#x200B; Report Suite aktiviert ist](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md) werden IP-Adressen überall in Analytics, einschließlich Data Warehouse, verschleiert oder entfernt.

## Dimensionselemente

Dimension-Elemente enthalten die IP-Adressen, von denen Treffer gesendet wurden.
