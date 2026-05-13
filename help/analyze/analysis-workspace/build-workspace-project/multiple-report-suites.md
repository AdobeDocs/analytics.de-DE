---
title: Mehrere Report Suites
description: Erfahren Sie, wie Sie mit mehreren Report Suites in einem Analysis Workspace-Projekt arbeiten.
feature: Workspace Basics
role: User, Admin
exl-id: 0429ddd9-935f-44ef-ae1e-97bb02e6e2df
TQID: https://experienceleague.adobe.com/IrWsvooPWqWmbDAD-70CgI71gEPJCQY-1wFHFyuJsyc
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2: id: a544b409-2610-410d-a842-474ac1d0d54eid: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: dcae653e-62c6-4cc8-84e6-ee110b848296id: e38cbddc-1633-4cd5-bed5-9f289f2a6029id: e93b8c4c-c5f7-45f8-9abe-9b710f53f502id: ef60b66e-5984-4336-ba72-6d978b1b6f87
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 455
ht-degree: 69%

---

# Mehrere Report Suites

Sie können in Analysis Workspace Projekte mit Daten aus mehr als einer Report Suite erstellen. Report Suites werden auf Bedienfeldebene ausgewählt, sodass Sie für jedes Bedienfeld innerhalb desselben Workspace-Projekts eine andere Report Suite auswählen können.

Diese Funktion ist nützlich, wenn Sie Folgendes tun möchten:

* Daten aus zwei verschiedenen Regionen vergleichen und sich die Daten in zwei verschiedenen Report Suites befinden. Sie können Tabellen und Visualisierungen erstellen, um die Daten nebeneinander zu vergleichen.

* ein Dashboard mit Metriken und Visualisierungen erstellen, um Berichte an andere Organisationen zu senden. Sie können Daten aus verschiedenen Report Suites in im selben Projekt abrufen.


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Mehrere Report Suites](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/analysis-workspace/using-panels/multiple-report-suites-in-analysis-workspace){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]


## Anwenden einer Report Suite auf alle Panels

Sie können eine Report Suite auf alle Bedienfelder gleichzeitig anwenden, indem Sie mit der rechten Maustaste auf eine beliebige Bedienfeldüberschrift klicken und **[!UICONTROL Report Suite auf alle Bedienfelder anwenden]** auswählen.

![](assets/apply-rs-all-panels.png)

## Aktives Bedienfeld

Sie erkennen das aktive Bedienfeld am hellblauen Rand. Wählen Sie einfach in einem Bedienfeld aus, um dieses Bedienfeld in das aktive Bedienfeld zu verwandeln.

>[!TIP]
>
>Sie können Objekte per Drag-and-Drop in ein beliebiges Bedienfeld ziehen, das sich in derselben Report Suite wie das aktive Bedienfeld befindet. Durch Ziehen eines Objekts in ein inaktives Bedienfled derselben Report Suite wird das Bedienfeld aktiv.
>

## Arbeiten mit mehreren Report Suites

![](assets/mrs-ui.png)

1. Erstellen Sie ein neues Projekt mit zwei oder mehr Bedienfeldern im Workspace.

1. Verschieben Sie Komponenten (Metriken, Dimensionen, Segmente, Datumsbereiche) per Drag &amp; Drop in den Bereich. Stellen Sie sicher, dass Bedienfelder über Daten und Visualisierungen verfügen, die für ihre Report Suite spezifisch sind.


   >[!NOTE]
   >
   >Manchmal wird beim Laden eines Projekts (oder beim Umschalten auf eine Report Suite) ein Banner angezeigt, wenn nicht alle Komponenten des Projekts in der Report Suite enthalten sind. Die fehlenden Komponenten werden aufgelistet. Befolgen Sie [diese Anweisungen](/help/admin/admin-console/permissions/product-profile.md), um Berechtigungen für die erforderlichen Metriken/Dimensionen festzulegen.
   >

   ![](assets/incompat-rs.png)

   Sie haben 3 Optionen, um mit dieser Inkompatibilität umzugehen:
   * Erforderliche Dimensionen/Metriken aktivieren.
   * Ändern Sie die Report Suite.
   * Fahren Sie mit einigen fehlenden Komponenten fort. Dies führt dazu, dass für diese Komponenten keine Daten verfügbar sind und/oder zu leeren Visualisierungen.

1. Wechseln Sie die Report Suite für das Bedienfeld und beobachten Sie, wie die Bezeichnung der Komponente (derzeit aktive Report Suite) und die aufgelisteten Komponenten basierend auf der neuen Report Suite aktualisiert werden.

1. Verwenden Sie eine Tastenkombination (`shift` während Sie ziehen), um einen inaktives Bedienfeld in ein aktives Bedienfeld umzuwandeln.

1. (Optional) Sie können auch andere Komponenten-Builder in Analytics aufrufen und sicherstellen, dass ihnen nun eine Report Suite-Bezeichnung angezeigt wird, die angibt

   * Wo ein Segment erstellt wird: [Segment Builder](/help/components/segmentation/segmentation-workflow/seg-build.md).
   * Wo eine berechnete Metrik erstellt wird: [Generator für berechnete ](/help/components/calculated-metrics/workflow/c-build-metrics/cm-build-metrics.md)).
   * Wo ein Warnhinweis erstellt wird: [Warnhinweiserstellung](/help/components/alerts/alert-builder.md).
