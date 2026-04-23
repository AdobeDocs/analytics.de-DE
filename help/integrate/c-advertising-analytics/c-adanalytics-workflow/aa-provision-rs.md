---
description: Konfigurieren Sie eine Report Suite, die Experience Cloud zugeordnet ist, für die Verwendung in Advertising Analytics.
title: Report Suite für Advertising Analytics aktivieren
feature: Advertising Analytics
exl-id: 3a467e41-2755-46c1-b077-b42946562e6b
source-git-commit: cbfe932eecf2e89d72b1aa373d723de4cf0af073
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 27%

---

# Report Suite für Advertising Analytics aktivieren

To see any Advertising Analytics search data in Analytics, you need to configure each Experience Cloud-mapped report suite for Advertising Analytics reporting.

1. Navigieren Sie zu **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.

1. Wählen Sie die Report Suite aus, die Ihrer Experience Cloud-Organisation zugeordnet ist.
1. Klicken Sie auf **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Advertising Analytics-Konfiguration]**.

   ![Berichterstellung](assets/aa-reporting.png)

1. Select **[!UICONTROL Unfamiliar with Advertising Analytics? Click here to learn more]** for more information on Advertising Analytics.

1. Set the variable allocation and expiration that you want the AMO ID variable to use. Conversion variables (eVars) allow Adobe Analytics to attribute success events to specific variable values. Sometimes, variables encounter more than one value before hitting a success event. For these cases, allocation determines which variable value gets credit for the event.

   | Einstellung | Definition |
   |--- |--- |
   | **[!UICONTROL Zuordnung]** | Select between:<br/> **[!UICONTROL Original Value (First)]**: The first value seen gets full allocation credit, no matter what subsequent values for that variable are. <br/>**[!UICONTROL Most Recent (Last)]**: The last value seen gets full allocation credit for the success event, no matter what variables were fired before it. |
   | **[!UICONTROL Läuft ab nach]** | Lets you specify a time period, or event, after which the eVar value expires (that is, no longer receives credit for success events).  Falls nach Ablauf der eVar (d. h. wenn keine eVar aktiv ist) ein Erfolgsereignis eintritt, wird das Ereignis dem Wert „Keine“ gutgeschrieben. |

1. Click **[!UICONTROL Enable Advertising Analytics Reporting]** (first time), or **[!UICONTROL Update Advertising Analytics Reporting]** (subsequent times). Your report suite is now ready to receive Advertising Analytics Search data. You are now ready to [create Advertising Accounts](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-create-ad-account.md).
