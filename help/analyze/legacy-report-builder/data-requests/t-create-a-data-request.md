---
description: Schritte zum Erstellen einer grundlegenden Report Builder-Datenanforderung.
title: Datenanforderung erstellen
feature: Report Builder
role: User, Admin
exl-id: 21d552a0-7a58-4217-ba8a-7c87eb4757f6
TQID: https://experienceleague.adobe.com/w-oiIfs1qFMoQbaN8YrNIn1TRNHeN97lQOlkLeXdLb0
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 284
ht-degree: 50%

---

# Report Builder-Datenanforderung erstellen

{{legacy-arb}}

Schritte zum Erstellen einer grundlegenden Datenanforderung.

1. Klicken Sie in Excel auf **[!UICONTROL Erstellen]**.
1. Wählen Sie im Fenster [!UICONTROL Anforderungs-Assistent: Schritt 1] eine [Report Suite](/help/analyze/legacy-report-builder/data-requests/selecting-report-suites/t-select-report-suites.md).
1. (Optional) Wählen Sie ein Segment, auf das Sie die Anforderung anwenden möchten. Wenn Sie eines oder mehrere Segmente ausgewählt haben, werden diese an den Anfang der Liste verschoben.

   Report Builder verwendet Segmente auf dieselbe Weise wie Adobe Analytics. Weitere Informationen finden Sie im [Analytics-Segmentierungshandbuch](/help/components/segmentation/seg-home.md).
1. Wählen Sie einen [Berichtstyp](/help/analyze/legacy-report-builder/data-requests/c-report-types/select-report-types.md) aus.
1. Definieren Sie einen [Datumsbereich](/help/analyze/legacy-report-builder/data-requests/configuring-report-dates/custom-calendar.md) und eine [Granularität](/help/analyze/legacy-report-builder/data-requests/configuring-report-dates/granularity.md) für den Bericht.
1. Klicken Sie auf **[!UICONTROL Weiter]**.
1. Geben Sie im Fenster [Layout – Anforderungs-Assistent: Schritt 2](/help/analyze/legacy-report-builder/layout/layout.md) ein Layout an:

   | Element | Beschreibung |
   |---|---|
   | Pivot-Layout | Stellt ein Zeilen-, Spalten- und Metrikraster für das Layout bereit, das den standardmäßigen Excel-Tabellen ähnelt. Mit diesem Layout können Sie Aufschlüsselungsanfragen innerhalb einer ursprünglichen Anfrage hinzufügen. |
   | Benutzerdefiniertes Layout | Bietet den Großteil der Funktionalität des [!UICONTROL Pivot-Layouts] ermöglicht jedoch die Auswahl, wo jedes Element im Raster in der Tabelle platziert werden soll. Dieses Layout bietet die Flexibilität, die in früheren Versionen verfügbar war. |

1. Doppelklicken Sie auf der Registerkarte [!UICONTROL Metriken] auf Metriken, um sie dem Raster [!UICONTROL Metriken] hinzuzufügen (wahlweise können Sie die Metriken auch in das Raster ziehen).
1. Doppelklicken Sie auf der Registerkarte [!UICONTROL Dimensionen] auf Dimensionen, um sie dem Raster [!UICONTROL Zeilenbezeichnungen] hinzuzufügen.

   Die [Dimensionen](/help/analyze/report-builder/filter-dimensions.md) die in Schritt 2 verfügbar sind, hängen vom in Schritt 1 ausgewählten Basisbericht und von der Konfiguration Ihrer Report Suite ab. Die Dimensionen sind Elemente, die korrelieren, untergeordnete Beziehungen herstellen oder eine Klassifizierung der ursprünglichen Berichtsmetrik darstellen, die Sie im Fenster [!UICONTROL Anforderungs-Assistent: Schritt 1] ausgewählt haben. Durch Hinzufügen mehrerer Dimensionen in Schritt 2 wird eine Aufschlüsselung in Ihrer Datenanfrage erstellt.

   Weitere [ finden Sie unter ](/help/analyze/legacy-report-builder/layout/c-metrics-dimensions/t-add-metrics-and-dimensions.md) und Dimensionen hinzufügen .
