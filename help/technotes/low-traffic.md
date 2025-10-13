---
description: Wenn ein Bericht viele eindeutige Werte aufweist, verwendet Adobe das Dimensionselement „Geringer Traffic“, um die Berichtsleistung zu verbessern.
title: Wert „Geringer Datenverkehr“ in Adobe Analytics
feature: Metrics, Data Configuration and Collection
exl-id: 6c3d8258-cf75-4716-85fd-ed8520a2c9d5
source-git-commit: 42d044c3c56f13a232b721ef60f64bcf622ffa9f
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 8%

---

# [!UICONTROL Geringer Traffic]-Wert in Adobe Analytics

Wenn eine Dimension Millionen eindeutiger Werte enthält, stellt Adobe eine Funktion bereit, mit der sichergestellt wird, dass die wichtigsten Werte zeitnah im Bericht angezeigt werden. Eindeutige Werte, die über einen bestimmten Schwellenwert hinaus erfasst wurden, werden unter einem Dimensionselement mit der Bezeichnung **[!UICONTROL Geringer Traffic]** aufgeführt.

Mit dem Dimensionselement [!UICONTROL Geringer Traffic] kann Adobe sicherstellen, dass Berichte rechtzeitig zurückgegeben werden, indem übermäßige eindeutige Werte erfasst und in Buckets zusammengefasst werden.

Beachten Sie[!UICONTROL  dass die Logik „Geringer Traffic] am besten mit Dimensionen funktioniert, die Elemente haben, die im Laufe des Monats oft wiederkehren. Wenn Dimensionselemente bei jedem Treffer nahezu oder vollständig eindeutig sind, erreicht die Anzahl der eindeutigen Werte schnell den Schwellenwert, und alle nachfolgenden Werte für den Monat landen im Bereich [!UICONTROL Geringer Traffic].

## Eingabe von Werten [!UICONTROL Low-Traffic]

Standardmäßig wird ein Schwellenwert von **2.000.000 eindeutigen Werten** pro Dimension, pro Report Suite und pro Kalendermonat festgelegt. Dimension-Elemente, die diesen eindeutigen Wertschwellenwert überschreiten, werden unter [!UICONTROL Geringer Traffic“ ].

* Dimension-Elemente, die vor Erreichen des Schwellenwerts gesammelt wurden, werden normal berechnet.
* Dimension-Elemente, die nach Überschreiten des Schwellenwerts gesammelt werden, werden unter [!UICONTROL Geringer Traffic“ ].

>[!NOTE]
>Die Dimension [Seite](../components/dimensions/page.md) verwendet mehrere Backend-Spalten, die alle auf den eindeutigen Schwellenwert angerechnet werden, einschließlich `pagename`, `page_url`, `first_hit_pagename`, `first_hit_page_url`, `visit_pagename`, `visit_page_url` und `click_context`. Diese Backend-Spalten können dazu führen[!UICONTROL  dass Logik vom Typ „Geringer Traffic] angewendet wird, lange bevor die Anzahl der Dimensionselemente „Eindeutige Seite“ in Workspace den Schwellenwert erreicht.

Das Limit von 2.000.000 Unique kann für jede Dimension geändert werden. Siehe [Ändern der eindeutigen Grenzwerte](#changing-unique-limit-thresholds) unten. Am Ende eines Kalendermonats wird die Anzahl der verfolgten eindeutigen Werte global zurückgesetzt.

## Wie Werte nach Überschreiten [!UICONTROL  Schwellenwerts mit „Low-Traffic] escapen können

Wenn eine bestimmte Dimension in einem bestimmten Monat mehr als 2.000.000 eindeutige Werte erfasst, können einzelne Dimensionselemente zum Bericht über ihr eigenes Dimensionselement zurückkehren. Der primäre Anwendungsfall dieser Funktion besteht darin, das Reporting von wichtigen Dimensionselementen zu ermöglichen, die möglicherweise Ende des Monats, nachdem der eindeutige Schwellenwert überschritten wurde, einen Popularitätsschub erhalten. Wenn Ihr Unternehmen beispielsweise eine Website mit Millionen von Artikeln betreibt und gegen Ende des Monats ein neuer Artikel beliebt wird, können Sie die Leistung dieses Artikels dennoch analysieren. Mit dieser Logik soll nicht alles, was eine bestimmte Anzahl von Instanzen erhält, aus einem Bucket entfernt werden. Sie bietet vielmehr eine Möglichkeit, Inhalte zu analysieren, die einen Zustrom von Traffic erhalten.

Die Anforderungen an das Entweichen eines einzelnen Dimensionselements [!UICONTROL Low-Traffic] hängen von vielen Faktoren ab, von denen viele die Möglichkeit verhindern, einen genauen Schwellenwert zu berechnen:

* **Anzahl der Server, die Daten für die Report Suite verarbeiten**: Report Suites mit höherem Traffic erfordern mehr Instanzen eines einzelnen Dimensionselements, um [!UICONTROL Geringer Traffic) ].
* **Zeitraum zwischen den einzelnen Dimensionselementinstanzen**: Treffer, die ein über den Tag verteiltes Dimensionselement enthalten, erfordern mehr Instanzen als einen konzentrierten Trefferanstieg.
* **Anzahl der eindeutigen Werte für die Dimension**: Für jede Dimension ist ein zweiter Schwellenwert standardmäßig auf 2.100.000 eindeutige Werte festgelegt. Wenn die Anzahl der eindeutigen Werte in einer Dimension diesen höheren Schwellenwert überschreitet, wird eine sehr viel aggressivere Filterung angewendet.

Unter Berücksichtigung der oben genannten Faktoren ist davon auszugehen **dass** Hunderte bis Tausende“ Instanzen für ein einzelnes Dimensionselement [!UICONTROL Geringer Traffic) ], wenn nur der erste Schwellenwert überschritten wird. Es wird erwartet **dass (Tausende bis Zehntausende** Instanzen für ein einzelnes Dimensionselement [!UICONTROL Geringer Traffic) ], wenn der höhere Schwellenwert überschritten wird. Adobe garantiert nicht, dass Dimensionselemente zuverlässig dem Bucket [!UICONTROL Geringer Traffic] entweichen. Dieses Konzept ist in der Regel für Dimensionselemente mit ungewöhnlich hohem Volumen am Ende des Monats reserviert.

Wenn ein Dimensionselement aus dem Bucket [!UICONTROL Geringer Traffic] austritt, bleiben Instanzen, die vor dem Traffic-Zufluss erfasst wurden, unter [!UICONTROL Geringer Traffic].

## Ändern der Schwellenwerte für eindeutige Werte

Schwellenwerte können manchmal auf Basis einzelner Dimensionen geändert werden. Wenden Sie sich an die Kundenunterstützung von Adobe oder Ihr Adobe-Accountteam, um diese Änderung anzufordern. Das Ausmaß, in dem die Schwellenwerte erhöht werden können, hängt von mehreren Faktoren ab; Adobe garantiert nicht, dass alle Anforderungen zur Erhöhung der Schwellenwerte berücksichtigt werden können. Fügen Sie Änderungsanforderungen Folgendes hinzu:

* Die Report Suite-ID
* Die Dimension, für die Sie den Schwellenwert erhöhen möchten
* Sowohl der erste als auch der zweite Schwellenwert sind erwünscht:
   * Der erste Schwellenwert (anfängliches Bucketing) ist standardmäßig auf **2.000.000** festgelegt.
   * Der zweite Schwellenwert (aggressivere Filterung) ist standardmäßig auf **2.100.000** festgelegt.

>[!IMPORTANT]
>
>Änderungen an Schwellenwerten können sich auf die Berichtsleistung auswirken. Adobe empfiehlt dringend, bei der Anforderung einer Erhöhung auf eindeutige Werte für eine Dimension Vorsicht walten zu lassen. Erhöhen Sie nur eindeutige Beschränkungen für Dimensionen, die für die Reporting-Anforderungen Ihres Unternehmens wichtig sind.

[!UICONTROL Geringer Traffic]-Schwellenwerte sind in der Analytics-Benutzeroberfläche nicht sichtbar. Wenden Sie sich an die Kundenunterstützung von Adobe, wenn Sie weitere Informationen zu den vorhandenen Schwellenwerten wünschen.

## Interaktionen mit anderen Funktionen

Verschiedene Funktionen behandeln [!UICONTROL Low-Traffic]-Werte unterschiedlich.

* **Data Warehouse:** In den meisten Fällen gibt es keine Begrenzung für die Anzahl der eindeutigen Werte in Data Warehouse-Berichten. Seine eindeutige Architektur ermöglicht die Berichterstellung einer beliebigen Anzahl eindeutiger Werte. Werte [!UICONTROL Geringer Traffic] können jedoch in einigen eingeschränkten Szenarien weiterhin angezeigt werden. Beispiele sind Listenvariablen, Listen-Props, Merchandising-eVars und Marketing-Kanal-Detaildimensionen.
* **Segmentierung:** Wenn die Segmentkriterien eine Dimension mit einer hohen Anzahl eindeutiger Werte enthalten, werden Werte, die unter [!UICONTROL Geringer Traffic] erfasst werden, nicht einbezogen.
* **Klassifizierungen:** Auch Klassifizierungsberichte unterliegen eindeutigen Beschränkungen. Wenn das übergeordnete Dimensionselement einer Klassifizierung unter „Geringer [!UICONTROL &quot; enthalten ist] wird der Wert nicht klassifiziert.
   * [!UICONTROL Geringer Datenverkehr] Werte, die über den Importer klassifiziert werden, können in Data Warehouse angezeigt werden. <!-- AN-115871 -->
   * [!UICONTROL Geringer Traffic]-Werte, die über den Regel-Builder klassifiziert *können* in Data Warehouse angezeigt werden. <!-- AN-122872 -->
