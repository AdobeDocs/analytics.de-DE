---
title: transactionID
description: Verwenden Sie diese Variable, um Online- und Offline-Daten miteinander zu verknüpfen.
feature: Appmeasurement Implementation
exl-id: 525e90d8-99a7-4f4f-9bce-1395bf72fd8f
role: Admin, Developer
source-git-commit: fc52bfaa13f7fc93ef53aa49746d432676b3d55f
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 75%

---

# transactionID

Die Variable `transactionID` identifiziert eine Transaktion eindeutig, sodass der Treffer Dimensionswerte für Daten bereitstellen kann, die über [Transaktions-ID-Datenquellen“ hochgeladen ](/help/import/data-sources/transactionid.md). Diese Variable ist nützlich, wenn Sie Offline-Kanaldaten mit Werten ausfüllen möchten, die aus Online-Kanaldaten erfasst wurden.

>[!NOTE]
>
>Stellen Sie sicher, dass der [!UICONTROL Transaktions-ID-Speicher] in einer Report Suite aktiviert ist, bevor Sie diese Variable verwenden. Weitere Informationen finden Sie im Admin-Benutzerhandbuch unter [Allgemeine Kontoeinstellungen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md).

Wenn Sie `transactionID` für einen Treffer festlegen, erstellt Adobe einen „Schnappschuss“ aller zu diesem Zeitpunkt festgelegten oder beibehaltenen Analytics-Variablen. Siehe [Transaktions-ID-Datenquellen](/help/import/data-sources/transactionid.md) für die Liste der im Snapshot enthaltenen Dimensionen. Adobe speichert alle Transaktions-ID-Werte (verknüpft und nicht verknüpft) für bis zu 25 Monate.

## Transaktions-ID unter Verwendung des Web SDK

Die Transaktions-ID ist den folgenden Variablen zugeordnet:

* [XDM-Objekt](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.commerce.order.payments[3].transactionID` oder `xdm.commerce.order.payments.transactionID`
* [Datenobjekt](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.transactionID` oder `data.__adobe.analytics.xact`

## Transaktions-ID unter Verwendung der Adobe Analytics-Erweiterung

Sie können die Transaktions-ID entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Legen Sie [!UICONTROL  Dropdown]Liste „Erweiterung“ auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen] fest.
6. Suchen Sie den Abschnitt [!UICONTROL Transaktions-ID].

Sie können die Transaktions-ID auf einen beliebigen Zeichenfolgenwert einstellen, einschließlich Datenelementen.

## s.transactionID in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.transactionID`-Variable ist eine Zeichenfolge, die eine eindeutige Kennung für eine Transaktion enthält. Gültige Werte sind alphanumerische Zeichen bis zu 100 Byte. Der Standardwert ist eine leere Zeichenfolge.

```js
s.transactionID = "ABC123";
```

Wenn Sie mehr als eine Transaktions-ID für einen Treffer haben, können Sie diese mit einem Komma trennen. Für mehrere Transaktions-IDs gilt weiterhin die 100-Byte-Grenze.

```js
s.transactionID = "ABC123,XYZ456";
```

>[!TIP]
>
>Wenn Sie mit dieser Variablen mehrere Offline-Kanäle integrieren, stellen Sie sicher, dass sich die Transaktions-IDs nicht in verschiedenen Kanälen überschneiden. Wenn Sie beispielsweise eine Call-Center-Transaktions-ID mit dem Wert `1234` und eine Verkaufs-Lead-Transaktions-ID mit dem Wert `1234` haben, können sie miteinander in Konflikt geraten und unerwartete Ergebnisse verursachen. Stellen Sie sicher, dass Transaktions-IDs eindeutige Formate pro Offline-Kanal enthalten, und unterscheiden Sie diese bei Bedarf. Setzen Sie z. B. Ihre Call-Center-Transaktions-ID `call_1234` und Ihre Verkaufs-Lead-Transaktions-ID `lead_1234` sowohl in Data Sources als auch in AppMeasurement.
