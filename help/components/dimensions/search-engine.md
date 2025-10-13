---
title: Suchmaschine
description: Die Suchmaschine, mit der der Besucher Ihre Site erreichte.
feature: Dimensions
exl-id: 2815f1fa-d938-4d2b-b864-c4ed834f3ed3
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 93%

---

# Suchmaschine

Die Dimension „Suchmaschine[&#x200B; zeigt die Suchmaschinen an](overview.md) die Besucher verwenden, um zu Ihrer Site zu gelangen. Ein Referrer muss die beiden folgenden Kriterien erfüllen, um als Suchmaschine: klassifiziert zu werden:

* Die Referrer-Domäne wird von Adobe als gültige Suchmaschine erkannt.
* In der Referrer-URL ist ein Abfragezeichenfolgenparameter für Suchbegriffe vorhanden. Der Abfragezeichenfolgenparameter kann leer sein (wie dies bei mehreren Suchmaschinen aus Datenschutzgründen der Fall ist).

Wenn Sie zwischen gebührenpflichtiger und kostenloser Suche unterscheiden möchten, ist eine [Gebührenpflichtige Sucherkennung](/help/admin/tools/manage-rs/edit-settings/general/paid-search-detection/paid-search-detection.md) erforderlich. Für Suchmaschinen stehen mehrere Dimensionen zur Verfügung:

* **Suchmaschine**: Die Suchmaschine, mit der Sie Ihre Site erreichen, unabhängig davon, ob die Suche gebührenpflichtig oder kostenlos ist.
* **Suchmaschine – bezahlt**: Die Suchmaschine, mit der Ihre Site erreicht wurde und die mit der gebührenpflichtigen Sucherkennung übereinstimmt.
* **Suchmaschine – kostenlos**: Die Suchmaschine, mit der Ihre Site erreicht wurde und die nicht mit der gebührenpflichtigen Sucherkennung übereinstimmt.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf mehrere interne Suchtabellen von Adobe. Jeder Wert basiert auf dem [Referrer](referrer.md) des Treffers, der von [internen URL-Filtern](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) abhängig ist. Vergewissern Sie sich, dass die Dimension „Referrer“ und die internen URL-Filter korrekt konfiguriert sind.

## Dimensionselemente

Zu den Dimensionselementen gehören Suchmaschinen, die zum Erreichen Ihrer Site verwendet werden. Zu den Beispielwerten gehören `"Google"`, `"Microsoft Bing"` und `"DuckDuckGo"`. Das Dimensionselement `"Unspecified"` ist der gesamte Traffic ohne Suchvorgänge.
