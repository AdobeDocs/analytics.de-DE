---
description: Adobe bietet verschiedene berechnete Metriken, die Sie verwenden können. Auf dieser Seite werden diese Metriken und die vorgesehenen Verwendungszwecke aufgelistet.
title: Standardmäßige berechnete Metriken
feature: Calculated Metrics
exl-id: 84468e63-f967-41cd-8084-525b1b90957a
source-git-commit: 43332660bbf19ffd22409ef48528bcdef81b5e01
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 41%

---

# Standardmäßige berechnete Metriken

Adobe Analytics bietet verschiedene berechnete Metriken, die die häufigsten Anwendungsfälle abdecken. Diese berechneten Metriken sind in Analysis Workspace standardmäßig verfügbar.

Im Folgenden finden Sie eine Liste aller berechneten Metriken, die von Adobe bereitgestellt werden, mit der beabsichtigten Funktion und der zugrunde liegenden Formel, die zur Berechnung verwendet wird:

>[!NOTE]
>
>Zusätzlich zu den auf dieser Seite beschriebenen standardmäßigen berechneten Metriken können Sie auch zusätzliche berechnete Metriken zu einer Report Suite hinzufügen.
>
>Sie haben folgende Möglichkeiten:
>
> * Fügen Sie standardmäßige berechnete Metriken für das Streaming-Mediensammlungs-Add-on hinzu, wie unter [Berechnete Metriken](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/variables/calculated-metrics.html) beschrieben.
> * Erstellen Sie benutzerdefinierte berechnete Metriken aus vorhandenen Metriken, wie unter [Berechnete und erweiterte berechnete Metriken](/help/components/c-calcmetrics/cm-overview.md) beschrieben.


| Name der berechneten Metrik | Funktion | Formel |
| --- | --- | --- |
| Akquise-Link-Klicks | Die Häufigkeit, mit der Besucherinnen und Besucher auf einen Link klicken, der dazu dient, den Traffic zur Website zu leiten. | `[Campaign Click-throughs]` |
| Aktionen | Die Gesamtzahl der in der App durchgeführten Aktionen | `[Has an Action] (segment)`<br>`[Custom Link Instances] (metric)` |
| App-Benutzer | Gesamtanzahl der Benutzer einer mobilen App | `[Mobile App Users] (segment)`<br>`[Unique Visitors] (metric)` |
| Durchschnittliche Sitzungslänge (Mobil) | Die durchschnittliche Zeit, die Besucher während einer einzelnen Sitzung auf der Site verbringen. | Leer |
| Durchschnittliche Besuchszeit pro Site | Die durchschnittliche Zeit, die ein Besucher auf der Site verbringt, bevor er die Site verlässt oder wegnavigiert. | `[Average Time Spent on Site (Seconds)]` |
| Absprungrate | Das Verhältnis der Besuche, die genau einen Treffer enthielten, zur Anzahl der Besuche auf dieser Seite. Diese Metrik kann Ihnen dabei helfen zu verstehen, welche Dimensionselemente die höchste Absprungrate aufweisen, oder eine aggregierte Gesamtabsprungrate Ihrer Site im Zeitverlauf anzuzeigen. | `[Bounces] / [Entries]` |
| Verhältnis von Bot-Seitenansichten | Das Verhältnis der beiden Seitenansichten zur Gesamtanzahl der Seitenansichten. | `[Bot Page Views] / [Page Views]` |
| Content-Geschwindigkeit | Die Geschwindigkeit, mit der neue Inhalte auf der Website erstellt und veröffentlicht werden, und wie schnell dadurch Benutzerinteraktionen generiert werden. | `[Page Views] / [Visits]` |
| Konversionsrate | Der Prozentsatz der Besucherinnen und Besucher, die eine gewünschte Aktion durchgeführt haben, z. B. einen Kauf getätigt haben. | `[Orders] / [Visits]` |
| Einstiegsrate | Der Prozentsatz der Besucherinnen und Besucher, die die Website über eine bestimmte Seite aufgerufen haben, verglichen mit der Gesamtzahl der Sitzungen auf der Website. | `[Entries] / [Visits]` |
| Geschätzte Unique Visitors (ITP 2.1) | Teilen Sie für ITP-Besucher (Benutzer in Safari-Browsern) Unique Visitors durch 2 oder weniger. Diese berechnete Metrik setzt voraus, dass Sie Cookies mit clientseitigem JavaScript setzen (ohne eine CNAME-Implementierung zu verwenden). Implementierungen, die Cookies mit clientseitigem JavaScript setzen, wurden ab ITP 2.1 beeinträchtigt. Weitere Informationen finden Sie unter [Intelligent Tracking Prevention](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) . | `[Unique Visitors (metric) with ITP Visitors (ITP 2.1, Non-CNAME implementations) segment] / [Unique Visitors metric + Non-ITP Visitors (ITP 2.1, Non-CNAME implementations) segment]` |
| Experience Cloud ID-Abdeckung | Die Anzahl der Besucherinnen und Besucher mit einer Experience Cloud-ID. | `[Visitors with Experience Cloud ID] / [Unique Visitors]` |
| Ausstiegsrate | Der Prozentsatz der Besucherinnen und Besucher, die die Website nach dem Anzeigen einer bestimmten Seite verlassen. | `[Exits] / [Visits]` |
| Unique Visitors (ITP 2.1) / Unique Visitors | Der Prozentsatz der Unique Visitors, die einen Browser verwenden, der von ITP 2.1-Cookie-Beschränkungen betroffen ist. | `[Unique Visitors metric with ITP Visitors segment] / [Unique Visitors]` |
| Bestellhilfen | Die Anzahl der Fälle, in denen ein Kanal oder eine Quelle zum Kauf einer Kundin oder eines Kunden im Zuge der Journey beigetragen, aber nicht zum endgültigen Kauf geführt hat. | `[Orders (Visit Participation)] - [Orders]` |
| Bestellungen/Besuche | Der Prozentsatz der Besuche auf der Website, die zu einer abgeschlossenen Transaktion führen. | `[Orders] / [Visits]` |
| Bestellungen/Besucher | Die durchschnittliche Anzahl von Bestellungen oder Transaktionen, die von jedem einzelnen Besucher der Site generiert wurden. | `[Orders] / [Unique Visitors]` |
| Seitenansichten/Geschätzte Unique Visitors (ITP 2.1) | Die durchschnittliche Anzahl der für „Geschätzte Unique Visitors“ (ITP 2.1) angezeigten Seiten. | `[Unique Visitors (metric) with ITP Visitors (ITP 2.1, Non-CNAME implementations) segment] / [Unique Visitors (metric) with Non-ITP Visitors (ITP 2.1, Non-CNAME implementations) segment]` |
| Seitenansichten/Unique Visitor | Die durchschnittliche Anzahl der pro Unique Visitor der Website angezeigten Seiten. | `[Page Views] / [Unique Visitors]` |
| Seitenansichten/Besuche | Die durchschnittliche Anzahl von Seiten, die sich eine Benutzerin oder ein Benutzer bei einem einzelnen Besuch der Website ansieht. | `[Page Views] / [Visits]` |
| Seitengeschwindigkeit | Die Anzahl der zusätzlichen Seitenansichten, die ein Inhaltselement generiert. Diese Metrik kann Ihnen dabei helfen zu bestimmen, welche Inhalte zu zusätzlicher Interaktion führen. | `[Page Views] / [Visits]` |
| Neuladungen/Seitenansichten | Der Prozentsatz der Seitenansichten, die zu einem erneuten Laden oder Aktualisieren der Seite geführt haben. | `[Reloads] / [Page Views]` |
| Umsatz/Bestellung | Die durchschnittliche Umsatzhöhe, die durch jede abgeschlossene Transaktion oder Bestellung auf der Website generiert wird. | `[Revenue] / [Orders]` |
| Umsatz/Besuche | Die durchschnittliche Umsatzhöhe, die durch einen einzelnen Besuch der Website generiert wird. | `[Revenue] / [Visits]` |
| Umsatz/Besucher | Der durchschnittliche Umsatz, der von jeder einzelnen Besucherin und jedem einzelnen Besucher der Website generiert wird. | `[Revenue] / [Unique Visitors]` |
| Statusansichten | Die Anzahl der Ansichten für die verschiedenen Status oder Bildschirme der App | `[Mobile App Users] (segment)`<br>`[Page Views] (metric)` |
| Besuchszeit/Benutzer (Status) | Die Zeitdauer, die der durchschnittliche Besucher in einem bestimmten Bundesstaat auf der Site verbringt. | `[Mobile App Users] (segment)`<br>`[Time Spent per Visitor (Seconds)] (metric)` |
| Unique Visitors/Unique Visitors, die nach 7 Tagen zurückkehren | Der Prozentsatz der Unique Visitors, die nach einem Zeitraum von sieben oder mehr Tagen zurückkehren. | `[Unique Visitors metric with Users returning after 7 days segment] / [Unique Visitors]` |
| Benutzer (Mobil) | Gesamtanzahl der Benutzer einer mobilen App | `[Mobile App Users] (segment)`<br>`[Unique Visitors] (metric)` |
| Besuche/Besucher | Die durchschnittliche Anzahl der Besuche eines Unique Visitors auf der Website. | `[Visits] / [Unique Visitors]` |
| Gewichtete Rücksendungsrate | Funktion | `IF([Visits] > PERCENTILE([Visits]), [Bounce Rate], 0)` |

{style="table-layout:auto"}
