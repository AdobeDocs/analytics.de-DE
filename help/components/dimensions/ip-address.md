---
title: IP-Adresse
description: Die IP-Adresse, von der jeder Treffer gesendet wurde, verfügbar in Data Warehouse.
feature: Dimensions
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: d4db20e3498d54162806b3fdef0b34f45c93a6ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 17%

---

# IP-Adresse

Die Dimension „IP[Adresse](overview.md) listet die IP-Adresse auf, von der jeder Treffer gesendet wurde.

>[!IMPORTANT]
>
>Diese Dimension ist nur in Data Warehouse verfügbar.

## Füllen dieser Dimension mit Daten

AppMeasurement erfasst die IP-Adresse automatisch aus dem HTTP-Header jeder Bildanforderung. Dies entspricht der `ip` Spalte in Daten-Feeds. Siehe [Datenspaltenreferenz](../../export/analytics-data-feed/c-df-contents/datafeeds-reference.md) für weitere Informationen.

Wenn [!UICONTROL IP-Verschleierung] in den allgemeinen Kontoeinstellungen [ Report Suite aktiviert ist](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md) werden IP-Adressen überall in Analytics, einschließlich Data Warehouse, verschleiert oder entfernt.

## Dimensionselemente

Dimension-Elemente enthalten die IP-Adressen, von denen Treffer gesendet wurden.
