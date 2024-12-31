---
title: Klassifizierungssatz-Regeln
description: Anzeigen und Bearbeiten von Regeln für einen einzelnen Klassifizierungssatz.
exl-id: 1ccb6a20-1993-4fd3-90eb-9154d12d0ec7
feature: Classifications
source-git-commit: 9f70dbeb9dfe54897915213480f05cbdfaf920ef
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 1%

---

# Klassifizierungssatz-Regeln

Klassifizierungssatzregeln ermöglichen es Ihnen, Werte automatisch basierend auf dem Wert zu klassifizieren, auf den die Variable gesetzt ist. Diese Regeln gelten für alle eingehenden Variablenwerte für alle Abonnements des Klassifizierungssatzes.

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]** > **[!UICONTROL Sets]** > Klicken Sie auf den Namen des gewünschten Klassifizierungssatzes > **[!UICONTROL Regeln]**

## Regeleinstellungen

Einstellungen, die für den gesamten Regelsatz gelten.

* **[!UICONTROL Regeln überschreiben]**: Bestimmt das Verhalten aller Regeln, wenn ein Classification-Wert vorhanden ist.
   * **[!UICONTROL Auf alle Werte anwenden]**: Wenn eine Regel übereinstimmt, den Classification-Wert immer überschreiben.
   * **[!UICONTROL Nur auf nicht eingestellte Werte anwenden]**: Wenn eine Regel übereinstimmt, muss der Classification-Wert nur geschrieben werden, wenn er leer ist. Wenn ein Classification-Wert vorhanden ist, führen Sie keine Aktionen aus.
* **[!UICONTROL Lookback-]**: Wenn diese Regel aktiviert ist, werden alle Regeln für alle eindeutigen Werte ausgeführt, die im hier festgelegten Lookback-Fenster angezeigt werden.

## Regeln

Eine Liste von Regeln, die für jeden eindeutigen Wert ausgeführt werden.

* **[!UICONTROL Suche]**: Ein Suchfeld, mit dem Sie Regeln nach Übereinstimmungskriterien filtern können.
* **[!UICONTROL Regel hinzufügen]**: Fügt der Regeltabelle eine leere Zeile hinzu.
* **[!UICONTROL Regelsatz testen]**: Ruft eine Test-Benutzeroberfläche auf, über die Sie Ihre Regeln überprüfen können. Auf der linken Seite können Sie Schlüsselwerte manuell eingeben oder eine Classification-Datei per Drag-and-Drop ziehen, um viele zu testende Werte zu importieren. Rechts sehen Sie eine Tabelle mit vorläufigen Ergebnissen dazu, wie klassifizierte Werte aussehen würden, wenn der Regelsatz aktiviert würde. Da diese Schnittstelle nur zur Validierung verwendet wird, werden keine Werte klassifiziert.

Wählen Sie eine oder mehrere Regeln aus, indem Sie auf das Kontrollkästchen neben der gewünschten Regel klicken. Bei Auswahl einer Regel werden die folgenden Optionen angezeigt:

* **[!UICONTROL Löschen]**: Löscht die Zeile aus der Regeltabelle.
* **[!UICONTROL Duplizieren]**: Kopiert die ausgewählten Zeilen in neue Zeilen in der Regeltabelle.

## Regeltabelle

Die Regeltabelle ist vertikal in zwei Hauptteile unterteilt: übereinstimmende Bedingung und Klassifizierungsaktion. Jede Zeile (eine einzelne Regel) enthält eine übereinstimmende Bedingung und eine Klassifizierungsaktion.

* **Regelnummer**: Regeln werden in der gleichen Reihenfolge ausgeführt wie die Regeltabelle. Wenn [!UICONTROL Regeln überschreiben] auf [!UICONTROL Auf alle Werte anwenden] festgelegt ist, überschreibt die letzte übereinstimmende Regel alle vorherigen Regeln für dieselbe Klassifizierungsdimension. Wenn [!UICONTROL Regeln überschreiben] auf &quot;[!UICONTROL  nur auf nicht festgelegte Werte anwenden] festgelegt ist, gilt die erste Regel, die einen Klassifizierungswert festlegt.
* **[!UICONTROL Regeltyp auswählen]**: Die Regelkriterien. Die Optionen umfassen [!UICONTROL Enthält], [!UICONTROL Endet mit], [!UICONTROL Regulärer Ausdruck], [!UICONTROL Regulärer Ausdruck] und [!UICONTROL Beginnt mit].
* **[!UICONTROL Übereinstimmungskriterien eingeben]**: Die zuzuordnende Textzeichenfolge. Wenn Sie [!UICONTROL  Regeltyp ]Regulärer Ausdruck“ auswählen, wird eine Überlagerung angezeigt, in der Sie den Wert eingeben, den regulären Ausdruck testen und eine Beispielsyntax angeben können.
* **[!UICONTROL Klassifizierung festlegen]**: Eine Dropdown-Liste, die die Klassifizierungsdimension festlegt, der Sie einen Wert zuweisen möchten. Gültige Optionen umfassen Elemente in Ihrem [Schema](schema.md).
* **[!UICONTROL An]**: Die Textzeichenfolge, auf die der klassifizierte Wert festgelegt werden soll. Wenn der Regeltyp &quot;[!UICONTROL &quot; ist] können Sie eine Kombination aus Text- und Übereinstimmungsgruppen einbeziehen.
