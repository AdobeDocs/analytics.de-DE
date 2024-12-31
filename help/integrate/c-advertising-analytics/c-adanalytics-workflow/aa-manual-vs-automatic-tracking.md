---
description: Der Tracking-Typ bestimmt, wie die Adobe Analytics-Implementierung Ihre Suchmaschinendaten verfolgt. Dieser Tracking-Typ ist ein erforderlicher Schritt, um die Adobe Analytics-Daten ordnungsgemäß um Suchmaschinendaten zu erweitern.
title: Tracking-Typ
feature: Advertising Analytics
exl-id: 3e2ed26f-dfb2-43ea-8eb6-e332cd10fb29
source-git-commit: 243da53fda562c856d95db0f6d13b7ee1a9adae5
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 32%

---

# Tracking-Typ

Der Tracking-Typ bestimmt, wie die Adobe Analytics-Implementierung Ihre Suchmaschinendaten verfolgt. Dieser Tracking-Typ ist ein erforderlicher Schritt, um die Adobe Analytics-Daten ordnungsgemäß um Suchmaschinendaten zu erweitern.

<!--

Here is a video overview of how to implement the Advertising Analytics tracking template:

>[!VIDEO](https://video.tv.adobe.com/v/23120/?quality=12)

-->

Es werden zwei Tracking-Modi unterstützt[!UICONTROL  „Auto] und [!UICONTROL Manuell].

## [!UICONTROL Auto]-Tracking {#concept_C4C6107838C947CFBB7F4E0CB94264F0}

[!UICONTROL Auto]-Tracking ermöglicht es der Advertising Cloud-Engine zu entscheiden, wie die Suchmaschinendaten verarbeitet werden sollen. Automatisches Tracking ist der einfachere Ansatz, führt jedoch möglicherweise nicht zum am besten integrierten Datensatz.

Daher müssen Sie bei Auswahl von „Automatisch“ ein Bestätigungs-Kontrollkästchen aktivieren **[!UICONTROL bevor Sie]** Kontoeinstellung speichern können.

Beachten Sie, dass Sie für die Konfiguration eines Suchmaschinenkontos mit **[!UICONTROL Auto]**-Typ für die folgenden Aktionen verantwortlich sind:

* Der `s_kwcid` und der Wert werden zu den Konto-Tracking-Vorlagen oder Landingpage-URLs im hinzugefügten Konto hinzugefügt. Dieser Parameter und Wert werden am Ende der URL eingefügt. Möglicherweise sind zusätzliche Aktionen Ihrerseits erforderlich, wenn Ihr Webserver ein bestimmtes `key=value` am Ende der URL benötigt. Oder eine Aktualisierung zur Unterstützung jedes neuen `key=value` in der URL. Sie müssen sicherstellen, dass die hinzugefügten URL-Parameter korrekt auf der endgültigen Landingpage bestehen bleiben.
* Darüber hinaus können Keywords als Teil des Wertes `s_kwcid` in die Landingpage-URL eingefügt werden. Wenn sie Sonderzeichen oder Symbole enthalten, überprüfen Sie bitte, ob Ihr Webserver diese Zeichen unterstützen kann. Beispielsweise wird ein gängiges Sonderzeichen `+`, das in Schlüsselwörtern vom Typ „Broad Match Modified“ verwendet wird.

>[!IMPORTANT]
>
>Erfahren Sie mehr darüber, ob Sie den Parameter `s_kwcid` zu Ihrer [Richtlinie zur Inhaltssicherheit](https://experienceleague.adobe.com/en/docs/id-service/using/reference/csp) hinzufügen sollten.

## Manuelles Tracking {#concept_87B28BA9E7F84BA5972F69E6F3482A33}

Mit dem manuellen Tracking können Sie festlegen, wie die Suchmaschinendaten im Advertising Analytics-Datenintegrationsprozess verarbeitet werden sollen.

### Manuelles Tracking zu Google-Konto hinzufügen {#section_41C1EB1AEB034544A5BC291F53C05C67}

Weiter unten finden Sie die Zeichenfolge, die zu Ihrem Google-Konto hinzugefügt werden muss. Sie müssen die Zeichenfolge zu allen Tracking-Vorlagen hinzufügen, die innerhalb Ihres Kontos verwendet werden.

>[!IMPORTANT]
>
>Der Wert *`<Advertising Analytics ID>`* (unten in **Fettschrift**) ist nur ein allgemeiner Wert, den Sie **durch Ihre Konto-ID-Zeichenfolge ersetzen** müssen. Sie können Ihre spezifische Konto-ID-Zeichenfolge aus dem Kontobildschirm unter dem Abschnitt [!UICONTROL Tracking] abrufen.

**Tracking-Zeichenfolge für Kampagnen:**

```
s_kwcid=AL! 
<b><Advertising Analytics ID></b>!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}
```

![Google](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/assets/google-account.png)

Beispiele für Trackingcodes in verschiedenen Tracking-Vorlagenformaten:

**`{lpurl}`**

```
{lpurl}?s_kwcid=AL!9999!3!{creative}!{matchtype}!{placement}!network}!{product_partition_id}!{keyword}
```

**`{lpurl}`mit zusätzlichem URL-Parameter**

```
{lpurl}?campaign=PPC&s_kwcid=AL!9999!3!{creative}!{matchtype}!{placement}!network}!{product_partition_id}!{keyword}
```

**Drittanbieter (DoubleClick)`{unescapedlpurl}`**

```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={unescapedlpurl}?s_kwcid=AL!9999!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}
```

**Drittanbieter (DoubleClick)`{lpurl}`**

Um sicherzustellen, dass die Zeichenfolge durch die Umleitung zur endgültigen Landingpage-URL erhalten bleibt, müssen Sie die Zeichenfolge ausreichend kodieren:

* wenn die URL eine Umleitung durchläuft und
* verwendet keinen „UnescapedLpURL“-Wert.


```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={lpurl}?s_kwcid%3DAL!9999!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}
```

### Manuelles Tracking zu Bing-Konto hinzufügen {#section_094F8ACA493C4D65B1F54A695558EBF2}

Weiter unten finden Sie die Zeichenfolge, die zu Ihrem Bing-Konto hinzugefügt werden muss. Sie müssen die Zeichenfolge zu allen finalen URL-Suffixen hinzufügen, die innerhalb Ihres Kontos verwendet werden.

>[!IMPORTANT]
>
>Der Wert _`<Advertising Analytics ID>`_(unten in **Fettschrift**) ist nur ein allgemeiner Wert, den Sie **durch Ihre Konto-ID-Zeichenfolge ersetzen**müssen. Sie können Ihre spezifische Konto-ID-Zeichenfolge aus dem Kontobildschirm unter dem Abschnitt „Tracking“ abrufen.

**Tracking-Zeichenfolge für Kampagnen:**

```
s_kwcid=AL!<Advertising Analytics ID>!10!{AdId}!{OrderItemId} 
```

![Bing](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/assets/bing-account.png)

Beispiele für Trackingcodes in verschiedenen finalen URL-Suffix-Formaten:

**{lpurl}**

```
{lpurl}?s_kwcid=AL!9999!10!{AdId}!{OrderItemId}
```

**`{lpurl}`mit zusätzlichem URL-Parameter**

```
{lpurl}?campaign=PPC&
s_kwcid=AL!9999!10!{AdId}!{OrderItemId}
```

**Drittanbieter (DoubleClick)`{unescapedlpurl}`**

```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={unescapedlpurl}?s_kwcid=AL!9999!10!{AdId}!{OrderItemId}
```

**Drittanbieter (DoubleClick)`{lpurl}`**

Um sicherzustellen, dass die Zeichenfolge durch die Umleitung zur endgültigen Landingpage-URL erhalten bleibt, müssen Sie die Zeichenfolge ausreichend kodieren:

* wenn die URL eine Umleitung durchläuft und
* verwendet keinen „UnescapedLpURL“-Wert.

```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={lpurl}?s_kwcid%3DAL!9999!10!{AdId}!{OrderItemId}
```
