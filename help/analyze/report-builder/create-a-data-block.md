---
title: Erstellen eines Datenblocks mit Report Builder
description: Beschreibt, wie ein Datenblock erstellt wird.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
source-git-commit: a8cb45c11089a0b69373ef3cf2a49687cd20da09
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 55%

---

# Datenblock erstellen

Ein *Datenblock* ist die Datentabelle, die von einer einzelnen Datenanforderung erstellt wird. Eine Report Builder-Arbeitsmappe kann mehrere Datenblöcke enthalten. Wenn Sie einen Datenblock erstellen, konfigurieren Sie ihn zunächst und erstellen Sie dann den Build.

## Datenblock konfigurieren

Konfigurieren Sie die anfänglichen Datenblockparameter für die Position des Datenblocks, die Report Suite und einen Datumsbereich.

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   ![ Screenshot mit der Option &quot;Datenblock erstellen&quot;.](./assets/create_db.png)

1. Legen Sie den **[!UICONTROL Speicherort des Datenblocks]** fest.

   Die Option „Datenblock-Speicherort“ definiert den Speicherort des Arbeitsblatts, an dem Report Builder die Daten zu Ihrem Arbeitsblatt hinzufügt.

   Um den Speicherort des Datenblocks anzugeben, wählen Sie eine einzelne Zelle im Arbeitsblatt aus oder geben Sie eine Zellenadresse ein, z. B. a3, \\\$a3, a\\\$3 oder sheet1!a2. Die angegebene Zelle markiert die obere linke Ecke des Datenblocks, wenn die Daten abgerufen werden.

1. Wählen Sie eine **Report Suite** aus.

   Mit der Option Report Suites können Sie eine Report Suite aus einem Dropdown-Menü auswählen oder auf eine Report Suite aus einer Zellenposition verweisen.

1. Legen Sie den **[!UICONTROL Datumsbereich]** fest.

   Mit der Option „Datumsbereich“ können Sie einen Datumsbereich auswählen. Datumsbereiche können fest oder rollierend sein. Weitere Informationen zu den Datumsbereichsoptionen finden Sie unter [Einen Datumsbereich auswählen](select-date-range.md).

1. Klicken Sie auf **[!UICONTROL Weiter]**.

   ![Screenshot mit der Option &quot;Datumsbereich&quot;und der aktiven Schaltfläche &quot;Weiter&quot;](./assets/choose_date_data_view3.png)

   Nach der Konfiguration des Datenblocks können Sie Dimensionen, Metriken und Segmente auswählen, um Ihren Datenblock zu erstellen. Die Registerkarten „Dimensionen“, „Metriken“ und „Filter“ werden über dem Bereich „Tabellen-Builder“ angezeigt.

## Datenblock erstellen

Um den Datenblock zu erstellen, wählen Sie Berichtkomponenten aus und passen Sie dann das Layout an.

1. Fügen Sie Dimensionen, Metriken und Filter hinzu.

   Scrollen Sie in den Komponentenlisten durch oder verwenden Sie das Feld **[!UICONTROL Suche]** , um Komponenten zu finden. Ziehen Sie Komponenten per Drag &amp; Drop in den Tabellenbereich oder doppelklicken Sie auf einen Komponentennamen in der Liste, um die Komponente automatisch zum Tabellenbereich hinzuzufügen.

   Doppelklicken Sie auf eine Komponente, um sie einem Standardabschnitt der Tabelle hinzuzufügen.

   - Dimensionskomponenten werden zum Bereich „Zeile“ oder zum Bereich „Spalte“ hinzugefügt, wenn bereits eine Dimension in den Spalten vorhanden ist.
   - Datumskomponenten werden dem Abschnitt „Spalte“ hinzugefügt.
   - Filterkomponenten werden dem Abschnitt „Filter“ hinzugefügt.

   **Startdatum als Dimension**

   Legen Sie das **[!UICONTROL Startdatum]** als Dimension fest, um das Startdatum Ihres Datenblocks eindeutig zu identifizieren. Dies ist hilfreich, wenn Sie einen regelmäßig terminierten Bericht mit einem rollierenden Datumsbereich haben oder wenn Sie einen unkonventionellen Datumsbereich haben und Sie am Startdatum klar sein müssen.

   ![Screenshot mit dem Startdatum in der Liste der Dimensionen.](./assets/start-date-dimension.png){width="30%"}

1. Ordnen Sie die Elemente im Tabellenbereich an, um das Layout Ihres Datenblocks anzupassen.

   Ziehen Sie Komponenten per Drag &amp; Drop in den Tabellenbereich, um sie neu anzuordnen, oder klicken Sie mit der rechten Maustaste auf einen Komponentennamen und wählen Sie im Optionsmenü die Option aus.

   Wenn Sie Komponenten zur Tabelle hinzufügen, wird eine Vorschau des Datenblocks an der Stelle des Datenblocks im Arbeitsblatt angezeigt. Das Layout der Datenblock-Vorschau wird automatisch aktualisiert, wenn Sie in der Tabelle Elemente hinzufügen, verschieben oder entfernen.

   ![ Screenshot mit den hinzugefügten Komponenten und dem aktualisierten Arbeitsblatt.](./assets/image10.png)

   **Anzeigen oder Ausblenden von Zeilen- und Spaltenüberschriften**

1. Klicken Sie auf das Symbol **[!UICONTROL Tabelleneinstellungen]**.

   ![ Screenshot mit der Option Tabelleneinstellungen.](./assets/table-settings.png){width="35%"}

1. Aktivieren oder deaktivieren Sie die Option zum Anzeigen von Zeilen- und Spaltenüberschriften. Die Kopfzeilen werden standardmäßig angezeigt.

   **Ausblenden oder Anzeigen von Dimensionsbezeichnungen und Metrik-Überschriften**

1. Klicken Sie auf das Auslassungssymbol in den Dimensionen oder Spaltenüberschriften, um die Einstellungen anzuzeigen.

   ![Das Symbol mit Auslassungspunkten im Abschnitt &quot;Zeile&quot;.](./assets/row-heading.png){width="35%"}

1. Klicken Sie auf Ausblenden oder Anzeigen , um die Dimensionsbezeichnungen oder Spaltenüberschriften umzuschalten. Alle Bezeichnungen werden standardmäßig angezeigt.

1. Klicken Sie auf **[!UICONTROL Fertig stellen]**.

   Eine Verarbeitungsmeldung wird angezeigt, während die Analysedaten abgerufen werden.

   ![ Die Verarbeitungsmeldung.](./assets/image11.png)

   Report Builder ruft die Daten ab und zeigt den abgeschlossenen Datenblock im Arbeitsblatt an.

   ![Der abgeschlossene Datenblock.](./assets/image12.png)
