---
description: Adobe benötigt eine vorherige Ankündigung bei Einrichtung neuer Konten, Traffic-Spitzen und Traffic-Zunahmen. Hardware muss im Voraus zugewiesen werden, um die Latenz und mögliche negative Auswirkungen auf das Gesamtsystem zu minimieren.
title: Erforderliche Vorlaufzeit für Traffic-Zunahme
feature: Report Suite Settings
exl-id: fb428f8d-9dff-43a6-a1e8-1a892cbed7ac
TQID: 'https://experienceleague.adobe.com/NJpOBQXD9CulN-UjbKnQiPzPWusWzLEo0RgvBioJe3I'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
source-git-commit: 50f9ff18816ad88f231762b8b37c1ab9e1787b6f
workflow-type: tm+mt
source-wordcount: 328
ht-degree: 100%

---

# Erforderliche Vorlaufzeit für Traffic-Zunahme

Adobe benötigt eine vorherige Ankündigung bei Einrichtung neuer Konten, Traffic-Spitzen und Traffic-Zunahmen. Hardware muss im Voraus zugewiesen werden, um die Latenz und mögliche negative Auswirkungen auf das Gesamtsystem zu minimieren.

>[!IMPORTANT]
>
>Adobe kann keine Traffic-Änderungsanfragen für „Platzhalter“ berücksichtigen. Sofern nicht anders angegeben, halten Sie die vorgeschlagene Vorlaufzeit so gut wie möglich ein. Senden Sie wenn möglich auch keinen Warnhinweis zu früh.

Ermitteln Sie anhand der folgenden Richtlinien, wie weit im Voraus Sie einen Traffic-Warnhinweis übermitteln müssen:

## Vorlaufzeiten für Hardware-Zuweisung


<table id="table_A67CC3B164F740088797BD8913244E47">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Typ der Traffic-Änderung </th>
   <th colname="col2" class="entry"> Benötigte Vorlaufzeit </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> Neue Kontoeinrichtung </td>
   <td colname="col2"> <ul><li>3 Werktage</li></ul></td>
  </tr>
  <tr>
   <td colname="col1"> Traffic-Spitze oder plötzlicher permanenter Traffic-Anstieg von bis zu 25 % des durchschnittlichen täglichen Volumens im Vergleich zu den letzten 30 Tagen</td>
   <td colname="col2"> <ul><li>Report Suites mit &lt; 100 Mio. Treffern/Tag: Keine Benachrichtigung erforderlich</li><li>Report Suites mit &gt; 100 Mio Treffern/Tag: 5 Werktage</li></ul></td>
  </tr>
  <tr>
   <td colname="col1"> Traffic-Spitze oder plötzlicher permanenter Traffic-Anstieg von mehr als 25 % des durchschnittlichen täglichen Volumens im Vergleich zu den letzten 30 Tagen</td>
   <td colname="col2"> <ul><li>5 Werktage</li></ul></td>
  </tr>
  <tr>
   <td colname="col1"> Feiertagsereignisse Oktober – Dezember </td>
   <td colname="col2"> <ul><li>1 Kalendermonat</li></ul> </td>
  </tr>
 </tbody>
</table>

Was Sie außerdem noch beachten müssen:

* Wenn Sie mehrere Report Suites in Betrieb nehmen oder hinzufügen, die die oben angegebenen Zahlen erhöhen, gilt als Vorlaufzeit die Summe des für jede Report Suite erwarteten Traffics.
* Halten Sie die folgenden Informationen bereit, um eine Traffic-Änderung zu übermitteln:

   * Report Suite-ID
   * Geschätzte Treffer pro Tag
   * Tag der Live-Schaltung

* Client-Warnhinweise sind auch erforderlich, wenn der Traffic abnimmt oder eine Report Suite außer Betrieb genommen wird.

## Aufhebung der Hardware-Zuordnung aufgrund von nicht realisiertem Traffic

Die Hardware-Zuordnungen bei neuen Konten, Traffic-Spitzen und Traffic-Zunahmen werden aufgehoben, wenn sich die Traffic-Prognose im Client-Warnhinweis nicht binnen vier Wochen ab „Aufschaltdatum“ einstellt. Wenn der Traffic nach wie vor erwartet wird, muss ein neuer Client-Warnhinweis für eine Traffic-Zunahme erstellt werden.
