---
title: Erstellen eines Datenblocks mit Report Builder
description: Beschreibt, wie ein Datenblock erstellt wird.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: fd3ff12a-14de-46f6-ab89-a0152fb11b0d
source-git-commit: c35d5bdc29ce80f0c9357339b04fd2d656cfbe52
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 49%

---

# Datenblock erstellen

Ein *Datenblock* ist die Datentabelle, die von einer einzelnen Datenanforderung erstellt wird. Eine Report Builder-Arbeitsmappe kann mehrere Datenblöcke enthalten. Wenn Sie einen Datenblock erstellen, konfigurieren Sie ihn zunächst und erstellen Sie dann den Build.

## Datenblock konfigurieren

Konfigurieren Sie die anfänglichen Datenblockparameter für den Speicherort des Datenblocks, die Report Suite und einen Datumsbereich.

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   ![Screenshot mit der Option „Datenblock erstellen“.](./assets/create_db.png)

1. Legen Sie den **[!UICONTROL Speicherort des Datenblocks]** fest.

   Die Option „Datenblock-Speicherort“ definiert den Speicherort des Arbeitsblatts, an dem Report Builder die Daten zu Ihrem Arbeitsblatt hinzufügt.

   Um die Position des Datenblocks anzugeben, wählen Sie eine einzelne Zelle im Arbeitsblatt aus und klicken Sie auf das Symbol neben **[!UICONTROL Speicherort des Datenblocks]**:

   Sie können auch eine Zellenadresse eingeben, z. B. a3, \\\$a3, a\\\$3 oder sheet1!a2. Die angegebene Zelle markiert die obere linke Ecke des Datenblocks, wenn die Daten abgerufen werden.

1. Wählen Sie eine **Report Suite**.

   Mit der Option Report Suites können Sie eine Report Suite aus einem Dropdown-Menü auswählen oder eine Report Suite aus einer Zellenposition referenzieren.

1. Legen Sie den **[!UICONTROL Datumsbereich]** fest.

   Mit der Option „Datumsbereich“ können Sie einen Datumsbereich auswählen. Datumsbereiche können fest oder rollierend sein. Weitere Informationen zu den Datumsbereichsoptionen finden Sie unter [Einen Datumsbereich auswählen](select-date-range.md).

1. Klicken Sie auf **[!UICONTROL Weiter]**.

   ![Screenshot mit der Option „Datumsbereich“ und der Schaltfläche „Aktiv Weiter“.](./assets/choose_date_report_suite.png)

   Nach der Konfiguration des Datenblocks können Sie Dimensionen, Metriken und Segmente auswählen, um Ihren Datenblock zu erstellen. Die Registerkarten „Dimensionen“, „Metriken“ und „Filter“ werden über dem Bereich „Tabellen-Builder“ angezeigt.

## Datenblock erstellen

Um den Datenblock zu erstellen, wählen Sie Berichtkomponenten aus und passen Sie dann das Layout an.

1. Dimensionen, Metriken und Segmente hinzufügen.

   Scrollen Sie in den Komponentenlisten oder verwenden Sie das Feld **[!UICONTROL Suchen]**, um Komponenten zu finden. Ziehen Sie Komponenten per Drag &amp; Drop in den Tabellenbereich oder doppelklicken Sie auf einen Komponentennamen in der Liste, um die Komponente automatisch zum Tabellenbereich hinzuzufügen.

   Doppelklicken Sie auf eine Komponente, um sie einem Standardabschnitt der Tabelle hinzuzufügen.

   - Dimensionskomponenten werden zum Bereich „Zeile“ oder zum Bereich „Spalte“ hinzugefügt, wenn bereits eine Dimension in den Spalten vorhanden ist.
   - Datumskomponenten werden dem Abschnitt „Spalte“ hinzugefügt.
   - Segmentkomponenten werden zum Abschnitt Segmente hinzugefügt.

   **Startdatum als Dimension**

   Legen Sie **[!UICONTROL Startdatum]** als Dimension fest, um das Startdatum Ihres Datenblocks eindeutig zu identifizieren. Dies ist hilfreich, wenn Sie einen regelmäßig geplanten Bericht mit einem rollierenden Datumsbereich haben oder wenn Sie einen unkonventionellen Datumsbereich haben und Sie am Startdatum klar sein müssen.

   ![Screenshot mit dem Startdatum in der Liste der Dimensionen.](./assets/start-date-dimension.png){width="30%"}

1. Ordnen Sie die Elemente im Tabellenbereich an, um das Layout Ihres Datenblocks anzupassen.

   Ziehen Sie Komponenten per Drag &amp; Drop in den Tabellenbereich, um sie neu anzuordnen, oder klicken Sie mit der rechten Maustaste auf einen Komponentennamen und wählen Sie im Optionsmenü die Option aus.

   Wenn Sie Komponenten zur Tabelle hinzufügen, wird eine Vorschau des Datenblocks an der Stelle des Datenblocks im Arbeitsblatt angezeigt. Das Layout der Datenblock-Vorschau wird automatisch aktualisiert, wenn Sie in der Tabelle Elemente hinzufügen, verschieben oder entfernen.

   ![Screenshot mit den hinzugefügten Komponenten und dem aktualisierten Arbeitsblatt.](./assets/image10.png)

   **Zeilen- und Spaltenüberschriften anzeigen oder ausblenden**

1. Klicken Sie auf **[!UICONTROL Symbol]** Tabelleneinstellungen“.

   ![Screenshot mit der Option „Tabelleneinstellungen“](./assets/table-settings.png){width="35%"}

1. Aktivieren oder deaktivieren Sie die Option, um Zeilen- und Spaltenüberschriften anzuzeigen. Die Kopfzeilen werden standardmäßig angezeigt.

   **Dimensionskennzeichnungen und Metrikkopfzeilen ein- oder ausblenden**

1. Klicken Sie auf das Symbol mit den Auslassungspunkten entweder auf den Dimensionen oder auf den Spaltenüberschriften, um die Einstellungen anzuzeigen.

   ![Das Symbol mit den Auslassungspunkten im Zeilenabschnitt.](./assets/row-heading.png){width="35%"}

1. Klicken Sie auf Ausblenden oder Anzeigen , um die Dimensionsbeschriftungen oder Spaltenüberschriften umzuschalten. Alle Beschriftungen werden standardmäßig angezeigt.

1. Klicken Sie auf **[!UICONTROL Fertig stellen]**.

   Eine Verarbeitungsmeldung wird angezeigt, während die Analysedaten abgerufen werden.

   Report Builder ruft die Daten ab und zeigt den abgeschlossenen Datenblock im Arbeitsblatt an.

   ![Der abgeschlossene Datenblock.](./assets/image12.png)
