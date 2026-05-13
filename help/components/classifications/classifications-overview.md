---
title: Übersicht über Klassifizierungen
description: Passen Sie die Gruppierung von Dimensionselementen an.
feature: Classifications
exl-id: 0d2c77ea-610f-48e0-b6a2-6e91794783b1
TQID: https://experienceleague.adobe.com/raB90u-JEBgDroQPLC1eCSmxs4V-J7Av8Snr6oeKwvk
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 309
ht-degree: 84%

---

# Übersicht über Klassifizierungen

Eine Klassifizierung ist eine Methode, mit der Sie Analytics-Variablendaten in Kategorien aufgliedern und diese Daten auf unterschiedliche Weise darstellen, wenn Sie einen Bericht erzeugen. Sie stellen eine Beziehung zwischen einem Variablenwert und Metadaten her, die sich auf diesen Wert beziehen. Klassifizierungen können für die meisten benutzerdefinierten Dimensionen wie [Trackingcode](/help/components/dimensions/tracking-code.md), [Props](/help/components/dimensions/prop.md) und [eVars](/help/components/dimensions/evar.md) verwendet werden.

* **Klassifizierungssätze** sind die wichtigsten Komponenten zum Klassifizieren von Daten. Mit [Klassifizierungssätzen](/help/components/classifications/sets/overview.md) können Sie auf einer einheitlichen, einfachen Oberfläche Klassifizierungen erstellen und verwalten.

* **Legacy-Klassifizierungen** dokumentiert die alten Klassifizierungsmethoden zum Klassifizieren von Daten. Diese Methoden werden in naher Zukunft nicht mehr unterstützt und nicht mehr zugänglich sein.

   * [Klassifizierungsregeln](/help/components/classifications/crb/classification-rule-builder.md): Erstellen Sie Regeln, die ein bestimmtes Dimensionselement einem Klassifizierungs-Dimensionselement zuweisen. Diese Methode zum Klassifizieren von Daten eignet sich am besten, wenn eine Dimension häufig neue eindeutige Werte findet oder wenn eine manuelle Klassifizierung häufig und aufwendig wäre. Diese Funktion wird nach dem 28. Februar 2027 eingestellt.

   * [Klassifizierungs-Import-Tool](/help/components/classifications/importer/c-working-with-saint.md): Exportieren Sie eine Vorlagentabelle mit Dimensionselementen in jeder Zeile. Spalten stellen jede Klassifizierung für eine Dimension dar. Diese Methode zur Datenklassifizierung eignet sich am besten, wenn alle Dimensionselemente bekannt sind und keine häufige Aktualisierung erforderlich ist. Diese Funktion wird nach dem 31. August 2026 eingestellt. Mit der Einstellung können Sie keine Klassifizierungen mehr über Standard-FTP importieren.

Eine einzelne Dimension kann mehrere Klassifizierungsdimensionen haben. Sie können beispielsweise [!UICONTROL Produkt-IDs] mit zusätzlichen Produktattributen wie Produktname, Farbe, Größe, Beschreibung und SKU klassifizieren. Jedes dieser Attribute wäre eine separate Klassifizierungsdimension, die zur selben übergeordneten Dimension gehört. Wenn Sie Ihre Berichte um diese Attribute erweitern, erhalten Sie tiefere und komplexere Reporting-Möglichkeiten. Sobald eine Dimension Klassifizierungsdaten enthält, ist die Klassifizierungsdimension im Reporting verfügbar, das nur Dimensionselemente für die Klassifizierung enthält. Jedes übergeordnete Dimensionselement, das keinen Klassifizierungswert enthält, wird unter [Nicht angegeben](/help/technotes/unspecified.md) zusammengefasst.
