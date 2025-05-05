---
title: Fehlerbehebung bei der Activity Map-Datenerfassung
description: Ermitteln Sie, warum Sie keine Activity Map-Daten in Bildanforderungen sehen können.
feature: Activity Map
role: User, Admin
exl-id: 7f9e06ba-4040-483b-b18b-cdfe85bca486
source-git-commit: 72b38970e573b928e4dc4a8c8efdbfb753be0f4e
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 15%

---

# Fehlerbehebung bei der Activity Map-Datenerfassung

Wenn keine Daten für Activity Map-Dimensionen angezeigt werden, können Sie auf dieser Seite ermitteln, warum.

## Bestätigen der Datenerfassung mit dem Debugger

Stellen Sie zunächst sicher, dass AppMeasurement die Activity Map-Daten korrekt erfasst.

1. Herunterladen und Installieren der [Adobe Experience Cloud Debugger Chrome-Erweiterung](https://experienceleague.adobe.com/de/docs/experience-platform/debugger/home).
2. Navigieren Sie zu Ihrer Web-Seite und klicken Sie auf einen Link.
3. Öffnen Sie den Debugger, wenn die nachfolgende Seite geladen wird. Überprüfen Sie, ob Sie Activity Map-Kontextdatenvariablen sehen, die zwischen `activitymap.` und `.activitymap` eingeschlossen sind:

## Mögliche Gründe, warum keine Activity Map-Daten vorhanden sind

Überprüfen Sie die folgenden Komponenten, um sicherzustellen, dass Activity Map-Komponenten vorhanden sind:

* **AppMeasurement-Version**: Activity Map wird ab Version 1.6 unterstützt. Viele Probleme mit Edge-Fällen werden behoben, wenn Sie auf die neueste stabile Version von AppMeasurement aktualisieren.
* **Activity Map-Modul**: Überprüfen Sie, ob das `AppMeasurement_Module_Activity_Map` in Ihrer `AppMeasurement.js` vorhanden ist. Wenn Ihre Implementierung Adobe Experience Platform zur Datenerfassung verwendet, stellen Sie sicher, dass **[!UICONTROL ClickMap aktivieren]** beim Konfigurieren der Analytics-Erweiterung unter &quot;**[!UICONTROL -Tracking“]** ist.
* **Das `s_sq`-**: Activity Map hängt vom `s_sq`-Cookie für die Datenerfassung ab.
   * Stellen Sie sicher, dass die `cookieDomainPeriods`-Variable korrekt festgelegt ist, insbesondere für regionale Domains wie `*.co.uk` oder `*.co.jp`.
   * Stellen Sie sicher, dass die `linkInternalFilters` auf die gewünschten Werte eingestellt ist. Wenn ein angeklickter Link nicht mit internen Filtern übereinstimmt, betrachtet Activity Map ihn als Exitlink und erfasst keine Daten.
* **Activity Map-Überlagerung läuft**: AppMeasurement verfolgt keine Klickdaten für Ihre Web-Seite, wenn die Activity Map-Überlagerung aktiviert ist.

Führt die Browserparameter auf, die nicht mit der Verwendung von Activity Map kompatibel sind. Adobe empfiehlt, diese Einstellungen zu deaktivieren.

## Chrome

![](assets/Chrome1.png)

![](assets/Chrome2.png)

![](assets/Chrome3.png)

## Firefox

![](assets/Firefox.png)

## Safari

![](assets/Safari1.png)

![](assets/Safari2.png)

## Internet Explorer

![](assets/IE1.png)


**Validierung**

Interaktionsaufrufe über die Registerkarte „Netzwerk“ von Developer Console:

1. Laden Sie das Skript „Development Launch“ auf der Site.
1. Suchen Sie für Klicks auf Elemente auf der Registerkarte „Netzwerk“ nach „/ee“.

Adobe Experience Platform Debugger:

1. Laden Sie [Adobe Experience Platform Debugger](https://chromewebstore.google.com/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob) herunter und installieren Sie diese Erweiterung.
1. Navigieren Sie zu [!UICONTROL Protokolle] > [!UICONTROL Edge] > [!UICONTROL Mit Edge verbinden].

* **Der Interaktionsaufruf wird nicht auf der Registerkarte „Netzwerk“ ausgelöst**: Klicken Sie in einem Sammlungsaufruf auf die Datenerfassung und filtern Sie entweder mit `"/ee"` oder `"collect?"`.
* **Es gibt keine Payload-Anzeige für den Sammlungsaufruf**: Der Sammlungsaufruf ist so konzipiert, dass das Tracking die Navigation zu anderen Sites nicht beeinflusst, sodass die Funktion zum Entladen von Dokumenten für die Sammlungsaufrufe anwendbar ist. Diese Funktion wirkt sich nicht auf Ihre Datenerfassung aus, aber wenn Sie eine Validierung auf der Seite durchführen müssen, fügen Sie dem entsprechenden Element `target="_blank"` hinzu. Der Link wird in einer neuen Registerkarte geöffnet.
