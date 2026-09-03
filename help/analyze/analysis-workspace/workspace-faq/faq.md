---
description: Erhalten Sie Antworten auf häufig gestellte Fragen zu Analysis Workspace.
title: Häufig gestellte Fragen
feature: Workspace Basics
role: User, Admin
exl-id: cf7a9a73-bcbe-4bf5-b5dc-913199ab229c
TQID: https://experienceleague.adobe.com/Cp7KvN1Y7Mxr4iGWNF08TYBzJWqhVWVSHApX0989lZ4
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7aid: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2: id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: c069c44e-5426-4c1a-accc-8028662f2fdeid: ef60b66e-5984-4336-ba72-6d978b1b6f87
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d3cdead0-685a-4489-9250-4bb709942f66id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 598
ht-degree: 84%

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
Sie können jetzt in Analysis Workspace Projekte mit Daten aus [mehreren Report Suites](/help/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.md) erstellen.
+++

+++Wie wird Analysis Workspace implementiert?
Es ist keine spezielle Implementierung erforderlich. Analysis Workspace steht allen Unternehmen mit Analytics Standard oder Premium zur Verfügung. Es gelten jedoch die Standardberechtigungen für Inhalte (z. B. Report Suites und Projektkomponenten) und für das Kuratieren und Freigeben von Projekten. Weitere Informationen finden Sie unter [Administrations- und Zugriffsanforderungen](/help/analyze/analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md).
+++

+++Kann ich Analysis Workspace für Data Warehouse verwenden?
Analysis Workspace wird für den Massendatenexport nicht empfohlen. Es handelt sich um Arbeitsplatz für die Visualisierung, über den dashboardartiger Analyseprojekte erstellt werden können.
+++

+++Wie kann ich die Leistung von Analysis Workspace optimieren?

Siehe [Leistungsoptimierung](/help/analyze/analysis-workspace/workspace-faq/optimizing-performance.md).

+++

+++Wie fließen Daten in Ihr Analysis Workspace-Projekt ein?

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Datenaufnahme in Analysis Workspace](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/analysis-workspace/analysis-workspace-basics/understanding-how-data-gets-into-your-analysis-workspace-project){target="_blank"} finden Sie ein Demovideo.

+++

+++Wie kann ich die Workspace-Nutzung nachverfolgen?

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Protokoll-Tracking](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/administration/logs/usage-log-tracking-for-analysis-workspace){target="_blank"} finden Sie ein Demovideo.

+++

+++Wenn ich eine Metrik per Drag-and-Drop ziehe, wird die Meldung „Ungültige Daten“ angezeigt. Wie kann ich dieses Problem beheben?

„Ungültige Daten“ bedeuten, dass Adobe keine Daten mit der Kombination von Dimensionen und Metriken zurückgeben kann, die im Bericht verwendet werden. Beispielsweise können zwei Metriken, die übereinander gestapelt sind, nicht als Daten zurückgegeben werden, da es nicht möglich ist, zwei Metriken in dieser Weise anzuzeigen. Platzieren Sie die Metriken stattdessen nebeneinander.

+++

+++Wenn ich eine Metrik per Drag-and-Drop ziehe, sehe ich keine tatsächlichen Daten, sondern nur Nullen. Wie kann ich dieses Problem beheben?

Wenn Sie einen Workspace-Bericht erfolgreich erstellt haben, aber keine Daten vorhanden sind, können Sie einige Punkte prüfen:

* Überprüfen Sie die Report Suite und stellen Sie sicher, dass sie mit Daten gefüllt ist.
* Wenn Sie ein Segment in Ihrem Bericht angewendet haben, stimmen die Segmentkriterien möglicherweise nicht mit den Daten überein. Versuchen Sie, das Segment zu entfernen oder die Segmentdefinition anzupassen.
* Überprüfen Sie den Datumsbereich oben rechts und stellen Sie sicher, dass er auf einen erwarteten Wert eingestellt ist.
* Navigieren Sie zu Ihrer Website und überprüfen Sie mit dem [Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=de), ob Daten erfasst werden.


+++

+++Welche Aktionen können Benutzende mit Leserechten in Analysis Workspace durchführen?
Wenn ein Projekt schreibgeschützt freigegeben wird, sind alle Bearbeitungsfunktionen vollständig deaktiviert, und die Empfängerinnen und Empfänger können das Dropdown-Menü nur ändern, um einen Filter auf vordefinierte Weise auf das Panel anzuwenden.
+++
