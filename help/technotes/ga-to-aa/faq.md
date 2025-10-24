---
title: Häufig gestellte Fragen zur Migration zu Adobe Analytics
description: Erhalten Sie Antworten auf häufig gestellte Fragen, wenn Sie von einer Plattform eines Drittanbieters zu Adobe wechseln.
feature: Third-party Integration
exl-id: 1201909e-b20c-48c5-b287-393da8e22d78
source-git-commit: 58d53d6013abcd7d99f2c3cb640d6a648a4ef360
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 53%

---

# Häufig gestellte Fragen zur Migration zu Adobe Analytics

**Wie migriere ich meine historischen Daten von meiner Drittanbieterplattform zu Adobe Analytics?**

Jede Analytics-Plattform verfügt über unterschiedliche Methoden zum Erfassen, Verarbeiten und Speichern von Daten. Anstatt Altdaten zu migrieren, empfiehlt Adobe, ein klares Umstellungsdatum festzulegen, ab dem Daten in Adobe Analytics erfasst und verwendet werden. Beliebte Umstellungsdaten sind der Beginn eines Geschäftsjahres, der Beginn eines Kalenderjahres oder der Beginn eines Kalendermonats. Wenn Anwender Altdaten anzeigen möchten, können sie sich bei der Drittanbieterplattform anmelden, um spezielle Anforderungen hinsichtlich Verlaufsberichten zu erfüllen.

Wenn Ihr Unternehmen daran zweifelt, historische Daten nach Adobe portieren zu lassen, wenden Sie sich an Ihr Adobe-Accountteam. Ein Implementierungsberater kann mit Ihrem Unternehmen zusammenarbeiten, um einen Google Analytics-Datenexport in eine Datenquelle zu übersetzen, die in die Adobe-Datenerfassungs-Server eingespeist werden kann.

Für die Übertragung historischer Daten wird die Verwendung von [Customer Journey Analytics](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-overview/cja-overview) empfohlen, wodurch jede beliebige Omni-Channel-Datenquelle eingebunden werden kann.

**Ich bin es gewohnt, in vielen meiner Berichte eine Dropdown-Liste zur Segmentierung aufzurufen. Wie erhalte ich eine solche Funktion in [!UICONTROL Analysis Workspace]?**

Dropdown-Filter sind eine flexible und zuverlässige Funktion in [!UICONTROL Analysis Workspace] die eine Dropdown-Liste für die Segmentierung ermöglicht. In einem Workspace-Projekt:

1. Verwenden Sie ***Strg***+***Klick*** (Windows) oder ***Befehlstaste***+***Klick*** (Mac) für die Komponenten, die Sie in den Dropdown-Filter aufnehmen möchten. Sie sind nicht auf Segmente beschränkt. Jede Komponente kann in einem Dropdown-Filter enthalten sein.
2. Ziehen Sie die Gruppe der Komponenten in den Arbeitsbereich mit der Bezeichnung *Segment hier ablegen*. Bevor Sie loslassen, halten Sie **[!UICONTROL Shift]**.

Benutzende, die auf dieses [!UICONTROL Workspace]-Projekt zugreifen, können jetzt diesen Dropdown-Filter verwenden, um Segmente oder andere Komponenten auf das Projekt anzuwenden. Weitere Informationen finden Sie unter [Bedienfelder – Übersicht](/help/analyze/analysis-workspace/c-panels/panels.md) im Handbuch zu Adobe Analytics-Tools.

**Ich bin es gewohnt, auf ein Dimensionselement zu klicken, um einen Drilldown zu sehen. Wie kann ich diesen einfachen Workflow in Analysis Workspace replizieren?**

Dimensionselemente in [!UICONTROL Analysis Workspace] verfügen auch über einen einfachen Aufschlüsselungs-Workflow. Greifen Sie auf die Aufschlüsselung zu, indem Sie das Kontextmenü für ein Dimensionselement verwenden. Wählen Sie dann **[!UICONTROL Aufschlüsselung]** und die gewünschte Komponente aus. Sie können dieselbe Aufschlüsselung auf mehrere Dimensionselemente anwenden, indem Sie für jeden Wert ***Strg***+***Auswählen*** (Windows) oder ***Befehlstaste***+***Auswählen*** (Mac) verwenden.
