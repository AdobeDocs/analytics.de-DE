---
title: Suchbegriff
description: Der Suchbegriff, mit dem der Besucher Ihre Site erreichte.
feature: Dimensions
exl-id: 5a1236a6-f94b-4679-906a-b539afe36887
TQID: https://experienceleague.adobe.com/4naavrC42ddsxGFJfkOJ0wzHLTa7tdMeI9nKDgVWrBY
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
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 70%
---
# Suchbegriff

Die Dimension „Suchbegriff[ zeigt die Suchbegriffe an](overview.md) die Besucher verwenden, um zu Ihrer Site zu gelangen.

>[!IMPORTANT]
>
>Die meisten Suchmaschinen übergeben den Suchbegriff nicht mehr, da die Datenschutzpraktiken zunehmen. Treffer, bei denen Adobe eine Suchmaschine erkennt, aber ein Suchbegriff fehlt, werden unter dem Dimensionselement `"Keyword unavailable"` gruppiert.

Ein Referrer muss die beiden folgenden Kriterien erfüllen, um als Suchbegriff klassifiziert zu werden:

* Die Referrer-Domäne wird von Adobe als gültige [Suchmaschine](search-engine.md) erkannt.
* In der Referrer-URL ist ein Keyword-Abfragezeichenfolge-Parameter vorhanden. Wenn die Abfragezeichenfolge für Suchbegriffe vorhanden ist, jedoch keinen Wert enthält, wird sie unter dem Dimensionselement `"Keyword unavailable"` gruppiert.

Wenn Sie zwischen gebührenpflichtiger und kostenloser Suche unterscheiden möchten, ist eine [Gebührenpflichtige Sucherkennung](/help/admin/tools/manage-rs/edit-settings/general/paid-search-detection/paid-search-detection.md) erforderlich. Für Suchbegriffe stehen mehrere Dimensionen zur Verfügung:

* **Suchbegriff**: Der Suchbegriff, mit dem Sie Ihre Site erreichen, unabhängig davon, ob die Suche gebührenpflichtig oder kostenlos ist.
* **Suchbegriff - bezahlt**: Der Suchbegriff, mit dem Ihre Site erreicht wurde und der mit der gebührenpflichtigen Sucherkennung übereinstimmt.
* **Suchbegriff - kostenlos**: Der Suchbegriff, mit dem Ihre Site erreicht wurde und der nicht mit der gebührenpflichtigen Sucherkennung übereinstimmt.

## Füllen dieser Dimension mit Daten

Adobe leitet diese Dimension von der Suchmaschine [Referrer](referrer.md) jedes Treffers ab, indem das Keyword aus der Abfragezeichenfolge des Referrers extrahiert wird. Es gibt keine Variable zum Festlegen. Da jeder Wert vom Referrer abhängt, stellen Sie sicher, dass die Dimension „Referrer“ und [Interne URL-Filter](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) korrekt konfiguriert sind.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (abgeleitet vom Suchmaschinen-Referrer) |
| **Feld Web SDK/XDM** | Keine (abgeleitet vom Suchmaschinen-Referrer) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | nicht angegeben |

## Dimensionselemente

Zu den Dimensionselementen gehören Suchbegriffe, die zum Erreichen Ihrer Site verwendet werden. Das Dimensionselement `"Unspecified"` ist der gesamte Traffic ohne Suchvorgänge.
