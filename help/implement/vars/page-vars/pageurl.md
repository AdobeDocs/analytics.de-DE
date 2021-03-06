---
title: pageURL
description: Überschreiben Sie die automatisch erfasste Seiten-URL auf Ihrer Website.
feature: Variables
exl-id: 411f894d-c31f-4d07-9568-b0b02786735d
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 78%

---

# pageURL

AppMeasurement erfasst automatisch die Seiten-URL bei jedem Treffer. Wenn Sie die automatisch von AppMeasurement erfasste Seiten-URL überschreiben möchten, können Sie diese Variable verwenden. In den meisten Fällen müssen Sie diese Variable nicht festlegen.

>[!NOTE]
>
>Diese Variable ist keine verfügbare Dimension in Analysis Workspace. Sie ist nur in Data Warehouse und in Daten-Feeds verfügbar. Darüber hinaus entfernen die Datenerfassungs-Server von Adobe diese Dimension aus allen [Linktracking](/help/implement/vars/functions/tl-method.md)-Bildanforderungen. Wenn Sie die Seiten-URL als Dimension in Analysis Workspace verwenden möchten oder diese Dimension bei Linktracking-Treffern verwenden möchten, übergeben Sie bei jedem Treffer die Variable `pageURL` in eine [eVar](evar.md).

## Seiten-URL mit dem Web SDK

Seiten-URL ist [für Adobe Analytics zugeordnet](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) unter dem XDM-Feld `web.webPageDetails.URL`.

## Seiten-URL mit der Adobe Analytics-Erweiterung

Die Analytics-Erweiterung in der Adobe Experience Platform-Datenerfassung füllt die Seiten-URL automatisch. Sie können die Seiten-URL-Überschreibung jedoch entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte **[!UICONTROL Regeln]** und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter **[!UICONTROL Aktionen]** auf eine bestehende Aktion **[!UICONTROL Adobe Analytics – Variablen festlegen]** oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü **[!UICONTROL Erweiterung]** die Option „Adobe Analytics“ aus und setzen Sie den **[!UICONTROL Aktionstyp]** auf **[!UICONTROL Variablen festlegen]**.
6. Suchen Sie den Abschnitt **[!UICONTROL Seiten-URL]**.

Sie können die Seiten-URL auf einen beliebigen Zeichenfolgenwert einstellen.

## s.pageURL in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.pageURL`-Variable ist eine Zeichenfolge, die die URL der Seite enthält. AppMeasurement erfasst diese Variable automatisch. Sie können jedoch ihren Wert bei Bedarf überschreiben.

```js
s.pageURL = "https://example.com";
```

Wenn Sie die Seiten-URL als Dimension in Berichten verwenden möchten, sollten Sie Folgendes in Ihrer Implementierung berücksichtigen:

```js
// Set eVar1 to page URL without protocol or query strings
s.eVar1 = window.location.hostname + window.location.pathname;
```

Bei Verwendung der `digitalData` [Datenschicht](../../prepare/data-layer.md):

```js
s.pageURL = digitalData.page.pageInfo.destinationURL;
```
