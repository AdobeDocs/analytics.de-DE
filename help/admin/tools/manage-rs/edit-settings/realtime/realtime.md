---
description: Zeigt den Traffic der Web-Seite an und ordnet Seitenansichten in Echtzeit zu. Liefert relevante Daten, auf die Sie Ihre Geschäftsentscheidungen stützen können.
title: Echtzeitberichte
feature: Real-time
exl-id: 267246ba-617f-4284-aaad-d0ace0f6a8cf
TQID: https://experienceleague.adobe.com/SqFAddRYrXCrQyB-LjgsaLWoEQXMLc7hkdgcAcgUdsM
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 611
ht-degree: 14%

---

# Echtzeitberichte

Zeigt den Traffic der Web-Seite an und ordnet Seitenansichten in Echtzeit zu. Liefert relevante Daten, auf die Sie Ihre Geschäftsentscheidungen stützen können.

>[!NOTE]
>
>Für den Echtzeitbericht sind keine zusätzlichen Implementierungen oder Taggings erforderlich. Sie nutzt die vorhandene Implementierung von Adobe Analytics. Informationen zum Konfigurieren von Echtzeitberichten finden Sie unter [Konfiguration von Echtzeitberichten](/help/admin/tools/manage-rs/edit-settings/realtime/t-realtime-admin.md).

Um den Echtzeitbericht anzuzeigen, navigieren Sie zu:

**[!UICONTROL Workspace]** > **[!UICONTROL Berichte]** > **[!UICONTROL Interaktion]** > **[!UICONTROL Echtzeit]**.

Real-Time beantwortet die folgenden Fragen: Was liegt auf meiner Website im Trend und warum? Dadurch können Sie als Marketing-Experte schnell auf die Leistung Ihrer Marketing-Inhalte und -Kampagnen reagieren und diese aktiv verwalten. Die gemeldeten Echtzeitdaten sind weniger als zwei Minuten lang latent und werden jede Minute automatisch aktualisiert.

![](/help/admin/tools/manage-rs/edit-settings/realtime/assets/report-realtime.png)

Das Dashboard enthält hochfrequente Adobe Analytics-Metriken und Site-Analysen, um Traffic und Seitenansichts-Trends von dynamischen Nachrichten- und Einzelhandels-Websites visuell zu melden. Echtzeit versteht Trends in Ihren Daten von Minute zu Minute, innerhalb von Sekunden nach der Erfassung. Es erfasst und streamt Daten in eine automatisch aktualisierende Benutzeroberfläche, wobei die Echtzeit-Korrelation und das Tracking von Inhalten sowie einige Konversionen verwendet werden.

Zu den häufigsten Nutzungsszenarien gehören Publisher, die Storys bei Änderungen der Benutzeraktivität bewerben/herunterstufen möchten, und Marketing-Experten, die die Einführung einer neuen Produktlinie verfolgen möchten.

Als Administrator haben Sie folgende Möglichkeiten

* Erstellen von bis zu 3 Echtzeitberichten pro Report Suite unter Verwendung vorhandener Dimensionen oder Klassifizierungen und Metriken. Verwenden Sie die sekundären Dimensionen, um sie mit der primären Dimension zu korrelieren (oder aufzuschlüsseln).
* Fügen Sie zusätzlich zu einer Site-weiten Metrik drei Dimensionen (oder Klassifizierungen) pro Bericht hinzu (eine primäre und zwei sekundäre).
* Verwenden Sie ein benutzerdefiniertes Ereignis, ein Warenkorbereignis oder eine Instanz.
* Zeigen Sie bis zu 2 Stunden historische Echtzeitdaten an und ändern Sie diese Einstellung:

   * Letzte 15 Minuten: Granularität von 1 Minute
   * Letzte 30 Minuten: Granularität von 1 Minute
   * Letzte Stunde: Granularität von 2 Minuten
   * Letzte 2 Stunden: Granularität von 4 Minuten

* Vergleichen Sie beispielsweise die Werte der letzten Woche mit den Werten des letzten Jahres (sowie mit dem heutigen Gesamtwert).

Beachten Sie, dass eVars (Konversionsmetriken) nicht unterstützt werden, da es kein Persistenzkonzept gibt. Sie können zwar Konversionsmetriken auswählen, sie funktionieren jedoch nur, wenn sie auf derselben Seite wie die Dimension(en) festgelegt sind. Weitere Informationen finden Sie in der Warnmeldung unter [Einrichten von Echtzeitberichten](/help/admin/tools/manage-rs/edit-settings/realtime/t-realtime-admin.md).

Das Einrichten und Anzeigen von Echtzeitberichten ist auf Administratoren oder alle Benutzer in den Berechtigungsgruppen „Zugriff auf alle Berichte“ und „Erweiterte Berichterstellung“ beschränkt. In Echtzeit werden die Berechtigungen jedoch nicht beachtet. Wenn Sie beispielsweise nicht über die erforderlichen Rechte zur Anzeige von Umsatz verfügen, können Sie keinen Echtzeitbericht anzeigen, der Umsatzdaten enthält.

## Datenlatenz als Folge der A4T-Konfiguration {#latency}

Nachdem die A4T-Integration in Adobe Target aktiviert wurde, tritt in Adobe Analytics eine zusätzliche Latenz von 5-10 Minuten auf. Durch diese Latenzerhöhung können Daten aus Analytics und Target im selben Treffer gespeichert werden, sodass Sie Tests nach Seite und Site-Abschnitt aufschlüsseln können.

Dieser Anstieg spiegelt sich in allen Services und Tools von Adobe Analytics wider, einschließlich Live-Stream und Echtzeitberichten, und gilt in den folgenden Szenarien:

* Bei Live-Streams, Echtzeitberichten und API-Anfragen sowie aktuellen Daten zu Traffic-Variablen werden nur Treffer mit einer zusätzlichen Daten-ID verzögert.
* Bei aktuellen Daten zu Konversionsmetriken, finalisierten Daten und Daten-Feeds werden alle Treffer um weitere 5-7 Minuten verzögert.

Achten Sie darauf, dass die Erhöhung der Latenz nach der Implementierung des Identity Service beginnt, auch wenn Sie diese Integration nicht vollständig implementiert haben.
