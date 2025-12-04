---
title: Erstellen und Bearbeiten von Klassifizierungskonsolidierungen
description: Erläutert, wie Klassifizierungskonsolidierungen erstellt, validiert, ausgeführt, genehmigt und abgebrochen werden.
exl-id: f36bcbcb-0ed0-44a7-a6a9-b28fd244fb27
feature: Classifications
source-git-commit: cabddc619e0d2ddaba6b232eb4d72c60301f76bb
workflow-type: tm+mt
source-wordcount: '982'
ht-degree: 1%

---

# Erstellen und Bearbeiten von Klassifizierungskonsolidierungen

Eine Konsolidierung von Klassifizierungssätzen ermöglicht es Ihnen, Klassifizierungen aus mehreren Klassifizierungssätzen zu nehmen und zu einem zusammenzufassen. Verwenden Sie diese Schnittstelle, um eine Klassifizierungssatz-Konsolidierung von Anfang bis Ende zu erstellen. Diese Benutzeroberfläche ist besonders nützlich für Unternehmen, die von alten Klassifizierungen zu Klassifizierungssätzen wechseln. Organisationen, die Klassifizierungssätze verwenden, müssen diesen Konsolidierungs-Workflow bereits nicht verwenden.

## Erstellen einer Konsolidierung {#create-a-consolidation}


>[!CONTEXTUALHELP]
>id="classificationsets_consolidation_setpriority"
>title="Priorität des Klassifizierungssatzes"
>abstract="Der ![Schlüssel](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Key_18_N.svg) *Klassifizierungssatz* ist der Basisklassifizierungssatz und definiert das Gesamtschema und hat bei Zusammenführungskonflikten Vorrang. Die anderen Klassifizierungssätze werden in der Reihenfolge von oben nach unten angewendet."


So erstellen Sie eine Klassifizierungskonsolidierung in der Adobe Analytics-Hauptbenutzeroberfläche:

1. Wählen **[!UICONTROL Klassifizierungssätze]** im Menü **[!UICONTROL Komponenten]** aus.
1. Wählen **[!UICONTROL Manager „Klassifizierungssätze]** die Registerkarte **[!UICONTROL Konsolidierungen]** aus.
1. Wählen Sie im **[!UICONTROL Classification Sets - Konsolidierungen]** Manager ![Kreis hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Neu]**.
1. Im **[!UICONTROL Neue Konsolidierung]** Dialogfeld

   ![Klassifizierungssätze - Neue Konsolidierung](assets/classifications-sets-consolidations-new.png)
   1. Geben Sie einen &quot;**[!UICONTROL &quot;]**. Beispiel: `Consolidation Example`.
   1. Geben Sie eine **[!UICONTROL Beschreibung (optional)]** ein. Zum Beispiel `Example classification set`.
   1. Geben Sie eine oder mehrere E-Mail-Adressen (durch Kommata getrennt) in **[!UICONTROL Bei Problemen]**. Diese Benutzer erhalten bei Problemen eine E-Mail-Benachrichtigung.
   1. Wählen Sie einen Klassifizierungssatz aus dem Dropdown **[!UICONTROL Menü „Klassifizierungssatz]** Übereinstimmung“ aus.

      Die linke Liste **[!UICONTROL Source]** Klassifizierungssatz“ enthält Klassifizierungssätze, die der ausgewählten Klassifizierungsliste ähnlich sind und für die Konsolidierung verfügbar sind. Die rechte Liste wird automatisch mit dem ausgewählten Klassifizierungssatz ![Schlüssel](/help/assets/icons/Key.svg) gefüllt. Dieser Basissatz definiert das Gesamtschema und hat bei Zusammenführungskonflikten immer Vorrang.

   1. Wählen Sie die Klassifizierungssätze, die Sie in der linken Liste zusammenfassen möchten, und legen Sie die ausgewählten Sätze in der rechten Liste unter dem ausgewählten ![Schlüssel](/help/assets/icons/Key.svg) Basis-**[!UICONTROL _Klassifizierungssatz_]** ab.

      Die zusätzlichen Klassifizierungssätze werden bei der Konsolidierung in aufsteigender Reihenfolge konsolidiert. Wenn ein Schlüssel in mehreren zusätzlichen Sätzen vorhanden ist, wird der Wert für den Schlüssel aus dem obersten Klassifizierungssatz genommen. Wenn sowohl im Basissatz ![Schlüssel](/help/assets/icons/Key.svg) als auch in einem zusätzlichen Satz ein Schlüssel vorhanden ist, wird der Wert aus dem Basissatz verwendet.

      Um zu verwalten, welche Werte für Schlüssel verwendet werden, verschieben Sie einzelne und ausgewählte Klassifizierungssätze in der Liste per Drag-and-Drop. Sie können den Klassifizierungssatz ![Schlüssel](/help/assets/icons/Key.svg) **[!UICONTROL _auch_]** einen ausgewählten Klassifizierungssatz durch Drag-and-Drop ersetzen.

   1. Wählen Sie **[!UICONTROL Speichern]**, um die Klassifizierungskonsolidierung zu speichern. Wählen Sie zum Abbrechen **[!UICONTROL Abbrechen]** aus.

Nach dem Speichern wird eine Klassifizierungskonsolidierung automatisch für die Konsolidierung validiert. Diese Validierung stellt sicher, dass jeder einzelne Klassifizierungssatz für diese Konsolidierung gültig ist. Nach erfolgreicher Ausführung zeigt der Eintrag in der Konsolidierungsliste für Klassifizierungen den Status **[!UICONTROL Validiert]**.

Nachdem Sie eine Konsolidierung erstellt haben, sind die nächsten Schritte:

* [Überprüfen Sie &#x200B;](#re-validate) Klassifizierungskonsolidierung erneut, wenn Sie Änderungen an der ursprünglichen Konfiguration vorgenommen haben.
* [Ausführen](#run) der Klassifizierungskonsolidierung.
* [Genehmigen](#approve) die Klassifizierungskonsolidierung.



<!--
         
  

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Consolidations]** > **[!UICONTROL Add]**

The following fields are available when creating a consolidation:

* **[!UICONTROL Name]**: The name of the consolidation.
* **[!UICONTROL Notify of issues]**: A comma-delimited list of email addresses that are notified of issues with this consolidation.
* **[!UICONTROL Dataset to match]**: A drop-down list of all classification sets.

Once you select a classification set, a table with two columns appears:

* The right column contains all classification sets that you want to consolidate. It starts with the classification set selected using the above drop-down list.
* The left column contains all classification sets eligible to be merged with the originally selected dataset. **Schemas must exactly match to be eligible for consolidation**. If schemas do not match the selected classification set, they do not appear in this left column.

Drag the desired classification sets from the available column on the left to the consolidation column on the right. Once the consolidation is given a name and two or more classification sets are in the right column, click **[!UICONTROL Save & Continue]**.

-->

## Bearbeiten einer Konsolidierung

So bearbeiten Sie eine Klassifizierungskonsolidierung in der Adobe Analytics-Hauptbenutzeroberfläche:

1. Wählen **[!UICONTROL Klassifizierungssätze]** im Menü **[!UICONTROL Komponenten]** aus.
1. Wählen **[!UICONTROL Manager „Klassifizierungssätze]** die Registerkarte **[!UICONTROL Konsolidierungen]** aus.
1. Im **[!UICONTROL Konsolidierungs-Manager für Klassifizierungssätze]**:
   1. Wählen Sie den Namen Ihrer Klassifizierungskonsolidierung aus. Das **[!UICONTROL Konsolidierung: _Klassifizierungskonsolidierungsname_]**&#x200B;wird angezeigt. Das Erscheinungsbild und die verfügbaren Aktionen hängen vom aktuellen Status der Konsolidierung ab und davon, ob Sie noch die Möglichkeit haben, die Klassifizierungskonsolidierung zu ändern.

      | Verfügbare Aktionen | Beschreibung |
      |---|---|
      | ![Abbrechen](/help/assets/icons/Cancel.svg) **[!UICONTROL Abbrechen]** | [Konsolidierung abbrechen](#cancel). |
      | ![Häkchen](/help/assets/icons/Checkmark.svg) **[!UICONTROL Erneut überprüfen]** | [Validieren Sie die Konsolidierung erneut](#re-validate). |
      | ![play](/help/assets/icons/Play.svg) **[!UICONTROL run]** | [Konsolidierung ausführen](#run). |
      | ![ThumbUp](/help/assets/icons/ThumbUp.svg) **[!UICONTROL Approve]** | [Validieren Sie die Konsolidierung](#approve). |



### Erneut validieren

Sie können eine Klassifizierungskonsolidierung im Dialogfeld Konsolidierung: Klassifizierungskonsolidierung erneut überprüfen. Ein ![Warnhinweis](/help/assets/icons/Alert.svg) kann zusätzliche Informationen zu Problemen bei Ihrer Konsolidierung bereitstellen, die eine Neukonfiguration der Konsolidierung erfordern.

![Klassifizierungssätze - Konsolidierung erneut überprüfen](assets/classifications-sets-consolidations-validated.png)

So validieren Sie die Klassifizierungskonsolidierung erneut:

1. Konfigurieren Sie die Konsolidierung erneut mit derselben Drag-and-Drop-Oberfläche, die Sie zum Erstellen der Konsolidierung verwendet haben.
1. Wählen ![Häkchen](/help/assets/icons/Checkmark.svg) **[!UICONTROL Erneut überprüfen]** aus. Die Validierung stellt sicher, dass jeder einzelne Klassifizierungssatz für diese Konsolidierung gültig ist. Bei Erfolg wird eine Popup-Meldung angezeigt: ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg) **[!UICONTROL Erfolgreich gesendete Konsolidierung zur Validierung!]**
1. Wählen Sie ![CrossSize400](/help/assets/icons/CrossSize400.svg) aus, um das Dialogfeld zu schließen. Oder wählen Sie ![Play](/help/assets/icons/Play.svg) **[!UICONTROL Run]**, um die Konsolidierung auszuführen, oder ![Cancel](/help/assets/icons/Cancel.svg) **[!UICONTROL Cancel]**, um die Klassifizierung abzubrechen.



<!--
Once you have created a consolidation, a list of source datasets appears on the right. The **[!UICONTROL Validate]** button makes sure that each individual classification set is valid for this consolidation. You can reorder the classification steps here to determine priority in cases of mismatched classification values. **The highest classification set in the list overwrites any mismatched values in other classification sets.**

-->

### Ausführen

Nachdem eine Klassifizierungskonsolidierung erfolgreich validiert wurde, können Sie die Konsolidierung ausführen.

So führen Sie eine Klassifizierungskonsolidierung durch:

1. Wählen Sie ![Play](/help/assets/icons/Play.svg) **[!UICONTROL run]** aus. Eine Popup-Meldung wird angezeigt ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg) **[!UICONTROL Erfolgreich gesendete Konsolidierung zur Verarbeitung!]**
1. Wählen Sie ![CrossSize400](/help/assets/icons/CrossSize400.svg) aus, um das Dialogfeld zu schließen.


### Genehmigen {#approve}


>[!CONTEXTUALHELP]
>id="classificationsets_consolidations_mismatch"
>title="Keine Übereinstimmung"
>abstract="Der Prozentsatz der nicht übereinstimmenden Schlüssel, wenn der Wert im konsolidierten Klassifizierungssatz nicht mit dem Quellklassifizierungssatz übereinstimmt."

>[!CONTEXTUALHELP]
>id="classificationsets_consolidations_absent"
>title="Abwesend"
>abstract="Der Prozentsatz der Schlüssel im konsolidierten Klassifizierungssatz, aber nicht im Quellklassifizierungssatz."

Sobald eine Klassifizierungskonsolidierung erfolgreich ausgeführt wurde, lautet der Konsolidierungsstatus ![StatusOrange](/help/assets/icons/StatusOrange.svg) **[!UICONTROL Wartet auf Genehmigung]**. Die Genehmigung einer Klassifizierungskonsolidierung ersetzt die einzelnen Klassifizierungssätze durch den konsolidierten Klassifizierungssatz und die einzelnen Klassifizierungssätze werden entfernt.

![Klassifizierungssätze - Konsolidierung wartet auf Genehmigung](assets/classifications-sets-consolidations-waitingforapproval.png)

So validieren Sie einen Klassifizierungssatz:

1. Verwenden Sie die **[!UICONTROL Ähnlichkeitsberichte]**, um die Konsolidierung zu überprüfen. Dieser Bericht zeigt eine Tabelle mit den folgenden Spalten:

   * **[!UICONTROL Name des Klassifizierungssatzes]**: Der Name des Klassifizierungssatzes.
   * **[!UICONTROL Nicht]**: Der Prozentsatz der Zeilen, in denen die Schlüsselwerte nicht mit dem Quellklassifizierungssatz übereinstimmen. Wenn der Prozentsatz der Nicht-Übereinstimmung hoch ist, kann die Nicht-Übereinstimmung ein Hinweis darauf sein, dass die Klassifizierungsdaten zu unterschiedlich sind. Überprüfen Sie, ob die ausgewählten Klassifizierungssätze ähnliche Klassifizierungsdaten aufweisen.
   * **[!UICONTROL Absent]**: Der Prozentsatz der Zeilen, in denen sich Schlüsselwerte im Klassifizierungssatz ![Schlüssel](/help/assets/icons/Key.svg), aber nicht im Quellklassifizierungssatz befinden. Alle fehlenden Zeilen werden dem konsolidierten Klassifizierungssatz hinzugefügt.

1. Wenn die Klassifizierungskonsolidierung zur Genehmigung bereit ist, wählen Sie ![Häkchen](/help/assets/icons/Checkmark.svg) **[!UICONTROL Genehmigen]**. Eine **[!UICONTROL Konsolidierung genehmigen?]** Dialogfeld fordert Sie zur Bestätigung auf. Wählen **[!UICONTROL Genehmigen]**, um die Konsolidierung zu genehmigen. Wählen Sie zum Abbrechen **[!UICONTROL Abbrechen]** aus.

Nach der Genehmigung wird der konsolidierte Klassifizierungssatz erstellt. Der Status ist auf &quot;**[!UICONTROL &quot;]**.


### Abbrechen

Sie können eine Klassifizierungskonsolidierung vor der Genehmigung abbrechen.

So brechen Sie eine Klassifizierungskonsolidierung ab:

1. Wählen Sie **[!UICONTROL Abbrechen]** aus.

   Eine Konsolidierung kann nach Abbruch der Konsolidierung nicht mehr fortgesetzt werden.
1. Wählen Sie **[!UICONTROL Konsolidierung abbrechen]**, um die Konsolidierung abzubrechen. Wählen Sie **[!UICONTROL Zurück]**, um den Abbruch rückgängig zu machen.
