---
description: Häufig gestellte Fragen zu Advertising Analytics.
title: Häufig gestellte Fragen zu Advertising Analytics
feature: Advertising Analytics
exl-id: 664a5641-1c79-439f-a9fb-2ff134574412
TQID: https://experienceleague.adobe.com/HC9F-en-nLFRkxsaY6Szdtb3jR5NgdpsbjSAX6kTBlQ
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: a9364d69-0c51-44bf-8b5f-6d99c04493b8id: c80b99d6-98b9-4aeb-b5c4-933ef2ef705c
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c2296997-5d79-4905-b32e-99b5aa892429id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 1298
ht-degree: 11%

---

# Häufig gestellte Fragen

## Zugriff/Berechtigungen {#access}

+++ Muss ich Adobe Advertising-Kunde sein, um auf diese Funktion zugreifen zu können?

Nein, diese Funktion ist für Kunden verfügbar, die nicht Advertising sind. Adobe Advertising-Kunden können die vorhandene Analytics- und Advertising-Integration nutzen.

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

+++ Kann ich, wenn ich bereits Adobe Advertising verwende, trotzdem die Advertising Analytics-Funktion verwenden?

Jedes kompatible Suchmaschinenkonto wird an Advertising Analytics übergeben und als schreibgeschützt angezeigt. Alle Bearbeitungen oder Aktualisierungen sollten in Advertising vorgenommen werden.

+++

+++ Ich besitze die richtige SKU, kann aber nicht auf Advertising Analytics zugreifen. Warum ist das so? 

Advertising Analytics ist nur für Adobe Analytics-Administratoren verfügbar. Administratoren können jedoch Benutzern ohne Administratorrechte Zugriff gewähren. Wenden Sie sich an Ihren Administrator, um Zugriffsrechte zu erhalten.

+++

## Verwenden von Advertising Analytics {#using}

+++ Welche Suchmaschinenkonten sind in Advertising Analytics enthalten?

Zu den Suchmaschinenkonten gehören Google Ads und Microsoft Advertising.

+++

+++ Wo greife ich auf Advertising Analytics zu?

Navigieren Sie nach der Anmeldung bei Adobe Analytics zu [!UICONTROL Admin]. Wählen Sie dann [!UICONTROL Advertising Analytics] aus, um Ihre Suchmaschinenkonten hinzuzufügen.

+++

+++ Wie werden die Daten erfasst und an Analytics weitergegeben? 

Advertising Analytics verwendet eine Reihe benutzerdefinierter APIs, um Daten von Suchmaschinen über Adobe Advertising an Adobe Analytics zu übergeben.

+++

+++ Welche Suchdaten erhalte ich mit dieser Integration? 

Sie erhalten:

* Impressionen
* Klicks
* Kosten
* Qualitätsbewertung
* Durchschnittliche Position direkt aus den Suchmaschinen
* AMO ID-Instanzen (Klickinstanzen)

+++

+++ Kann ich meine Advertising Analytics-Daten nach anderen Analytics-Daten (Metriken/Dimensionen) aufschlüsseln? 

Nein, die Rohsuchdaten werden als unabhängiger Datensatz angezeigt. Es gibt jedoch eine Instanzversion der Klickdaten, die von anderen Analytics-Daten aufgeschlüsselt werden kann.

+++

+++ Wie sind die verschiedenen Statusindikatoren für meine Konten definiert (ausstehend, aktiv, angehalten usw.)? Jeder dieser Statusindikatoren identifiziert die Lebenszyklusphase jedes Suchmaschinenkontos. 

* [!UICONTROL Ausstehend]
* [!UICONTROL Ausgesetzt] bedeutet, dass das Konto zuvor eingerichtet wurde, sich jedoch in einem inaktiven Status befindet.
* [!UICONTROL Aktiv] bedeutet, dass das Konto vollständig eingerichtet wurde und Suchdaten abruft.

+++

+++ Ich versuche, meine Advertising Analytics-Konten einer bestimmten Report Suite zuzuordnen, aber dies ist nicht im Report Suite-Modal verfügbar. Warum? 

Bevor Sie eine Report Suite einem Advertising Analytics-Konto zuweisen können, muss die gewünschte Report Suite [ Advertising Analytics-Reporting bereitgestellt werden](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-provision-rs.md)
Dies erfolgt über eine separate Admin-Seite, auf die über Admin > Report Suites > `[select report suite]` > Einstellungen bearbeiten > Advertising Analytics-Konfiguration zugegriffen werden kann.

+++

+++ Ist es möglich, einem Advertising Analytics-Konto eine Virtual Report Suite zuzuweisen? 

Virtual Report Suites erfassen keine Daten, sodass Sie ein Advertising Analytics-Konto nicht direkt einer Virtual Report Suite zuordnen können. Sie können jedoch das Advertising Analytics-Konto der übergeordneten Report Suite der Virtual Report Suite zuordnen, in der Daten angezeigt werden sollen. Die Suchmaschinenmetriken (Klick/Kosten/Impressions) werden möglicherweise nicht in der Virtual Report Suite angezeigt, es sei denn, Sie fügen eine „oder“-Bedingung basierend auf der AMO-ID (oder ihrer Klassifizierung) in Ihre Segmentlogik ein. Beispiel: Durch das Hinzufügen von „alle Treffer, bei denen eine AMO-ID existiert“ werden die Suchmaschinenmetriken in das Segment aufgenommen.

+++

+++ Sind Advertising Analytics-Metriken im Bericht *Marketing-Kanäle* zu melden? 

Nein, sie sind nicht im Bericht Marketing-Kanäle enthalten.

+++

+++ Wann werden die Suchdaten in Analytics übernommen? 

Die Suchdaten werden um ca. 6:06 Uhr :00 in der Zeitzone Ihres Analytics-Rechenzentrums von den Suchmaschinen abgerufen. Zu diesem Zeitpunkt werden die AMO-Daten erfasst und in die Report Suite eingefügt. Diese Daten werden dann im Rahmen ihrer Einfügung in Analytics in die Report Suite-Zeitzonen umgewandelt.

+++

+++ Was kann *vor dem Klick erfasst*? Bringen wir auch ohne Klick Impressionen, Kosten, durchschnittliche Position usw. mit?

Die AMO-ID erfasst die Suchmaschinenmetriken: Impressionen, Kosten, Klicks, durchschnittliche Position und durchschnittliche Qualitätsbewertung. Wenn keine Klicks, aber Impressionen vorhanden sind, werden die Impressions-/Positions-/Qualitätsbewertungsdaten weiterhin an Analytics gesendet. In der Regel fallen auch keine Kosten an, wenn keine Klicks erfolgen.

+++

+++ Auf welcher Ebene werden diese Daten erfasst? *Besucher? Treffer?* 

Die Suchmaschinenmetriken werden auf Trefferebene erfasst und mit der AMO ID (und deren Klassifizierungen) verbunden. Es handelt sich um Daten auf Zusammenfassungsebene, die nicht mit Besuchen/Besuchern verbunden sind. Daher können Suchmaschinenmetriken nur in Segmenten verwendet werden, die im Bereich der Trefferebene liegen und auf der AMO-ID (oder ihren Klassifizierungen) basieren.

Die AMO ID wird auch auf der Landingpage im Treffer für diese Seite erfasst (wodurch sie mit dem Besuch/Besucher verbunden wird) und bleibt nachgelagert bestehen, um Gutschriften für andere Analytics-Metriken zu erhalten (bis sie abläuft oder durch eine neue AMO ID überschrieben wird). Sie ist wie jede andere eVar vollständig in den Datensatz integriert.

+++

+++ google.com Erfassen wir auch nur *oder Länderversionen* (wie google.co.uk, google.it, google.fr oder google.de)? 

Die Anzeigenplattform-Klassifizierung erfasst diese Werte: &quot;Google AdWords“ und „Bing Ads“. Als gängige Best Practice sollte der Ländercode bei der Benennung der Kampagnen eingefügt werden. Anschließend können Sie detaillierter filtern oder eine Segmentierung vornehmen (Beispiel: Wenn alle Kampagnen mit „ländercode_“ beginnen, würden Sie durch die Erstellung eines Segments, in dem die Kampagnen (AMO-ID) mit „UK_“ beginnen, nur Daten für Großbritannien erhalten).

+++

+++ Die Metrik „AMO-Kosten“ entspricht den von der Suchmaschine für jedes Keyword/jede Anzeige angegebenen Kosten. Sind dies Nettokosten oder Bruttokosten? 

„AMO-Kosten“ sind nur die Kosten, die an die Suchmaschinen gezahlt werden. Es sind keine Gebühren für Agenturen oder Suchoptimierungs-/Verwaltungsplattformen enthalten.

+++

+++ Gibt es Pläne, andere Werbekanäle wie *Display* oder *Social* einzubeziehen? 

Nein, derzeit haben wir keine Pläne für diese anderen Kanäle auf der Roadmap.

+++


## Automatisches Tracking im Vergleich zu manuellem Tracking {#section_7437C4698A6D482EB7ED94A948390119}

+++ Bei der Einrichtung meines Advertising-Kontos wird angegeben, dass *automatisches Tracking* zu unbeabsichtigten Folgen führen kann. Welche Folgen können auftreten? 

Im Auto-Modus wird versucht, URL-Parameter im korrekten Format an das Ende der Tracking-Vorlagen/Ziel-URLs anzuhängen. Sie müssen jedoch sicherstellen, dass die hinzugefügten URL-Parameter ordnungsgemäß auf der endgültigen Landingpage bestehen bleiben. Der Auto-Modus kann Schlüsselwörter in die Ziel-URL einfügen, und Ihr Webserver unterstützt möglicherweise keine Schlüsselwörter mit Sonderzeichen.

+++

+++ Kann ich, wenn ich das manuelle oder automatische Tracking anfänglich eingerichtet habe, später in den anderen Tracking-Modus wechseln? Was sind die Implikationen? 

Ja, Sie können Tracking-Modi wechseln, aber Sie müssen die alte Tracking-Logik entfernen, bevor Sie den Wechsel vornehmen. Dies kann am Tag des Wechsels zu Ausfallzeiten des Trackings führen (insbesondere beim Wechsel von manuell zu automatisch). Daher empfehlen wir, nur dann zu wechseln, wenn dies unbedingt erforderlich ist.

* Wechseln von Manuell zu Automatisch: Entfernen Sie die manuellen Ergänzungen der Tracking-Vorlagen und wechseln Sie dann in der Advertising Analytics-Benutzeroberfläche den Umschalter von Manuell zu Automatisch und speichern Sie die Einstellung. Beachten Sie, dass es mehrere Stunden dauern kann, bis das System die automatischen Trackingcodes ausfüllt.

* Wechseln von „Automatisch“ zu „Manuell“: Aktualisieren Sie den Umschalter von „Manuell“ zu „Automatisch“ in der Advertising Analytics-Setup-Benutzeroberfläche und stellen Sie dann die manuellen Trackingcodes so schnell wie möglich bereit. Wenn Sie bei der Bereitstellung der manuellen Trackingcodes die automatischen Trackingcodes in den Suchmaschinen-Trackingvorlagen sehen, entfernen Sie diese.

+++
