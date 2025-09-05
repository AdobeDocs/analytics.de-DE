---
description: Erhalten Sie Antworten auf häufig gestellte Fragen zu Daten-Feeds in Adobe Analytics.
keywords: Daten-Feed;Auftrag;vor Spalte;nach Spalte;Groß-/Kleinschreibung
title: Häufig gestellte Fragen zu Daten-Feeds
feature: Data Feeds
exl-id: 1bbf62d5-1c6e-4087-9ed9-8f760cad5420
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '1462'
ht-degree: 84%

---

# Häufig gestellte Fragen zu Daten-Feeds

Häufig gestellte Fragen zu Daten-Feeds.

## Müssen Feed-Namen eindeutig sein? {#unique}

Adobe Analytics verhindert nicht das Überschreiben von Daten-Feed-Dateien.

Um zu verhindern, dass Daten-Feed-Dateien überschrieben werden, empfehlen wir, dass alle Daten-Feed-Dateien, die an denselben Speicherort gesendet werden, eindeutige Dateinamen haben.

Daten-Feed-Dateinamen bestehen aus den folgenden Daten-Feed-Merkmalen:

* Report Suite-ID (RSID)

* Exportdatum

Zwei Feeds, die für dieselbe RSID und dasselbe Datum konfiguriert sind, haben denselben Dateinamen. Wenn diese Feeds an denselben Speicherort bereitgestellt werden, überschreibt eine Datei die andere.

Um das Überschreiben einer Datei zu verhindern, sollten Sie die folgenden Problemumgehungen in Betracht ziehen:

* Bereitstellungspfad ändern
* Termine ändern, falls möglich
* Report Suite ändern, falls möglich

## Wann werden die Daten verarbeitet? {#processed}

Bevor stündliche oder tägliche Daten verarbeitet werden, warten die Daten-Feeds, bis alle Treffer, die innerhalb des Zeitrahmens (Tag oder Stunde) in die Datenerfassung eingehen, in Data Warehouse geschrieben wurden. Anschließend erfassen die Daten-Feeds die Daten mit Zeitstempeln, die in diesen Zeitrahmen fallen, komprimieren die Daten und senden sie per FTP. Bei stündlichen Feeds werden die Daten normalerweise innerhalb von 15 bis 30 Minuten nach Ablauf der entsprechenden Stunde aus dem Data Warehouse geschrieben, es gibt jedoch keinen festgelegten Zeitraum. Wenn es keine Daten mit Zeitstempeln gibt, die in diesen Zeitrahmen passen, erfolgt der Prozess im nächsten Zeitrahmen erneut. Der aktuelle Daten-Feed-Prozess nutzt das Feld `date_time`, um zu ermitteln, welche Treffer zur entsprechenden Stunde gehören. Dieses Feld basiert auf der Zeitzone der Report Suite.

## Was ist der Unterschied zwischen Spalten mit `post_`-Präfix und Spalten ohne `post_`-Präfix? {#post}

Spalten ohne `post_`-Präfix enthalten Daten exakt so, wie sie an die Datenerfassung gesendet wurden. Spalten mit `post_`-Präfix enthalten den Wert nach der Verarbeitung. Beispiele, die einen Wert ändern können, sind Variablenpersistenz, Verarbeitungsregeln, VISTA-Regeln, Währungsumrechnung oder andere serverseitige Logik, die Adobe anwendet. Adobe empfiehlt, nach Möglichkeit die `post_`-Version einer Spalte zu verwenden.

Wenn für eine Spalte keine `post_`-Version vorliegt (z. B. bei `visit_num`), kann die Spalte als Post-Spalte betrachtet werden.

## Wie gehen Daten-Feeds mit Groß-/Kleinschreibung um? {#case}

In Adobe Analytics wird bei den meisten Variablen beim Reporting nicht zwischen Groß- und Kleinschreibung unterschieden. Beispielsweise werden „schnee“, „Schnee“, „SCHNEE“ und „sChnee“ alle als gleicher Wert betrachtet. Die Groß-/Kleinschreibung wird in Daten-Feeds beibehalten.

Wenn Sie unterschiedliche Schreibweisen desselben Werts zwischen Nicht-Post- und Post-Spalten sehen (z. B. „schnee“ in der Pre-Spalte und „Schnee“ in der Post-Spalte), verwendet Ihre Implementierung auf Ihrer Site sowohl Groß- als auch Kleinbuchstaben. Die Variante in der Post-Spalte wurde entweder zuvor eingereicht und ist in einem virtuellen Cookie gespeichert, oder sie wurde etwa zur selben Zeit für diese Report Suite verarbeitet.

## Enthalten Daten-Feeds Bots, die nach Admin Console-Bot-Regeln gefiltert wurden? {#bots}

Daten-Feeds enthalten keine Bots, die nach [Admin Console-Bot-Regeln](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-removal.md) gefiltert wurden.

## Warum werden in der Daten-Feed-Spalte `event_list` oder `post_event_list` mehrere `000`-Werte angezeigt? {#values}

Einige Tabellenkalkulationsprogramme, insbesondere Microsoft Excel, runden große Zahlen automatisch. Die Spalte `event_list` enthält viele kommagetrennte Zahlen, was manchmal dazu führt, dass Excel sie als eine große Zahl behandelt. Die letzten Ziffern werden auf `000` gerundet.

Adobe empfiehlt deswegen, `hit_data.tsv`-Dateien nicht automatisch in Microsoft Excel zu öffnen. Verwenden Sie stattdessen das Excel-Dialogfeld „Daten importieren“ und stellen Sie sicher, dass alle Felder als Text behandelt werden.

## Sind Spalten wie `hitid_high`, `hitid_low`, `visid_high` und `visid_low` garantiert eindeutig für den Treffer oder Besuch? {#hitid}

In fast allen Fällen kennzeichnet die Verkettung von `hitid_high` und `hitid_low` einen Treffer eindeutig. Dasselbe Konzept gilt für die Verkettung von `visid_high` und `visid_low` für Besuche. Verarbeitungsanomalien können jedoch in seltenen Fällen dazu führen, dass zwei Treffer dieselbe Treffer-ID teilen. Adobe empfiehlt, keine Daten-Feed-Workflows zu erstellen, da diese unflexibel darauf angewiesen sind, dass jeder Treffer eindeutig ist.

## Warum fehlen bei einigen Betreibern Informationen in der Spalte „Domain“? {#domain}

Einige Mobilnetzbetreiber (wie T-Mobile und O1) bieten keine Domänen mehr für Reverse-DNS-Lookups an. Daher sind die Daten nicht für die Domänenberichterstellung verfügbar.

## Warum kann ich aus Daten, die älter als sieben Tage sind, keine „Stündlich“-Dateien extrahieren? {#hourly}

Bei Daten, die älter als sieben Tage sind, werden die „Stündlich“-Dateien eines Tages zu einer einzigen „Täglich“-Datei zusammengefasst.

Beispiel: Am 9. März 2021 wird ein neuer Daten-Feed erstellt. Die Daten vom 1. Januar 2021 bis zum 9. März werden als „Stündlich“ bereitgestellt. Die „Stündlich“-Dateien, die vor dem 2. März 2021 vorlagen, werden jedoch in einer einzigen „Täglich“-Datei zusammengefasst. Sie können „Stündlich“-Dateien nur aus Daten extrahieren, die weniger als sieben Tage ab Erstellungsdatum alt sind. In diesem Fall vom 2. März bis 9. März.

## Welche Auswirkungen hat die Sommerzeit auf stündliche Daten-Feeds? {#dst}

Für einige Zeitzonen ändert sich zweimal jährlich die Uhrzeit aufgrund der Sommerzeitdefinition. Die Daten-Feeds berücksichtigen die Zeitzone, für die die Report Suite konfiguriert ist. Wenn in der für die Report Suite gewählten Zeitzone keine Sommerzeit berücksichtigt wird, erfolgt die Dateibereitstellung ganz normal wie an jedem anderen Tag. Wenn in der für die Report Suite gewählten Zeitzone jedoch die Sommerzeit berücksichtigt wird, ändert sich die Dateibereitstellung für die Stunde, in der die Zeitumstellung erfolgt (in der Regel um 2 :00 Uhr morgens).

Bei der Umstellung von Normalzeit auf Sommerzeit (im Frühling) erhält der Kunde nur 23 Dateien. Die Stunde, die bei der Zeitumstellung übersprungen wird, entfällt. Wenn die Umstellung beispielsweise um 2 Uhr morgens erfolgt, erhalten sie eine Datei für die :00 Stunde und eine Datei für die 3:00 Stunde. Es gibt keine 2:00-Datei, da sie bei 2:00 STD zu 3:00 DST wird.

Bei der Umstellung von Sommerzeit auf Normalzeit (im Herbst) erhält der Kunde 24 Dateien. Die Stunde der Zeitumstellung enthält dabei Daten für insgesamt zwei Stunden. Wenn die Umstellung beispielsweise um 2:00 :00 erfolgt, wird die Datei für 1::00 um eine Stunde verzögert, sie enthält jedoch Daten für zwei Stunden. Es enthält Daten von 1:00 DST bis 2:00 STD (was 3:00 DST gewesen wäre). Die nächste Datei beginnt um 2:00 STD.

## Wie behandelt Analytics FTP-Übertragungsfehler? {#ftp-failure}

Wenn eine FTP-Übertragung fehlschlägt (aufgrund einer verweigerten Anmeldung, verlorenen Verbindung, eines Nicht-Kontingent-Fehlers oder eines anderen Problems), versucht Adobe automatisch bis zu dreimal separat, eine Verbindung herzustellen und die Daten zu senden. Sollten die Fehler weiterhin bestehen, wird der Feed als fehlgeschlagen markiert und es wird eine E-Mail-Benachrichtigung gesendet.

Wenn eine Übertragung fehlschlägt, können Sie einen Auftrag erneut ausführen, bis er erfolgreich ist.

Wenn Sie Probleme haben, einen Daten-Feed auf Ihrer FTP-Site anzuzeigen, finden Sie weitere Informationen unter [Fehlerbehebung bei Daten-Feeds](troubleshooting.md).

## Wie sende ich einen Vorgang erneut? {#resend}

Nachdem Sie das Bereitstellungsproblem überprüft/korrigiert haben, führen Sie den Vorgang erneut aus, um die Dateien abzurufen.

## Was ist die BucketOwnerFullControl-Einstellung für Amazon S3-Daten-Feeds? {#BucketOwnerFullControl}

**BucketOwnerFullControl** beinhaltet kontenübergreifende Berechtigungen zum Erstellen von Objekten in anderen Buckets.

Bei einer üblichen Verwendung von Amazon S3 erstellt der Kontoinhaber eines Amazon Web Services (AWS)-Kontos zunächst einen Bucket. Dann erstellt er einen Benutzer, der dazu berechtigt ist, Objekte in diesem Bucket zu erstellen. Schließlich stellt der Kontoinhaber die Anmeldeinformationen für diesen Benutzer zur Verfügung. In diesem Fall gehören die Objekte eines Benutzers zum selben Konto und der Kontoinhaber hat implizit die vollständige Kontrolle über das Objekt (Lesen, Löschen usw.). Dieser Prozess entspricht der Funktionsweise der FTP-Bereitstellung.

Mit AWS kann ein Benutzer aber auch Objekte in einem Bucket erstellen, die einem anderen Benutzerkonto zugeordnet sind. Beispiel: Zwei AWS-Benutzer, Benutzer A und Benutzer B, verfügen über kein gemeinsames AWS-Konto, möchten aber in anderen Buckets Objekte erstellen. Erstellt Benutzer A einen Bucket namens „Bucket A“, so kann Benutzer A eine Bucket-Richtlinie festlegen, die Benutzer B explizit erlaubt, in Bucket A Objekte zu erstellen, auch wenn der Bucket nicht Benutzer B gehört. Diese Richtlinie kann vorteilhaft sein, da es nicht notwendig ist, dass Benutzer A und Benutzer B Anmeldeinformationen austauschen. Stattdessen stellt Benutzer B Benutzer A die Nummer seines Benutzerkontos zur Verfügung und Benutzer A erstellt eine Bucket-Richtlinie, die im Wesentlichen aussagt, dass „Benutzer B Objekte in Bucket A erstellen darf“.

Objekte erben jedoch keine Berechtigungen vom übergeordneten Bucket. Lädt Benutzer B ein Objekt in den Bucket von Benutzer A hoch, „gehört“ das Objekt immer noch Benutzer B und Benutzer A hat standardmäßig keine Berechtigungen bezüglich des Objekts, auch wenn der Bucket Benutzer A gehört. Benutzer B muss Benutzer A explizit Berechtigungen einräumen, da Benutzer B immer noch der Eigentümer des Objekts ist. Um diese Berechtigung zu erteilen, muss Benutzer B das Objekt mit einer BucketOwnerFullControl-ACL hochladen, die angibt, dass dem Bucket-Inhaber (Benutzer A) vollständige Berechtigungen für das Objekt (Lesen, Schreiben, Löschen usw.) gewährt werden, auch wenn das Objekt Benutzer B „gehört“.

>[!NOTE]
>
>Adobe Analytics ermittelt nicht, ob für den Bucket eine Richtlinie gilt, die dem Bucket-Besitzer die volle Kontrolle über neue Objekte gibt, oder ob der Bucket-Besitzer ein anderes Konto hat als der Benutzer, der die Daten schreibt. Stattdessen fügt Analytics bei jedem Feed-Upload automatisch den Eigentümer des Buckets zur `BucketOwnerFullControl`-ACL hinzu.

