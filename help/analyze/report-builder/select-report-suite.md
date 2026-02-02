---
title: Report Suite in Report Builder auswählen
description: Erfahren Sie, wie Sie eine Report Suite in Report Builder auswählen.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: 96e24d5d-78fb-4e5c-8513-c5fe221d0aeb
source-git-commit: 6f7de360ac24261eabb46c6cfce99449261706de
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 1%

---

# Report Suite auswählen

Sie können eine Report Suite aus dem Dropdown-Menü auswählen oder eine Report Suite aus einer Zelle auswählen und Ihren Datenblock automatisch mit einer neuen Report Suite aktualisieren.

## Report Suite aus einer Zelle auswählen

Wenn Sie eine Report Suite aus einer Zelle auswählen, können Sie Datenblöcke einfach mit verschiedenen Report Suites aktualisieren. Anstatt völlig neue Berichte mit separaten Datenblöcken zu erstellen, können Sie Datenblöcke mit einer Report Suite aktualisieren, die aus einer Zelle ausgewählt wurde.

Die Auswahl einer Report Suite aus einer Zelle ist bei folgenden Aufgaben hilfreich:

* Mehrere Report Suites, die sich in ihrer Struktur ähnlich oder identisch sind.
* Komplizierte Datenblockformate, die benutzerdefinierte Komponenten und Layouts enthalten.

Um eine Report Suite aus einer Zelle auszuwählen, erstellen Sie zunächst einen Datenblock und weisen Sie einer Zelle außerhalb Ihres Datenblocks mehrere Report Suites zu. Verwenden Sie dann das Bedienfeld **[!UICONTROL Report Suite aus Zelle]**, um Ihre Datenblöcke aus verschiedenen Report Suites zu aktualisieren.

1. Erstellen Sie einen Datenblock. Informationen zum Erstellen eines Datenblocks finden Sie unter [Erstellen eines Datenblocks](/help/analyze/report-builder/create-a-data-block.md).

1. Wählen Sie ![DataViewSelector](/help/assets/icons/DataViewSelector.svg) in **[!UICONTROL Report Suites]** aus.

1. Wählen Sie mit ![DataBlockSelector](/help/assets/icons/DataBlockSelector.svg) eine Zelle außerhalb des Datenblocks aus.

1. Fügen Sie eine oder mehrere Report Suites aus der **[!UICONTROL Wählen Sie Report Suites aus, die der Report Suite aus der Zelle hinzugefügt werden sollen]** per Drag-and-Drop hinzu. Alternativ können Sie eine Report Suite doppelt auswählen, um die Report Suite zur Liste **[!UICONTROL Enthaltene Report Suites“]**.

   * Sie können ![Suche](/help/assets/icons/Search.svg) **[!UICONTROL _Report Suites auswählen_]** verwenden, um nach Report Suites zu suchen.
   * Verwenden Sie ![MehrKlein](/help/assets/icons/MoreSmall.svg), um ein Kontextmenü zu öffnen, in dem Sie Report Suites in der Liste **[!UICONTROL Enthaltene Report Suites“ nach oben]** unten verschieben können.
   * Verwenden Sie ![CrossSize](/help/assets/icons/CrossSize75.svg), um eine Report Suite aus der Liste **[!UICONTROL Enthaltene Report Suites]** zu löschen.

   ![Report Suite aus einer Zelle auswählen](assets/dataviews-from-a-cell.png){zoomable="yes"}

1. Wählen Sie **[!UICONTROL Anwenden]** aus, um die ausgewählten Report Suites auf die ausgewählte Zelle anzuwenden.


## Ändern der Report Suite aus einer Zelle

1. Wählen Sie die Report Suite-Zellenposition in Ihrem Blatt aus.
1. Wählen Sie im Report Builder-Hub den Link **[!UICONTROL Report Suites aus Zelle]** in **[!UICONTROL Schnellbearbeitung]**.
1. Wählen Sie eine Report Suite aus dem Dropdown **[!UICONTROL Menü]** Report Suite“.

   ![Report Suite aus einer Zelle ändern](assets/change-data-view-from-cell.png){zoomable="yes"}
1. Optional: Wählen Sie **[!UICONTROL Datenblock/Datenblöcke bei Änderung aktualisieren]**.

1. Wählen Sie **[!UICONTROL Anwenden]** aus. Report Builder aktualisiert den Datenblock basierend auf der ausgewählten Report Suite.
