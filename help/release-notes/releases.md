---
description: Erläutert die Strategie zur kontinuierlichen Veröffentlichung von Funktionen für Adobe Analytics.
title: Veröffentlichung von Adobe Analytics-Funktionen
feature: Release Notes
exl-id: 1e403bef-4aab-4a9a-a358-62449ce801ff
TQID: https://experienceleague.adobe.com/gDUf5ZiM-DUiG52nlMIFMbXc4NPNTI7bLrugWGicjgI
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 7d733a6375f6c6009563bc53f5a3ff090dbc48ed
workflow-type: tm+mt
source-wordcount: 395
ht-degree: 90%

---

# Veröffentlichung von Adobe Analytics-Funktionen

Adobe Analytics-Versionen basieren auf einem kontinuierlichen Bereitstellungsmodell, das eine besser skalierbare, schrittweise Implementierung von Funktionen ermöglicht.

## Veröffentlichungsstrategie

[!UICONTROL Analysis Workspace] verwendet Funktionsmarkierungen (auch als „Umschalter“ bezeichnet), um die Sichtbarkeit neuer Funktionen zu steuern, sodass vor der Vollversion ein kontrollierter Skalierungstest durchgeführt werden kann. Diese Veröffentlichungsstrategie umfasst die folgenden Phasen:

* **Eingeschränktes Testen**: Eine schrittweise Veröffentlichung beginnt mit Tests durch Adobe-interne Benutzende. Sie wird dann einer kleinen Gruppe von Kundenkonten zur Verfügung gestellt, um sicherzustellen, dass die Funktion den Kundenanforderungen und Erwartungen entspricht.

* **Start des Rollouts**: Der Rollout einer stufenweisen Veröffentlichung beginnt mit der eingeschränkten Testphase. Die Verfügbarkeit der Version für Kunden wird dann im Laufe einiger Monate von 0 % auf 100 % skaliert. Der schrittweise Rollout erfolgt auf der Ebene der CX Enterprise-Organisation, sodass alle berechtigten Benutzenden in einer Organisation dasselbe Erlebnis erhalten.

* **Allgemeine Verfügbarkeit (GA)**: Die Funktion steht 100 % berechtigten CX Enterprise-Organisationen zur Verfügung und die Funktionsveröffentlichung ist abgeschlossen.

Bei jeder Funktionsveröffentlichung kann die Timeline vom Start des Rollouts bis zur GA variieren. Ziel ist es, die Veröffentlichungszeiträume kurz zu halten, sodass eine Funktion innerhalb von 2 Monaten nach dem Start des Rollouts allgemein verfügbar (GA) ist.

## Funktionsmarkierungen

Mithilfe von Funktionsmarkierungen wird die Sichtbarkeit neuer Funktionen während der Veröffentlichung gesteuert. Adobe empfiehlt, `app.launchdarkly.com` zur [Zulassungsliste](/help/technotes/ip-addresses.md) Ihrer Firewall hinzuzufügen, um eine optimale Funktionalität bei der Veröffentlichung zu erzielen. Kurz nach der allgemeinen Verfügbarkeit wird die Markierung entfernt.

Sie können sich Ihre aktiven Funktionsmarkierungen jederzeit unter **Hilfe > Über den Workspace > Aktive Funktionsmarkierungen** ansehen.

## Vorteile

Die stufenweise Veröffentlichung ermöglicht es Adobe, den Software-Bereitstellungsprozess besser zu skalieren und sicherzustellen, dass die Funktionen vor der allgemeinen Verfügbarkeit vollständig gehärtet sind. Außerdem können Funktionen veröffentlicht werden, sobald sie verfügbar sind, anstatt sich an ein festes monatliches Veröffentlichungsfenster zu halten.

## Häufig gestellte Fragen (FAQ)

| Frage | Antwort |
| --- | --- |
| Kann ich frühzeitigen Zugriff auf eine Funktion anfordern? | Nein. Es wird kein frühzeitiger Zugriff gewährt.<br>Wenn Sie frühe Analytics-Konzepte testen möchten, empfehlen wir Ihnen, [Adobe Analytics Labs](/help/analyze/labs.md) zu testen, um Feedback zu unseren branchenführenden Innovationen zu geben. |
| Hat diese Veröffentlichungsstrategie Auswirkungen auf meinen Zugriff auf Funktionen? | Nein. Sobald eine Funktion GA erreicht hat, haben Sie Zugriff auf die Funktion, wenn sie in Ihrem Analytics-Paket enthalten ist.<br>Details zu Ihrem Analytics-Paket finden Sie unter [Funktionszugriffsebenen](/help/admin/tools/company/feature-access-levels.md). |
