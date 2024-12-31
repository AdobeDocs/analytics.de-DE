---
title: Vorfälle
description: Die Anzahl der Treffer, für die eine Variable festgelegt oder beibehalten wurde.
feature: Metrics
exl-id: 8428e813-0fb4-4620-884e-1aa92fe33209
source-git-commit: 0c5062363e10d9b545a3209ebaefcc6fa5d02c8b
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 57%

---

# Vorfälle

Die [Metrik](overview.md) „Vorfälle“ zeigt die Anzahl der Treffer an, bei denen eine bestimmte Dimension festgelegt oder beibehalten wurde. Wenn Sie eine Dimension in Workspace auf eine leere Arbeitsfläche ziehen, wendet Adobe diese Metrik automatisch auf das Projekt an.

## Berechnung dieser Metrik

Schließen Sie von allen Treffern in einer Report Suite die Treffer ein, bei denen ein Dimensionselement definiert oder beibehalten wird. Einige Dimensionen, wie z. B. [eVars](../dimensions/evar.md), bleiben über den Treffer hinaus bestehen, für den sie festgelegt wurden. Diese Metrik zählt sowohl anfängliche als auch persistente Werte.

## Vergleich mit ähnlichen Metriken

* **Vorfälle oder [Instanzen](instances.md)**: Vorfälle zählen Treffer, bei denen ein Dimensionselement festgelegt oder beibehalten wurde. Instanzen enthalten keine Treffer, bei denen ein Dimensionselement beibehalten wird.
* **Vorfälle im Vergleich zu [Seitenansichten](page-views.md)**: Zu den Vorfällen gehören alle Treffertypen, darunter Seitenansicht-Tracking-Aufrufe ([`t()`](/help/implement/vars/functions/t-method.md)), Linktracking-Aufrufe ([`tl()`](/help/implement/vars/functions/tl-method.md)) und Daten aus [Datenquellen](/help/import/data-sources/overview.md) auf Zusammenfassungsebene. Die Metrik „Seitenansichten“ umfasst nur Seitenansichts-Tracking-Aufrufe, aber keine Linktracking-Aufrufe und Datenquellen auf Zusammenfassungsebene.

## Persistenz

Persistenz ist die Fähigkeit, dass ein bestimmter Dimensionswert sich über das Ereignis hinaus auf eine Metrik beziehen kann. Es wird eine Kombination aus Zuordnung und Gültigkeit verwendet. Mit Zuordnung können Sie festlegen, welcher Wert beibehalten wird, wenn mehrere Dimensionselemente gleichzeitig in einer Spalte beibehalten werden können. Mit Gültigkeit können Sie festlegen, wie lange ein Dimensionselement über das Ereignis hinaus bestehen bleibt, für das es festgelegt ist.

Persistenz ist nur für Dimensionen verfügbar und rückwirkend für die Daten, auf die sie angewendet wird. Es handelt sich um eine sofortige Datenumwandlung, die vor der Anwendung von Filtern oder anderen Analysevorgängen erfolgt. Wenn die Persistenz nicht aktiviert ist, bezieht sich die Dimension nur auf Metriken, die im selben Ereignis vorhanden sind.