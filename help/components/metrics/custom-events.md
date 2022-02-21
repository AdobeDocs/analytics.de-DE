---
title: Benutzerspezifische Ereignisse
description: Die Anzahl der Treffer, bei denen ein benutzerspezifisches Ereignis vorhanden ist.
feature: Metrics
exl-id: 9ae3ff53-8634-466a-a9f6-786c1e62c2fa
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 100%

---

# Benutzerspezifische Ereignisse

*Auf dieser Hilfeseite wird beschrieben, wie benutzerspezifische Ereignisse als Metrik funktionieren. Informationen dazu, wie benutzerspezifische Ereignisse als Implementierungsvariable funktionieren, finden Sie unter [Übersicht über Ereignisse](/help/implement/vars/page-vars/events/events-overview.md) im Benutzerhandbuch zu Implementierungen.*

Die Metriken zum benutzerspezifischen Ereignis zeigen die Anzahl der Treffer an, bei denen ein bestimmtes benutzerspezifisches Ereignis in einer Bildanforderung festgelegt wurde. Diese Metriken sind für viele Implementierungen unverzichtbar, da sie Einblicke in unternehmensspezifische Ereignisse bieten.

## Berechnung dieser Metrik

Benutzerspezifische Ereignisse werden je nach Typ unterschiedlich berechnet. Sie können den Typ eines Ereignisses in den Report Suite-Einstellungen unter [Erfolgsergebnisse](../../admin/admin/c-success-events/success-event.md) überprüfen.

* **Zählerereignisse**: Die Standardeinstellung für Ereignisse. Die meisten Ereignisse sind Zählerereignisse. Zählt die Anzahl der Treffer, bei denen das passende benutzerspezifische Ereignis `event1` – `event1000` in der [`events`](/help/implement/vars/page-vars/events/events-overview.md)-Variablen vorhanden ist.
* **Numerische Ereignisse**: Summieren den numerischen Wert, der dem Ereignis in der `events`-Variablen zugewiesenen ist.
* **Währungsereignisse**: Wendet die Währungsumrechnung auf den Wechselkurs dieses Tages an und summiert dann den numerischen Wert, der jedem Treffer in der `events`-Variablen zugewiesen ist.

Die Anzahl der verfügbaren Ereignisse hängt vom Analytics-Vertrag Ihres Unternehmens ab. In den meisten Unternehmen, die nicht über einen Altvertrag verfügen, stehen 1000 benutzerdefinierte Ereignisse zur Verfügung. Wenden Sie sich an den Kundenbetreuer Ihres Unternehmens, wenn Sie nicht sicher sind, wie viele benutzerspezifische Ereignisse für Sie verfügbar sind.

Adobe empfiehlt, dass Sie die Verwendung der einzelnen Ereignisse im [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) Ihres Unternehmens erfassen.
