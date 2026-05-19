---
description: Beispiel mit einer Reihe von Server-Aufrufen, die bei einer gewöhnlichen Kundeninteraktion gesendet werden.
keywords: Analytics-Implementierung
subtopic: Visitors
title: Beispiel zur geräteübergreifenden Besucheridentifizierung
feature: Implementation Basics
exl-id: c68bb745-29de-48e3-8731-d714503a2447
role: Developer
TQID: https://experienceleague.adobe.com/ZYFxZyY5ZzmM064d2vx-8Ek-LftVwhxSsvLkzE9mgCI
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 386
ht-degree: 83%

---

# Beispiel zur geräteübergreifenden Besucheridentifizierung

>[!IMPORTANT]
>
>Diese Methode zur geräteübergreifenden Identifizierung von Besuchern wird nicht mehr empfohlen. Weitere Informationen finden Sie unter [Cross-Device Analytics](/help/components/cda/overview.md) im Benutzerhandbuch zu den Komponenten.

Das folgende Beispiel veranschaulicht die geräteübergreifende Besucheridentifizierung anhand eines Beispiels von Server-Aufrufen, die in einer üblichen Kundeninteraktion gesendet werden.

| Server-Aufruf | Aktion | Besucher-ID-Cookie | Besucher-ID-Variable | Gültige Besucher-ID | Seitennummer des Besuchs | Besuchsnummer |
|--- |--- |--- |--- |--- |--- |--- |
| 1 | Ein Besucher klickt auf einen Link in einer Marketing-E-Mail und gelangt so von seinem privaten Computer aus auf Ihre Website. Dieser Besucher hat Ihre Site in der Vergangenheit 7 weitere Male besucht. | 1 | – | 1 | 1 | 8 |
| 2-8 | Besucht 7 zusätzliche Seiten auf Ihrer Site. | 1 | – | 1 | 2-8 | 8 |
| 9 | Authentifizierung auf dem Heimcomputer. | 1 | CID1 | CID1 | 9 <br>(Dies ist der erste Treffer für CID1, also übernimmt CID1 und wird für das Besucherprofil von Besucher-ID 1 weiterverwendet.) | 8 |
| 10 | Besuche 1 zusätzliche Seite. | 1 | CID1 | CID1 | 10 | 8 |
| 11 | Öffnet Ihre Website auf seinem Laptop im Büro. Dieser Besucher hat Ihre Site vor der Verwendung dieses Geräts nicht besucht. | 2 | – | 2 | 1 | 1 |
| 12 | Authentifizierung auf Laptop. | 2 | CID1 | CID1 | 1 | 9 |
| 13 | Aufrufe 1 zusätzliche Seite. | 2 | CID1 | CID1 | 2 | 9 |

## Besuchszählung

Analytics zählt einen Besuch bei jedem Treffer, bei dem die Besuchsseitenzahl gleich 1 ist.

In der obigen Tabelle wurde ein neuer Besuch viermal gezählt: bei Treffern 1, 9, 11 und 12.

## Besucherzählung

In Analytics wird jede Unique-Visitor-ID als ein Unique Visitor gezählt.

In der obigen Tabelle wurde ein neuer Besucher dreimal gezählt: bei Treffern 1, 9 und 10.

Wenn Sie die geräteübergreifende Besucheridentifizierung verwenden, kann sich die Anzahl der Unique Visitors, die Sie sehen, erhöhen. So kann der Besucher während desselben Besuchs doppelt gezählt werden: Das erste Mal bei seinem ersten Besuch, und das zweite Mal nach seiner Authentifizierung.

![](assets/visitors.png)

Nach der anfänglichen Zuordnung verhält sich die Besuchsanzahl wieder wie gewohnt, da der Besucher über das Besucher-Cookie zugeordnet wird. Wenn der Besucher später wieder auf Ihre Website zurückkehrt und sich authentifiziert, wird die Besucheranzahl nicht überhöht, da sich die effektive Besucher-ID nach der Authentifizierung nicht mehr geändert hat.

![](assets/visitors_2.png)

Stellen Sie sicher, dass Sie bei der Identifizierung von Unique Visitors so konsistent wie möglich sind. Verwenden Sie beispielsweise immer die `visitorID`-Variable, wenn der Benutzer authentifiziert ist.
