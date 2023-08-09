---
description: Der erste Schritt beim Erstellen einer Anfrage in Report Builder.
title: 'Datenanforderungen – Anforderungs-Assistent: Schritt 1'
feature: Report Builder
role: User, Admin
exl-id: 698662a8-8b6b-4338-a315-b41cf6a9424e
source-git-commit: fb39f906d6c08713e4dc8211c917b2942502868e
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 98%

---

# Datenanforderungen – Anforderungs-Assistent: Schritt 1

Im Dialogfeld „Anforderungs-Assistent: Schritt 1“ wählen Sie die Report Suite, den Berichtstyp sowie die Segmente aus und konfigurieren Datumswerte.

![Screenshot mit dem Formular Anforderungs-Assistent: Schritt 1.](assets/rw1_overview.png)

1. **[!UICONTROL Report Suite:]** Die Liste der für Sie aufgrund Ihrer Anmeldedaten verfügbaren Report Suites. Siehe [Report Suites auswählen](/help/analyze/report-builder/data-requests/selecting-report-suites/t-select-report-suites.md).

1. **Bereichsauswahl:** Hier können Sie eine Report Suite-ID aus einer Zelle in Excel auswählen. Siehe [Report Suites auswählen](/help/analyze/report-builder/data-requests/selecting-report-suites/t-select-report-suites.md).

1. **Segment**: Segmente sind benutzerspezifische Teildatensätze oder Daten, die durch eigens erstellte Regeln gefiltert wurden. Segmente basieren auf Treffern, Besuchen und Besuchern. Weitere Informationen zu Segmenten finden Sie im [Analytics-Segmentierungsleitfaden](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html?lang=de).

   Beispiel: Sie führen einen [!UICONTROL Seitenbericht] aus und wenden dann das Segment „Erstbesuche“ an.

1. **Berichtstyp**: Hier wird der Basisbericht festgelegt, der in der Datenanforderung ausgeführt werden soll. Es wird ein Bericht pro Anforderung ausgeführt, und dieser Bericht kann 1:n Dimensionen und 1:n Metriken enthalten. Metriken und Dimensionen für einen Berichtstyp werden im Dialogfeld [!UICONTROL Anforderungs-Assistent: Schritt 2] angezeigt. Siehe [Berichtstypen auswählen](/help/analyze/report-builder/data-requests/c-report-types/select-report-types.md).

1. **Datumsbereiche**: Hier wird die von der Anforderung abgedeckte Zeitspanne festgelegt. Es sind verschiedene Arten von Zeiträumen verfügbar, z. B. vordefinierte, feste und rollierende. Es sind maximal 366 Zeiträume erlaubt. Sie können außerdem einen Datumsbereich wählen, der durch eine Zelle festgelegt wird, und Datumsbereiche als Vorlagen zur späteren Verwendung speichern.  Siehe [Berichtsdaten konfigurieren](/help/analyze/report-builder/data-requests/configuring-report-dates/custom-calendar.md).

1. **Granularität anwenden**: Hier wird der Detailgrad für die zeitliche Auflösung des Berichts angegeben. Siehe [Granularität](/help/analyze/report-builder/data-requests/configuring-report-dates/granularity.md).

## Fehlerbehebung

Manchmal wird der Anforderungs-Assistent außerhalb des Bildschirms angezeigt, insbesondere für Benutzer, die zwischen den Monitorinstallationen wechseln. Sie verwenden beispielsweise eine Dockingstation am Arbeitsplatz und Ihren Laptop-Bildschirm zu Hause. Wenn Sie erneut auf „Erstellen“ klicken, während ein Anforderungs-Assistent bereits geöffnet ist, erhalten Sie folgende Fehlermeldung:

„Sie müssen zunächst den Vorgang für den Anforderungs-Assistenten abschließen, bevor Sie einen neuen Anforderungs-Assistenten starten.“

Dieses Problem wird behoben, wenn Sie den Anforderungs-Assistenten wieder zurück auf den Bildschirm bewegen.

1. Öffnen Sie Microsoft Excel und melden Sie sich bei Report Builder an.
2. Klicken Sie auf [!UICONTROL Erstellen], um den Anforderungs-Assistenten außerhalb des Bildschirms zu öffnen.
3. Drücken Sie `[Alt]` + `[Space]`.
4. Drücken Sie `[M]`.
5. Drücken Sie eine der Pfeiltasten.
6. Bewegen Sie die Maus, um den Anforderungsassistenten an Ihren Cursor anzuhängen.
7. Klicken Sie auf die Maus, um den Anforderungs-Assistenten innerhalb des Bildschirms abzulegen.
