---
description: Sie können Daten von Analysis Workspace durch Kopieren oder in PDF- und CSV-Formaten herunterladen.
title: PDF- oder CSV-Dateien herunterladen
feature: Curate and Share
role: User, Admin
exl-id: 085013dc-8263-4fc8-9492-99f0ecadf14b
source-git-commit: 830d9cd13db1a0767cce4e3d2574a120d00a9ac8
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 90%

---

# PDF- oder CSV-Dateien herunterladen

Es gibt verschiedene Möglichkeiten, Daten aus Analysis Workspace zu exportieren. Welche Methode auswählen, hängt davon ab, welche Datensätze Sie analysieren möchten und wer darauf zugreifen muss.

Exportierte Daten können in Form kopierter Daten, CSV- oder PDF-Dateien vorliegen. Eine PDF wird normalerweise bevorzugt, wenn Sie möchten, dass Visualisierungen in der Datei enthalten sind. CSV- und kopierte Daten werden bevorzugt, wenn Sie Daten in Textform verwenden möchten.

## Herunterladen eines Projekts als CSV- oder PDF-Datei {#download-project}

Beachten Sie beim Herunterladen von Projekten Folgendes:

* Beim Herunterladen von Projekten als CSV- oder PDF-Datei kann das Projekt gespeichert oder nicht gespeichert werden, wenn Sie einen Projektdownload anfordern. Es können jedoch nur gespeicherte Projekte [geplant](/help/analyze/analysis-workspace/curate-share/t-schedule-report.md) sein.

* Beim Herunterladen von Projekten als PDF:
   * Der Export von Downloads kann mehrere Minuten dauern, da das Projekt auf Adobe-Servern erneut ausgeführt wird, bevor es im PDF-Format gerendert wird. Wir empfehlen, das Projekt nicht zu verlassen, bis die PDF-Datei in Ihren Browser heruntergeladen wurde. Sie können jedoch beim Warten weiterhin Änderungen am Projekt vornehmen. Wenn die Ausgabe einer PDF-Datei länger als 5 Minuten dauert, werden Sie aufgefordert, diese stattdessen per E-Mail zu erhalten.
   * Downloads werden als einzelne Seite ohne Seitenumbruch gerendert.
   * PDF-Renderings enthalten die Informationen auf der Seite in Workspace. Wenn ein Projekt Visualisierungen und Bedienfelder in benutzerdefinierter Größe enthält, müssen Sie diese so ändern, dass die Größe automatisch bestimmt wird (Schaltfläche in der oberen rechten Ecke), damit der Inhalt nicht abgeschnitten wird.
   * Alle [Hyperlinks](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table-hyperlinks.md), die in Freiformtabellen vorhanden sind, sind auf der heruntergeladenen PDF nicht funktionsfähig.

Herunterladen eines Projekts als CSV- oder PDF-Datei:

1. Führen Sie je nach dem Format, in dem Sie das Projekt herunterladen möchten, einen der folgenden Schritte aus:

   * **PDF:** Wählen Sie **[!UICONTROL Projekt]** > **[!UICONTROL PDF herunterladen]** aus.

     Wählen Sie diese Option, wenn die heruntergeladene Datei alle angezeigten (sichtbaren) Tabellen und Visualisierungen im Projekt enthalten soll.

   * **CSV:** Wählen Sie **[!UICONTROL Projekt]** > **[!UICONTROL CSV herunterladen]** aus.

     Wählen Sie diese Option aus, wenn Sie Daten in Textform verwenden möchten.

   ![](assets/download-project.png)

1. (Bedingt) Wenn Sie sich für den Download einer PDF entschieden haben, wird eine Nachricht angezeigt, sobald das Projekt heruntergeladen werden kann. Klicken Sie auf [!UICONTROL **Herunterladen**].

## Daten in die Zwischenablage kopieren (Hotkey: Strg + C) {#copy-data}

Mit der Rechtsklick-Option **[!UICONTROL In Zwischenablage kopieren]** können Sie Daten schnell aus Workspace kopieren und im Tool eines Drittanbieters einfügen.

* Wenn die angezeigte Tabelle kopiert werden soll, klicken Sie mit der rechten Maustaste auf die Tabellenkopfzeile und wählen Sie **Daten in die Zwischenablage kopieren**.
* Wenn Sie möchten, dass nur ein Teil der Daten kopiert wird, wählen Sie ihn in der Tabelle aus, und klicken Sie dann mit der rechten Maustaste auf >**Auswahl in Zwischenablage kopieren**.

>[!TIP]
>
>Sie können den Hotkey `Ctrl+C` verwenden, um Ihre Auswahl in die Zwischenablage zu kopieren, und dann `Ctrl+V`, um es in ein Tool eines Drittanbieters einzufügen.

![](assets/copy-selection.png)

## Daten als CSV herunterladen {#download-data}

Mit der Rechtsklick-Option **[!UICONTROL Daten als CSV herunterladen]** können Sie eine Datentabelle oder die Datenquelle einer beliebigen Visualisierung als CSV herunterladen.

* Klicken Sie in der Kopfzeile einer Tabelle oder Visualisierung mit der rechten Maustaste und wählen Sie **[!UICONTROL Daten als CSV herunterladen]** aus. Dadurch werden die in der Tabelle angezeigten Daten bzw. die zugrunde liegende Datenquelle für eine Visualisierung als CSV heruntergeladen.

  >[!NOTE]
  >
  >  Hinweis: Diese Option wird von der Kartenvisualisierung nicht unterstützt.

* Klicken Sie in einer Tabelle mit der rechten Maustaste und wählen Sie **[!UICONTROL Auswahl als CSV herunterladen]**. Mit dieser Option wird nur die Auswahl heruntergeladen, nicht die vollständige, angezeigte Tabelle.

![](assets/download-data-viz.png)

## Objekte als CSV herunterladen {#download-items}

Wenn Sie mehr als die 400 sichtbaren Zeilen mit Daten in einer Tabelle analysieren möchten, klicken Sie mit der rechten Maustaste auf die Tabellenkopfzeile oder eine beliebige Zeile und wählen Sie **Elemente als CSV herunterladen (_Dimensionsname_)**. Diese Option exportiert bis zu 50.000 Dimensionselemente (basierend auf der Tabellensortierung) für die ausgewählte Dimension, wobei Filter und Segmente angewendet werden. Wenn Sie diese Option oben in der Tabelle auswählen, wird die erste Dimension in der Tabelle exportiert. Obwohl in Freiformtabellen keine Beschränkungen gelten, wird empfohlen, die Option zum Herunterladen von Elementen in Tabellen mit weniger als 20 Spalten zu verwenden, um optimale Leistung sicherzustellen.

>[!TIP]
>
> Wenn Ihre Dimension 50.000 Elemente überschreitet, laden Sie die Datei mit unterschiedlichen Sortierkriterien herunter oder wenden Sie einen Filter an. Sortieren Sie z. B. absteigend nach Besuchen in einem Download und dann aufsteigend nach Besuchen in einem zweiten Download. Dieser Tipp hilft Ihnen beim Abrufen von längeren Elementen.

Während eines Downloads können Sie mehrere Aufgaben im Projekt ausführen und sogar zu einem neuen Workspace-Projekt auf derselben Registerkarte navigieren. Der Download wird angehalten, wenn Sie eine neue Browser-Registerkarte öffnen. Der Download wird abgebrochen, wenn Sie Workspace vollständig verlassen oder die Browser-Registerkarte schließen.

![](assets/download-items.png)

### Datei mit heruntergeladenen Elementen

Die Eigenschaften der Tabelle werden wie folgt auf die heruntergeladene Datei angewendet:

* Alle Bedienfeldsegmente werden als Filter angewendet.
* Aufschlüsselungen **oberhalb** der ausgewählten Dimension in der Tabelle werden als Filter über jeder einzelnen Spalte angezeigt.
* Aufschlüsselungen **unterhalb** der ausgewählten Dimension in der Tabelle werden entfernt.

Im obigen Beispiel werden Page-Elemente mit dem Bedienfeldsegment („New Visitor Customers“) heruntergeladen und die darüber liegenden Komponenten („Marketing Channel = Email“) als Filter angewendet, während die darunter liegenden Komponenten („Mobile Device Type“) aus der heruntergeladenen CSV entfernt werden.

![](assets/downloaded-file.png)

### Download-Benachrichtigungen

Beim Herunterladen der Datei wird eine Benachrichtigung mit dem Fortschritt angezeigt. Sie können den Download jederzeit abbrechen, indem Sie auf **[!UICONTROL Download abbrechen]** klicken. Durch Schließen des Popups wird der Download **nicht** abgebrochen.

Sobald die Datei abgeschlossen ist, wird eine Benachrichtigung angezeigt und die Datei wird in Ihren Browser heruntergeladen.

Wenn Sie mehrere Downloads gleichzeitig anfordern, erhalten Sie eine Benachrichtigung, dass jeder weitere Download in die Warteschlange gestellt wird, bis der vorherige Download abgeschlossen ist.

![](assets/toast.png)

## Häufig gestellte Fragen {#faq}

| Frage | Antwort |
| --- | --- |
| Warum besteht meine heruntergeladene PDF-Datei aus einer Seite? | In Workspace werden heruntergeladene PDFs derzeit nicht in Seiten unterteilt. |
| Kann ich mehr als 50.000 Elemente mit der Option „Elemente als CSV herunterladen“ exportieren? | Während jeder Download bis zu 50.000 Dimensionselemente enthalten kann, können Sie die Sortierung der Tabelle ändern, um längere Elemente abzurufen, oder einen Filter anwenden, um spezifischere Elemente herunterzuladen. |
| Beschreibung der Funktion **[!UICONTROL Visualisierung kopieren]** | Im Gegensatz zu [!UICONTROL **Daten in die Zwischenablage kopieren**] oder [!UICONTROL **Auswahl in Zwischenablage kopieren**] handelt es sich bei der Rechtsklick-Option **[!UICONTROL Visualisierung kopieren]** um keine Exportoption. Damit können Sie eine Visualisierung oder ein Bedienfeld von einem Bereich in Workspace in einen anderen kopieren. Beispielsweise von einem Bedienfeld in ein anderes im selben Projekt oder von einem Projekt in ein anderes. [Intra-linking-Video](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/visualizations/intra-linking-in-analysis-workspace.html?lang=de) |
