---
description: Erläutert die neue Strategie zur kontinuierlichen Veröffentlichung von Funktionen für Adobe Analytics.
title: Veröffentlichung von Adobe Analytics-Funktionen
translation-type: ht
source-git-commit: 322e2e87ab532d5e8a864dc06613a9b275c71df5
workflow-type: ht
source-wordcount: '358'
ht-degree: 100%

---


# Veröffentlichung von Adobe Analytics-Funktionen

Bisher wurden die Adobe Analytics-Funktionen nach einem festen monatlichen Zeitplan veröffentlicht. Ab April 2020 wurde Adobe Analytics auf ein kontinuierliches Bereitstellungsmodell umgestellt, das einen skalierbareren, schrittweisen Ansatz für die Implementierung von Funktionen ermöglicht.

## Veröffentlichungsstrategie

[!UICONTROL Analysis Workspace] verwendet Funktionsmarkierungen (auch als „Umschalter“ bezeichnet), um die Sichtbarkeit neuer Funktionen zu steuern, sodass vor der Vollversion ein kontrollierter Skalierungstest durchgeführt werden kann. Diese Veröffentlichungsstrategie umfasst die folgenden Phasen:

* **Freigabe für die Produktion (RTP)**: Der Code wird für die Produktion freigegeben, wobei die Sichtbarkeit der Funktionen in Analysis Workspace deaktiviert ist. **Hinweis**: Bei RTP ist die Funktion möglicherweise in der Analytics-API 2.0 verfügbar.

* **Eingeschränktes Testen**: Eine schrittweise Veröffentlichung beginnt mit Tests durch interne Adobe-Benutzer. Die Verfügbarkeit der Version wird dann im Laufe einiger Monate von 0 % auf 100 % skaliert. Die schrittweise Einführung erfolgt auf der Organisationsebene in Experience Cloud, sodass alle Benutzer mit Berechtigung in einem Unternehmen dasselbe Erlebnis erhalten.

* **Allgemeine Verfügbarkeit (GA)**: Die Funktion steht 100 % der berechtigten Experience Cloud-Organisationen zur Verfügung und die Veröffentlichung der Funktion ist abgeschlossen.

Bei jeder Funktionsveröffentlichung kann die Timeline von RTP bis GA variieren. Ziel ist es, die Veröffentlichungen kurz zu halten, sodass innerhalb von 2 Monaten nach Beginn der Veröffentlichung (RTP) eine Funktion allgemein verfügbar (GA) ist.

## Vorteile

Die stufenweise Veröffentlichung ermöglicht es Adobe, den Software-Implementierungsprozess besser zu skalieren und sicherzustellen, dass die Funktionen vor der allgemeinen Verfügbarkeit vollständig gehärtet sind. Außerdem können Funktionen veröffentlicht werden, sobald sie verfügbar sind, anstatt sich an ein festes monatliches Veröffentlichungsfenster zu halten.

## Häufig gestellte Fragen (FAQ)

| Frage | Antwort |
|---|---|
| Kann ich frühzeitigen Zugriff auf eine Funktion anfordern? | Nein. Es wird kein frühzeitiger Zugriff gewährt.<br>Wenn Sie frühe Analytics-Konzepte testen möchten, empfehlen wir Ihnen, [Adobe Analytics Labs](https://docs.adobe.com/content/help/de-DE/analytics/analyze/tech-previews/overview.html) zu testen, um Feedback zu unseren branchenführenden Innovationen zu geben. |
| Hat diese Veröffentlichungsstrategie Auswirkungen auf meinen Zugriff auf Funktionen? | Nein. Sobald eine Funktion GA erreicht hat, haben Sie Zugriff auf die Funktion, wenn sie in Ihrem Analytics-Paket enthalten ist.<br>Details zu Ihrem Analysen-Paket finden Sie unter [!UICONTROL Admin] > [!UICONTROL Unternehmenseinstellungen] > [Funktionszugriffsebenen](https://docs.adobe.com/content/help/de-DE/analytics/admin/company-settings/feature-access-levels.html). |