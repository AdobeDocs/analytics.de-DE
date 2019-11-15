---
description: Bei der Data Connectors-Integration für DFA werden für das Tracking der DFA-Kampagnenergebnisse Analytics-Variablen verwendet.
keywords: DFA
solution: Analytics
title: Analytics-Variablen und -Ereignisse
topic: Data connectors
uuid: 8996cb58-c793-4600-99ef-af3064642b29
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Analytics-Variablen und -Ereignisse{#analytics-variables-and-events}

Bei der Data Connectors-Integration für DFA werden für das Tracking der DFA-Kampagnenergebnisse Analytics-Variablen verwendet.

Neben Kampagnenvariablen können Sie Analytics-Ereignisse und eVars verwenden, die für Sie nützlich sind. Wenn Sie die Ereignisse und eVars ausgemacht haben, die Sie für diese DFA-Integration verwenden möchten, aktivieren Sie sie mithilfe der Analytics Admin Console. Die Integrationsvariablen müssen vor der Aktivierung der DFA-Integration eingeschaltet werden. In der folgenden Tabelle sind die für die DFA-Integration benötigten Analytics-Variablen aufgeführt.

| Variable | Anzeigename | Methode zum Ausfüllen | Beschreibung |
|---|---|---|---|
| s.campaign oder eVar | Anzeigentrackingcode | Automatisch durch Data Connectors für DFA-Kampagnen ausgefüllt | Trackt Clickthrough-Konversionen für alle Kampagnen |
| eVar* | Durchsicht | Automatisch durch VISTA und DFA für DFA-Kampagnen ausgefüllt | Trackt Durchsichtsdaten für DFA-IDs Diese eVar sollte dasselbe Ablaufdatum wie die Variable *`s.campaign`* festgelegt. Muss dieselbe Konversionsvariable sein wie in der Variablen-Provider-ID angegeben. Stellen Sie sicher, dass für die eVar vollständige untergeordnete Beziehungen aktiviert sind. Die Kosten für die Aktivierung dieser Funktion sind in der Gebühr für die Data Connectors-Integration enthalten. |
| eVar* | DFA-Abfragefehler | (Optional) Durch JavaScript-Erfassungscode ausgefüllt | Enthält einen von mehreren von DFA zurückgegebenen Fehlercodes. |
| event* | Anzahl Durchsichten | Automatisch durch Data Connectors für DFA-Kampagnen ausgefüllt | Erfasst die Anzahl der Anzeigenansichten durch Benutzer, die keinen Clickthrough durchgeführt haben, aber letztendlich auf Ihre Site gelangt sind. |
| event* | Impressionen | Automatisch durch einen Datenfeed von DFA ausgefüllt | Trackt die Zeit, in der eine spezielle DFA-Anzeige bereitgestellt wurde. |
| event* | Klicks | Automatisch durch einen Datenfeed von DFA ausgefüllt | Trackt die Anzahl der Klicks durch Benutzer auf eine spezielle DFA-Banneranzeige Bei dieser Metrik können aus einem von verschiedenen Gründen im Vergleich zur nativen Analytics-Clickthrough-Metrik andere Zahlenwerte ausgegeben werden. Weitere Informationen zu diesem Thema finden Sie unter [Abgleich von Metrikdiskrepanzen](/help/import/data-connectors/dfa-data-connector-analytics/dfa-reconciling-metric-discrepancies.md) |
| event* | DFA-Timeouts | (Optional) Durch JavaScript-Erfassungscode ausgefüllt | Erfasst die Anzahl der DFA-Reaktionsfehlschläge vor Ablauf von *`s.maxDelay`* . So können Sie einfacher herausfinden, ob ein Problem bei der DFA-Implementierung vorliegt. |
| event* | DFA-Medienkosten | Automatisch durch einen Datenfeed von DFA ausgefüllt | Enthält die Metrik zu Medienkosten, die in der DFA-Oberfläche eingegeben wurden. Diese Funktion muss in DFA aktiviert werden, damit diese Metriken angezeigt werden. |

* Wählen Sie ein nicht verwendetes eVar- oder benutzerdefiniertes Ereignis.
