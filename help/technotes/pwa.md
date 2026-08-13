---
title: PWAs für Analytics
description: Progressive Web-Apps für Adobe Analytics
role: User, Admin
feature: Progressive Web Apps
exl-id: f28e0bfc-0e3e-4f28-9533-6788a36d37fe
TQID: https://experienceleague.adobe.com/IKf2D1AqfbD6qurNczyJWaZIOzQyOTURfJFSJNDucnU
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 279
ht-degree: 100%

---

# PWAs für Adobe Analytics

Auf dieser Seite wird die Verwendung von Adobe Analytics mit progressiven Web-Apps (PWAs) beschrieben.

## Einführung

PWAs können eine native App-Erfahrung sowie Offline-Funktionen für eine Website bereitstellen. Normalerweise umfassen PWAs einen Service Worker, Lösungen zum Zwischenspeichern und eine Manifestdatei. Dies alles kann zu schnelleren Ladezeiten, einfacherer Navigation und responsiverem Verhalten beitragen.

Adobe Analytics funktioniert genauso nahtlos mit PWAs wie mit herkömmlichen Websites. Obwohl PWAs einige zusätzliche Anforderungen haben, um sich progressiv zu verhalten, sind sie im Hinblick auf die Datenerfassung und Berichterstellung durch Adobe Analytics mit den gleichen Hindernissen oder Einschränkungen wie herkömmliche Websites verbunden. Da Analytics bereits Offline-Tracking-Funktionen enthält, können Sie mit PWAs diese integrierte Funktion einfacher als mit herkömmlichen Websites nutzen.

## PWA-Analytics-Daten abrufen

Zur Erfassung und Analyse Ihrer PWA-Daten mit [!UICONTROL Analytics] müssen Sie keine Konfigurationsänderungen vornehmen. [!UICONTROL Analytics] bietet automatisch die gleichen Funktionen und Merkmale wie bei einer herkömmlichen Website.

## Offline-Tracking zur Erhöhung der PWA-Effektivität hinzufügen

Sie können die Effektivität Ihrer PWA steigern, indem Sie die Adobe Analytics-Funktionen für [Offline-Tracking](/help/implement/vars/config-vars/trackoffline.md) verwenden. Standardmäßig ist diese Funktion deaktiviert. Sie können der Datei AppMeasurement.js jedoch die folgende Eigenschaft hinzufügen, um sie zu aktivieren: `s.trackOffline=true;`.

In der folgenden Datei AppMeasurement.js wurde die Eigenschaft beispielsweise am Ende des Abschnitts `CONFIG SECTION` hinzugefügt:

```
/************************** CONFIG SECTION **************************/ 
/* You may add or alter any code config here. */ 
/* Link Tracking Config */ 
s.trackDownloadLinks=true 
s.trackExternalLinks=true 
s.trackInlineStats=true 
s.linkDownloadFileTypes="exe,zip,wav,mp3,mov,mpg,avi,wmv,pdf,doc,docx,xls,xlsx,ppt,pptx" 
s.linkInternalFilters="javascript:" //optional: add your internal domain here 
s.linkLeaveQueryString=false 
s.linkTrackVars="None" 
s.linkTrackEvents="None" 
s.trackOffline=true
*** 
```

Weitere Informationen zum Konfigurieren der Datei AppMeasurement.js finden Sie unter [Übersicht über Konfigurationsvariablen](/help/implement/vars/config-vars/configuration-variables.md) und auf den einzelnen variablenspezifischen Seiten im selben Unterkapitel.

Weitere Informationen zu den Eigenschaften der Datei AppMeasurement.js finden Sie unter [Übersicht über die JavaScript-Implementierung](/help/implement/js/overview.md).
