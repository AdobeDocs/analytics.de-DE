---
description: Mit dem Dashboard-Manager können Sie Dashboards kopieren, freigeben, archivieren und deren Auslieferung planen.
seo-description: Mit dem Dashboard-Manager können Sie Dashboards kopieren, freigeben, archivieren und deren Auslieferung planen.
seo-title: Dashboard-Manager
solution: Analytics
subtopic: Dashboards
title: Dashboard-Manager
topic: Reports and Analytics
uuid: 380fd148-2ed9-43bf-9d42-46e373e788e4
translation-type: tm+mt
source-git-commit: cc87c5a7b193fe8a36ce7409a833cc0b91b8af60

---


# Dashboard-Manager

Mit dem Dashboard-Manager können Sie Dashboards kopieren, freigeben, archivieren und deren Auslieferung planen.

>[!IMPORTANT]
>
>Beim Einsatz des Dashboard-Managers wird empfohlen, für einen Benutzer nicht mehr als 300 Dashboards zu verwenden. Beachten Sie auch, dass der Manager alle freigegebenen Dashboards unten lädt. Achten Sie daher darauf, Dashboards freizugeben.

## Dashboard-Manager

Mit dem Dashboard-Manager können Sie Dashboards kopieren, freigeben, archivieren und deren Auslieferung planen.

Click **[!UICONTROL Analytics]** &gt; **[!UICONTROL Components]** &gt; **[!UICONTROL Dashboards]**.

| Element | Beschreibung |
|--- |--- |
| Freigegeben | Zeigt an, ob das Dashboard freigegeben ist. |
| Eingeplant | Damit können Sie die Bereitstellung eines Dashboards einplanen. |
| Archiv anzeigen | Hiermit können Sie das Dashboard-Archiv anzeigen. Diese Funktion ist ab Januar 2020 nicht mehr verfügbar. |
| An Benutzer senden | Hiermit können Sie ein Dashboard freigeben. |
| Verwalten | Hiermit können Sie ein Dashboard bearbeiten, kopieren und löschen. |

## Freigegebene Dashboards verwalten

Schritte, in denen beschrieben wird, wie Sie die Verwaltungsoptionen für freigegebene Dashboards verwenden.

1. Go to **[!UICONTROL Analytics]** &gt; **[!UICONTROL Components]** &gt; **[!UICONTROL Dashboards]**.
1. Suchen Sie unter [!UICONTROL „Freigegebene Dashboards“] das freigegebene Dashboard (oder Legacy-Dashboard), das Sie verwalten möchten, und wählen Sie eine oder mehrere der folgenden Optionen:

<table id="choicetable_857E0E816D63404683D4E24DC8D7FC69"> 
 <thead class="chhead sthead"> 
  <th class="choptionhd"> Option </th> 
  <th class="chdeschd"> Beschreibung </th> 
 </thead> 
 <tr class="chrow strow"> 
  <td class="choption"><strong>Archiv anzeigen</strong></td> 
  <td class="chdesc stentry"> Damit können Sie das Berichtsarchiv für das freigegebene Dashboard anzeigen, sofern ein Archiv vorhanden ist. </td> 
 </tr> 
 <tr class="chrow strow"> 
  <td class="choption"><strong>Dashboard-Player</strong></td> 
  <td class="chdesc stentry"> <p>Die Server von SiteCatalyst 14 reagieren nicht mehr auf Dashboard Player-Datenanforderungen. Alle Dashboards, die derzeit im Dashboard Player angezeigt werden, können über die Standardoberfläche „Reports &amp; Analytics“ aufgerufen oder als Real-Time Dashboard neu erstellt werden. Real-Time Dashboards sind speziell für die kontinuierliche Anzeige konzipiert und enthalten einen Vollbildmodus für die Anzeige auf TV-Geräten oder anderen Geräten mit großen Bildschirmen. </p> <p>Erforderliche Benutzeraktion: Sie müssen aufhören, den Dashboard Player zu verwenden. </p> </td> 
 </tr> 
 <tr class="chrow strow"> 
  <td class="choption"><strong>Kopier mich</strong></td> 
  <td class="chdesc stentry"> Fügt Ihrer Dashboard-Liste eine Kopie hinzu und verwendet dabei den gleichen Namen wie das Original. Sie können allerdings keine vom Eigentümer des Dashboards vorgenommenen Aktualisierungen/Änderungen sehen. Wenn Sie ein Legacy-Dashboard kopieren, wird ein leeres Dashboard geöffnet, in das Sie dann den Legacy-Inhalt einfügen können. <p>Wichtig: Wenn die von Ihnen am Dashboard vorgenommenen Änderungen für gemeinsame Benutzer nicht sichtbar sind, prüfen Sie Ihren Dashboard-Manager, um zu sehen, ob die Benutzer die Option <span class="uicontrol">Kopier mich</span> ausgewählt haben. Falls nicht, können sie die von Ihnen vorgenommenen Aktualisierungen/Änderungen nicht sehen. Um alle Änderungen/Updates sehen zu können, müssen gemeinsame Benutzer die Option <span class="uicontrol">Im Menü</span> im Dashboard-Manager auswählen. </p> </td> 
 </tr> 
 <tr class="chrow strow"> 
  <td class="choption"><strong>Im Menü</strong></td> 
  <td class="chdesc stentry"> Damit können Sie vom Dashboard-Eigentümer vorgenommene Änderungen/Aktualisierungen anzeigen. </td> 
 </tr> 
 <tr class="chrow strow"> 
  <td class="choption"><strong>Freigabe aufheben</strong></td> 
  <td class="chdesc stentry"> Entfernt das Dashboard aus Ihrer Liste freigegebener Dashboards. </td> 
 </tr> 
</table>

## Legacy-Dashboard migrieren

Sie können vorhandene Legacy-Dashboards weiterhin ausführen, bearbeiten, herunterladen und planen. Neue Legacy-Dashboards können Sie jedoch nicht mehr erstellen. Wir empfehlen Ihnen dringend, vorhandene Legacy-Dashboards auf das neue Dashboard-Format zu aktualisieren.

>[!NOTE]
>
>Moving forward, consider using [Analysis Workspace projects](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/) and their ability to be downloaded and scheduled.

Beim Kopieren eines Legacy-Dashboards öffnet das System dieses zur Bearbeitung, wobei Sie Legacy-Inhalt oder neuen Inhalt hinzufügen können. Wenn Sie ein Legacy-Dashboard kopieren, bleibt das Original in der Liste der Legacy-Dashboards erhalten.

>[!NOTE]
>
>Durch das Hinzufügen von Legacy-Inhalten zu einem Dashboard wird ein Dashboard auf der Grundlage der neuesten Dashboard-Funktionalität erstellt. Das Legacy-Reportlet enthält jedoch eventuell Daten, die auf der vorherigen Datenplattform basieren.

**So migrieren Sie ein Legacy-Dashboard der Version 14.x**

1. Click **[!UICONTROL Analytics]** &gt; **[!UICONTROL Components]** &gt; **[!UICONTROL Manage Dashboards]**.
1. Klicken Sie in der Spalte [!UICONTROL Verwalten] unter [!UICONTROL Legacy-Dashboards]**auf[!UICONTROL In neues Dashboard kopieren]**.

   Das kopierte Dashboard wird im Dashboard-Layout-Bearbeiter geöffnet. 

   Siehe [Bearbeiten von Dashboard- und Reportlet-Daten](../../analyze/reports-analytics/dashboard.md#task_B460CCD70D9F40FCAC6BBC1C044CC460).

## Dashboard freigeben

In diesen Schritten wird beschrieben, wie ein Administrator ein Dashboard für mehrere Benutzer freigeben (oder auf diese übertragen) kann. Wenn Sie Benutzern Dashboards senden, stehen die Dashboards diesen Benutzern in deren [!UICONTROL freigegebenen Dashboards] zur Verfügung.

1. Suchen Sie im [!UICONTROL Dashboard-Manager]**das Dashboard und aktivieren Sie anschließend[!UICONTROL Freigegeben]**.
1. Klicken Sie auf **[!UICONTROL An Benutzer senden]**.  ![](assets/push.png)

1. Wählen Sie auf der Seite [!UICONTROL Dashboard verschieben] die Zielbenutzer aus oder klicken Sie auf **[!UICONTROL Alle markieren]**.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

Wenn die von Ihnen am Dashboard vorgenommenen Änderungen für gemeinsame Benutzer nicht sichtbar sind, prüfen Sie Ihren Dashboard-Manager, um zu sehen, ob die Benutzer die Option **[!UICONTROL Kopier mich]ausgewählt haben.** Falls nicht, können sie die von Ihnen vorgenommenen Aktualisierungen/Änderungen nicht sehen. Um alle Änderungen/Updates sehen zu können, müssen gemeinsame Benutzer die Option **[!UICONTROL Im Menü]im Dashboard-Manager auswählen.**

## Bereitstellung eines Dashboards planen

Im [!UICONTROL Dashboard-Manager] können Sie sehen, ob ein Dashboard für die Auslieferung eingeplant ist, sowie den Plan bearbeiten. Die Dashboard-Auslieferungsoptionen sind identisch mit den Optionen für die Berichtsauslieferung.

1. Öffnen Sie ein Dashboard.
1. Click **[!UICONTROL More]** &gt; **[!UICONTROL Send]**.

   See [Schedule and Distribution](../../analyze/reports-analytics/scheduling.md#concept_4EA333DFC7FD4E9CA086385A3DA10BE9) for more information.

## Dashboard archivieren

>[!NOTE]
>
>Diese Funktion ist ab Januar 2020 nicht mehr verfügbar.

In diesen Schritten wird beschrieben, wie Sie ein gesendetes Dashboard als PDF-Datei archivieren können. Das System speichert die archivierte Datei zwei Jahre lang oder bis das 4-GB-Limit für archivierte Berichte erreicht wurde, je nachdem, was zuerst eintritt.

1. Öffnen Sie ein Dashboard.
1. Click **[!UICONTROL More]** &gt; **[!UICONTROL Send]**.
1. Aktivieren Sie in der Gruppe [!UICONTROL Bericht per E-Mail]**die Option[!UICONTROL Archiv]**.
1. Legen Sie die gewünschten Übermittlungsoptionen fest, und klicken Sie anschließend auf **[!UICONTROL Senden]**.

   Archivierte Dashboards können Sie im Dashboard-Manager anzeigen. Alternatively, open a dashboard and click **[!UICONTROL More]** &gt; **[!UICONTROL View Archive]**.
