---
title: Häufig gestellte Fragen zu Datenquellen
description: Häufig gestellte Fragen zu Datenquellen.
exl-id: a948dfe9-289f-43e2-a9e7-7990cf609f5c
feature: Data Sources
role: Admin
source-git-commit: f7d07525c97f4aa145dc46198f883a37cde80158
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 5%

---

# Häufig gestellte Fragen zu Datenquellen

Häufig gestellte Fragen zu Datenquellen.

+++Wie hoch sind die Kosten für die Verwendung von Datenquellen?
Für Datenquellen fallen keine Gebühren an und sie werden auch nicht für die Nutzung der Server-Aufrufe berücksichtigt. [Datenquellen mit vollständiger Verarbeitung](full-processing-eol.md) werden vor ihrer Einstellung auf Server-Aufrufe angerechnet.
+++

+++Wie wirken sich Datenquellen auf die Attribution und den Ablauf von eVars aus?
Wenn eine transactionID zwischen einer Datenquelle und einem Online-Treffer übereinstimmt, gehen die zugehörigen eVar-Werte von derselben Attribution und demselben Ablauf aus, als ob sie im Online-Treffer festgelegt worden wären.

Alle anderen Daten, die über Datenquellen hochgeladen werden, haben keine Attribution oder Gültigkeit.
+++

+++Wie wirken sich Datenquellen auf Standardmetriken aus, z. B. Seitenansichten, Besuche oder Unique Visitors?
Daten, die über Datenquellen hochgeladen wurden[ wirken sich in keiner Weise auf ](/help/components/metrics/page-views.md)Seitenansichten[ (](/help/components/metrics/visits.md)) oder [Unique Visitors](/help/components/metrics/unique-visitors.md) aus. Die einzige Standardmetrik, auf die sie sich auswirken, umfasst [Vorfälle](/help/components/metrics/occurrences.md).
+++

+++Kann ich Daten löschen, die mithilfe von Datenquellen importiert wurden?

Ja. Sie können diese Daten mithilfe der [Data Repair API“ ](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/data-repair/). Darüber hinaus empfiehlt Adobe dringend, Datenquellendaten in eine Test-Report-Suite hochzuladen, bevor Sie sie in eine Produktions-Report-Suite hochladen.
+++

+++Wie viele Daten kann ich gleichzeitig importieren?

Die Verarbeitung wird angehalten, wenn die Datenmenge 50 MB übersteigt, und wird erst fortgesetzt, wenn die Gesamtmenge unter 50 MB liegt. Stellen Sie sicher, dass die Gesamtgröße aller Dateien auf der FTP-Site weniger als 50 MB beträgt.
+++

+++Was passiert, wenn ich über Datenquellen negative Werte in Berichte übergebe?

Der Wert wird entsprechend verringert. Einige Unternehmen verwenden negative Datenquellenwerte, um zu versuchen, Daten zu korrigieren. Negative Datenquellenwerte können sich auf Berichte in potenziell unerwünschter oder unerwarteter Weise auswirken. Adobe empfiehlt, negative Datenquellen nur als letztes Mittel zu verwenden.
+++

+++Wird bei Dateierweiterungen zwischen Groß- und Kleinschreibung unterschieden?
Ja. Dateien mit der Erweiterung `.TXT` oder `.FIN` werden nicht verarbeitet. Stellen Sie sicher, dass die Dateierweiterungen vollständig in Kleinbuchstaben geschrieben sind.
+++

+++Wie viele Spalten kann ich einer Datenquellendatei hinzufügen?
Sie können beliebig viele Spalten in eine Datenquellendatei einbeziehen, wenn es sich um gültige Spalten handelt. Siehe [Dateiformat](file-format.md) für eine Liste gültiger Variablen-/Spaltennamen.
+++

+++Kann ich Datenquellen verwenden, ohne den von Adobe bereitgestellten FTP-Speicherort zu verwenden?
Sie können die [Datenquellen-API](https://developer.adobe.com/analytics-apis/docs/1.4/guides/data-sources/) verwenden, mit der Sie API-Aufrufe direkt an Adobe senden können. Diese API-Aufrufe enthalten eine `UploadData`-Methode, mit der Sie Daten über eine JSON-Objekt-Payload senden können.
+++
