---
title: PWAs für Analytics
description: Progressive Web-Apps für Adobe Analytics
role: User, Admin
feature: Progressive Web Apps
exl-id: f28e0bfc-0e3e-4f28-9533-6788a36d37fe
TQID: 'https://experienceleague.adobe.com/IKf2D1AqfbD6qurNczyJWaZIOzQyOTURfJFSJNDucnU'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
    internal-label: Data configuration and collection
subfeature_v2:
  - id: b9fe5dd8-e052-4fb5-86db-a5f6ced5bbb8
    internal-label: Progressive web apps
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
source-git-commit: 9a50beeb0aa51cf9f4baf212566947c14029ce8e
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 100%
---
# PWAs für Adobe Analytics

Auf dieser Seite wird die Verwendung von Adobe Analytics mit progressiven Web-Apps (PWAs) beschrieben.

## Einführung

PWAs können eine native App-Erfahrung sowie Offline-Funktionen für eine Website bereitstellen. Normalerweise umfassen PWAs einen Service Worker, Caching-Lösungen und eine Manifestdatei. Dies alles kann zu schnelleren Ladezeiten, einfacherer Navigation und responsivem Verhalten beitragen.

Adobe Analytics funktioniert genauso nahtlos mit PWAs wie mit herkömmlichen Websites. Obwohl PWAs einige zusätzliche Anforderungen haben, um sich progressiv zu verhalten, schaffen sie keine Hindernisse oder Einschränkungen dafür, wie Analytics Daten von ihnen erfasst oder darüber berichtet – im Vergleich zu herkömmlichen Websites gibt es hier keine Unterschiede. Da Analytics bereits Offline-Tracking-Funktionen enthält, können Sie mit PWAs diese integrierte Funktion einfacher als mit herkömmlichen Websites nutzen.

## PWA-Analytics-Daten abrufen

Zur Erfassung und Analyse Ihrer PWA-Daten mit [!UICONTROL Analytics] müssen Sie keine Konfigurationsänderungen vornehmen. [!UICONTROL Analytics] bietet automatisch die gleichen Funktionen und Merkmale wie bei einer herkömmlichen Website.

## Hinzufügen von Offline-Tracking zum Erhöhen der PWA-Effektivität

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
