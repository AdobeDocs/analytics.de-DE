---
description: Suchtabelle zur Bestimmung des Typs eines Treffers auf der Grundlage des Seitenereignisses.
keywords: page;event;page_event;post_page_event
title: Seitenereignissuche
feature: Data Feeds
exl-id: ef0467df-b94b-4cec-b312-96d8f42c23b0
source-git-commit: e16b0d7b3fe585dc8e9274a77833ad5af3c63124
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 4%

---

# Seitenereignissuche

Suchtabelle zur Bestimmung des Typs eines Treffers auf der Grundlage des `page_event`. Wie in der [Datenspaltenreferenz“ erwähnt](datafeeds-reference.md) sind die `page_event` und `post_page_event` Spalten winzig unsigniert.

* Siehe [`t()`](/help/implement/vars/functions/t-method.md) , um die Implementierung von Seitenansichtsaufrufen für AppMeasurement und die Web-SDK zu verstehen.
* Siehe [`tl()`](/help/implement/vars/functions/tl-method.md) , um die Implementierung von Linktracking-Aufrufen für AppMeasurement und die Web-SDK zu verstehen.
* Unter [Implementieren von Adobe Analytics mit der Adobe Experience Platform-Edge Network](/help/implement/aep-edge/overview.md) erfahren Sie, wie Adobe Analytics XDM-Payloads in Seitenereignistypen übersetzt.

| Wert `page_event` | Wert `post_page_event` | Beschreibung |
| --- | --- | --- |
| `0` | `0` | Alle Aufrufe von Standardseitenansichten. Dies ist der Standardwert für die meisten Treffer. |
| `10` | `100` | Benutzerdefinierte Links. Setzen Sie den Link-Typ auf `o` (AppMeasurement) oder `xdm.web.webInteraction.type` auf `other` (Web SDK oder Mobile SDK). |
| `11` | `101` | Downloadlinks. Setzen Sie den Link-Typ auf `d` (AppMeasurement) oder `xdm.web.webInteraction.type` auf `download` (Web SDK oder Mobile SDK). |
| `12` | `102` | Exitlinks Setzen Sie den Link-Typ auf `e` (AppMeasurement) oder `xdm.web.webInteraction.type` auf `exit` (Web SDK oder Mobile SDK). |
| `31` | `76` | Medienstart |
| `32` | `77` | Medienaktualisierungen (ohne andere Variablenverarbeitung) |
| `33` | `78` | Medienaktualisierungen (mit anderer Variablenverarbeitung) |
| `40` | `80` | Umfrage |
| `50` | `50` | Start von Streaming-Medien |
| `51` | `51` | Schließen von Streaming-Medien |
| `52` | `52` | Bereinigung von Streaming-Medien |
| `53` | `53` | Streaming-Medien bleiben am Leben |
| `54` | `54` | Anzeigenstart für Streaming-Medien |
| `55` | `55` | Streaming-Medien und Schließen |
| `56` | `56` | Streaming-Medien und Bereinigung |
| `60` | `60` | Medienstart zu Primetime |
| `61` | `61` | Primetime-Medienschluss |
| `62` | `62` | Primetime-Medienbereinigung |
| `63` | `63` | Primetime-Medien bleiben am Leben |
| `64` | `64` | Anzeigenstart für Primetime-Medien |
| `65` | `65` | Primetime-Medienanzeige schließen |
| `66` | `66` | Primetime-Medien und -Scrubbing |
| `70` | `70` | Enthält Target-Aktivitätsdaten |
