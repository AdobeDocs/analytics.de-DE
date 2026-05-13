---
description: Nachschlagetabelle zur Bestimmung des Typs eines Treffers basierend auf einem Seitenereignis.
keywords: page;event;page_event;post_page_event
title: Seitenereignissuche
feature: Data Feeds
exl-id: ef0467df-b94b-4cec-b312-96d8f42c23b0
TQID: https://experienceleague.adobe.com/QAGYKNnpMl2tM6BRux7BBL-YFpMTgUIXsHT-9bGKWnA
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 226
ht-degree: 100%

---

# Seitenereignissuche

Nachschlagetabelle zur Bestimmung des Typs eines Treffers basierend auf dem Wert `page_event`. Gemäß der [Datenspaltenreferenz](datafeeds-reference.md) sind die Spalten `page_event` und `post_page_event` tinyint unsigned.

* Siehe [`t()`](/help/implement/vars/functions/t-method.md), um die Implementierung von Seitenansichtsaufrufen für AppMeasurement und Web SDK zu verstehen.
* Siehe [`tl()`](/help/implement/vars/functions/tl-method.md), um die Implementierung von Linktracking-Aufrufen für AppMeasurement und Web SDK zu verstehen.
* Siehe [Implementieren von Adobe Analytics mit dem Adobe Experience Platform Edge Network](/help/implement/aep-edge/overview.md), um zu verstehen, wie Adobe Analytics XDM-Payloads in Seitenereignistypen übersetzt.

| Wert `page_event` | Wert `post_page_event` | Beschreibung |
| --- | --- | --- |
| `0` | `0` | Alle standardmäßigen Seitenansichtsaufrufe. Dies ist der Standardwert für die meisten Treffer. |
| `10` | `100` | Benutzerdefinierte Links. Legen Sie den Link-Typ auf `o` (AppMeasurement) oder `xdm.web.webInteraction.type` bis `other` (Web SDK oder Mobile SDK) fest. |
| `11` | `101` | Download-Links. Legen Sie den Link-Typ auf `d` (AppMeasurement) oder `xdm.web.webInteraction.type` bis `download` (Web SDK oder Mobile SDK) fest. |
| `12` | `102` | Exit-Links. Legen Sie den Link-Typ auf `e` (AppMeasurement) oder `xdm.web.webInteraction.type` bis `exit` (Web SDK oder Mobile SDK) fest. |
| `31` | `76` | Medienstart |
| `32` | `77` | Medienaktualisierungen (ohne andere Variablenverarbeitung) |
| `33` | `78` | Medienaktualisierungen (mit anderer Variablenverarbeitung) |
| `40` | `80` | Umfrage |
| `50` | `50` | Streaming-Medienstart |
| `51` | `51` | Streaming-Medienabschluss |
| `52` | `52` | Streaming-Medien-Scrubbing |
| `53` | `53` | Keep-Alive für Streaming-Medien |
| `54` | `54` | Anzeigenstart für Streaming-Medien |
| `55` | `55` | Anzeigenabschluss für Streaming-Medien |
| `56` | `56` | Anzeigen-Scrubbing für Streaming-Medien |
| `60` | `60` | Primetime-Medienstart |
| `61` | `61` | Primetime-Medienabschluss |
| `62` | `62` | Primetime-Medien-Scrubbing |
| `63` | `63` | Keep-Alive für Primetime-Medien |
| `64` | `64` | Anzeigenstart für Primetime-Medien |
| `65` | `65` | Anzeigenabschluss für Primetime-Medien |
| `66` | `66` | Anzeigen-Scrubbing für Primetime-Medien |
| `70` | `70` | Enthält Target-Aktivitätsdaten |
