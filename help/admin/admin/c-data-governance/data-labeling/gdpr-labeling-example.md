---
description: Zeigt Beispiele zum Beschriften von Daten für Trefferdaten, Zugriffsanfragen und Löschanfragen
title: Beschriftungsbeispiele
feature: Data Governance
role: Admin
exl-id: 9bea8636-c79c-4998-8952-7c66d31226e3
source-git-commit: 3e87d420591405e57e57e18fda4287d5fbd3bf1b
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 72%

---

# Beschriftungsbeispiele

## Beispiel für Trefferdaten {#hit}

Angenommen, es liegen die folgenden Trefferdaten vor:

* Die erste Zeile enthält die Beschriftungen für die einzelnen Variablen.
* Die zweite Zeile entspricht dem Namen der Variable. Wenn sie eine ID-Beschriftung aufweist, enthält sie den zugewiesenen Namespace in Klammern.
* Die Trefferdaten beginnen in der dritten Reihe.

| Bezeichnungen | I2 <br> ID-PERSON <br> DEL-PERSON <br> ACC-PERSON | I2 <br> ID-DEVICE <br> DEL-DEVICE <br> ACC-ALL | I2 <br> DEL-PERSON <br> ACC-PERSON | I2 <br> DEL-DEVICE <br> DEL-PERSON <br> ACC-ALL | I2 <br> ID-DEVICE <br> DEL-DEVICE <br> ACC-ALL |
|---|---|---|---|---|---|
| **Variablenname** <br> **(Namespace)** | **MyProp1** <br> **(user)** | **Besucher-ID** <br> **(AAID)** | **MyEvar1** | **MyEvar2** | **MyEvar3** <br> **(xyz)** |
| Trefferdaten | Mary | 77 | A | M | X |
| | Mary | 88 | B | N | Y |
| | Mary | 99 | C | O | Z |
| | John | 77 | D | P | W |
| | John | 88 | E | N | U |
| | John | 44 | F | Q | V |
| | John | 55 | G | R | X |
| | Alice | 66 | A | N | Z |

## Beispiel einer Zugriffsanfrage {#access}

Wenn Sie eine Zugriffsanfrage stellen, erhalten Sie zwei Dateien, die Sie an die betroffene Person zurücksenden können. Eine Datei ist eine CSV-Datei, die eine Zeile für jeden für die betroffene Person empfangenen Treffer und eine Spalte für jede Variable mit der entsprechenden Zugriffskennzeichnung enthält. Die andere Datei ist eine zusammenfassende HTML-Datei, in der jede Variable aufgelistet ist, gefolgt von allen eindeutigen Werten, die für diese Variable bei der betroffenen Person angezeigt wurden, und der Häufigkeit, mit der jeder eindeutige Wert angezeigt wurde.

Für unser Beispiel enthält die Zusammenfassungsdatei die in der folgenden Tabelle angegebenen Werte. Eine Anfrage kann nur eine Gerätedatei, eine Personendatei oder je eine von beiden zurückgeben. Zwei Zusammenfassungsdateien werden nur zurückgegeben, wenn eine Personen-ID verwendet wird und `expandIds` „true“ ist.

<table>
  <tr>
    <th colspan="2" style="text-align:center">API-Werte</th>
    <th rowspan="2">Summary<br/>file type<br/>returned</th>
    <th colspan="5" style="text-align:center">Daten in der Zusammenfassungsdatei für den Zugriff</th>
  </tr>
  <tr>
    <th>Namensraum/ID</th>
    <th>expandIDs</th>
    <th>MyProp1</th>
    <th>Besucher-ID</th>
    <th>MyEvar1</th>
    <th>MyEvar2</th>
    <th>MyEvar3</th>
  </tr>
  <tr>
    <td>AAID=77</td>
    <td>false (falsch)</td>
    <td>Gerät</td>
    <td>nicht vorhanden</td>
    <td>77</td>
    <td>nicht vorhanden</td>
    <td>M, P</td>
    <td>X, W</td>
  </tr>
  <tr>
    <td>AAID=77</td>
    <td>true (wahr)</td>
    <td>Gerät</td>
    <td>nicht vorhanden</td>
    <td>77</td>
    <td>nicht vorhanden</td>
    <td>M, P</td>
    <td>X, W</td>
  </tr>
  <tr>
    <td>user=Mary</td>
    <td>false (falsch)</td>
    <td>Person</td>
    <td>Mary</td>
    <td>77, 88, 99</td>
    <td>A,B,C</td>
    <td>M, N, O</td>
    <td>X, Y, Z</td>
  </tr>
  <tr>
    <td rowspan="2">user=Mary</td>
    <td rowspan="2">true (wahr)</td>
    <td>Person</td>
    <td>Mary</td>
    <td>77, 88, 99</td>
    <td>A,B,C</td>
    <td>M, N, O</td>
    <td>X, Y, Z</td>
  </tr>
  <tr>
    <td>Gerät</td>
    <td>nicht vorhanden</td>
    <td>77, 88</td>
    <td>A,B,C</td>
    <td>N, P</td>
    <td>U, W</td>
  </tr>
  <tr>
    <td rowspan="2">user=Mary<br>AAID=66</td>
    <td rowspan="2">true (wahr)</td>
    <td>Person</td>
    <td>Mary</td>
    <td>77, 88, 99</td>
    <td>A,B,C</td>
    <td>M, N, O</td>
    <td>X, Y, Z</td>
  </tr>
  <tr>
    <td>Gerät</td>
    <td>nicht vorhanden</td>
    <td>66, 77, 88</td>
    <td>A,B,C</td>
    <td>N, P</td>
    <td>U, W, Z</td>
  </tr>
  <tr>
    <td>xyz=X</td>
    <td>false (falsch)</td>
    <td>Gerät</td>
    <td>nicht vorhanden</td>
    <td>55, 77</td>
    <td>nicht vorhanden</td>
    <td>M, R</td>
    <td>X</td>
  </tr>
  <tr>
    <td>xyz=X</td>
    <td>true (wahr)</td>
    <td>Gerät</td>
    <td>nicht vorhanden</td>
    <td>55, 77</td>
    <td>nicht vorhanden</td>
    <td>M, P, R</td>
    <td>W, X</td>
  </tr>
</table>

Beachten Sie, dass die Einstellung für `expandIDs` keinen Unterschied bei der Ausgabe macht, wenn eine Cookie-ID verwendet wird.

## Beispiel für Löschanfragen {#delete}

Wenn für eine Löschanfrage die API-Werte in der ersten Zeile der Tabelle verwendet werden, wird die Treffertabelle aktualisiert und sieht dann folgendermaßen aus:

<table>
  <tr>
    <th colspan="5" style="text-align:center">AAID=77 <br>(Wert von „expandIDs“ spielt keine Rolle)</th>
  </tr>
  <tr>
    <th>MyProp1</th>
    <th>AAID</th>
    <th>MyEvar1</th>
    <th>MyEvar2</th>
    <th>MyEvar3</th>
  </tr>
  <tr>
    <td>Mary</td>
    <td>42</td>
    <td>A</td>
    <td>Datenschutz-7398</td>
    <td>Datenschutz-9152</td>
  </tr>
  <tr>
    <td>Mary</td>
    <td>88</td>
    <td>B</td>
    <td>N</td>
    <td>Y</td>
  </tr>
  <tr>
    <td>Mary</td>
    <td>99</td>
    <td>C</td>
    <td>O</td>
    <td>Z</td>
  </tr>
  <tr>
    <td>John</td>
    <td>42</td>
    <td>D</td>
    <td>Datenschutz-1866</td>
    <td>Datenschutz-8216</td>
  </tr>
  <tr>
    <td>John</td>
    <td>88</td>
    <td>E</td>
    <td>N</td>
    <td>U</td>
  </tr>
  <tr>
    <td>John</td>
    <td>44</td>
    <td>F</td>
    <td>Q</td>
    <td>V</td>
  </tr>
  <tr>
    <td>John</td>
    <td>55</td>
    <td>G</td>
    <td>R</td>
    <td>X</td>
  </tr>
  <tr>
    <td>Alice</td>
    <td>66</td>
    <td>A</td>
    <td>N</td>
    <td>Z</td>
  </tr>
</table>

>[!NOTE]
>
>Dies hat nur Einfluss auf Spalten in Zeilen, die `AAID=77` und eine `DEL-DEVICE` enthalten.

<table>
  <tr>
    <th colspan="5" style="text-align:center">user=Mary <br> expandIDs=false</th>
  </tr>
  <tr>
    <th>MyProp1</th>
    <th>AAID</th>
    <th>MyEvar1</th>
    <th>MyEvar2</th>
    <th>MyEvar3</th>
  </tr>
  <tr>
    <td>Datenschutz-0523</td>
    <td>77</td>
    <td>Datenschutz-1866</td>
    <td>Datenschutz-3681</td>
    <td>X</td>
  </tr>
  <tr>
    <td>Datenschutz-0523</td>
    <td>88</td>
    <td>Datenschutz-2178</td>
    <td>Datenschutz-1975</td>
    <td>Y</td>
  </tr>
  <tr>
    <td>Datenschutz-0523</td>
    <td>99</td>
    <td>Datenschutz-9045</td>
    <td>Datenschutz-2864</td>
    <td>Z</td>
  </tr>
  <tr>
    <td>John</td>
    <td>77</td>
    <td>D</td>
    <td>P</td>
    <td>W</td>
  </tr>
  <tr>
    <td>John</td>
    <td>88</td>
    <td>E</td>
    <td>N</td>
    <td>U</td>
  </tr>
  <tr>
    <td>John</td>
    <td>44</td>
    <td>F</td>
    <td>Q</td>
    <td>V</td>
  </tr>
  <tr>
    <td>John</td>
    <td>55</td>
    <td>G</td>
    <td>R</td>
    <td>X</td>
  </tr>
  <tr>
    <td>Alice</td>
    <td>66</td>
    <td>A</td>
    <td>N</td>
    <td>Z</td>
  </tr>
</table>

>[!NOTE]
>
>Dies hat nur Einfluss auf cellColumns in Zeilen, die `user=Mary` und eine `DEL-PERSON` enthalten. In der Praxis wäre die Variable, die `A_ID` enthält, wahrscheinlich auch eine Prop oder eine eVar. Der Ersatzwert wäre eine Zeichenfolge, die mit `Privacy-` beginnt, gefolgt von einer zufälligen Zahl (GUID), anstatt den numerischen Wert durch einen anderen, zufälligen numerischen Wert zu ersetzen.

<table>
  <tr>
    <th colspan="5" style="text-align:center">user=Mary <br> expandIDs=true</th>
  </tr>
  <tr>
    <th>MyProp1</th>
    <th>AAID</th>
    <th>MyEvar1</th>
    <th>MyEvar2</th>
    <th>MyEvar3</th>
  </tr>
  <tr>
    <td>Datenschutz-5782</td>
    <td>09</td>
    <td>Datenschutz-0859</td>
    <td>Datenschutz-8183</td>
    <td>Datenschutz-9152</td>
  </tr>
  <tr>
    <td>Datenschutz-5782</td>
    <td>16</td>
    <td>Datenschutz-6104</td>
    <td>Datenschutz-2911</td>
    <td>Datenschutz-6821</td>
  </tr>
  <tr>
    <td>Datenschutz-5782</td>
    <td>83</td>
    <td>Datenschutz-2714</td>
    <td>Datenschutz-0219</td>
    <td>Datenschutz-4395</td>
  </tr>
  <tr>
    <td>John</td>
    <td>09</td>
    <td>D</td>
    <td>Datenschutz-8454</td>
    <td>Datenschutz-8216</td>
  </tr>
  <tr>
    <td>John</td>
    <td>16</td>
    <td>E</td>
    <td>Datenschutz-2911</td>
    <td>Datenschutz-2930</td>
  </tr>
  <tr>
    <td>John</td>
    <td>44</td>
    <td>F</td>
    <td>Q</td>
    <td>V</td>
  </tr>
  <tr>
    <td>John</td>
    <td>55</td>
    <td>G</td>
    <td>R</td>
    <td>X</td>
  </tr>
  <tr>
    <td>Alice</td>
    <td>66</td>
    <td>A</td>
    <td>N</td>
    <td>Z</td>
  </tr>
</table>

Beachten Sie Folgendes:

* Dies hat Einfluss auf Zellen in Zeilen, die `user=Mary` und eine `DEL-PERSON`-Kennzeichnung enthalten.

