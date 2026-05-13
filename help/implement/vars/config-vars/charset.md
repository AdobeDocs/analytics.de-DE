---
title: charSet
description: Die Variable „charSet“ bestimmt, mit welcher Codierung Adobe Ihre Bildanforderung analysiert.
feature: Appmeasurement Implementation
exl-id: 2a2660c6-809d-4b33-a846-01e49dd99c7f
role: Admin, Developer
TQID: https://experienceleague.adobe.com/bPK-uLu-IgKnJWGpAUnS7cmRm808jhetzm-Cyd2R39o
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 235
ht-degree: 66%

---

# charSet

Die `charSet`-Variable wird von Adobe verwendet, um eingehende Daten zur Speicherung und Berichterstellung durch Analytics in UTF-8 zu konvertieren. Die meisten Sites müssen diese Variable nicht festlegen.

Legen Sie diese Variable nur fest, wenn in Berichten unleserliche Werte ([Zeichensalat](https://de.wikipedia.org/wiki/Zeichensalat)) angezeigt werden. Diese Variable kann seitenweise eingestellt werden, wenn Ihre Website auf verschiedenen Seiten unterschiedliche Codierungen verwendet.

## Zeichensatz in Web SDK

Web SDK unterstützt derzeit nur UTF-8 und bietet keine Optionen zum Ändern der Codierung.

## Zeichensatz in der Adobe Analytics-Erweiterung

„Zeichensatz“ ist ein Feld unter dem Akkordeon [!UICONTROL Allgemein] bei der Konfiguration der Adobe Analytics-Erweiterung in der Adobe Experience Platform-Datenerfassung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
1. Erweitern Sie das Akkordeon [!UICONTROL Allgemein], wodurch das Feld [!UICONTROL Zeichensatz] angezeigt wird.

Sie können entweder einen vorab festgelegten oder einen benutzerdefinierten Zeichensatz verwenden. Ändern Sie den Wert nicht von `UTF-8`, es sei denn, Sie sehen beschädigte Werte in Berichten.

## s.charSet in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `charSet`-Variable ist eine Zeichenfolge. Wenn Sie in Adobe Analytics über beschädigte Werte verfügen, setzen Sie diese Variable auf denselben Wert wie das HTML-Tag `<meta charset="">` auf Ihrer Site.

```js
s.charSet = "UTF-8";
```
