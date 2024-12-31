---
description: Virtual Report Suites können so zusammengestellt werden, dass Komponenten in Analysis Workspace aufgenommen oder aus Analysis Workspace entfernt werden.
title: Kuratierung von Komponenten der Virtual Report Suite
feature: VRS
exl-id: 19163829-328a-4064-b1be-8c09d1d94a0d
source-git-commit: 93099d36a65ca2bf16fbd6342f01bfecdc8c798e
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 94%

---

# Kuratierung von Komponenten der Virtual Report Suite

Virtual Report Suites können so zusammengestellt werden, dass Komponenten in Analysis Workspace aufgenommen oder aus Analysis Workspace entfernt werden.

Hier finden Sie ein Video zur Kuratierung von Komponenten:

>[!VIDEO](https://video.tv.adobe.com/v/23544/?quality=12)

>[!NOTE]
>
>Die Änderungen betreffen die Komponenten, die Admins und Benutzende ohne diese Rolle in kuratierten Workspace-Projekten und kuratierten Virtual Report Suites anzeigen können. Vor dieser Änderung konnten alle Benutzer nichtkuratierte Komponenten anzeigen, und zwar durch Klicken auf **[!UICONTROL Alle Komponenten anzeigen]**. Die [aktualisierte Kuratierungserfahrung](/help/analyze/analysis-workspace/curate-share/curate.md) bietet umfassendere Möglichkeiten, festzulegen, welche Komponenten sichtbar sind.

So ermöglichen Sie die Kuratierung von Komponenten:

1. Navigieren Sie **[!UICONTROL Analytics]** > **[!UICONTROL Komponenten]** > **[!UICONTROL Virtual Report Suites]** > **[!UICONTROL Neue Virtual Report Suite erstellen]**.
1. Wenn Sie die **[!UICONTROL Einstellungen]** festgelegt haben, klicken Sie auf die Registerkarte **[!UICONTROL Komponenten]**.

1. Aktivieren Sie das Kontrollkästchen **[!UICONTROL Anpassung der Virtual Report Suite-Komponenten aktivieren]**:

   ![](assets/vrs-enable.png)

   >[!NOTE]
   >
   >Bei Aktivierung der Komponentenanpassung ist die Virtual Report Suite **nur über Analysis Workspace** zugänglich, nicht aber über Folgendes:
   >
   >* [!UICONTROL Data Warehouse]
   >* [!UICONTROL Report Builder]
   >* [!UICONTROL Activity Map]
   >* Analytics-Reporting-API

   Nach der Aktivierung können Sie die in die Virtual Report Suite einzubeziehenden Komponenten hinzufügen, indem Sie die betreffenden Komponenten aus der Spalte „ausgeschlossene Komponenten“ in die Spalte „eingeschlossene Komponenten“ ziehen. Die ein- und ausschließbaren Komponenten lauten wie folgt:

   * Dimensionen
   * Metriken
   * Segmente
   * Datumsbereiche

   >[!NOTE]
   >
   >Kuratierte Komponenten (Segmente, berechnete Metriken, Datumsbereiche) müssen nicht *freigegeben* werden. Für die Virtual Report Suite kuratierte Komponenten sind in Analysis Workspace stets sichtbar, auch wenn sie nicht freigegeben werden.

1. Zudem können Sie die Komponenten filtern oder suchen und die gesamte gefilterte Auswahl der Spalte der eingeschlossenen Elemente hinzufügen, indem Sie auf **[!UICONTROL Alle hinzufügen klicken]**.

   ![](assets/vrs-add-all.png)

## Umbenannte Komponenten {#section_0F7CD9F684FE4765BC00A2AFED56550E}

Sie können die Anzeigenamen eingeschlossener Komponenten je nach Virtual Report Suite ändern. Wenn Sie beispielsweise den Seitennamen in die Virtual Report Suite einschließen möchten, er jedoch in einen Mobilgeräte-tauglicheren Kontext umbenannt werden soll, können Sie ihn in App-Bildschirme ändern. Der neue Name wird immer dann in Analysis Workspace angezeigt, wenn diese Virtual Report Suite verwendet wird.

![](assets/vrs-rename-component.png)

Klicken Sie in Analysis Workspace auf das Informationssymbol für eine beliebige eingeschlossene Komponente, um den ursprünglichen Namen der umbenannten Komponente anzuzeigen:

![](assets/vrs-aw-renamed.png)

## Komponentengruppen {#section_483BEC76F49E46ADAAA03F0A12E48426}

Mithilfe von Komponentengruppen können Sie Ihrer Virtual Report Suite stapelweise Komponenten hinzufügen. Wenn Sie beispielsweise einen Standardsatz mit spezifischen Komponenten für die Mobile-App-Analyse importieren möchten, wählen Sie die Mobile-App-Gruppe aus. Daraufhin wird der Liste „Eingeschlossen“ der Virtual Report Suite automatisch ein entsprechender Satz mit Dimensionen und Metriken (bereits umbenannt) hinzugefügt.

![](assets/vrs-comp-grp.png)

## Workspace-Verhalten {#section_6C32F8B642804C0097FCB14E21028D4A}

Weitere Informationen zum Kuratieren in Analysis Workspace finden Sie unter [Kuratieren und Freigeben von Projekten](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/curate.html?lang=de).
