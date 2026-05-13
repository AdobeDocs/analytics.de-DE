---
title: Content-Geschwindigkeit
description: Content-Geschwindigkeit misst die Auswirkungen von Inhalten auf nachgeordnete Inhalte.
feature: Metrics
exl-id: 8ba54990-ff7d-4693-92de-7f9d9f916b55
TQID: https://experienceleague.adobe.com/KEcYF9OWDaxwZX798AETiAIxcffBAwj29Go-oHLOnaU
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 12%

---

# Content-Geschwindigkeit

Mit der berechneten Metrik „Inhaltsgeschwindigkeit“ können Sie messen, wie eine Dimension (normalerweise [[!UICONTROL Seite]](/help/components/dimensions/page.md)) dazu beiträgt, dass Benutzer Zeit auf Ihrer Website oder in Ihrem Programm verbringen.

Diese Metrik verwendet [Partizipationsattribution](/help/analyze/analysis-workspace/attribution/models.md) für die Metrik [Seitenansichten](page-views.md) als Teil ihrer Berechnung. Bei der Teilnahme an Besuchen wird jedes Mal, wenn eine Seite aufgerufen wird, allen Seiten, die zuvor während desselben Besuchs getroffen wurden, auch die Seitenansicht angerechnet. Diese Formel bedeutet in der Regel, dass eine Seite umso mehr Anerkennung erhält, je früher sie während eines Besuchs aufgerufen wurde. (Weitere [ finden Sie unter „Seitenansichten (Teilnahme | Besuch)“ oder &quot;](#page-views-participation--visit-or-visit-participation)&quot;.)

## Kalkulation

„Inhaltsgeschwindigkeit“ ist eine standardmäßig berechnete [Metrik](overview.md) und verwendet die Formel `Page views (Visit participation)` dividiert durch `Visits`.

![](assets/cont-velo-1.png)

## Häufige Verwendungszwecke

[!UICONTROL Content-Geschwindigkeit] wird häufig bei der Analyse von Inhalten neben anderen Schlüsselmetriken wie [!UICONTROL Seitenansichten], [!UICONTROL Besuche] und [!UICONTROL Absprungrate] verwendet.

![](assets/cont-velo-3.png)

## Beispiel

Im folgenden Beispiel werden die 2 Teile der Inhaltsgeschwindigkeit aufgeschlüsselt: „Seitenansichten (Teilnahme | Besuch)“ und „Besuche“.

### Seitenansichten (Teilnahme | Besuch) oder „Besuchsbeteiligung“

Im Folgenden finden Sie ein Beispiel dafür, wie sich die Besuchsbeteiligung auf die Attribution auswirkt:

Auf einer Website besucht ein Benutzer die folgenden Seiten in dieser Reihenfolge:

* Seite A
* Seite B
* Seite C
* Seite D

Im obigen Beispiel würde Seite A eine Gutschrift für 4 Treffer erhalten, Seite B für 3 Treffer, Seite C für 2 Treffer und Seite D für 1 Treffer.

Das folgende Beispiel veranschaulicht dasselbe Prinzip, jedoch mit einigen Seiten, die mehrmals besucht werden.

* Seite A
* Seite B
* Seite C
* Seite B
* Seite D
* Seite A

Im obigen Beispiel würde Seite A eine Gutschrift für 7 Treffer erhalten, Seite B für 8 Treffer, Seite C für 4 Treffer und Seite D für 2 Treffer.

### Besuche

Nachdem die Besuchsbeteiligung berechnet wurde, wird das Ergebnis durch die Anzahl der Besuche dividiert.
