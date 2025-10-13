---
title: Seitenereignisse
description: Die Anzahl der ausgelösten Linktracking-Aktionen.
feature: Metrics
exl-id: 1afe86e3-65b3-4e4e-b436-ed7cb5da9641
source-git-commit: 205d86b13046bd17e321734904bf57435ef6e106
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 33%

---

# Seitenereignisse

Die Metrik „Seitenereignisse[ ](overview.md) gibt an, wie oft ein Linktracking-Aufruf durchgeführt wurde. Diese Metrik ist hilfreich, wenn Sie wissen möchten, welche Seiten den interessantesten Inhalt haben. Die Messung für diese Metrik ist am nützlichsten, wenn ein Besucher eine Seitenaktion ausführen kann, ohne zu einer neuen Seite zu navigieren.

Auf einer typischen Journey einer eCommerce-Website kann ein Besucher beispielsweise mehrere Interaktionen auf einer Seite haben. Bei einer typischen Analytics-Implementierung sind diese Interaktionen als Linktracking-Aufruf ([`tl()`](/help/implement/vars/functions/tl-method.md)) konfiguriert, während ein Aufruf für die Seitenansicht ([`t()`](/help/implement/vars/functions/t-method.md)) für den anfänglichen Seitenladevorgang reserviert ist. Diese Implementierungsmethode bietet eine erweiterte Ereignisverfolgung, die insight Aufschluss darüber gibt, welche Interaktionen stattfinden, bevor ein Besucher seinen Journey fortsetzt.

## Berechnung dieser Metrik

Diese Metrik zählt alle Linktracking-Aufrufe ([`tl()`](/help/implement/vars/functions/tl-method.md)) in einer Report Suite. Alle Link-Typen sind in dieser Metrik enthalten, insbesondere [benutzerspezifische Links](../dimensions/custom-link.md), [Downloadlinks](../dimensions/download-link.md) und [Exitlinks](../dimensions/exit-link.md). Sie enthält keine Seitenansichtsaufrufe ([`t()`](/help/implement/vars/functions/t-method.md)).

## Vergleich mit ähnlichen Metriken

* **Seitenereignisse vs. [Seitenansichten](page-views.md)**: Seitenereignisse zählen die Anzahl der Linktracking-Aufrufe ([`tl()`](/help/implement/vars/functions/tl-method.md)) und schließen Seitenansichts-Tracking-Aufrufe ([`t()`](/help/implement/vars/functions/t-method.md)) aus. Im Gegensatz dazu zählen Seitenansichten die Anzahl der Seitenansichts-Tracking-Aufrufe und schließen Links aus.
