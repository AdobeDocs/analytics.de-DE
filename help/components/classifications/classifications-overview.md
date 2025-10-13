---
title: Übersicht über Klassifizierungen
description: Passen Sie die Gruppierung von Dimensionselementen an.
feature: Classifications
exl-id: 0d2c77ea-610f-48e0-b6a2-6e91794783b1
source-git-commit: a40f30bbe8fdbf98862c4c9a05341fb63962cdd1
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 39%

---

# Übersicht über Klassifizierungen

Eine Klassifizierung ist eine Methode, mit der Sie Analytics-Variablendaten in Kategorien aufgliedern und diese Daten auf unterschiedliche Weise darstellen, wenn Sie einen Bericht erzeugen. Sie stellen eine Beziehung zwischen einem Variablenwert und Metadaten her, die sich auf diesen Wert beziehen. Klassifizierungen können für die meisten benutzerdefinierten Dimensionen verwendet werden, wie [Trackingcode](/help/components/dimensions/tracking-code.md), [Props](/help/components/dimensions/prop.md) und [eVars](/help/components/dimensions/evar.md).

**Klassifizierungssätze** sind die primäre Möglichkeit, Daten zu klassifizieren. **Klassifizierungsregeln** und der **Klassifizierungs-Importer** sind veraltete Methoden zum Klassifizieren von Daten. Alle Klassifizierungsdaten funktionieren im Reporting letztendlich gleich. Sie können jede dieser Methoden kombinieren, um den Workflow Ihres Unternehmens optimal zu erfüllen.

* **Klassifizierungssätze**: Erstellen und verwalten Sie Klassifizierungen und deren Regeln auf einer einzigen, vereinfachten Benutzeroberfläche.
* **Klassifizierungsregeln** (veraltet): Erstellen Sie Regeln, die ein bestimmtes Dimensionselement einem Klassifizierungsdimensionselement zuweisen. Diese Methode zur Klassifizierung von Daten ist am besten geeignet, wenn eine Dimension häufig auf neue eindeutige Werte trifft oder wenn manuelle Klassifizierungen häufig und aufwändig wären.
* **Classification Importer** (veraltet): Exportieren Sie eine Vorlagenkalkulationstabelle mit Dimensionselementen in jeder Zeile. Spalten stellen jede Klassifizierung für eine Dimension dar. Diese Methode zur Datenklassifizierung eignet sich am besten, wenn alle Dimensionselemente bekannt sind und keine häufige Aktualisierung erforderlich ist.

Eine einzelne Dimension kann mehrere Klassifizierungs-Dimensionen haben. Sie können beispielsweise [!UICONTROL Produkt-IDs] mit zusätzlichen Produktattributen wie Produktname, Farbe, Größe, Beschreibung und SKU klassifizieren. Jedes dieser Attribute wäre eine separate Klassifizierungsdimension, die zur gleichen übergeordneten Dimension gehört. Wenn Sie Ihre Berichte um diese Attribute erweitern, erhalten Sie tiefere und komplexere Berichtsmöglichkeiten. Sobald eine Dimension Klassifizierungsdaten enthält, ist die Klassifizierungsdimension in Berichten verfügbar, die nur Klassifizierungsdimensionselemente enthalten. Jedes übergeordnete Dimensionselement, das keinen Classification-Wert enthält, wird unter &quot;[&quot; &#x200B;](/help/technotes/unspecified.md)
