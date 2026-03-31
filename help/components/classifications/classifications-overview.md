---
title: Übersicht über Klassifizierungen
description: Passen Sie die Gruppierung von Dimensionselementen an.
feature: Classifications
exl-id: 0d2c77ea-610f-48e0-b6a2-6e91794783b1
source-git-commit: 2e07f1b9495801383b030b2396e5468c39299f50
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 71%

---

# Übersicht über Klassifizierungen

Eine Klassifizierung ist eine Methode, mit der Sie Analytics-Variablendaten in Kategorien aufgliedern und diese Daten auf unterschiedliche Weise darstellen, wenn Sie einen Bericht erzeugen. Sie stellen eine Beziehung zwischen einem Variablenwert und Metadaten her, die sich auf diesen Wert beziehen. Klassifizierungen können für die meisten benutzerdefinierten Dimensionen wie [Trackingcode](/help/components/dimensions/tracking-code.md), [Props](/help/components/dimensions/prop.md) und [eVars](/help/components/dimensions/evar.md) verwendet werden.

* **Klassifizierungssätze** sind die wichtigsten Komponenten zum Klassifizieren von Daten. Mit [Klassifizierungssätzen](/help/components/classifications/sets/overview.md) können Sie auf einer einheitlichen, einfachen Oberfläche Klassifizierungen erstellen und verwalten.

* **Legacy-Klassifizierungen** dokumentiert die alten Klassifizierungsmethoden zum Klassifizieren von Daten. Diese Methoden werden in naher Zukunft nicht mehr unterstützt und nicht mehr zugänglich sein.

   * [Klassifizierungsregeln](/help/components/classifications/crb/classification-rule-builder.md): Erstellen Sie Regeln, die ein bestimmtes Dimensionselement einem Klassifizierungs-Dimensionselement zuweisen. Diese Methode zur Klassifizierung von Daten ist am besten geeignet, wenn eine Dimension häufig auf neue eindeutige Werte trifft oder wenn manuelle Klassifizierungen häufig und aufwändig wären. Diese Funktion wird nach dem 28. Februar 2027 eingestellt.

   * [Klassifizierungs-Import-Tool](/help/components/classifications/importer/c-working-with-saint.md): Exportieren Sie eine Vorlagentabelle mit Dimensionselementen in jeder Zeile. Spalten stellen jede Klassifizierung für eine Dimension dar. Diese Methode zur Klassifizierung von Daten ist am besten geeignet, wenn alle Dimensionselemente bekannt sind und nicht häufig aktualisiert werden müssen. Diese Funktion wird nach dem 31. August 2026 eingestellt. Mit der Einstellung können Sie keine Klassifizierungen mehr über Standard-FTP importieren.

Eine einzelne Dimension kann mehrere Klassifizierungsdimensionen haben. Sie können beispielsweise [!UICONTROL Produkt-IDs] mit zusätzlichen Produktattributen wie Produktname, Farbe, Größe, Beschreibung und SKU klassifizieren. Jedes dieser Attribute wäre eine separate Klassifizierungsdimension, die zur selben übergeordneten Dimension gehört. Wenn Sie Ihre Berichte um diese Attribute erweitern, erhalten Sie tiefere und komplexere Reporting-Möglichkeiten. Sobald eine Dimension Klassifizierungsdaten enthält, ist die Klassifizierungsdimension im Reporting verfügbar, das nur Dimensionselemente für die Klassifizierung enthält. Jedes übergeordnete Dimensionselement, das keinen Klassifizierungswert enthält, wird unter [Nicht angegeben](/help/technotes/unspecified.md) zusammengefasst.
