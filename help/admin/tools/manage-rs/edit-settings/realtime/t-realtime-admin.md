---
description: Administrative Schritte zum Einrichten von Echtzeitberichten.
title: Konfiguration von Echtzeitberichten
feature: Real-time
exl-id: e039ed67-3694-40fc-a4d9-3cb576e0535c
TQID: https://experienceleague.adobe.com/HTu1UvUUIGK0SzAQWEFBclV-P1JaPCJUp6j5MiYC3A0
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: d3cdead0-685a-4489-9250-4bb709942f66id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 226
ht-degree: 68%

---

# Konfiguration von Echtzeitberichten

Administrative Schritte zum Einrichten von Echtzeitberichten.

Das Einrichten von Echtzeitberichten in Adobe Analytics besteht darin, die Report Suite auszuwählen und bis zu drei Berichte dafür zu konfigurieren. Standardmäßig haben alle Benutzer Zugriff auf Echtzeitberichte.

1. Wählen Sie die Report Suite aus, für die Sie Echtzeit-Berichte aktivieren möchten.

   Navigieren Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin > Report Suites]**.

1. Klicken Sie **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Echtzeit]**.

1. Richten Sie die Echtzeit-Datenerfassung für bis zu drei Berichte ein, wobei pro Bericht eine Metrik und drei Dimensionen oder Classifications erstellt werden.

   ![](/help/admin/tools/manage-rs/edit-settings/realtime/assets/real_time_admin.png)

   Informationen zu unterstützten Echtzeit-Metriken und -Dimensionen finden Sie unter [Unterstützte Metriken und Dimensionen](/help/admin/tools/manage-rs/edit-settings/realtime/realtime-metrics.md).

   Falls Sie Classifications erstellt haben, werden sie unter der Dimension angezeigt, für die sie definiert wurden:

   ![](/help/admin/tools/manage-rs/edit-settings/realtime/assets/classifications.png)

   >[!NOTE]
   >
   >Für einzelne Echtzeitberichte wird die Aktivierung doppelter Dimensionen derzeit nicht unterstützt, auch wenn für jede Dimension eine andere Classification ausgewählt wird.

   >[!NOTE]
   >
   >Manche Dimensionen wie „Keyword“ oder „Produkt“ sind im Gegensatz zu anderen Funktionsbereichen in Adobe Analytics in Echtzeit nicht persistent. Wenn Sie eine nicht persistente Metrik auswählen, erscheint folgende Warnmeldung:

   ![](/help/admin/tools/manage-rs/edit-settings/realtime/assets/warning_dimensions.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   Nach dieser ersten Berichteinrichtung kann es bis zu 20 Minuten dauern, bis die Daten gestreamt werden. Ab diesem Zeitpunkt sind die Daten sofort verfügbar.

1. Um den Echtzeitbericht anzuzeigen, navigieren Sie zu:

   **[!UICONTROL Workspace]** > **[!UICONTROL Berichte]** > **[!UICONTROL Interaktion]** > **[!UICONTROL Echtzeit]**.

