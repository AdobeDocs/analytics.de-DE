---
title: referrer
description: Überschreiben Sie den automatisch erfassten Referrer für einen Treffer.
feature: Appmeasurement Implementation
exl-id: 09a76de9-0689-424a-aead-3fdff1709fd9
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 80%

---

# referrer

Die `referrer`-Variable überschreibt den automatisch erfassten Referrer in Berichten. Diese Variable ist hilfreich in Situationen, in denen der Referrer verloren gehen könnte, z. B. bei Redirects oder vorübergehender Weiterleitung des Besuchers an einen Zahlungsverarbeiter. Diese Variable hilft beim Ausfüllen der Dimensionen „Referrer“ und „Referrer-Domäne“.

## Referrer unter Verwendung der Web-SDK

Referrer ist den folgenden Variablen zugeordnet:

* [XDM-Objekt](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.web.webReferrer.URL`
* [Datenobjekt](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.referrer`

Die Web-SDK enthält automatisch `web.webReferrer.URL` zu jedem gesendeten Ereignis, sofern verfügbar.

## Referrer, der die Adobe Analytics-Erweiterung verwendet

Sie können „referrer“ entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Legen Sie [!UICONTROL &#x200B; Dropdown]Liste „Erweiterung“ auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen] fest.
6. Suchen Sie den Abschnitt [!UICONTROL Referrer].

Sie können den Referrer auf einen beliebigen Zeichenfolgenwert einstellen, einschließlich Datenelementen.

## s.referrer in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.referrer`-Variable ist eine Zeichenfolge, die die URL der vorherigen Seite enthält. Diese Variable kann maximal 255 Byte speichern. Werte, die länger als 255 Byte sind, werden abgeschnitten. AppMeasurement setzt diese Variable automatisch auf `document.referrer`. Sie müssen diese Variable nur dann festlegen, wenn Sie den automatisch erfassten Wert überschreiben möchten.

```js
s.referrer = "https://example.com";
```

Bei Verwendung der `digitalData` [Datenschicht](../../prepare/data-layer.md):

```js
s.referrer = digitalData.page.pageInfo.referringURL;
```

>[!CAUTION]
>
>Vermeiden Sie es, diese Variable auf Nicht-URL-Werte festzulegen. Entfernen Sie nicht das Protokoll der URL.

## Beispiel

Viele Unternehmen beschäftigen sich mit Implementierungen rund um Redirects. Mit dem Dienstprogramm [`Util.getQueryParam()`](../functions/util-getqueryparam.md) können Sie den Referrer aus der URL abrufen, wenn Ihre Website dies zulässt. Stellen Sie sicher, dass Ihre URL alle Werte codiert, die in der Abfragezeichenfolge enthalten sind.

```js
// Example if the URL is https://example.com?r=https%3A%2F%2Fexample.org
s.referrer = s.Util.getQueryParam("r");
```
