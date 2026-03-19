---
title: AMO EF ID
description: Die Adobe Media Optimizer-EF-ID, die in Adobe Advertising-Integrationen verwendet wird.
feature: Dimensions
source-git-commit: 408d8db0d1e3c8301a066fe54d611ec7b8e3418a
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 4%

---

# AMO EF ID

Die **[!UICONTROL AMO EF ID]** ist eine Anzeigenklickkennung, die in Adobe Advertising-Integrationen verwendet wird. Es handelt sich dabei um ein eindeutiges Token, das Adobe Advertising verwendet, um Aktivitäten mit einem Online-Klick oder einer Anzeigenexposition auf Besucherebene zu verknüpfen. Die Dimension wird automatisch erstellt, wenn die Integration von [Analytics for Advertising](https://experienceleague.adobe.com/en/docs/advertising/integrations/analytics/overview) aktiviert wird.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst ihre Werte auf verschiedene Weise:

* Für Clickthrough-Traffic werden Daten aus dem `ef_id` Abfragezeichenfolgenparameter in der [Seiten-URL](page-url.md) erfasst, normalerweise auf der Seite, über die anzeigengesteuerter Traffic auf die Website gelangt.
* Clickthrough-Traffic kann auch erfasst werden, wenn die URL keine Trackingcodes enthält, der Adobe Advertising JavaScript jedoch innerhalb der letzten zwei Minuten einen Klick erkennt.
* Für unterstützten View-Through-Traffic ergänzt Adobe Advertising die Werte im Backend mithilfe einer zusätzlichen ID (`SDID`).

>[!NOTE]
>
>Bei EF-IDs wird zwischen Groß- und Kleinschreibung unterschieden. Wenn Ihre Implementierung das URL-Tracking in Kleinbuchstaben erzwingt, erkennt Adobe Advertising die EF-ID nicht.

## Dimensionselemente

Dimension-Elemente enthalten Ad-Click-Kennungen, die von unterstützten Werbenetzwerken generiert wurden. Das Zeichenfolgenformat hängt vom Netzwerk und Kanal ab, von dem es generiert wurde.

### Google Ads-Suchanzeigen

```text
{gclid}:G:{s}
```

* **`gclid`**: Die Google-Klick-ID (GCLID).
* **`s`**: Der Netzwerktyp (`"s"` für die Suche).

### Microsoft Advertising Suchanzeigen

```text
{msclkid}:G:{s}
```

* **`msclkid`**: Die Microsoft-Klick-ID (MSCLKID).
* **`s`**: Der Netzwerktyp (`"s"` für die Suche).

### Anzeigen und Suchanzeigen in anderen Suchmaschinen anzeigen

```text
{amovid}:{ts}:{channel}
```

* **`amovid`**: Die Adobe Advertising-Besucher-ID, auch als Surfer-ID bezeichnet.
* **`ts`**: Der von Adobe Advertising generierte Zeitstempel.
* **`channel`**: Der für das Klicken oder Belichten verantwortliche Kanaltyp:
   * **`d`**: Ein Klick auf eine DSP-Anzeige (Display-Clickthrough).
   * **`i`**: Eine Impression auf einer DSP-Display-Anzeige (Durchsicht der Anzeige).
   * **`s`**: Ein Klick auf eine Suchanzeige (Such-Clickthrough).

### Beispiele

```text
CjwKCAiAkbbMBhB2EiwANbxtbb9L573Dys0rjTDqcMo3x7tv2yEfh1RGb8exG9N892NoMqAzMBEGmhoCWxwQAvD_BwE:G:s
06207ca63ae6f4fa832197585547393c:20260301111101:i
WcmibgAAAHJK1RyY:1551968087687:d
```
