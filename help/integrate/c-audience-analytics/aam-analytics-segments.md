---
description: Analytics und Audience Manager verwenden beide Segmente. Ein Analytics-Segment ist jedoch nicht genau dasselbe wie ein Audience Manager-Segment. Diese Unterschiede führen teilweise zu den Diskrepanzen, die Sie in Ihren Analytics- und Audience Manager-Berichten sehen werden. Daher ist es wichtig und nützlich, diese Unterschiede zu verstehen, wenn Sie mit Segmenten in beiden Lösungen arbeiten.
title: Segmente in Analytics und Audience Manager – Grundlagen
feature: Audience Analytics
exl-id: 2bc662e7-7552-41e1-9d4a-bc7aa81b8c1d
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 10%

---

# Segmente in Analytics und Audience Manager – Grundlagen

Analytics und Audience Manager verwenden beide Segmente. Ein Analytics-Segment ist jedoch nicht genau dasselbe wie ein Audience Manager-Segment. Diese Unterschiede führen teilweise zu den Diskrepanzen, die Sie in Ihren Analytics- und Audience Manager-Berichten sehen werden. Daher ist es wichtig und nützlich, diese Unterschiede zu verstehen, wenn Sie mit Segmenten in beiden Lösungen arbeiten.

## Audience Manager-Segmente {#aam-segments}

Ein Audience Manager-Segment ist eine Besuchergruppe (Benutzer-IDs), die für einen Satz definierter Eigenschaften qualifiziert sind, die durch logische Regeln verbunden werden. Es gibt vier Kriterien, die bestimmen, ob eine Besucherin oder ein Besucher (Benutzer-ID) Teil eines Segments in Audience Manager ist:

* Regeln werden für die Segmente selbst und die Eigenschaften festgelegt, aus denen die einzelnen Segmente bestehen. Diese Regeln definieren die Bedingungen, die eine Benutzer-ID erfüllen oder anzeigen muss, um für ein Segment qualifiziert zu sein.
* Algorithmische Modellierung. Benutzer, die sich für ein bestimmtes Segment qualifizieren, können sich auf der Grundlage algorithmischer Modellierung und Analyse für andere Segmente qualifizieren.
* TTL-Intervalle (Time-to-Live). Die Segmentzugehörigkeit kann nach einem festgelegten Intervall ablaufen oder unbegrenzt fortgesetzt werden.
* Neuigkeit und Häufigkeit. Wenn Sie definieren, wann und wie oft Benutzende interagieren (Eigenschaftenrealisierung), können Sie Segmente erstellen, die auf der tatsächlichen (oder wahrgenommenen) Ebene des Interesses an einer Site, einem Bereich oder einem bestimmten kreativen Element basieren.

Bei Audience Manager-Segmenten ist die Zugehörigkeit fließend. Benutzende können ein Segment eingeben oder es verlassen, je nachdem, ob sie zum aktuellen Zeitpunkt für die Segmentkriterien qualifiziert sind. Dies bedeutet, dass die Population eines Audience Manager-Segments im Laufe der Zeit zunehmen oder abnehmen kann.

Ein Audience Manager-Segment wird in Analytics als Zielgruppe gekennzeichnet.

Weitere Informationen finden Sie unter [Daten zu Eigenschaften und Segmentpopulation in Segment Builder](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder-data.html?lang=de) und [Signale, Eigenschaften und Segmente](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html?lang=de).

## Analytics-Segmente {#analytics-segments}

Ein Analytics-Segment ist ein Filtermechanismus für Daten in Ihren Berichten. Das Filtern kann sich auf den Besucher, den Besuch oder die Trefferebene beziehen – und nicht nur strikt auf die Besucherebene wie im Audience Manager. Beim Vergleich eines Analytics-Segments mit einem Audience Manager-Segment sind verschiedene wichtige Faktoren zu berücksichtigen:

* Analytics-Segmente verwenden einen anderen Datensatz als Audience Manager-Segmente. Bei der Datenerfassung wendet Analytics viele verschiedene Nachbearbeitungsschritte auf die Daten an, die für Audience Manager nicht verfügbar sind. Die Nachbearbeitung kann eVar-Persistenz, Verarbeitungsregeln, Suchen (Geografie, Mobilgerät), VISTA und viele andere umfassen. Audience Manager empfängt vorverarbeitete Daten über die Server-seitige Weiterleitung (oder DIL).

  Häufig auftretende Datendiskrepanzen treten auf, wenn Segmente auf der Grundlage von Dimensionen, die in Analytics nie ablaufen, mit derselben Dimension in Audience Manager verglichen werden. Zum Beispiel listVars oder Merchandising-eVars, die nie ablaufen.

  Ein Beispiel: Wenn „eVar = blau“ und so konfiguriert ist, dass es in Analytics niemals abläuft, enthält jedes beliebige Segment mit dem Kriterium „eVar = blau“ stets diesen Besucher. In Audience Manager hingegen könnte dieser Besucher nach einem bestimmten Zeitraum aus einem ähnlich definierten Segment herausfallen.

* Analytics-Segmente verfügen über mehr Funktionen als Adobe Audience Manager-Segmente. Audience Manager-Segmente werden immer auf Besucherebene ausgewertet. Analytics-Segmente können auf Besucher-, Besuchs- oder Trefferebene (oder einer Kombination dieser Ebenen) definiert werden. Darüber hinaus unterstützt Analytics erweiterte Segmentierungsfunktionen, die Audience Manager nicht bietet, z. B. sequenzielle Segmentierung.

* Wie bereits erwähnt, können Audience Manager-Besucherinnen und -Besucher ein Segment aufrufen oder daraus aussteigen, je nachdem, ob sie sich zum aktuellen Zeitpunkt für die Segmentkriterien qualifizieren.

  Umgekehrt werden Besucher in Analytics basierend auf dem Berichtsdatumsbereich in ein Segment eingeschlossen oder aus einem Segment ausgeschlossen. Beispielsweise tätigte ein einzelner Besucher im letzten Monat einen Kauf. In Adobe Audience Manager würde dieser Besucher unabhängig vom Datumsbereich in ein Segment „Käufer“ aufgenommen. In Analytics würde ein Bericht, der auf diesem Monat basiert, den Besucher nicht in das Segment einschließen. Ein Bericht, der auf diesem Monat und dem letzten Monat basiert, würde den Besucher jedoch in das Segment einschließen.

Weitere Informationen finden [ im Analytics](/help/components/segmentation/seg-home.md)Segmentierungshandbuch .
