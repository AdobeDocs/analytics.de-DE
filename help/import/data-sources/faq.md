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

+++ Wie hoch sind die Kosten für die Verwendung von Datenquellen?
Für Datenquellen fallen keine Gebühren an und sie werden auch nicht für die Nutzung von Server-Aufrufen berücksichtigt. [Datenquellen mit vollständiger Verarbeitung](full-processing-eol.md), die vor ihrer Ausbuchung für Server-Aufrufe gezählt werden.
+++

+++ Wie wirken sich Datenquellen auf die Attribution und Gültigkeit von eVars aus?
Wenn eine transactionID zwischen einer Datenquelle und einem Online-Treffer übereinstimmt, gehen die zugehörigen eVar von der gleichen Attribution und Gültigkeit aus wie beim Online-Treffer.

Alle anderen Daten, die über Datenquellen hochgeladen werden, haben keine Attribution oder Gültigkeit.
+++

++ Wie wirken sich Datenquellen auf Standardmetriken wie Seitenansichten, Besuche oder Unique Visitors aus?
Daten, die über Datenquellen hochgeladen werden, wirken sich in keiner Weise auf [Seitenansichten](/help/components/metrics/page-views.md), [Besuche](/help/components/metrics/visits.md) oder [Unique Visitors](/help/components/metrics/unique-visitors.md) aus. Die einzige Standardmetrik, auf die sie sich auswirken, ist [Vorfälle](/help/components/metrics/occurrences.md).
+++

+++ Kann ich Daten löschen, die mithilfe von Datenquellen importiert wurden?

Ja. Sie können diese Daten mit der [Datenreparatur-API](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/data-repair/) löschen. Darüber hinaus empfiehlt Adobe dringend, Datenquellen-Daten in eine Test-Report Suite hochzuladen, bevor sie in eine Produktions-Report Suite hochgeladen werden.
+++

++ Wie viele Daten kann ich gleichzeitig importieren?

Die Verarbeitung wird angehalten, wenn die Datenmenge 50 MB übersteigt, und wird erst fortgesetzt, wenn die Gesamtmenge unter 50 MB liegt. Stellen Sie sicher, dass die Gesamtgröße aller Dateien auf der FTP-Site weniger als 50 MB beträgt.
+++

++ Was passiert, wenn ich über Datenquellen negative Werte in Berichte einfüge?

Der Wert wird entsprechend verringert. Einige Unternehmen verwenden negative Datenquellenwerte, um zu versuchen, Daten zu korrigieren. Negative Datenquellenwerte können sich auf Berichte auf möglicherweise unerwünschte oder unerwartete Weise auswirken. Adobe empfiehlt die Verwendung negativer Datenquellen nur als letztes Mittel.
+++

+++Wird bei Dateierweiterungen zwischen Groß- und Kleinschreibung unterschieden?
Ja. Dateien mit der Erweiterung `.TXT` oder `.FIN` werden nicht verarbeitet. Stellen Sie sicher, dass Dateierweiterungen nur in Kleinbuchstaben erfolgen.
+++

++ Wie viele Spalten kann ich zu einer Datenquellendatei hinzufügen?
Sie können beliebig viele Spalten in eine Datenquellendatei aufnehmen, wenn es sich um gültige Spalten handelt. Eine Liste der gültigen Variablen-/Spaltennamen finden Sie unter [Dateiformat](file-format.md) .
+++

+++ Kann ich Datenquellen verwenden, ohne den vom Adobe bereitgestellten FTP-Speicherort zu verwenden?
Sie können die [Datenquellen-API](https://developer.adobe.com/analytics-apis/docs/1.4/guides/data-sources/) verwenden, mit der Sie API-Aufrufe direkt an Adobe senden können. Diese API-Aufrufe enthalten eine `UploadData` -Methode, mit der Sie Daten von einer JSON-Objekt-Payload senden können.
+++
