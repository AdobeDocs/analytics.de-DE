---
title: Unique Visitors
description: Die Anzahl der eindeutigen Einzelanwender (oder Geräte).
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 87%

---


# Unique Visitors

Die Metrik &quot;Individuelle Besucher&quot;zeigt die Anzahl der Besucher-IDs für das Dimensionselement an. Es handelt sich dabei um eine der am häufigsten verwendeten Metriken zur Bestimmung des Datenverkehrs, da es einen Überblick über die Popularität eines Dimensionselements auf hoher Ebene gibt. Beispielsweise kann ein Besucher einen Monat lang jeden Tag auf Ihre Website kommen. Er zählt aber trotzdem als ein Unique Visitor.

Wenn Sie [geräteübergreifende Analysen](../cda/overview.md) verwenden, wird diese Metrik in „Unique Devices“ umbenannt.

## Unique Visitors pro Tag, Woche, Monat, Quartal und Jahr

Reports &amp; Analytics bietet Optionen für Unique Visitors pro Tag, Woche, Monat, Quartal und Jahr. Anstatt einen Unique Visitor für den gesamten Zeitraum zu zählen, werden Unique Visitor basierend auf der ausgewählten Metrik gezählt. Sie möchten beispielsweise die Unique Visitors pro Tag Ihrer Site anzeigen. Wenn ein Besucher morgens und abends auf Ihre Site kommt, zählt er als ein Unique Visitor pro Tag. Wenn ein Besucher am Montag und erneut am Dienstag auf Ihre Site kommt, zählt er als zwei Unique Visitors pro Tag.

Analysis Workspace behandelt Unique Visitors auf Grundlage der Granularität des Berichts. For example, if you use the [Day](../dimensions/day.md) dimension, you&#39;ll see daily unique visitors for each dimension item. Für den Gesamtwert des Berichts werden jedoch für den Datumsbereich der Freiformtabelle deduplizierte Unique Visitors angezeigt.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der eindeutigen Besucher-IDs für ein bestimmtes Dimensionselement. Sie verwendet mehrere fortschrittliche Mechanismen, um Unique Visitors zu identifizieren, da es mehrere Möglichkeiten gibt, sie zu identifizieren. In der folgenden Tabelle sind die Art und Weise aufgeführt, wie ein Besucher identifiziert wird, sowie deren Priorität. Einige Treffer können über mehrere Methoden zur Besucheridentifizierung verfügen. In diesen Fällen wird die Methode mit der höheren Priorität verwendet.

| Verwendete Reihenfolge | Abfrageparameter (Erfassungsmethode) | Vorhanden, wenn |
| --- | --- | --- |
| 1 | `vid` | Die [`visitorID`](/help/implement/vars/config-vars/visitorid.md)-Variable ist gesetzt. |
| 2 | `aid` | Der Besucher verfügt über ein vorhandenes [`s_vi`](https://docs.adobe.com/content/help/de-DE/core-services/interface/ec-cookies/cookies-analytics.html)-Cookie. Wird bei Implementierungen ohne oder vor der Implementierung des Besucher-Identity Service gesetzt. |
| 3 | `mid` | Der Besucher verfügt über ein vorhandenes [`s_ecid`](https://docs.adobe.com/content/help/de-DE/core-services/interface/ec-cookies/cookies-analytics.html)-Cookie. Wird bei Implementierungen mit dem [Adobe Experience Cloud Identity Service](https://docs.adobe.com/content/help/de-DE/id-service/using/home.html) gesetzt. |
| 4 | `fid` | Besucher hat ein bestehendes [`s_fid`](https://docs.adobe.com/content/help/de-DE/core-services/interface/ec-cookies/cookies-analytics.html)-Cookie, oder wenn `aid` und `mid` aus irgendeinem Grund nicht gesetzt werden konnten. |
| 5 | IP-Adresse, Benutzeragent, Gateway-IP-Adresse | Letztes Mittel, einen Unique Visitor zu identifizieren, wenn der Browser des Besuchers keine Cookies akzeptiert. |

>[!NOTE]
>
>Jede Analytics-Besucher-ID ist einem Profil auf Adobe-Servern zugeordnet. Diese Besucherprofile werden nach einer Inaktivität von mindestens 13 Monaten gelöscht, unabhängig vom Ablauf der Besucher-ID-Cookies.

## Verhalten, das sich auf die Anzahl der Unique Visitors auswirkt

Unique Visitor-IDs werden in der Regel in einem Browser-Cookie gespeichert. Ein neuer Unique Visitor wird gezählt, wenn er eine der folgenden Aktionen ausführt:

* Löscht seinen Cache zu einem beliebigen Zeitpunkt.
* Öffnet einen anderen Browser auf demselben Computer. Pro Browser wird ein Unique Visitor gezählt.
* Derselbe Benutzer surft auf verschiedenen Geräten auf Ihrer Site. Pro Gerät wird ein Unique Visitor gezählt. Sie können [geräteübergreifende Analysen](../cda/overview.md) verwenden, um Besucher mithilfe der Metrik [Personen](people.md) zusammenzufassen.
* Öffnet eine private Browser-Sitzung (z. B. Registerkarte „Inkognito“ in Chrome).

Solange die Cookie-ID beibehalten wird, wird *kein* neuer Unique Visitor gezählt:

* Schließt den Browser für einen längeren Zeitraum.
* Aktualisiert den Browser auf die neueste Version.
