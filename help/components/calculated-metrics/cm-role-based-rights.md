---
description: Bei den Rechten für berechnete Metriken wird zwischen Benutzern der Administratorebene und Nicht-Administratoren unterschieden.
title: Rollenbasierte Berechtigungen
feature: Calculated Metrics
exl-id: 018d9ef5-5a6f-4ebc-a241-c1291ba6b561
source-git-commit: 325a42c080290509309e90c9127138800d5ac496
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 81%

---

# Rollenbasierte Berechtigungen

Bei den Rechten für berechnete Metriken wird zwischen Benutzern der Administratorebene und Nicht-Administratoren unterschieden.

|  | Erstellung | Freigeben | Anzeigen/Verwalten | Genehmigen | Übernehmen |
|--- |--- |--- |--- |--- |--- |
| Benutzer auf Admin-Ebene | Administratoren können in der Admin Console berechnete Metriken sowie Produktprofile erstellen, um die Rechte von Benutzern zur Erstellung berechneter Metriken einzuschränken. | Können eine Freigabe für das gesamte Unternehmen, für Benutzergruppen und für einzelne Benutzer durchführen. | Report Builder: Kann anzeigen/bearbeiten/löschen usw. die eigenen berechneten sowie die freigegeben Metriken anzeigen/bearbeiten/löschen usw. | Können berechnete Metriken als autorisiert genehmigen. | Können beliebige berechnete Metriken innerhalb der gesamten Organisation anwenden. |
| Benutzer, die keine Administratoren sind | Standardmäßig können Benutzer berechnete Metriken erstellen. Diese Rechte können jedoch von Administratoren eingeschränkt werden. | Können nur für einzelne Benutzer freigeben. | Können nur Nur ihre eigenen berechneten Metriken. Benutzer ohne Administratorrechte müssen Zugriff auf alle Komponentenereignisse haben, um eine freigegebene Metrik anzeigen zu können (die Berechtigungen in der Admin Console werden weiterhin erzwungen).  Wenn ein Dashboard oder ein terminierter Bericht für einen Nicht-Administrator freigegeben wird, die Metrik für diesen Benutzer aber nicht freigegeben wurde, wird der Bericht mit angewendeter Metrik ausgeführt (vorausgesetzt, der Benutzer ist berechtigt, die Ereignisse anzuzeigen). Er kann allerdings nicht die Definition anzeigen oder die Metrik bearbeiten. | Können ausschließlich genehmigte berechnete Metriken nutzen. Können keine Metriken als genehmigt markieren. | Können ihre eigenen berechneten Metriken und Segmente, die für sie freigegeben wurden, anwenden. |
