---
title: zip
description: Füllen Sie die Dimension „Postleitzahl“ manuell, wenn die Report Suite-Einstellungen dies zulassen.
feature: Appmeasurement Implementation
exl-id: 1acf4bf7-3788-46bd-bcdb-9885c7b93b59
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/dv564yEz9tChaxot0w65ZGIc1T0Jqdnp1Mua0QUbn5Y'
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
source-wordcount: 275
ht-degree: 81%

---

# zip

Mit der `zip`-Variablen können Sie die Dimension „Postleitzahl“ manuell füllen, wenn die [!UICONTROL Zip-Option] in den Report Suite-Einstellungen dies zulässt. In früheren Versionen von Adobe Analytics konnte diese Variable nur manuell eingestellt werden, üblicherweise bei Eingabe von Versandinformationen auf einer Retail-Website. Dank der Verbesserungen an Adobe Analytics kann diese Variable mithilfe von Standortdaten automatisch eingestellt werden. Diese Variable bleibt nicht über den Treffer hinaus bestehen, in dem sie gesetzt wurde.

>[!IMPORTANT]
>
>Stellen Sie sicher, dass die [!UICONTROL Postleitzahlenoption] in den Report Suite-Einstellungen auf den gewünschten Wert eingestellt ist. Sie können diese Variable nicht verwenden, wenn [!UICONTROL Geo zip] immer verwendet wird. Weitere Informationen finden Sie im Admin-Benutzerhandbuch unter [Allgemeine Kontoeinstellungen](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md).

## Postleitzahl, die die Web-SDK verwendet

Die Postleitzahl ist den folgenden Variablen zugeordnet:

* [XDM-Objekt](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.placeContext.geo.postalCode`
* [Datenobjekt](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.zip`

## Postleitzahl, die die Adobe Analytics-Erweiterung verwendet

Sie können die Postleitzahl entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und legen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen] fest.
6. Suchen Sie den Abschnitt [!UICONTROL Postleitzahl].

Sie können die Postleitzahl auf einen beliebigen Zeichenfolgenwert einstellen, einschließlich Datenelementen.

## s.zip in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.zip`-Variable ist eine Zeichenfolge, die normalerweise eine Postleitzahl enthält, jedoch einen beliebigen Wert mit einer Länge von bis zu 50 Byte enthalten kann.

```js
s.zip = "84043";
```
