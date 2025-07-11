---
description: In diesem Abschnitt wird erläutert, wie häufig verwendete Metriken mithilfe von Daten-Feeds berechnet werden.
keywords: Daten-Feed;Auftrag;Metrik;vor Spalte;nach Spalte;Bots;Datumsfilterung;Ereigniszeichenfolge;allgemein;Formeln
title: Metriken berechnen
feature: Data Feeds
exl-id: f9b0d637-7a6e-416a-adff-3c7e533bfac7
source-git-commit: adee2f1013cfd2ae231e3133b5a5327b8792bd16
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 76%

---

# Berechnung von häufig verwendeten Metriken mithilfe von Daten-Feeds

In diesem Abschnitt wird erläutert, wie häufig verwendete Metriken mithilfe von Daten-Feeds berechnet werden.

>[!NOTE]
>
>Treffer, die normalerweise von Analysis Workspace ausgeschlossen sind, sind in Daten-Feeds enthalten. Erwägen Sie, Ihren Abfragen die folgenden Bedingungen hinzuzufügen, falls sie relevant sind:
>
>* **`exclude_hit`**: Analysis Workspace umfasst nur Daten, bei denen `exclude_hit = 0`.
>* **`customer_perspective`**: Analysis Workspace umfasst nur Daten, bei denen `customer_perspective = 0` sind, es sei denn, Sie verwenden eine Virtual Report Suite, die mobile Hintergrundtreffer enthält.
>* **`hit_source`**: Daten aus Datenquellen können Unterschiede zwischen Rohdaten und Analysis Workspace enthalten. Wenn Sie Treffer aus Datenquellen ausschließen möchten, schließen Sie alle Zeilen aus, für die `hit_source = 5,7,8,9` gilt.

## Seitenansichten

1. Zählt die Anzahl der Zeilen, bei denen sich ein Wert in `post_pagename` oder `post_page_url` befindet.

## Vorkommen

1. Zählen Sie die Gesamtzahl der Zeilen.

## Besuche

1. Verkettet `post_visid_high`, `post_visid_low`, `visit_num` und `visit_start_time_gmt`.
1. Zählen Sie die Anzahl der eindeutigen Werte.

>[!TIP]
>
>In seltenen Fällen kann es vorkommen, dass bei Problemen mit dem Internet oder dem System oder der Verwendung benutzerspezifischer Besucher-IDs dieselben `visit_num`-Werte für verschiedene Besuche verwendet werden. Verwenden Sie bei der Zählung von Besuchen `visit_start_time_gmt`, um sicherzustellen, dass diese Besuche gezählt werden, auch wenn dies optional ist.

## Besuchende

Alle Methoden, die Adobe verwendet, um Unique Visitors zu identifizieren (benutzerdefinierte Besucher-ID, Experience Cloud-ID-Service usw.), werden letztendlich als Wert in `post_visid_high` und `post_visid_low` berechnet. Die Verkettung dieser beiden Spalten kann als Standardmethode zur Identifizierung von Unique Visitors verwendet werden, unabhängig davon, wie Besucher als Unique Visitors identifiziert wurden. In der Spalte `post_visid_type` ist die Methode ersichtlich, die Adobe zur Identifizierung eines Unique Visitors verwendet hat.

1. Verketten Sie `post_visid_high` und `post_visid_low`.
2. Zählen Sie die Anzahl der eindeutigen Werte.

## Benutzerspezifische Links, Download- oder Exitlinks

1. Zählen Sie die Anzahl der Zeilen, wobei Folgendes gilt:
   * `post_page_event = 100` für benutzerspezifische Links
   * `post_page_event = 101` für Downloadlinks
   * `post_page_event = 102` für Exitlinks

## Benutzerspezifische Ereignisse

Alle Metriken werden in der Spalte `post_event_list` als kommagetrennte Ganzzahlen gezählt. Verwenden Sie `event.tsv`, um numerische Werte mit dem gewünschten Ereignis abzugleichen. `post_event_list = 1,200` gibt beispielsweise an, dass der Treffer ein Kaufereignis und das benutzerdefinierte Ereignis 1 enthielt.

1. Zählen Sie die Häufigkeit, mit der der Ereignissuchwert in `post_event_list` auftritt.

## Besuchszeit

Treffer müssen zunächst nach Besuchen gruppiert und dann nach der Trefferanzahl innerhalb des Besuchs geordnet werden.

1. Verketten Sie `post_visid_high`, `post_visid_low`, `visit_num` und `visit_start_time_gmt`.
2. Nehmen Sie nach diesem verketteten Wert eine Sortierung vor und wenden Sie dann eine sekundäre Sortierung nach `visit_page_num` an.
3. Wenn ein Treffer nicht der letzte während eines Besuchs ist, subtrahieren Sie den Wert `post_cust_hit_time` vom Wert `post_cust_hit_time` des nachfolgenden Treffers.
4. Diese Zahl ist die Dauer der Besuchszeit (in Sekunden) für den Treffer. Filter können angewendet werden, um Dimensionselemente oder Ereignisse auszuwählen.

## Bestellungen, Stückzahl und Umsatz

Wenn der Wert `currency` eines Treffers nicht mit der Währung einer Report Suite übereinstimmt, wird er mit dem Umrechnungskurs dieses Tages konvertiert. Die Spalte `post_product_list` verwendet den konvertierten Währungswert, sodass alle Treffer in dieser Spalte dieselbe Währung verwenden.

1. Schließen Sie alle Zeilen mit `duplicate_purchase = 1` aus.
2. Schließen Sie nur Zeilen ein, in denen das Kaufereignis in `event_list` enthalten ist.
3. Parsen Sie die Spalte `post_product_list`, um alle Preisdaten zu extrahieren. Die Spalte `post_product_list` ist so formatiert wie die Variable `s.products`.
4. Berechnen Sie die gewünschte Metrik:
   * Zählen Sie die Zeilen zur Berechnung der Bestellungen.
   * Addieren Sie die Anzahl der `quantity`-Einheiten in der Produktzeichenfolge, um die Stückzahlen zu berechnen.
   * Addieren Sie die Anzahl der `price`-Einheiten in der Produktzeichenfolge, um den Umsatz zu berechnen.
