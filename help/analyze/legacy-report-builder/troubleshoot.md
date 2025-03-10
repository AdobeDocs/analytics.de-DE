---
description: Erfahren Sie, wie Sie den Versand von Report Buildern optimieren können, und lernen Sie eine Liste von Fehlermeldungen kennen, die möglicherweise auftreten können.
title: Fehlerbehebung und Best Practices für Report Builder
uuid: 36a08143-dc78-40f5-9ce9-7d16980aa27b
feature: Report Builder
role: User, Admin
exl-id: 41a640ce-2316-439b-b3ba-f0bace9af268
source-git-commit: fcecc8a493852f5682fd7fbd5b9bb484a850922c
workflow-type: tm+mt
source-wordcount: '1424'
ht-degree: 84%

---

# Fehlerbehebung und Best Practices für Report Builder

{{legacy-arb}}

In diesem Artikel werden die Fehlerbehebung und Best Practices beschrieben, mit denen Sie Report Builder optimieren können. Sie enthält auch eine Liste von Fehlermeldungen, die möglicherweise angezeigt werden.

## Benutzer von Report Builder 5.0 und Öffnen von 5.1-Arbeitsmappen {#section_C29898775999453FABB5FB0E098415C8}

Adobe hat das Trennzeichen zwischen Dimensionen und Classifications von einem Unterstrich (_) in || geändert. Diese Änderung wirkt sich auf die Kompatibilität für Benutzer von Report Builder Version 5.0 aus, die eine Report Builder 5.1-Arbeitsmappe mit Classification-Anforderungen öffnen. Sobald eine Arbeitsmappe, die mit Version 5.1 oder älter erstellt wurde, geöffnet wird, werden alle serialisierten Classification-Anforderungen in dieses Format umgewandelt.

Dies bringt ein Kompatibilitätsproblem beim Weiterleiten mit sich: Sobald eine Arbeitsmappe, die in Version 5.1 konvertiert wurde, an einen Benutzer mit Report Builder Version 5.0 weitergegeben wird, kann dieser Benutzer die Classification-Anforderung nicht mehr erkennen (es wird nach „_“ gesucht, aber Version 5.1 hat „||“ serialisiert).

Außerdem bewirkt das Öffnen einer ARB Version 5.1-Arbeitsmappe mit Classification-Anforderung Folgendes:

* Wenn Sie die Arbeitsmappe öffnen, erhalten Sie folgende Warnmeldung: „Diese Arbeitsmappe wurde zuletzt mit Report Builder Version 5.1 gespeichert. Diese Version hat einige Funktionen eingefügt, die mit der Report Builder-Version, die auf diesem Computer installiert ist, nicht kompatibel sind. Es wird dringend empfohlen, ein Upgrade auf die neueste Version von Report Builder durchzuführen, bevor diese Arbeitsmappe aktualisiert wird.“
* Wenn Sie einen Rechtsklick auf eine ARB-Anfrage mit Classification ausführen, werden die Report Builder-Kontextmenüs („Anforderung bearbeiten“, „Abhängige Anforderung hinzufügen“ ...) nicht angezeigt.
* Wenn Sie die Option „Alle aktualisieren“ ausführen, indem Sie auf die dritte Schaltfläche klicken oder indem Sie einen Satz Anforderungen aus dem Anforderungs-Manager aktualisieren, wird die Classification-Anforderung ohne Fehler ausgeführt. Die Classification-Werte werden jedoch nicht ausgeschrieben.
* Sie können die Anforderung weiterhin bearbeiten, indem Sie den Anforderungs-Manager öffnen und dann von Zeile zu Zeile navigieren, bis Sie bei der richtigen Anforderung angelangt sind.
* Wenn Sie die Anforderung bearbeiten, alle Parameter beibehalten und dann auf „Abschließen“ klicken, wird die Antwort ordnungsgemäß ausgeschrieben. Das Bearbeiten der Anforderung löst also das Problem, da die Antwortlayoutparameter neu serialisiert werden. Abhilfe ist also möglich, wenn auch zeitaufwendig.

## Authentifizierungsprobleme in Report Builder {#section_FD79104DF1414FE2B36591606C963DE6}

Zur Erstellung von Datenanforderungen aus Report Suites durch Report Builder ist eine Authentifizierung erforderlich. Manchmal gibt es Probleme bei der Anmeldung beim Report Builder, abhängig von Ihren Einstellungen in [!DNL Analytics] oder Ihrem Netzwerk.

* **Ungültige Unternehmensanmeldung** Dieser Fehler tritt am häufigsten auf, wenn die Unternehmensanmeldung nicht korrekt eingegeben wurde oder Probleme mit der Netzwerkaktivität auftreten. Gehen Sie folgendermaßen vor:
   * Überprüfen Sie Ihre Eingabe auf Tippfehler oder überflüssige Leerzeichen.
   * Melden Sie sich mit demselben Firmennamen bei Analytics an, um sicherzustellen, dass die Angaben korrekt sind. Wenn Sie sich mit diesen Benutzerdaten nicht anmelden können, wenden Sie sich an einen Administrator in Ihrem Unternehmen und fordern Sie die korrekten Daten an.
* **Firewall**: Der Report Builder verwendet die Ports 80 und 443. Stellen Sie sicher, dass diese Ports von der Firewall in Ihrem Unternehmen freigegeben sind. Überprüfen Sie auch die interne IP-Adresse von Adobe auf weitere Firewall-Ausnahmen.

## Empfehlungen für die Anforderungsoptimierung {#section_33EF919255BF46CD97105D8ACB43573F}

Durch die folgenden Faktoren kann die Anfragekomplexität erhöht und damit die Verarbeitungsgeschwindigkeit verringert werden.

* **Faktoren, die die Bereitstellung verlangsamen können**: Es wurden zu viele Lesezeichen, Dashboards und Report Builder-Arbeitsmappen innerhalb weniger Stunden geplant. Es wurden möglicherweise zu viele Report Builder-Arbeitsmappen um die gleiche Uhrzeit herum geplant. In diesem Fall tritt in der Berichts-API-Warteschlange ein Rückstand ein.
* **Faktoren, die die Arbeitsmappen-Laufzeit verlangsamen können**: Signifikante Zunahme der Klassifizierungen oder Vergrößerung des Anfragedatumsbereichs im Laufe der Zeit.
* **Ursachen, die zum Scheitern der Bereitstellung von Arbeitsmappen führen**: Komplexe Excel-Formeln in einer Arbeitsmappe, insbesondere solche mit Datum und Uhrzeit.
* **Zellen, die 0 (keine Werte) zurückgeben**: Ein Apostroph oder ein einfaches Anführungszeichen im Namen des Excel-Arbeitsblatts führt dazu, dass der Report Builder keine Werte zurückgibt. (Dies ist eine Microsoft Excel-Einschränkung.)
* **Individuelle Anfrageleistung**: Die Verarbeitungsgeschwindigkeit kann durch die folgenden Einstellungen beeinflusst werden:

  | Einstellung | Schnellere Leistung | Langsamere Leistung |
  |--- |--- |--- |
  | Aufschlüsselung und Aufschlüsselungsreihenfolge | Wenig | Viele |
  |  | Beispiel: Bei einer Aufteilung von A bis Z sollte die Anzahl der Elemente für A immer niedriger sein als die Anzahl der Elemente für Z. Andernfalls kann sich die Anforderungszeit deutlich erhöhen. |
  | Datumsbereich | Kleiner Bereich | Großer Bereich |
  | Filtern | Spezifische Filter | Bevorzugte Filter |
  | Granularität | Aggregiert | Stündlich<ul><li>Täglich</li><li>Wöchentlich</li><li>Monatlich</li><li>Quartalsweise</li><li>Jährlich</li></ul> |
  | Anzahl der Einträge | Kleiner Datensatz | Großer Datensatz |

* **Zeitplanung**: Staffeln Sie die Zeitplanung über einen Zeitraum von 24 Stunden (siehe Tabelle unten). Durch vorhandene Lesezeichen, Dashboards und Report Builder-Arbeitsmappen, die zeitlich kurz aufeinander folgen, können Verzögerungen verursacht werden. Planen Sie größere, komplexere Anforderungen in den frühen Morgenstunden, um manuelle Abrufe und Aktualisierungen im Laufe des Arbeitstages zuzulassen.

  | Zeitplanung | 01:00 – 02:00 Uhr | 02:00 – 07:00 Uhr | 07:00 – 18:00 Uhr | 18:00 – 24:00 Uhr |
  |--- |--- |--- |--- |--- |
  | Report Builder – Nutzung | Ruhig | Hohe Auslastung | clientseitige Nutzung<br>Höhere Anzahl an Nutzern, die eine lokale Aktualisierung vornehmen und ein „Sofortiges Senden“ anfordern.<br>Überprüfen Sie außerdem, ob die API-Warteschlange gelöscht wird, wenn bei geplanten Arbeitsmappen ein Timeout auftritt. | Geringe Auslastung |

* **Zeitüberschreitungen**: Alle terminierten Berichte werden nach vier Stunden beendet. Das System versucht drei weitere Male eine Planung, die möglicherweise zu einem Fehler führen. (Im Allgemeinen gilt: Je größer der Datensatz, desto länger dauert seine Ausführung.) Diese sind in [!DNL Analytics] Reporting und Report Builder zu sehen:

## Beispiele für Fehlermeldungen {#section_3DF3A1EEDAD149CB941BEABEF948A4A5}

Dieser Abschnitt enthält eine Beispielliste von Fehlermeldungen, die bei der Verwendung von Report Builder auftreten können.

>[!NOTE]
>
>Dies ist ein Beispiel für Fehlermeldungen und keine erschöpfende Liste. Weitere Informationen zur Behebung von Fehlern erhalten Sie von Ihrem Administrator.

* **Diese Funktion kann nur auf eine geöffnete Arbeitsmappe angewendet werden.**: Wenn in Excel keine Arbeitsmappen (Kalkulationstabellen) geöffnet sind und Sie auf eines der Symbole in der Report Builder-Symbolleiste klicken, wird diese Meldung angezeigt. Darüber hinaus wird die Symbolleiste deaktiviert, bis Sie eine Arbeitsmappe öffnen. Sie können allerdings auf das Hilfesymbol klicken, solange die Symbolleiste noch aktiviert ist, ohne dass diese Fehlermeldung erfolgt.
* **Sie müssen zunächst den [!UICONTROL Anforderungs-Assistenten] beenden, bevor Sie den [!UICONTROL Anforderungs-Manager aktivieren].**: Der [!UICONTROL Anforderungs-Assistent] und der [!UICONTROL Anforderungs-Manager] sind zwar funktional verbunden, aber es ist nicht möglich, den [!UICONTROL Anforderungs-Manager] zu verwenden, bevor Sie eine im [!UICONTROL Anforderungs-Assistenten] begonnene Arbeit abgebrochen oder abgeschlossen haben.
* **Mit diesem Bereich ist keine Anforderung verbunden.**: Diese Fehlermeldung wird angezeigt, wenn Sie im [!UICONTROL Anforderungs-Manager] auf die Schaltfläche [!UICONTROL Aus Blatt] klicken, aber die entsprechende Zelle im Arbeitsblatt keine Anforderungen enthält. Um zu prüfen, welche Zellen des Arbeitsblatts Anforderungen enthalten, klicken Sie auf die einzelnen Anforderungen in der Liste im [!UICONTROL Anforderungs-Manager]. Wenn eine Anforderung mit Zellen verknüpft ist, werden die Zellen bei Auswahl der Anforderung in der Liste markiert dargestellt.
* **Der ausgewählte Bereich ist ungültig. Wählen Sie einen anderen Bereich aus.**: Diese Fehlermeldung wird angezeigt, wenn eine Zelle des Arbeitsblatts ausgewählt wird, der bereits eine Anforderung zugeordnet ist. Löschen Sie entweder die der Zelle zugeordnete Anforderung oder wählen Sie einen anderen Zellenbereich für die Verknüpfung aus. Wenn Sie Zellen löschen möchten, müssen Sie unbedingt Zellen vorher ermitteln, welche Zellen Anforderungen enthalten und die Anforderung löschen, bevor Sie die Zellen löschen (indem Sie Zeilen oder Spalten entfernen).
* **Verlassen Sie die Excel-Zelle, während diese ausgewählt ist, um diese Funktion zu verwenden.**: Wenn Sie sich im *Bearbeitungsmodus* in einer Excel-Zelle befinden und auf eines der Report Builder-Symbole klicken, wird diese Fehlermeldung angezeigt. Unter Bearbeitungsmodus für eine Excel-Zelle ist zu verstehen, dass die Zelle ausgewählt ist und der Cursor sich in der Zelle befindet. Sie befinden sich in Excel außerdem im Bearbeitungsmodus, wenn Sie Daten direkt in das [!UICONTROL Namensfeld] in der [!UICONTROL Formelleiste] eingeben.
* **Der ausgewählte Bereich überschneidet sich mit dem Bereich einer anderen Anforderung. Ändern Sie Ihre Auswahl.**: Wenn Sie bereits eine Gruppe von Zellen mit dem Arbeitsblatt verknüpft haben, wird diese Fehlermeldung angezeigt.
* **Reparaturen an Arbeitsmappen (entfernte Datensätze: Formel aus dem Teil /xl/calcChain.xml)**: Manchmal werden die Formeln einer Arbeitsmappe beim Speichern oder Übertragen beschädigt. Wenn die Datei geöffnet wird, versucht Excel diese Formeln auszuführen und schlägt damit fehl. Sie können dieses Problem beheben, indem Sie `calcChain.xml` aus der Tabelle entfernen, was Excel zwingt, die Formelberechnungen zu aktualisieren.
   1. Benennen Sie die Dateierweiterung der Arbeitsmappe von `.xlsx` in `.zip` um.
   2. Dekomprimieren Sie dann den Inhalt und öffnen Sie den Ordner `/xl/`.
   3. Löschen `calcChain.xml`.
   4. Komprimieren Sie den Inhalt erneut und ändern Sie die Dateierweiterung wieder zurück in `.xlsx`.
   5. Öffnen Sie die Arbeitsmappe in Excel und aktualisieren Sie alle Report Builder-Anfragen.
* **Excel-Zellen, die mit den Eingangsfiltern oder dem Ausgangsbereich verbunden sind, wurden möglicherweise gelöscht**: Report Builder verwendet Excel-Namen, um Datenanforderungen an Zellen anzuhängen. Wenn Sie Excel-Namen aus Names Manager löschen, kann dieser Fehler auftreten. Anfragen können nicht wiederhergestellt werden, wenn Excel-Namen gelöscht werden. Wenn die Arbeitsmappe eingeplant war, können Sie entweder eine Kopie vom Zeitplan-Manager herunterladen oder zuvor bereitgestellte Kopien der Arbeitsmappe öffnen.
