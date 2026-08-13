---
description: Der erste Schritt beim Erstellen einer Anfrage in Report Builder.
title: 'Datenanforderungen – Anforderungs-Assistent: Schritt 1'
feature: Report Builder
role: User, Admin
exl-id: 698662a8-8b6b-4338-a315-b41cf6a9424e
TQID: https://experienceleague.adobe.com/87MzdxBePRZKBttF3P6XhuDq5hR6XpEWaLdrYDMu-5Y
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2: id: ac8a38fa-dec3-4581-8f64-178fde9f64e8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 401
ht-degree: 66%

---

# Datenanforderungen – Anforderungs-Assistent: Schritt 1

{{legacy-arb}}

Im Dialogfeld „Anforderungs-Assistent: Schritt 1“ wählen Sie die Report Suite, den Berichtstyp sowie die Segmente aus und konfigurieren Datumswerte.

![Screenshot mit dem Anforderungs-Assistenten: Schritt 1 Formular.](assets/rw1_overview.png)

1. **[!UICONTROL Report Suite:]** Die Liste der für Sie aufgrund Ihrer Anmeldedaten verfügbaren Report Suites. Siehe [Report Suites auswählen](/help/analyze/legacy-report-builder/data-requests/selecting-report-suites/t-select-report-suites.md).

1. **Bereichsauswahl:** Hier können Sie eine Report Suite-ID aus einer Zelle in Excel auswählen. Siehe [Report Suites auswählen](/help/analyze/legacy-report-builder/data-requests/selecting-report-suites/t-select-report-suites.md).

1. **Segment**: Segmente sind benutzerspezifische Daten-Teilmengen oder Daten, die durch eigens erstellte Regeln gefiltert wurden. Segmente basieren auf Treffern, Besuchen und Besuchern. Weitere Informationen zu Segmenten finden [ im ](/help/components/segmentation/seg-home.md) Analytics-Segmentierungshandbuch .

   Beispiel: Sie führen einen [!UICONTROL Seitenbericht] aus und wenden dann das Segment „Erstbesuche“ an.

1. **Überschreiben der Veröffentlichungsliste zulassen**: Veröffentlichungslisten waren eine Funktion in Reports &amp; Analytics, die [Ende der Lebensdauer](https://new.express.adobe.com/webpage/WFCyq7w8kijmB?) wurde.

1. **Berichtstyp**: Gibt den Basisbericht an, den Sie in Ihrer Datenanfrage ausführen möchten. Es wird ein Bericht pro Anforderung ausgeführt, und dieser Bericht kann 1:n Dimensionen und 1:n Metriken enthalten. Metriken und Dimensionen für einen Berichtstyp werden in der Benutzeroberfläche [!UICONTROL Anforderungs-Assistent; Schritt 2] angezeigt. Siehe [Auswählen von Berichtstypen](/help/analyze/legacy-report-builder/data-requests/c-report-types/select-report-types.md).

1. **Datumsbereiche**: Definiert die Zeitspanne, die von der Anfrage abgedeckt wird. Es stehen verschiedene Arten von Anfragezeiträumen zur Verfügung, z. B. „Voreingestellt“, „Festgelegt“ und „Rollierend“. Die maximale Anzahl von Zeiträumen beträgt 366. Sie können auch einen durch eine Zelle angegebenen Datumsbereich auswählen und Datumsbereiche zur späteren Verwendung als Vorlagen speichern.  Siehe [Berichtsdaten konfigurieren](/help/analyze/legacy-report-builder/data-requests/configuring-report-dates/custom-calendar.md).

1. **Granularität anwenden**: Hier wird der Detailgrad für die zeitliche Auflösung des Berichts angegeben. Siehe [Granularität](/help/analyze/legacy-report-builder/data-requests/configuring-report-dates/granularity.md).

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
