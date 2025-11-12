---
description: Erfahren Sie, wie Sie den Report Builder-Versand optimieren können, und lernen Sie eine Liste der Fehlermeldungen kennen, die auftreten können.
title: Fehlerbehebung und Best Practices für Report Builder
uuid: 36a08143-dc78-40f5-9ce9-7d16980aa27b
feature: Report Builder
role: User, Admin
exl-id: 41a640ce-2316-439b-b3ba-f0bace9af268
source-git-commit: ca84a5f807545d7196e2e0e90d3209c32d3fd789
workflow-type: tm+mt
source-wordcount: '1424'
ht-degree: 61%

---

# Fehlerbehebung und Best Practices für Report Builder

{{legacy-arb}}

In diesem Artikel werden die Fehlerbehebung und Best Practices beschrieben, mit denen Sie Report Builder optimieren können. Sie enthält auch eine Liste von Fehlermeldungen, die möglicherweise angezeigt werden.

## Benutzer von Report Builder 5.0 und Öffnen von 5.1-Arbeitsmappen {#section_C29898775999453FABB5FB0E098415C8}

Adobe hat das Trennzeichen zwischen Dimensionen und Klassifizierungen von einem Unterstrich (_) in Folgendes geändert || Diese Änderung wirkt sich auf die Kompatibilität für Benutzer von Report Builder Version 5.0 aus, die eine Report Builder 5.1-Arbeitsmappe mit Classification-Anforderungen öffnen. Jedes Mal, wenn eine Arbeitsmappe mit einer älteren Version als v5.1 geöffnet wird, werden alle serialisierten Klassifizierungsanfragen in dieses Format konvertiert.

Dies bringt ein Kompatibilitätsproblem beim Weiterleiten mit sich: Sobald eine Arbeitsmappe, die in Version 5.1 konvertiert wurde, an einen Benutzer mit Report Builder Version 5.0 weitergegeben wird, kann dieser Benutzer die Classification-Anforderung nicht mehr erkennen (es wird nach „_“ gesucht, aber Version 5.1 hat „||“ serialisiert).

Außerdem bewirkt das Öffnen einer ARB Version 5.1-Arbeitsmappe mit Classification-Anforderung Folgendes:

* Wenn Sie die Arbeitsmappe öffnen, erhalten Sie folgende Warnmeldung: „Diese Arbeitsmappe wurde zuletzt mit Report Builder Version 5.1 gespeichert. Diese Version hat einige Funktionen eingefügt, die mit der Report Builder-Version, die auf diesem Computer installiert ist, nicht kompatibel sind. Es wird dringend empfohlen, ein Upgrade auf die neueste Version von Report Builder durchzuführen, bevor diese Arbeitsmappe aktualisiert wird.“
* Wenn Sie einen Rechtsklick auf eine ARB-Anfrage mit Classification ausführen, werden die Report Builder-Kontextmenüs („Anforderung bearbeiten“, „Abhängige Anforderung hinzufügen“ ...) nicht angezeigt.
* Wenn Sie eine Aktualisierung für alle durchführen, indem Sie auf die dritte Schaltfläche klicken oder indem Sie eine Gruppe von Anfragen aus dem Anforderungs-Manager -Formular aktualisieren, wird die Klassifizierungsanfrage ohne Fehler ausgeführt. Die Classifications-Werte werden jedoch nicht ausgeschrieben.
* Sie können die Anfrage dennoch bearbeiten, indem Sie den Anforderungs-Manager öffnen und dann von Zeile zu Zeile wechseln, bis die richtige Anfrage erreicht ist.
* Wenn Sie die Anfrage bearbeiten, alle Parameter unverändert lassen und dann auf Beenden klicken, wird die Antwort ordnungsgemäß geschrieben. Durch die Bearbeitung der Anfrage wird das Problem behoben, da die Antwort-Layout-Parameter erneut serialisiert werden. Es gibt also eine Problemumgehung, obwohl sie zeitaufwendig ist.

## Authentifizierungsprobleme in Report Builder {#section_FD79104DF1414FE2B36591606C963DE6}

Zur Erstellung von Datenanforderungen aus Report Suites durch Report Builder ist eine Authentifizierung erforderlich. Manchmal gibt es Probleme bei der Anmeldung bei Report Builder, abhängig von Ihren Einstellungen in [!DNL Analytics] oder Ihrem Netzwerk.

* **Ungültige Unternehmensanmeldung** Dieser Fehler tritt am häufigsten auf, wenn die Unternehmensanmeldung nicht korrekt eingegeben wurde oder Probleme mit der Netzwerkaktivität auftreten. Gehen Sie folgendermaßen vor:
   * Überprüfen Sie die Schreibweise des Anmeldeunternehmens, um sicherzustellen, dass weder ein Tippfehler noch ein fehlerhaftes Leerzeichen auftritt.
   * Melden Sie sich mit demselben Firmennamen bei Analytics an, um sicherzustellen, dass die Angaben korrekt sind. Wenn Sie sich mit diesen Benutzerdaten nicht anmelden können, wenden Sie sich an einen Administrator in Ihrem Unternehmen und fordern Sie die korrekten Daten an.
* **Firewall**: Report Builder verwendet die Ports 80 und 443. Stellen Sie sicher, dass diese Ports über die Firewall Ihres Unternehmens zugelassen sind. Siehe auch Interne IP-Adressen von Adobe für zusätzliche Firewall-Ausschlüsse.

## Empfehlungen für die Anforderungsoptimierung {#section_33EF919255BF46CD97105D8ACB43573F}

Durch die folgenden Faktoren kann die Anfragekomplexität erhöht und damit die Verarbeitungsgeschwindigkeit verringert werden.

* **Faktoren, die die Bereitstellung verlangsamen können**: Es wurden zu viele Lesezeichen, Dashboards und Report Builder-Arbeitsmappen innerhalb weniger Stunden geplant. Es wurden möglicherweise zu viele Report Builder-Arbeitsmappen um die gleiche Uhrzeit herum geplant. In diesem Fall tritt in der Berichts-API-Warteschlange ein Rückstand ein.
* **Faktoren, die die Arbeitsmappen-Laufzeit verlangsamen können**: Signifikante Zunahme der Klassifizierungen oder Vergrößerung des Anfragedatumsbereichs im Laufe der Zeit.
* **Ursachen, die zum Scheitern der Bereitstellung von Arbeitsmappen führen**: Komplexe Excel-Formeln in einer Arbeitsmappe, insbesondere solche mit Datum und Uhrzeit.
* **Zellen, die 0 (keine Werte) zurückgeben**: Wenn im Namen des Excel-Arbeitsblatts ein Apostroph oder ein einfaches Anführungszeichen enthalten ist, gibt Report Builder keine Werte zurück. (Dies ist eine Microsoft Excel-Einschränkung.)
* **Individuelle Anfrageleistung**: Die Verarbeitungsgeschwindigkeit kann durch die folgenden Einstellungen beeinflusst werden:

  | Einstellung | Schnellere Leistung | Langsamere Leistung |
  |--- |--- |--- |
  | Aufschlüsselungen und Aufschlüsselungsreihenfolge | wenige | Viele |
  |  | Beispiel: Bei einer Aufteilung von A bis Z sollte die Anzahl der Elemente für A immer niedriger sein als die Anzahl der Elemente für Z. Andernfalls kann sich die Anforderungszeit deutlich erhöhen. |  |
  | Datumsbereich | Kleiner Bereich | Weit reichender Bereich |
  | Filtern | Spezifische Filter | Bevorzugte Filter |
  | Granularität | Aggregiert | Stündlich<ul><li>Täglich</li><li>Wöchentlich</li><li>Monatlich</li><li>Quartalsweise</li><li>Jährlich</li></ul> |
  | Anzahl der Einträge | Kleiner Datensatz | Großer Datensatz |

* **Zeitplanung**: Staffeln Sie die Zeitplanung über einen Zeitraum von 24 Stunden (siehe Tabelle unten). Durch vorhandene Lesezeichen, Dashboards und Report Builder-Arbeitsmappen, die zeitlich kurz aufeinander folgen, können Verzögerungen verursacht werden. Planen Sie größere, komplexere Anfragen am frühen Morgen, damit manuelle Pull- und Aktualisierungsvorgänge während des Geschäftstages möglich sind.

  | Geplanter Zeitpunkt | 1:00 bis 2:00 Uhr | 02:00 - 07:00 Uhr | 7:00 - 18:00 Uhr | 18:00 bis Mitternacht |
  |--- |--- |--- |--- |--- |
  | Report Builder – Nutzung | beruhigen | Sehr beschäftigt | Client-seitige Verwendung.<br>Höhere Anzahl an Nutzern, die eine lokale Aktualisierung vornehmen und ein „Sofortiges Senden“ anfordern.<br>Überprüfen Sie außerdem, ob die API-Warteschlange gelöscht wird, wenn bei geplanten Arbeitsmappen ein Timeout auftritt. | Nicht beschäftigt |

* **Zeitüberschreitungen**: Alle terminierten Berichte werden nach vier Stunden beendet. Das System versucht, eine Planung noch dreimal durchzuführen, was möglicherweise zu einem Fehler führt. (Im Allgemeinen gilt: Je größer der Datensatz, desto länger dauert seine Ausführung.) Diese sind in [!DNL Analytics] Reporting und Report Builder zu sehen:

## Beispiele für Fehlermeldungen {#section_3DF3A1EEDAD149CB941BEABEF948A4A5}

Dieser Abschnitt enthält eine Beispielliste von Fehlermeldungen, die bei der Verwendung von Report Builder auftreten können.

>[!NOTE]
>
>Dies ist ein Beispiel für Fehlermeldungen und keine erschöpfende Liste. Weitere Informationen zur Behebung von Fehlern erhalten Sie von Ihrem Administrator.

* **Diese Funktion kann nur auf eine geöffnete Arbeitsmappe angewendet werden.**: Wenn in Excel keine Arbeitsmappen (Kalkulationstabellen) geöffnet sind und Sie auf eines der Symbole der Report Builder-Symbolleiste klicken, wird diese Meldung angezeigt. Darüber hinaus wird die Symbolleiste deaktiviert, bis Sie eine Arbeitsmappe öffnen. Sie können jedoch auf das Online-Hilfesymbol klicken, während die Symbolleiste noch aktiviert ist, ohne diesen Fehler zu verursachen.
* **Sie müssen zunächst den [!UICONTROL Anforderungs-Assistenten] beenden, bevor Sie den [!UICONTROL Anforderungs-Manager aktivieren].**: Der [!UICONTROL Anforderungs-Assistent] und der [!UICONTROL Anforderungs-Manager] sind zwar funktional verbunden, aber es ist nicht möglich, den [!UICONTROL Anforderungs-Manager] zu verwenden, bevor Sie eine im [!UICONTROL Anforderungs-Assistenten] begonnene Arbeit abgebrochen oder abgeschlossen haben.
* **Mit diesem Bereich ist keine Anforderung verbunden.**: Diese Fehlermeldung wird angezeigt, wenn Sie im [!UICONTROL Anforderungs-Manager] auf die Schaltfläche [!UICONTROL Aus Blatt] klicken, aber die entsprechende Zelle im Arbeitsblatt keine Anforderungen enthält. Um zu ermitteln, welche Zellen im Arbeitsblatt Anforderungen enthalten, klicken Sie auf die einzelnen Anforderungen, die in der Tabelle im [!UICONTROL Anforderungs-Manager“ aufgeführt &#x200B;]. Wenn eine Anforderung mit Zellen verknüpft ist, werden die Zellen bei Auswahl der Anforderung in der Liste markiert dargestellt.
* **Der ausgewählte Bereich ist ungültig. Wählen Sie einen anderen Bereich aus.**: Diese Fehlermeldung wird angezeigt, wenn eine Zelle des Arbeitsblatts ausgewählt wird, der bereits eine Anforderung zugeordnet ist. Löschen Sie entweder die der Zelle zugeordnete Anforderung oder wählen Sie einen anderen Zellenbereich für die Verknüpfung aus. Wenn Sie Zellen löschen möchten, müssen Sie unbedingt Zellen vorher ermitteln, welche Zellen Anforderungen enthalten und die Anforderung löschen, bevor Sie die Zellen löschen (indem Sie Zeilen oder Spalten entfernen).
* **Verlassen Sie die Excel-Zelle, während diese ausgewählt ist, um diese Funktion zu verwenden.**: Wenn Sie sich im *Bearbeitungsmodus* in einer Excel-Zelle befinden und auf eines der Report Builder-Symbole klicken, wird diese Fehlermeldung angezeigt. Unter Bearbeitungsmodus für eine Excel-Zelle ist zu verstehen, dass die Zelle ausgewählt ist und der Cursor sich in der Zelle befindet. Sie befinden sich auch im Bearbeitungsmodus in einer Excel-Zelle, wenn Sie direkt in die Leiste [!UICONTROL Formel] oder in das Feld [!UICONTROL Name] oben in Excel eingeben.
* **Der ausgewählte Bereich überschneidet sich mit dem Bereich einer anderen Anforderung. Ändern Sie Ihre Auswahl.**: Wenn Sie bereits eine Gruppe von Zellen mit dem Arbeitsblatt verknüpft haben, wird diese Fehlermeldung angezeigt.
* **Reparaturen an Arbeitsmappen (entfernte Einträge: Formel aus dem Teil /xl/calcChain.xml)**: Manchmal werden die Formeln einer Arbeitsmappe beim Speichern oder Übertragen beschädigt. Wenn die Datei geöffnet wird, versucht Excel diese Formeln auszuführen und schlägt damit fehl. Sie können dieses Problem beheben, indem Sie `calcChain.xml` aus der Tabelle entfernen, was Excel zwingt, die Formelberechnungen zu aktualisieren.
   1. Benennen Sie die Dateierweiterung der Arbeitsmappe von `.xlsx` in `.zip` um.
   2. Dekomprimieren Sie dann den Inhalt und öffnen Sie den Ordner `/xl/`.
   3. Löschen `calcChain.xml`.
   4. Komprimieren Sie den Inhalt erneut und ändern Sie die Dateierweiterung wieder zurück in `.xlsx`.
   5. Öffnen Sie die Arbeitsmappe in Excel und aktualisieren Sie alle Report Builder-Anfragen.
* **Excel-Zellen, die mit den Eingangsfiltern oder dem Ausgangsbereich verbunden sind, wurden möglicherweise gelöscht**: Report Builder verwendet Excel-Namen, um Datenanforderungen an Zellen anzuhängen. Wenn Sie Excel-Namen aus Names Manager löschen, kann dieser Fehler auftreten. Anfragen können nicht wiederhergestellt werden, wenn Excel-Namen gelöscht werden. Wenn die Arbeitsmappe eingeplant war, können Sie entweder eine Kopie vom Zeitplan-Manager herunterladen oder zuvor bereitgestellte Kopien der Arbeitsmappe öffnen.
