---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 45642bdbe18627caa20b1def6443f1e596a41f52

---



# Ereignisse

Die Variable „“ wird zur Aufzeichnung von Erfolgsereignissen normaler Warenkorbvorgänge sowie benutzerspezifischer Erfolgsereignisse verwendet.

<!-- 

events.xml

 -->

<table id="table_9EB9D08C80544CD68C4B1A2012440472"> 
 <thead> 
  <tr> 
   <th class="entry"> Maximale Größe </th> 
   <th class="entry"> Debug-Parameter </th> 
   <th class="entry"> Ausgefüllte Berichte </th> 
   <th class="entry"> Standardwert </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> Keine Begrenzung </td> 
   <td> events </td> 
   <td> <p>Warenkorbereignisse </p> <p>Benutzerspezifische Ereignisse </p> </td> 
   <td> Keine </td> 
  </tr> 
 </tbody> 
</table>

[!UICONTROL Ereignisse] sollten als Meilenstein in einer Site dienen. Erfolgsereignisse werden in den meisten Fällen auf der abschließenden Bestätigungsseite eines Vorgangs (z. B. einer Registrierung oder einer Anmeldung) ausgefüllt. Benutzerspezifische Ereignisse werden definiert, indem in der „events“-Variablen entsprechende Zeichenwerte eingetragen werden (siehe dazu Abschnitt Mögliche Werte weiter unten).

In der Standardeinstellung werden Erfolgsereignisse als *Zählerereignisse* konfiguriert. Zählerereignisse zählen, wie oft ein Erfolgsereignis eintritt (x+1). Ereignisse können auch als *numerische* Ereignisse festgelegt werden. Mithilfe numerischer Ereignisse können Sie angeben, um welche Höhe ein Wert erhöht werden soll (was beim Zählen dynamischer oder beliebiger Werte nützlich sein kann, zum Beispiel bei der Anzahl der von einer internen Suche zurückgegebenen Ergebnisse).

Mit Ereignissen vom Typ *Währung* können Sie einen hinzuzufügenden Geldbetrag festlegen. Dieser ist eine Zahlangabe wie bei numerischen Ereignissen, wird jedoch in Berichten als Geldbetrag angezeigt. Er kann gemäß der im Wert s. *`currencyCode`* und der in Ihrer Report Suite festgelegten Standardwährung in andere Währungen umgerechnet werden. Weitere Informationen zur Arbeit mit numerischen und Währungs-Ereignissen finden Sie in [Produkte](/help/implement/js-implementation/c-variables/page-variables.md).

**Konfigurieren der Variablen** {#section_9195286C34C54B02B2598E2B856492C3}

Die Variable [!UICONTROL s.events] ist in der Standardeinstellung für alle Implementierungen aktiviert. Die sieben vorkonfigurierten Konversionsereignisse sind bei allen neuen Report Suites automatisch aktiviert. Neue benutzerspezifische Ereignisse (event1– [event100 oder event1000](/help/implement/js-implementation/c-variables/page-variables.md)) können von jedem Nutzer mit Administratorrechten über die Admin Console aktiviert werden.

**Mögliche Werte** {#section_18395A3BEFEB4E9F8D7B2ED0001FBE4E}

Die folgenden Werte sind in der „events“-Variablen möglich:

| Ereignis | Beschreibung | Ausgefüllte Berichte |
|---|---|---|
| prodView | Produktansichten | Produkte |
| scOpen | Öffnen / Initialisieren eines neuen Warenkorbs | Warenkörbe |
| scAdd | Hinzufügen von Artikeln zum Warenkorb | Zusatz zum Warenkorb |
| scRemove | Entfernen von Artikeln aus dem Warenkorb | Entnahme aus Warenkorb |
| scView | Anzeigen von Warenkorb | Warenkorbansicht |
| scCheckout | Beginn des Checkout-Prozess | Checkouts |
| purchase | Abschluss eines Kaufs (oder einer Bestellung) | Bestellungen |
| event1 - event1000 (event100 für Punktprodukt) | Benutzerspezifische Ereignisse | Benutzerspezifische Ereignisse |

**Syntax und Beispiele** {#section_45A159DF00114066B8551DDEB15E084C}

Zählerereignisse werden festgelegt, indem die gewünschten Ereignisse in die [!UICONTROL s.events]-Variable eingetragen werden (bei mehreren Ereignissen in Form einer kommagetrennten Liste).

```js
s.events="scAdd"
```

```js
s.events="scAdd,event1,event7"
```

```js
s.events="event5"
```

```js
s.events="purchase,event10"
```

In H23-Code (oder höher) können Zählerereignissen auch ganzzahlige Werte größer Eins zugewiesen werden.

```js
s.events="event1=10"
```

```js
s.events="scRemove=3,event6,event2=4"
```

Zählerereignisse, die mit ganzzahligen Werten implementiert sind, werden so behandelt, als ob das Ereignis innerhalb der Bildanforderung mehrere Male ausgelöst wurde. Dezimalstellen sind in Zählerereignissen nicht zulässig. Sollte dies erforderlich sein, empfiehlt sich stattdessen die Verwendung von numerischen Ereignissen.
Numerische und Währungs-Ereignisse müssen in der Variablen [!UICONTROL s.events] stehen, obwohl sie ihre numerischen Werte (z. B. „24,99“) meist über die Variable [!UICONTROL s.products] erhalten. Dadurch können Sie bestimmte numerische und Währungswerte mit bestimmten Produkteinträgen verknüpfen.

**Ereignis-Serialisierung** {#section_A89488EF4471405AAFC4D6DD05E77621}

In der Standardeinstellung wird ein Ereignis jedes Mal gezählt, wenn es auf Ihrer Site festgestellt wird.

Weitere Informationen dazu finden Sie unter [Ereignis-Serialisierung](/help/implement/js-implementation/event-serialization.md).

**Syntax** {#section_8559D42D3F344AF3BB3C0125F78C4989}

```js
s.events="event1:3167fhjkah"
```

**Beispiele** {#section_7B5B5728A59648ADB3E2548CDAD2C9D4}

```js
s.events="scAdd:003717174"
```

```js
s.events="scAdd:user228197,event1:577247280,event7:P7fhF8571"
```
