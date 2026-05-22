---
title: Häufig gestellte Fragen zur Migration zu Adobe Analytics
description: Erhalten Sie Antworten auf häufig gestellte Fragen, wenn Sie von einer Plattform eines Drittanbieters zu Adobe wechseln.
feature: Third-party Integration
exl-id: 1201909e-b20c-48c5-b287-393da8e22d78
TQID: https://experienceleague.adobe.com/NJPnGHUG-9krAfzRZiNbMd7DS9q5gRGTm-1KM3DMXag
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2: id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: e38cbddc-1633-4cd5-bed5-9f289f2a6029
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 418
ht-degree: 54%

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
