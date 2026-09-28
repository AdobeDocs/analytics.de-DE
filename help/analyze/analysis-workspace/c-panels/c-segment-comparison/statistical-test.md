---
description: Erfahren Sie, wie statistische Tests beim Segmentvergleich verwendet werden.
keywords: Analysis Workspace;Segment IQ
title: Im Segmentvergleich verwendete statistische Tests
feature: Segmentation
role: User, Admin
exl-id: b1c235ca-2eab-48d2-bf11-e8a8c4067d03
TQID: 'https://experienceleague.adobe.com/49kZ6LC9OMizQvqxE2PCq1LtqhUHtf5iKQUgpgqSmmE'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
    internal-label: Analysis Workspace
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
    internal-label: Dashboards
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
    internal-label: Data configuration and collection
subfeature_v2:
  - id: e38cbddc-1633-4cd5-bed5-9f289f2a6029
    internal-label: Panels
  - id: c47a19a5-f47b-4e53-afe0-e230da195ebe
    internal-label: Segmentation
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: 9a50beeb0aa51cf9f4baf212566947c14029ce8e
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 9%
---
# Im Segmentvergleich verwendete statistische Tests

Jede der obersten Vergleichstabellen zeigt einen Differenzwert an. Dieser Wert wird durch verschiedene statistische Tests in Abhängigkeit vom durchgeführten Vergleich ermittelt. Unabhängig davon, welcher Test verwendet wird, wird der Differenzwert jedoch als Wert zwischen 0 und 1 angezeigt.

Ein Score von 0 bedeutet, dass es keinen Unterschied zwischen den beiden Segmenten gibt, und ein Score von 1 bedeutet, dass es einen sehr großen Unterschied zwischen den beiden Segmenten gab. Es gibt zwei Arten von statistischen Tests, mit denen diese Differenzwerte erzeugt werden:

* Für die Tabelle **[!UICONTROL Top]** Metriken wird ein Mann-Whitney-U-Test verwendet,
* Für die **[!UICONTROL Top-Dimension]** Elemente und **[!UICONTROL Top-Segmente]** Tabelle wird ein Risikodifferenzvergleich verwendet.

## Differenzwert der Top-Metriken

In der Tabelle Top-Metriken verwendet das Tool für den Segmentvergleich einen Mann-Whitney-Benutzeroberflächentest mit zwei Beispielen. Dieser Test ist ein nichtparametrischer Gleichheitstest, mit dem die eindimensionalen Wahrscheinlichkeitsverteilungen jeder Metrik für jedes berücksichtigte Segment verglichen werden. Der Differenzwert in der Metriktabelle ist eine Kombination aus dem p-Wert aus der berechneten U-Statistik (die darstellt, wie stochastisch unterschiedlich die beiden Segmente über eine bestimmte Metrik verteilt sind) und der relativen Größe der beobachteten Differenz. Ein hoher Differenzwert (nahe 1) bedeutet, dass die jeweilige Metrik einen großen relativen Unterschied sowie eine hohe statistische Konfidenz aufweist, dass die Segmente unterschiedlich sind.

## Differenzwerte der Top-Dimensionselemente und Top-Segmente

Zur Berechnung der Differenzbewertung in den Dimension-Top-Elementen und den Differenztabellen des obersten Segments wird ein relativer Risikodifferenzierungsalgorithmus verwendet (ähnlich dem Risikoverhältnis, jedoch mit einer Differenz anstelle eines Verhältnisses). Eine Risikodifferenz wird berechnet, indem die kumulativen Inzidenzen eines Dimensionselements (oder der Überschneidung mit einem Segment aus der Segmenttabelle) eines ausgewählten Segments von dem anderen abgezogen werden. Ein hoher Differenzwert (nahe 1) bedeutet, dass das bestimmte Dimensionselement oder tertiäre Segment in einem der ausgewählten Segmente sehr prominent war und nicht im anderen.

>[!NOTE]
>
>In allen drei Tabellen basiert die Differenzstatistik auf einer geeigneten Stichprobe von Besuchern, damit der Prozess schnellstmöglich ausgeführt werden kann, während er dennoch statistisch genau bleibt. Während der Differenzwert auf einer Stichprobe basiert, werden die in der Tabelle dargestellten Ergebnisse nicht berechnet. Um die statistische Signifikanz sicherzustellen, stützt sich jeder statistische Test auf einen dynamischen Zuordnungsalgorithmus, sodass das kleinere Segment eine Stichprobengröße enthält, die weniger als 3 % Fehlermarge bietet. Wenn ein Segment nur sehr wenige Besucher (weniger als 1.000) enthält, werden alle verfügbaren Daten anstelle von Beispieldaten verwendet, um die Differenzbewertung zu berechnen.
