---
title: Fehlerbehebung bei H-Code-Implementierungen
description: Erfahren Sie mehr über einige häufige Probleme bei älteren JavaScript-Implementierungen.
feature: Implementation Basics
exl-id: 51d6e286-7008-4736-a196-bd8ac4e3e9cb
role: Developer
TQID: https://experienceleague.adobe.com/DootwtTj5kDIRHKhFPeY3Fnt3bWdVLsXc6J3UEc5LPI
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: df312454-73c4-43f6-a90e-18f5043f074c
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 246
ht-degree: 100%

---

# Fehlerbehebung bei H-Code-Implementierungen

Im Folgenden finden Sie Schritte zur Fehlerbehebung bei H-Code-Implementierungen.

## Analytics-Code im Head-Tag platzieren

>[!NOTE]
>
>Während bei H-Code-Implementierungen der Code im `<body>`-Tag referenziert werden muss, ist bei anderen Implementierungen (z. B. bei Verwendung von Tags in Adobe Experience Platform) der Code im `<head>`-Tag zu referenzieren.

Analytics-Code erstellt ein unsichtbares 1x1-Pixelbild. Früher war es gängige Praxis, den `s_code.js`-Verweis im `<head>`-Tag zu platzieren. Die Platzierung des Codes hier verhinderte, dass das Bild das Seitenlayout in irgendeiner Weise beeinflusst. Er wurde auch früher ausgeführt, sodass Seitenansichten auch bei partiell geladenen Seiten effizienter gezählt werden können.

Allerdings setzen bestimmte Elemente des Codes voraus, dass ein `<body>`-Objekt vorhanden ist. Wenn sich der Analytics-JavaScript-Code im `<head>`-Tag befindet, wird er ausgeführt, bevor das `<body>`-Objekt vorhanden ist. Infolgedessen sammelt Ihre Implementierung keine [!UICONTROL ClickMap]-Daten, kein automatisches Tracking von Datei-Downloads oder Exitlinks und keine Daten zum Verbindungstyp. Die Platzierung der Skript-Referenz auf `s_code.js` im `<head>`-Tag funktioniert, aber das Ergebnis ist eine sehr begrenzte Version von Analytics.

Der Analytics-Code kann an einer beliebigen Stelle innerhalb der `<body>`-Tags einer korrekt formatierten HTML-Seite untergebracht werden. Adobe empfiehlt, Analytics-Code so nah wie möglich am Anfang des `<body>`-Tags zu platzieren. Stellen Sie sicher, dass alle Seitenvariablen festgelegt werden, nachdem die `s_code.js`-Datei geladen wurde.

>[!TIP]
>
>Wenn Sie Adobe Analytics mit Adobe Target integrieren möchten, muss die JavaScript-Include-Datei am Ende der Seite platziert werden.
