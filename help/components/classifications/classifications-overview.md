---
title: Übersicht über Klassifizierungen
description: Passen Sie die Gruppierung von Dimensionselementen an.
feature: Classifications
exl-id: 0d2c77ea-610f-48e0-b6a2-6e91794783b1
source-git-commit: 1e209d4313c3d9d67f15a0c3a0939ceeb7a1ed31
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 38%

---

# Übersicht über Klassifizierungen

Eine Klassifizierung ist eine Methode, mit der Sie Analytics-Variablendaten in Kategorien aufgliedern und diese Daten auf unterschiedliche Weise darstellen, wenn Sie einen Bericht erzeugen. Sie stellen eine Beziehung zwischen einem Variablenwert und Metadaten her, die sich auf diesen Wert beziehen. Klassifizierungen können für die meisten benutzerdefinierten Dimensionen verwendet werden, wie [Trackingcode](/help/components/dimensions/tracking-code.md), [Props](/help/components/dimensions/prop.md) und [eVars](/help/components/dimensions/evar.md).

* **Klassifizierungssätze** sind die primären Komponenten zum Klassifizieren von Daten. [Klassifizierungssätze](/help/components/classifications/sets/overview.md) ermöglichen Ihnen die Erstellung und Verwaltung von Klassifizierungen in einer einzigen, vereinfachten Benutzeroberfläche.

* **Legacy-Klassifizierungen** dokumentiert die alten Klassifizierungsmethoden, um Daten zu klassifizieren. Diese Methoden werden nicht mehr unterstützt und sind nach dem 31. August 2026 nicht mehr verfügbar.

   * [Klassifizierungsregeln](/help/components/classifications/crb/classification-rule-builder.md): Erstellen Sie Regeln, die ein bestimmtes Dimensionselement einem Klassifizierungs-Dimensionselement zuweisen. Diese Methode zur Klassifizierung von Daten ist am besten geeignet, wenn eine Dimension häufig auf neue eindeutige Werte trifft oder wenn manuelle Klassifizierungen häufig und aufwändig wären.
   * [Klassifizierungs-Import-Tool](/help/components/classifications/importer/c-working-with-saint.md): Exportieren Sie eine Vorlagentabelle mit Dimensionselementen in jeder Zeile. Spalten stellen jede Klassifizierung für eine Dimension dar. Diese Methode zur Datenklassifizierung eignet sich am besten, wenn alle Dimensionselemente bekannt sind und keine häufige Aktualisierung erforderlich ist.

Eine einzelne Dimension kann mehrere Klassifizierungs-Dimensionen haben. Sie können beispielsweise [!UICONTROL Produkt-IDs] mit zusätzlichen Produktattributen wie Produktname, Farbe, Größe, Beschreibung und SKU klassifizieren. Jedes dieser Attribute wäre eine separate Klassifizierungsdimension, die zur gleichen übergeordneten Dimension gehört. Wenn Sie Ihre Berichte um diese Attribute erweitern, erhalten Sie tiefere und komplexere Berichtsmöglichkeiten. Sobald eine Dimension Klassifizierungsdaten enthält, ist die Klassifizierungsdimension in Berichten verfügbar, die nur Klassifizierungsdimensionselemente enthalten. Jedes übergeordnete Dimensionselement, das keinen Classification-Wert enthält, wird unter &quot;[&quot; ](/help/technotes/unspecified.md)
