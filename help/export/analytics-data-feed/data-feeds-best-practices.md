---
description: Erfahren Sie mehr über Best Practices für die Verarbeitung und Bereitstellung von Daten-Feeds in Analytics.
keywords: Daten-Feed;Best Practices;Traffic-Spitze;stündlich;FTP
title: Best Practice und allgemeine Informationen
feature: Data Feeds
exl-id: 5f6fbc13-b176-4f69-8f2d-7accc6e6ac2d
TQID: 'https://experienceleague.adobe.com/-8EoregiCONFrXywjKP5zMdypH-FM67ij1nVfxupBdY'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
subfeature_v2:
  - id: ede9f3ba-4ee4-4497-9d8e-e9da5848bda0
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 84%

---

# Best Practices für Daten-Feeds

Nachstehend sind einige Best-Practice-Methoden für die Verarbeitung und Bereitstellung von Datenfeeds aufgeführt.

* Stellen Sie sicher, dass Sie erwartete Traffic-Spitzen frühzeitig kommunizieren. Latenz wirkt sich direkt auf die Verarbeitungszeit für Daten-Feeds aus. Siehe [Planen von Traffic-Spitzen](/help/admin/tools/manage-rs/edit-settings/c-traffic-management/t-traffic-schedule-spike.md) im Admin-Benutzerhandbuch.

* Daten-Feeds enthalten kein Service-Level-Agreement, es sei denn, in Ihrem Vertrag mit Adobe ist dies ausdrücklich festgelegt. Feeds werden in der Regel mehrere Stunden nach Ablauf des Berichtsfensters bereitgestellt, gelegentlich kann es jedoch bis zu 12 Stunden oder mehr dauern.

* Stündliche Feeds mit der Bereitstellung mehrerer Dateien werden am schnellsten verarbeitet. Erwägen Sie die Verwendung stündlicher Feeds mit mehreren Dateien, wenn eine rechtzeitige Bereitstellung für Ihre Organisation hohe Priorität hat.

* Wenn Sie Ihren Feed-Aufnahmevorgang automatisieren, sollten Sie die Möglichkeit in Betracht ziehen, dass Treffer und Dateien mehrmals übertragen werden können. Ihr Feed-Aufnahmevorgang muss doppelte Treffer und doppelte Dateien verarbeiten, ohne Fehler zu verursachen oder Daten zu duplizieren. Es wird empfohlen, die Spalten `hitid_high` und `hitid_low` zur eindeutigen Identifizierung eines Treffers zu verwenden.

  In seltenen Fällen werden möglicherweise doppelte Werte für `hitid_high` und `hitid_low` angezeigt. Bestätigen Sie in diesem Fall, dass die Datei noch nicht gesendet und verarbeitet wurde. Wenn nur einige Zeilen in einer Datei dupliziert sind, sollten Sie `visit_num` und `visit_page_num` hinzufügen, um die Eindeutigkeit zu ermitteln.

* Wenn Sie FTP verwenden (nicht empfohlen), stellen Sie sicher, dass auf Ihrer FTP-Site ausreichend Platz vorhanden ist. Entfernen Sie Dateien regelmäßig aus dem Ziel, damit Ihnen nicht versehentlich der Speicherplatz ausgeht.

* Wenn Sie sFTP verwenden (nicht empfohlen), lesen oder löschen Sie keine Dateien mit einem `.part` Suffix. Das `.part`-Suffix zeigt an, dass die Datei teilweise übertragen wurde. Sobald die Datei übertragen wurde, verschwindet das `.part`-Suffix.