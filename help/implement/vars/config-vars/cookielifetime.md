---
title: cookieLifetime
description: Überschreiben Sie die Gültigkeit für von AppMeasurement erstellte Cookies.
feature: Variables
exl-id: 2cd64301-9f12-4e77-abae-af431e4b499d
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 80%

---

# cookieLifetime

Von AppMeasurement gesetzte Cookies haben in der Regel eine Gültigkeit von 2 Jahren. Verwenden Sie die `cookieLifetime`-Variable, um das Ablaufdatum für Cookies zu überschreiben, die von AppMeasurement gesetzt werden.

>[!NOTE]
>
>Diese Variable wirkt sich auf die Zählung und Attribution von Unique Visitors aus. Gehen Sie beim Festlegen dieser Variablen mit Bedacht vor.

## Cookie-Lebensdauer mit dem Web SDK

Das Web SDK bietet noch keine Anpassung an die Lebensdauer der von ihm festgelegten Cookies.

## Cookie-Lebensdauer mit der Adobe Analytics-Erweiterung

„Cookie-Lebensdauer“ ist ein Dropdown-Menü unter dem Akkordeon [!UICONTROL Cookies] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
1. Erweitern Sie das Akkordeon [!UICONTROL Cookies], wodurch das Dropdown-Menü [!UICONTROL Cookie-Lebensdauer] angezeigt wird.

Dieses Dropdown-Menü enthält die folgenden Werte:

* **Standardmäßig**: Cookie läuft nach 2 Jahren ab.
* **Keine**: AppMeasurement setzt keine Cookies.
* **Sitzung**: Cookie läuft am Ende der Sitzung des Besuchers ab.
* **Sekunden**: Cookie läuft nach der angegebenen Anzahl von Sekunden ab. Wenn Sie dieses Dropdown-Menü beispielsweise auf [!UICONTROL Sekunden] festlegen und `86400` in das benutzerdefinierte Feld platzieren, laufen Cookies nach genau 24 Stunden ab.

## s.cookieLifetime in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.cookieLifetime`-Variable ist eine Zeichenfolge, die das Ablaufdatum der von AppMeasurement gesetzten Cookies festlegt.

* Wenn auf `SESSION` gesetzt, laufen von AppMeasurement gesetzte Cookies nach Abschluss der Browser-Sitzung ab.
* Wenn auf `NONE` gesetzt, versucht AppMeasurement nicht, Cookies zu setzen.
* Wenn auf eine ganzzahlige Zeichenfolge gesetzt, laufen die von AppMeasurement gesetzten Cookies nach Ablauf der angegebenen Anzahl von Sekunden ab.

```js
// Expire cookies after each session
s.cookieLifetime = "SESSION";

// Expire cookies after exactly 24 hours
s.cookieLifetime = "86400";
```
