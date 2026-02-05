---
title: Übersicht über Klassifizierungen
description: Passen Sie die Gruppierung von Dimensionselementen an.
feature: Classifications
exl-id: 0d2c77ea-610f-48e0-b6a2-6e91794783b1
source-git-commit: 1e209d4313c3d9d67f15a0c3a0939ceeb7a1ed31
workflow-type: ht
source-wordcount: '273'
ht-degree: 100%

---

# Übersicht über Klassifizierungen

Eine Klassifizierung ist eine Methode, mit der Sie Analytics-Variablendaten in Kategorien aufgliedern und diese Daten auf unterschiedliche Weise darstellen, wenn Sie einen Bericht erzeugen. Sie stellen eine Beziehung zwischen einem Variablenwert und Metadaten her, die sich auf diesen Wert beziehen. Klassifizierungen können für die meisten benutzerdefinierten Dimensionen wie [Trackingcode](/help/components/dimensions/tracking-code.md), [Props](/help/components/dimensions/prop.md) und [eVars](/help/components/dimensions/evar.md) verwendet werden.

* **Klassifizierungssätze** sind die wichtigsten Komponenten zum Klassifizieren von Daten. Mit [Klassifizierungssätzen](/help/components/classifications/sets/overview.md) können Sie auf einer einheitlichen, einfachen Oberfläche Klassifizierungen erstellen und verwalten.

* **Legacy-Klassifizierungen** dokumentiert die alten Klassifizierungsmethoden zum Klassifizieren von Daten. Diese Methoden sind veraltet und sind nach dem 31. August 2026 nicht mehr zugänglich.

   * [Klassifizierungsregeln](/help/components/classifications/crb/classification-rule-builder.md): Erstellen Sie Regeln, die ein bestimmtes Dimensionselement einem Klassifizierungs-Dimensionselement zuweisen. Diese Methode zum Klassifizieren von Daten eignet sich am besten, wenn eine Dimension häufig neue eindeutige Werte findet oder wenn eine manuelle Klassifizierung häufig und aufwendig wäre.
   * [Klassifizierungs-Import-Tool](/help/components/classifications/importer/c-working-with-saint.md): Exportieren Sie eine Vorlagentabelle mit Dimensionselementen in jeder Zeile. Spalten stellen jede Klassifizierung für eine Dimension dar. Diese Methode zur Datenklassifizierung eignet sich am besten, wenn alle Dimensionselemente bekannt sind und keine häufige Aktualisierung erforderlich ist.

Eine einzelne Dimension kann mehrere Klassifizierungsdimensionen haben. Sie können beispielsweise [!UICONTROL Produkt-IDs] mit zusätzlichen Produktattributen wie Produktname, Farbe, Größe, Beschreibung und SKU klassifizieren. Jedes dieser Attribute wäre eine separate Klassifizierungsdimension, die zur selben übergeordneten Dimension gehört. Wenn Sie Ihre Berichte um diese Attribute erweitern, erhalten Sie tiefere und komplexere Reporting-Möglichkeiten. Sobald eine Dimension Klassifizierungsdaten enthält, ist die Klassifizierungsdimension im Reporting verfügbar, das nur Dimensionselemente für die Klassifizierung enthält. Jedes übergeordnete Dimensionselement, das keinen Klassifizierungswert enthält, wird unter [Nicht angegeben](/help/technotes/unspecified.md) zusammengefasst.
