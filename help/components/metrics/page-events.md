---
title: Seitenereignisse
description: Die Anzahl der ausgelösten Linktracking-Aktionen.
feature: Metrics
exl-id: 1afe86e3-65b3-4e4e-b436-ed7cb5da9641
TQID: https://experienceleague.adobe.com/tOEidVQjv4ynokjH53SEdKeOHiqwZn02WZDalUESsAs
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f1f1a2d4-0976-4881-b091-c2bb8de7ffacid: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 210
ht-degree: 33%

---

# Seitenereignisse

Die Metrik „Seitenereignisse[ ](overview.md) gibt an, wie oft ein Linktracking-Aufruf durchgeführt wurde. Diese Metrik ist hilfreich, wenn Sie wissen möchten, welche Seiten den interessantesten Inhalt haben. Die Messung für diese Metrik ist am nützlichsten, wenn ein Besucher eine Seitenaktion ausführen kann, ohne zu einer neuen Seite zu navigieren.

Auf einer typischen Journey einer eCommerce-Website kann ein Besucher beispielsweise mehrere Interaktionen auf einer Seite haben. Bei einer typischen Analytics-Implementierung sind diese Interaktionen als Linktracking-Aufruf ([`tl()`](/help/implement/vars/functions/tl-method.md)) konfiguriert, während ein Aufruf für die Seitenansicht ([`t()`](/help/implement/vars/functions/t-method.md)) für den anfänglichen Seitenladevorgang reserviert ist. Diese Implementierungsmethode bietet eine erweiterte Ereignisverfolgung, die insight Aufschluss darüber gibt, welche Interaktionen stattfinden, bevor ein Besucher seinen Journey fortsetzt.

## Berechnung dieser Metrik

Diese Metrik zählt alle Linktracking-Aufrufe ([`tl()`](/help/implement/vars/functions/tl-method.md)) in einer Report Suite. Alle Link-Typen sind in dieser Metrik enthalten, insbesondere [benutzerspezifische Links](../dimensions/custom-link.md), [Downloadlinks](../dimensions/download-link.md) und [Exitlinks](../dimensions/exit-link.md). Sie enthält keine Seitenansichtsaufrufe ([`t()`](/help/implement/vars/functions/t-method.md)).

## Vergleich mit ähnlichen Metriken

* **Seitenereignisse vs. [Seitenansichten](page-views.md)**: Seitenereignisse zählen die Anzahl der Linktracking-Aufrufe ([`tl()`](/help/implement/vars/functions/tl-method.md)) und schließen Seitenansichts-Tracking-Aufrufe ([`t()`](/help/implement/vars/functions/t-method.md)) aus. Im Gegensatz dazu zählen Seitenansichten die Anzahl der Seitenansichts-Tracking-Aufrufe und schließen Links aus.
