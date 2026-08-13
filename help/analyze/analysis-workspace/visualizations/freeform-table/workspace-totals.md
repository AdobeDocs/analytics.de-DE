---
description: Erfahren Sie, wie Summen in Freiformtabellen in Analysis Workspace berechnet werden.
title: Gesamt
feature: Freeform Tables
role: User, Admin
exl-id: 883c3e44-4139-46a1-a261-e11841312465
TQID: https://experienceleague.adobe.com/wxOqh9uQC1oDpjGjZwp-A4Ir0PfH1cH8y5l9IYM-3io
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2:
  - id: dcae653e-62c6-4cc8-84e6-ee110b848296
  - id: e318d41c-1d01-4c1e-9b18-1f61d435ceee
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 504
ht-degree: 78%

---

# Gesamt {#workspace-totals}

>[!CONTEXTUALHELP]
>id="workspace_freeformtable_grandtotal"
>title="Gesamtsumme"
>abstract="Die Gesamtsumme wird für Tabellen oder Aufschlüsselungen mit statischen Zeilen nicht unterstützt."

In Freiformtabellen wird auf jeder Unterteilungsebene eine Zeile insgesamt angezeigt, die zwei Summen enthalten kann:

![Freiformtabelle mit hervorgehobener Gesamt- und Tabellensumme.](assets/total-row.png)

* **[!UICONTROL Tabellensumme]** ➊ - Dieser Gesamtwert entspricht in der Regel der Gesamtsumme oder einer Teilmenge [!UICONTROL Gesamtsumme]. Er spiegelt alle Tabellenfilter wider, die innerhalb der Freiformtabelle angewendet werden, einschließlich der Option [!UICONTROL Keine einschließen].
* **[!UICONTROL Gesamtsumme]** (**[!UICONTROL von]** *Anzahl*) ➋ - Dieser Gesamtwert stellt alle erfassten Ereignisse dar. Wenn ein Filter entweder auf Panel-Ebene oder in der Freiformtabelle angewendet wird, passt sich diese Summe an, sodass alle Ereignisse wiedergegeben werden, die den Filterkriterien entsprechen.




## Anzeigen von Summen

Unter ![Setting](/help/assets/icons/Setting.svg) **[!UICONTROL Spalteneinstellungen]** finden Sie die Optionen **[!UICONTROL Summen anzeigen]** und **[!UICONTROL Gesamtsumme anzeigen]**. Wenn diese Einstellungen nicht aktiviert sind, werden Summen aus der Tabelle entfernt. In Fällen, in denen Summen nicht sinnvoll sind, kann dies durchaus erwünscht sein.


In einer Freiformtabelle, die (statische [) enthält](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md) verhalten sich Summen anders. und werden mithilfe von ![Einstellung](/help/assets/icons/Setting.svg) **[!UICONTROL Zeileneinstellungen]**.

| Option | Beschreibung |
|---|---|
| **[!UICONTROL Als Summe der aktuellen Zeilen anzeigen]** | Zeigt eine Client-seitige Summe der Zeilen in der Tabelle an. Bei dieser Summe werden Metriken wie Sitzungen oder Personen **nicht** dedupliziert. |
| **[!UICONTROL Gesamtsumme anzeigen]** | Zeigt eine Server-seitige Summe an. Bei dieser Summe werden Metriken wie Sitzungen oder Personen dedupliziert. |

Siehe [Dynamische und statische Dimensionselemente in Freiformtabellen](column-row-settings/manual-vs-dynamic-rows.md).


## Häufig gestellte Fragen

| Fragen | Antwort |
|---|---|
| Auf welcher *Summe* basieren die grauen Spaltenprozentsätze? | Diese *Summe* hängt von der Einstellung **[!UICONTROL Prozentsatz]** unter **[!UICONTROL Zeileneinstellungen]** ab:<ul><li>Prozentsätze nach Spalte berechnen: Diese Einstellung ist die Standardeinstellung. Prozentsätze basieren auf der Tabellensumme.</li><li>Prozentsätze nach Zeile berechnen: Prozentsätze werden auf Basis der Gesamtsumme berechnet.</li></ul> |
| Wie wirkt sich die Einstellung **[!UICONTROL Nicht angegeben (keine) einschließen]** auf die Gesamtwerte aus? | Wenn die Einstellung Nicht angegeben einschließen (Keine) nicht aktiviert ist, wird die Zeile „Keine“/„Nicht angegeben“ aus der Tabelle „Tabellensumme“ entfernt und in alle berechneten Metriken übertragen, die [&#x200B; Metriktypen „Gesamt“ verwenden](/help/components/calculated-metrics/workflow/c-build-metrics/m-metric-type-alloc.md). |
| Wenn benutzerdefinierte Tabellenfilter auf eine Freiformtabelle angewendet werden, werden alle berechneten Metriken und die bedingte Formatierung für den Filter berücksichtigt? | Derzeit nicht. **[!UICONTROL Nicht spezifizierte einschließen (keine]** wird berücksichtigt, aber benutzerdefinierte Tabellenfilter wirken sich nicht auf Folgendes aus:<ul><li>Maximaler/minimaler Spaltenbereich, der bei der bedingten Formatierung verwendet wird, wird über alle Daten hinweg angezeigt.</li><li>Berechnete Metriken, die Metriktypen **[!UICONTROL Gesamtsumme]** nutzen.</li><li>Berechnete Metriken mit Funktionen, die über Berechnungen für alle Zeilen in einer Freiformtabelle durchführen – d. h. Spaltensumme, Spaltenmaximum, Spaltenminimum, Anzahl, Mittelwert, Median, Perzentil, Quartil, Zeilenzahl, Standardabweichung, Varianz, kumulativer Wert, kumulativer Durchschnitt, Regressionsvarianten, T-Score, T-Test, Z-Score und Z-Test.</li></ul> |
| Was spiegelt der Metriktyp **[!UICONTROL Gesamtsumme]** in berechneten Metriken wider? | Die **[!UICONTROL Gesamtsumme]** bezieht sich weiterhin auf die **[!UICONTROL Gesamtsumme]** und spiegelt keine Filter wider, die auf eine Tabelle oder die **[!UICONTROL Tabellensumme]** angewendet wurden. |
| Welcher Gesamtwert wird angezeigt, wenn Daten entweder kopiert und aus einer Freiformtabelle eingefügt oder über CSV heruntergeladen werden? | Die Zeile insgesamt spiegelt nur die **[!UICONTROL Tabellensumme]** wider und berücksichtigt die Einstellung **[!UICONTROL Summen anzeigen]**. |
