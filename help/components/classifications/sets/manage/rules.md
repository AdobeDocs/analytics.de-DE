---
title: Klassifizierungssatz-Regeln
description: Anzeigen und Bearbeiten von Regeln für einen einzelnen Classification-Satz.
exl-id: 1ccb6a20-1993-4fd3-90eb-9154d12d0ec7
feature: Classifications
source-git-commit: 9f70dbeb9dfe54897915213480f05cbdfaf920ef
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 1%

---

# Klassifizierungssatz-Regeln

Mit Classification-Satzregeln können Sie Werte automatisch basierend auf dem Wert klassifizieren, auf den die Variable gesetzt ist. Diese Regeln gelten für alle eingehenden Variablenwerte für alle Abonnements des Classification-Sets.

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]** > **[!UICONTROL Sets]** > Klicken Sie auf den Namen des gewünschten Klassifizierungssatzes > **[!UICONTROL Regeln]**

## Regeleinstellungen

Einstellungen, die für den gesamten Regelsatz gelten.

* **[!UICONTROL Regeln überschreiben]**: Bestimmt das Verhalten aller Regeln in Fällen, in denen ein Classification-Wert vorhanden ist.
   * **[!UICONTROL Auf alle Werte anwenden]**: Wenn eine Regel übereinstimmt, überschreiben Sie immer den Classification-Wert.
   * **[!UICONTROL Nur auf nicht festgelegte Werte anwenden]**: Wenn eine Regel übereinstimmt, schreiben Sie den Classification-Wert nur, wenn er leer ist. Wenn ein Classification-Wert vorhanden ist, führen Sie keine Schritte aus.
* **[!UICONTROL Lookback-Fenster]**: Wenn diese Regel aktiviert ist, werden alle Regeln für alle eindeutigen Werte ausgeführt, die im hier festgelegten Lookback-Fenster angezeigt werden.

## Regeln

Eine Liste von Regeln, die für jeden eindeutigen Wert ausgeführt werden.

* **[!UICONTROL Suche]**: Ein Suchfeld, mit dem Sie Regeln nach Übereinstimmungskriterien filtern können.
* **[!UICONTROL Regel hinzufügen]**: Fügt der Regeltabelle eine leere Zeile hinzu.
* **[!UICONTROL Regelsatz testen]**: Öffnet eine Test-Benutzeroberfläche, über die Sie Ihre Regeln überprüfen können. Auf der linken Seite können Sie Schlüsselwerte manuell eingeben oder eine Classification-Datei per Drag-and-Drop verschieben, um viele Werte zu importieren, mit denen Sie testen können. Rechts befindet sich eine Tabelle, die vorläufige Ergebnisse zeigt, wie klassifizierte Werte aussehen würden, wenn der Regelsatz aktiviert würde. Da diese Schnittstelle nur zur Validierung dient, werden keine Werte klassifiziert.

Wählen Sie eine oder mehrere Regeln aus, indem Sie auf das Kontrollkästchen neben der gewünschten Regel klicken. Wenn Sie eine Regel auswählen, werden die folgenden Optionen angezeigt:

* **[!UICONTROL Löschen]**: Löscht die Zeile aus der Regeltabelle.
* **[!UICONTROL Duplizieren]**: Kopiert die ausgewählten Zeilen in neue Zeilen in der Regeltabelle.

## Regeltabelle

Die Regeltabelle wird vertikal in zwei Hauptteile unterteilt: übereinstimmende Bedingung und Classification-Aktion. Jede Zeile (eine einzelne Regel) enthält eine übereinstimmende Bedingung und eine Classification-Aktion.

* **Regelnummer**: Regeln werden in derselben Reihenfolge ausgeführt, in der Sie die Regeltabelle konfigurieren. Wenn [!UICONTROL Regeln überschreiben] auf [!UICONTROL Auf alle Werte anwenden] festgelegt ist, überschreibt die letzte übereinstimmende Regel alle vorherigen Regeln für dieselbe Classification-Dimension. Wenn [!UICONTROL Regeln überschreiben] auf [!UICONTROL Nur nicht festgelegte Werte anwenden] festgelegt ist, gilt die erste Regel, die einen Classification-Wert festlegt.
* **[!UICONTROL Regeltyp auswählen]**: Die Regelkriterien. Zu den Optionen gehören [!UICONTROL Enthält], [!UICONTROL Endet mit], [!UICONTROL Regulärer Ausdruck], [!UICONTROL Regulärer Ausdruck] und [!UICONTROL Beginnt mit ].
* **[!UICONTROL Geben Sie Übereinstimmungskriterien ein]**: Die Textzeichenfolge, die abgeglichen werden soll. Wenn Sie als Regeltyp [!UICONTROL Regulärer Ausdruck] auswählen, wird eine Überlagerung angezeigt, über die Sie den Wert eingeben, den regulären Ausdruck testen und eine Beispielsyntax bereitstellen können.
* **[!UICONTROL Classification festlegen]**: Eine Dropdown-Liste, die die Classification-Dimension festlegt, der Sie einen Wert zuweisen möchten. Gültige Optionen sind Elemente in Ihrem [Schema](schema.md).
* **[!UICONTROL To]**: Die Textzeichenfolge, auf die der klassifizierte Wert gesetzt werden soll. Wenn der Regeltyp [!UICONTROL Regulärer Ausdruck] ist, können Sie eine Kombination aus Text und Übereinstimmungsgruppen einfügen.
