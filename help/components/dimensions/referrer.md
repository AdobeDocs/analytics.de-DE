---
title: Referrer
description: Die URL, auf der sich ein Besucher befand, bevor er zu Ihrer Site durchklickte.
feature: Dimensions
exl-id: 146f0327-c73c-40f5-8cc1-584e31d163a2
TQID: https://experienceleague.adobe.com/VE1bJD2ah1N9t-fHKc5GC0-pC4YmXEDkCwhVmI5rHZQ
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
source-wordcount: '418'
ht-degree: 76%
---
# Referrer

Die Dimension „Referrer[&#x200B; gibt &#x200B;](overview.md) URLs an, auf denen sich Besucher befanden, als sie zu Ihrer Site klickten. Diese Dimension ist nützlich, um zu verstehen, welche spezifischen URLs den meisten Traffic zu Ihrer Site leiten. Auf der externen URL muss ein Link vorhanden sein, und ein Besucher muss darauf klicken, damit das Dimensionselement angezeigt wird.

>[!IMPORTANT]
>
>Sie müssen die [internen URL-Filter](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) Ihrer Report Suite konfigurieren, um diese Dimension verwenden zu können. Wenn die internen URL-Filter nicht konfiguriert werden, können entweder interne URLs enthalten sein oder die Anzeige externer URLs verhindert werden.

Derselbe Bericht kann zwischen Analysis Workspace und Data Warehouse unterschiedliche Ergebnisse anzeigen. Analysis Workspace meldet den Referrer für jede einzelne Seite, ausgenommen Werte, die mit internen URL-Filtern übereinstimmen. Data Warehouse meldet nur den ersten Referrer des Besuchs und ignoriert interne URL-Filter.

## Füllen dieser Dimension mit Daten

AppMeasurement erfasst den Referrer automatisch aus dem `document.referrer` des Browsers. Sie können den erfassten Wert mithilfe der Variablen [`referrer`](/help/implement/vars/page-vars/referrer.md) überschreiben. Sie müssen auch die Report Suite-Filter [Interne URL](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) konfigurieren. Andernfalls können entweder interne URLs eingeschlossen oder das Auftreten externer URLs verhindert werden.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | [`referrer`](/help/implement/vars/page-vars/referrer.md) |
| **Feld Web SDK/XDM** | [`web.webReferrer.URL`](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/data-types/web-information) |
| **Abfrageparameter** | [`r`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<referrer>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Byte-Grenze** | 255 Byte |
| **Persistenz** | nicht angegeben |

## Dimensionselemente

Zu den Dimensionselementen gehören die URLs, durch die Besucher zu Ihrer Site klicken. Wenn ein Treffer keine Referrer-Daten enthält, wird er unter dem Dimensionselement `"Typed/Bookmarked"` gruppiert. Dieses Dimensionselement bedeutet, dass kein Referrer-Wert vorhanden ist, z. B. wenn der Besucher die Browser-Adresse manuell in die Adressleiste eingegeben oder auf ein Lesezeichen geklickt hat. Das Dimensionselement `"Typed/Bookmarked"` wird auch bei Umleitungen angezeigt, die nicht für Analytics geeignet sind. Weitere Informationen finden Sie unter [Umleitungen und Aliase](/help/technotes/redirects.md) im Technotes-Benutzerhandbuch.

### Dimensionselemente, die `googleusercontent.com` enthalten

Benutzer können Dimensionselemente mit der Domain `googleusercontent.com` anzeigen.

* **Zwischengespeicherte Seiten**: Die Spider von Google durchsuchen ständig das Web und speichern Kopien von Seiten, falls diese offline geschaltet werden. Diese zwischengespeicherten Seiten sind neben den meisten Suchergebnissen verfügbar, indem Sie auf den Link „Zwischengespeichert“ klicken. Wenn ein Nutzer auf diesen Link klickt und den von Google zwischengespeicherten Inhalt anzeigt, ist `webcache.googleusercontent.com` ein typisches Dimensionselement.
* **Übersetzte Seiten**: Google bietet einen robusten und bequemen Übersetzungsdienst. Wenn Sie eine Site mit diesem Service anzeigen, stammt sie von `translate.googleusercontent.com`. Dieses Dimensionselement wird angezeigt, wenn der Benutzer auf einen Link klickt, um zum ursprünglichen Inhalt zurückzukehren.
