---
description: Wenn ein Bericht viele eindeutige Werte aufweist, verwendet Adobe das Dimensionselement „Geringer Traffic“, um die Berichtsleistung zu verbessern.
title: Wert „Geringer Datenverkehr“ in Adobe Analytics
feature: Metrics, Data Configuration and Collection
exl-id: 6c3d8258-cf75-4716-85fd-ed8520a2c9d5
source-git-commit: f242ec6613cf046224f76f7edc7813a34c65fff8
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 77%

---

# Wert „Geringer Datenverkehr“ in Adobe Analytics

Wenn ein Bericht zahlreiche eindeutige Werte aufweist, kann mit Adobe nun sichergestellt werden, dass die wichtigsten Werte in Ihrem Bericht auftauchen. Eindeutige Variablenwerte, die über einen bestimmten Schwellenwert hinausgehend gesammelt werden (siehe unten), werden unter einem Dimensionselement mit der Bezeichnung **[!UICONTROL Geringer Traffic]** aufgeführt.

## So funktioniert [!UICONTROL Geringer Traffic]

* Adobe Analytics verwendet zwei Schwellenwerte, um zu bestimmen, welche eindeutigen Werte jeden Monat in Berichten angezeigt werden: einen **[!UICONTROL niedrigen Schwellenwert]** und einen **[!UICONTROL hohen Schwellenwert]**. Diese Schwellenwerte können von Zeit zu Zeit durch Adobe angepasst werden. Die aktuellen Schwellenwerte sind:
   * **[!UICONTROL Niedriger Schwellenwert]**: 2.000.000 eindeutige Werte während des Monats.
   * **[!UICONTROL Hoher Schwellenwert]**: 2.100.000 eindeutige Werte während des Monats.
* Die Berichterstellung ist nicht betroffen, wenn eine Variable den niedrigen Schwellenwert in einem bestimmten Monat nicht erreicht.
* Wenn eine Variable den niedrigen Schwellenwert erreicht, werden Daten unter einem Dimensionselement mit der Bezeichnung [!UICONTROL Geringer Traffic“ ]. Jeder Wert, der über diesen Schwellenwert hinausgeht, durchläuft die folgende Logik:
   * Wenn ein Wert bereits in Berichten enthalten ist, wird er wie gewohnt hinzugefügt.
   * Wenn ein Wert noch nicht in Berichten angezeigt wird, fügen Sie ihn zunächst zum Dimensionselement [!UICONTROL Geringer Traffic] hinzu.
   * Wenn ein Wert, der unter [!UICONTROL Geringer Traffic] zusammengefasst wird, einen Traffic-Zufluss erhält (normalerweise Instanzen im zweistelligen Bereich an einem Tag), erkennen Sie ihn als sein eigenes Dimensionselement. Instanzen, die vor dem Traffic-Zustrom erfasst wurden, verbleiben unter [!UICONTROL Geringer Traffic]. Der genaue Zeitpunkt, zu dem das Dimensionselement in Berichten angezeigt wird, weist viele Abhängigkeiten auf. Dazu gehören die Anzahl der Server, die Daten für die Report Suite verarbeiten, und die Zeitspanne zwischen den einzelnen Dimensionselementinstanzen.
* Erreicht eine Variable den hohen Schwellenwert, wird eine aggressivere Filterung angewendet. Eindeutige Werte erfordern Instanzen im dreistelligen Bereich an einem Tag, bevor sie als eigenes Dimensionselement erkannt werden.

Diese Logik ermöglicht es Adobe, die Berichterstellungsfunktionen zu optimieren, während Ihr Unternehmen weiterhin wichtige Dimensionselemente melden kann, die später im Monat erfasst werden. Wenn Ihr Unternehmen beispielsweise eine Site mit Millionen von Artikeln betreibt und gegen Ende des Monats ein neuer Artikel sehr nachgefragt ist (nachdem er beide eindeutigen Schwellenwerte überschritten hat), können Sie die Leistung dieses Artikels dennoch analysieren, ohne dass der Artikel unter [!UICONTROL Geringer Traffic] erfasst wird. Diese Logik strebt nicht an, alle Elemente aus dem Bucket entfernen, die eine bestimmte Anzahl von Seitenaufrufen pro Tag oder Monat erhalten.

>[!NOTE]
>Die Dimension [Seite](../components/dimensions/page.md) verwendet mehrere Backend-Spalten, die alle auf eindeutige Schwellenwerte angerechnet werden, darunter `pagename`, `page_url`, `first_hit_pagename`, `first_hit_page_url`, `visit_pagename`, `visit_page_url` und `click_context`. Diese Backend-Spalten können die Anwendung der Logik [!UICONTROL Geringer Traffic] verursachen, bevor die Anzahl der eindeutigen Dimensionselemente „Seite“ in Workspace den unteren Schwellenwert erreicht.

Beachten Sie, dass Logik mit geringem Traffic am besten mit Variablen funktioniert, die Dimensionselemente haben, die im Verlauf des Monats oft wiederkehren. Wenn die Dimensionselemente einer Variablen bei jedem Treffer fast oder vollständig eindeutig sind, erreicht die Anzahl der eindeutigen Werte der Variablen schnell beide Schwellenwerte und alle nachfolgenden Dimensionselemente für den Monat landen im Bereich für geringen Traffic.

## Ändern der Schwellenwerte für eindeutige Werte

Schwellenwertbeschränkungen können manchmal variablenweise geändert werden. Wenden Sie sich an die Kundenunterstützung von Adobe oder Ihr Adobe-Accountteam, um diese Änderung anzufordern. Das Ausmaß, in dem die Schwellenwerte erhöht werden können, hängt von mehreren Faktoren ab. Dabei ist Adobe möglicherweise nicht in der Lage, Schwellenwerterhöhungen in allen Fällen zu berücksichtigen. Fügen Sie Änderungsanforderungen Folgendes hinzu:

* Die Report Suite-ID
* Die Variable, für die Sie den Schwellenwert erhöhen möchten
* Sowohl den ersten als auch den zweiten gewünschten Schwellenwert

Änderungen an Schwellenwerten können sich auf die Berichtsleistung auswirken. Adobe empfiehlt dringend, bei der Anforderung einer Erhöhung der eindeutigen Werte in einer Variablen achtsam vorzugehen. Erhöhen Sie nur die eindeutigen Beschränkungen für Variablen, die für die Anforderungen Ihres Unternehmens an die Berichterstellung von entscheidender Bedeutung sind.

Schwellenwerte für niedrigen Traffic sind in der Analytics-Benutzeroberfläche nicht sichtbar. Wenden Sie sich an die Kundenunterstützung von Adobe, wenn Sie weitere Informationen zu den vorhandenen Schwellenwerten wünschen.

## „Geringer Datenverkehr“ mit Komponenten und anderen Funktionen

Verschiedene Funktionen behandeln Werte mit geringem Traffic auf unterschiedliche Weise.

* **Data Warehouse:** Die Anzahl der eindeutigen Werte in Data-Warehouse-Berichten ist unbegrenzt. Die einzigartige Architektur ermöglicht das Reporting beliebig vieler eindeutiger Werte.
   * In einigen eingeschränkten Szenarien können weiterhin „Geringer Datenverkehr“-Werte angezeigt werden. Beispiele sind Listenvariablen, Listen-Props, Merchandising-eVars und Marketing-Kanal-Detaildimensionen.
* **Segmentierung:** Wenn die Segmentkriterien eine Variable mit einer hohen Anzahl eindeutiger Werte enthalten, werden unter „Geringer Datenverkehr“ erfasste Werte nicht berücksichtigt.
* **Klassifizierungen:** Auch Klassifizierungsberichte unterliegen eindeutigen Beschränkungen. Wenn der Wert der übergeordneten Variablen einer Classification unter „Geringer Datenverkehr“ fällt, wird der Wert nicht klassifiziert.
   * Klassifizierungswerte für geringen Traffic, die über den Importer bezogen wurden, können in Data Warehouse angezeigt werden. <!-- AN-115871 -->
   * Klassifizierungswerte für geringen Traffic, die über den Regelaufbau erhalten wurden, *können nicht* in Data Warehouse angezeigt werden. <!-- AN-122872 -->
