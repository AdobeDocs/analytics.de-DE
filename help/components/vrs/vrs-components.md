---
description: Virtual Report Suites können so kuratiert werden, dass Komponenten in Analysis Workspace ein- und ausgeschlossen werden.
title: Kuratierung von Komponenten der Virtual Report Suite
feature: VRS
exl-id: 19163829-328a-4064-b1be-8c09d1d94a0d
TQID: https://experienceleague.adobe.com/j86dD5Yzd6GIoQOzhHsU8YbShQiODtbU8aCdM3UxRMg
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b0ca67c6-0a35-482c-ad91-baac1bcb26d6id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: ac8a38fa-dec3-4581-8f64-178fde9f64e8id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: c4cb071e-4667-4fb1-b1f1-d8994549cfb2id: ef60b66e-5984-4336-ba72-6d978b1b6f87id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 434
ht-degree: 44%

---

# Kuratierung von Komponenten der Virtual Report Suite

Virtual Report Suites können so kuratiert werden, dass Komponenten in Analysis Workspace ein- und ausgeschlossen werden.


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Komponentenkuratierung](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/components/virtual-report-suites/component-curation-in-virtual-report-suites){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]


>[!NOTE]
>
>Die Änderungen betreffen die Komponenten, die Admins und Benutzende ohne diese Rolle in kuratierten Workspace-Projekten und kuratierten Virtual Report Suites anzeigen können. Vor dieser Änderung konnten alle Benutzer nichtkuratierte Komponenten anzeigen, und zwar durch Klicken auf **[!UICONTROL Alle Komponenten anzeigen]**. Das [aktualisierte Kuratierungserlebnis](/help/analyze/analysis-workspace/curate-share/curate.md) ermöglicht eine detailliertere Kontrolle darüber, welche Komponenten sichtbar sind.

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

   Wenn diese Option aktiviert ist, können Sie die Komponenten hinzufügen, die in die Virtual Report Suite aufgenommen werden sollen, indem Sie die entsprechenden Komponenten aus der Spalte „Ausgeschlossene Komponenten“ in die Spalte „Enthaltene Komponenten“ ziehen. Die Komponenten, die ein- und ausgeschlossen werden können, sind:

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

Sie können die Anzeigenamen der enthaltenen Komponenten ändern, die für die Virtual Report Suite spezifisch sind. Wenn Sie beispielsweise den Seitennamen in die Virtual Report Suite einbeziehen, ihn jedoch in einen mobileren Kontext umbenennen möchten, können Sie ihn in App Screens ändern. Der neue Name wird in Analysis Workspace angezeigt, wenn diese Virtual Report Suite verwendet wird.

![](assets/vrs-rename-component.png)

Klicken Sie in Analysis Workspace für eine beliebige enthaltene Komponente auf das Informationssymbol, um den Originalnamen der umbenannten Komponente anzuzeigen:

![](assets/vrs-aw-renamed.png)

## Komponentengruppen {#section_483BEC76F49E46ADAAA03F0A12E48426}

Verwenden Sie Komponentengruppen, um Ihrer Virtual Report Suite Massenkomponenten hinzuzufügen. Wenn Sie beispielsweise einen Standardsatz mit spezifischen Komponenten für die Mobile-App-Analyse importieren möchten, wählen Sie die Mobile-App-Gruppe aus. Ein entsprechender Satz von Dimensionen und Metriken (bereits umbenannt) wird automatisch zur Liste „Virtual Report Suite Included“ hinzugefügt.

![](assets/vrs-comp-grp.png)

## Workspace-Verhalten {#section_6C32F8B642804C0097FCB14E21028D4A}

Weitere Informationen zum Kuratieren in Analysis Workspace finden Sie unter [Kuratieren und Freigeben von Projekten](/help/analyze/analysis-workspace/curate-share/curate.md).
