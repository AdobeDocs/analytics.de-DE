---
title: trackInlineStats
description: (Eingestellt) Aktivieren oder deaktivieren Sie ClickMap in Ihrer Implementierung.
keywords: ClickMap deaktivieren
feature: Appmeasurement Implementation
exl-id: a52adc1d-1be7-4002-b393-7ce66332b483
role: Admin, Developer
TQID: https://experienceleague.adobe.com/K6rwl-ZECfoMLfC0Z25PPq2jV1FBo0cTsl1YfDeNpBQ
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 194
ht-degree: 29%

---

# trackInlineStats

>[!IMPORTANT]
>
>Diese Variable wurde eingestellt und wird nicht mehr verwendet.

ClickMap ist eine eingestellte Funktion in Adobe Analytics, mit der Daten darüber erfasst werden, wo Besucherinnen und Besucher klicken und worauf sie klicken. Die Funktion wurde durch [Activity Map ersetzt](/help/analyze/activity-map/overview.md).

Wenn diese Option aktiviert ist, erfasst AppMeasurement Informationen zum Link und sendet diese Daten in der nächsten Bildanforderung. Die Informationen jedes Klicks werden in einem Cookie mit der Bezeichnung `s_sq` gespeichert.

## Aktivieren von ClickMap mithilfe der Adobe Analytics-Erweiterung

[!UICONTROL ClickMap aktivieren] ist ein Kontrollkästchen unter dem Akkordeon [!UICONTROL Linktracking] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
4. Erweitern Sie das Akkordeon [!UICONTROL Linktracking], wodurch das Kontrollkästchen [!UICONTROL ClickMap aktivieren] angezeigt wird.

>[!NOTE]
>
>Dieses Kontrollkästchen unterscheidet sich vom [!UICONTROL Activity Map verwenden] Kontrollkästchen unter dem Akkordeon [!UICONTROL Bibliotheksverwaltung].

## s.trackInlineStats in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.trackInlineStats` ist ein boolescher Wert, der das ClickMap-Tracking aktiviert oder deaktiviert. Da die Funktion eingestellt wurde, empfiehlt Adobe nicht, diese Variable festzulegen. Der Standardwert lautet `false`.

```js
s.trackInlineStats = false;
```
