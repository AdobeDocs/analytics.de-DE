---
title: referrer
description: Überschreiben Sie den automatisch erfassten Referrer für einen Treffer.
feature: Appmeasurement Implementation
exl-id: 09a76de9-0689-424a-aead-3fdff1709fd9
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/YsYfgjFNDiJoQbvPU-XoB6bQt2IAriP1qmkOqc2lFDk'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
subfeature_v2:
  - id: c069c44e-5426-4c1a-accc-8028662f2fde
    internal-label: Functions
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
    internal-label: Variables
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
    internal-label: Appmeasurement implementation
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 9a50beeb0aa51cf9f4baf212566947c14029ce8e
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 85%
---
# referrer

Die `referrer`-Variable überschreibt den automatisch erfassten Referrer in Berichten. Diese Variable ist hilfreich in Situationen, in denen der Referrer verloren gehen könnte, z. B. bei Umleitungen oder bei der vorübergehenden Weiterleitung der Besuchenden an einen Zahlungsverarbeiter. Diese Variable hilft beim Ausfüllen der Dimensionen „Referrer“ und „Referrer-Domain“.

## Referrer unter Verwendung der Web-SDK

Referrer ist den folgenden Variablen zugeordnet:

* [XDM-Objekt](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.web.webReferrer.URL`
* [Datenobjekt](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.referrer`

Die Web-SDK enthält automatisch `web.webReferrer.URL` zu jedem gesendeten Ereignis, sofern verfügbar.

## Referrer, der die Adobe Analytics-Erweiterung verwendet

Sie können „Referrer“ entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und legen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen] fest.
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
>Vermeiden Sie, diese Variable auf Nicht-URL-Werte festzulegen. Entfernen Sie nicht das Protokoll der URL.

## Beispiel

Viele Unternehmen beschäftigen sich mit Implementierungen rund um Umleitungen. Mit dem Dienstprogramm [`Util.getQueryParam()`](../functions/util-getqueryparam.md) können Sie den Referrer aus der URL abrufen, wenn Ihre Website dies zulässt. Stellen Sie sicher, dass Sie alle Werte, die in der Abfragezeichenfolge enthalten sind, URL-codieren.

```js
// Example if the URL is https://example.com?r=https%3A%2F%2Fexample.org
s.referrer = s.Util.getQueryParam("r");
```
