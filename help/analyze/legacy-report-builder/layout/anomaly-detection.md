---
description: Erfahren Sie mehr über die Anomalieerkennung und deren Berechnung.
title: Verwendung der Anomalieerkennung zur automatischen Suche von Trends
uuid: 02da21b4-3394-471b-97b5-aa1bddf1f445
feature: Report Builder
role: User, Admin
exl-id: 6e3881c8-3e1c-4df8-ba38-e8bc84cfc3d4
source-git-commit: fcecc8a493852f5682fd7fbd5b9bb484a850922c
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 91%

---

# Anomalieerkennung{#anomaly-detection}

{{legacy-arb}}

Die Anomalieerkennung verwendet die statistische Modellierung, um unerwartete Trends in Ihren Daten automatisch zu finden. Das Modell analysiert Metriken und ermittelt Ober- und Untergrenze sowie eine erwartete Bandbreite von Werten. Treten unerwartete Spitzen oder Rückgänge auf, meldet das System dies im entsprechenden Bericht.

Zu Beispielen von Fehlern, die ein Eingreifen Ihrerseits erfordern, zählen:

* Erhebliche Verwerfungen im durchschnittlichen Bestellwert
* Spitzen in Bestellungen mit geringem Umsatz
* Spitzen oder Verwerfungen in Testprogrammregistrierungen
* Verwerfungen bei Landingpage-Aufrufen
* Spitzen in Videopufferereignissen
* Spitzen in niedrigen Video-Bitraten

>[!NOTE]
>
>Die Anomalieerkennung ist nur verfügbar, wenn Sie als Granularität „Tag“ auswählen.

<p class="head"> <b>Metrik für die Anomalieerkennung</b> </p>

Mit der Anomalieerkennung werden neue Metrikwerte für jede ausgewählte Metrik hinzugefügt, darunter:

<table id="table_BF75FC874634498DB6632C12CBD8D533"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Untere Grenze </td> 
   <td colname="col2"> <p>Untergrenze des Prognoseintervalls. Werte unter dieser Grenze werden als abweichend betrachtet. </p> <p>Stellt eine Konfidenz von 95 % dar, dass Werte über dieser Grenze liegen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Erwartet </td> 
   <td colname="col2"> <p>Der anhand der Datenanalyse prognostizierte Wert. Dieser Wert ist auch der Mittelpunkt zwischen Ober- und Untergrenze. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Obere Grenze </td> 
   <td colname="col2"> <p>Obergrenze des Prognoseintervalls. Werte über dieser Grenze werden als abweichend betrachtet. </p> <p>Stellt eine Konfidenz von 95 % dar, dass Werte unter dieser Grenze liegen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Report Builder wendet diese Werte auf ausgewählte Metriken an. Wenn Sie beispielsweise eine Seitenansichtsmetrik auswählen und die Anomalieerkennung anwenden, wird eine *`Page Views Lower Bound`* Metrik verwendet.

**Berechnung der Anomalieerkennung**

Die Anomalieerkennung nutzt einen Schulungszeitraum zum Berechnen, Erlernen und Berichten von Prognoseintervalldaten pro Tag. Der Schulungszeitraum ist der Verlaufszeitraum, der bestimmt, was als normal bzw. abweichend betrachtet wird, und wendet an, was im Berichtzeitraum gelernt wurde. In Marketing-Berichten sind Schulungszeiträume von 30, 60 und 90 Tagen verfügbar. In Report Builder sind 30 Tage verfügbar.

Der Schulungszeitraum ist nicht notwendigerweise mit dem ausgewählten Berichtzeitraum identisch. Eine Berichtsgrafik zeigt den Datumsbereich an, den Sie im Kalender angegeben haben.

Zum Berechnen der Daten wird der Tagesgesamtwert für jede Metrik anhand jedes der folgenden Algorithmen mit dem Schulungszeitraum verglichen:

* Holt-Winters-Multiplikativ (Dreifache exponentielle Ausgleichung)
* Holt-Winters-Additiv (Dreifache exponentielle Ausgleichung)
* Trendkorrektur nach Holt (Doppelte exponentielle Ausgleichung)

Es wird jeder einzelne Algorithmus angewendet, um den Algorithmus mit der kleinsten Summe der Fehlerquadrate (SFQ) zu bestimmen. Anschließend werden der mittlere absolute Prozentfehler (MAPF) und der aktuelle Standardfehler berechnet, um die statistische Gültigkeit des Modells sicherzustellen.

Diese Algorithmen können erweitert werden, um Prognosen für Metriken in zukünftigen Zeiträumen bereitzustellen.

Da der Schulungszeitraum je nach Beginn des Berichtzeitraums schwankt, treten in den gemeldeten Daten möglicherweise Unterschiede für dasselbe Datum auf, wenn dieses Teil zweier unterschiedlicher Zeiträume ist.

Wenn Sie beispielsweise einen Bericht für den 1. bis 14. Januar und dann einen Bericht für den 7. bis 21. Januar ausführen, können in den beiden Berichten für den 7. bis 14. Januar unterschiedliche Prognosedaten für dieselbe Metrik ausgegeben werden. Dies ergibt sich aus der Unterschiedlichkeit der Schulungszeiträume.

| Berichtszeitraum | Schulungszeitraum |
|--- |--- |
| &#x200B;1. bis 14. Januar | 27. November bis 31. Dezember |
| &#x200B;7. bis 21. Januar | 4. Dezember bis 6. Januar |
