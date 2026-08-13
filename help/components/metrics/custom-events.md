---
title: Benutzerspezifische Ereignisse
description: Die Anzahl der Treffer, bei denen ein benutzerspezifisches Ereignis vorhanden ist.
feature: Metrics
exl-id: 9ae3ff53-8634-466a-a9f6-786c1e62c2fa
TQID: https://experienceleague.adobe.com/1D8ONiUuG3T6DqM7HygbBbf0Y4ja5ej1Hfy8-hKo0yg
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: e7d92df1-c5ba-4e93-85df-f83171b889beid: f1f1a2d4-0976-4881-b091-c2bb8de7ffacid: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 223
ht-degree: 91%

---

# Benutzerspezifische Ereignisse

*Auf dieser Hilfeseite wird beschrieben, wie benutzerspezifische Ereignisse als Metrik funktionieren. Informationen dazu, wie benutzerspezifische Ereignisse als Implementierungsvariable funktionieren, finden Sie unter [Übersicht über Ereignisse](/help/implement/vars/page-vars/events/events-overview.md) im Benutzerhandbuch zu Implementierungen.*

Benutzerspezifisches Ereignis [Metriken](overview.md) zeigen die Anzahl der Treffer an, bei denen ein bestimmtes benutzerspezifisches Ereignis in einer Bildanforderung festgelegt wurde. Diese Metriken sind für viele Implementierungen unverzichtbar, da sie Einblicke in unternehmensspezifische Ereignisse bieten.

## Berechnung dieser Metrik

Benutzerspezifische Ereignisse werden je nach Typ unterschiedlich berechnet. Sie können den Typ eines Ereignisses in den Report Suite-Einstellungen unter [Erfolgsergebnisse](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/c-success-events/success-event.md) überprüfen.

* **Zählerereignisse**: Die Standardeinstellung für Ereignisse. Die meisten Ereignisse sind Zählerereignisse. Zählt die Anzahl der Treffer, bei denen das passende benutzerspezifische Ereignis `event1` – `event1000` in der [`events`](/help/implement/vars/page-vars/events/events-overview.md)-Variablen vorhanden ist.
* **Numerische Ereignisse**: Summieren den numerischen Wert, der dem Ereignis in der `events`-Variablen zugewiesenen ist.
* **Währungsereignisse**: Wendet die Währungsumrechnung auf den Wechselkurs dieses Tages an und summiert dann den numerischen Wert, der jedem Treffer in der `events`-Variablen zugewiesen ist.

Die Anzahl der verfügbaren Ereignisse hängt vom Analytics-Vertrag Ihres Unternehmens ab. In den meisten Unternehmen, die nicht über einen Altvertrag verfügen, stehen 1000 benutzerdefinierte Ereignisse zur Verfügung. Wenden Sie sich an Ihr Adobe-Accountteam, wenn Sie nicht sicher sind, wie viele benutzerdefinierte Ereignisse Ihnen zur Verfügung stehen.

Adobe empfiehlt, dass Sie die Verwendung der einzelnen Ereignisse im [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) Ihres Unternehmens erfassen.
