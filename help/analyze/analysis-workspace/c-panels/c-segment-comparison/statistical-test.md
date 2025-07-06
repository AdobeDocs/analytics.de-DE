---
description: Erfahren Sie, wie statistische Tests beim Segmentvergleich verwendet werden.
keywords: Analysis Workspace;Segment IQ
title: Im Segmentvergleich verwendete statistische Tests
feature: Segmentation
role: User, Admin
exl-id: b1c235ca-2eab-48d2-bf11-e8a8c4067d03
source-git-commit: b4c1636bdc9d5be522b16f945a46beabf4f7a733
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 43%

---

# Im Segmentvergleich verwendete statistische Tests

Jede der obersten Vergleichstabellen zeigt einen Differenzwert an. Dieser Wert wird durch verschiedene statistische Tests in Abhängigkeit vom durchgeführten Vergleich ermittelt. Unabhängig davon, welcher Test verwendet wird, wird der Differenzwert jedoch als Wert zwischen 0 und 1 angezeigt.

Ein Score von 0 bedeutet, dass es keinen Unterschied zwischen den beiden Segmenten gibt, und ein Score von 1 bedeutet, dass es einen sehr großen Unterschied zwischen den beiden Segmenten gab. Es gibt zwei Arten von statistischen Tests, mit denen diese Differenzwerte erzeugt werden:

* Für die Tabelle **[!UICONTROL Top]** Metriken wird ein Mann-Whitney-U-Test verwendet,
* Für die **[!UICONTROL Top-Dimension]** Elemente und **[!UICONTROL Top-Segmente]** Tabelle wird ein Risikodifferenzvergleich verwendet.

## Differenzwert der Top-Metriken

In der Tabelle Top-Metriken verwendet das Tool für den Segmentvergleich einen Mann-Whitney-Benutzeroberflächentest mit zwei Beispielen. Dieser Test ist ein nichtparametrischer Gleichheitstest, mit dem die eindimensionalen Wahrscheinlichkeitsverteilungen jeder Metrik für jedes berücksichtigte Segment verglichen werden. Der Differenzwert in der Tabelle der Metriken ist eine Kombination aus dem p-Wert der berechneten U-Statistik (der angibt, wie stochastisch unterschiedlich die beiden Segmente innerhalb einer bestimmten Metrik verteilt sind) und der relativen Größenordnung der beobachteten Differenz. Ein hoher Differenzwert (nahe 1) bedeutet, dass die jeweilige Metrik einen großen relativen Unterschied sowie eine hohe statistische Konfidenz aufweist, dass die Segmente unterschiedlich sind.

## Differenzwerte für Top-Dimensionselemente und Top-Segmente

Für die Berechnung des Differenzwerts der Tabelle der Top-Dimensionselemente und der Top-Segmente wird ein relativer Risikodifferenz-Algorithmus verwendet (vergleichbar mit dem Risikoverhältnis, auch wenn anstelle eines Verhältnisses eine Differenz verwendet wird). Eine Risikodifferenz wird durch Subtraktion der kumulierten Häufigkeiten eines Dimensionselements (oder der Überschneidung mit einem Segment der Segmenttabelle) eines ausgewählten Segments von der eines anderen berechnet. Ein hoher Differenzwert (nahe 1) bedeutet, dass das bestimmte Dimensionselement oder tertiäre Segment in einem der ausgewählten Segmente sehr prominent war und nicht im anderen.

>[!NOTE]
>
>In allen drei Tabellen basiert die Differenzstatistik auf einer geeigneten Stichprobe von Besuchern, damit der Prozess schnellstmöglich ausgeführt werden kann, während er dennoch statistisch genau bleibt. Während der Differenzwert auf einer Stichprobe basiert, handelt es sich bei den in der Tabelle angezeigten Ergebnissen nicht um eine Stichprobe. Damit die statistische Bedeutung sichergestellt ist, basiert jeder statistische Test auf einem dynamischen Zuteilungsalgorithmus, sodass das kleinere Segment eine Stichprobengröße enthält, die eine Fehlergrenze von unter 3 % gewährleistet. Wenn ein Segment nur sehr wenige Besucher (weniger als 1.000) enthält, werden alle verfügbaren Daten anstelle von Beispieldaten verwendet, um die Differenzbewertung zu berechnen.
