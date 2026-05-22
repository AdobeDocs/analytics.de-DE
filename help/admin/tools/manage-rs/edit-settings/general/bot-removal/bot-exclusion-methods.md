---
title: Vergleich verschiedener Methoden zum Ausschluss von Bots
description: Ermöglicht den Vergleich verschiedener Methoden zum Ausschluss von Bots.
exl-id: c54ba98a-b396-479e-bfe8-dc6211b26f61
role: Admin
feature: Bot Removal
TQID: 'https://experienceleague.adobe.com/lbb7D0NNvtqw-65JRgT-K7I1k0lBw2ekfcoOTAmbQi0'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
subfeature_v2:
  - id: ec140990-1570-4311-94d4-2d6b38511bbe
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 327
ht-degree: 46%

---

# Vergleich verschiedener Methoden zum Ausschluss von Bots

Die folgende Tabelle zeigt verschiedene Methoden zum Ausschluss von Bots und deren Vergleich untereinander.

| Methode | Bot-Regeln | Nach IP-Adresse ausschließen | Kundenattribute | Segmentierung | Bewertung durch Dritte + Segmentierung | Unterdrücken des Server-Aufrufs für Bots zur Laufzeit | Benutzerspezifische DB VISTA-Regel |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Beschreibung der Methode zum Ausschluss von Daten** | Ausschließen basierend auf Benutzeragent, IP-Adresse oder IP-Adressbereich | IP-Adresse | Eine Markierung in Kundenattributen, die ECID als Bot identifiziert | Kriterien in einem Analytics-Segment, das bekannte Bots basierend auf dem Verhalten von Bots identifiziert | Ein Drittanbieter wie [Perimeter X](https://www.perimeterx.com) oder [Akamai Bot Manager](https://www.akamai.com/de/de/products/security/bot-manager.jsp) weist jeder Seitenansicht einen Wert zu, der angibt, mit welcher Wahrscheinlichkeit es sich um einen Bot handelt. Die Bewertung wird an Analytics gesendet und Segmente können verwendet werden, um Daten basierend auf dem Ergebnis auszufiltern. | Client-seitige Logik verhindert, dass der Analytics-Server-Aufruf für Bots ausgeführt wird. | Eine VISTA-Regel verschiebt Traffic von Bots, die bestimmte Kriterien erfüllen, in eine separate Report Suite. |
| **Sind Bot-Namen für das Reporting verfügbar?** | Ja | Nein | Nein | Nein | Nein | Nein | Ja |
| **Kann angezeigt werden, welche Seiten von Bots besucht werden?** | Ja | Nein | Nein | Nein | Ja | Nein | Ja |
| **Entstehen Kosten für Server-Aufrufe wegen Bots?** | Ja | Ja | Ja | Ja | Ja | Nein | Ja |
| **Sind Bot-Daten in Daten-Feeds verfügbar?** | Nein | Nein | Ja | Nein | Ja | Nein | Ja |
| **Ist es möglich, Berichte zum Traffic von Bots zu erstellen, als ob es sich um tatsächliche Server-Aufrufe handelt?** | Nein | Nein | Ja | Ja | Ja | Nein | Nein |
| **Können Daten nachträglich aus einem Datensatz entfernt werden?** | Nein | Nein | Ja, sobald deklarierte IDs implementiert sind | Ja | Ja, sobald die Bewertungen implementiert wurden | Nein | Nein |
| **Gibt es bei den Kriterien Beschränkungen für Unique-Werte?** | Nein | Nein | Nein | Ja | Nein | Nein | Nein |
| **Fallen zusätzliche Kosten an?** | Nein | Nein | Möglich, je nach Analytics-SKU | Nein | Ja | Nein | Ja - Kosten für die Implementierung und Pflege einer VISTA-Regel |
