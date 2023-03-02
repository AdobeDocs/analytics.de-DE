---
description: In diesen Schritten wird beschrieben, wie Erfolgsereignisse konfiguriert werden.
title: Konfigurieren von Erfolgsereignissen
feature: Event
exl-id: 0e9a6d8f-2ce7-4551-885d-bd77ff131da0
source-git-commit: ce7f953b8f7f1f7d0616074454e4401937fcc0c7
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 100%

---

# Konfigurieren von Erfolgsereignissen

So konfigurieren Sie Erfolgsereignisse:

1. Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Wählen Sie eine Report Suite aus.
1. Klicken Sie auf **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Konversion]** > **[!UICONTROL Erfolgsereignisse]**.

   ![Schritt Ergebnis](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/assets/success_event_page.png)

1. Aktivieren Sie in der Spalte **[!UICONTROL Name]** das Kontrollkästchen neben dem jeweiligen Element, um die Bearbeitung zu aktivieren, und geben Sie anschließend den gewünschten Namen ein.
1. Aktivieren Sie in der Spalte **[!UICONTROL Typ]** das Kontrollkästchen neben dem jeweiligen Element, um die Dropdown-Liste zu aktivieren, und wählen Sie anschließend den gewünschten Typ aus.

   >[!NOTE]
   >
   >Bevor Sie einen Ereignistyp ändern, lesen Sie [Ändern des Ereignistyps](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/event-type.md).

   Weitere Informationen zu diesen Elementen finden Sie unter [Seite „Erfolgsereignisse“ – Beschreibungen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md).

1. Geben Sie in der Spalte **[!UICONTROL Polarität]** an, ob ein Aufwärtstrend für diese Metrik positiv oder negativ ist.
1. In der Spalte **[!UICONTROL Sichtbarkeit]** können Sie Standardmetriken (integrierte Metriken), benutzerspezifische Ereignisse und die im Menü, in der Metrikauswahl, im Generator für berechnete Metriken und im Segment Builder integrierten Ereignisse ausblenden.

   Diese Einstellung wirkt sich nicht auf die Datenerfassung für diese Metrik oder das Ereignis aus, sondern nur auf die Sichtbarkeit in der Benutzeroberfläche,:


   | Einstellung | Sichtbar in | Nicht sichtbar in |
   |---------|----------|---------|
   | [!UICONTROL **Überall eingeblendet**] | <ul><li>Reports &amp; Analytics (Menü und Metrikauswahl)</li><li>Analysis Workspace</li><li>Segmentaufbau</li><li>Aufbau berechneter Metriken</li></ul> | nicht angegeben |
   | [!UICONTROL **Builder**] | <ul><li>Segmentaufbau</li><li>Aufbau berechneter Metriken</li></ul> | <ul><li>Reports &amp; Analytics (Menü und Metrikauswahl)</li><li>Analysis Workspace</li></ul> |
   | [!UICONTROL **Überall ausgeblendet**] | nicht angegeben | <ul><li>Reports &amp; Analytics (Menü und Metrikauswahl)</li><li>Analysis Workspace</li><li>Segmentaufbau</li><li>Aufbau berechneter Metriken</li></ul> |

1. Geben Sie eine Beschreibung ein.
1. Legen Sie fest, ob das Ereignis immer aufgezeichnet werden soll.
1. Aktivieren oder deaktivieren Sie Beitragsmetriken.

   >[!NOTE]
   >
   >Sie können den Beitrag für bis zu 100 benutzerspezifische Ereignisse aktivieren. Darüber hinaus können Sie im Generator für [berechnete Metriken](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/participation-metric.md) Beitragsmetriken erstellen.

1. Klicken Sie auf **[!UICONTROL Speichern]**.
