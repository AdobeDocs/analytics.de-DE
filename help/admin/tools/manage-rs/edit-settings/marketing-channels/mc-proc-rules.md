---
title: Verarbeitungsregeln für Marketing-Kanäle
description: Verwenden Sie Regeln, um zu bestimmen, zu welchem Marketing-Kanal ein Treffer gehört.
feature: Marketing Channels
exl-id: 825f70a5-cce3-4b1c-bb42-828388348216
role: Admin
source-git-commit: e934de3938f013067d6bbd6b516b0444b0c9f782
workflow-type: tm+mt
source-wordcount: '819'
ht-degree: 3%

---

# Verarbeitungsregeln für Marketing-Kanäle

_Diese Seite bezieht sich auf Verarbeitungsregeln, die einem Treffer einen Marketing-Kanal zuweisen. Siehe [Verarbeitungsregeln](../general/processing-rules/pr-overview.md) für die Funktion, mit der Sie anpassen können, wie Daten erfasst werden._

Mit Marketing-Kanal-Verarbeitungsregeln können Sie eine Logik erstellen, die den Wert für die Dimensionen [Marketing](/help/components/dimensions/marketing-channel.md) und [Marketing-Kanal-Detail](/help/components/dimensions/marketing-detail.md) bestimmt. Verwenden Sie den [Marketing-Kanal-](c-channels.md)), um zu bestimmen, welche Marketing-Kanäle Sie verwenden, und verwenden Sie dann Verarbeitungsregeln, um zu bestimmen, wie die einzelnen Kanäle festgelegt werden.

![Marketing-Kanal-Buckets](assets/buckets_2.png)

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Marketing-Kanäle]** > **[!UICONTROL Marketing-Kanal-Verarbeitungsregeln]**

Sobald die [Automatische Einrichtung](/help/components/c-marketing-channels/c-getting-started-mchannel.md) ausgeführt wird, wird für jeden beim Setup generierten Kanal eine Regel erstellt.

![Standardregeln](assets/marketing_channel_rules.png)

Sie können mehrere Regeln verwenden, um einen einzelnen Marketing-Kanal zu definieren. Die Verwendung mehrerer Regeln für einen einzelnen Kanal kann vorteilhaft sein, wenn Sie die Kanaldetails je nach Regelbedingungen unterschiedlich festlegen möchten. Sie können auch mehrere Bedingungen verwenden, um eine einzelne Regel zu definieren.

## Regeldefinitionen

Jede Regel enthält eine Bedingung und eine Zuweisung:

* **[!UICONTROL Wenn Folgendes zutrifft:]** Sie einer einzelnen Regel mehrere Bedingungen hinzufügen, können Sie bestimmen, ob alle Bedingungen erfüllt sein müssen oder eine der Bedingungen erfüllt sein muss, um den Kanal und den zugehörigen Wert festzulegen.
* **Regelbedingungen**: Geben Sie eine oder mehrere Regelbedingungen an, die erfüllt werden müssen. Normalerweise geben Sie eine Dimension an, mit der ein Treffer übereinstimmen muss, damit er für den Marketing-Kanal qualifiziert werden kann.
* **[!UICONTROL Gehen Sie dann wie folgt vor]**: Wenn die Regelbedingungen übereinstimmen, setzen Sie [Marketing-Kanal](/help/components/dimensions/marketing-channel.md) ([!UICONTROL Identifizieren Sie den Kanal als]) und [Marketing-Kanal-Detail](/help/components/dimensions/marketing-detail.md) ([!UICONTROL Legen Sie den Kanalwert ]).

## Regelbedingungen

Beim Festlegen von Regelbedingungen sind die folgenden Optionen verfügbar.

>[!NOTE]
>
>Bei der Auswertung aller Textfelder wird nicht zwischen **Groß- und Kleinschreibung**. Wenn Sie beispielsweise eine Regelbedingung verwenden, bei der der Abfragezeichenfolgenparameter `cmp` gleich `abc123` ist, können sowohl der Abfragezeichenfolgenparameter als auch der Wert eine beliebige Kombination aus Groß- und Kleinschreibung verwenden.

**Von Adobe erkannte Bedingungen** enthalten keine Optionen oder Felder zur Texteingabe.

| Adobe-erfasste Bedingung | Beschreibung |
|---|---|
| **[!UICONTROL Entspricht den Erkennungsregeln für Paid Search]** | Der Treffer stammt von einer anerkannten Suchmaschine und entsprach [Regeln zur Erkennung gebührenpflichtiger Suchvorgänge](../general/paid-search-detection/paid-search-detection.md). |
| **[!UICONTROL Entspricht den Regeln der natürlichen Sucherkennung]** | Der Treffer stammt von einer anerkannten Suchmaschine und entsprach nicht den Erkennungsregeln für Paid Search. |
| **[!UICONTROL Referrer stimmt mit internen URL-Filtern überein]** | Der Treffer enthielt einen [Referrer](/help/components/dimensions/referrer.md) der mit [internen URL-Filtern](../general/internal-url-filter-admin.md) übereinstimmte. |
| **[!UICONTROL Referrer stimmt nicht mit internen URL-Filtern überein]** | Der Treffer enthielt einen Referrer, der nicht mit den internen URL-Filtern übereinstimmte. |
| **[!UICONTROL Ist Erster Treffer des Besuchs]** | Der Treffer war der erste in einem Besuch. |
| **[!UICONTROL Referrer ist ein soziales Netzwerk]** | Der [Referrer-Typ](/help/components/dimensions/referrer-type.md) ist „Social Networks“. |
| **[!UICONTROL Referrer ist kein soziales Netzwerk]** | Der Referrer-Typ ist nicht „Social Networks“. |
| **[!UICONTROL Referrer ist Conversational AI]** | Der Referrer-Typ ist „Conversational AI“. |
| **[!UICONTROL Referrer ist keine Konversations-KI]** | Der Referrer-Typ ist nicht „Conversational AI“. |

**Trefferattribute** ermöglichen es Ihnen, eine Dimension, einen übereinstimmenden Operator und einen zu suchenden Wert anzugeben.

| Trefferattributbedingung | Beschreibung |
|---|---|
| **[!UICONTROL Seite]** | Die Dimension [Seite](/help/components/dimensions/page.md). |
| **[!UICONTROL Seiten-Domain]** | Die Domain der URL. Zum Beispiel `products.example.com`. |
| **[!UICONTROL Seiten-Domain und -Pfad]** | Domain und Pfad der URL. Zum Beispiel `products.example.com/mens/pants/overview.html`. |
| **[!UICONTROL Seitenstamm-Domain]** | Die Stamm-Domain der URL. Zum Beispiel `example.co.uk`. |
| **[!UICONTROL Seiten-URL]** | Die vollständige Seiten-URL. |
| **[!UICONTROL Abfragezeichenfolgen-Parameter]** | Ein einzelner Abfragezeichenfolgenparameter in der Seiten-URL. Verwenden Sie für jede Regelbedingung einen Abfragezeichenfolgenparameter. Wenn Sie mehrere Abfragezeichenfolgenparameter in eine Regel einbeziehen möchten, verwenden Sie mehrere Regelbedingungen. |
| **[!UICONTROL Referrer]** | Die Dimension [Referrer](/help/components/dimensions/referrer.md). |
| **[!UICONTROL Verweisende Domain]** | Die Dimension [Verweisende Domain](/help/components/dimensions/referring-domain.md) . |
| **[!UICONTROL Verweisende Domain und Pfad]** | Eine Verkettung aus verweisender Domain und URL-Pfad des Referrers. Beispiel: `www.example.com/products/id/12345` oder `ad.example.com/foo`. |
| **[!UICONTROL Verweisender Parameter]** | Ein Abfragezeichenfolgenparameter im Referrer. |
| **[!UICONTROL Verweisende Stammdomäne]** | Die verweisende Stamm-Domain. |
| **[!UICONTROL Suchmaschine]** | Die Dimension [Suchmaschine](/help/components/dimensions/search-engine.md) . |
| **[!UICONTROL Suchbegriff(e)]** | Die Dimension [Suchbegriff](/help/components/dimensions/search-keyword.md) . |
| **[!UICONTROL Suchmaschine + Suchbegriff(e)]** | Eine Verkettung aus Suchmaschine und Suchbegriff. |
| **[!UICONTROL AMO-ID]** | Der von den Adobe Advertising- und Advertising Analytics-Integrationen verwendete primäre Trackingcode. Wenn eine dieser Integrationen aktiviert ist, kann das Trackingcode-Präfix verwendet werden, um Advertising-spezifische Kanäle zu identifizieren. Werte, die mit „AL“ beginnen, sind für Suche und Social. Werte, die mit „AC“ beginnen, sind für die Anzeige vorgesehen. Wenn die AMO-ID in Marketing-Kanälen verwendet wird, können Klick-/Kosten-/Impressionsmetriken dem richtigen Kanal zugeordnet werden. |
| **[!UICONTROL AMO EF ID]** | Der von Adobe Advertising verwendete sekundäre Trackingcode. Dient als Schlüssel zum Zurücksenden von Daten an Advertising. Er kann verwendet werden, um Display-Clickthroughs und Display-Viewthroughs als zwei separate Marketing-Kanäle zu identifizieren. Legen Sie dazu fest, dass die Marketing-Kanal-Logik für „AMO EF ID“ mit `:d` für Display-Clickthroughs endet, oder „AMO EF ID“ mit `:i` für Display-View-Throughs. Wenn die Anzeige nicht in zwei Kanäle aufgeteilt werden soll, verwenden Sie stattdessen die AMO ID-Dimension. |

**Konversionsvariablen** ermöglichen es Ihnen, eine benutzerdefinierte eVar, einen übereinstimmenden Operator und einen zu suchenden Wert anzugeben.

| Bedingung der Konversionsvariablen | Beschreibung |
|---|---|
| **eVar 1-250** | Die zugehörige Dimension [eVar](/help/components/dimensions/evar.md). |
