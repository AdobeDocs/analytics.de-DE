---
title: Fehlerbehebung bei H-Code-Implementierungen
description: Erfahren Sie mehr über einige häufige Probleme bei älteren JavaScript-Implementierungen.
feature: Implementation Basics
exl-id: 51d6e286-7008-4736-a196-bd8ac4e3e9cb
role: Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '245'
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
