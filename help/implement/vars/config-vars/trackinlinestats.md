---
title: trackInlineStats
description: (Eingestellt) Aktivieren oder deaktivieren Sie ClickMap in Ihrer Implementierung.
keywords: ClickMap deaktivieren
feature: Variables
exl-id: a52adc1d-1be7-4002-b393-7ce66332b483
role: Admin, Developer
source-git-commit: 1cdcc748e50c7eeffa98897006154aa0953ce7e3
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 28%

---

# trackInlineStats

>[!IMPORTANT]
>
>Diese Variable wurde eingestellt und wird nicht mehr verwendet.

ClickMap ist eine eingestellte Funktion in Adobe Analytics, mit der Daten darüber erfasst werden, wo Besucherinnen und Besucher klicken und worauf sie klicken. Die Funktion wurde durch [Activity Map](/help/analyze/activity-map/overview.md) ersetzt.

Wenn diese Option aktiviert ist, erfasst AppMeasurement Informationen zum Link und sendet diese Daten in der nächsten Bildanforderung. Die Informationen jedes Klicks werden in einem Cookie mit der Bezeichnung `s_sq` gespeichert.

## Aktivieren von ClickMap mithilfe der Adobe Analytics-Erweiterung

[!UICONTROL ClickMap aktivieren] ist ein Kontrollkästchen unter dem Akkordeon [!UICONTROL Linktracking] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
4. Erweitern Sie das Akkordeon [!UICONTROL Linktracking], wodurch das Kontrollkästchen [!UICONTROL ClickMap aktivieren] angezeigt wird.

>[!NOTE]
>
>Dieses Kontrollkästchen unterscheidet sich vom Kontrollkästchen [!UICONTROL Activity Map verwenden] das sich unter dem Akkordeon [!UICONTROL Bibliotheksverwaltung] befindet.

## s.trackInlineStats in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.trackInlineStats` ist ein boolescher Wert, der das ClickMap-Tracking aktiviert oder deaktiviert. Da die Funktion eingestellt wurde, empfiehlt Adobe nicht, diese Variable festzulegen. Der Standardwert lautet `false`.

```js
s.trackInlineStats = false;
```
