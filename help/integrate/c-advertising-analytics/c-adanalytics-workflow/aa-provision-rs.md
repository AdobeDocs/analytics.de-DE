---
description: Konfigurieren einer zugeordneten Report Suite von CX Enterprise für die Verwendung in Advertising Analytics.
title: Report Suite für Advertising Analytics aktivieren
feature: Advertising Analytics
exl-id: 3a467e41-2755-46c1-b077-b42946562e6b
TQID: 'https://experienceleague.adobe.com/sGEXiz2RiDhf9p-2df76o-XxBERTKPB-O-rZeIb4BBI'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
subfeature_v2:
  - id: fe0a7292-80bc-407a-b456-64170267d1cc
  - id: a9364d69-0c51-44bf-8b5f-6d99c04493b8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 301a0341e725ca15f1700046528ea5f42969add4
workflow-type: tm+mt
source-wordcount: 268
ht-degree: 18%

---

# Report Suite für Advertising Analytics aktivieren

Um Advertising Analytics-Suchdaten in Analytics anzuzeigen, müssen Sie jede von CX Enterprise zugeordnete Report Suite für das Reporting in Advertising Analytics konfigurieren.

1. Navigieren Sie zu **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.

1. Wählen Sie die Report Suite aus, die Ihrer CX Enterprise-Organisation zugeordnet ist.
1. Klicken Sie auf **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Advertising Analytics-Konfiguration]**.

   ![Berichterstellung](assets/aa-reporting.png)

1. Wählen Sie **[!UICONTROL Mit Advertising Analytics nicht vertraut? Klicken Sie hier, um mehr zu erfahren]** um weitere Informationen zu Advertising Analytics zu erhalten.

1. Legen Sie die Variablenzuordnung und den Gültigkeitszeitraum fest, die die AMO ID-Variable verwenden soll. Konversionsvariablen (eVars) ermöglichen es Adobe Analytics, Erfolgsereignisse bestimmten Variablenwerten zuzuordnen. Manchmal stoßen Variablen auf mehr als einen Wert, bevor sie auf ein Erfolgsereignis treffen. In diesen Fällen bestimmt die Zuordnung, welcher Variablenwert für das Ereignis gutgeschrieben wird.

   | Einstellung | Definition |
   |--- |--- |
   | **[!UICONTROL Zuordnung]** | Auswählen zwischen:<br/> **[!UICONTROL Ausgangswert (Erste)]**: Der erste angezeigte Wert erhält eine vollständige Zuordnung, unabhängig davon, welche nachfolgenden Werte für diese Variable sind. <br/>**[!UICONTROL Zuletzt verwendet (Letzte)]**: Der zuletzt angezeigte Wert erhält die volle Zuordnung für das Erfolgsereignis, unabhängig davon, welche Variablen zuvor ausgelöst wurden. |
   | **[!UICONTROL Läuft ab nach]** | Hier können Sie einen Zeitraum oder ein Ereignis angeben, nach dem der eVar-Wert abläuft (d. h. nicht mehr für Erfolgsereignisse angerechnet wird).  Falls nach Ablauf der eVar (d. h. wenn keine eVar aktiv ist) ein Erfolgsereignis eintritt, wird das Ereignis dem Wert „Keine“ gutgeschrieben. |

1. Klicken Sie auf **[!UICONTROL Advertising Analytics-Reporting aktivieren]** (erstes Mal) oder **[!UICONTROL Advertising Analytics-Reporting aktualisieren]** (nachfolgende Male). Ihre Report Suite ist jetzt für den Empfang von Advertising Analytics-Suchdaten bereit. Sie können jetzt &quot;[&#x200B; Advertising-Konten erstellen](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-create-ad-account.md).
