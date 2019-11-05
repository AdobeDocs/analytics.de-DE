---
description: Erläutert die Schritte, die der Analytics-Administrator ausführen muss, um die Activity Map-Linkerfassung und den Download durch den Benutzer zu ermöglichen.
seo-description: Erläutert die Schritte, die der Analytics-Administrator ausführen muss, um die Activity Map-Linkerfassung und den Download durch den Benutzer zu ermöglichen.
seo-title: Activity Map aktivieren
solution: Analytics
title: Activity Map aktivieren
topic: Activity Map
uuid: 30433319-d0e6-4977-951a-4492b356e1f2
translation-type: tm+mt
source-git-commit: 57fe1f6d613b9f54a5191ac8684d36bccfebf4e5

---


# Activity Map aktivieren{#enable-activity-map}

Erläutert die Schritte, die der Analytics-Administrator ausführen muss, um die Activity Map-Linkerfassung und den Download durch den Benutzer zu ermöglichen.

## Schritt 1. Update Your AppMeasurement (Javascript) Code to v1.6 (or higher) {#section_5D1586289DF2489289B1B6C1C80C300D}

Das Activity Map-Modul ist Bestandteil der Datei AppMeasurement.js (befindet sich oben in der Datei). Die AppMeasurement-Bibliothek lädt das Activity Map-Modul nach der Instanziierung.

Activity Map-Daten können erst erfasst werden, nachdem AppMeasurement auf diese Version (oder höher) aktualisiert wurde.

1. Download the latest AppMeasurement code (AppMeasurement_Javascript-1.6.zip) by going to  **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Code Manager]** and [implement it](https://marketing.adobe.com/resources/help/en_US/sc/implement/js_implementation.html).

   Der verfügbare [Beispiel-Implementierungscode](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-sample-implementation-code.md) veranschaulicht die Änderungen, die am Code durch Einbindung des Activity Map-Moduls vorgenommen wurden.

1. Validieren Sie die Implementierung:

   1. Wenn auf ein klickbares Element geklickt wird, werden Daten in einem Cookie namens s_sq gespeichert.
   1. Die Activity Map-Daten sind in der Abfragezeichenfolge des Tracking-Aufrufs sichtbar. Beispiel:

      ```
      …&c.&a.&Activity Map.&link=My%20Link&region=My%20Region&page=My%20Page&.Activity Map&.a&.c&...
      ```

1. Break this report down by **[!UICONTROL Activity Map Link by Region]** to see the link/region for that page:  ![](assets/am_breakdown.png){width="400px"}

## Schritt 2: Enable Activity Map reports {#section_D14F15D2FC0346FCAD8B3B87E6DD33D4}

Zunächst müssen Sie Activity Map-Berichte auf einer Report Suite-Ebene aktivieren.

1. Log in to Adobe Analytics and navigate to  **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin &gt; Report Suites &gt;[select report suite]&gt; Edit Settings &gt; Activity Map]** &gt; **[!UICONTROL Activity Map Reporting]** .
1. Activity Map erfasst die Linkdaten in Activity Map-Berichten. Zur Aktivierung müssen Sie zunächst die Variablen aktivieren, indem Sie auf **[!UICONTROL Activity Map-Berichte aktivieren klicken]**.

   Dieser Schritt fügt alle Analytics-Dimensionen hinzu, die Sie zur Datenerfassung benötigen.

1. Nach etwa einer Stunde können Sie sich den [Activity Map-Seitenbericht](/help/analyze/activity-map/activitymap-reporting-analytics.md) ansehen, der alle Seiten enthält, auf denen Benutzer auf einen Link geklickt haben.

## Schritt 3. Add users to Activity Map access group {#section_4C7A47BB7DEF4AFFBC276392467F9675}

1. Klicken Sie auf **[!UICONTROL Benutzer zur Gruppe hinzufügen]**.

   Dies bringt Sie zur Gruppenverwaltungsseite in der Admin Console.

1. [Fügen Sie Benutzer dieser Gruppe hinzu](https://marketing.adobe.com/resources/help/en_US/reference/groups.html) und klicken Sie auf **[!UICONTROL Gruppe speichern]**.

1. This allow your Admin users to download Activity Map from  **[!UICONTROL Adobe Analytics]** &gt; **[!UICONTROL Tools]** &gt; **[!UICONTROL ActivityMap]** .

> [!NOTE] Wenn Sie möchten, dass Benutzer, die keine Administratoren sind, Activity Map herunterladen können, erstellen Sie eine neue Benutzergruppe, die Berechtigungen für "Tools"und "Legacy ClickMap-Installation"bereitstellt. Diese Berechtigungsstufe in Verbindung mit dem Activity Map-Zugriff bietet Berechtigungen zum Herunterladen und Verwenden des Tools.
