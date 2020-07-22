---
title: Häufig gestellte Fragen
description: Erhalten Sie Antworten auf häufig gestellte Fragen, wenn Sie von einer Plattform eines Drittanbieters zu Adobe wechseln.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 66%

---


# Häufig gestellte Fragen

**Wie migriere ich meine historischen Daten von meiner Drittanbieterplattform nach Adobe Analytics?**

Jede Analyseplattform verfügt über unterschiedliche Methoden zum Erfassen, Verarbeiten und Speichern von Daten. Anstatt Altdaten zu migrieren, empfiehlt Adobe, ein klares Umstellungsdatum festzulegen, ab dem Daten in Adobe Analytics erfasst und verwendet werden. Beliebte Umstellungsdaten sind der Beginn eines Geschäftsjahres, der Beginn eines Kalenderjahres oder der Beginn eines Kalendermonats. Wenn Anwender Altdaten anzeigen möchten, können sie sich bei der Drittanbieterplattform anmelden, um spezielle Anforderungen hinsichtlich Verlaufsberichten zu erfüllen.

Wenden Sie sich an den Kundenbetreuer Ihres Unternehmens, wenn Sie Altdaten zu Adobe übertragen möchten. Ein Implementierungsberater kann mit Ihrem Unternehmen zusammenarbeiten, um einen Google Analytics-Datenexport in eine Datenquelle zu übersetzen, die in die Adobe-Datenerfassungs-Server eingespeist werden kann.

Adobe empfiehlt nicht, Altdaten zu importieren, da es sich um einen komplexen Prozess handelt, der für Ihr Unternehmen kostenaufwändig ist. Auch die Besucheridentifizierung kann nicht nahtlos zu Adobe übertragen werden, da die verschiedenen Plattformen Besucherinformationen in unterschiedlichen Cookies und Formaten speichern.

**Ich bin es gewohnt, in vielen meiner Berichte eine Dropdown-Liste zur Segmentierung aufzurufen. How can I recreate that in[!UICONTROL Analysis Workspace]?**

Dropdown filters are a flexible and robust feature in [!UICONTROL Analysis Workspace] that allows a segmentation dropdown. In einem Workspace-Projekt:

1. Halten Sie Strg (Windows) oder Befehlstaste (Mac) gedrückt und klicken Sie auf die Komponenten, die Sie in die Dropdown-Liste aufnehmen möchten. Sie sind nicht auf Segmente beschränkt. Jede Komponente kann in einen Dropdown-Filter aufgenommen werden.
2. Ziehen Sie die Gruppe von Komponenten in den Arbeitsbereich mit der Bezeichnung „Segment hier ablegen“. Halten Sie vor dem Loslassen die Umschalttaste gedrückt.

Users accessing this [!UICONTROL Workspace] project can now use this dropdown to apply segments or other components to the project. See [Panels Overview](/help/analyze/analysis-workspace/c-panels/panels.md) in the Adobe Analytics Tools guide for more information.

**Ich bin es gewohnt, auf ein Dimensionselement zu klicken, um einen Drilldown zu sehen. Wie kann ich diesen einfachen Workflow in Analysis Workspace replizieren?**

Dimensionselemente in [!UICONTROL Analysis Workspace] verfügen ebenfalls über einen einfachen Aufschlüsselungsarbeitsablauf. Greifen Sie darauf zu, indem Sie mit der rechten Maustaste statt mit der linken Maustaste klicken. Right-click on a dimension item, click **[!UICONTROL Breakdown], then select the desired component. Sie können die gleiche Aufschlüsselung auf mehrere Dimensionselemente anwenden, indem Sie bei jedem Wert Strg+Klick (Windows) bzw. Cmd+Klick (Mac) verwenden.
