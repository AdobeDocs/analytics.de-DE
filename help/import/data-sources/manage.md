---
title: Verwalten von Datenquellen
description: Navigieren Sie in der Benutzeroberfläche zum Verwalten von Datenquellen .
exl-id: 315501fb-26e1-436a-938d-5957ca037cd0
feature: Data Sources
role: Admin
source-git-commit: 27bcbd638848650c842ad8d8aaa7ab59e27e900e
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 7%

---

# Verwalten von Datenquellen

Verwenden Sie den Datenquellen-Manager, um Datenquellen zu erstellen, zu bearbeiten oder zu deaktivieren. Sie können diese Benutzeroberfläche auch verwenden, um den Status von Dateien zu verfolgen, die zu FTP-Speicherorten für Datenquellen hochgeladen wurden.

**[!UICONTROL Admin]** > **[!UICONTROL Alle Administratoren]** > **[!UICONTROL Datenquellen]**

Verwenden Sie den Report Suite-Selektor oben rechts, um zwischen Report Suites in Ihrer Organisation zu wechseln.

Diese Benutzeroberfläche verfügt über drei Registerkarten: **[!UICONTROL Verwalten]**, **[!UICONTROL Erstellen]** und **[!UICONTROL Dateiprotokoll]**.

## Verwalten

Die **[!UICONTROL Verwalten]** verarbeitet alle Datenquellen, die Ihr Unternehmen erstellt hat. Sie können FTP-Informationen anzeigen, Änderungen an Variablen vornehmen, die in Vorlagendateien verwendet werden, oder Datenquellen vollständig deaktivieren.

![Verwalten](assets/manage.png)

Die oberste Datenquelle ist immer [!UICONTROL Web Beacon]. Diese Datenquelle wird für die typische Datenerfassung über AppMeasurement verwendet. Sie kann nicht bearbeitet oder deaktiviert werden.

Jede Datenquelle verfügt über die folgenden Optionen:

* **[!UICONTROL Verarbeitung neu starten]**: Startet die Verarbeitung von Datenquellen neu, die zuvor aufgrund von Fehlern angehalten wurde. Die Verarbeitung wird fortgesetzt, bis der nächste Fehler erkannt wird. Datenquellen : Hält die Verarbeitung einer Datenquellendatei nur an, wenn Sie die Option **[!UICONTROL Verarbeitung bei Fehlern anhalten]** auswählen.
* **[!UICONTROL Vollständige Verarbeitung]**: Nicht mehr verwendet - Diese Schaltfläche wurde nur für „Vollständige [&quot; ](full-processing-eol.md).
* **[!UICONTROL Verarbeitung bei Fehlern anhalten]**: Ein Kontrollkästchen, das den Verarbeitungs-Server anweist, bei einem Fehler anzuhalten. Die Datenquelle nimmt die Verarbeitung erst wieder auf, wenn Sie auf **[!UICONTROL Verarbeitung neu starten]** klicken. Wenn eine Datenquelle auf einen Dateifehler stößt, werden Sie über den Fehler benachrichtigt. Adobe verschiebt die fehlerhafte Datei in einen Ordner namens `files_with_errors` auf dem FTP-Server. Nachdem Sie das Problem behoben haben, senden Sie die Datei erneut zur Verarbeitung.
* **[!UICONTROL Konfigurieren]**: Ein Link, der Sie durch den Assistenten zur Erstellung von Datenquellen für diese Datenquelle führt. Dieser Assistent ermöglicht es Ihnen, die Datenquelle umzubenennen oder die beim Herunterladen einer Vorlagendatei automatisch eingeschlossenen Variablen neu zu konfigurieren.
* **[!UICONTROL FTP-]**: Ein Link, der Sie zum letzten Schritt des Assistenten zur Erstellung von Datenquellen führt, in dem FTP-Anmeldeinformationen angezeigt werden.

Sobald eine Datenquelle Daten erhält, wird eine Tabelle angezeigt, die mehrere Spalten für die hochgeladenen Dateien enthält.

* **[!UICONTROL Dateien in der Verarbeitungswarteschlange]**: Der Name der Datei.
* **[!UICONTROL Zeilen]**: Die Gesamtzahl der Zeilen in der Datei.
* **[!UICONTROL Fehler]**: Die Anzahl der Zeilen, die Fehler enthielten und nicht aufgenommen werden konnten.
* **[!UICONTROL Warnungen]**: Die Anzahl der Zeilen, die Warnungen enthielten.
* **[!UICONTROL Received]**: Der Zeitstempel, mit dem die Datei in der Zeitzone der Report Suite empfangen wurde.
* **[!UICONTROL Status]**: Der Status der Datei (`Success` oder `Failed`).

## Erstellen

Die **[!UICONTROL Erstellen]** gibt Ihnen einen Ausgangspunkt für den Assistenten zur Erstellung von Datenquellen.

![Erstellen](assets/create.png)

Die Kategorie und der Typ der Datenquelle waren in früheren Versionen von Adobe Analytics wertvoller. Sie haben jedoch immer noch eine begrenzte Verwendung:

* Der Datenquellentyp wird auf der Registerkarte [Verwalten](#manage) für die Datenquelle selbst und auf der Registerkarte [Dateiprotokoll](#file-log) für jede einzelne Datei angezeigt.
* Einige Datenquellentypen enthalten beim Herunterladen der Vorlagendatei automatisch Variablen. Sie können jedoch jede verfügbare Dimension oder Metrik einbeziehen, solange sie dem etablierten [Dateiformat“ ](file-format.md).

Abgesehen von diesen Gründen sind alle Datenquellenkategorien und -typen, die Sie auswählen können, effektiv identisch. Wählen Sie die Kategorie und den Typ aus, die bzw. der Ihren Zweck bei der Verwendung von Datenquellen am besten widerspiegelt.

Mit der Einstellung [Full Processing Data Sources](full-processing-eol.md) können mehrere Kategorien und Typen nicht mehr ausgewählt werden. Wenn Sie einen Datenquellentyp für die vollständige Verarbeitung auswählen, wird **[!UICONTROL Schaltfläche]** Aktivieren“ ausgegraut.

## Dateiprotokoll

Die Registerkarte **[!UICONTROL Dateiprotokoll]** bietet eine aggregierte Ansicht aller Datenquellendateien, die für die jeweilige Report Suite hochgeladen wurden.

![Dateiprotokoll](assets/file-log.png)

Es ist eine Suchleiste verfügbar, mit der Sie eine bestimmte Datenquelle finden können. Die Tabelle zeigt die folgenden Spalten:

* **[!UICONTROL Data Source Name]**: Der Name der Datenquelle.
* **[!UICONTROL Type]**: Der Typ der Datenquelle.
* **[!UICONTROL Dateiname]**: Der Name der hochgeladenen Datei.
* **[!UICONTROL Zeilen]**: Die Gesamtzahl der Zeilen in der Datei.
* **[!UICONTROL Fehler]**: Die Anzahl der Zeilen, die Fehler enthielten.
* **[!UICONTROL Warnungen]**: Wird nicht mehr verwendet. Die Anzahl der Zeilen, die Warnungen enthielten.
* **[!UICONTROL Received]**: Datum und Uhrzeit des Beginns der Verarbeitung der Datei durch Adobe.
* **[!UICONTROL Status]**: Der Status der Datei (`Success` oder `Failed`).
