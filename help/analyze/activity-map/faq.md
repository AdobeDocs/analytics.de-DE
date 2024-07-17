---
title: Activity Map – Häufig gestellte Fragen
description: Häufig gestellte Fragen zum Activity Map.
feature: Activity Map
role: User, Admin
exl-id: 6b2767cb-6c2c-4bf3-b9a9-a23418624650
source-git-commit: 64964972410911c2bea1460039def39b7c6dfa38
workflow-type: tm+mt
source-wordcount: '1094'
ht-degree: 15%

---

# Activity Map – Häufig gestellte Fragen

Häufig gestellte Fragen zum Activity Map.

+++Wie erteile ich Berechtigungen für Activity Map?

Berechtigungen zur Verwendung von Activity Map und den zugehörigen Dimensionen werden in der [Adobe Admin Console](/help/admin/admin-console/home.md) verarbeitet.

Die für das Activity Map erforderlichen [Berechtigungselemente](/help/admin/admin-console/permissions/product-profile.md) umfassen:

* **[!UICONTROL Analytics-Tools]** > **[!UICONTROL Activity Map]**
* **[!UICONTROL Analytics-Tools]** > **[!UICONTROL Segmentveröffentlichung]**
* **[!UICONTROL Dimensionen]** > **[!UICONTROL Activity Map Scroll-Reichweite]**
* **[!UICONTROL Dimensionen]** > **[!UICONTROL Activity Map-Link nach Region]**
* **[!UICONTROL Dimensionen]** > **[!UICONTROL Activity Map Region]**
* **[!UICONTROL Dimensionen]** > **[!UICONTROL Activity Map-Link]**
* **[!UICONTROL Dimensionen]** > **[!UICONTROL Activity Map-Seite]**

Weitere Informationen finden Sie unter [Produktprofilberechtigungen für Analytics-Tools](/help/admin/admin-console/permissions/analytics-tools.md) .

+++

++ Haben alle Analytics-Kunden Zugriff auf Activity Map?

Organisationen mit Adobe Analytics Standard, Premium und Ultimate haben Zugriff auf Activity Map. Auf diese Vertragstypen entfallen die meisten Adobe Analytics-Kunden.

+++

+++ Wie unterstützt Activity Map Einzelseiten-Apps (SPA)?

Alle paar Sekunden scannt Activity Map die Webseite nach Änderungen. Activity Map findet neue Inhalte auf der Seite, ohne dass eine Neuladung erforderlich ist. Dieser neue Inhalt wird jedoch immer dem Dimensionswert der ersten Seite zugeordnet.

* Activity Map prüft, ob sich die Sichtbarkeit von bekannten Links geändert hat. Wenn eine Änderung der Sichtbarkeit festgestellt wird, wird die Spalte „Präsenz“ der Tabelle „Links auf Seite“ für diesen Link mit [!UICONTROL Angezeigt] oder [!UICONTROL Ausgeblendet] aktualisiert.

* Wenn durch die Benutzerinteraktion neuer Inhalt erstellt wird, werden alle neuen Elemente, die von AppMeasurement als Link bestimmt werden, zur Tabelle [!UICONTROL Links auf Seite] hinzugefügt. Activity Map sendet eine neue Datenanfrage, die diese neuen Links enthält. Die neuen Links werden in der Tabelle [!UICONTROL Links auf Seite] angezeigt, wenn die Datenanforderung zurückgegeben wird.

+++

+++ Bietet Activity Map Daten zu Links, die angezeigt, aber nicht angeklickt werden?

Nein, Adobe verfolgt nicht automatisch Links, die nur angezeigt wurden.

+++

+++ Welche Browser und Versionen unterstützt Activity Map?

Activity Map unterstützt die aktuelle Version der gängigsten Browser.

+++

+++ Erhöht Activity Map Server-Aufrufe?

Activity Map sendet keine Server-Aufrufe von sich aus. Stattdessen werden Activity Map-Kontextdatenvariablen in Analytics-Seitenansichtsaufrufe auf der nachfolgenden Seite einbezogen. Einige frühere Versionen von Activity Map im Web SDK senden jedoch einen separaten Aufruf für Activity Map-Daten. Wenn Sie die neueste Version des Web SDK verwenden, werden Activity Map-Daten mit dem folgenden Ereignis zusammengeführt.

+++

+++ Warum fehlen einige Rangnummern in der Überlagerung?

Einige Links, wie z. B. die in Menüs enthaltenen, werden von der Seite ausgeblendet. Daher werden die entsprechenden Linküberlagerungen nicht angezeigt. Der Rang wird für alle Links auf der Seite berechnet, einschließlich ausgeblendeter Links.

+++

+++ Wie wird die Linkranking-Rangfolge im Bericht &quot;Alle Links&quot;bestimmt?

* **Im Verlaufs- und Blasenmodus**: Die Metrikspalte bestimmt den Rang. Bei Links mit demselben Metrikwert basiert der Rang weiter auf der alphabetischen Reihenfolge der Link-IDs.
* **Im Modus Gewinner und Verlierer**: Die Spalte mit dem zugenommenen Prozentsatz bestimmt den Rang. Für Links mit dem gleichen Gewinn basiert der Rang außerdem auf der alphabetischen Reihenfolge der Link-IDs.

+++

+++ Wie funktioniert Activity Map mit Seiten, die mehrere Report Suites verwenden?

Standardmäßig verwendet Activity Map die Report Suite, die mit dem ersten Tag auf der Seite verknüpft ist. Sie können eine andere Report Suite über die Registerkarte **[!UICONTROL Activity Map-Einstellungen]** > **[!UICONTROL Sonstige]** auswählen.

+++

+++Wie lange sucht Activity Map auf der Seite nach Adobe Analytics?

Activity Map sucht bis zu 20 Sekunden nach Adobe Analytics, nachdem ein „page complete“-Ereignis abgeschlossen ist.

+++

+++Wie behandelt Activity Map dynamische Inhalte?

Activity Map sucht alle zwei Sekunden nach Statusänderungen der Web-Seite wie:

* HTML-Inhalt wurde angezeigt
* HTML-Inhalt wurde verborgen
* Neuer HTML-Inhalt wurde eingefügt

Wenn Inhalt ausgeblendet oder angezeigt wird, ändert die Erweiterung automatisch den Status der betroffenen Links (und somit Überlagerungen) von ausgeblendet in eingeblendet oder von eingeblendet in ausgeblendet. Wenn neue Inhalte eingefügt werden, ruft die Anwendung die zugehörigen Links ab, ruft Analysedaten für sie ab und fügt Überlagerungen für diese Links hinzu.

+++

+++ Auf welcher Metrik basiert der Seitenflussbericht?

Alle angezeigten Daten basieren auf Seitenansichten.

+++

+++ Kann ich Activity Map-Daten über Daten-Feeds exportieren?

Ja. Die [Daten-Feed-Spalten](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md), die von Activity Map verwendet werden, sind:

* Activity Map-Link: `clickmaplink`
* Activity Map page: `clickmappage`
* Activity Map region: `clickmapregion`
* Activity Map-Link nach Region: `clickmaplinkbyregion`

+++

+++ Funktionieren Segmente im Livemodus?

Nein, Segmente funktionieren nicht im Livemodus.

+++

+++ Ist Activity Map mit Virtual Report Suites kompatibel?

Ja. Aufgrund der Einschränkungen der Virtual Report Suite ist der Activity Map-Livemodus jedoch nicht mit Virtual Report Suites kompatibel.

+++

+++Wie kann ich Activity Map deaktivieren?

Die Methode zum Deaktivieren von Activity Map hängt von Ihrem Implementierungstyp ab:

* **Web SDK-Erweiterung**: Deaktivieren Sie in den Konfigurationseinstellungen der Erweiterung die Kontrollkästchen **[!UICONTROL Interne Link-Klicks abrufen]**, **[!UICONTROL Externe Link-Klicks abrufen]** und **[!UICONTROL Download-Link-Klicks abrufen]**.
* **Web SDK JavaScript Library**: Setzen Sie [`clickCollectionEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) auf `false`.
* **Analytics-Erweiterung**: Deaktivieren Sie in den Erweiterungskonfigurationseinstellungen das Kontrollkästchen **[!UICONTROL Activity Map verwenden]**.
* **AppMeasurement**: Entfernen oder kommentieren Sie das Activity Map-Modul innerhalb von `AppMeasurement.js` aus oder überschreiben Sie den Aufruf der Modulfunktion mit einem leeren Hauptteil:

  ```js
  function AppMeasurement_Module_ActivityMap() {}
  ```

+++

++ + Welche Systemanforderungen gelten für die Verwendung der Activity Map-Überlagerung?

Sie können die neueste Version von Chrome, Edge oder Firefox mit der Activity Map-Erweiterung verwenden.

+++

+++Was muss ich bei der Verwendung von Activity Map für persönlich identifizierbare Informationen beachten?

Betrachten Sie die folgenden Szenarien, in denen persönlich identifizierbare Daten mithilfe von Activity Map erfasst werden können:

* **E-Mail-Links**: Wenn eine E-Mail-Adresse angeklickt werden kann, um den E-Mail-Client des Benutzers zu öffnen, kann Activity Map die angeklickte E-Mail-Adresse erfassen.
* **Benutzer-ID-Links**: Nachdem sich ein Besucher angemeldet hat, kann Activity Map alle Links aufzeichnen, die die Benutzer-ID des Besuchers enthalten.
* **Links mit vertraulichen Informationen**: Für Finanzinstitute können vertrauliche Informationen wie die Kontonummer verfolgt werden, wenn es sich um einen Link handelt und die Besucher darauf klicken.
* **Links mit personenbezogenen Daten**: Für Websites im Gesundheitswesen können Links personenbezogene Daten enthalten. Wenn ein Besucher auf diese Links klickt, erfasst Activity Map diesen Link-Text.

+++

+++ Welche Daten verfolgt Activity Map standardmäßig?

Activity Map verfolgt die folgenden Elemente:

* Ein `<a>` - oder `<area>` -Tag mit der Eigenschaft `href` . Anker-Tag-Links (`#`) werden standardmäßig nicht verfolgt.
* Ein `onclick` -Attribut, das eine `s_objectID` -Variable festlegt
* Ein `<input>` -Tag oder eine `submit` -Schaltfläche mit einem Wert oder untergeordneten Text
* Ein `<input>` -Tag mit dem Typ `image` und einer `src` -Eigenschaft
* Ein `<button>` -Tag ohne das Attribut `type="button"`. Wenn Sie `<button>` -Tags verfolgen möchten, sollten Sie stattdessen Attribute wie `role="button"` oder `submit="button"` verwenden.

+++

+++ Was sind einige Beispiele für Links, die Activity Map automatisch verfolgt?

Im Folgenden finden Sie einige Beispiele, in denen Activity Map alle erforderlichen Informationen zum Verfolgen eines Links hat.

```html
<a href="home.html">Home</a>

<input type="submit" value="Submit"/>

<input type="image" src="submit-button.png"/>

<p onclick="var s_objectID='Market rates';">
  <span class="title">Current Market Rates</span>
  <span class="subtitle">1.45 USD</span>
</p>

<div onclick="s.tl(true,'o','Chat button')">
  <span class="title">Chat with an agent now</span>
  <span class="subtitle">Current wait: 0 minutes</span>
</div>
```

+++

+++ Was sind einige Beispiele für Links, die Activity Map NICHT automatisch verfolgt?

Im Folgenden finden Sie einige Beispiele, in denen Activity Map Klicks nicht verfolgt.

```html
<!-- Anchor tag does not have a valid href -->
<a name="innerAnchor">Section header</a>

<!-- Neither s_objectID or tl() method present -->
<p onclick="showPanel('stock price')">
  <span class="title">Current company stock price</span>
  <span class="subtitle">987.65 USD</span>
</p>

<!-- Neither s_objectID or tl() method present -->
<input type="radio" onclick="changeState(this)" name="group1" value="A"/>
<input type="radio" onclick="changeState(this)" name="group1" value="B"/>
<input type="radio" onclick="changeState(this)" name="group1" value="C"/>

<!-- src property missing on a form input element -->
<input type="image"/>
```

+++
