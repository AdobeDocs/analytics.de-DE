---
description: Administrative Schritte zum Einrichten von Echtzeitberichten.
title: Echtzeitberichte konfigurieren
feature: Real-time
exl-id: 9e7fc67c-71d5-465a-9553-5bb7e02a9bfd
source-git-commit: a40f30bbe8fdbf98862c4c9a05341fb63962cdd1
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 77%

---

# Echtzeitberichte konfigurieren

Die folgenden Informationen enthalten administrative Schritte zum Einrichten von Echtzeitberichten.

Sie können dabei die Report Suite auswählen und bis zu drei Berichte dafür konfigurieren.

1. Wählen Sie die Report Suite aus, für die Sie Echtzeit-Berichte aktivieren möchten.

   1. Wählen Sie in Analysis Workspace die Registerkarte [!UICONTROL **Workspace**] und dann [!UICONTROL **Berichte**] > [!UICONTROL **Interaktion**] > **[!UICONTROL Echtzeit]**.

   1. Wählen Sie die Report Suite aus der Dropdownliste oben aus:

      ![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/assets/report_suite_selector.png)

      Wenn Sie versuchen, Echtzeitberichte für eine Report Suite anzuzeigen, die nicht für Echtzeitberichte eingerichtet wurde, wird eine Meldung angezeigt, die Ihnen das Einrichten der Report Suite ermöglicht.

      ![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/assets/rep_suite_not_set_up.png)

1. Wählen Sie **[!UICONTROL Konfigurieren]** aus, um den [!UICONTROL Report Suite Manager] auszuführen.

   (Auch verfügbar unter **[!UICONTROL Analytics]** > **[!UICONTROL Admin > Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Echtzeit]**)

1. Aktivieren Sie die Einstellung **[!UICONTROL Echtzeit aktivieren]**.
1. Richten Sie die Echtzeit-Datenerfassung für bis zu drei Berichte ein, wobei pro Bericht eine Metrik und drei Dimensionen oder Classifications erstellt werden.

   ![](assets/real_time_admin.png)

   Informationen zu unterstützten Echtzeit-Metriken und -Dimensionen finden Sie unter [Unterstützte Metriken und Dimensionen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime-metrics.md).

   Falls Sie Classifications erstellt haben, werden sie unter der Dimension angezeigt, für die sie definiert wurden:

   ![](assets/classifications.png)

   >[!NOTE]
   >
   >Für einzelne Echtzeitberichte wird die Aktivierung doppelter Dimensionen derzeit nicht unterstützt, auch wenn für jede Dimension eine andere Classification ausgewählt wird.

   >[!NOTE]
   >
   >Manche Dimensionen wie „Keyword“ oder „Produkt“ sind im Gegensatz zu anderen Funktionsbereichen in Adobe Analytics in Echtzeit nicht persistent. Wenn Sie eine nicht persistente Metrik auswählen, erscheint folgende Warnmeldung:

   ![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/assets/warning_dimensions.png)

1. Wählen Sie **[!UICONTROL Speichern]** oder **[!UICONTROL Speichern und Bericht anzeigen]**.

   Nach diesem ersten Bericht-Setup kann es bis zu 20 Minuten dauern, bis Daten gestreamt werden. Daraufhin sind die Daten sofort verfügbar. Informationen zum Anzeigen von Echtzeitberichten erhalten Sie unter [Einen Echtzeitbericht ausführen](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/t-running-report-types.html?lang=de).

1. Standardmäßig haben alle Benutzer Zugriff auf Echtzeitberichte.
