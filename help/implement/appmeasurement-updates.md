---
title: Versionshinweise für AppMeasurement für JavaScript
description: Gesammelte Versionshinweise für AppMeasurement für JavaScript.
feature: Appmeasurement Implementation
exl-id: 80b935f0-3ec5-4ffa-9858-f83ae9a6b763
role: Admin, Developer, Leader, User
TQID: https://experienceleague.adobe.com/iszRZIB8QN3ihEcNWcOHyO1rVGMuKpt6YTkrquuKfWs
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
  - id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2:
  - id: c069c44e-5426-4c1a-accc-8028662f2fde
  - id: df312454-73c4-43f6-a90e-18f5043f074c
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: d4db20e3498d54162806b3fdef0b34f45c93a6ff
workflow-type: tm+mt
source-wordcount: 2881
ht-degree: 56%

---

# Versionshinweise für AppMeasurement für JavaScript

>[!IMPORTANT]
>
>Ab März 2025 wird dieser Artikel nicht mehr aktualisiert. Sie können die Versionshinweise für anzeigen und die neueste Version von AppMeasurement von [GitHub](https://github.com/adobe/appmeasurement/releases) herunterladen.


## Version 2.27.0

Releasedatum: **Dienstag, 12. August 2024**

* Das `s_ac`-Cookie wird jetzt mit der `secure`-Markierung geschrieben, wenn `writeSecureCookies` aktiviert wurde.
* Fehlerkorrektur - Bei der Initialisierung tritt jetzt kein Fehler mehr auf, wenn die Bibliothek inline eingebettet ist.
* Fehlerkorrektur - Wenn `localStorage` oder `sessionStorage` deaktiviert wurden, tritt jetzt kein Fehler mehr auf.
* Benutzeragenten-Hinweise mit hoher Entropie sind jetzt in Linktracking-Aufrufen (`tl`) enthalten, wenn `collectHighEntropyUserAgentHints` aktiviert wurde.

## Version 2.26.0

Releasedatum: **Dienstag, 4. März 2024**

* AppMeasurement erkennt und verwendet automatisch die Stamm-Domain für Länder-Code-Domains auf oberster Ebene, für die zuvor bestimmte Cookie-Domain-Konfigurationen erforderlich waren. Die Aktualisierung kann aufgrund dieser automatischen Erkennung Auswirkungen haben.
* Die Verteilung umfasst die Identity Service-Bibliothek 5.5.0 und Data Integration Library 9.6.

## Version 2.25.0

Veröffentlichungsdatum: **Mittwoch, 12. September 2023**

* Es wurde die optionale Methode [`bufferRequests()`](vars/functions/bufferrequests.md) hinzugefügt, um die Zuverlässigkeit der Erfassung von Anfragen zu erhöhen, wenn ein Browser die Beacon-API nicht unterstützt, oder Anfragen beim Entladen einer Seite abbricht.
* Es wurden Sicherheitsmaßnahmen hinzugefügt, um mehrere Nachverfolgungs-Callbacks für eine einzelne Verfolgungsanfrage zu verhindern.

## Version 2.24.0

Releasedatum: **Mittwoch, 18. Juli 2023**

* Es wurde die optionale Konfigurationsvariable [`decodeLinkParameters`](vars/config-vars/decodelinkparameters.md) hinzugefügt, um Link-URLs zu decodieren, die doppelbyte-codierte Zeichen enthalten.
* Es wurde eine zusätzliche Fehlerbehandlung für Browser mit fehlerhaften APIs für Benutzeragenten-Client-Hinweise mit hoher Entropie hinzugefügt.
* Die Kopfzeile des POST-Inhaltstyps wurde geändert, sodass `x-www-form-urlencoded` standardmäßig verwendet wird.

## Version 2.23.0

Veröffentlichungsdatum: **23. September 2022**

* AppMeasurement unterstützt jetzt die Erfassung von Benutzeragenten-Client-Hinweisen mit hoher Entropie, die von Chromium-Browsern (Google Chrome und Microsoft Edge) verwendet werden, um Geräteinformationen bereitzustellen. Sie können Client-Hinweise über Tags konfigurieren oder die Konfigurationsvariable [`collectHighEntropyUserAgentHints`](vars/config-vars/collecthighentropyuseragenthints.md) verwenden. Die Sammlung von Hinweisen mit hoher Entropie ist standardmäßig deaktiviert. Weitere Informationen zu Benutzeragenten-[Client-Hinweisen](/help/technotes/client-hints.md).

## Version 2.22.4

Veröffentlichungsdatum: **18. Januar 2022**

* Der Linktracking-Aufruf `s.tl()` überprüft jetzt, ob das Objekt, das an diesen übergeben wird, ein `href`-Attribut des Typs `string` enthält. Wenn es sich nicht um einen `string` handelt, wird das `href`-Attribut einfach ignoriert, anstatt fehlzuschlagen. Dieses Szenario kann eintreten, wenn Sie `svg` -Objekte an den Linktracking-Aufruf übergeben.

## Version 2.22.3

Releasedatum: **11. Oktober 2021**

* Links in Dateien, die auf die -Dokumentation verweisen, wurden aktualisiert.

## Version 2.22.2

Releasedatum: **7. September 2021**

* Durch diese Aktualisierung werden `opt.dmp` und `opt.sell` beim Verfolgen von Links immer einbezogen. Weitere Informationen finden [&#x200B; im &#x200B;](/help/admin/tools/manage-rs/edit-settings/privacy-reporting.md) „Datenschutzberichte“ im Admin-Benutzerhandbuch.

## Version 2.22.1

Releasedatum: **17. August 2021**

* Kunden, die das Opt-out verwenden, haben möglicherweise gesehen, dass die Opt-out-Parameter für die Server-seitige Weiterleitung beim Verfolgen von Links nicht berücksichtigt wurden. Die Korrekturen in dieser Version führen dazu, dass die Opt-out-Flags gesendet werden, wenn sie beim Verfolgen von Links vorhanden sind.

## Version 2.22.0

Releasedatum: **4. August 2020**

* Korrektur für fehlenden Referrer, wenn der erste Treffer aufgrund der Opt-out-Einstellungen des Benutzers nicht gesendet wurde.

## Version 2.21.0

Releasedatum: **24. Juni 2020**

* Es wurde ein Problem behoben, bei dem der Activity Map-linkExclusions-Filter nicht immer für Firefox angewendet wurde.

## Version 2.20.0

Releasedatum: **5. März 2020**

* Es wurde ein sicherheitsbezogenes Problem behoben, indem die Erkennung von Internet Explorer aktualisiert wurde, um die JSLint-Warnung zu unterdrücken.

## Version 2.19.0

Releasedatum: **21. Februar 2020**

* Aktualisiertes Zielgruppen-Management-Modul auf DIL 9.4. (AN-209341)

## Version 2.18.0

Releasedatum: **13. Februar 2020**

* AppMeasurement kann nun erzwingen, dass Cookies das Secure-Attribut einschließen, indem die [`writeSecureCookies`](vars/config-vars/writesecurecookies.md)-Variable festgelegt wird. Voraussetzung für diese Variable ist, dass die gesamte Client-Website sicher bereitgestellt wird (HTTPS). (AN-204604)

## Version 2.17.0

Releasedatum: **23. August 2019**

* Unterstützung für die Neuordnung der Baidu-Abfragezeichenfolge wurde hinzugefügt. (AN-182483)
* Ein Fehler wurde behoben, aufgrund dessen alte Besucherwerte für Aufrufe angezeigt wurden, die vor dem Opt-in in einer Warteschlange warteten. (AN-184391)

## Version 2.16.0

Releasedatum: **15. August 2019**

* `sendBeacon`-Unterstützung in [!UICONTROL AppMeasurement] für Exitlinks wurde implementiert. Wenn ein Treffer `sendBeacon` verwendet und die Seite entladen wird, ist die Anforderung trotzdem abgeschlossen. Dies ist sehr nützlich für Exitlinks, da es wahrscheinlicher ist, dass der Treffer die Datenerfassungs-Server erreicht. (AN-175142)
* ECID/fid-Werte werden jetzt beim ersten Treffer zwischengespeichert, auch wenn sich die OptIn-Einstellungen ändern. (AN-175142)
* Zielgruppen-Management Modul wurde auf DIL 9.3 aktualisiert. (AN-182704)
* Scroll-Reichweiten-Tracking kann jetzt in `s.ActivityMap.trackScrollReach` über einen Schalter ein- oder ausgeschaltet werden. (AN-182754)
* AppMeasurement wurde für die Verwendung von Besucher-ID-Dienst 4.4.0 aktualisiert. (AN-182912)

## Version 2.15.0

Releasedatum: **15. Juli 2019**

* Scroll-Reichweitenverfolgung für ActivityMap zur ActivityMap-Erweiterung hinzugefügt (AN-172949)
* DIL 9.2 zu AppMeasurement (AN-182472) hinzugefügt

## Version 2.14.0

Releasedatum: **21. Mai 2019**

* Korrektur von Problemen mit Verwaltung des Status von Trackerparametern, wenn mehrere Treffer ausstehend sind. (AN-176931, AN-176629, DTM-12758)
* Aktualisierung von AppMeasurement, sodass Visitor.js 4.3.0 eingeschlossen ist (AN-180049)

## Version 2.13.0

Releasedatum: **10. April 2019**

* Behebung vieler gemeldeter Probleme mit clearVars. Das Problem tritt auf, wenn Treffer gesendet werden, bevor der Tracker bereit ist. Sobald der Tracker fertig ist, kann die Bibliothek Variablen festlegen, die bereits gelöscht oder geändert wurden. (AN-176931, AN-176629, DTM-12758).

## Version 2.12.0

Releasedatum: **22. Februar 2019**

* Aktualisiertes Zielgruppen-Management-Modul auf DIL 9.1. (AN-175255)
* GTM-Sicherheitsrichtlinie lässt Activity Map-Modul nicht zu. (AN-174679)
* Verbessertes AppMeasurement berücksichtigt Abmeldungen (Opt-out), auch wenn der Identitätsdienst bei der Anmeldung nicht genehmigt wurde. (AN-175259)

## Version 2.11.0

Releasedatum: **11. Februar 2019**

* Die Unterstützung für die neue Funktionalität der Adobe-Opt-in-Dienste in AppMeasurement wurde hinzugefügt. (AN-163546)
* Die Unterstützung zum Speichern von Linktracking-Daten im Sitzungsspeicher wurde hinzugefügt. (AN-162272)
* Der Medien-Streamtyp für Audio Analytics wird nun unterstützt. (AN-173265)

## Version 2.10.0

Releasedatum: **20. September 2018**

Diese Version stellt sicher, dass die AppMeasurement-Bibliothek Cookies für alle Verbindungstypen korrekt sendet.

* AppMeasurement blockiert Cookie-Übertragungen während POST. (AN-165538)
* Unterstützung für XDomainRequest einstellen. (AN-165733)
* Verkürzen Sie die Lebensdauer der standardmäßigen AppMeasurement-Cookies von fünf auf zwei Jahre. (AN-158572)
* Entfernen des Medienmoduls aus dem Code-Manager ( AppMeasurement) (AN-166590)

## Version 2.9.0

Releasedatum: **24. Mai 2018**

>[!NOTE]
>
>Die Besucher-API 3.0 oder höher ist für Kunden erforderlich, die den Experience Cloud ID-Service verwenden. Adobe empfiehlt, ein Upgrade auf die aktuelle Visitor API durchzuführen, wenn die verbundenen Codebibliotheken aktualisiert werden (`at.js`, `AppMeasurement.js` usw.)

* AppMeasurement wurde aktualisiert und verwendet jetzt die aktualisierte Benutzeroberfläche zum Anfordern von IDs. (AN-151483)
* Es wurde ein Problem behoben, durch das nach der Deaktivierung von Linktracking weiterhin ein Linktracking-Cookie erstellt wurde. (AN-156332)
* Es wurde ein Problem behoben, durch das `registerPreTrackCallback` und `registerPostTrackCallback` im Falle von mehrmaligem Aufrufen die Signatur der Rückruffunktion unbrauchbar machten. (AN-158566)

## Version 2.8.2

Releasedatum: **12. April 2018**

* Aktualisieren Sie AppMeasurement , um die aktualisierte Besucherschnittstelle zum Anfordern von IDs zu verwenden. (AN-151483)
* Das Linktracking-Cookie wird weiterhin geschrieben, sobald das Linktracking deaktiviert ist. (AN-156332)
* Verkürzen Sie die Lebensdauer der standardmäßigen AppMeasurement-Cookies von fünf auf zwei Jahre. (AN-158572)

## Version 2.8.1

Releasedatum: **29. März 2018**

Re-Bundle Visitor API 3.1.0 (AN-159524), die folgende Korrekturen beinhaltet: (CORE-11390, CORE-10634)

## Version 2.8.0

Releasedatum: **15. März 2018**

Re-Bundle Visitor API 3.1.0 (AN-159524), die folgende Korrekturen beinhaltet: (CORE-11390, CORE-10634)

* Bundle von VAPI v3.1 mit AppMeasurement v2.8. (AN-158353)
* Umgestalteter Aufbau des Datenerfassungsendpunkts zur Vereinfachung der Freigabe. (AN-156647)
* Fügen Sie AppMeasurement Metriken zum Anforderungs-Roundtrip hinzu. (AN-158343)

## Version 2.7.0

Releasedatum: **18. Januar 2018**

* Die Unterstützung für IE 6 bis 9 wird eingestellt
* Einschließen der Besucher-API v3.0.0
* Aufnahme von DIL 7.00

## Version 2.6.0

Releasedatum: **9. November 2017**

Es wurde ein Problem behoben, bei dem die AppMeasurement-Bibliothek beim Aufruf von s_gl nicht immer die richtige Kontokombination festlegt. (AN-152153)

## Version 2.5.0

Releasedatum: **21. September 2017**

* Einbindung von `dil.js` 6.12 (Audience Manager-Modul)
* Aufnahme der Visitor API 2.5.0.

## Version 2.4.0

Releasedatum: **17. August 2017**

* dil.js v6.11 einschließen
* Die Visitor API 2.4.0 wurde hinzugefügt

## Version 2.3.0

Releasedatum: **20. Juli 2017**

* Fehler behoben, bei dem `s.Util.getQueryParam` `#` erfasst hat
* `dil.js` v6.10 wurde hinzugefügt (AN-145701)

## Version 2.2.0

Releasedatum: **8. Juni 2017**

* Es wurde Unterstützung für die Instanziierungsreihenfolge mehrerer AppMeasurement hinzugefügt. (AN-138237)
* Aufnahme von Version 2.2.0 der Visitor API. (AN-144042)

## Version 2.1.0

Releasedatum: **20. April 2017**

* Die letzte Version von `dil.js` wurde hinzugefügt (AN-140396).
* Der Parameter `adobe_mc_ref`, der die verweisende Stelle der Seite außer Kraft setzt, wird jetzt unterstützt. (AN-131920)
* Neu eingeschlossene Besucher-API 2.1.0. (AN-140873)
* Parameter `mcorgid` hinzugefügt. (AN-139586)
* Der Parameter cp (customerPerspective) wurde hinzugefügt. (AN-140897)

## Version 2.0.0

Releasedatum: **9. März 2017**

* Zu einem neuen Build-Prozess gewechselt, für den eine Aktualisierung der Versionsnummer auf 2.0.0 erforderlich ist. (AN-137878)
* Die mboxMCSDID-Verarbeitung wurde an den richtigen Ort im Abschnitt verschoben, an dem der Tracking-Aufruf erfolgt. (AN-138483)

## Version 1.8.0

Releasedatum: **19. Januar 2017**

* VisitorAPI 2.0.0 einschließen
* Funktionsaufrufe und Prüfungen neu sequenzieren, damit die SDID nach Abschluss der Abbruchprüfung genutzt wird. (AN-134364)
* `s.registerPreTrackCallback`- und `s.registerPostTrackCallback`-Hooks hinzugefügt. (AN-134567)

## Version 1.7.0

Aktualisiert: **11. November 2016**

* Die Visitor API 1.10.1 wurde hinzugefügt.
* Aktualisieren Sie das Audience Manager-Modul mit der Demdex Integration Library (DIL) 6.6. (AN-132065)
* Aufnahme der Visitor API 1.9.0. (AN-132072)
* Aktualisieren des AppMeasurement Audience Manager-Moduls mit DIL 6.5 und zusätzlichen Konfigurationen (AN-129411)
* Aufnahme der Visitor API 1.8.0 (AN-129887)

## Version 1.6.4

Aktualisiert: **18. August 2016**

* AppMeasurement wurde aktualisiert, um AMCV-Cookies zu lesen und zu schreiben. (AN-127098)
* Aufnahme der Visitor API 1.7.0.

>[!NOTE]
>
>Siehe auch die folgenden Versionshinweise für JavaScript Version 1.6.3, die aktualisierte Anforderungen für den Experience Cloud ID-Service enthält.

## Version 1.6.3

Aktualisiert: **4. August 2016**

* Es wurde ein Problem behoben, bei dem AppMeasurement Anfrageverbindungen vorzeitig beendete. (AN-126448)

>[!IMPORTANT]
>
>Version 1.6.0 des Experience Cloud ID-Service *erfordert* AppMeasurement für JavaScript Version 1.6.3 oder höher. Wenn Sie auf Version 1.6.0 des ID-Services von Experience Cloud aktualisieren möchten, stellen Sie sicher, dass Sie AppMeasurement 1.6.3 oder höher verwenden.

## Version 1.6.2

Releasedatum: **21. Juli 2016**

* Aufnahme der Visitor API 1.6.0.
* Es wurde ein Problem behoben, das dazu führte, dass AppMeasurement die falsche verschleierte Methode in der Besucher-API aufrief. (AN-126006)
* Es wurde ein Problem behoben, das den JavaScript-Fehler „Nur Attribut gültig auf v:image&quot; verursachte. (AN-124009)

## Version 1.6.1

Releasedatum: **16. Juni 2016**

* Aufnahme der Visitor API 1.5.7.
* Die Behandlung des Link-Klick-Trackings in Firefox, bei der nicht das vollständige Ereignis gestartet wurde, wurde repariert.

## Version 1.6

Releasedatum: **21. April 2016**

* Das AppMeasurement Activity Map-Modul wurde in das AppMeasurement-Standardmodul integriert, sodass Sie nur auf eine `.js` verweisen müssen. Darüber hinaus ist das Activity Map-Tracking standardmäßig aktiviert. (AN-112689)
* Fehlerkorrektur - Bei der Reihenfolge von Abfragezeichenfolgen-Variablen in AppMeasurement tritt jetzt kein Abschneideproblem mehr auf, sodass *`pageURLRest`* als letztes angezeigt wird. (AN-114647)

## Version 1.5.4

Releasedatum: **17. März 2016**

* Aufnahme der Visitor API 1.5.4
* Unterstützung für Opt-out von der Besucher-API 1.5.4+

## Version 1.5.3

Releasedatum: **21. Januar 2016**

* Fehlerkorrektur - Die Handhabung des Audience Manager-Moduls bei der Verwendung von POSTs zum Tracking von Aufrufen wurde korrigiert. (AN-115381)
* Der Rest der Seiten-URL (“-g„) wurde an das Ende der Abfragezeichenfolge der Tracking-Anfrage verschoben. (AN-114647)

## Version 1.5.2

Releasedatum: **5. November 2015**

* Aufnahme der Visitor API 1.5.3.
* Die Erkennung von IE11 für das URL-Abschneiden 2047 (AN-114914) wurde korrigiert.

## Version 1.5.1

Releasedatum: **17. September 2015**

* Aufnahme der Visitor API 1.5.2
* Das Audience Manager-Modul wurde aktualisiert, um Adobe Audience Manager DIL 6.2 zu verwenden - Kunden-IDs von VisitorAPI.js abzurufen und sie im /event-Aufruf an Adobe Audience Manager zu übergeben. (AN-104978)

## Version 1.5

Releasedatum: **18. Juni 2015**

* Unterstützung für Visitor API 1.5, die die Methode *`getCustomerIDs`* verwendet, um Kunden-IDs und authentifizierte Status zu erfassen und die IDs mit Datenerfassungsanforderungen zu senden.
* Das Erstellen eines doppelten zielangebenden iFrames im **[!UICONTROL AudienceManagement]**-Modul (DIL 6.1) wurde korrigiert
* In Version 1.4.5. beschriebenes, bekanntes Problem behoben.

## Version 1.4.5

Releasedatum: **21. Mai 2015**

* Ab iOS SDK Version 4.5 können Sie mit einer neuen iOS-Erweiterung Nutzungsdaten aus Ihren Apple Watch-Apps, Today-Widgets, Fotobearbeitungs-Widgets und allen anderen iOS-Erweiterungs-Apps erfassen.
* Ab Android SDK Version 4.5 können Sie mit einer neuen Android-Erweiterung Daten aus Ihrer Android Wearable-App erfassen.
* Aufnahme der Visitor API 1.4.
* Das AudienceManagement-Modul wurde auf die Verwendung von DIL Version 6.0 aktualisiert.

>[!NOTE]
>
>**Bekanntes Problem**: Bei den Integrationen mit der Besucher-API und dem AppMeasurement Audience Manager-Modul gibt es zwei iFrame-Anfragen zur Zielveröffentlichung, die in IE6-9 ausgeführt werden: `//fast.<subdomain>.demdex.net/dest5.html` und `//fast.<subdomain>.demdex.net/dest4.html`. Die richtige Einstellung ist – wie in anderen Browsern – nur Folgendes zu laden: `//fast.<subdomain>.demdex.net/dest5.html`.

## Version 1.4.4

Releasedatum: **16. April 2015**

* Sie können nun benutzerdefinierte Kontextdatenvariablen in Lebenszyklusmetriken verwenden.
* Die Aufrufe `trackBeacon` und `clearCurrentBeacon` sind jetzt in PhoneGap verfügbar.
* Fehlerbehebung hinzugefügt, die die Profil-ID des Light-Server-Aufrufs nach dem Aufruf `trackLight` löscht.

## Version 1.4.3

Releasedatum: **19. Februar 2015**

* Die Verarbeitung aller verzögerten Tracking-Aufrufe wurde vereinheitlicht. Dadurch werden Probleme mit während der Verzögerung zurückgestellten Variablen, z. B. dem angeklickten Objekt, behoben.
* Geändert, sodass nach dem ersten Tracking-Aufruf kein automatisches Referrer-Tracking stattfindet. Der zweite, dritte usw. Tracking-Aufruf (in der Regel Linktracking) zählen daher den Referrer nicht doppelt, wenn *`s.referrer`* vor dem ersten Tracking-Aufruf manuell festgelegt wurde.
* Die ZIP-Datei für die Verteilung wurde aktualisiert und enthält nun die Visitor API 1.3.5.

## Version 1.4.2

Releasedatum: **15. Januar 2015**

* Fehlerkorrektur - Die Handhabung der WebKit-Vorabbearbeitung wird jetzt korrigiert, um das Tracking von vorab gerenderten Seiten zu verhindern, die nicht angezeigt werden.
* Die ZIP-Datei für die Verteilung wurde aktualisiert und enthält nun die Visitor API 1.3.4 sowie ein aktualisiertes **[!UICONTROL AudienceManagement]**-Modul mit DIL-Version 5.5.

## Version 1.4.1

Releasedatum: **18. September 2014**

* Es wurde eine `tagContainerMarker`-Variable hinzugefügt, die in der Implementierung die Angabe von bis zu 4 Zeichen ermöglicht. Diese Zeichen werden zusammen mit einer zusätzlichen Gedankenstrich-Zeichenbegrenzung an die Versionszeichenfolge angehängt. Diese Variable wird im dynamischen Tag-Management verwendet.

  ```js
  // JavaScript
  s.tagContainerMarker = "D1.0";
  
  // Data Collection request
  //.../b/ss/myrsid/1/JS-1.4.1-D1.0/s43317392037311?...
  ```

  Die 4 Zeichen sind auf Zeichen beschränkt, die in URL-Dateipfaden zulässig sind, z. B. alphanumerische Zeichen und Punkte.

* Auf Seiten, die mit Dual-Tags mit H-Code versehen sind, wurde eine Schleife behoben, die während des automatischen Linktrackings (Download und Exit) auftreten konnte, wenn das erzwungene Linktracking aktiviert war (standardmäßig in Webkit-Browsern). Darüber hinaus wurde eine allgemeine Sicherheitsmaßnahme zum automatischen Linktracking hinzugefügt, um ähnliche Schleifen zu verhindern. Diese Sicherheitsmaßnahme beschränkt das automatische Linktracking wiederholter Klicks auf *dasselbe* Objekt auf einmal alle 10 Sekunden. Diese Sicherheitsmaßnahme gilt nur für das automatische Linktracking, sodass manuelle Linktracking-Aufrufe (s.tl) nicht beschränkt sind. Klicks auf verschiedene Objekte sind von dieser Sicherheitsmaßnahme ebenfalls nicht betroffen und werden verfolgt.
* Fehlerkorrektur - Die Handhabung angeklickter Objekte ist jetzt problemlos, wenn eine Verzögerung erforderlich ist.
* Es wurde ein Problem behoben, das zu einer doppelten Seitenansichtsanzahl führte, wenn s.t über eine Link-onclick-Funktion aufgerufen wurde und die Besucher-API noch nicht über die erforderlichen Werte verfügte.
* HTTP-POST-Unterstützung.

  >[!IMPORTANT]
  >
  >Damit ein Analytics-Aufruf die `POST` anstelle der `GET` in AppMeasurement verwenden kann (eine Lösungsmethode für [gekürzte URLs in IE](/help/implement/js/troubleshooting.md)), müssen Sie die neueste Implementierung des Visitor ID Service für CX Enterprise verwenden.

## Version 1.4

Releasedatum: **21. August 2014**

* Das Tracking von Browser-Plug-ins (Abfrage-Parameter `p`) wurde entfernt, da Plug-ins in Version 15 nicht mehr gemeldet werden.
* Die Download-Zip-Datei wurde um das **[!UICONTROL AudienceManagement]**-Modul ergänzt.
* Unterstützung für zusätzliche eVars (76 bis 250) und Ereignisse (101 bis 1000) hinzugefügt.

>[!NOTE]
>
>H-Code unterstützt diese zusätzlichen eVars und Ereignisse nicht.

## Version 1.3.2

Releasedatum: **19. Juni 2014**

* Fehlerkorrektur - Die Handhabung von Flags „Fertig“ und „Warten“ für Besucher-API-Felder wie die veraltete Analytics-Besucher-ID wurde korrigiert, was zu Fehlern führte.
* Der Besucher-ID-Dienst 1.3 unterstützt ab sofort neue Funktionen.

## Version 1.3.1

Releasedatum: **22. Mai 2014**

* AppMeasurement für JavaScript `s_gi` hat Instanzen, die mit H-Code `s_gi` erstellt wurden, nicht korrekt gefunden. Beachten Sie, dass dieses Problem nur einige Dual-Tagging-Implementierungen betraf, bei denen sich der AppMeasurement für JavaScript- und H-Code auf derselben Seite mit separaten Instanzen befand und `s_gi` verwendet wurde, um Instanzen nach Report Suite zu finden.

## Version 1.3

Releasedatum: **17. April 2014**

* Unterstützung für den [CX Enterprise Visitor ID-Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de).

## Version 1.2.4

Releasedatum: **13. März 2014**

* Fehlerbehebungen für Heartbeat Video.

## Version 1.2.3

Releasedatum: **20. Februar 2014**

* Fehlerbehebungen für Heartbeat Video.

## Version 1.2.2

Releasedatum: **6. Februar 2014**

* Es wurde ein Kompatibilitätsproblem mit dem Audience Manager DIL-Modul behoben. Audience Manager-Kunden müssen außerdem ein Update auf Version 4.8 des DIL-Moduls durchführen.

## Version 1.2.1

Releasedatum: **15. November 2013**

* Für die Heartbeat-Videomessung verwendete Seitenereignisse korrigiert.

## Version 1.2

Releasedatum: **14. November 2013**

* Unterstützung für [Heartbeat-Videomessungen](https://experienceleague.adobe.com/de/docs/media-analytics/using/media-overview) hinzugefügt.
* `VisitorAPI.js` wurde hinzugefügt, um den [Besucher-ID-Dienst](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de) zu unterstützen.

## Version 1.1.1

* Verhinderte, dass ein Linktracking-Aufruf von Opera-Browsern für Links gesendet wurde, die mit „opera:“ beginnen („opera:“ ähnelt „about:“ und „chrome:“ in anderen Browsern).
* Allen Bildobjekten wurde `alt=""` hinzugefügt, um dem Accessible Video and Communications Act zu entsprechen.

## Version 1.1

Releasedatum: **18. September 2013**

* Problem mit der Unterstützung für das Platzieren des Bibliotheks- und Seiten-Codes im Tag `head` behoben.
* Fehlende Unterstützung für Modul `onLoad` wurde hinzugefügt.

## Version 1.0.3

Releasedatum: **15. August 2013**

* Unterstützung für die Bereitstellung durch Adobe Tag Management wurde hinzugefügt.
* Es wurde ein Problem behoben, das verhinderte, dass Hierarchievariablen im AppMeasurement-Objekt festgelegt wurden.

## Version 1.0.2

Releasedatum: **18. Juli 2013**

* Der Hash/das Fragment wird jetzt von der automatischen Linkverfolgung ignoriert. Zuvor wurde die folgende URL automatisch verfolgt, weil das gesamte `href` auf `.pdf` endete:

  ```js
  <a href="index.htm#anchor.pdf">Test Link</a>
  ```

  Nun werden Hashes/Fragmentbezeichner ignoriert, sodass der Link nur verfolgt wird, wenn der Dateiname mit einer passenden Erweiterung endet.

## Version 1.0.1

Releasedatum: **23. Mai 2013**

Eine neue JavaScript AppMeasurement-Bibliothek ist jetzt im Code-Manager verfügbar. Diese Bibliothek bietet die gleichen Kernfunktionen wie `s_code.js`, ist jedoch schlanker und schneller und kann sowohl für mobile als auch für Desktop-Websites verwendet werden.

* 3-7x schneller als der H.25-Code.
* Nur 21k unkomprimiert und 8k gzip (H.25-Code ist 33k unkomprimiert und 13k gzip).
* Native Unterstützung für das Abrufen von Abfrageparametern, Lesen und Schreiben von Cookies und für das erweiterte Linktracking.
* Klein und schnell genug, um mit mobilen Sites verwendet zu werden, und robust genug, um im gesamten Desktop-Web verwendet zu werden, sodass Sie eine einzige Bibliothek für alle Web-Umgebungen nutzen können.
