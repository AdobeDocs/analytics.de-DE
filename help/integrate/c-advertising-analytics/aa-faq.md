---
description: Häufig gestellte Fragen zu Advertising Analytics.
title: Häufig gestellte Fragen zu Advertising Analytics
feature: Advertising Analytics
exl-id: 664a5641-1c79-439f-a9fb-2ff134574412
source-git-commit: 02b6c4f4504785353f9b2457099d3332cd25a852
workflow-type: tm+mt
source-wordcount: '1300'
ht-degree: 36%

---

# Häufig gestellte Fragen

## Zugriff/Berechtigungen {#access}

+++ Muss ich Adobe Advertising Cloud- oder Adobe Advertising Cloud (AMO)-Kunde sein, um auf diese Funktion zugreifen zu können?

Nein, diese Funktion ist für Kunden verfügbar, die nicht Advertising Cloud oder AMO sind.

AMO-Kunden können die bestehende Analytics-AMO-Integration nutzen, jedoch nicht Advertising Analytics verwenden.

+++

+++ Welche Adobe Analytics-SKUs berechtigen Sie zur Verwendung von Advertising Analytics?

Advertising Analytics ist für Adobe Analytics verfügbar

* [Auswählen](https://www.adobe.com/de/data-analytics-cloud/analytics/select.html)

* [Prime](https://www.adobe.com/de/data-analytics-cloud/analytics/prime.html)

* [Ultimate](https://www.adobe.com/de/data-analytics-cloud/analytics/ultimate.html)

+++

+++ Muss ich für die Nutzung von Advertising Analytics extra bezahlen?

Nein, außerhalb der ordnungsgemäßen SKU-Bereitstellung fallen für Advertising Analytics keine zusätzlichen Kosten an.

+++

+++ Zählt Advertising Analytics für meine Nutzung der Server-Aufrufe?

Nein, Advertising Analytics verwendet einen speziellen Datenquellentyp, der keine Kosten für Server-Aufrufe verursacht.

+++

+++ Kann ich die Advertising Analytics-Funktion verwenden, wenn ich bereits Advertising Cloud/AMO verwende?

Jedes kompatible Suchmaschinenkonto wird an Advertising Analytics übergeben und als schreibgeschützt angezeigt. Sämtliche Bearbeitungen oder Aktualisierungen müssen in Advertising Cloud/AMO vorgenommen werden.

+++

+++ Ich besitze die richtige SKU, kann aber nicht auf Advertising Analytics zugreifen. Warum ist das so?

Advertising Analytics ist nur für Adobe Analytics-Administratoren verfügbar. Administratoren können jedoch Benutzern ohne Administratorrechte Zugriff gewähren. Wenden Sie sich also an Ihren Administrator, um Zugriffsrechte zu erhalten.

+++

## Verwenden von Advertising Analytics {#using}

+++ Welche Suchmaschinenkonten sind in Advertising Analytics enthalten?

Zu den Suchmaschinenkonten gehören Google AdWords und Microsoft Bing.

+++

+++ Wo greife ich auf Advertising Analytics zu?

Navigieren Sie nach der Anmeldung bei Adobe Analytics zu [!UICONTROL Admin]. Wählen Sie dann [!UICONTROL Advertising Analytics] aus, um Ihre Suchmaschinenkonten hinzuzufügen.

+++

+++ Wie werden die Daten erfasst und an Analytics weitergegeben?

Advertising Analytics verwendet eine Reihe benutzerdefinierter APIs, um Daten von Suchmaschinen über die Adobe Advertising Cloud an Analytics zu übergeben.

+++

+++ Welche Suchdaten erhalte ich mit dieser Integration?

Sie erhalten

* Impressions
* Klicks
* Kosten
* Qualitätsbewertung
* Durchschnittliche Position direkt aus den Suchmaschinen sowie
* AMO ID-Instanzen (Klickinstanzen).

+++

+++ Kann ich meine Advertising Analytics-Daten nach anderen Analytics-Daten (Metriken/Dimensionen) aufschlüsseln?

Nein, die Rohsuchdaten werden als unabhängiger Datensatz angezeigt. Es gibt jedoch eine Instanzenversion der Klickdaten, die nach anderen Analytics-Daten aufgeschlüsselt werden kann.

+++ Wie sind die verschiedenen Statusindikatoren für meine Konten definiert (ausstehend, aktiv, angehalten usw.)? Jeder dieser Statusindikatoren identifiziert die Lebenszyklusphase jedes Suchmaschinenkontos.

* [!UICONTROL Ausstehend]
* [!UICONTROL Angehalten] bedeutet, dass das Konto zuvor eingerichtet wurde, aber inaktiv ist.
* [!UICONTROL Aktiv] bedeutet, dass das Konto vollständig eingerichtet wurde und Suchdaten abruft.

+++

+++ Ich versuche, meine Advertising Analytics-Konten einer bestimmten Report Suite zuzuordnen, aber dies ist nicht im Report Suite-Modal verfügbar. Warum?

Bevor Sie eine Report Suite einem Advertising Analytics-Konto zuweisen können, muss die gewünschte Report Suite bereitgestellt [für Advertising Analytics-Berichte](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-provision-rs.md)
Dies erfolgt über eine separate Admin-Seite, auf die über Admin > Report Suites > `[select report suite]` > Einstellungen bearbeiten > Advertising Analytics-Konfiguration zugegriffen werden kann.

+++

+++ Ist es möglich, einem Advertising Analytics-Konto eine Virtual Report Suite zuzuweisen?

Virtual Report Suites erfassen keine Daten, sodass Sie ein Advertising Analytics-Konto nicht direkt einer Virtual Report Suite zuordnen können. Sie können jedoch das Advertising Analytics-Konto der übergeordneten Report Suite der Virtual Report Suite zuordnen, in der Daten angezeigt werden sollen. Die Suchmaschinenmetriken (Klick/Kosten/Impressions) werden möglicherweise nicht in der Virtual Report Suite angezeigt, es sei denn, Sie fügen eine „oder“-Bedingung basierend auf der AMO-ID (oder ihrer Klassifizierung) in Ihre Segmentlogik ein. Beispiel: Durch das Hinzufügen von „alle Treffer, bei denen eine AMO-ID existiert“ werden die Suchmaschinenmetriken in das Segment aufgenommen.

+++

+++ Sind Advertising Analytics-Metriken im Bericht *Marketing-Kanäle* zu melden?

Nein, sie sind nicht im Bericht Marketing-Kanäle enthalten.

+++

+++ F: Wann werden die Suchdaten in Analytics abgerufen?

A: Die Suchdaten werden um ca. 6:00 Uhr in der Zeitzone Ihres Analytics-Rechenzentrums von den Suchmaschinen abgerufen. Zu diesem Zeitpunkt werden die AMO-Daten erfasst und in die Report Suite eingefügt. Diese Daten werden dann im Rahmen ihrer Einfügung in Analytics in die Report Suite-Zeitzonen umgewandelt.

+++

+++ Was kann *vor dem Klick erfasst*? Werden Impressionen, Kosten, durchschnittliche Position usw. auch ohne Klick erfasst?

Die AMO-ID erfasst die Suchmaschinenmetriken: Impressionen, Kosten, Klicks, durchschnittliche Position und durchschnittliche Qualitätsbewertung. Sind keine Klicks aber Impressionen vorhanden, werden die Daten zu Impression/Position/Qualität dennoch an Analytics gesendet. In der Regel entstehen keine Kosten, wenn keine Klicks vorhanden sind.

+++

+++ Auf welcher Ebene werden diese Daten erfasst? *Besucher? Treffer?*

Die Suchmaschinenmetriken werden auf Trefferebene erfasst und mit der AMO ID (und deren Klassifizierungen) verbunden. Dabei handelt es sich um Daten der Zusammenfassungsebene, die nicht mit Besuchen/Besuchern verbunden sind. Daher können die Suchmaschinen-Metriken nur in Segmenten verwendet werden, die sich im Umfang der Trefferebene befinden und die auf der AMO-ID (oder zugehörigen Klassifizierungen) basieren.

Die AMO-ID wird auch auf der Landingpage im Treffer für die betreffende Seite (über die die Verbindung zum Besuch/Besucher hergestellt wird) erfasst. Sie bleibt in der absteigenden Hierarchie bestehen, um für andere Analytics-Metriken berücksichtigt zu werden (bis sie abläuft oder durch eine neue AMO-ID überschrieben wird). Sie ist wie jede andere eVar vollständig in den Datensatz integriert.

+++

+++ google.com Erfassen wir auch nur *oder Länderversionen* (wie google.co.uk, google.it, google.fr oder google.de)?

Die Anzeigenplattform-Klassifizierung erfasst diese Werte: &quot;Google AdWords“ und „Bing Ads“. Als gängige Best Practice sollte der Ländercode bei der Benennung der Kampagnen eingefügt werden. Anschließend können Sie detaillierter filtern oder eine Segmentierung vornehmen (Beispiel: Wenn alle Kampagnen mit „ländercode_“ beginnen, würden Sie durch die Erstellung eines Segments, in dem die Kampagnen (AMO-ID) mit „UK_“ beginnen, nur Daten für Großbritannien erhalten).

+++

+++ Die Metrik „AMO-Kosten“ entspricht den von der Suchmaschine für jedes Keyword/jede Anzeige angegebenen Kosten. Handelt es sich hierbei um Netto- oder Bruttokosten?

„AMO-Kosten“ sind nur die Kosten, die an die Suchmaschinen gezahlt werden. Sie enthalten keinerlei Gebühren für Agenturen oder Suchoptimierungs-/Verwaltungsplattformen.

+++

+++ Gibt es Pläne, andere Werbekanäle wie *Display* oder *Social* einzubeziehen?

Nein, derzeit haben wir keine Pläne für diese anderen Kanäle auf der Roadmap.

+++


## Automatisches Tracking im Vergleich zu manuellem Tracking {#section_7437C4698A6D482EB7ED94A948390119}

+++ Bei der Einrichtung meines Advertising-Kontos wird angegeben, dass *automatisches Tracking* zu unbeabsichtigten Folgen führen kann. Welche Art von Folgen sind hier gemeint?

Im Auto-Modus wird versucht, URL-Parameter im korrekten Format an das Ende der Tracking-Vorlagen/Ziel-URLs anzuhängen. Sie müssen jedoch sicherstellen, dass die hinzugefügten URL-Parameter ordnungsgemäß auf der endgültigen Landingpage bestehen bleiben. Der Auto-Modus kann Keywords in die Landing-URL einfügen, die möglicherweise Sonderzeichen enthalten, die Ihr Webserver nicht unterstützt.

+++

+++ Kann ich, wenn ich das manuelle oder automatische Tracking anfänglich eingerichtet habe, später in den anderen Tracking-Modus wechseln? Was sind die Auswirkungen?

Ja, Sie können Tracking-Modi wechseln, aber Sie müssen die alte Tracking-Logik entfernen, bevor Sie den Wechsel vornehmen. Dies kann zu Ausfallzeiten beim Tracking am Tag des Wechsels führen (insbesondere beim Wechsel vom manuellen zum automatischen Tracking). Daher empfehlen wir, nur dann zu wechseln, wenn dies unbedingt erforderlich ist.

* Wechseln von Manuell zu Automatisch: Entfernen Sie die manuellen Ergänzungen der Tracking-Vorlagen und wechseln Sie dann in der Advertising Analytics-Benutzeroberfläche den Umschalter von Manuell zu Automatisch und speichern Sie die Einstellung. Beachten Sie, dass es mehrere Stunden dauern kann, bis das System die automatischen Trackingcodes ausfüllt.

* Wechseln von „Automatisch“ zu „Manuell“: Aktualisieren Sie den Umschalter von „Manuell“ zu „Automatisch“ in der Advertising Analytics-Setup-Benutzeroberfläche und stellen Sie dann die manuellen Trackingcodes so schnell wie möglich bereit. Wenn Sie während der Bereitstellung der manuellen Trackingcodes die automatischen Trackingcodes in den Tracking-Vorlagen der Suchmaschine sehen, entfernen Sie sie.

+++
