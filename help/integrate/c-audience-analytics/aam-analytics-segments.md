---
description: Sowohl Analytics als auch der Audience Manager verwenden Segmente. Jedoch ist ein Segment in Analytics nicht dasselbe wie ein Segment in Audience Manager. Diese Unterschiede tragen zu einem Teil der Diskrepanzen bei, die bei Ihren Berichten von Analytics und Audience Manager auftreten. Aus diesem Grund ist es wichtig und hilfreich, diese Unterschiede zu verstehen, wenn Sie mit der Arbeit mit Segmenten in den beiden Lösungen beginnen.
seo-description: Sowohl Analytics als auch der Audience Manager verwenden Segmente. Jedoch ist ein Segment in Analytics nicht dasselbe wie ein Segment in Audience Manager. Diese Unterschiede tragen zu einem Teil der Diskrepanzen bei, die bei Ihren Berichten von Analytics und Audience Manager auftreten. Aus diesem Grund ist es wichtig und hilfreich, diese Unterschiede zu verstehen, wenn Sie mit der Arbeit mit Segmenten in den beiden Lösungen beginnen.
seo-title: Segmente in Analytics und Audience Manager – Grundlagen
title: Segmente in Analytics und Audience Manager – Grundlagen
uuid: 13f7d1d7-6a3f-42f1-822e-8d3523999efa
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Segmente in Analytics und Audience Manager – Grundlagen

Sowohl Analytics als auch der Audience Manager verwenden Segmente. Jedoch ist ein Segment in Analytics nicht dasselbe wie ein Segment in Audience Manager. Diese Unterschiede tragen zu einem Teil der Diskrepanzen bei, die bei Ihren Berichten von Analytics und Audience Manager auftreten. Aus diesem Grund ist es wichtig und hilfreich, diese Unterschiede zu verstehen, wenn Sie mit der Arbeit mit Segmenten in den beiden Lösungen beginnen.

## Audience Manager-Segmente {#section_417DC4B5648547778A27E42CE1D09900}

Ein Audience Manager-Segment ist eine Gruppe von Besuchern (Benutzer-IDs), die sich für einen Satz festgelegter Eigenschaften qualifizieren, welche durch logische Regeln verbunden sind. Es gibt vier Kriterien, die bestimmen, ob ein Besucher (Benutzer-ID) Teil eines Segments in Audience Manager ist:

* Regeln, die für die Segmente selbst und die Eigenschaften, aus denen die einzelnen Segmente bestehen, festgelegt wurden. Diese Regeln legen die Bedingungen fest, die eine Benutzer-ID erfüllen oder vorweisen muss, um sich für ein Segment zu qualifizieren.
* Algorithmische Modellierung. Unter Umständen qualifizieren sich Benutzer, die sich für ein bestimmtes Segment qualifizieren, basierend auf der algorithmischen Modellierung und Analyse auch für andere Segmente.
* Time-to-live-Intervalle (TTL). Die Mitgliedschaft in einem Segment kann nach einem festgelegten Intervall ablaufen oder auf unbestimmte Zeit fortgeführt werden.
* Neuigkeit und Häufigkeit. Festzulegen, wann und wie häufig Interaktionen (Eigenschaftsumsetzungen) bei Benutzern auftreten, kann dabei helfen, Segmente basierend auf dem tatsächlichen (oder wahrgenommenen) Interesse an einer Seite, einem Abschnitt oder einem bestimmten kreativen Element zu erstellen.

Bei Audience Manager-Segmenten ist die Zugehörigkeit fließend. Je nachdem, ob sie die Segmentkriterien zu einem bestimmten Zeitpunkt erfüllen, können Benutzer Teil eines Segments werden oder daraus ausscheiden. Das bedeutet, dass sich die Population eines Audience Manager-Segments mit der Zeit vergrößern oder verkleinern kann.

Ein Audience Manager-Segment wird in Analytics als Zielgruppe berechnet.

Weitere Informationen finden Sie unter [Populationsdaten für Eigenschaften und Segmente im Segmentaufbau](https://marketing.adobe.com/resources/help/en_US/aam/segment-builder-data.html) und [Signale, Eigenschaften und Segmente](https://marketing.adobe.com/resources/help/en_US/aam/c_signal_trait_segment.html).

## Analytics-Segmente {#section_62EC584BB7134E10923BCBA7F9BD89A8}

Ein Analytics-Segment ist ein Filtermechanismus für Daten in Ihren Berichten. Die Filterung kann auf Besucher-, Besuchs- oder Trefferebene erfolgen - und nicht ausschließlich auf Besucherebene wie in Audience Manager. Es müssen verschiedene wichtige Faktoren bedacht werden, wenn ein Analytics-Segment mit einem Audience Manager-Segment verglichen wird:

* Analytics-Segmente stützen sich auf einen anderen Datensatz als Audience Manager-Segmente. Während der Datenerfassung wendet Analytics viele verschiedene Nachbearbeitungsschritte auf die Daten an, die Audience Manager nicht zur Verfügung stehen. Die Nachbearbeitung kann unter anderem die eVar-Speicherung, Verarbeitungsregeln, Suchbegriffe (Geo-Standort, Mobilgerät) und VISTA umfassen. Audience Manager erhält über die serverseitige Weiterleitung (oder DIL) bereits vorverarbeitete Daten.

   Häufige Diskrepanzen bei den Daten treten auf, wenn Segmente, die auf Dimensionen basieren, die in Analytics niemals ablaufen, mit derselben Dimension in Audience Manager verglichen werden. Zum Beispiel listVars oder Merchandising eVars, die niemals ablaufen.

   Wenn z. B. eVar = blau ist und in Analytics nie ablaufen soll, wird dieser Besucher in jedem Segment in Analytics mit den Kriterien "eVar = blau"immer einbezogen. Im Gegensatz dazu könnte dieser Besucher nach einem festgelegten Zeitraum aus einem ähnlich definierten Segment in Audience Manager ausscheiden.

* Analytics-Segmente bieten mehr Funktionen als AAM-Segmente. Audience Manager-Segmente werden immer auf der Besucherebene ausgewertet. Analytics-Segmente können auf Besucher-, Besuchs- oder Trefferebene (oder einer Kombination dieser Ebenen) definiert werden. Darüber hinaus unterstützt Analytics erweiterte Segmentierungsfähigkeiten, die es im Audience Manager nicht gibt, beispielsweise die sequenzielle Segmentierung.
* Je nachdem, ob sie die Segmentkriterien zu einem bestimmten Zeitpunkt erfüllen, können Audience Manager-Besucher wie erwähnt Teil eines Segments werden oder daraus ausscheiden.

   Im Gegensatz dazu werden Besucher in Analytics basierend auf dem Datumsbereich für die Berichterstellung zu Segmenten hinzugefügt oder daraus entfernt. Ein Beispiel: Ein einzelner Besucher hat im vergangenen Monat einen Kauf getätigt. In AAM würde dieser Besucher unabhängig vom Datumsbereich in ein Segment "Käufer"einbezogen. In Analytics wäre der Besucher bei einem auf diesem Monat basierenden Bericht nicht im Segment enthalten. Allerdings wäre der Besucher bei einem auf diesem und dem vergangenen Monat basierenden Bericht im Segment enthalten.

Weitere Informationen finden Sie im [Analytics-Segmentierungsleitfaden](https://marketing.adobe.com/resources/help/en_US/analytics/segment/).
