---
description: Erfahren Sie mehr über die Anomalieerkennung und deren Berechnung.
title: Verwendung der Anomalieerkennung zur automatischen Suche von Trends
uuid: 02da21b4-3394-471b-97b5-aa1bddf1f445
feature: Report Builder
role: User, Admin
exl-id: 6e3881c8-3e1c-4df8-ba38-e8bc84cfc3d4
TQID: https://experienceleague.adobe.com/P2dvU8YgWcjCZ6h4oTxK-2-z1X3-wl-oMp70UIJGeXo
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2: id: ac8a38fa-dec3-4581-8f64-178fde9f64e8id: c67272a6-888e-425e-9e97-a87304637eedid: e93b8c4c-c5f7-45f8-9abe-9b710f53f502id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 511
ht-degree: 20%

---

# Anomalieerkennung{#anomaly-detection}

{{legacy-arb}}

Die Anomalieerkennung verwendet die statistische Modellierung, um unerwartete Trends in Ihren Daten automatisch zu finden. Das Modell analysiert Metriken und ermittelt Ober- und Untergrenze sowie eine erwartete Bandbreite von Werten. Treten unerwartete Spitzen oder Rückgänge auf, meldet das System dies im entsprechenden Bericht.

Beispiele für Anomalien, die Sie untersuchen können:

* Drastische Rückgänge beim durchschnittlichen Bestellwert
* Spitzen bei Bestellungen mit niedrigem Umsatz
* Spitzen oder Rückgänge bei Testregistrierungen
* Rückgänge bei Landingpage-Ansichten
* Gewürze in Videopuffer-Ereignissen
* Spitzen bei niedrigen Video-Bitraten

>[!NOTE]
>
>Die Anomalieerkennung ist nur verfügbar, wenn Sie als Granularität „Tag“ auswählen.

<p class="head"> <b>Metriken der Anomalieerkennung</b> </p>

Die Anomalieerkennung fügt für jede ausgewählte Metrik neue Metrikwerte hinzu, darunter:

<table id="table_BF75FC874634498DB6632C12CBD8D533"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Untergrenze </td> 
   <td colname="col2"> <p>Niedrigere Ebene des Prognoseintervalls. Werte unterhalb dieser Ebene werden als anomal betrachtet. </p> <p>Stellt eine 95%ige Konfidenz dar, dass Werte über diesem Wert liegen werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Erwartet </td> 
   <td colname="col2"> <p>Der auf der Datenanalyse basierende Prognosewert. Dieser Wert ist auch der Mittelpunkt zwischen der oberen und der unteren Grenze. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Obergrenze </td> 
   <td colname="col2"> <p>Obere Ebene des Prognoseintervalls. Werte oberhalb dieser Ebene werden als anomal betrachtet. </p> <p>Stellt eine 95%ige Konfidenz dar, dass Werte unter diesem Wert liegen werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

Report Builder wendet diese Werte auf ausgewählte Metriken an. Wenn Sie beispielsweise eine Seitenansichtsmetrik auswählen und die Anomalieerkennung anwenden, wird eine *`Page Views Lower Bound`* Metrik verwendet.

**Wie wird die Anomalieerkennung berechnet**

Die Anomalieerkennung verwendet einen Trainingszeitraum, um Prognoseintervalldaten pro Tag zu berechnen, zu erlernen und zu melden. Der Schulungszeitraum ist der historische Zeitraum, der angibt, was normal und was anomal ist, und das Gelernte auf den Berichtszeitraum anwendet. In Marketing-Berichten stehen Schulungszeiten von 30, 60 und 90 zur Verfügung. In Report Builder sind 30 Tage verfügbar.

Der Ausbildungszeitraum ist nicht unbedingt identisch mit dem ausgewählten Berichtszeitraum. Ein Berichtsdiagramm zeigt den Datumsbereich an, den Sie im Kalender angeben.

Um die Daten zu berechnen, wird der tägliche Gesamtwert für jede Metrik mit dem Trainings-Zeitraum verglichen, indem jeder der folgenden Algorithmen verwendet wird:

* Holt Winters Multiplikativ (Dreifach-Exponentialglättung)
* Holt Winters Additive (dreifach exponentielle Glättung)
* Holts-Trend korrigiert (doppelte exponentielle Glättung)

Jeder Algorithmus wird angewendet, um den Algorithmus mit der kleinsten Summe von quadrierten Fehlern (SSE) zu bestimmen. Der mittlere absolute Prozentfehler (Mean Absolute Percent Error, MAPE) und der aktuelle Standardfehler werden dann berechnet, um sicherzustellen, dass das Modell statistisch gültig ist.

Diese Algorithmen können erweitert werden, um Prognosen für Metriken in zukünftigen Zeiträumen bereitzustellen.

Da der Schulungszeitraum je nach Beginn des Berichtszeitraums variiert, können Unterschiede in den für dasselbe Datum gemeldeten Daten als Teil von zwei verschiedenen Zeiträumen auftreten.

Wenn Sie beispielsweise einen Bericht für den 1. bis 14. Januar ausführen und dann einen Bericht für den 7. bis 21. Januar ausführen, werden möglicherweise in den beiden verschiedenen Berichten unterschiedliche Prognosedaten für dieselbe Metrik zwischen dem 7. und 14. Januar angezeigt. Dies ist auf die unterschiedlichen Ausbildungszeiten zurückzuführen.

| Reporting-Bereich | Ausbildungszeit |
|--- |--- |
| &#x200B;1. bis 14. Januar | &#x200B;27. November - 31. Dezember |
| &#x200B;7. bis 21. Januar | &#x200B;4. Dezember - 6. Januar |
