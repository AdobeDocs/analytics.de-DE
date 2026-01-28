---
title: Erstellen von Klassifizierungssätzen
description: Erfahren Sie, wie Sie verfügbare Felder und Beschreibungen beim Erstellen eines Klassifizierungssatzes erstellen können.
exl-id: 6d692d90-8cc7-4306-a780-58d03db45be8
feature: Classifications
source-git-commit: cfa8335008548254786e46dfe634229edad5bd54
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 3%

---

# Erstellen und Bearbeiten von Klassifizierungssätzen

Über [ Manager für Klassifizierungssätze ](#create-a-classification-set) Sie [ Klassifizierungssätze erstellen und ](#edit-a-classification-set) bearbeiten.

## Erstellen eines Klassifizierungssatzes

So erstellen Sie einen Klassifizierungssatz:

1. Wählen Sie **[!UICONTROL Komponenten]** in der oberen Menüleiste von Adobe Analytics aus und wählen Sie dann **[!UICONTROL Klassifizierungssätze]**.
1. Wählen **[!UICONTROL unter]** die Registerkarte **[!UICONTROL Klassifizierungssätze]** aus.
1. Wählen Sie ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL New]**.
1. Im Dialogfeld **[!UICONTROL Neuen Klassifizierungssatz hinzufügen]**:

   ![Klassifizierungssätze - Neuen Klassifizierungssatz hinzufügen](assets/classifications-sets-new.png)

   1. Geben Sie einen &quot;**[!UICONTROL &quot;]**. Beispiel: `Classification Set Example`.
   1. Geben Sie eine **[!UICONTROL Beschreibung (optional)]** ein. Zum Beispiel `Example classification set`.
   1. Geben Sie eine oder mehrere E-Mail-Adressen (durch Kommata getrennt) in **[!UICONTROL Bei Problemen]**. Diese Benutzer erhalten bei Problemen eine E-Mail-Benachrichtigung.
   1. Wählen Sie **[!UICONTROL Klassifizierungssatz]** Typ“ aus. Mögliche Typen sind:
      * **[!UICONTROL Primär]**. Ein primärer Klassifizierungssatz gilt für Dimensionen, die in Adobe Analytics erfasst wurden. Primäre Klassifizierungen sind eine Möglichkeit, granulare Dimensionswerte in aussagekräftigere Datenebenen zu gruppieren (klassifizieren). Beispielsweise können Sie interne Suchbegriffe in internen Suchkategorien gruppieren, um Designs in Ihren Suchdaten zu verstehen. Oder klassifizieren Sie Produkt-SKUs nach Farbe oder Kategorie.
         * Geben Sie ein oder mehrere **[!UICONTROL Abonnements]** ein.  Sie können mehrere **[!UICONTROL Report Suite]**- und **[!UICONTROL Dimension]**-Kombinationen zu einem Klassifizierungssatz definieren.

         * Wählen Sie ![CrossSize400](/help/assets/icons/CrossSize400.svg) aus, um eine Kombination **[!UICONTROL Report Suite]** und **[!UICONTROL Key Dimension]** zu löschen.

        Wenn Sie eine Kombination aus **[!UICONTROL Report Suite]** und **[!UICONTROL Key Dimension]** hinzufügen, die bereits in einem anderen Klassifizierungssatz vorhanden ist, wird eine rote Meldung angezeigt.
Sie haben folgende Möglichkeiten:
         * Wählen Sie **[!UICONTROL Zu vorhandenem hinzufügen]** aus, um den anderen Klassifizierungssatz zu öffnen und [Klassifizierungen zum Schema hinzufügen](manage/schema.md) für diesen anderen Klassifizierungssatz.
         * Ändern Sie **[!UICONTROL Report Suite]** und **[!UICONTROL Key Dimension]** in eine Kombination, die noch nicht für einen anderen Klassifizierungssatz abonniert wurde.
      * **[!UICONTROL Suche]**. Eine Lookup-Tabelle wird häufig als untergeordnete Klassifizierung oder Unterklassifizierung bezeichnet und ist eine Klassifizierung einer primären Klassifizierung. Bei einer Suche handelt es sich um Metadaten über einen Klassifizierungswert und nicht um die ursprüngliche Dimension. Beispielsweise könnte eine Dimension *Produkt* über eine primäre Classification mit *Farbcode* verfügen. Eine Lookup-Tabelle mit *Farbname* kann dann an den *Farbcode“ angehängt werden* um jeden Farbcode zu erklären.
1. Wählen **[!UICONTROL Speichern]**, um den Klassifizierungssatz zu speichern. Wählen Sie **[!UICONTROL Abbrechen]**, um die Definition aufzuheben.
1. Um das Schema für den Klassifizierungssatz zu definieren, wählen Sie den neu erstellten Klassifizierungssatz aus dem Manager **[!UICONTROL Klassifizierungssätze]** aus, um [Klassifizierungssatz zu bearbeiten](#edit-a-classification-set).


## Bearbeiten eines Klassifizierungssatzes

So bearbeiten Sie einen Klassifizierungssatz:

1. Wählen Sie **[!UICONTROL Komponenten]** in der oberen Menüleiste von Adobe Analytics aus und wählen Sie dann **[!UICONTROL Klassifizierungssätze]**.
1. Wählen **[!UICONTROL unter]** die Registerkarte **[!UICONTROL Klassifizierungssätze]** aus.
1. Wählen Sie den Namen Ihres Klassifizierungssatzes aus.
1. Im Dialogfeld **[!UICONTROL Klassifizierungssatz: _Klassifizierungssatzname_]**können Sie die [Einstellungen](manage/settings.md) und das [Schema](manage/schema.md) für den Klassifizierungssatz definieren.
1. Klicken Sie abschließend auf **[!UICONTROL Speichern]**, um Ihre Änderungen zu speichern. Wählen Sie zum Abbrechen **[!UICONTROL Abbrechen]** aus.
