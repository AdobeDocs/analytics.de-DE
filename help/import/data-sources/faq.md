---
title: Häufig gestellte Fragen zu Datenquellen
description: Häufig gestellte Fragen zu Datenquellen.
exl-id: a948dfe9-289f-43e2-a9e7-7990cf609f5c
feature: Data Sources
role: Admin
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 7%

---

# Häufig gestellte Fragen zu Datenquellen

Häufig gestellte Fragen zu Datenquellen.

+++Wie hoch sind die Kosten für die Verwendung von Datenquellen?
Für Datenquellen fallen keine Gebühren an und sie werden auch nicht für die Nutzung der Server-Aufrufe berücksichtigt. [Datenquellen mit vollständiger Verarbeitung](full-processing-eol.md) werden vor ihrer Einstellung auf Server-Aufrufe angerechnet.
+++

+++Wie wirken sich Datenquellen auf die Attribution und den Ablauf von eVars aus?
Datenquellen verfügen über keine Attribution oder Gültigkeit.
+++

+++Wie wirken sich Datenquellen auf Metriken wie Seitenansichten, Besuche oder Unique Visitors aus?
Daten, die über Datenquellen hochgeladen wurden[ wirken sich in keiner Weise auf ](/help/components/metrics/page-views.md)Seitenansichten[ (](/help/components/metrics/visits.md)) oder [Unique Visitors](/help/components/metrics/unique-visitors.md) aus. Die einzige Standardmetrik, auf die sie sich auswirken, umfasst [Vorfälle](/help/components/metrics/occurrences.md).
+++

+++Werden Daten, die über Datenquellen hochgeladen wurden, durch zusätzliche Verarbeitungsregeln wie Verarbeitungsregeln verarbeitet?
Nein. Daten, die über Datenquellen hochgeladen wurden:

* Durchläuft nicht [Verarbeitungsregeln](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md)
* Durchläuft nicht [Marketing-Kanal-Verarbeitungsregeln](/help/admin/tools/manage-rs/edit-settings/marketing-channels/c-rules.md)
* Durchläuft nicht [VISTA-Regeln](/help/technotes/vista.md)
+++

+++Kann ich Daten löschen, die mit Datenquellen importiert wurden?
Ja. Sie können diese Daten mithilfe der [Data Repair API“ ](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/data-repair/). Adobe empfiehlt dringend, Datenquellendaten in eine Test-Report-Suite hochzuladen, bevor Sie sie in eine Produktions-Report-Suite hochladen, um die Notwendigkeit zum Entfernen von Daten zu verringern.
+++

+++Wie viele Daten kann ich gleichzeitig importieren?
Die Verarbeitung wird angehalten, wenn die Datenmenge 50 MB übersteigt, und wird erst fortgesetzt, wenn die Gesamtmenge unter 50 MB liegt. Stellen Sie sicher, dass die Gesamtgröße aller Dateien auf der FTP-Site weniger als 50 MB beträgt.
+++

+++Was passiert, wenn ich über Datenquellen negative Werte in Berichte einfüge?
Der Wert wird entsprechend verringert. Einige Unternehmen verwenden negative Datenquellenwerte, um zu versuchen, Daten zu korrigieren. Negative Datenquellenwerte können sich auf Berichte in potenziell unerwünschter oder unerwarteter Weise auswirken. Adobe empfiehlt die Verwendung negativer Werte in Datenquellen nur als letztes Mittel.
+++

+++Wird bei Dateierweiterungen zwischen Groß- und Kleinschreibung unterschieden?
Ja. Dateien mit der Erweiterung `.TXT` oder `.FIN` werden nicht verarbeitet. Stellen Sie sicher, dass die Dateierweiterungen vollständig in Kleinbuchstaben geschrieben sind.
+++

+++Wie viele Spalten kann ich einer Datenquellendatei hinzufügen?
Sie können beliebig viele Spalten in eine Datenquellendatei einbeziehen, wenn es sich um gültige Spalten handelt. Siehe [Dateiformat](file-format.md) für eine Liste gültiger Variablen-/Spaltennamen.
+++

+++Kann ich Datenquellen verwenden, ohne den von Adobe bereitgestellten FTP-Speicherort zu verwenden?
Sie können die [Data Sources-API](https://developer.adobe.com/analytics-apis/docs/1.4/guides/data-sources/) verwenden, mit der Sie API-Aufrufe direkt an Adobe senden können. Diese API-Aufrufe enthalten eine `UploadData`-Methode, mit der Sie Daten über eine JSON-Objekt-Payload senden können.
+++
