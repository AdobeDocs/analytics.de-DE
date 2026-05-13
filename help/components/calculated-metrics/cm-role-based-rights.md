---
description: Bei den Rechten für berechnete Metriken wird zwischen Benutzern der Administratorebene und Nicht-Administratoren unterschieden.
title: Rollenbasierte Berechtigungen
feature: Calculated Metrics
exl-id: 018d9ef5-5a6f-4ebc-a241-c1291ba6b561
TQID: https://experienceleague.adobe.com/M2ZwpkhpvhavBOwrVsDxcEYsS9kAFGAcuCl5TSUzxXU
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 244
ht-degree: 44%

---

# Rollenbasierte Berechtigungen

Bei den Rechten für berechnete Metriken wird zwischen Benutzern der Administratorebene und Nicht-Administratoren unterschieden.

|  | Erstellung | Freigeben | Anzeigen/Verwalten | Genehmigen | Übernehmen |
|--- |--- |--- |--- |--- |--- |
| Benutzer auf Admin-Ebene | Administratoren können in der Admin Console berechnete Metriken sowie Produktprofile erstellen, um die Rechte von Benutzern zur Erstellung berechneter Metriken einzuschränken. | Können eine Freigabe für das gesamte Unternehmen, für Benutzergruppen und für einzelne Benutzer durchführen. | Report Builder : Kann seine eigenen berechneten Metriken und die mit ihnen freigegebenen anzeigen/bearbeiten/löschen usw. | Kann berechnete Metriken als kanonisch genehmigen. | Kann beliebige berechnete Metriken im gesamten Unternehmen anwenden. |
| Benutzer, die keine Administratoren sind | Standardmäßig können Benutzer berechnete Metriken erstellen. Diese Rechte können jedoch von Administratoren eingeschränkt werden. | Freigabe nur für einzelne Benutzer möglich | Kann nur die eigenen berechneten Metriken anzeigen/bearbeiten/löschen usw. Benutzer ohne Administratorrechte müssen Zugriff auf alle Komponentenereignisse haben, um eine freigegebene Metrik anzeigen zu können (die Berechtigungen in der Admin Console werden weiterhin erzwungen).  Wenn ein Dashboard oder ein terminierter Bericht für einen Nicht-Administrator freigegeben wird, die Metrik für diesen Benutzer aber nicht freigegeben wurde, wird der Bericht mit angewendeter Metrik ausgeführt (vorausgesetzt, der Benutzer ist berechtigt, die Ereignisse anzuzeigen). Sie können jedoch die Definition nicht sehen und die Metrik nicht bearbeiten. | Kann nur genehmigte berechnete Metriken verwenden und nicht als genehmigt markieren. | Können ihre eigenen berechneten Metriken und Segmente anwenden, die für sie freigegeben wurden. |
