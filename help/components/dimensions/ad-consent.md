---
title: Einverständnis für Anzeigenplattform
description: Siehe die Konfiguration für die Werbezustimmung bei Werbeanbietern von Drittanbietern.
feature: Dimensions
exl-id: bf63112d-7d20-4e35-9a59-5be21135ae51
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '331'
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
