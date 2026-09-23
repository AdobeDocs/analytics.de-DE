---
title: Referrer-Domain
description: Die übergeordnete Domain, auf der sich ein Besucher befand, bevor er zu Ihrer Site klickte.
feature: Dimensions
exl-id: 9e04cb62-6526-4d84-aff7-c962c0ce42b5
TQID: https://experienceleague.adobe.com/iLpQGPuxOFmhb-WCU0EEfhmGgHgeQaPgBmOETdCczGQ
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
    internal-label: Analysis Workspace
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
subfeature_v2:
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
    internal-label: Components
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
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 81%
---
# Referrer-Domain

Die Dimension „Referrerdomäne[ gibt an](overview.md) welche Domains Besucher durchklicken, um zu Ihrer Site zu gelangen. Diese Dimension ist nützlich, um zu verstehen, welche Drittanbieter-Sites den meisten Traffic zu Ihrer Site generieren. Auf der externen Site muss ein Link vorhanden sein und ein Besucher muss darauf klicken, damit das Dimensionselement angezeigt wird.

>[!IMPORTANT]
>
>Sie müssen die [internen URL-Filter](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) Ihrer Report Suite konfigurieren, um diese Dimension verwenden zu können. Wenn die internen URL-Filter nicht konfiguriert werden, können entweder interne Domänen enthalten sein oder die Anzeige externer Domänen verhindert werden.

Derselbe Bericht kann zwischen Analysis Workspace und Data Warehouse unterschiedliche Ergebnisse anzeigen. Analysis Workspace meldet die Referrer-Domäne für jede einzelne Seite, ausgenommen Werte, die mit internen URL-Filtern übereinstimmen. Data Warehouse meldet nur die erste Referrer-Domain des Besuchs und ignoriert interne URL-Filter.

## Füllen dieser Dimension mit Daten

Adobe leitet diese Dimension aus dem [Referrer](referrer.md) jedes Treffers ab und verwendet dabei den Domain-Teil der Referrer-URL. Es gibt keine Variable zum Festlegen. Sie müssen die „Internen URL[Filter“ Ihrer Report Suite konfigurieren](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) Andernfalls können interne Domains einbezogen oder das Auftreten externer Domains verhindert werden.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (abgeleitet vom Referrer) |
| **Feld Web SDK/XDM** | Keine (abgeleitet vom Referrer) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | Besuch |

Adobe behält die Referrer-Domain für einen Besuch bei. Wenn ein Besucher innerhalb eines einzelnen Besuchs Ihre Site verlässt und auf einer anderen Domain erneut auf einen Link zu Ihnen klickt, wird der neue Wert aktualisiert und bleibt für den Rest des Besuchs erhalten. Wenn Sie nur den ursprünglichen Wert anzeigen möchten, finden Sie weitere Informationen unter [Ursprüngliche Referrer-Domäne](original-referring-domain.md).

## Dimensionselemente

Zu den Dimensionselementen gehören die Domänen, durch die Besucher zu Ihrer Site klicken. Wenn ein Treffer keine Referrer-Daten (entweder gesetzt oder beibehalten) enthält, wird er unter dem Dimensionselement `"Typed/Bookmarked"` gruppiert. Dieses Dimensionselement bedeutet, dass kein Referrer-Wert vorhanden ist, z. B. wenn der Besucher die Browser-Adresse manuell in die Adressleiste eingegeben oder auf ein Lesezeichen geklickt hat. Das Dimensionselement `"Typed/Bookmarked"` wird auch bei Umleitungen angezeigt, die nicht für Analytics geeignet sind. Weitere Informationen finden Sie unter [Umleitungen und Aliase](/help/technotes/redirects.md) im Technotes-Benutzerhandbuch.

### Dimensionselemente, die `googleusercontent.com` enthalten

Benutzer können Dimensionselemente mit der Domain `googleusercontent.com` anzeigen.

* **Zwischengespeicherte Seiten**: Die Spider von Google durchsuchen ständig das Web und speichern Kopien von Seiten, falls diese offline geschaltet werden. Diese zwischengespeicherten Seiten sind neben den meisten Suchergebnissen verfügbar, indem Sie auf den Link „Zwischengespeichert“ klicken. Wenn ein Nutzer auf diesen Link klickt und den von Google zwischengespeicherten Inhalt anzeigt, ist `googleusercontent.com` das Dimensionselement.
* **Übersetzte Seiten**: Google bietet einen robusten und bequemen Übersetzungsdienst. Wenn Sie eine Site mit diesem Service anzeigen, stammt sie von `googleusercontent.com`. Dieses Dimensionselement wird angezeigt, wenn der Benutzer auf einen Link klickt, um zum ursprünglichen Inhalt zurückzukehren.
