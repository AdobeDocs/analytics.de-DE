---
title: Suchbegriff
description: Der Suchbegriff, mit dem der Besucher Ihre Site erreichte.
feature: Dimensions
exl-id: 5a1236a6-f94b-4679-906a-b539afe36887
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 94%

---

# Suchbegriff

Der Suchbegriff [Dimension](overview.md) erfasst die Suchbegriffe, die Besucher zum Erreichen Ihrer Site verwenden.

>[!IMPORTANT]
>
>Die meisten Suchmaschinen übergeben den Suchbegriff nicht mehr, da die Datenschutzpraktiken zunehmen. Treffer, bei denen Adobe eine Suchmaschine erkennt, aber ein Suchbegriff fehlt, werden unter dem Dimensionselement `"Keyword unavailable"` gruppiert.

Ein Referrer muss die beiden folgenden Kriterien erfüllen, um als Suchbegriff klassifiziert zu werden:

* Die Referrer-Domäne wird von Adobe als gültige [Suchmaschine](search-engine.md) erkannt.
* In der Referrer-URL ist ein Abfragezeichenfolgenparameter für Suchbegriffe vorhanden. Wenn die Abfragezeichenfolge für Suchbegriffe vorhanden ist, jedoch keinen Wert enthält, wird sie unter dem Dimensionselement `"Keyword unavailable"` gruppiert.

Wenn Sie zwischen gebührenpflichtiger und kostenloser Suche unterscheiden möchten, ist eine [Gebührenpflichtige Sucherkennung](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/paid-search-detection/paid-search-detection.md) erforderlich. Für Suchbegriffe stehen mehrere Dimensionen zur Verfügung:

* **Suchbegriff**: Der Suchbegriff, mit dem Sie Ihre Site erreichen, unabhängig davon, ob die Suche gebührenpflichtig oder kostenlos ist.
* **Suchbegriff - bezahlt**: Der Suchbegriff, mit dem Ihre Site erreicht wurde und der mit der gebührenpflichtigen Sucherkennung übereinstimmt.
* **Suchbegriff - kostenlos**: Der Suchbegriff, mit dem Ihre Site erreicht wurde und der nicht mit der gebührenpflichtigen Sucherkennung übereinstimmt.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf mehrere interne Suchtabellen von Adobe. Jeder Wert basiert auf dem [Referrer](referrer.md) des Treffers, der von [internen URL-Filtern](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md) abhängig ist. Vergewissern Sie sich, dass die Dimension „Referrer“ und die internen URL-Filter korrekt konfiguriert sind.

## Dimensionselemente

Zu den Dimensionselementen gehören Suchbegriffe, die zum Erreichen Ihrer Site verwendet werden. Das Dimensionselement `"Unspecified"` ist der gesamte Traffic ohne Suchvorgänge.
