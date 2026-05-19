---
description: Bei der Verwendung von „Ausdruck anpassen“ für die Festlegung eines Datumsbereichs sind zwei Umstände besonders zu beachten
title: Überlegungen zum benutzerdefinierten Datum
uuid: a3bb3a63-0f15-4292-ade7-4ea852fe68c8
feature: Report Builder
role: User, Admin
exl-id: 66b817b3-7e9e-4030-92f3-797e730f9661
TQID: https://experienceleague.adobe.com/7PLNffmZnNnQ2X0HgnqYa8R3zWQvFPMSM8sbWocmxH4
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2:
  - id: ac8a38fa-dec3-4581-8f64-178fde9f64e8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 415
ht-degree: 19%

---

# Überlegungen zum benutzerdefinierten Datum

{{legacy-arb}}

Bei der Verwendung von „Ausdruck anpassen“ für die Festlegung eines Datumsbereichs sind zwei Umstände besonders zu beachten:

* Der Tag, an dem der Bericht (ab) ausgeführt (oder Anforderungen aktualisiert) wird, bestimmt, welche Daten verfügbar sind.
* Das Rollover von Start- und Enddatum des Berichts wirkt sich auf den vom Bericht abgedeckten Datumsbereich aus.

Da die Verfügbarkeit der Daten sowohl vom Zeitrahmen des Berichts als auch von dem Datum abhängt, an dem Sie die Anfragen im Bericht aktualisieren, stellen Sie sicher, dass Sie den Bericht an dem entsprechenden Tag ausführen, um die gewünschten Informationen zu extrahieren. Die folgenden Beispiele zeigen beide Überlegungen.

Angenommen, Sie stellen eine Anfrage für [!UICONTROL Seitenansichten] mit aggregierter Granularität. In Nordamerika beginnt die Woche am Sonntag. Um aktualisierte Berichte für den Zeitraum von Sonntag bis Samstag zu erhalten (z. B. 23. November bis 29. November 2008), führen Sie den Bericht (Aktualisierungsanfragen) am Sonntag (30. November) für die Vorwoche (23. 11. bis 11. November 29) aus.

Verwenden Sie diesen benutzerdefinierten Ausdruck:

*Von:* cw-1w *Bis:* cw-1d

Eine Analyse des angepassten Ausdrucks, wenn das einschließlich [!UICONTROL Enddatum] für die Anfrage 11/30 ist:

*Von:* cw-1w

der aktuelle Tag in der am Sonntag, dem 30. November beginnenden Woche minus sieben Tage = der Tag der am Sonntag, dem 23. November beginnenden vergangenen Woche

*An:* cw-1d

Der Tag der aktuellen Woche, die am Sonntag beginnt, 30. November minus einem Tag = Samstag, 29. November

Nachdem der angepasste Ausdruck der Tabelle zugeordnet wurde, aktualisieren Sie die Anfrage mit Sonntag, dem 30. November 2008 als einschließlich [!UICONTROL Enddatum] für die schwebende Anfrage. Die Daten spiegeln den einwöchigen Zeitraum wider.

Wenn Sie stattdessen den Ausdruck aktualisieren und Samstag, den 29. November als [!UICONTROL Enddatum] für die Gleitkommaanforderung angeben, spiegeln die Daten die Wochen 11/16 bis 11/22 wider. Dies liegt daran, dass das Referenzdatum für die Anfrageaktualisierung einen Tag früher liegt.

Im Folgenden finden Sie die Unterschiede, wenn das [!UICONTROL &#x200B; (Enddatum] für die Anfrage 11/29 ist:

*Von:* cw-1w

der aktuelle Tag in der am Sonntag, dem 23. November beginnenden Woche minus sieben Tage = der Tag der am Sonntag, dem 16. November beginnenden vergangenen Woche

*An:* cw-1d

Der Tag der aktuellen Woche, die am Sonntag beginnt, 23. November minus einem Tag = Samstag, 22. November

In Europa und einigen anderen Ländern beginnt die Woche am Montag und nicht am Sonntag. In diesem Fall können Sie den Kalender anpassen, um das Startdatum zu ändern. (Siehe [Benutzerdefinierter Kalender](/help/analyze/legacy-report-builder/data-requests/configuring-report-dates/custom-calendar.md).)
