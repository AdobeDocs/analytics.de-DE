---
description: Häufig gestellte Fragen zu Workspace
title: Häufig gestellte Fragen und Fehlerbehebung in Workspace
feature: Workspace Basics
role: User, Admin
exl-id: cf7a9a73-bcbe-4bf5-b5dc-913199ab229c
source-git-commit: 8eb15d8211bf2a5418465baa902e533198637a4a
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 91%

---

# Häufig gestellte Fragen

+++Was sind die Voraussetzungen für die Verwendung von Analysis Workspace?
[Senden von Daten an Adobe Analytics mithilfe von Adobe Analytics-Erweiterungen](/help/implement/launch/validate-publish-prod.md): Für die Verwendung von Analysis Workspace ist eine funktionierende Implementierung erforderlich. Vergewissern Sie sich, dass Ihre Organisation Daten an Adobe sendet, bevor Sie das Tool verwenden. Andere Implementierungen wie DTM oder ältere manuelle Implementierungen können ebenfalls funktionieren.
+++

+++Welche Administrations- und Zugriffsanforderungen gibt es für Analysis Workspace?
Siehe [Administrationsanforderungen](/help/analyze/analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md).
+++

+++Wirkt sich die Verwendung von Analysis Workspace auf die Datenerfassung aus?
Da Analysis Workspace ein Berichtswerkzeug ist, hat dies keine Auswirkungen auf die Datenerfassung. Komponenten wahllos in ein Projekt zu ziehen, um zu sehen, was funktioniert, hat keine weiteren Folgen. Ziehen Sie verschiedene Kombinationen von Dimensionen und Metriken in Ihr Workspace-Projekt, um zu sehen, welche Möglichkeiten Sie haben. Wenn Sie versehentlich eine ungültige Komponente in Ihr Workspace-Projekt ziehen oder einen Schritt zurückgehen möchten, drücken Sie Strg + Z (Windows) oder Befehl + Z (Mac), um die letzte durchgeführte Aktion rückgängig zu machen. Sie können auch mit einem leeren Arbeitsbereich beginnen, indem Sie im Menü oben links auf **[!UICONTROL Projekt]** > **[!UICONTROL Neu]** klicken.
+++

+++Wie viele Report Suites können in einem Projekt in Analysis Workspace angezeigt werden?
Sie können jetzt in Analysis Workspace Projekte mit Daten aus [mehreren Report Suites](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.html?lang=de) erstellen.
+++

+++Wie wird Analysis Workspace implementiert?
Es ist keine spezielle Implementierung erforderlich. Der Analysis Workspace steht allen Unternehmen mit Analytics Standard oder Premium zur Verfügung. Es gelten jedoch die Standardberechtigungen für Inhalte (z. B. Report Suites und Projektkomponenten) und für die Kuratierung und Freigabe von Projekten. Weitere Informationen finden Sie unter [Administrations- und Zugriffsanforderungen](/help/analyze/analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md).
+++

+++Kann ich Analysis Workspace für Data Warehouse verwenden?
Der Analysis Workspace wird für den Export von Massendaten nicht empfohlen. Es handelt sich um Arbeitsplatz für die Visualisierung, über den dashboardartiger Analyseprojekte erstellt werden können.
+++

+++Wie kann ich die Leistung von Analysis Workspace optimieren?
Siehe [Leistungsoptimierung](/help/analyze/analysis-workspace/workspace-faq/optimizing-performance.md).
+++

+++Wie fließen Daten in Ihr Analysis Workspace-Projekt ein?
Sehen Sie sich dieses Video an:

>[!VIDEO](https://video.tv.adobe.com/v/31072/?quality=12)

+++

+++ Wie kann ich die Workspace-Nutzung nachverfolgen?

Sehen Sie sich dieses Video zur Nutzungsprotokollverfolgung für Analysis Workspace an:

>[!VIDEO](https://video.tv.adobe.com/v/29768/?quality=12)

+++

+++Wenn ich eine Metrik per Drag-and-Drop ziehe, wird die Meldung „Ungültige Daten“ angezeigt. Wie kann ich dieses Problem beheben?
„Ungültige Daten“ bedeuten, dass Adobe keine Daten mit der Kombination von Dimensionen und Metriken zurückgeben kann, die im Bericht verwendet werden. Beispielsweise können zwei Metriken, die übereinander gestapelt sind, nicht als Daten zurückgegeben werden, da es nicht möglich ist, zwei Metriken in dieser Weise anzuzeigen. Platzieren Sie die Metriken stattdessen nebeneinander.
+++

+++Wenn ich eine Metrik per Drag-and-drop ziehe, sehe ich keine tatsächlichen Daten, sondern nur Nullen. Wie kann ich dieses Problem beheben?
Wenn Sie einen Workspace-Bericht erfolgreich erstellt haben, aber keine Daten vorhanden sind, können Sie einige Punkte prüfen:

* Überprüfen Sie die Report Suite und stellen Sie sicher, dass sie mit Daten gefüllt ist.
* Wenn Sie ein Segment in Ihrem Bericht angewendet haben, stimmen die Segmentkriterien möglicherweise nicht mit den Daten überein. Versuchen Sie, das Segment zu entfernen oder die Segmentdefinition anzupassen.
* Überprüfen Sie den Datumsbereich oben rechts und stellen Sie sicher, dass er auf einen erwarteten Wert eingestellt ist.
* Navigieren Sie zu Ihrer Website und überprüfen Sie mit dem [Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=de), ob Daten erfasst werden.
+++

+++Welche Aktionen kann ich als schreibgeschützter Benutzer in Analysis Workspace durchführen?
Wenn ein Projekt schreibgeschützt freigegeben wird, sind alle Bearbeitungsfunktionen und -funktionen vollständig deaktiviert und die Empfänger können die Dropdown-Liste nur ändern, um einen Filter auf vordefinierte Weise auf das Bedienfeld anzuwenden.
+++