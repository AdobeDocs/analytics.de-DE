---
title: pageName
description: Der Name der Seite auf Ihrer Website.
feature: Appmeasurement Implementation
exl-id: 24ac40a9-f0e7-4534-abf2-2397f5fe16c2
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/UVcun7asSJzB20Q4TD5EAqt1-M1OY4VUhH--rEJRdc4'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 262
ht-degree: 86%

---

# pageName

Die `pageName`-Variable speichert normalerweise den Namen einer bestimmten Seite. Es ist hilfreich, zu bestimmen, welche einzelnen Seiten am beliebtesten sind. Diese Variable befüllt die Dimension [Seite](/help/components/dimensions/page.md).

Wenn diese Variable bei einem gegebenen Seiten-Tracking-Aufruf nicht definiert ist, wird stattdessen die [`pageURL`](pageurl.md)-Variable verwendet.

>[!NOTE]
>
>Datenerfassungs-Server von Adobe entfernen diese Dimension aus allen [Linktracking](/help/implement/vars/functions/tl-method.md)-Bildanforderungen. Wenn diese Dimension bei Linktracking-Treffern angezeigt werden soll, kopieren Sie sie in eine [eVar](evar.md).

## Seitenname bei Verwendung der Web-SDK

Der Seitenname wird den folgenden Variablen zugeordnet:

* [XDM-Objekt](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.web.webPageDetails.name`
* [Datenobjekt](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.pageName`

## Seitenname bei Verwendung der Adobe Analytics-Erweiterung

Sie können den Seitennamen entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und legen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen] fest.
6. Suchen Sie den Abschnitt [!UICONTROL Seitenname].

Sie können den Seitennamen auf einen beliebigen Zeichenfolgenwert einstellen, einschließlich Datenelementen.

## s.pageName in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.pageName`-Variable ist eine Zeichenfolge, die normalerweise den Namen der Seite enthält. Sie hat einen Maximalwert von 100 Byte. Längere Werte werden abgeschnitten. Diese Kürzung umfasst Fälle, in denen auf `pageURL` zurückgegriffen wird, wenn diese Variable leer ist.

```js
// Set page name to a static value
s.pageName = "Example page name";

// Set page name to the page's title
s.pageName = window.document.title;
```

Bei Verwendung der `digitalData` [Datenschicht](../../prepare/data-layer.md):

```js
s.pageName = digitalData.page.pageInfo.pageName;
```
