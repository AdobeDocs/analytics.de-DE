---
description: 'Activity Map verfolgt Links mit einem stabileren Algorithmus, der Folgendes ermöglicht '
solution: Analytics
title: Zuverlässiges Linktracking
topic: Activity map
uuid: a72b1652-2e69-41c7-8cf2-d39e9c705302
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Zuverlässiges Linktracking

Activity Map verfolgt Links mit einem stabileren Algorithmus, der Folgendes ermöglicht:

* Verfolgung von Seitenregionen, um zu verhindern, dass der gleiche Link auf unterschiedlichen Geräten verwechselt wird, da sich der Link an verschiedenen Positionen auf der Seite befindet,
* Eindeutigkeit von Links, d. h. unterschiedliche Links können nicht aufgrund von Problemen mit der Link-ID oder verschiedenen Browsermarken für ein und denselben Link gehalten werden.

Weitere Informationen zum Linktracking in Activity Map erhalten Sie [hier](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md).

## Art der Sammlung von PII-Daten mittels Activity Map-Linktracking {#section_AEE57510D17B4C21A7D49D32D21D67B9}

> [!CAUTION] Beim Aktivieren von Activity Map-Tracking erfassen Sie möglicherweise persönlich identifizierbare Informationen (PII). Diese Daten können alleine oder in Verbindung mit anderen Informationen dazu verwendet werden, eine Einzelperson zu identifizieren, zu kontaktieren oder zu lokalisieren oder eine Einzelperson im Kontext zu identifizieren.

Im Folgenden finden Sie einige Fälle, in denen PII-Daten möglicherweise mit dem Activity Map-Tracking gesammelt werden:

* `Mailto`-Links. Ein Mailto-Link ist ein HTML-Linktyp, der den standardmäßigen E-Mail-Client auf dem Computer für das Senden einer E-Mail aktiviert.
* `User ID`-Links, die in der Kopf-/Fußzeile einer Website angezeigt werden, nachdem sich der Benutzer angemeldet hat.
* Für Kreditinstitute wird möglicherweise die Kontonummer als ein Link angezeigt. Wenn darauf geklickt wird, wird der Linktext erfasst.
* Auf Websites für das Gesundheitswesen werden PII-Daten ebenfalls als Links angezeigt. Durch Klicken auf diese Links wird der Linktext erfasst. Dadurch werden die PII-Daten gesammelt.
