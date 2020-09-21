---
description: Besucher-IDs können durch Auswahl der Kategorie „Generisch (Transaktions-ID)“ integriert werden.
subtopic: Data sources
title: Visitor ID
topic: Developer and implementation
uuid: 4e9ce675-72c2-42a4-8f2e-25140df19539
translation-type: ht
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
workflow-type: ht
source-wordcount: '230'
ht-degree: 100%

---


# Visitor ID

Besucher-IDs können durch Auswahl der Kategorie „Generisch (Transaktions-ID)“ integriert werden.

Weitere Informationen finden Sie im Thema über das [Integrieren von Offline-Daten](/help/import/c-data-sources/datasrc-integrating-offline-data.md).

<p class="head"> <b>Besucher-ID-Dimensionen</b> </p>

| Spaltenname | Beschreibung |
|--- |--- |
| Visitor ID | (Erforderlich) Eindeutiger Wert, der einen Kunden in Online- und Offline-Systemen kennzeichnet. |
| Datum | Verwenden Sie das folgende Datumsformat: MM/TT/JJJJ/HH/mm/SS (zum Beispiel 07/14/2017/06/00/00) |
| Trackingcode | Name des Trackingcodes. |
| Kategorie | Name der Kategorie.  Wenn Sie eine Kategorie angeben, müssen Sie auch ein Produkt auswählen. |
| Kanal | Kanalname. |
| eVarn | eVarn-Name. Gültige Werte für n sind Ganzzahlen zwischen 1 und 75. |
| Produkt | Produktname. |
| Bundesland | Name des Landes. |
| Zip | Postleitzahl. |

**Besucher-ID-Metriken**

| Spaltenname | Beschreibung |
|--- |--- |
| Clickthroughs | Anzahl der Trackingcode-Ansichten. |
| Hinzufügen zum Einkaufswagen | Anzahl der Zusätze zum Einkaufswagen. |
| Öffnung des Einkaufswagens | Anzahl der Öffnungen des Einkaufswagens. |
| Entnahmen aus dem Einkaufswagen | Anzahl der Entnahmen aus dem Einkaufswagen. |
| Warenkorbansichten | Anzahl der Einkaufswagenansichten. |
| Checkouts | Anzahl der Kassengänge. |
| Ereignis n | Häufigkeit, in der Ereignis n eintritt. Gültige Werte für n sind Ganzzahlen zwischen 1 und 100.  Wenn Sie ein Ansichtereignis festlegen, müssen Sie auch die entsprechende Datendimension (eVar) festlegen. Wenn Sie beispielsweise eVar2-Ansichten einschließen, müssen Sie eVar2 mit einem Wert angeben. |
| eVarn-Ansichten | Häufigkeit, in der eVar n angezeigt wurde. Gültige Werte für n sind Ganzzahlen zwischen 1 und 75. |
| Preis | Produktpreis. |
| Bestellungen | Anzahl der aufgegebenen Bestellungen. |
| Produktansichten | Anzahl der Produktansichten. |
| Menge | Anzahl der verkauften Einheiten. |
