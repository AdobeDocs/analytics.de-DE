---
title: AMO-ID
description: Die Adobe Media Optimizer-ID, die in Adobe Advertising-Integrationen verwendet wird.
feature: Dimensions
source-git-commit: 408d8db0d1e3c8301a066fe54d611ec7b8e3418a
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 3%

---

# AMO-ID

Die **[!UICONTROL AMO ID]** ist eine Sammlung verketteter Kennungen, die in Adobe Advertising-Integrationen verwendet werden. Die in dieser Dimension gespeicherten Werte werden zur Verwendung in Analytics-Berichten automatisch in separate, für Menschen besser lesbare Klassifizierungsdimensionen unterteilt. Die Dimension wird automatisch erstellt, wenn die Integration von [Analytics for Advertising](https://experienceleague.adobe.com/en/docs/advertising/integrations/analytics/overview) aktiviert wird.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst ihre Werte auf verschiedene Weise:

* Für Clickthrough-Traffic werden Daten aus dem `s_kwcid` Abfragezeichenfolgenparameter in der [Seiten-URL](page-url.md) erfasst, normalerweise auf der Seite, über die anzeigengesteuerter Traffic auf die Website gelangt.
* Clickthrough-Traffic kann auch erfasst werden, wenn die URL keine Trackingcodes enthält, der Adobe Advertising JavaScript jedoch innerhalb der letzten zwei Minuten einen Klick erkennt.
* Für unterstützten View-Through-Traffic ergänzt Adobe Advertising die Werte im Backend mithilfe einer zusätzlichen ID (`SDID`).

## Dimensionselemente

Dimension-Elemente enthalten AMO-IDs, auch als `s_kwcid` bezeichnet. Das genaue Format hängt davon ab, ob der Traffic von DSP oder von Search, Social und Commerce stammt. AMO-IDs sind weniger granulär als EF-IDs und werden hauptsächlich für Klassifizierungen und die Aufnahme von Adobe Advertising-Metriken in Analytics verwendet.

### DSP

```text
AC!{ad key}!{placement key}
```

* **`AC`**: Zeigt den Anzeigekanal an.
* **`ad key`**: Adobe Advertising-generierte alphanumerische Kennung für die Anzeige.
* **`placement key`**: Adobe Advertising-generierte alphanumerische Kennung für die Platzierung.

Beispielwert:

```text
AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7
```

### Anzeigen für Suche, Social Media und Commerce

Die AMO-IDs für Suche, Social und Commerce beginnen mit `AL`, gefolgt von der Advertiser-Benutzer-ID, der ID des Werbenetzwerkkontos und den netzwerkspezifischen IDs. Zu den IDs für freigegebene Werbenetzwerkkonten gehören:

* **`3`**: Google Ads
* **`10`**: Microsoft Advertising
* **`45`**: Meta
* **`86`**: Yahoo! Display-Netzwerk
* **`87`**: Naver
* **`88`**: Baidu
* **`90`**: Yandex
* **`94`**: Yahoo! Japan Ads
* **`105`**: Yahoo Native (veraltet)
* **`106`**: Pinterest (veraltet)

#### Google Ads

Google Ads verwendet zwei verwandte Formate. Neuere Konten können die Kampagnen-ID und die Anzeigengruppen-ID enthalten, die das Reporting auf Kampagnen- und Anzeigengruppenebene für Kampagnen mit dem Typ „Performance Max“ und „Entwürfe/Experimente“ unterstützt.

```text
AL!{user}!3!{creative}!{matchtype}!{placement}!{network}!{product partition}!{keyword}[!{campaign id}!{ad group id}]
```

* **`creative`**: Kreativ-ID für Google Ads.
* **`matchtype`**: Typ der Keyword-Übereinstimmung (`e` für exakt, `p` für Phrase, `b` für allgemein).
* **`placement`**: Domain, auf der auf die Anzeige geklickt wurde.
* **`network`**: Netzwerk, in dem der Klick aufgetreten ist (`g` für die Google-Suche, `s` für einen Suchpartner, `d` für die Anzeige).
* **`product partition`**: Produktgruppen-ID für Produktanzeigen.
* **`keyword`**: Keyword auf Such-Sites auslösen oder am besten übereinstimmendes Keyword auf Inhalts-Sites.
* **`campaign id`**: Google Ads-Kampagnen-ID, falls vorhanden.
* **`ad group id`**: Google Ads-Anzeigengruppen-ID, falls vorhanden.

Bei dynamischen Suchanzeigen wird das Keyword-Feld mit dem automatischen Targeting ausgefüllt.

Beispiel:

```text
AL!1234!3!569345525675!e!!g!!adobe express!15557590691!136734402131
```

#### Microsoft Advertising

```text
AL!{user}!10!{ad id}!!!!{keyword/order item id}!!{campaign id}!{ad group id}
```

* **`ad id`**: Microsoft Advertising Creative ID.
* **`keyword/order item id`**: Microsoft Advertising Schlüsselwort-ID.
* **`campaign id`**: Microsoft Advertising-Kampagnen-ID.
* **`ad group id`**: Anzeigengruppen-ID für Microsoft Advertising.

Für einige nicht migrierte Konten können weiterhin Legacy-Microsoft-Formate vorhanden sein.

Beispiel:

```text
AL!1234!10!79577297926903!!!!79577437127536!!291647087!1273234845019564
```

#### Baidu

```text
AL!{user}!88!{creative}!{placement}!{keyword id}
```

* **`creative`**: Baidu-Kreativ-ID.
* **`placement`**: Website, auf der die Anzeige angeklickt wurde.
* **`keyword id`**: Baidu-Schlüsselwort-ID.

#### Yahoo! Japan Ads

```text
AL!{user}!94!{creative}!{matchtype}!{network}!{keyword}
```

* **`creative`**: Yahoo! Japan Ads Kreativ-ID.
* **`matchtype`**: Typ der Keyword-Übereinstimmung (`be` exakt, `bp` Phrase `bb` breit).
* **`network`**: Netzwerk, in dem der Klick aufgetreten ist (`n` nativ, `s` Suche).
* **`keyword`**: Keyword wird ausgelöst.

#### Yandex

```text
AL!{user}!90!{ad id}!{source type}!!!{phrase id}
```

* **`ad id`**: Kreative ID von Yandex.
* **`source type`**: Site-Typ, auf dem die Anzeige angezeigt wurde (`b` Suche, `c`/Inhalt, `ct` Kategorie).
* **`phrase id`**: Yandex-Schlüsselwort-ID.

## Klassifizierungen

Bei Aktivierung der [Analytics for Advertising](https://experienceleague.adobe.com/en/docs/advertising/integrations/analytics/overview)-Integration werden automatisch die folgenden Klassifizierungen erstellt. Klassifizierungswerte werden automatisch von der Integration verwaltet.

| Klassifizierung | Beschreibung | DSP | Suche,<br>Social, &amp;<br>Commerce |
| --- | --- | :---: | :---: |
| **[!UICONTROL Konto]** | Der Kontoname. | &check; | &check; |
| **[!UICONTROL Anzeige-URL]** | Die in der Anzeige angezeigte URL. | | &check; |
| **[!UICONTROL Anzeigenbeschreibung]** | Die Anzeigenbeschreibung (DSP) oder der Anzeigenhauptteil (Suche, Social und Commerce). | &check; | &check; |
| **[!UICONTROL Werbeziel-URL]** | Die Ziel-URL für die Anzeige. | | &check; |
| **[!UICONTROL Anzeigengruppe]** | Der Name der Anzeigengruppe. | | &check; |
| **[!UICONTROL Anzeigenplattform]** | Der Name der Advertising DSP oder Suchmaschine. | &check; | &check; |
| **[!UICONTROL Anzeigentitel]** | Der Anzeigentyp (DSP) oder Anzeigentitel (Suche, Social und Commerce). | &check; | &check; |
| **[!UICONTROL Ad Type]** | Der Anzeigentyp, z. B. `text`, `video`, `display` oder `native`. | &check; | &check; |
| **[!UICONTROL AdCloud-Attribut 1]** -<br>**[!UICONTROL AdCloud-Attribut 5 &#x200B;]** | Platzhalterklassifizierungen, die für zukünftige benutzerdefinierte Attribute reserviert sind. Wird derzeit nicht verwendet. | | |
| **[!UICONTROL Kampagne]** | Der Kampagnenname. | &check; | &check; |
| **[!UICONTROL Creative Experience Name]** | Name des Kreativerlebnisses, das mit der Anzeigeninteraktion verknüpft ist und eine Gruppe kreativer Varianten darstellt, die beim Testen oder bei der Personalisierung verwendet werden. | &check; | |
| **[!UICONTROL Name der Creative-Verzweigung]** | Name der Verzweigung innerhalb eines kreativen Erlebnisses, die eine bestimmte Variante oder einen bestimmten Pfad im kreativen Experiment darstellt. | &check; | |
| **[!UICONTROL Creative-Verzweigungs-ID]** | Eindeutige Kennung, die einer kreativen Verzweigung innerhalb eines kreativen Erlebnisses zugewiesen ist. | &check; | |
| **[!UICONTROL Creative-Name]** | Name des spezifischen und kreativen Assets, das dem Benutzer bereitgestellt wurde. | &check; | |
| **[!UICONTROL Creative-Variantenname]** | Name der spezifischen Variante eines Kreativprodukts, das in einem Kreativerlebnis oder einer Kreativverzweigung verwendet wird. | &check; | |
| **[!UICONTROL Keyword]** | Das Keyword . | | &check; |
| **[!UICONTROL Übereinstimmungstyp des Keywords]** | Das Keyword und der Übereinstimmungstyp. | | &check; |
| **[!UICONTROL Landing Type]** | Ob es sich bei dem Einstiegsseiteneintrag um eine Durchsicht oder einen Clickthrough handelte. | &check; | &check; |
| **[!UICONTROL Übereinstimmungstyp]** | Der Suchtyp. | | &check; |
| **[!UICONTROL Netzwerk]** | RTB (DSP) oder der Name des Werbenetzwerks (Search, Social und Commerce). | &check; | &check; |
| **[!UICONTROL Optimierung]** | Der Paketname (DSP) oder Portfolioname (Search, Social und Commerce). | &check; | &check; |
| **[!UICONTROL Platzierung]** | Der Name der Platzierung. | &check; | |
| **[!UICONTROL Produktzielgruppe]** | Die Produktzielgruppe für eine Produktlistenanzeige. | | &check; |
