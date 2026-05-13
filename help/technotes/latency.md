---
description: Die nachfolgenden Informationen helfen bei der Fehlerbehebung von Report Suite-Latenzproblemen in Analytics-Daten.
keywords: fehlende Daten;langsam
title: Datenverfügbarkeit und -latenz
feature: Data Configuration and Collection
exl-id: fedef3ea-dde6-460f-90e3-1e661ed29b78
TQID: https://experienceleague.adobe.com/tUoPm4FFCjyp9J4w6fHMMe-guBoVzLwbpU0Tbk-lgCA
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 824
ht-degree: 81%

---

# Datenverfügbarkeit und -latenz in Adobe Analytics

Die vollständigen Daten sind im Allgemeinen zwei Stunden nach dem Erfassen der Daten in Berichten verfügbar. Die nachfolgenden Informationen helfen bei der Fehlerbehebung von Report Suite-Latenzproblemen in Analytics-Daten.

## Grundlagen des Daten-Batchings

Jeder Datenerfassungs-Server erfasst und verarbeitet Analytics-Rohdaten und lädt dann stündlich Batch-Daten für das Reporting hoch. Der Übertragungsvorgang dauert in der Regel 30 Minuten, sodass die normale Latenz für Traffic, der direkt nach Abschluss des vorherigen Upload-Prozesses auftritt, etwa 90 Minuten beträgt (60 Minuten bis zum nächsten Batch-Upload und dann 30 Minuten für die Dateiübertragung und Anzeige). Bei Traffic, der direkt vor dem Hochladen anfällt, kann die Datenlatenz auf 30 Minuten sinken (0 Minuten bis zum nächsten Batchupload und anschließend 30 Minuten für die Dateiübertragung und die Anzeige).

Bei Bedarf können Sie bei der Adobe-Kundenunterstützung anfordern, halbstündliche (statt stündliche) Batch-Daten-Uploads für Ihre meistgenutzten Report Suites einzurichten.

## Gründe für Latenz

Latenz ist eine Verzögerung, die länger dauert als die zwei Stunden, die Datenerfassungs-Server normalerweise für die vollständige Verarbeitung der Daten benötigen. Die Datenerfassung wird hierdurch nicht beeinträchtigt. Daten werden weiterhin für eine funktionierende Implementierung erfasst, unabhängig davon, wie hoch die Latenz einer Report Suite ist. Der Schweregrad (wie aktuell die Daten sind) und die Länge (die Zeit, die es dauert, um sie zu beheben) können stark variieren. Meist sind Latenzen nur auf eine einzelne Report Suite beschränkt.

Latenzzeiten werden durch eine der folgenden allgemeinen Kategorien verursacht:

* **Unerwartete Traffic-Spitzen:** Diese Art von Latenz tritt auf, wenn mehr Daten an eine Report Suite gesendet werden als vertraglich festgelegt oder erwartet wurde. Dies ist die häufigste Ursache für Latenzzeiten.
* **Normale Hardwareprobleme:** Adobe setzt branchenführende Strategien für die Rechenzentrumsverwaltung und -überwachung, Datenredundanz und Hardware-Zuverlässigkeit ein. Die Hardware wird regelmäßig und in Verbindung mit bekanntgegebenen Wartungsfenstern aktualisiert. Für außerplanmäßige Wartungsarbeiten an fehlerhafter Hardware kann ein vorübergehender Stopp der Datenverarbeitung (nicht der Datenerfassung) erforderlich sein, wenn Ersatz-Hardware in Betrieb genommen werden muss. Dieser vorübergehende Stillstand bei der Verarbeitung kann zu einer merklichen Latenzzeit führen.
* **Anomale Daten:** Unnatürliche Datenmuster, wie ungewöhnlich lange, von einem Bot oder Crawler verursachte Besuche, können zeitweilig bestimmte Verarbeitungslasten erhöhen, die dann zu Latenz führen.

## Von Latenz abhängige Funktionen

Einige Funktionen von Adobe Experience Cloud verfügen zusätzlich zur standardmäßigen Verarbeitungszeit auch über eine standardmäßige Latenzzeit.

* Für Analytics for Target (A4T) ist eine zusätzliche Latenz von 5 bis 10 Minuten erforderlich, damit gesammelte Daten von beiden Plattformen im selben Treffer gespeichert werden können.
* Daten mit Zeitstempel erfordern aufgrund verschiedener Server, auf denen diese Daten verarbeitet werden, zusätzliche Zeit. Treffer mit Zeitstempel, die (nahezu) in Echtzeit empfangen werden, können bis zu 15 Minuten erfordern. Treffer mit einem Zeitstempel von gestern können bis zu zwei Stunden dauern. Ältere Treffer können länger dauern und jeden Tag bis zu einer Höchstdauer von etwa 24 Stunden ansteigen.

## Möglichkeiten zur Senkung oder Vermeidung von Latenzen

Zur Vermeidung von Latenzzeiten oder Verkürzung der Wiederherstellungsdauer bei eingetretener Latenz gibt es mehrere Strategien:

* **Informieren Sie Adobe über erwartete Traffic-Spitzen:** Es ist zwar nicht möglich, jede Traffic-Spitze Ihrer Site vorherzusehen, es kann jedoch vorkommen, dass Sie einen erheblichen Traffic-Anstieg erwarten. Beispiele sind besonders erfolgreiche Phasen während der Feiertagssaison oder kurz nach dem Start einer großen Kampagne. In diesen Situationen stellt Adobe eine Möglichkeit bereit, wie Ihre Firma uns über erwartete Trafficzunahmen informieren kann, damit wir Ihrer Report Suite zusätzliche Verarbeitungsressourcen zuweisen können. Weitere Informationen zur Benachrichtigung von Adobe über erhöhten Traffic finden Sie unter [Planen von Traffic-Spitzen](/help/admin/tools/manage-rs/edit-settings/c-traffic-management/t-traffic-schedule-spike.md) im Administratorhandbuch.
* **Berücksichtigen Sie beim Aktivieren neuer Funktionen die Verarbeitungslast:** Einige Funktionen sind verarbeitungsintensiver als andere. Je mehr Funktionen in einer Report Suite aktiviert sind, desto schwieriger ist es, die Latenz zu überwinden. Beachten Sie beim Aktivieren von Funktionen für eine Report Suite die folgenden Funktionen, die die zu verarbeitende Datenmenge erhöhen:

   * Implementieren von mehr als 20 Ereignissen auf derselben Seite
   * Komplexe VISTA-Regeln
   * Mehr als 20 Werte in der Variablen „products“
   * Ereignis-Serialisierung

* Aktivieren Sie die IAB-Bot-Filterung: Durch die [Bot-Filterung](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-removal.md) können Latenzzeiten deutlich reduziert werden, wenn Ihre Report Suite häufig von Bots oder Crawlern besucht wird. Verwenden Sie die IAB-Botliste, da diese vom [Interactive Advertising Bureau](https://www.iab.net/about_the_iab) aktualisiert und gewartet wird. Anwender können in Ergänzung zu den IAB-Regeln eigene Bot-Regeln erstellen.

## Verfahren bei Latenzzeit

Wenn Latenzen auftreten, stellen Sie sicher, dass Adobe die Verarbeitungs-Pipeline proaktiv überwacht und alles unternimmt, um die Verarbeitungszeit so schnell wie möglich wieder auf den Normalzustand zurückzusetzen. Viele Latenzprobleme können innerhalb von Stunden behoben werden. Wenn Sie mit einer bestimmten Report Suite befasst sind, kann sich einer der unterstützten Benutzer Ihrer Organisation an die Kundenunterstützung wenden und die Report Suite-ID erhalten, die Latenz aufweist. Der Adobe-Support-Mitarbeiter kann die Latenz überprüfen und Sie informieren, wenn sich das Problem verbessert und behoben ist.
