---
title: Referrer-Domain
description: Die übergeordnete Domain, auf der sich ein Besucher befand, bevor er zu Ihrer Site klickte.
feature: Dimensions
exl-id: 9e04cb62-6526-4d84-aff7-c962c0ce42b5
TQID: https://experienceleague.adobe.com/iLpQGPuxOFmhb-WCU0EEfhmGgHgeQaPgBmOETdCczGQ
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 494
ht-degree: 97%

---

# Referrer-Domain

Die Dimension „Referrerdomäne[ gibt an](overview.md) welche Domains Besucher durchklicken, um zu Ihrer Site zu gelangen. Diese Dimension ist nützlich, um zu verstehen, welche Websites von Drittanbietern den meisten Traffic zu Ihrer Site leiten. Auf der externen Site muss ein Link vorhanden sein und ein Besucher muss darauf klicken, damit das Dimensionselement angezeigt wird.

>[!IMPORTANT]
>
>Sie müssen die [internen URL-Filter](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) Ihrer Report Suite konfigurieren, um diese Dimension verwenden zu können. Wenn die internen URL-Filter nicht konfiguriert werden, können entweder interne Domänen enthalten sein oder die Anzeige externer Domänen verhindert werden.

Derselbe Bericht kann zwischen Analysis Workspace und Data Warehouse unterschiedliche Ergebnisse anzeigen. Analysis Workspace meldet die Referrer-Domäne für jede einzelne Seite, ausgenommen Werte, die mit internen URL-Filtern übereinstimmen. Data Warehouse meldet nur die erste Referrer-Domäne des Besuchs und ignoriert interne URL-Filter.

## Füllen dieser Dimension mit Daten

Diese Dimension erfordert die Konfiguration auf der Analytics-Benutzeroberfläche und Daten in Bildanforderungen.

* Innerhalb Ihrer Implementierung ruft diese Dimension Daten aus der [`r` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mithilfe der JavaScript-Variablen `document.referrer` im Browser. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Tags in Adobe Experience Platform), ist diese Dimension vorkonfiguriert. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Abfragezeichenfolgenparameter `r` bei allen Bildanforderungen einbeziehen.
* Auf der Analytics-Benutzeroberfläche müssen Sie die [internen URL-Filter](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) Ihrer Report Suite konfigurieren. Wenn die internen URL-Filter nicht konfiguriert werden, können entweder interne Domänen enthalten sein oder die Anzeige externer Domänen verhindert werden.

Adobe behält die Referrer-Domäne für einen Besuch bei. Wenn ein Besucher innerhalb eines einzelnen Besuchs Ihre Site verlässt und auf einer anderen Domain erneut auf einen Link zu Ihnen klickt, wird der neue Wert aktualisiert und bleibt für den Rest des Besuchs erhalten. Wenn Sie nur den ursprünglichen Wert anzeigen möchten, finden Sie weitere Informationen unter [Ursprüngliche Referrer-Domäne](original-referring-domain.md).

## Dimensionselemente

Zu den Dimensionselementen gehören die Domänen, durch die Besucher zu Ihrer Site klicken. Wenn ein Treffer keine Referrer-Daten (entweder gesetzt oder beibehalten) enthält, wird er unter dem Dimensionselement `"Typed/Bookmarked"` gruppiert. Dieses Dimensionselement bedeutet, dass kein Referrer-Wert vorhanden ist, z. B. wenn der Besucher die Browser-Adresse manuell in die Adressleiste eingegeben oder auf ein Lesezeichen geklickt hat. Das Dimensionselement `"Typed/Bookmarked"` wird auch bei Umleitungen angezeigt, die nicht für Analytics geeignet sind. Weitere Informationen finden Sie unter [Umleitungen und Aliase](/help/technotes/redirects.md) im Technotes-Benutzerhandbuch.

### Dimensionselemente, die `googleusercontent.com` enthalten

Benutzer können Dimensionselemente mit der Domain `googleusercontent.com` anzeigen.

* **Zwischengespeicherte Seiten**: Die Spider von Google durchsuchen ständig das Web und speichern Kopien von Seiten, falls diese offline geschaltet werden. Diese zwischengespeicherten Seiten sind neben den meisten Suchergebnissen verfügbar, indem Sie auf den Link „Zwischengespeichert“ klicken. Wenn ein Nutzer auf diesen Link klickt und den von Google zwischengespeicherten Inhalt anzeigt, ist `googleusercontent.com` das Dimensionselement.
* **Übersetzte Seiten**: Google bietet einen robusten und bequemen Übersetzungsdienst. Wenn Sie eine Site mit diesem Service anzeigen, stammt sie von `googleusercontent.com`. Dieses Dimensionselement wird angezeigt, wenn der Benutzer auf einen Link klickt, um zum ursprünglichen Inhalt zurückzukehren.
