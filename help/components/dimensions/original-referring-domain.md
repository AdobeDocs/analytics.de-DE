---
title: Ursprüngliche Referrer-Domain
description: Die erste Referrer-Domäne, auf der sich ein Besucher befand, bevor er zu Ihrer Site klickte.
feature: Dimensions
exl-id: 6b9ac662-a79a-477b-8612-7980da7cfadd
TQID: https://experienceleague.adobe.com/G-se6LH33gMTt8ttrP5RBzL85m335ujtbiSm6EjLGuU
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 409
ht-degree: 95%

---

# Ursprüngliche Referrer-Domain

Die Dimension „Ursprüngliche Referrer[&#x200B; gibt die erste Referrer](overview.md)Domain an, auf die sich ein Besucher geklickt hat, um zu Ihrer Site zu gelangen. Sobald sie festgelegt wurde, enthält sie denselben Wert für die gesamte Lebensdauer dieser Besucher-ID. Diese Dimension ist nützlich, um zu verstehen, welche Drittanbieter-Sites den Traffic ursprünglich zu Ihrer Site leiten.

>[!IMPORTANT]
>
>Sie müssen die [internen URL-Filter](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) Ihrer Report Suite konfigurieren, um diese Dimension verwenden zu können. Wenn die internen URL-Filter nicht konfiguriert werden, können entweder interne Domänen enthalten sein oder die Anzeige externer Domänen verhindert werden.

## Füllen dieser Dimension mit Daten

Diese Dimension muss sowohl in der Analytics-Oberfläche als auch in Ihrer Implementierung konfiguriert werden.

* Innerhalb Ihrer Implementierung ruft diese Dimension Daten aus der [`r` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mithilfe der JavaScript-Variablen `document.referrer` im Browser. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Tags in Adobe Experience Platform), ist diese Dimension vorkonfiguriert. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Abfragezeichenfolgenparameter `r` bei allen Bildanforderungen einbeziehen.
* Auf der Analytics-Benutzeroberfläche müssen Sie die [internen URL-Filter](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) Ihrer Report Suite konfigurieren. Wenn die internen URL-Filter nicht konfiguriert werden, können entweder interne Domänen enthalten sein oder die Anzeige externer Domänen verhindert werden.

Adobe behält die ursprüngliche Referrer-Domäne für die gesamte Lebensdauer eines Besuchers bei. Wenn ein Besucher zu irgendeinem Zeitpunkt einen Link auf einer anderen Domain durchklickt, wird der neue Wert nicht erfasst. Informationen zum Anzeigen der neuen Werte finden Sie unter [Referrer-Domäne](referring-domain.md).

## Dimensionselemente

Zu den Dimensionselementen gehören die Domänen, durch die Besucher zu Ihrer Site klicken. Wenn ein Treffer keine Referrer-Daten (entweder gesetzt oder beibehalten) enthält, wird er unter dem Dimensionselement `"None"` gruppiert. Dieses Dimensionselement bedeutet, dass kein Referrer-Wert vorhanden ist, z. B. wenn der Besucher die Browser-Adresse manuell in die Adressleiste eingegeben oder auf ein Lesezeichen geklickt hat.

## Referrer-Domäne im Vergleich zur ursprünglichen Referrer-Domäne

Die Referrer-Domäne kann sich zwischen Besuchen ändern. So gelangt beispielsweise ein Besucher über `google.com` zu Ihrer Site und dann eine Woche später über `twitter.com`. Eventuell tätigt er einen Kauf auf Ihrer Site. Wenn Sie Referrer-Domäne als Dimension mit Letztkontakt-Attribution verwenden, wird der Kauf `twitter.com` gutgeschrieben. Wenn Sie die ursprüngliche Referrer-Domäne als Dimension verwenden, wird der Kauf unabhängig vom Attributionsmodell `google.com` gutgeschrieben.

Die ursprüngliche Referrer-Domäne ändert sich während der gesamten Lebensdauer einer bestimmten Besucher-ID nie.
