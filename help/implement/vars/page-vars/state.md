---
title: state
description: (Eingestellt) Der Bericht „Bundesstaat des Besuchers“ wurde ausgefüllt, der nicht mehr verfügbar ist.
feature: Appmeasurement Implementation
exl-id: a6e3f30b-b5d1-48f8-8961-8e9c6d4d29da
role: Admin, Developer
TQID: https://experienceleague.adobe.com/3GhnJJj6gxEt0Qiefd4siS6-YzDbOw4hdY4IsNhwYDU
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2:
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 230
ht-degree: 87%

---

# state

>[!IMPORTANT]
>
>Diese Variable wurde eingestellt und ist keine verfügbare Dimension in Analysis Workspace. Verwenden Sie stattdessen [&#x200B; Dimension &#x200B;](/help/components/dimensions/us-states.md)US-Bundesstaaten“, die AppMeasurement basierend auf dem Standort des Besuchers automatisch erfasst.

In früheren Versionen von Adobe Analytics wurde die `state`-Variable verwendet, wenn Besucher Versandinformationen auf Retail-Websites ausfüllten. Sie ist funktionell mit einer Prop identisch, aber nicht in Analysis Workspace verfügbar.

## Status bei Verwendung der Adobe Analytics-Erweiterung

Sie können den Status entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und legen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen] fest.
6. Suchen Sie den Abschnitt [!UICONTROL Bundesstaat].

Sie können „state“ auf einen beliebigen Zeichenfolgenwert oder ein beliebiges Datenelement einstellen.

## s.state in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.state`-Variable ist eine Zeichenfolge, die normalerweise das Bundesland oder den Bundesstaat des Besuchers enthält. Vollständige Namen oder Zweibuchstaben-Codes der Bundesstaaten sind gültig. Sie hat einen Maximalwert von 50 Byte. Längere Werte werden abgeschnitten. Der Standardwert ist eine leere Zeichenfolge.

```js
s.state = "Utah";
```
