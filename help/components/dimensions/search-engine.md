---
title: Suchmaschine
description: Die Suchmaschine, mit der der Besucher Ihre Site erreichte.
feature: Dimensions
exl-id: 2815f1fa-d938-4d2b-b864-c4ed834f3ed3
TQID: https://experienceleague.adobe.com/fOk6ypu24XzT6aypOHUAE-RYSW39wyrzkyt-lvOKy7Y
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
source-wordcount: '265'
ht-degree: 69%
---
# Suchmaschine

Die Dimension „Suchmaschine[&#x200B; zeigt die Suchmaschinen an](overview.md) die Besucher verwenden, um zu Ihrer Site zu gelangen. Ein Referrer muss die beiden folgenden Kriterien erfüllen, um als Suchmaschine klassifiziert zu werden:

* Die Referrer-Domain wird von Adobe als gültige Suchmaschine erkannt.
* In der Referrer-URL ist ein Keyword-Abfragezeichenfolge-Parameter vorhanden. Der Abfragezeichenfolge-Parameter kann leer sein (wie dies bei mehreren Suchmaschinen aufgrund von Datenschutzpraktiken der Fall ist).

Wenn Sie zwischen gebührenpflichtiger und kostenloser Suche unterscheiden möchten, ist eine [Gebührenpflichtige Sucherkennung](/help/admin/tools/manage-rs/edit-settings/general/paid-search-detection/paid-search-detection.md) erforderlich. Für Suchmaschinen stehen mehrere Dimensionen zur Verfügung:

* **Suchmaschine**: Die Suchmaschine, mit der Sie Ihre Site erreichen, unabhängig davon, ob die Suche gebührenpflichtig oder kostenlos ist.
* **Suchmaschine – bezahlt**: Die Suchmaschine, mit der Ihre Site erreicht wurde und die mit der gebührenpflichtigen Sucherkennung übereinstimmt.
* **Suchmaschine – kostenlos**: Die Suchmaschine, mit der Ihre Site erreicht wurde und die nicht mit der gebührenpflichtigen Sucherkennung übereinstimmt.

## Füllen dieser Dimension mit Daten

Adobe leitet diese Dimension vom [Referrer](referrer.md) jedes Treffers ab und ordnet sie mehreren Adobe-internen Suchtabellen zu. Es gibt keine Variable zum Festlegen. Da jeder Wert vom Referrer abhängt, stellen Sie sicher, dass die Dimension „Referrer“ und [Interne URL-Filter](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) korrekt konfiguriert sind.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (abgeleitet vom Referrer) |
| **Feld Web SDK/XDM** | Keine (abgeleitet vom Referrer) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | nicht angegeben |

## Dimensionselemente

Zu den Dimensionselementen gehören Suchmaschinen, die zum Erreichen Ihrer Site verwendet werden. Zu den Beispielwerten gehören `"Google"`, `"Microsoft Bing"` und `"DuckDuckGo"`. Das Dimensionselement `"Unspecified"` ist der gesamte Traffic ohne Suchvorgänge.
