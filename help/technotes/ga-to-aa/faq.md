---
title: Häufig gestellte Fragen zur Migration zu Adobe Analytics
description: Erhalten Sie Antworten auf häufig gestellte Fragen, wenn Sie von einer Plattform eines Drittanbieters zu Adobe wechseln.
feature: Third-party Integration
exl-id: 1201909e-b20c-48c5-b287-393da8e22d78
source-git-commit: 6de20d2fbbab6ded6c92f0c6f3536671f4b2ae46
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 74%

---

# Häufig gestellte Fragen zur Migration zu Adobe Analytics

**Wie migriere ich meine historischen Daten von meiner Drittanbieterplattform zu Adobe Analytics?**

Jede Analytics-Plattform verfügt über unterschiedliche Methoden zum Erfassen, Verarbeiten und Speichern von Daten. Anstatt Altdaten zu migrieren, empfiehlt Adobe, ein klares Umstellungsdatum festzulegen, ab dem Daten in Adobe Analytics erfasst und verwendet werden. Beliebte Umstellungsdaten sind der Beginn eines Geschäftsjahres, der Beginn eines Kalenderjahres oder der Beginn eines Kalendermonats. Wenn Anwender Altdaten anzeigen möchten, können sie sich bei der Drittanbieterplattform anmelden, um spezielle Anforderungen hinsichtlich Verlaufsberichten zu erfüllen.

Wenden Sie sich an Ihr Adobe-Kundenbetreuungsteam, wenn Sie Altdaten in Adobe übertragen möchten. Ein Implementierungsberater kann mit Ihrem Unternehmen zusammenarbeiten, um einen Google Analytics-Datenexport in eine Datenquelle zu übersetzen, die in die Adobe-Datenerfassungs-Server eingespeist werden kann.

Für die Übertragung historischer Daten empfehlen wir [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=de), das beliebige Omni-Channel-Datenquellen einbringen kann.

**Ich bin es gewohnt, in vielen meiner Berichte eine Dropdownliste zur Segmentierung aufzurufen. Wie erhalte ich eine solche Funktion in [!UICONTROL Analysis Workspace]?**

Dropdown-Filter sind eine flexible und zuverlässige Funktion in [!UICONTROL Analysis Workspace] , die eine Dropdown-Liste für die Segmentierung ermöglicht. In einem Workspace-Projekt:

1. Verwenden Sie Strg+Klicken (Windows) oder Befehl+Klicken (Mac) für die Komponenten, die Sie in den Dropdown-Filter aufnehmen möchten. Sie sind nicht auf Segmente beschränkt. Jede Komponente kann in einen Dropdown-Filter aufgenommen werden.
2. Ziehen Sie die Gruppe von Komponenten in den Arbeitsbereich mit der Bezeichnung „Segment hier ablegen“. Halten Sie vor dem Loslassen die Umschalttaste gedrückt.

Benutzer, die darauf zugreifen [!UICONTROL Arbeitsbereich] -Projekt kann jetzt diesen Dropdown-Filter verwenden, um Segmente oder andere Komponenten auf das Projekt anzuwenden. Weitere Informationen finden Sie unter [Bedienfelder – Übersicht](/help/analyze/analysis-workspace/c-panels/panels.md) im Handbuch zu Adobe Analytics-Tools.

**Ich bin es gewohnt, auf ein Dimensionselement zu klicken, um einen Drilldown zu sehen. Wie kann ich diesen einfachen Workflow in Analysis Workspace replizieren?**

Dimensionselemente in [!UICONTROL Analysis Workspace] verfügen auch über einen einfachen Aufschlüsselungs-Workflow. Greifen Sie darauf zu, indem Sie mit der rechten Maustaste statt mit der linken klicken. Klicken Sie mit der rechten Maustaste auf ein Dimensionselement, klicken Sie auf [!UICONTROL Aufschlüsselung] und wählen Sie dann die gewünschte Komponente aus. Sie können dieselbe Aufschlüsselung auf mehrere Dimensionselemente anwenden, indem Sie bei gedrückter Strg- (Windows) bzw. Befehlstaste (Mac) auf die Werte klicken.
