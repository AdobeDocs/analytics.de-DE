---
title: Erstellen und Bearbeiten von Klassifizierungssätzen
description: Erfahren Sie, wie Sie in Adobe Analytics Klassifizierungssätze erstellen und bearbeiten, einschließlich Primär- und Lookup-Klassifizierungstypen, Abonnements und Auftragsbenachrichtigungen.
exl-id: 6d692d90-8cc7-4306-a780-58d03db45be8
feature: Classifications
source-git-commit: 9feefd318d5239812f62afd727836e8aa203a4b2
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 2%

---

# Erstellen und Bearbeiten von Klassifizierungssätzen

Über [&#x200B; Manager für Klassifizierungssätze &#x200B;](#create-a-classification-set) Sie [&#x200B; Klassifizierungssätze erstellen und &#x200B;](#edit-a-classification-set) bearbeiten.

## Erstellen eines Klassifizierungssatzes

So erstellen Sie einen Klassifizierungssatz:

1. Wählen Sie **[!UICONTROL Komponenten]** in der oberen Menüleiste von Adobe Analytics aus und wählen Sie dann **[!UICONTROL Klassifizierungssätze]**.
1. Wählen **[!UICONTROL unter]** die Registerkarte **[!UICONTROL Klassifizierungssätze]** aus.
1. Wählen Sie ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL New]**.
1. Im Dialogfeld **[!UICONTROL Neuen Klassifizierungssatz hinzufügen]**:

   ![Klassifizierungssätze - Neuen Klassifizierungssatz hinzufügen](assets/classifications-sets-new.png)

   1. Geben Sie einen &quot;**[!UICONTROL &quot;]**. Beispiel: `Classification Set Example`.
   1. Geben Sie eine **[!UICONTROL Beschreibung (optional)]** ein. Zum Beispiel `Example classification set`.
   1. Wählen Sie **[!UICONTROL Klassifizierungssatz]** Typ“ aus. Mögliche Typen sind:
      * **[!UICONTROL Primär]**. Ein primärer Klassifizierungssatz gilt für Dimensionen, die in Adobe Analytics erfasst wurden. Primäre Klassifizierungen sind eine Möglichkeit, granulare Dimensionswerte in aussagekräftigere Datenebenen zu gruppieren (klassifizieren). Beispielsweise können Sie interne Suchbegriffe in internen Suchkategorien gruppieren, um Designs in Ihren Suchdaten zu verstehen. Oder klassifizieren Sie Produkt-SKUs nach Farbe oder Kategorie.
      * **[!UICONTROL Suche]**. Eine Lookup-Tabelle wird häufig als untergeordnete Klassifizierung oder Unterklassifizierung bezeichnet und ist eine Klassifizierung einer primären Klassifizierung. Bei einer Suche handelt es sich um Metadaten über einen Klassifizierungswert und nicht um die ursprüngliche Dimension. Beispielsweise könnte eine Dimension *Produkt* über eine primäre Classification mit *Farbcode* verfügen. Eine Lookup-Tabelle mit *Farbname* kann dann an den *Farbcode“ angehängt werden* um jeden Farbcode zu erklären.
1. Wählen **[!UICONTROL im Abschnitt]** Auftragsbenachrichtigungen“ aus, wen Sie über einen Fehler oder Erfolg der Klassifizierungssatz-Aufträge benachrichtigen möchten.
   * So benachrichtigen Sie Benutzer über einen Fehler:
      1. Aktivieren **[!UICONTROL Bei Fehler benachrichtigen]**.
      1. Geben Sie unter „E-Mail-Empfänger mit **[!UICONTROL &quot; eine oder mehrere kommagetrennte E-Mail-Adressen]**.
   * So benachrichtigen Sie Benutzer über den Erfolg:
      1. Aktivieren Sie **[!UICONTROL Bei Erfolg benachrichtigen]**.
      1. Geben Sie unter „E-Mail-Empfänger mit **[!UICONTROL &quot; mindestens eine kommagetrennte E-Mail-Adresse]**.
1. Geben **[!UICONTROL im Abschnitt]** Abonnements“, falls Sie **[!UICONTROL Primär]** ausgewählt haben, ein oder mehrere &quot;**[!UICONTROL &quot;]**.  Sie können mehrere **[!UICONTROL Report Suite]**- und **[!UICONTROL Dimension]**-Kombinationen zu einem Klassifizierungssatz definieren.

   * Wählen Sie ![CrossSize400](/help/assets/icons/CrossSize400.svg) aus, um eine Kombination **[!UICONTROL Report Suite]** und **[!UICONTROL Key Dimension]** zu löschen.

   Wenn Sie eine Kombination aus **[!UICONTROL Report Suite]** und **[!UICONTROL Key Dimension]** hinzufügen, die bereits in einem anderen Klassifizierungssatz vorhanden ist, wird eine rote Meldung angezeigt.
Sie haben folgende Möglichkeiten:
   * Wählen Sie **[!UICONTROL Zu vorhandenem hinzufügen]** aus, um den anderen Klassifizierungssatz zu öffnen und [Klassifizierungen zum Schema hinzufügen](manage/schema.md) für diesen anderen Klassifizierungssatz.
   * Ändern Sie **[!UICONTROL Report Suite]** und **[!UICONTROL Key Dimension]** in eine Kombination, die noch nicht für einen anderen Klassifizierungssatz abonniert wurde.
1. Wählen **[!UICONTROL Speichern]**, um den Klassifizierungssatz zu speichern. Wählen Sie **[!UICONTROL Abbrechen]**, um die Definition aufzuheben.

Um das Schema für den Klassifizierungssatz zu definieren, wählen Sie den neu erstellten Klassifizierungssatz aus dem Manager **[!UICONTROL Klassifizierungssätze]** aus, um [Klassifizierungssatz zu bearbeiten](#edit-a-classification-set).


## Bearbeiten eines Klassifizierungssatzes

So bearbeiten Sie einen Klassifizierungssatz:

1. Wählen Sie **[!UICONTROL Komponenten]** in der oberen Menüleiste von Adobe Analytics aus und wählen Sie dann **[!UICONTROL Klassifizierungssätze]**.
1. Wählen **[!UICONTROL unter]** die Registerkarte **[!UICONTROL Klassifizierungssätze]** aus.
1. Wählen Sie den Namen Ihres Klassifizierungssatzes aus.
1. Im Dialogfeld **[!UICONTROL Klassifizierungssatz: _Klassifizierungssatzname_]**&#x200B;können Sie die [Einstellungen](manage/settings.md) und das [Schema](manage/schema.md) für den Klassifizierungssatz definieren.
1. Klicken Sie abschließend auf **[!UICONTROL Speichern]**, um Ihre Änderungen zu speichern. Wählen Sie zum Abbrechen **[!UICONTROL Abbrechen]** aus.
