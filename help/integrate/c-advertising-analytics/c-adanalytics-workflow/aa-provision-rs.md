---
description: Konfigurieren Sie eine Report Suite, die Experience Cloud zugeordnet ist, für die Verwendung in Advertising Analytics.
title: Report Suite für Advertising Analytics aktivieren
feature: Advertising Analytics
exl-id: 3a467e41-2755-46c1-b077-b42946562e6b
source-git-commit: c53b533a1d037ab3ed811bcc0960418f037a708f
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 47%

---

# Report Suite für Advertising Analytics aktivieren

Um Advertising Analytics-Suchdaten in Analytics anzuzeigen, müssen Sie jede Experience Cloud-zugeordnete Report Suite für die Advertising Analytics-Berichterstellung konfigurieren.

1. Navigieren Sie zu **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.

1. Wählen Sie die Report Suite aus, die Ihrer Experience Cloud-Organisation zugeordnet ist.
1. Klicken Sie auf **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Advertising Analytics-Konfiguration]**.

   ![Berichterstellung](assets/aa-reporting.png)

   >[!IMPORTANT]
   >
   >AMO-ID bezieht sich auf die Adobe Advertising Cloud-Variable (auch als Adobe Media Optimizer bezeichnet), in die die Suchdaten eingefügt werden.

1. Wählen Sie **[!UICONTROL Unbekannt mit Advertising Analytics? Hier erfahren Sie mehr zu Advertising Analytics]** .

1. Legen Sie die Variablenzuordnung und -gültigkeit fest, die die AMO-ID-Variable verwenden soll. Konversionsvariablen (eVars) ermöglichen es Adobe Analytics, Erfolgsereignisse spezifischen Variablenwerten zuzuordnen. Manchmal weisen Variablen mehrere Werte auf, bevor sich ein Erfolgsereignis einstellt. In diesen Fällen wird durch die Zuordnung festgelegt, auf welchen Variablenwert das Ereignis zurückgeführt wird.

   | Einstellung | Definition |
   |--- |--- |
   | **[!UICONTROL Zuordnung]** | Wählen Sie zwischen:<br/> **[!UICONTROL Ausgangswert (Erster)]**: Der erste angezeigte Wert erhält eine vollständige Zuordnungsgutschrift, unabhängig davon, welche nachfolgenden Werte für diese Variable vorhanden sind. <br/>**[!UICONTROL Zuletzt verwendet (Letzter)]**: Der zuletzt angezeigte Wert erhält die vollständige Zuordnung für das Erfolgsereignis, unabhängig davon, welche Variablen zuvor ausgelöst wurden. |
   | **[!UICONTROL Läuft ab nach]** | Ermöglicht die Angabe eines Zeitraums oder Ereignisses, nach dem der eVar abläuft (d. h. keine Gutschrift für Erfolgsereignisse mehr erhält).  Falls nach Ablauf der eVar (d. h. wenn keine eVar aktiv ist) ein Erfolgsereignis eintritt, wird das Ereignis dem Wert „Keine“ gutgeschrieben. |

1. Klicken Sie auf **[!UICONTROL Advertising Analytics-Reporting aktivieren]** (beim ersten Mal) oder **[!UICONTROL Advertising Analytics-Reporting aktualisieren]** (bei darauffolgenden Malen). Ihre Report Suite kann jetzt Advertising Analytics-Suchdaten empfangen. Sie können jetzt [Advertising-Konten erstellen](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-create-ad-account.md).
