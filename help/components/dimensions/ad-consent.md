---
title: Einverständnis für Anzeigenplattform
description: Siehe die Konfiguration für die Werbezustimmung bei Werbeanbietern von Drittanbietern.
feature: Dimensions
exl-id: bf63112d-7d20-4e35-9a59-5be21135ae51
TQID: https://experienceleague.adobe.com/Ou6-B5pFx-ku9H2iEqLN0Ly6-t01CzQUODo0poMk8Bs
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
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 342
ht-degree: 3%

---

# Einverständnis für Anzeigenplattform

Die Dimension [Einverständnis zur Anzeigenplattform](overview.md) zeigt an, ob Einverständnis eingeholt wird, um Daten an Drittanbieter von Werbeanbietern wie Google, Meta und andere zu senden.

Derzeit wird diese Dimension nur für Google verwendet. Aufgrund der europäischen Datenschutzbestimmungen, dem Digital Markets Act (DMA), verlangt Google, dass Daten, die an ihre Server gesendet und in Europa erfasst werden, angeben müssen, ob eine Einwilligung eingeholt wird. Einige Analytics-Kunden senden Ereignisdaten über Adobe Advertising als Konversionsereignisse an Google.

In Zukunft kann diese Dimension verwendet werden, um die Codierung zusätzlicher Einverständnisinformationen für andere Drittanbieter von Werbung zu unterstützen.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst Daten aus den folgenden [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md)

* `contextData.['adConsent']`

Sie füllen die Kontextdatenvariable mit relevanten Werten für die Google-Einverständnisfelder

* `ad_user_data` (1. Zeichen) und
* `ad_personalization` (2. Zeichen)

Weitere Informationen finden [&#x200B; unter „Einverständnis“ in der Google Ads](https://developers.google.com/google-ads/api/reference/rpc/v15/Consent)API-Referenz.

Die möglichen Werte für jedes dieser Felder können sein:

| Wert | ad_user_data | ad_personalization |
|:-:|---|---|
| `Y` | Erteilen Sie Google Ihr Einverständnis für die Daten von Anzeigenbenutzenden. | Erteilen Sie Google Ihr Einverständnis zur Personalisierung von Anzeigen. |
| `N` | Einverständnis für Anzeigenbenutzerdaten an Google verweigern. | Einverständnis zur Personalisierung von Anzeigen an Google senden. |
| `U` | Nicht angegeben. | Nicht angegeben. |

Im folgenden Beispiel wird Google das Einverständnis für Anzeigenbenutzerdaten, nicht jedoch für die Anzeigenpersonalisierung erteilt:

```
contextData.['adConsent'] = "YN..."
```

Jenseits des ersten und zweiten Zeichens werden derzeit ignoriert.

## Verwenden der Daten

Sie können die erfassten Anzeigeneinverständnisdaten verwenden:

* Daten-Feeds: Die Daten zum Werbeeinverständnis sind über die `dataprivacydmaconsent` ([) &#x200B;](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md).
* Data Warehouse-Berichte: Die Daten zum Anzeigeneinverständnis sind über die Dimension **[!UICONTROL Anzeigenplattformeinverständnis]** verfügbar.

Ihr Unternehmen bestimmt die Logik zur Implementierung dieser Kontextdatenvariablen. Der Wert bleibt nicht über den Treffer hinaus erhalten, für den er festgelegt wurde. Daher müssen Sie die Kontextdatenvariable auf jeder Seite festlegen.

Wenn Sie Werbedaten von Adobe Analytics über Adobe Advertising als Konversionsereignisse an Google senden, wenden Sie sich an das Adobe Advertising-Team, um Unterstützung bei der Integration zu erhalten.

Weitere Informationen finden Sie unter [Datenschutzberichte](/help/admin/tools/manage-rs/edit-settings/privacy-reporting.md).
