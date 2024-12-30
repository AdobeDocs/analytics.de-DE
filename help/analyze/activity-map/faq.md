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

Berechtigungen zur Verwendung von Activity Map und den zugehörigen Dimensionen werden in der [Adobe Admin Console](/help/admin/admin-console/home.md) behandelt.

Die [Berechtigungselemente](/help/admin/admin-console/permissions/product-profile.md) die für das Activity Map erforderlich sind:

* **[!UICONTROL Analytics-Tools]** > **[!UICONTROL Activity Map]**
* **[!UICONTROL Analytics-Tools]** > **[!UICONTROL Segmentveröffentlichung]**
* **[!UICONTROL Dimensionen]** > **[!UICONTROL Activity Map Scroll-Reichweite]**
* **[!UICONTROL Dimensionen]** > **[!UICONTROL Activity Map-Link nach Region]**
* **[!UICONTROL Dimensionen]** > **[!UICONTROL Activity Map-Region]**
* **[!UICONTROL Dimensionen]** > **[!UICONTROL Activity Map-Link]**
* **[!UICONTROL Dimensionen]** > **[!UICONTROL Activity Map Seite]**

Weitere [ finden Sie unter „Produktprofilberechtigungen für ](/help/admin/admin-console/permissions/analytics-tools.md) Tools“.

+++

+++Haben alle Analytics-Kunden Zugriff auf Activity Map?

Unternehmen mit Verträgen für Adobe Analytics Standard, Premium und Ultimate haben Zugriff auf Activity Map. Diese Vertragstypen repräsentieren die Mehrheit der Adobe Analytics-Kunden.

+++

+++Wie unterstützt Activity Map Single Page Applications (SPA)?

Alle paar Sekunden scannt Activity Map die Webseite und sucht nach Änderungen. Activity Map findet neuen Inhalt auf der Seite, ohne dass ein Neuladen erforderlich ist. Dieser neue Inhalt wird jedoch immer dem Wert der Dimension „Erste Seite“ zugeordnet.

* Activity Map prüft, ob sich die Sichtbarkeit von bekannten Links geändert hat. Wenn eine Änderung der Sichtbarkeit festgestellt wird, wird die Spalte „Präsenz“ der Tabelle „Links auf Seite“ für diesen Link mit [!UICONTROL Angezeigt] oder [!UICONTROL Ausgeblendet] aktualisiert.

* Wenn durch Benutzerinteraktion neue Inhalte erstellt werden, werden alle neuen Elemente, die AppMeasurement als Link bestimmt, zur Tabelle [!UICONTROL Links auf Seite] hinzugefügt. Activity Map sendet eine neue Datenanfrage, die diese neuen Links enthält. Die neuen Links werden in der Tabelle [!UICONTROL Links auf Seite] angezeigt, wenn die Datenanfrage zurückgegeben wird.

+++

+++Bietet Activity Map Daten zu Links, die angezeigt, aber nicht angeklickt werden?

Nein, Adobe verfolgt Links, die nur angezeigt wurden, nicht automatisch.

+++

+++Welche Browser und Versionen werden von Activity Map unterstützt?

Activity Map unterstützt die aktuelle Version der gängigsten Browser.

+++

+++Erhöht Activity Map die Anzahl der Server-Aufrufe?

Activity Map sendet keine Server-Aufrufe von sich aus. Stattdessen werden Activity Map-Kontextdatenvariablen in die Analytics-Seitenansichtsaufrufe auf der nachfolgenden Seite eingeschlossen. Einige frühere Versionen von Activity Map auf dem Web-SDK senden jedoch einen separaten Aufruf für Activity Map-Daten. Wenn Sie die neueste Version von Web SDK verwenden, werden Activity Map-Daten mit dem folgenden Ereignis zusammengeführt.

+++

+++Warum fehlen einige Rangnummern in der Überlagerung?

Einige Links, z. B. in Menüs, werden auf der Seite ausgeblendet. Daher werden die entsprechenden Link-Überlagerungen nicht angezeigt. Der Rang wird für alle Links auf der Seite berechnet, einschließlich ausgeblendeter Links.

+++

+++Wie wird die Rangzuweisung für Links im Bericht „Alle Links“ bestimmt?

* **In den Modi „Verlauf“ und „Blase**: Die Metrikspalte bestimmt den Rang. Bei Links mit demselben Metrikwert basiert der Rang außerdem auf der alphabetischen Reihenfolge der Link-IDs.
* **Im Modus „Gewinner und Verlierer**: Die Spalte mit dem prozentualen Zuwachs bestimmt den Rang. Für Links mit dem gleichen Gewinn basiert der Rang außerdem auf der alphabetischen Reihenfolge der Link-IDs.

+++

+++Wie funktioniert das Activity Map mit Seiten, die mehrere Report Suites verwenden?

Standardmäßig verwendet Activity Map die Report Suite, die mit dem ersten Tag auf der Seite verknüpft ist. Sie können eine andere Report Suite auf der Registerkarte **[!UICONTROL Activity Map-Einstellungen]** > **[!UICONTROL Sonstige]** auswählen.

+++

+++Wie lange sucht Activity Map nach Adobe Analytics auf der Seite?

Activity Map sucht bis zu 20 Sekunden nach Adobe Analytics, nachdem ein „page complete“-Ereignis abgeschlossen ist.

+++

+++Wie verarbeitet Activity Map dynamische Inhalte?

Activity Map sucht alle zwei Sekunden nach Statusänderungen der Web-Seite wie:

* HTML-Inhalt wurde angezeigt
* HTML-Inhalt wurde verborgen
* Neuer HTML-Inhalt wurde eingefügt

Wenn Inhalte ausgeblendet oder angezeigt werden, ändert die Erweiterung automatisch den Status der betroffenen Links (und somit der Überlagerungen) von „ausgeblendet“ in „angezeigt“ oder von „angezeigt“ in „ausgeblendet“. Wenn neue Inhalte eingefügt werden, ruft das Programm die zugehörigen Links ab, ruft Analysedaten für sie ab und fügt Überlagerungen für diese Links hinzu.

+++

+++Auf welcher Metrik basiert der Seitenflussbericht?

Alle angezeigten Daten basieren auf Seitenansichten.

+++

+++Kann ich Activity Map-Daten über Daten-Feeds exportieren?

Ja. Activity Map verwendet [Daten-Feed](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md)Spalten):

* Activity Map-Link: `clickmaplink`
* Activity Map-Seite: `clickmappage`
* Activity Map-Region: `clickmapregion`
* Activity Map-Link nach Region: `clickmaplinkbyregion`

+++

+++Funktionieren Segmente im Live-Modus?

Nein, Segmente funktionieren nicht im Live-Modus.

+++

+++Ist Activity Map mit Virtual Report Suites kompatibel?

Ja. Aufgrund der Einschränkungen von Virtual Report Suites ist der Activity Map-Live-Modus jedoch nicht mit Virtual Report Suites kompatibel.

+++

+++Wie kann ich Activity Map deaktivieren?

Die Methode zum Deaktivieren von Activity Map hängt von Ihrem Implementierungstyp ab:

* **Web SDK-Erweiterung**: Deaktivieren Sie in den Erweiterungskonfigurationseinstellungen die Kontrollkästchen **[!UICONTROL Klicks auf interne Links erfassen]**, **[!UICONTROL Klicks auf externe Links erfassen]** und **[!UICONTROL Klicks auf Downloadlinks erfassen]**.
* **Web SDK JavaScript Library**: [`clickCollectionEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) auf `false` setzen.
* **Analytics-Erweiterung**: Deaktivieren Sie in den Erweiterungskonfigurationseinstellungen das Kontrollkästchen **[!UICONTROL Activity Map verwenden]**.
* **AppMeasurement**: Entfernen Sie das Activity Map-Modul in `AppMeasurement.js` oder kommentieren Sie es aus, oder überschreiben Sie den Modulfunktionsaufruf mit einem leeren Text:

  ```js
  function AppMeasurement_Module_ActivityMap() {}
  ```

+++

+++Welche Systemanforderungen gelten für die Verwendung der Activity Map-Überlagerung?

Sie können die neueste Version von Chrome, Edge oder Firefox mit der Activity Map-Erweiterung verwenden.

+++

+++Was muss ich beachten, wenn ich Activity Map für persönlich identifizierbare Informationen verwende?

Betrachten Sie die folgenden Szenarien, in denen persönlich identifizierbare Daten mithilfe von Activity Map erfasst werden können:

* **E-Mail-Links**: Wenn eine E-Mail-Adresse angeklickt werden kann, um den E-Mail-Client des Benutzers zu öffnen, kann Activity Map die angeklickte E-Mail-Adresse erfassen.
* **Benutzer-ID-Links**: Nach der Anmeldung eines Besuchers kann Activity Map alle Links aufzeichnen, die die Benutzer-ID des Besuchers enthalten.
* **Links zu sensiblen Informationen**: Bei Finanzinstituten können vertrauliche Informationen wie Kontonummern verfolgt werden, wenn es sich um einen Link handelt und die Besucher auf sie klicken.
* **Links, die personenbezogene Daten enthalten**: Bei Websites des Gesundheitswesens können Links personenbezogene Daten enthalten. Wenn ein Besucher auf diese Links klickt, erfasst Activity Map diesen Link-Text.

+++

+++Welche Daten werden von Activity Map standardmäßig nachverfolgt?

Activity Map verfolgt die folgenden Elemente:

* Ein `<a>`- oder `<area>`-Tag mit einer `href`. Anker-Tag-Links (`#`) werden standardmäßig nicht verfolgt.
* Ein `onclick`, das eine `s_objectID` festlegt
* Ein `<input>`-Tag oder eine `submit` mit einem Wert oder einem untergeordneten Text
* Ein `<input>` Tag mit dem Typ `image` und einer `src` Eigenschaft
* Ein `<button>`-Tag ohne das Attribut `type="button"`. Wenn Sie `<button>` Tags verfolgen möchten, sollten Sie stattdessen Attribute wie `role="button"` oder `submit="button"` verwenden.

+++

+++Was sind einige Beispiele für Links, die von Activity Map automatisch verfolgt werden?

Im Folgenden finden Sie einige Beispiele, bei denen Activity Map über alle erforderlichen Informationen zum Nachverfolgen eines Links verfügt.

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

+++Was sind einige Beispiele für Links, die von Activity Map NICHT automatisch verfolgt werden?

Im Folgenden finden Sie einige Beispiele, bei denen Activity Map Klicks nicht verfolgt.

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
