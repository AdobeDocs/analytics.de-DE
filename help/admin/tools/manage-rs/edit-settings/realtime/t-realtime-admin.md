---
description: Administrative Schritte zum Einrichten von Echtzeitberichten.
title: Konfiguration von Echtzeitberichten
feature: Real-time
exl-id: e039ed67-3694-40fc-a4d9-3cb576e0535c
TQID: 'https://experienceleague.adobe.com/HTu1UvUUIGK0SzAQWEFBclV-P1JaPCJUp6j5MiYC3A0'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
subfeature_v2:
  - id: e3f5b014-59dd-41c0-90f5-c405dcfaed07
    internal-label: Real time reporting
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9a50beeb0aa51cf9f4baf212566947c14029ce8e
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 68%
---
# Konfiguration von Echtzeitberichten

Administrative Schritte zum Einrichten von Echtzeitberichten.

Das Einrichten von Echtzeitberichten in Adobe Analytics besteht darin, die Report Suite auszuwählen und bis zu drei Berichte dafür zu konfigurieren. Standardmäßig haben alle Benutzer Zugriff auf Echtzeitberichte.

1. Wählen Sie die Report Suite aus, für die Sie Echtzeitberichte aktivieren möchten.

   Navigieren Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin > Report Suites]**.

1. Klicken Sie **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Echtzeit]**.

1. Richten Sie die Echtzeit-Datenerfassung für bis zu drei Berichte ein, mit jeweils einer Metrik und drei Dimensionen oder Klassifizierungen pro Bericht.

   ![](/help/admin/tools/manage-rs/edit-settings/realtime/assets/real_time_admin.png)

   Informationen zu unterstützten Echtzeit-Metriken und -Dimensionen finden Sie unter [Unterstützte Metriken und Dimensionen](/help/admin/tools/manage-rs/edit-settings/realtime/realtime-metrics.md).

   Falls Sie Klassifizierungen erstellt haben, werden sie unter der Dimension angezeigt, für die sie definiert wurden:

   ![](/help/admin/tools/manage-rs/edit-settings/realtime/assets/classifications.png)

   >[!NOTE]
   >
   >Für einen einzelnen Echtzeitbericht wird die Aktivierung doppelter Dimensionen derzeit nicht unterstützt, auch wenn für jede Dimension eine andere Klassifizierung ausgewählt wird.

   >[!NOTE]
   >
   >Manche Dimensionen wie „Suchbegriff“ oder „Produkt“ sind im Gegensatz zu anderen Funktionsbereichen in Adobe Analytics in Echtzeit nicht persistent. Wenn Sie eine nicht persistente Metrik auswählen, erscheint folgende Warnmeldung:

   ![](/help/admin/tools/manage-rs/edit-settings/realtime/assets/warning_dimensions.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   Nach dieser ersten Berichteinrichtung kann es bis zu 20 Minuten dauern, bis die Daten gestreamt werden. Ab diesem Zeitpunkt sind die Daten sofort verfügbar.

1. Um den Echtzeitbericht anzuzeigen, navigieren Sie zu:

   **[!UICONTROL Workspace]** > **[!UICONTROL Berichte]** > **[!UICONTROL Interaktion]** > **[!UICONTROL Echtzeit]**.

