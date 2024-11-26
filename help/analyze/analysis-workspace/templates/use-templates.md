---
description: Eine Übersicht über die Verwendung von Vorlagen in Analysis Workspace.
title: Verwenden von Vorlagen
feature: Analysis Workspace
role: User, Admin
hide: true
hidefromtoc: true
source-git-commit: e98458a96e9950ffab40876b80a9e799a9182e6a
workflow-type: tm+mt
source-wordcount: '18051'
ht-degree: 58%

---

# Verwenden von Vorlagen

Vorlagen (oder Unternehmensvorlagen) in Analysis Workspace bieten schnelle Einblicke in die gängigsten Berichtsszenarien. Im Folgenden finden Sie einige Beispiele für Fragen, die Sie mit Vorlagen beantworten können:

* Wie viele Personen Ihre Website besuchen
* Wie viele dieser Besucher Unique Visitors darstellen (d. h. nur ein Mal gezählt werden)
* Wie diese zu Ihrer Site gelangten (ob sie einem Link folgen oder Ihre Site direkt aufrufen)
* Welche Keywords die Besucher zum Browsen des Site-Inhalts einsetzen
* Wie lange sie auf einer bestimmten Seite oder der gesamten Website verweilen
* Welche Links von Besuchern angeklickt wurden und wann diese die Seite verlassen haben
* Welche Marketingkanäle am wirksamsten zu Umsatz oder Konversion-Ereignissen führen
* Wie viel Zeit sie mit dem Anschauen eines Videos verbracht haben
* Welche Browser und Geräte zum Besuch der Seite genutzt wurden

Im Folgenden wird beschrieben, wie Sie Vorlagen auf der Registerkarte [!UICONTROL Vorlagen] in Analysis Workspace aufrufen und verwenden.

## Zugreifen auf und Ausführen einer Vorlage

1. Wählen Sie in Analysis Workspace die Registerkarte [!UICONTROL **Workspace**].

   <!--update screenshot -->

   ![Registerkarte „Berichte“](assets/view-prebuilt-reports.png)

1. Wählen Sie im Abschnitt [!UICONTROL **Vorlagen**] eine der folgenden Registerkarten aus:

   * **[!UICONTROL Adobe templates]**: Zeigt alle Vorlagen an, die von Adobe bereitgestellt werden.

   * **[!UICONTROL _login_company_name _templates]**: Zeigt alle Unternehmensvorlagen an, für die in Ihrem Unternehmen erstellt wurde.

     Unternehmensvorlagen können nur von einem Administrator erstellt werden. Weitere Informationen zum Erstellen einer Unternehmensvorlage finden Sie unter [Erstellen und Verwalten von Vorlagen](/help/analyze/analysis-workspace/reports/create-company-reports.md).

1. Wählen Sie entweder das Spaltenansichtssymbol ![Spaltenansichtssymbol](assets/column-view-icon.png) oder das Kartenansichtssymbol ![Kartenansichtssymbol](assets/card-view-icon.png) aus, um Vorlagen in einer Spaltenansicht oder Kartenansicht anzuzeigen.

1. Geben Sie im Suchfeld den Namen der Vorlage ein, die Sie finden möchten, und wählen Sie sie dann aus der Vorlagenliste aus. Sie können die Vorlagenliste auch nach Eigenschaften, eVar und Ereignisnummern durchsuchen. <!-- still true? -->

   Oder

   Wählen Sie die Vorlagenkategorie aus, die Sie anzeigen möchten, und wählen Sie dann die Vorlage aus der Vorlagenliste aus.

   >[!TIP]
   >
   >Um mithilfe der Pfeiltasten durch das Menü zu navigieren, drücken Sie die Schrägstrich-Taste (/) und dann die Nach-unten-Taste. Drücken Sie die Eingabetaste , um die ausgewählte Vorlage zu laden.

   Eine Liste der verfügbaren Vorlagen finden Sie unten im Abschnitt [Verfügbare Vorlagen](#available-reports) .

1. (Optional) Zeigen Sie Vorlagen an und verwenden Sie Vorlagen, die Komponenten enthalten, die nicht in Ihrer Report Suite verfügbar sind. (Standardmäßig werden nur Vorlagen angezeigt, die Komponenten verwenden, die in Ihrer Report Suite verfügbar sind.) <!--does this apply to AA? -->

## Erstellen eines Projekts basierend auf einer Vorlage {#use-reports}

Eine Vorlage passt möglicherweise nicht genau zu Ihren Anforderungen, kann Sie jedoch schließen. In diesen Fällen können Sie die Vorlage als Ausgangspunkt verwenden und sie dann an Ihre spezifischen Zwecke anpassen.

Wenn Sie nach den Änderungen von einer Vorlage weg navigieren, werden Sie aufgefordert, Ihre Änderungen zu speichern oder zu verwerfen. Durch das Speichern von Änderungen an einer Vorlage wird die Vorlage als neues Projekt gespeichert.

So passen Sie eine Vorlage an und speichern sie als Projekt:

1. Wählen Sie in Adobe Analytics die Registerkarte [!UICONTROL **Workspace**] aus.

1. Wählen Sie die Registerkarte [!UICONTROL **Vorlagen**] aus.

1. Wählen Sie die Vorlage aus, die Sie anzeigen möchten. Wählen Sie beispielsweise unter &quot;[!UICONTROL **Am beliebtesten**]&quot;die Vorlage &quot;[!UICONTROL **Seiten**]&quot;aus.

   ![Bericht zu Seiten](assets/pages-report.png)

1. Die Seitenvorlage, wie in Analysis Workspace angezeigt, zeigt zwei [Visualisierungen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md) ([Balkendiagramm](/help/analyze/analysis-workspace/visualizations/bar.md) und [Zusammenfassungsnummer](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)) und eine [Freiformtabelle](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md) an. Die verwendete Metrik ist „Vorkommen“.
1. Führen Sie einen der folgenden Schritte aus:

   * Zeigen Sie die Vorlage an.
   * Sie können ein oder mehrere Segmente oben in den Ablagebereich ziehen. Ziehen Sie beispielsweise das Segment [!UICONTROL **Mobile-Kunden**] und sehen Sie sich die Ergebnisse an.
   * Ändern Sie den Datumsbereich, indem Sie zum Kalender oben rechts gehen.
   * Fügen Sie Dimensionsaufschlüsselungen hinzu, ziehen Sie andere Metriken hinzu und passen Sie die Vorlage im Allgemeinen an Ihre Anforderungen an.

1. (Optional) Speichern Sie die Vorlage als Projekt, indem Sie [!UICONTROL **Projekt**] > [!UICONTROL **Speichern**] auswählen.

   Die Vorlage wird als neues Projekt gespeichert. Sie ändert die vorhandene Vorlage nicht. Weitere Informationen zum Speichern von Projekten finden Sie unter [Projekte speichern](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md).

## Verfügbare Vorlagen

So greifen Sie auf alle verfügbaren vordefinierten Vorlagen zu:

1. Wählen Sie in Adobe Analytics die Registerkarte [!UICONTROL **Workspace**] und dann die Registerkarte [!UICONTROL **Vorlagen**] aus.

   Vordefinierte Vorlagen sind nach Kategorie geordnet.

   <!--add screenshot-->

1. Wählen Sie eine Kategorie aus, um die darin enthaltenen Vorlagen anzuzeigen.

   Die folgenden Abschnitte entsprechen den verfügbaren Kategorien und enthalten Informationen zu den einzelnen Vorlagen.

   * [[!UICONTROL ](#most-popular)

   * [[!UICONTROL ](#engagement)

### Am beliebtesten {#most-popular}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--training"
>title="Schulungsanleitung"
>abstract="Erfahren Sie mehr über die gängige Terminologie und die Schritte zum Erstellen Ihrer ersten Analyse in Analysis Workspace."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--pagesRankedReport"
>title="Identifizieren Sie die beliebtesten und unbeliebtesten Seiten."
>abstract="**Dies kann Ihnen helfen**, Ihre Zielgruppe und die Art von Informationen, die sie am meisten interessiert, besser zu verstehen.<br/>**Basierend auf dem, was Sie erfahren, können Sie** eine Reihe von Schritten ausführen, z. B. Seitenmetadaten anpassen, um die Sichtbarkeit auf seltener angezeigten Seiten zu erhöhen, oder Zeit in die Verbesserung des Inhalts Ihrer am häufigsten angezeigten Seiten investieren.<br/>Diese Vorlage verwendet die Dimension „Seite“ und die Metrik „Seitenansichten“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--pageViewsOvertimeReport"
>title="Zeigen Sie die Gesamtanzahl der Seitenansichten an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. "
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie der Traffic auf Ihrer Site im Laufe der Zeit möglicherweise zu- oder abnimmt.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne bewerten, indem Sie den Sitetraffic vor und nach dem Start der Kampagne vergleichen. Oder Sie vergleichen den jährlichen Feiertags-Traffic.<br/>Diese Vorlage verwendet die Dimension „Tag“ und die Metrik „Seitenansichten“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--visitsOvertimeReport"
>title="Zeigen Sie die Gesamtanzahl der Besuche an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie der Traffic auf Ihrer Site im Laufe der Zeit möglicherweise zu- oder abnimmt.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne bewerten, indem Sie den Sitetraffic vor und nach dem Start der Kampagne vergleichen. Oder Sie vergleichen den jährlichen Feiertags-Traffic.<br/>Diese Vorlage verwendet die Dimension „Tag“ und die Metrik „Besuche“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--visitorsOvertimeReport"
>title="Zeigen Sie die Gesamtanzahl der Unique Visitors an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. "
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie die Reichweite und die Zielgruppengröße Ihrer Site im Laufe der Zeit oder im Vergleich mit einem früheren Zeitraum zu- oder abnimmt.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob eine kürzlich gestartete Marketing-Kampagne erfolgreich darin war, neue Personen auf die Site zu locken, indem Sie Unique Visitors vor und nach dem Start der Kampagne vergleichen. Oder Sie können die Anzahl der Personen vergleichen, die die Site jedes Jahr während der Feiertage besuchen.<br/>Diese Vorlage verwendet die Dimension „Tag“ und die Metrik „Unique Visitors“. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--keyMetricsReport"
>title="Zeigen Sie einen Bericht an, der die Metriken „Seitenansichten“, „Besuche“ und „Unique Visitors“ nebeneinander anzeigt. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen."
>abstract="**Dies kann Ihnen helfen**, diese wichtigen Metriken zu vergleichen, um ein vollständigeres Bild über die Anzahl der Unique Visitors auf der Site, die Anzahl der Seitenbesuche und die Anzahl der Sitzungen zu erhalten.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die durchschnittliche Anzahl der Seiten bewerten, die jede Person während eines Besuchs auf der Site in einer bestimmten Woche oder in einem bestimmten Monat angesehen hat, und ermitteln, wie sich dies während bestimmter Zeiten des Jahres oder vor und nach der Durchführung von Marketing-Kampagnen verändert hat. <br/>Diese Vorlage verwendet die Dimension „Tag“, die Metrik „Seitenansichten“, die Metrik „Besuche“ und die Metrik „Unique Visitors“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--siteSectionRankedReport"
>title="Zeigen Sie die beliebtesten oder leistungsstärksten Bereiche Ihrer Site an."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Bereiche Ihrer Site am häufigsten besucht werden.<br>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, welche Ihrer Produkte oder Services das meiste Interesse generieren.<br/>Diese Vorlage verwendet die Dimension „Site-Bereich“ und die Metrik „Besuche“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--next-page-report"
>title="Sehen Sie sich die Bereiche an, die Personen am häufigsten direkt nach einem Besuch oder unmittelbar vor dem Besuch eines bestimmten Bereichs aufrufen."
>abstract="**Dies kann Ihnen dabei helfen**, zu verstehen, wie sich der Traffic von einer bestimmten Seite zu anderen Teilen Ihrer Site bewegt. Außerdem können Sie die Pfade verstehen, die Personen nehmen, um zu einer bestimmten Seite zu gelangen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob das Seiten-Design oder -Layout optimiert werden kann, um Personen zu wünschenswerteren Seiten zu leiten, z. B. zu einer Seite, auf der sie einen Kauf tätigen oder eine Rezension abgeben. Oder bewerten Sie, ob die Informationen auf der aktuellen Seite wahrscheinlich die Richtung oder die Aktionen angeben, nach denen Personen suchen, wenn sie von vorherigen Seiten kommen. Sie könnten auch bewerten, ob Seiten, die nicht als vorherige Seiten angezeigt werden, markantere Links zur aktuellen Seite benötigen.<br/>Diese Vorlage verwendet das Panel „Nächstes oder vorheriges Objekt“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--campaignRankedReport"
>title="Zeigen Sie die Links an, die am erfolgreichsten Traffic auf Ihre Site geleitet haben."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Trackingcodes (und Links, mit denen sie verknüpft sind) am häufigsten beim Zugriff auf Ihre Site verwendet wurden.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Strategie anpassen, wo Sie Links zu Ihrer Site hinzufügen.<br/>Diese Vorlage verwendet die Dimension „Trackingcode“ und die Metrik „Besuche“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--productsRankedReport"
>title="Zeigen Sie die Anzahl der Bestellungen nach Produkt an. Daten werden für einen bestimmten Zeitraum angezeigt."
>abstract="**Dies kann Ihnen helfen**, zu verstehen, welche Produkte die höchste oder die geringste Nachfrage aufweisen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Marketing-Strategien so anpassen, dass sie leistungsstarke Produkte bewerben oder Produkte mit schlechter Leistung verbessern oder einstellen. Sie könnten auch Ihren Produktbestand auf Grundlage Ihrer Datenanalyse anpassen.<br/>Diese Vorlage verwendet die Dimension „Produkt“ und die Metrik „Bestellungen“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--lastTouchChannelRankedReport"
>title="Zeigen Sie die neuesten Marketing-Kanäle an, zu denen Besuchende während ihres Interaktionszeitraums (standardmäßig 30 Tage) passen."
>abstract="**Dies kann Ihnen dabei helfen**, zu verstehen, welche Marketing-Kanäle am effektivsten waren, um Personen zu Ihrer Site zu leiten und um Konversionen zu erreichen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. mehr Ressourcen für leistungsstarke Kanäle oder weniger Ressourcen für leistungsschwache Kanäle zuweisen.<br/>Diese Vorlage verwendet die Dimension „Letztkontaktkanal“ und die Metrik „Unique Visitors“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--lastTouchChannelDetailRankedReport"
>title="Zeigen Sie Details zu den neuesten Marketing-Kanälen an, zu denen Besuchende während ihres Interaktionszeitraums (standardmäßig 30 Tage) passen."
>abstract="**Dies kann Ihnen dabei helfen**, nicht nur zu verstehen, welche Marketing-Kanäle am effektivsten waren, um Personen zu Ihrer Site zu leiten und Konversionen zu erreichen, sondern Sie erhalten auch Details zu diesen Marketing-Kanälen. Wenn beispielsweise ein Besucher zu Ihrer Site gelangt ist und mit dem Marketing-Kanal „Paid Search“ übereinstimmt, können Sie anhand des Kanaldetails sehen, welche Suchmaschine verwendet wurde oder nach welchem Schlüsselwort er gesucht hat.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. mehr Ressourcen für leistungsstarke Kanäle oder weniger Ressourcen für leistungsschwache Kanäle zuweisen.<br/>Diese Vorlage verwendet die Dimension „Details des Letztkontaktkanals“ und die Metrik „Unique Visitors“. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--revenueOvertimeReport"
>title="Zeigen Sie den Geldbetrag der bei allen Bestellungen gekauften Produkte an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen."
>abstract="**Dies kann Ihnen helfen**, zu verstehen, wie der Umsatz im Laufe der Zeit zu- oder abnimmt. Sie können diese Metrik mit einer beliebigen Dimension kombinieren, um zu erfahren, welche Dimensionselemente zum Umsatz beigetragen haben. <br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. zukünftige Umsätze basierend auf früheren Trends planen. Sie können auch eine weitere Dimension hinzufügen, z. B. die Dimension „Trackingcode“, um zu erfahren, welche Kampagnen den meisten Umsatz generieren.<br/>Diese Vorlage verwendet die Dimension „Tag“ und die Metrik „Umsatz“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--ordersOvertimeReport"
>title="Zeigen Sie die Gesamtanzahl der Kaufereignisse an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie das Interesse an Ihren Produkten und Services im Laufe der Zeit zu- oder abnimmt. Sie können ein Segment anwenden, um zu erfahren, welche Kundinnen und Kunden oder Regionen die meisten Bestellungen aufgeben und wie der Trend bei diesen Bestellungen im Laufe der Zeit aussieht.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne durch den Vergleich der Bestellungen vor und nach dem Start der Kampagne bewerten. Oder Sie vergleichen die jährlichen Bestellungen zu Feiertagen.<br/>Diese Vorlage verwendet die Dimension „Tag“ und die Metrik „Bestellungen“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--unitsOvertimeReport"
>title="Zeigen Sie die Gesamtzahl der bei allen Bestellungen gekauften Artikel an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, wie die Stückverkäufe im Laufe der Zeit zunehmen oder abnehmen. Sie können ein Segment anwenden, um zu erfahren, welche Kunden oder Regionen die meisten Einheiten kaufen und wie diese Verkaufseinheiten im Laufe der Zeit im Trend sind.<br/>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Maßnahmen durchführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne durch Vergleich der Einzelverkäufe vor und nach dem Start der Kampagne. Oder Sie vergleichen den Jahresvergleich der Einzelverkäufe während der Feiertage.<br/>Diese Vorlage verwendet die Dimension Tag und die Metrik Einheiten ."

<!-- markdownlint-enable MD034 -->

Die folgenden Vorlagen sind verfügbar:

| Vorlagenname | Warum diese Vorlage <!-- What do you do with it? What can it help you learn? and What are the potential actions? --> verwenden |
| --- | --- | 
| [!UICONTROL **Tutorial für Schulungen**] | Erfahren Sie mehr über die gängige Terminologie und die Schritte zur Erstellung Ihrer ersten Analyse in Analysis Workspace. |
| [!UICONTROL **Seiten**] | <!--duplicated in Engagement section--> Identifizieren Sie die beliebtesten und unbeliebtesten Seiten. <p>**Dies kann Ihnen helfen**, Ihre Zielgruppe und die Art von Informationen, die sie am meisten interessiert, besser zu verstehen.</p><p>**Basierend auf dem, was Sie erfahren, können Sie** eine Reihe von Schritten ausführen, z. B. Seitenmetadaten anpassen, um die Sichtbarkeit auf seltener angezeigten Seiten zu erhöhen, oder Zeit in die Verbesserung des Inhalts Ihrer am häufigsten angezeigten Seiten investieren.</p><p>Diese Vorlage verwendet die Dimension [Seite ](/help/components/dimensions/page.md) und die Metrik [Seitenansichten](/help/components/metrics/page-views.md).</p> |
| [!UICONTROL **Seitenansichten**] | <!--duplicated in Engagement section--> Zeigen Sie die Gesamtanzahl der Seitenansichten an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, wie der Traffic auf Ihrer Site im Laufe der Zeit möglicherweise zu- oder abnimmt.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne bewerten, indem Sie den Sitetraffic vor und nach dem Start der Kampagne vergleichen. Oder Sie vergleichen den jährlichen Feiertags-Traffic.</p><p>Diese Vorlage verwendet die Dimension [Tag](/help/components/dimensions/day.md) und die Metrik [Seitenansichten](/help/components/metrics/page-views.md).</p> |
| [!UICONTROL **Besuche**] | <!--duplicated in Engagement section--> Zeigen Sie die Gesamtanzahl der Besuche an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, wie der Traffic auf Ihrer Site im Laufe der Zeit möglicherweise zu- oder abnimmt.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne bewerten, indem Sie den Sitetraffic vor und nach dem Start der Kampagne vergleichen. Oder Sie vergleichen den jährlichen Feiertags-Traffic.</p><p>Diese Vorlage verwendet die Dimension [Tag](/help/components/dimensions/day.md) und die Metrik [Besuche](/help/components/metrics/visits.md).</p> |
| [!UICONTROL **Besucher**] | <!--duplicated in Engagement section--> Zeigen Sie die Gesamtanzahl der Unique Visitors an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, wie die Reichweite und die Zielgruppengröße Ihrer Site im Laufe der Zeit oder im Vergleich mit einem früheren Zeitraum zu- oder abnimmt.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob eine kürzlich gestartete Marketing-Kampagne erfolgreich darin war, neue Personen auf die Site zu locken, indem Sie Unique Visitors vor und nach dem Start der Kampagne vergleichen. Oder Sie können die Anzahl der Personen vergleichen, die die Site jedes Jahr während der Feiertage besuchen.</p><p>Diese Vorlage verwendet die Dimension &quot;[Tag&quot;](/help/components/dimensions/day.md) und die Metrik &quot;[Unique Visitors&quot;](/help/components/metrics/unique-visitors.md).</p> |
| [!UICONTROL **Schlüsselmetriken**] | <!--duplicated in Engagement section--> Zeigen Sie einen Bericht an, der die Metriken „Seitenansichten“, „Besuche“ und „Unique Visitors“ nebeneinander anzeigt. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, diese wichtigen Metriken zu vergleichen, um ein vollständigeres Bild über die Anzahl der Unique Visitors auf der Site, die Anzahl der Seitenbesuche und die Anzahl der Sitzungen zu erhalten.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** beliebig viele Dinge tun, z. B. die durchschnittliche Anzahl der Seiten, die jeder Besucher während eines Besuchs auf der Site in einer bestimmten Woche oder in einem bestimmten Monat angesehen hat, und wie sich dies während bestimmter Zeiten des Jahres oder vor und nach der Ausführung von Marketingkampagnen verändert hat. </p><p>Diese Vorlage verwendet die Dimension [Tag ](/help/components/dimensions/day.md), die Metrik [Seitenansichten](/help/components/metrics/page-views.md), die Metrik [Besuche](/help/components/metrics/visits.md) und die Metrik [Unique Visitors](/help/components/metrics/unique-visitors.md).</p> |
| [!UICONTROL **Site-Abschnitte**] | Zeigen Sie die beliebtesten oder leistungsstärksten Bereiche Ihrer Site an. <p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Bereiche Ihrer Site am häufigsten besucht werden.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, welche Ihrer Produkte oder Services das meiste Interesse generieren.</p> <p>Diese Vorlage verwendet die Dimension [Sitebereich](/help/components/dimensions/site-section.md) und die Metrik [Besuche](/help/components/metrics/visits.md).</p> |
| [!UICONTROL **Nächste und vorherige Seite**] | Sehen Sie sich die Bereiche an, die Personen am häufigsten direkt nach einem Besuch oder unmittelbar vor dem Besuch eines bestimmten Bereichs aufrufen. <p>**Dies kann Ihnen dabei helfen**, zu verstehen, wie sich der Traffic von einer bestimmten Seite zu anderen Teilen Ihrer Site bewegt. Außerdem können Sie die Pfade verstehen, die Personen nehmen, um zu einer bestimmten Seite zu gelangen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob das Seiten-Design oder -Layout optimiert werden kann, um Personen zu wünschenswerteren Seiten zu leiten, z. B. zu einer Seite, auf der sie einen Kauf tätigen oder eine Rezension abgeben. Oder bewerten Sie, ob die Informationen auf der aktuellen Seite wahrscheinlich die Richtung oder die Aktionen angeben, nach denen Personen suchen, wenn sie von vorherigen Seiten kommen. Sie könnten auch bewerten, ob Seiten, die nicht als vorherige Seiten angezeigt werden, markantere Links zur aktuellen Seite benötigen.</p><p>Diese Vorlage verwendet den Bereich [Nächstes oder vorheriges Element](/help/analyze/analysis-workspace/c-panels/next-previous.md).</p> |
| [!UICONTROL **Kampagnen (Trackingcode)**] | Zeigen Sie die Links an, die am erfolgreichsten Traffic auf Ihre Site geleitet haben. <p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Trackingcodes (und Links, mit denen sie verknüpft sind) am häufigsten beim Zugriff auf Ihre Site verwendet wurden.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Strategie anpassen, wo Sie Links zu Ihrer Site hinzufügen.</p><p>Diese Vorlage verwendet die Dimension [Trackingcode](/help/components/dimensions/tracking-code.md) und die Metrik [Besuche](/help/components/metrics/visits.md).</p> |
| [!UICONTROL **Produkte**] | Zeigen Sie die Anzahl der Bestellungen nach Produkt an. Daten werden für einen bestimmten Zeitraum angezeigt. <p>**Dies kann Ihnen helfen**, zu verstehen, welche Produkte die höchste oder die geringste Nachfrage aufweisen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Marketing-Strategien so anpassen, dass sie leistungsstarke Produkte bewerben oder Produkte mit schlechter Leistung verbessern oder einstellen. Sie könnten auch Ihren Produktbestand auf Grundlage Ihrer Datenanalyse anpassen.</p><p>Diese Vorlage verwendet die [Produktdimension](/help/components/dimensions/product.md) und die [Bestellmetrik](/help/components/metrics/orders.md).</p> |
| [!UICONTROL **Letztkontakt-Kanal**] | Zeigen Sie die neuesten Marketing-Kanäle an, zu denen Besuchende während ihres Interaktionszeitraums (standardmäßig 30 Tage) passen.<p>**Dies kann Ihnen dabei helfen**, zu verstehen, welche Marketing-Kanäle am effektivsten waren, um Personen zu Ihrer Site zu leiten und um Konversionen zu erreichen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. mehr Ressourcen für leistungsstarke Kanäle oder weniger Ressourcen für leistungsschwache Kanäle zuweisen.</p><p>Diese Vorlage verwendet die Dimension [Letztkontakt-Kanal](/help/components/dimensions/last-touch-channel.md) und die Metrik [Unique Visitors](/help/components/metrics/unique-visitors.md).</p> |
| [!UICONTROL **Letztkontakt-Kanaldetail**] | Zeigen Sie Details zu den neuesten Marketing-Kanälen an, zu denen Besuchende während ihres Interaktionszeitraums (standardmäßig 30 Tage) passen.<p>**Dies kann Ihnen dabei helfen**, nicht nur zu verstehen, welche Marketing-Kanäle am effektivsten waren, um Personen zu Ihrer Site zu leiten und Konversionen zu erreichen, sondern Sie erhalten auch Details zu diesen Marketing-Kanälen. Wenn beispielsweise ein Besucher zu Ihrer Site gelangt ist und mit dem Marketing-Kanal „Paid Search“ übereinstimmt, können Sie anhand des Kanaldetails sehen, welche Suchmaschine verwendet wurde oder nach welchem Schlüsselwort er gesucht hat.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. mehr Ressourcen für leistungsstarke Kanäle oder weniger Ressourcen für leistungsschwache Kanäle zuweisen.</p><p>Diese Vorlage verwendet die Dimension [Letztkontakt Kanaldetail](/help/components/dimensions/last-touch-detail.md) und die Metrik [Unique Visitors](/help/components/metrics/unique-visitors.md).</p> |
| [!UICONTROL **Umsatz**] | Zeigen Sie den Geldbetrag der bei allen Bestellungen gekauften Produkte an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen.<p>**Dies kann Ihnen helfen**, zu verstehen, wie der Umsatz im Laufe der Zeit zu- oder abnimmt. Sie können diese Metrik mit einer beliebigen Dimension kombinieren, um zu erfahren, welche Dimensionselemente zum Umsatz beigetragen haben. </p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. zukünftige Umsätze basierend auf früheren Trends planen. Sie können auch eine weitere Dimension hinzufügen, z. B. die Dimension „Trackingcode“, um zu erfahren, welche Kampagnen den meisten Umsatz generieren.</p><p>Diese Vorlage verwendet die Dimension [Tag](/help/components/dimensions/day.md) und die Metrik [Umsatz](/help/components/metrics/revenue.md).</p> |
| [!UICONTROL **Bestellungen**] | Zeigen Sie die Gesamtanzahl der Kaufereignisse an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, wie das Interesse an Ihren Produkten und Services im Laufe der Zeit zu- oder abnimmt. Sie können ein Segment anwenden, um zu erfahren, welche Kundinnen und Kunden oder Regionen die meisten Bestellungen aufgeben und wie der Trend bei diesen Bestellungen im Laufe der Zeit aussieht.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne durch den Vergleich der Bestellungen vor und nach dem Start der Kampagne bewerten. Oder Sie vergleichen die jährlichen Bestellungen zu Feiertagen.</p><p>Diese Vorlage verwendet die Dimension [Tag](/help/components/dimensions/day.md) und die Metrik [Bestellungen](/help/components/metrics/orders.md).</p> |
| [!UICONTROL **Einheiten**] | Zeigen Sie die Gesamtzahl der bei allen Bestellungen gekauften Artikel an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen** helfen, besser zu verstehen, wie die Stückverkäufe im Laufe der Zeit zunehmen oder abnehmen. Sie können ein Segment anwenden, um zu erfahren, welche Kunden oder Regionen die meisten Einheiten kaufen und wie diese Verkaufseinheiten im Laufe der Zeit im Trend sind.</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Maßnahmen durchführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne durch Vergleich der Einzelverkäufe vor und nach dem Start der Kampagne. Oder Sie vergleichen den Jahresvergleich der Einzelverkäufe während der Feiertage.</p><p>Diese Vorlage verwendet die Dimension &quot;[Tag&quot;](/help/components/dimensions/day.md) und die Metrik &quot;[Einheiten&quot;](/help/components/metrics/units.md).</p> |

### Interaktion {#web-engagement}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--timeSpentVisitOvertimeReport"
>title="Zeigen Sie die durchschnittliche Zeit an, die Besucher während jedes Besuchs auf Ihrer Site verbringen. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen."
>abstract="**Dies kann Ihnen** helfen, die Interaktionsstufen der Besucher und die Zeitdauer, die Besucher auf der Site verbringen, besser zu verstehen.<br/>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. um zu bewerten, ob Änderungen an Ihrer Site dazu führen, dass Besucher mehr Zeit auf der Site verbringen.<br/>Diese Vorlage verwendet die Dimension Tag und die Metrik Zeit pro Besuch (Sekunden) ."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--timePriorRankedReport"
>title="Zeigen Sie die durchschnittliche Zeit an, die Benutzer vor einem Erfolgsereignis verbringen."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, wie viel Zeit Besucher benötigen, um eine gewünschte Aktion durchzuführen, z. B. einen Kauf vorzunehmen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob Änderungen an Ihrer Site es den Besuchenden erleichtert, schnell ein Erfolgsereignis zu erreichen.<br/>Diese Vorlage verwendet die Dimension Zeit vor Ereignis und die Metrik Unique Visitors ."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--web-content-consumption"
>title="Zeigen Sie an, welche Web-Inhalte am häufigsten genutzt werden und für Benutzende interessant sind."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wo Personen beim ersten Aufrufen der Site hingehen, welche Bereiche der Site von Personen am häufigsten besucht werden und welche Seiten Personen am wahrscheinlichsten von der Site wegführen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, welche Pfade auf der Site Personen zu den wichtigsten Seiten führen und welche Seiten Personen wahrscheinlicher von der Site wegführen.<br/>Diese Vorlage verwendet die Dimension „Seite“ und die Metrik „Seitenansichten“, die Metrik „Besuche“, die Metrik „Unique Visitors“, die Metrik „Eintrittsrate“, die Metrik „Bounce-Rate“, die Metrik „Ausstiegsrate“ und die Metrik „Contentgeschwindigkeit“. Außerdem werden Flussvisualisierungen für Eintritts-, Ausstiegs- und Top-Abschnitte verwendet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--media-content-consumption"
>title="Zeigen Sie an, welche Medieninhalte am häufigsten genutzt werden und für Benutzende interessant sind."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wo Personen beim ersten Aufrufen der Site hingehen, welche Bereiche der Site von Personen am häufigsten besucht werden und welche Seiten Personen am wahrscheinlichsten von der Site wegführen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, welche Pfade auf der Site Personen zu den wichtigsten Seiten führen und welche Seiten Personen wahrscheinlicher von der Site wegführen.<br/>Diese Vorlage verwendet die Dimension „Seite“ und die Metrik „Seitenansichten“, die Metrik „Besuche“, die Metrik „Unique Visitors“, die Metrik „Eintrittsrate“, die Metrik „Bounce-Rate“, die Metrik „Ausstiegsrate“ und die Metrik „Contentgeschwindigkeit“. Darüber hinaus werden Flussvisualisierungen für Eintritt-, Ausstiegs- und Top-Abschnitte verwendet. Eine Scatterplot-Visualisierung zeigt die Seitenansichten für die gängigsten Seiten an. Eine Balkenvisualisierung zeigt die Seitenansichten nach zusammengefasster Zeit an. Eine Linienvisualisierung stellt eine Trend-Ansicht der durchschnittlichen Besuchszeit auf der Site dar."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--falloutReport"
>title="Sehen Sie sich an, wo Benutzer eine vordefinierte Seitensequenz verlassen oder wie sie weitermachen."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, wo Personen aus der Journey fallen.<br/>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Konversionsraten durch bestimmte Prozesse auf Ihrer Site analysieren (z. B. einen Kauf- oder Registrierungsprozess) oder Korrelationen zwischen Ereignissen auf Ihrer Site analysieren. (Zum Beispiel, welcher Prozentsatz der Personen, die sich Ihre Datenschutzrichtlinien angesehen haben, ein Produkt kauften.) Sie können diese Vorlage auch verwenden, um zwei verschiedene Segmente im selben Bericht nebeneinander zu vergleichen.<br/>Diese Vorlage verwendet die Fallout-Visualisierung."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--cross-device-analysis"
>title="Anzeigen der Geräte, die an allen Punkten des Journey verwendet werden"
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, wie viele Personen mit Ihrer Marke interagieren, welche Arten von Geräten sie verwenden und wie ihre Verwendung mehrerer Geräte deren Erlebnis beeinflusst. Wie oft beginnen Personen beispielsweise eine Aufgabe auf einem Mobilgerät und wechseln dann später zu einem Desktop, um eine Aufgabe abzuschließen? Welche sind die häufigsten Pfade, die Benutzer beim Wechsel von einem Gerät zum anderen verwenden? Wo steigen sie aus? Wo sind sie erfolgreich? Und so weiter.<br/>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. bestimmte Teile der Benutzer-Journey für ein mobiles Erlebnis optimieren.<br/>Diese Vorlage verwendet die Flussvisualisierung, die Fallout-Visualisierung, die Kohortenanalyse, die Metrik für Personen und die Metrik für Unique Geräte."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--web-retention"
>title="Sehen Sie sich an, wer Ihre treuen Benutzer sind und was sie auf Ihrer Site tun."
>abstract="**Dies kann Ihnen** dabei helfen, besser zu verstehen, wie oft die durchschnittliche Person Ihre Site besucht, mit welcher Häufigkeit Besucher zur Site zurückkehren und wie viele Tage zwischen wiederkehrenden Besuchen vergangen sind.<br/>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. analysieren, welcher Inhalt am effektivsten dazu beiträgt, Menschen zurück zur Site zu bringen.<br/>Diese Vorlage verwendet die Metrik Besuche und die Metrik Unique Visitors ."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--audio-consumption-template"
>title="Zeigen Sie Trends und Top-Metriken des Medienaudiokonsums auf allen digitalen Geräten an."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, wie Besucher Audioinhalte auf Ihrer Site konsumieren.<br/>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. analysieren, welche Inhalte am häufigsten konsumiert werden.<br/>Diese Vorlage verwendet die Metrik Besuche und die Metrik Unique Visitors ."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--media-recency-frequency-loyalty"
>title="Zeigen Sie Trends und Top-Metriken des Medienverbrauchs auf allen digitalen Geräten an."
>abstract="**Dies kann Ihnen** dabei helfen, besser zu verstehen, wie oft die durchschnittliche Person Ihre Site besucht, mit welcher Häufigkeit Besucher zur Site zurückkehren und wie viele Tage zwischen wiederkehrenden Besuchen vergangen sind.<br/>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. analysieren, welcher Inhalt am effektivsten dazu beiträgt, Menschen zurück zur Site zu bringen.<br/>Diese Vorlage verwendet die Metrik Besuche und die Metrik Unique Visitors ."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--page-summary-report"
>title="Zeigen Sie die durchschnittliche Zeit an, die Besucher während jedes Besuchs auf Ihrer Site verbringen. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen."
>abstract="**Dies kann Ihnen** helfen, die Interaktionsstufen der Besucher und die Zeitdauer, die Besucher auf der Site verbringen, besser zu verstehen.<br/>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. um zu bewerten, ob Änderungen an Ihrer Site dazu führen, dass Besucher mehr Zeit auf der Site verbringen.<br/>Diese Vorlage verwendet die Dimension Tag und die Metrik Zeit pro Besuch (Sekunden) ."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--reloadsRankedReport"
>title="Zeigt an, wie oft ein Dimensionselement während einer Neuladung vorhanden war. Ein Besucher, der seinen Browser aktualisiert, stellt die häufigste Methode dar, eine Neuladung auszulösen."
>abstract="**Dies kann Ihnen** dabei helfen festzustellen, wann Probleme auf einer bestimmten Seite auftreten können, die einen Besucher dazu auffordern würden, die Seite neu zu laden.<br/>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. um zu beurteilen, welche Seiten Probleme haben, die behoben werden müssen.<br/>Diese Vorlage verwendet die Metrik Neuladungen ."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--timeSpentPageRankedReport"
>title="Zeigen Sie die durchschnittliche Zeit an, die Besucher während jedes Besuchs auf Ihrer Site verbringen. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen."
>abstract="**Dies kann Ihnen** helfen, die Interaktionsstufen der Besucher und die Zeitdauer, die Besucher auf der Site verbringen, besser zu verstehen.<br/>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. um zu bewerten, ob Änderungen an Ihrer Site dazu führen, dass Besucher mehr Zeit auf der Site verbringen.<br/>Diese Vorlage verwendet die Dimension Tag und die Metrik Zeit pro Besuch (Sekunden) ."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--entryPageRankedReport"
>title="Zeigen Sie die wichtigsten Seiten an, auf die Personen beim ersten Besuch Ihrer Site zugreifen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Seiten den meisten Traffic zu Ihrer Site leiten, oder mehr über die ersten Eindrücke zu erfahren, die Besuchende auf Ihrer Site haben.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. das erste Erlebnis optimieren, das Personen auf der Site haben, oder sicherstellen, dass die Seiten, die Personen beim Eintritt in Ihre Site zuerst sehen, einladend sind und die erforderlichen Links zu anderen Bereichen Ihrer Site bereitstellen.<br/>Diese Vorlage verwendet die Metrik „Sitzungen“. Außerdem werden die Balkenvisualisierung und die Freiformtabellen-Visualisierung verwendet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--entryPageOriginalRankedReport"
>title="Zeigen Sie die wichtigsten Seiten an, auf die Besucher während des gesamten Lebenszyklus eines Besuchers beim ersten Besuch Ihrer Site zugreifen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Seiten den meisten Traffic zu Ihrer Site leiten, oder mehr über die ersten Eindrücke zu erfahren, die Besuchende auf Ihrer Site haben.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. das erste Erlebnis optimieren, das Personen auf der Site haben, oder sicherstellen, dass die Seiten, die Personen beim Eintritt in Ihre Site zuerst sehen, einladend sind und die erforderlichen Links zu anderen Bereichen Ihrer Site bereitstellen.<br/>Diese Vorlage verwendet die Metrik „Sitzungen“. Außerdem werden die Balkenvisualisierung und die Freiformtabellen-Visualisierung verwendet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--singlePageVisitsRankedReport"
>title="Zeigen Sie die Anzahl der Besuche an, die aus einer einzigen eindeutigen Seite bestanden."
>abstract="**Dies kann Ihnen** helfen, die Interaktionsstufen der Besucher und die Zeitdauer, die Besucher auf der Site verbringen, besser zu verstehen.<br/>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. um zu bewerten, ob Änderungen an Ihrer Site dazu führen, dass Besucher mehr Zeit auf der Site verbringen.<br/>Diese Vorlage verwendet die Dimension Einzelseitenbesuche ."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--exitPageRankedReport"
>title="Zeigen Sie die wichtigsten Seiten an, auf die Personen unmittelbar vor dem Verlassen Ihrer Site zugreifen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Seiten Personen von der Site wegführen. <br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. gängige Exitpages aktualisieren, um das Erlebnis zu optimieren, das Personen vor dem Verlassen haben, oder Inhalte oder Links aufnehmen, um Personen dazu aufzufordern, auf Ihrer Site zu bleiben.<br/>Diese Vorlage verwendet die Metrik „Sitzungen“. Außerdem werden die Balkenvisualisierung und die Freiformtabellen-Visualisierung verwendet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--sitePerformanceOverview"
>title="Zeigen Sie Leistungsdaten für Ihre Adobe Experience Manager-Site an."
>abstract="**Dies kann Ihnen** dabei helfen, die Wertrealisierung von Adobe Experience Manager besser zu verstehen.<br/>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Ihre Experience Manager-Einstellungen optimieren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--itp-impact"
>title="Auswirkungen von Intelligent Tracking Prevention (ITP) auf die Datenerfassung und -berichterstellung anzeigen und analysieren."
>abstract="**Dies kann Ihnen** dabei helfen, potenzielle Datenverluste aufgrund von durch ITP auferlegten Cookie-Beschränkungen besser zu verstehen.<br/>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Ihre Analyseeinrichtung so anpassen, dass die Auswirkungen von ITP minimiert werden."

<!-- markdownlint-enable MD034 -->

Die folgenden Vorlagen sind verfügbar:

| Vorlagenname | Warum diese Vorlage <!-- What do you do with it? What can it help you learn? and What are the potential actions? --> verwenden |
| --- | --- | 
| [!UICONTROL **Schlüsselmetriken**] | <!--duplicated in Most popular section--> Zeigen Sie einen Bericht an, der die Metriken „Seitenansichten“, „Besuche“ und „Unique Visitors“ nebeneinander anzeigt. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, diese wichtigen Metriken zu vergleichen, um ein vollständigeres Bild über die Anzahl der Unique Visitors auf der Site, die Anzahl der Seitenbesuche und die Anzahl der Sitzungen zu erhalten.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** beliebig viele Dinge tun, z. B. die durchschnittliche Anzahl der Seiten, die jeder Besucher während eines Besuchs auf der Site in einer bestimmten Woche oder in einem bestimmten Monat angesehen hat, und wie sich dies während bestimmter Zeiten des Jahres oder vor und nach der Ausführung von Marketingkampagnen verändert hat. </p><p>Diese Vorlage verwendet die Dimension [Tag ](/help/components/dimensions/day.md), die Metrik [Seitenansichten](/help/components/metrics/page-views.md), die Metrik [Besuche](/help/components/metrics/visits.md) und die Metrik [Unique Visitors](/help/components/metrics/unique-visitors.md).</p> |
| [!UICONTROL **Seitenansichten**] | <!--duplicated in Most popular section-->Zeigen Sie die Gesamtanzahl der Seitenansichten an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, wie der Traffic auf Ihrer Site im Laufe der Zeit möglicherweise zu- oder abnimmt.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne bewerten, indem Sie den Sitetraffic vor und nach dem Start der Kampagne vergleichen. Oder Sie vergleichen den jährlichen Feiertags-Traffic.</p><p>Diese Vorlage verwendet die Dimension [Tag](/help/components/dimensions/day.md) und die Metrik [Seitenansichten](/help/components/metrics/page-views.md).</p> |
| [!UICONTROL **Seiten**] | <!--duplicated in Most popular section-->Identifizieren Sie die beliebtesten und unbeliebtesten Seiten. <p>**Dies kann Ihnen helfen**, Ihre Zielgruppe und die Art von Informationen, die sie am meisten interessiert, besser zu verstehen.</p><p>**Basierend auf dem, was Sie erfahren, können Sie** eine Reihe von Schritten ausführen, z. B. Seitenmetadaten anpassen, um die Sichtbarkeit auf seltener angezeigten Seiten zu erhöhen, oder Zeit in die Verbesserung des Inhalts Ihrer am häufigsten angezeigten Seiten investieren.</p><p>Diese Vorlage verwendet die Dimension [Seite ](/help/components/dimensions/page.md) und die Metrik [Seitenansichten](/help/components/metrics/page-views.md).</p> |
| [!UICONTROL **Besuche**] | <!--duplicated in Most popular section-->Zeigen Sie die Gesamtanzahl der Besuche an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, wie der Traffic auf Ihrer Site im Laufe der Zeit möglicherweise zu- oder abnimmt.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne bewerten, indem Sie den Sitetraffic vor und nach dem Start der Kampagne vergleichen. Oder Sie vergleichen den jährlichen Feiertags-Traffic.</p><p>Diese Vorlage verwendet die Dimension [Tag](/help/components/dimensions/day.md) und die Metrik [Besuche](/help/components/metrics/visits.md).</p> |
| [!UICONTROL **Besucher**] | <!--duplicated in Most popular section-->Zeigen Sie die Gesamtanzahl der Unique Visitors an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, wie die Reichweite und die Zielgruppengröße Ihrer Site im Laufe der Zeit oder im Vergleich mit einem früheren Zeitraum zu- oder abnimmt.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob eine kürzlich gestartete Marketing-Kampagne erfolgreich darin war, neue Personen auf die Site zu locken, indem Sie Unique Visitors vor und nach dem Start der Kampagne vergleichen. Oder Sie können die Anzahl der Personen vergleichen, die die Site jedes Jahr während der Feiertage besuchen.</p><p>Diese Vorlage verwendet die Dimension &quot;[Tag&quot;](/help/components/dimensions/day.md) und die Metrik &quot;[Unique Visitors&quot;](/help/components/metrics/unique-visitors.md).</p> |
| [!UICONTROL **Zeit pro Besuch**] | Zeigen Sie die durchschnittliche Zeit an, die Besucher während jedes Besuchs auf Ihrer Site verbringen. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen** helfen, die Interaktionsstufen der Besucher und die Zeitdauer, die Besucher auf der Site verbringen, besser zu verstehen.</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. um zu bewerten, ob Änderungen an Ihrer Site dazu führen, dass Besucher mehr Zeit auf der Site verbringen.</p><p>Diese Vorlage verwendet die Dimension [Tag](/help/components/dimensions/day.md) und die Metrik [Zeit pro Besuch (Sekunden)](/help/components/metrics/time-spent-per-visit.md).</p> |
| [!UICONTROL **Zeit vor Ereignis**] | Zeigen Sie die durchschnittliche Zeit an, die Benutzer vor einem Erfolgsereignis verbringen. <p>**Dies kann Ihnen** helfen, besser zu verstehen, wie viel Zeit Besucher benötigen, um eine gewünschte Aktion durchzuführen, z. B. einen Kauf vorzunehmen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob Änderungen an Ihrer Site es den Besuchenden erleichtert, schnell ein Erfolgsereignis zu erreichen.</p><p>Diese Vorlage verwendet die Dimension [Zeit vor Ereignis](/help/components/dimensions/time-prior-to-event.md) und die Metrik [Unique Visitors](/help/components/metrics/unique-visitors.md).</p> |
| [!UICONTROL **Site-Abschnitte**] | <!--duplicated in Most popular section-->Zeigen Sie die beliebtesten oder leistungsstärksten Bereiche Ihrer Site an. <p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Bereiche Ihrer Site am häufigsten besucht werden.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, welche Ihrer Produkte oder Services das meiste Interesse generieren.</p> <p>Diese Vorlage verwendet die Dimension [Sitebereich](/help/components/dimensions/site-section.md) und die Metrik [Besuche](/help/components/metrics/visits.md).</p> |
| [!UICONTROL **Echtzeit**] | Zeigen Sie die Dimensionen und Metriken an, die derzeit auf Ihrer Site erfasst werden. <p>**Dies kann Ihnen** helfen, die Trends auf Ihrer Site besser zu verstehen.</p><p>**Je nach Ihren Erkenntnissen können Sie** auf die Leistung Ihrer aktuellen Marketing-Inhalte und -Kampagnen reagieren und diese aktiv verwalten.</p> <p>Diese Vorlage verwendet den [Echtzeitbericht](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime.md).</p> |
| [!UICONTROL **Verbrauch von Webinhalten**] | Zeigen Sie an, welche Web-Inhalte am häufigsten genutzt werden und für Benutzende interessant sind.<p>**Dies kann Ihnen helfen**, besser zu verstehen, wo Personen beim ersten Aufrufen der Site hingehen, welche Bereiche der Site von Personen am häufigsten besucht werden und welche Seiten Personen am wahrscheinlichsten von der Site wegführen.</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. feststellen, welche Pfade auf der Site Menschen zu den wichtigsten Seiten führen und welche Seiten die Besucher wahrscheinlicher von der Site wegführen <!-- not sure about these takeaways... -->.</p> <p>Diese Vorlage verwendet die [Dimension &quot;Seite&quot;](/help/components/dimensions/page.md) und die Metrik [Seitenansichten](/help/components/metrics/page-views.md), die Metrik [Besuche](/help/components/metrics/visits.md), die Metrik [Unique Visitors](/help/components/metrics/unique-visitors.md), die Metrik [Einstiegsrate](/help/components/metrics/entries.md), die Metrik [Absprungrate](/help/components/metrics/bounce-rate.md), die Metrik [Ausstiegsrate](/help/components/metrics/exits.md) und [Content-Geschwindigkeit-Metrik](/help/components/metrics/content-velocity.md). Außerdem werden [Flussvisualisierungen](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) für Einstiegs-, Ausstiegs- und oberste Abschnitte verwendet.</p> |
| [!UICONTROL **Verbrauch von Medieninhalten**] | Zeigen Sie an, welche Medieninhalte am häufigsten genutzt werden und für Benutzende interessant sind.<p>**Dies kann Ihnen helfen**, besser zu verstehen, wo Personen beim ersten Aufrufen der Site hingehen, welche Bereiche der Site von Personen am häufigsten besucht werden und welche Seiten Personen am wahrscheinlichsten von der Site wegführen.</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. feststellen, welche Pfade auf der Site Menschen zu den wichtigsten Seiten führen und welche Seiten die Besucher wahrscheinlicher von der Site wegführen <!-- not sure about these takeaways... -->.</p> <p>Diese Vorlage verwendet die [Dimension &quot;Seite&quot;](/help/components/dimensions/page.md) und die Metrik [Seitenansichten](/help/components/metrics/page-views.md), die Metrik [Besuche](/help/components/metrics/visits.md), die Metrik [Unique Visitors](/help/components/metrics/unique-visitors.md), die Metrik [Einstiegsrate](/help/components/metrics/entries.md), die Metrik [Absprungrate](/help/components/metrics/bounce-rate.md), die Metrik [Ausstiegsrate](/help/components/metrics/exits.md) und [Content-Geschwindigkeit-Metrik](/help/components/metrics/content-velocity.md). Außerdem werden [Flussvisualisierungen](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) für Einstiegs-, Ausstiegs- und oberste Abschnitte verwendet; eine [Startdiagrammvisualisierung](/help/analyze/analysis-workspace/visualizations/scatterplot.md), die Seitenansichten für die häufigsten Seiten anzeigt; eine [Balkenvisualisierung](/help/analyze/analysis-workspace/visualizations/bar.md), die Seitenansichten nach Zusammenfassungszeit anzeigt; und eine [Linienvisualisierung](/help/analyze/analysis-workspace/visualizations/line.md), die eine Trendansicht der durchschnittlichen Besuchszeit auf der Site anzeigt.</p> |
| [!UICONTROL **Nächster und vorheriger Seitenfluss**] | Sehen Sie sich die häufigsten Orte an, an denen Besucher vor oder nach dem Besuch eines bestimmten Ortes reisen.<p>**Dies kann Ihnen** helfen, besser zu verstehen, wo Personen nach dem ersten Sitebesuch auftauchen, welche Bereiche der Site von den Besuchern am häufigsten besucht werden und welche Seiten am ehesten besucht werden, bevor sie die Site verlassen.</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. feststellen, welche Pfade auf der Site Menschen zu den wichtigsten Seiten führen und welche Seiten die Besucher wahrscheinlicher von der Site wegführen <!-- not sure about these takeaways... -->.</p> <p>Diese Vorlage verwendet die [Dimension &quot;Seite&quot;](/help/components/dimensions/page.md) und die Metrik [Seitenansichten](/help/components/metrics/page-views.md), die Metrik [Besuche](/help/components/metrics/visits.md), die Metrik [Unique Visitors](/help/components/metrics/unique-visitors.md), die Metrik [Einstiegsrate](/help/components/metrics/entries.md), die Metrik [Absprungrate](/help/components/metrics/bounce-rate.md), die Metrik [Ausstiegsrate](/help/components/metrics/exits.md) und [Content-Geschwindigkeit-Metrik](/help/components/metrics/content-velocity.md). Außerdem werden [Flussvisualisierungen](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) für Einstiegs-, Ausstiegs- und oberste Abschnitte verwendet, eine [Streudiagrammdarstellung](/help/analyze/analysis-workspace/visualizations/scatterplot.md), die Seitenansichten für die häufigsten Seiten anzeigt, eine [Balkendiagrammdarstellung](/help/analyze/analysis-workspace/visualizations/bar.md), die Seitenansichten nach Zusammenfassungszeit anzeigt, und eine [Linienvisualisierung](/help/analyze/analysis-workspace/visualizations/line.md), die eine Trendansicht der durchschnittlichen Besuchszeit auf der Site anzeigt.</p> |
| [!UICONTROL **Fallout**] | Sehen Sie sich an, wo Benutzer eine vordefinierte Seitensequenz verlassen oder wie sie weitermachen.<p>**Dies kann Ihnen** helfen, besser zu verstehen, wo Personen aus der Journey fallen.</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Konversionsraten durch bestimmte Prozesse auf Ihrer Site analysieren (z. B. einen Kauf- oder Registrierungsprozess) oder Korrelationen zwischen Ereignissen auf Ihrer Site analysieren. (Zum Beispiel, welcher Prozentsatz der Personen, die sich Ihre Datenschutzrichtlinien angesehen haben, ein Produkt kauften.) Sie können diese Vorlage auch verwenden, um zwei verschiedene Segmente im selben Bericht nebeneinander zu vergleichen.</p> <p>Diese Vorlage verwendet die [Fallout-Visualisierung](/help/analyze/analysis-workspace/visualizations/fallout/fallout-flow.md).</p> |
| [!UICONTROL **Geräteübergreifende Analyse**] | Anzeigen der Geräte, die an allen Punkten des Journey verwendet werden<p>**Dies kann Ihnen** helfen, besser zu verstehen, wie viele Personen mit Ihrer Marke interagieren, welche Arten von Geräten sie verwenden und wie ihre Verwendung mehrerer Geräte deren Erlebnis beeinflusst. Wie oft beginnen Personen beispielsweise eine Aufgabe auf einem Mobilgerät und wechseln dann später zu einem Desktop, um eine Aufgabe abzuschließen? Welche sind die häufigsten Pfade, die Benutzer beim Wechsel von einem Gerät zum anderen verwenden? Wo steigen sie aus? Wo sind sie erfolgreich? Und so weiter.</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. bestimmte Teile der Benutzer-Journey für ein mobiles Erlebnis optimieren.</p> <p>Diese Vorlage verwendet die Metrik [Flussvisualisierung](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md), [Trichteranalyse-Visualisierung](/help/analyze/analysis-workspace/visualizations/fallout/fallout-flow.md), [Kohortenanalyse](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md), [Metrik &quot;Personen&quot;](/help/components/metrics/people.md) und [Metrik &quot;Eindeutige Geräte&quot;](/help/components/metrics/unique-devices.md).</p> |
| [!UICONTROL **Webbeibehaltung**] | Sehen Sie sich an, wer Ihre treuen Benutzer sind und was sie auf Ihrer Site tun.<p>**Dies kann Ihnen** dabei helfen, besser zu verstehen, wie oft die durchschnittliche Person Ihre Site besucht, mit welcher Häufigkeit Besucher zur Site zurückkehren und wie viele Tage zwischen wiederkehrenden Besuchen vergangen sind.</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. analysieren, welcher Inhalt am effektivsten dazu beiträgt, Menschen zurück zur Site zu bringen.<p>Diese Vorlage verwendet die Metrik [Besuche](/help/components/metrics/visits.md) und die Metrik [Unique Visitors](/help/components/metrics/unique-visitors.md).</p> |
| [!UICONTROL **Medien-Audionutzung**] | Zeigen Sie Trends und Top-Metriken des Medienaudiokonsums auf allen digitalen Geräten an.<p>**Dies kann Ihnen** helfen, besser zu verstehen, wie Besucher Audioinhalte auf Ihrer Site konsumieren.</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. analysieren, welche Inhalte am häufigsten konsumiert werden.<p>Diese Vorlage verwendet die Metrik [Besuche](/help/components/metrics/visits.md) und die Metrik [Unique Visitors](/help/components/metrics/unique-visitors.md).</p> |
| [!UICONTROL **Medienneuigkeit, Häufigkeit, Treue**] | Zeigen Sie Trends und Top-Metriken des Medienverbrauchs auf allen digitalen Geräten an.<p>**Dies kann Ihnen** dabei helfen, besser zu verstehen, wie oft die durchschnittliche Person Ihre Site besucht, mit welcher Häufigkeit Besucher zur Site zurückkehren und wie viele Tage zwischen wiederkehrenden Besuchen vergangen sind.</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. analysieren, welcher Inhalt am effektivsten dazu beiträgt, Menschen zurück zur Site zu bringen.<p>Diese Vorlage verwendet die Metrik [Besuche](/help/components/metrics/visits.md) und die Metrik [Unique Visitors](/help/components/metrics/unique-visitors.md).</p> |
| **[!UICONTROL Seitenanalyse]** > [!UICONTROL **Seitenzusammenfassung**] | Zeigen Sie die durchschnittliche Zeit an, die Besucher während jedes Besuchs auf Ihrer Site verbringen. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen** helfen, die Interaktionsstufen der Besucher und die Zeitdauer, die Besucher auf der Site verbringen, besser zu verstehen.</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. um zu bewerten, ob Änderungen an Ihrer Site dazu führen, dass Besucher mehr Zeit auf der Site verbringen.</p><p>Diese Vorlage verwendet die Dimension [Tag](/help/components/dimensions/day.md) und die Metrik [Zeit pro Besuch (Sekunden)](/help/components/metrics/time-spent-per-visit.md).</p> |
| **[!UICONTROL Seitenanalyse]** > [!UICONTROL **Neuladungen**] | Zeigt an, wie oft ein Dimensionselement während einer Neuladung vorhanden war. Ein Besucher, der seinen Browser aktualisiert, stellt die häufigste Methode dar, eine Neuladung auszulösen. <p>**Dies kann Ihnen** dabei helfen festzustellen, wann Probleme auf einer bestimmten Seite auftreten können, die einen Besucher dazu auffordern würden, die Seite neu zu laden.</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. um zu beurteilen, welche Seiten Probleme haben, die behoben werden müssen.</p><p>Diese Vorlage verwendet die Metrik [Neuladungen](https://experienceleague.adobe.com/en/docs/analytics/components/metrics/reloads).</p> |
| **[!UICONTROL Seitenanalyse]** > [!UICONTROL **Besuchszeit pro Seite**] | Zeigen Sie die durchschnittliche Zeit an, die Besucher während jedes Besuchs auf Ihrer Site verbringen. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen** helfen, die Interaktionsstufen der Besucher und die Zeitdauer, die Besucher auf der Site verbringen, besser zu verstehen.</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. um zu bewerten, ob Änderungen an Ihrer Site dazu führen, dass Besucher mehr Zeit auf der Site verbringen.</p><p>Diese Vorlage verwendet die Dimension [Tag](/help/components/dimensions/day.md) und die Metrik [Zeit pro Besuch (Sekunden)](/help/components/metrics/time-spent-per-visit.md).</p> |
| **[!UICONTROL Einstiege und Ausstiege]** > [!UICONTROL **Entrypages**] | Zeigen Sie die wichtigsten Seiten an, auf die Benutzer während einer bestimmten Sitzung beim ersten Besuch Ihrer Site zugreifen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Seiten den meisten Traffic zu Ihrer Site leiten, oder mehr über die ersten Eindrücke zu erfahren, die Besuchende auf Ihrer Site haben.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. das erste Erlebnis optimieren, das Personen auf der Site haben, oder sicherstellen, dass die Seiten, die Personen beim Eintritt in Ihre Site zuerst sehen, einladend sind und die erforderlichen Links zu anderen Bereichen Ihrer Site bereitstellen.</p><p>Diese Vorlage verwendet die Metrik Sitzungen . Außerdem werden die Balkenvisualisierung und die Freiformtabellen-Visualisierung verwendet.</p> |
| **[!UICONTROL Einstiege und Ausstiege]** > [!UICONTROL **Ursprüngliche Entrypages**] | Zeigen Sie die wichtigsten Seiten an, auf die Besucher während des gesamten Lebenszyklus eines Besuchers beim ersten Besuch Ihrer Site zugreifen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Seiten den meisten Traffic zu Ihrer Site leiten, oder mehr über die ersten Eindrücke zu erfahren, die Besuchende auf Ihrer Site haben.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. das erste Erlebnis optimieren, das Personen auf der Site haben, oder sicherstellen, dass die Seiten, die Personen beim Eintritt in Ihre Site zuerst sehen, einladend sind und die erforderlichen Links zu anderen Bereichen Ihrer Site bereitstellen.</p><p>Diese Vorlage verwendet die Metrik Sitzungen . Außerdem werden die Balkenvisualisierung und die Freiformtabellen-Visualisierung verwendet.</p> |
| **[!UICONTROL Einstiege und Ausstiege]** > [!UICONTROL **Einzelseitenbesuche**] | Zeigen Sie die Anzahl der Besuche an, die aus einer einzigen eindeutigen Seite bestanden. <p>**Dies kann Ihnen** helfen, die Interaktionsstufen der Besucher und die Zeitdauer, die Besucher auf der Site verbringen, besser zu verstehen.</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. um zu bewerten, ob Änderungen an Ihrer Site dazu führen, dass Besucher mehr Zeit auf der Site verbringen.</p><p>Diese Vorlage verwendet die Dimension [Einzelseitenbesuche](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/single-page-visits).</p> |
| **[!UICONTROL Einstiege und Ausstiege]** > [!UICONTROL **Ausstiegsseiten**] | Zeigen Sie die wichtigsten Seiten an, auf die Personen unmittelbar vor dem Verlassen Ihrer Site zugreifen.<p>**Dies kann Ihnen** helfen, besser zu verstehen, welche Seiten Personen von der Site wegführen. </p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. gängige Exitpages aktualisieren, um das Erlebnis zu optimieren, das Personen vor dem Verlassen haben, oder Inhalte oder Links aufnehmen, um Personen dazu aufzufordern, auf Ihrer Site zu bleiben.</p><p>Diese Vorlage verwendet die Metrik Sitzungen . Außerdem werden die Balkenvisualisierung und die Freiformtabellen-Visualisierung verwendet.</p> |
| [!UICONTROL **AEM**] > [!UICONTROL **Site-Leistung**] > [!UICONTROL **AEM Site-Leistung**] | Zeigen Sie Leistungsdaten für Ihre Adobe Experience Manager-Site an.  <p>**Dies kann Ihnen** dabei helfen, die Wertrealisierung von Adobe Experience Manager besser zu verstehen.</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Ihre Experience Manager-Einstellungen optimieren.</p> |
| [!UICONTROL **ITP-Auswirkung**] | Auswirkungen von Intelligent Tracking Prevention (ITP) auf die Datenerfassung und -berichterstellung anzeigen und analysieren. <p>**Dies kann Ihnen** dabei helfen, potenzielle Datenverluste aufgrund von durch ITP auferlegten Cookie-Beschränkungen besser zu verstehen.</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Ihre Analyseeinrichtung so anpassen, dass die Auswirkungen von ITP minimiert werden.</p> |




Unten ignorieren

| Menüelement | Berichte unter diesem Menüelement |
| --- | --- | 
| **[!UICONTROL Beliebteste]** | <ul><li>Schulungs-Tutorial (Vorhandene Vorlage für Arbeitsbereich)</li><li>Seiten (Was sind meine Top-Seiten?)</li><li>Seitenansichten (Wie viele Seitenaufrufe erzeuge ich?)</li><li>Besuche (Wie viele Besuche erhalte ich?)</li><li>Besucher (Wie viele Besucher bekomme ich?)</li><li>Schlüsselmetriken (Wie sehen meine wichtigsten Kennzahlen aus?)</li><li>Website-Abschnitte (Welche Abschnitte meiner Website generierten die meisten Seitenansichten?)</li><li>Echtzeit (Was liegt auf meiner Website im Trend und warum?)</li><li>Nächste Seite (Auf welche Seiten gehen meine Besucher als Nächstes?)</li><li>Vorherige Seite (Welche vorherigen Seiten haben meine Besucher aufgerufen?)</li><li>Kampagnen (Welche Kampagnen liegen meinen Schlüsselmetriken zugrunde?)</li><li>Produkte (Welche Produkte liegen meinen Schlüsselmetriken zugrunde?)</li><li>Letztkontakt-Kanal (Welcher Letztkontakt-Kanal erzielt die beste Leistung?)</li><li>Letztkontakt-Kanaldetail (Welcher spezifische Letztkontakt-Kanal ist leistungsstärker als andere?)</li><li>Umsatz (Wie entwickelt sich mein Umsatz?)</li><li>Bestellungen (Wie entwickeln sich meine Bestellungen?)</li><li>Einheiten (Wie viele Einheiten verkaufe ich?)</li></ul> |
| **[!UICONTROL Interaktion]** | <ul><li>Schlüsselmetriken (Wie sehen meine wichtigsten Kennzahlen aus?)</li><li>Seitenansichten (Wie viele Seitenaufrufe erzeuge ich?)</li><li>Seiten (Was sind meine Top-Seiten?)</li><li>Besuche (Wie viele Besuche erhalte ich?)</li><li>Besucher (Wie viele Besucher bekomme ich?)</li><li>Zeit pro Besuch (Wie viel Zeit verbringen meine Benutzer pro Besuch?)</li><li>Zeit vor Ereignis (Wie viel Zeit verbringen meine Benutzer vor einem Erfolgsereignis?)</li><li>Site-Bereiche (Welche Bereiche meiner Site generierten die meisten Seitenansichten?</li><li>Nutzung von Web-Inhalten (Welche Inhalte werden am häufigsten genutzt und sind für Benutzer interessant?)</li><li>Nutzung von Medieninhalten (Welche Inhalte werden am häufigsten genutzt und sind für Benutzer interessant?)</li><li>Fluss zur nächsten/vorherigen Seite (Was sind/waren die nächsten/vorherigen Pfade, die meine Besucher nutzen/genutzt haben?)</li><li>Fallout (Wo sehe ich Fallout für meine digitalen Eigenschaften?)</li><li>Geräteübergreifende Analyse (Verwendung geräteübergreifender Analysen in Analysis Workspace)</li><li>Web-Bindungsgrad (Wer sind meine treuen Benutzer und was tun sie?)</li><li>Medien-Audiokonsum (Was sind Trends und Top-Metriken beim Audiokonsum?)</li><li>Medien-Neuigkeit, -Häufigkeit, -Treue (Wer sind meine treuen Leser?)</li><li>Seitenanalyse > Neuladungen (Welche Seiten werden am häufigsten neu geladen?)</li><li>Seitenanalyse > Besuchszeit pro Seite (Wie viel Zeit verbringen meine Benutzer auf meinen Seiten?)</li><li>Einstiege und Ausstiege > Einstiegsseiten (Was sind meine Top-Einstiegsseiten?)</li><li>Einstiege und Ausstiege > Ursprüngliche Einstiegsseiten (Auf welcher Seite ist mein Besucher ursprünglich eingetreten?)</li><li>Einstiege und Ausstiege > Einzelseitenbesuche (Welche Seiten haben die meisten Einzelseitenbesuche generiert?)</li><li>Einstiege und Ausstiege > Ausstiegseiten (Was sind meine Top-Ausstiegsseiten?)</li><li>Seitenanalyse > Seitenzusammenfassung</li></ul> |
| **[!UICONTROL Konversion]** | <ul><li>Produkte > Produkte (Welche Produkte liegen meinen Schlüsselmetriken zugrunde?)</li><li>Produkte > Produktleistung (Welche Produkte schneiden am besten ab?)</li><li>Produkte > Kategorien (Was sind meine leistungsstärksten Produktkategorien?)</li><li>Warenkorb > Warenkörbe (Wie viele Benutzer haben ein Produkt zum Warenkorb hinzugefügt?)</li><li>Warenkorb > Warenkorbansichten (Wie oft haben meine Besucher ihren Warenkorb angesehen?)</li><li>Warenkorb > Zusatz zum Warenkorb (Wie oft fügen Benutzer ihrem Warenkorb ein Produkt hinzu?)</li><li>Warenkorb > Entnahme aus Warenkorb (Wie oft entfernen Benutzer ein Produkt aus ihrem Warenkorb?)</li><li>Einkäufe > Umsatz (Wie sieht mein Umsatz aus?)</li><li>Einkäufe > Bestellungen (Wie sehen meine Bestellungen aus?)</li><li>Käufe > Einheiten (Wie viele Einheiten verkaufe ich?)</li><li>[Magento: Marketing und Commerce](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#commerce)</li></ul> |
| **[!UICONTROL Zielgruppe]** | <ul><li>Personenmetrik (Wie viele Personen interagieren mit meiner Marke?)</li><li>Besucherprofil > Standortübersicht (Welche Standorte werden von Benutzern am meisten genutzt?)</li><li>Besucherprofil > GeoSegmentation > Geo-Länder, Geo-US-Bundesstaaten, Geo-Regionen, Geo-Städte, Geo-US-DMA (Aus welchen Regionen besuchen mich meine Benutzer?)</li><li>Besucherprofil > Sprachen (Welche Sprache bevorzugen meine Benutzer?)</li><li>Besucherprofil > Zeitzonen (Aus welchen Zeitzonen kommen meine Benutzer?)</li><li>Besucherprofil > Domains (Welche ISPs werden von meinen Besuchern verwendet, um auf meine Site zuzugreifen?)</li><li>Besucherprofil > Domains auf oberster Ebene (Welche Domains leiten den Traffic zu meiner Site?)</li><li>Besucherprofil > Technologie > Technologieübersicht (Welche Technologien werden verwendet, um auf meine Site zuzugreifen?)</li><li>Besucherprofil > Technologie > Browser, Browser-Typ, Browser-Breite, Browser-Höhe (welcher Browser, welche Browser-Version des Unternehmens und welche Breite und Höhe werden von Benutzern verwendet, um auf meine Site zuzugreifen?)</li><li>Besucherprofil > Technologie > Betriebssystem, Betriebssystemtypen (Welches Betriebssystem und welche Version davon verwenden meine Besucher?)</li><li>Besucherprofil > Technologie > Mobilnetzbetreiber (Welche Mobilnetzbetreiber verwenden meine Besucher, um auf meine Site zuzugreifen?)</li><li>Besuchertreue > Rückkehrhäufigkeit (Wie viel Zeit vergeht zwischen dem aktuellen Besuch meines Benutzers und vorherigen Besuchen?)</li><li>Besuchertreue > Erneute Besuche (Wie viele meiner Besucher kehren zurück?)</li><li>Besuchertreue > Besuchsnummer (Welcher Besuchsnummernbehälter liegt den meisten meiner Schlüsselmetriken zugrunde?)</li><li>Besucherbindung > Verkaufszyklus > Kundentreue (Zu welchem Treuesegment gehören meine Benutzer?)</li><li>Besucherbindung > Verkaufszyklus > Tage bis Erstkauf (Wie viele Tage sind zwischen dem ersten Besuch meiner Benutzer und dem ersten Kauf vergangen?)</li><li>Besucherbindung > Verkaufszyklus > Tage seit letztem Kauf (Wie viele Tage sind zwischen dem aktuellen Besuch meiner Benutzer und ihrem letzten Kauf vergangen? )</li><li>Besuchertreue > Mobile > Geräte und Gerätetypen (Welche Geräte und Gerätetypen verwenden meine Besucher?)</li><li>Besucherbindung > Mobile > Hersteller (Welchen Mobilgerätehersteller verwenden meine Besucher?)</li><li>Besuchertreue > Mobile > Bildschirmgröße, Bildschirmhöhe, Bildschirmbreite (Welche Bildschirmgröße/-höhe/-breite für Mobilgeräte verwenden meine Besucher?)</li><li>Besucherbindung > Mobile > [Mobile-App-Nutzung](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#mobile)</li><li>Besucherbindung > Mobile > [Mobile-App-Journey](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#mobile)</li><li>Besucherbindung > Mobile > [Mobile-App-Metriken](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#mobile)</li><li>Besucherbindung > Mobile > [Mobile-App-Nachrichten](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#mobile)</li><li>Besuchertreue > Mobile > [Leistung von Mobile Apps](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#mobile)</li><li>Besucherbindung > Mobile > [Bindung durch Mobile Apps](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#mobile)</li></ul> |
| **[!UICONTROL Akquise]** | <ul><li>Marketing-Kanäle > Erstkontakt-Kanal, Details zum Erstkontakt-Kanal (Welcher Erstkontakt-Kanal und welcher spezifische Erstkontakt-Kanal schneidet am besten ab?)</li><li>Marketing-Kanäle > Erster letzter Kanal, Details des ersten letzten Kanals (Welcher Letztkontakt-Kanal und welcher spezifische Letztkontakt-Kanal schneidet am besten ab?)</li><li>Kampagnen > Kampagnen (Welche Kampagnen liegen meinen Schlüsselmetriken zugrunde?)</li><li>Kampagnen > Kampagnenleistung (Welche Kampagnen erzielen den höchsten Umsatz?)</li><li>Kampagnen > Trackingcode (Welche Kampagnen-Trackingcodes erzielen die besten Ergebnisse?)</li><li>[Web-Akquise](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#web)</li><li>[Mobile-Akquise](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#mobile)</li><li>[Advertising Analytics: Paid Search](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#advertising)</li><li>Suchbegriffe – alle, gebührenpflichtig, kostenlos (Welche Suchbegriffe und gebührenpflichtigen/kostenlosen Suchbegriffe bringen meine Schlüsselmetriken am besten voran?)</li><li>Suchmaschinen – alle, gebührenpflichtig, kostenlos (Welche Suchmaschinen und gebührenpflichtigen/kostenlosen Suchmaschinen bringen meine Schlüsselmetriken am besten voran?)</li><li>Ranking aller Suchseiten (Von welcher Suchseite aus besuchen mich meine Benutzer?)</li><li>Verweisende Domains (Von welchen Domains kommt der Traffic auf meine Seite?)</li><li>Ursprüngliche verweisende Domain (Was waren die ersten Domains, auf denen sich Benutzer vor dem Besuch meiner Site befanden?)</li><li>Referrer (Auf welchen URLs waren meine Benutzer, bevor sie sich zu meiner Website durchgeklickt haben?)</li><li>Referrer-Typen (Zu welcher Kategorie gehören die auf mich verweisenden URLs?)</li></ul> |

### Konversion  {#web-conversion}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--productConversionReport"
>title="Vorlage für Produkt-Konversionstrichter"
>abstract=""

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--retail-products-template"
>title="Zeigen Sie die Produkte mit der höchsten Leistung."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Produkte am erfolgreichsten sind.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Finanzierung für erfolgreiche Produkte erhöhen und für weniger erfolgreiche Produkte verringern.<br/>Diese Vorlage verwendet die Metriken „Produktansichten“, „Zusatz zum Warenkorb“, „Bestellungen“, „Umsatz“ und „Einheiten“. Außerdem wird die Dimension „Produkt“ verwendet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--categoryRankedReport"
>title="."
>abstract=""

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--cartConversionReport"
>title="Sehen Sie sich an, wie oft Personen wichtige Checkout-Ereignisse ausgeführt haben, z. B. Hinzufügen von Artikeln zum Warenkorb, Anzeigen des Warenkorbs, Entfernen von Artikeln aus dem Warenkorb und Checkout-Vorgänge."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Teile des Checkout-Prozess-Trichters zu einer Konversion führen und welche eher zum Warenkorbabbruch führen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Reibung bei bestimmten Schritten des Checkout-Prozesses reduzieren.<br/>Diese Vorlage verwendet die"

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--cartsOvertimeReport"
>title="Zeigen Sie die Anzahl der Personen an, die ein Produkt zum Warenkorb hinzugefügt haben."
>abstract="**Dies kann Ihnen dabei helfen**, die Anzahl der Personen besser zu verstehen, die ein Produkt zum Warenkorb hinzufügen, im Gegensatz zur Gesamtzahl der Produkte, die zum Warenkorb hinzugefügt werden.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität Ihrer Produktseiten messen.<br/>Diese Vorlage verwendet die Metrik „Warenkörbe“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--cartViewsOvertimeReport"
>title="Zeigen Sie an, wie oft Personen ihren Warenkorb angezeigt haben."
>abstract="**Dies kann Ihnen dabei helfen**, das Checkout-Erlebnis besser zu verstehen, um die Warenkorbabbruch-Raten zu reduzieren oder die Zeit zwischen Warenkorbergänzungen und Checkouts für verschiedene Produkte zu analysieren.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Aktionen für Produkte anbieten, die am längsten im Warenkorb bleiben und das größte Risiko für einen Abbruch aufweisen.<br/>Diese Vorlage verwendet die Metrik „Warenkorbansichten“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--cartAdditionsOvertimeReport"
>title="Zeigen Sie an, wie häufig Personen etwas zum Warenkorb hinzugefügt haben."
>abstract="**Dies kann Ihnen helfen**, den Teil des Konversionstrichters besser zu verstehen, in dem das Kundeninteresse an einem Produkt so hoch ist, dass es zum Warenkorb hinzugefügt wird.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Produktempfehlungen für alle Kundinnen und Kunden verbessern. Dazu können Sie analysieren, welche Produkte häufig demselben Warenkorb hinzugefügt werden, und ähnliche Produkte auf der Grundlage von Artikeln vorschlagen, die bereits im Warenkorb enthalten sind."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--cartRemovalsOvertimeReport"
>title="Zeigen Sie an, wie oft Personen etwas aus dem Warenkorb entfernt haben."
>abstract="**Dies kann Ihnen dabei helfen**, den Teil des Konversionstrichters besser zu verstehen, in dem Kundschaft kein Interesse mehr an einem Produkt hat, oder zu verstehen, wo im Checkout-Prozess möglicherweise Probleme auftreten.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. potenzielle Barrieren beseitigen, die im Checkout-Prozess bestehen könnten, wie ein kompliziertes Kundenerlebnis.<br/>Diese Vorlage verwendet die Metrik „Entnahmen aus Warenkorb“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--purchaseConversionReport"
>title="Vorlage für Einkaufskonversionstrichter"
>abstract=""

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--commerce-and-marketing-management"
>title="Zeigen Sie vorgefertigte Einblicke für Einzelhändler in Ihre Commerce-Aktivitäten an, um den Umsatz zu verbessern. Dies richtet sich an Nutzer von Magento, kann aber von jedem Online-Händler genutzt werden."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, wie Ihre Commerce-Aktivitäten zu den Verkaufszahlen beitragen.<br/>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Budgets an Aktivitäten anpassen, die den meisten ROI erzielen."

<!-- markdownlint-enable MD034 -->

Die folgenden Vorlagen sind verfügbar:

| Vorlagenname | Warum diese Vorlage <!-- What do you do with it? What can it help you learn? and What are the potential actions? --> verwenden |
| --- | --- | 
| [!UICONTROL **Produktkonversionstrichter**] | <p>**Dies hilft Ihnen**, besser zu verstehen</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. </p><p>Diese Vorlage verwendet die |
| **Produkte** | Zeigen Sie an, auf welche Produkte Schlüsselmetriken wie Topverkäufe oder am häufigsten angezeigte Produkte verweisen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Produkte am erfolgreichsten sind.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Finanzierung für erfolgreiche Produkte erhöhen und für weniger erfolgreiche Produkte verringern.</p><p>Diese Vorlage verwendet die Metrik Bestellungen und die Dimension Produkt . |
| **Produktleistung** | Zeigen Sie die Produkte mit der höchsten Leistung.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Produkte am erfolgreichsten sind.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Finanzierung für erfolgreiche Produkte erhöhen und für weniger erfolgreiche Produkte verringern.</p><p>Diese Vorlage verwendet die Metriken Produktansichten, Zusatz zum Warenkorb, Bestellungen, Umsatz und Einheiten . Außerdem wird die Dimension „Produkt“ verwendet. |
| **Kategorien** |  |
| **Umrechnungstrichter für Warenkorb** | Sehen Sie sich an, wie oft Personen wichtige Checkout-Ereignisse ausgeführt haben, z. B. Hinzufügen von Artikeln zum Warenkorb, Anzeigen des Warenkorbs, Entfernen von Artikeln aus dem Warenkorb und Checkout-Vorgänge. <p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Teile des Checkout-Prozess-Trichters zu einer Konversion führen und welche eher zum Warenkorbabbruch führen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Reibung bei bestimmten Schritten des Checkout-Prozesses reduzieren.</p><p>Diese Vorlage verwendet die |
| **Warenkorb** | Zeigen Sie die Anzahl der Personen an, die ein Produkt zum Warenkorb hinzugefügt haben.<p>**Dies kann Ihnen dabei helfen**, die Anzahl der Personen besser zu verstehen, die ein Produkt zum Warenkorb hinzufügen, im Gegensatz zur Gesamtzahl der Produkte, die zum Warenkorb hinzugefügt werden.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität Ihrer Produktseiten messen.</p><p>Diese Vorlage verwendet die Metrik Warenkorb . |
| **Warenkorbansicht** | Zeigen Sie an, wie oft Personen ihren Warenkorb angezeigt haben. <p>**Dies kann Ihnen dabei helfen**, das Checkout-Erlebnis besser zu verstehen, um die Warenkorbabbruch-Raten zu reduzieren oder die Zeit zwischen Warenkorbergänzungen und Checkouts für verschiedene Produkte zu analysieren.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Aktionen für Produkte anbieten, die am längsten im Warenkorb bleiben und das größte Risiko für einen Abbruch aufweisen.</p><p>Diese Vorlage verwendet die Metrik Warenkorbansichten . |
| **Zusatz zum Warenkorb** | Zeigen Sie an, wie häufig Personen etwas zum Warenkorb hinzugefügt haben. <p>**Dies kann Ihnen helfen**, den Teil des Konversionstrichters besser zu verstehen, in dem das Kundeninteresse an einem Produkt so hoch ist, dass es zum Warenkorb hinzugefügt wird.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Produktempfehlungen für alle Kundinnen und Kunden verbessern. Dazu können Sie analysieren, welche Produkte häufig demselben Warenkorb hinzugefügt werden, und ähnliche Produkte auf der Grundlage von Artikeln vorschlagen, die bereits im Warenkorb enthalten sind. |
| **Entnahme aus Warenkorb** | Zeigen Sie an, wie oft Personen etwas aus dem Warenkorb entfernt haben.<p>**Dies kann Ihnen dabei helfen**, den Teil des Konversionstrichters besser zu verstehen, in dem Kundschaft kein Interesse mehr an einem Produkt hat, oder zu verstehen, wo im Checkout-Prozess möglicherweise Probleme auftreten.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. potenzielle Barrieren beseitigen, die im Checkout-Prozess bestehen könnten, wie ein kompliziertes Kundenerlebnis.</p><p>Diese Vorlage verwendet die Metrik Entnahme aus Warenkorb . |
| **Einkaufskonversionstrichter** | <p>**Dies hilft Ihnen**, besser zu verstehen</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. </p><p>Diese Vorlage verwendet die |
| **Umsatz** | <!--duplicated in Most popular section-->Zeigen Sie den Geldbetrag der bei allen Bestellungen gekauften Produkte an.<p>**Dies kann Ihnen** dabei helfen, besser zu verstehen, welche Dimensionselemente zum Umsatz beigetragen haben, indem die Umsatzmetrik mit einer beliebigen Dimension kombiniert wird. Sie könnten beispielsweise die Top-Kampagnen (unter Verwendung der Dimension Trackingcode ) sehen, die zum Umsatz beigetragen haben. </p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Kampagnen anpassen, die nicht den erwarteten Umsatzzielen entsprechen.</p><p>Diese Vorlage verwendet die Umsatzmetrik. |
| **Bestellungen** | <!--duplicated in Most popular section-->Anzeigen der Gesamtzahl der Kaufereignisse auf Ihrer Site. <p>**Dies kann Ihnen** dabei helfen, besser zu verstehen, welche Dimensionselemente zu einer Bestellung beigetragen haben, indem die Metrik &quot;Bestellungen&quot;mit einer beliebigen Dimension kombiniert wird. Sie könnten beispielsweise die Top-Kampagnen (unter Verwendung der Dimension Trackingcode ) sehen, die zu Käufen beigetragen haben.</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Kampagnen anpassen, die nicht den erwarteten Einkaufszielen entsprechen. </p><p>Diese Vorlage verwendet die Metrik Bestellungen . |
| [!UICONTROL **Einheiten**] | Zeigen Sie die Gesamtzahl der bei allen Bestellungen gekauften Artikel an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen** helfen, besser zu verstehen, wie die Stückverkäufe im Laufe der Zeit zunehmen oder abnehmen. Sie können ein Segment anwenden, um zu erfahren, welche Kunden oder Regionen die meisten Einheiten kaufen und wie diese Verkaufseinheiten im Laufe der Zeit im Trend sind.</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Maßnahmen durchführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne durch Vergleich der Einzelverkäufe vor und nach dem Start der Kampagne. Oder Sie vergleichen den Jahresvergleich der Einzelverkäufe während der Feiertage.</p><p>Diese Vorlage verwendet die Dimension &quot;[Tag&quot;](/help/components/dimensions/day.md) und die Metrik &quot;[Einheiten&quot;](/help/components/metrics/units.md).</p> |
| [!UICONTROL **Magento: Marketing und Commerce**] | Zeigen Sie vorgefertigte Einblicke für Einzelhändler in Ihre Commerce-Aktivitäten an, um den Umsatz zu verbessern. Dies richtet sich an Nutzer von Magento, kann aber von jedem Online-Händler genutzt werden. <p>**Dies kann Ihnen** helfen, besser zu verstehen, wie Ihre Commerce-Aktivitäten zu den Verkaufszahlen beitragen.</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Budgets an Aktivitäten anpassen, die den meisten ROI erzielen.</p> |

### Zielgruppe {#web-audience}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--countryGeoReport"
>title="Zeigen Sie das Land an, aus dem die Personen stammen, die Ihre Site besuchen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, aus welchen Ländern die meisten Personen stammen, die Ihre Site besuchen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Daten nutzen, um sich auf Marketing-Maßnahmen in diesen Ländern zu konzentrieren, oder sicherstellen, dass Ihr Site-Erlebnis in Ländern mit unterschiedlichen Hauptsprachen optimal ist.<br/>Diese Vorlage verwendet die Dimension „Länder“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--stateGeoReport"
>title="Zeigen Sie den Bundesstaat (in den USA) an, aus dem die Personen stammen, die Ihre Site besuchen. Diese Vorlage ähnelt der Vorlage für geografische Regionen, allerdings ist sie spezifisch für die USA. "
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, aus welchen US-Bundesstaaten die meisten Personen stammen, die Ihre Site besuchen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Daten verwenden, um sich auf Marketing-Maßnahmen in diesen Bundesstaaten zu konzentrieren.<br/>Diese Vorlage verwendet die Dimension „USA“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--regionGeoReport"
>title="Zeigen Sie die geografische Region an, aus der die Personen stammen, die Ihre Site besuchen. Eine Region ist ein geografischer Bereich, der kleiner als ein Land, jedoch größer als eine Stadt ist. In einigen Ländern ist eine Region ein Bundesland, eine Provinz oder eine Präfektur. In anderen Gebieten handelt es sich um einen Landesteil, ein Departement oder eine großstädtische Region. "
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, aus welchen Regionen die meisten Personen stammen, die Ihre Site besuchen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Daten nutzen, um sich auf Marketing-Maßnahmen in diesen Regionen zu konzentrieren, oder sicherstellen, dass Ihr Site-Erlebnis in Regionen mit unterschiedlichen Hauptsprachen optimal ist. <br/>Diese Vorlage verwendet die Dimensionen „ID(variables/geocountry)“ und „Regionen“. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--cityGeoReport"
>title="Zeigen Sie die Stadt an, aus der die Personen stammen, die Ihre Site besuchen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, aus welchen Städten die meisten Personen stammen, die Ihre Site besuchen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Daten verwenden, um sich auf Marketing-Maßnahmen in diesen Städten zu konzentrieren. <br/>Diese Vorlage verwendet die Dimension „Städte“"

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--dmaGeoReport"
>title="Zeigen Sie die designierten Marketing-Gebiete (DMAs) in den USA an, aus denen die Personen stammen, die Ihre Site besuchen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, aus welchen Regionen die meisten Personen stammen, die Ihre Site besuchen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Daten verwenden, um sich auf Marketing-Maßnahmen in der erfolgreichsten Regionen zu konzentrieren. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--languageRankedReport"
>title="Zeigen Sie die häufigsten Sprachen an, in denen die Besuchenden den Inhalt anzeigen."
>abstract="**Dies kann Ihnen dabei helfen**, die am häufigsten bevorzugten Sprachen der Besuchenden besser zu verstehen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Lokalisierungs- oder Marketing-Maßnahmen auf die beliebtesten Sprachen konzentrieren.<br/>Diese Vorlage verwendet die Dimension „Sprache“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--timeZoneRankedReport"
>title="Zeigen Sie die wichtigsten Zeitzonen der Besucher an, die auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, in welchen Zeitzonen Ihre Besucher leben.<br/>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. die Site-Wartung zu Zeiten anpassen, die sich auf die geringste Anzahl von Personen auswirken."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--domainRankedReport"
>title="Zeigen Sie die Top-Domänen der Besucher an, die auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, von welchen Organisationen Ihre Besucher kommen.<br/>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Ihren Inhalt auf Ihre größten Kunden ausrichten."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--topLevelDomainRankedReport"
>title="Zeigen Sie die Top-Domänen der Besucher an, die auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, von welchen Organisationen Ihre Besucher kommen.<br/>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Ihren Inhalt auf Ihre größten Kunden ausrichten."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--web-technology-template"
>title="Technologieübersicht"
>abstract=""

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--browserRankedReport"
>title="Zeigen Sie den Namen und die Version der wichtigsten Browser an, die für den Zugriff auf Ihre Site verwendet werden."
>abstract="**Dies kann Ihnen dabei helfen**, die gängigsten Browser, die beim Besuch verwendet werden, besser zu verstehen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität durch Testen neuer Versionen Ihrer Site mit den wichtigsten Browsern verbessern. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.<br/>Diese Vorlage verwendet die Dimension „Browser“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--browserTypeRankedReport"
>title="Zeigen Sie die Namen der Organisationen an, die die wichtigsten Browser erstellt haben, mit denen Personen auf Ihre Site zugreifen. Diese Vorlage unterscheidet sich insofern von der Vorlage „Browser“, als sie verschiedene Versionen desselben Browsers nicht als separate Dimensionselemente auflistet."
>abstract="**Dies kann Ihnen dabei helfen**, die gängigsten Browser, die Besuchende verwenden, besser zu verstehen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität verbessern, indem Sie neue Versionen Ihrer Site mit den wichtigsten Browsern testen. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden. <br/>Diese Vorlage verwendet die Dimension „Browsertyp“. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--browserWidthRankedReport"
>title="Zeigen Sie die wichtigsten Browser-Breiten an, mit denen Benutzer auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, wie Inhalte Besuchern angezeigt werden.<br/>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Maßnahmen ergreifen, z. B. die Verbesserung der Site-Qualität durch Testen neuer Versionen Ihrer Site mit den am häufigsten verwendeten Browserbreiten. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.<br/>Diese Vorlage verwendet die Dimension „Browser“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--browserHeightRankedReport"
>title="Zeigen Sie die obersten Browserhöhen an, mit denen Benutzer auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, wie Inhalte Besuchern angezeigt werden.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. die Site-Qualität verbessern, indem Sie neue Versionen Ihrer Site mit den gängigsten Browserhöhen testen. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.<br/>Diese Vorlage verwendet die Dimension „Browser“. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--operatingSystemRankedReport"
>title="Zeigen Sie den Namen der Betriebssysteme und die Version an, die Benutzer für den Zugriff auf Ihre Site verwenden."
>abstract="**Dies kann Ihnen** helfen, die gängigsten Betriebssysteme und Versionen, die Besucher verwenden, besser zu verstehen.<br/>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Maßnahmen ergreifen, z. B. die Verbesserung der Site-Qualität durch Testen neuer Versionen Ihrer Site mit den besten Betriebssystemen und Versionen. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--operatingSystemTypeRankedReport"
>title="Zeigen Sie den Namen der Betriebssysteme an, mit denen Benutzer auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen** helfen, die häufigsten Betriebssysteme, die Besucher verwenden, besser zu verstehen.<br/>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Maßnahmen ergreifen, z. B. die Verbesserung der Site-Qualität durch Testen neuer Versionen Ihrer Site mit den besten Betriebssystemen. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobileCarrierRankedReport"
>title="Zeigen Sie das Telekommunikationsunternehmen an, das Mobilfunkverbindungen mit den Mobilgeräten bereitstellt, mit denen Benutzende auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Mobilnetzbetreiber bei Ihrer Benutzerbasis am beliebtesten sind.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Inhaltsbereitstellung auf Grundlage der Netzwerkfunktionen verschiedener Betreiber anpassen, um ein reibungsloses Anwendererlebnis zu gewährleisten.<br/>Diese Vorlage verwendet die Dimension „Mobilnetzbetreiber“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--returnFrequencyRankedReport"
>title="Zeigen Sie das Telekommunikationsunternehmen an, das Mobilfunkverbindungen mit den Mobilgeräten bereitstellt, mit denen Benutzende auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Mobilnetzbetreiber bei Ihrer Benutzerbasis am beliebtesten sind.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Inhaltsbereitstellung auf Grundlage der Netzwerkfunktionen verschiedener Betreiber anpassen, um ein reibungsloses Anwendererlebnis zu gewährleisten.<br/>Diese Vorlage verwendet die Dimension „Mobilnetzbetreiber“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--returnVisitorsOvertimeReport"
>title="Zeigen Sie das Telekommunikationsunternehmen an, das Mobilfunkverbindungen mit den Mobilgeräten bereitstellt, mit denen Benutzende auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Mobilnetzbetreiber bei Ihrer Benutzerbasis am beliebtesten sind.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Inhaltsbereitstellung auf Grundlage der Netzwerkfunktionen verschiedener Betreiber anpassen, um ein reibungsloses Anwendererlebnis zu gewährleisten.<br/>Diese Vorlage verwendet die Dimension „Mobilnetzbetreiber“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--visitNumberRankedReport"
>title="Sehen Sie sich an, wie oft ein Besucher die Site besucht hat."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, wie engagiert Besucher sind, wenn sie zu Ihrer Site zurückkehren. Dies gilt für die Lebensdauer des Besuchers, unabhängig vom Datumsbereich des Projekts.<br/>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. die Marketing-Bemühungen für häufige Besucher anpassen.<br/>Diese Vorlage verwendet die Dimension Besuchsnummer ."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--customerLoyaltyRankedReport"
>title="Zeigen Sie die Anzahl der Besucher auf Ihrer Site an, die 0 frühere Käufe, 1 vorherigen Kauf, 2 vorherige Käufe oder mehr als 3 frühere Käufe getätigt haben."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, wie Ihre Site das Kaufverhalten beeinflusst. .<br/>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Maßnahmen durchführen, z. B. den Fokus auf Besucher, die zum Kauf zurückkehren, sodass Sie ein ähnliches Verhalten für neue Besucher fördern können.<br/>Diese Vorlage verwendet die Dimension Kundentreue ."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--daysBeforeFirstPurchaseRankedReport"
>title="Zeigen Sie die Anzahl der Tage an, die zwischen dem ersten Sitebesuch eines Besuchers und dem ersten Kauf verstrichen sind. Wenn ein Besucher beispielsweise einen Tag nach dem ersten Besuch einen Kauf tätigt, gehört jeder nachfolgende Besuch oder jedes nachfolgende Ereignis zum Dimensionselement 1 Tag ."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, wie lange es dauert, bis Besucher einen Kauf tätigen.<br/>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Ihre Site aktualisieren, um eine schnellere Akquise zu fördern.<br/>Diese Vorlage verwendet die Dimension Tage bis Erstkauf ."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--daysSinceLastPurchaseRankedReport"
>title="Zeigen Sie die Zeit an, die zwischen dem aktuellen Treffer des Besuchers und seinem letzten Kauf zu diesem Zeitpunkt verstrichen ist."
>abstract="**Dies kann Ihnen** dabei helfen, das Besucherverhalten nach dem Kauf von etwas auf Ihrer Site besser zu verstehen.<br/>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Ihre Site aktualisieren, um Folgekäufe zu fördern.<br/>Diese Vorlage verwendet die Dimension Tage seit letztem Kauf ."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobileDeviceNameRankedReport"
>title="Zeigen Sie die Marke und das Modell von Mobilgeräten an, mit denen Benutzende auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Mobilgeräte bei Ihrer Benutzerbasis am beliebtesten sind.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. das Rendering Ihrer Site für die gängigsten Mobilgeräte optimieren.<br/>Diese Vorlage verwendet die Dimension „Mobilgerätename“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobileDeviceTypeRankedReport"
>title="Zeigen Sie die Mobilgerätetypen an, mit denen Benutzende auf Ihre Site zugreifen, z. B. Smartphones und Tablets."
>abstract="**Dies kann Ihnen dabei helfen**, die verschiedenen Arten von Mobilgeräten besser zu verstehen, die für den Zugriff auf Ihre Site verwendet werden.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Site für die Mobilgerätetypen optimieren, die am häufigsten verwendet werden.<br/>Diese Vorlage verwendet die Dimension „Mobilgerätetyp“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobileManufacturerRankedReport"
>title="Zeigen Sie an, welche Hersteller die Mobilgeräte herstellen, mit denen Benutzende auf Ihre Site zugreifen, z. B. Apple und Samsung."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Hersteller bei Ihrer Benutzerbasis am beliebtesten sind.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Inhaltsbereitstellung auf Grundlage der Fähigkeiten verschiedener Hersteller anpassen, um ein reibungsloses Anwendererlebnis zu gewährleisten.<br/>Diese Vorlage verwendet die Dimension „Mobilgerätehersteller“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobileScreenSizeRankedReport"
>title="Zeigen Sie die wichtigsten Bildschirmgrößen für Mobilgeräte an, mit denen Benutzer auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, wie Inhalte Besuchern angezeigt werden.<br/>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Maßnahmen ergreifen, z. B. die Verbesserung der Site-Qualität durch Testen neuer Versionen Ihrer Site mit den am häufigsten verwendeten Bildschirmgrößen für Mobilgeräte. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobileScreenHeightRankedReport"
>title="Zeigen Sie die wichtigsten Mobilgerät-Bildschirmhöhen an, mit denen Benutzer auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, wie Inhalte Besuchern angezeigt werden.<br/>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Maßnahmen ergreifen, z. B. die Verbesserung der Site-Qualität durch Tests neuer Versionen Ihrer Site mit den am häufigsten verwendeten Mobilgerät-Bildschirmhöhen. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobileScreenWidthRankedReport"
>title="Zeigen Sie die oberen Mobilgerät-Bildschirmbreiten an, mit denen Benutzer auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, wie Inhalte Besuchern angezeigt werden.<br/>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Maßnahmen ergreifen, z. B. die Verbesserung der Site-Qualität durch Testen neuer Versionen Ihrer Site mit den am häufigsten verwendeten Mobilgerät-Bildschirmbreiten. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobile-lifecycle-metrics-app-usage-template"
>title="Zeigen Sie die Anzahl der Benutzer, Starts und ersten Starts in Ihrer App sowie die durchschnittliche Sitzungslänge an."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, wie viel Ihre App verwendet wird. <br/>**Je nachdem, was Sie lernen, können Sie** beliebig viele Dinge tun, z. B. die App-Leistung verbessern, damit sie auf die Nutzungsmenge skaliert werden kann."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobile-app-journeys"
>title="Zeigen Sie die markanten Nutzungsmuster für Ihre App an."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, wie Benutzer Ihre App verwenden. <br/>**Basierend auf dem, was Sie lernen, können Sie** beliebig viele Dinge tun, z. B. die Verbesserung, wie Benutzer von einem Bildschirm zum anderen gelangen können, um die häufigsten Workflows auszuwählen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobile-app-key-metrics"
>title="Zeigen Sie einige der häufigsten Mobile-App-Metriken an."
>abstract="**Dies kann Ihnen** dabei helfen, die grundlegende Leistung Ihrer App besser zu verstehen.<br/>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. die allgemeine Gesundheit und Leistung Ihrer App bewerten."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobile-app-messaging"
>title="Zeigen Sie Leistungsdaten für In-App-Nachrichten und Push-Nachrichten für Ihre App an."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, wie Benutzer In-App-Messaging-Funktionen verwenden und wie effektiv Push-Benachrichtigungen Traffic zu Ihrer App leiten.<br/>**Je nach Ihren Erkenntnissen können Sie** beliebig viele Dinge tun, z. B. die Verbesserung des Erlebnisses von In-App-Nachrichten-Push-Benachrichtigungen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobile-app-performance-template"
>title="Sehen Sie sich die Leistung Ihrer App an und erfahren Sie, wo Probleme bei Benutzern auftreten."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, ob Benutzer Ihrer App auf Langsamkeit oder eine beeinträchtigte Leistung stoßen. <br/>**Je nachdem, was Sie erfahren, können Sie** eine beliebige Anzahl von Maßnahmen ergreifen, z. B. vorhandene Probleme beheben oder die App-Leistung verbessern, bevor Probleme auftreten."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobile-app-retention"
>title="Zeigen Sie an, welche Benutzer die treuesten Benutzer Ihrer App sind und was sie in der App tun."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, wie Ihre treusten Benutzer Ihre App verwenden.<br/>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Maßnahmen durchführen, z. B. Ihre Marketing-Bemühungen für die Funktionen verbessern, die Ihre treusten Benutzer verwenden."

<!-- markdownlint-enable MD034 -->


Die folgenden Vorlagen sind verfügbar:

| Vorlagenname | Warum diese Vorlage <!-- What do you do with it? What can it help you learn? and What are the potential actions? --> verwenden |
| --- | --- | 
| [!UICONTROL **Metrik für Personen**] | Anzeigen der Anzahl der Personen, die mit Ihrer Marke interagieren <p>**Dies kann Ihnen** dabei helfen, Nutzungstrends auf Ihrer Site besser zu verstehen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine beliebige Anzahl von Maßnahmen durchführen, z. B. die Effektivität der jüngsten Marketing-Bemühungen bei der Generierung neuer Besucher Ihrer Site.</p> |
| **Besucherprofil** > **Standortübersicht** | Zeigen Sie eine Übersicht über die Besucherposition in einer Zuordnungsvisualisierung an.<p>**Dies kann Ihnen** helfen, besser zu verstehen, wo sich Besucher befinden, die Ihre Site besuchen. </p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Marketing-Ressourcen an den Orten konzentrieren, an denen Sie das größte Interesse und die beste Gelegenheit sehen.</p><!-- This template uses the --> |
| **Besucherprofil** > **Geoländer** | Zeigen Sie das Land an, aus dem die Personen stammen, die Ihre Site besuchen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, aus welchen Ländern die meisten Personen stammen, die Ihre Site besuchen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Daten nutzen, um sich auf Marketing-Maßnahmen in diesen Ländern zu konzentrieren, oder sicherstellen, dass Ihr Site-Erlebnis in Ländern mit unterschiedlichen Hauptsprachen optimal ist.</p><p>Diese Vorlage verwendet die Dimension Länder . </p> |
| **Besucherprofil** > **US-Bundesstaaten** | Zeigen Sie den Bundesstaat (in den USA) an, aus dem die Personen stammen, die Ihre Site besuchen. Diese Vorlage ähnelt der Vorlage für geografische Regionen, allerdings ist sie spezifisch für die USA. <p>**Dies kann Ihnen helfen**, besser zu verstehen, aus welchen US-Bundesstaaten die meisten Personen stammen, die Ihre Site besuchen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Daten verwenden, um sich auf Marketing-Maßnahmen in diesen Bundesstaaten zu konzentrieren.</p><p>Diese Vorlage verwendet die Dimension US-Bundesstaaten . </p> |
| **Besucherprofil** > **Geo-Regionen** | Zeigen Sie die geografische Region an, aus der die Personen stammen, die Ihre Site besuchen. Eine Region ist ein geografischer Bereich, der kleiner als ein Land, jedoch größer als eine Stadt ist. In einigen Ländern ist eine Region ein Bundesland, eine Provinz oder eine Präfektur. In anderen Gebieten handelt es sich um einen Landesteil, ein Departement oder eine großstädtische Region. <p>**Dies kann Ihnen helfen**, besser zu verstehen, aus welchen Regionen die meisten Personen stammen, die Ihre Site besuchen.</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. die Daten verwenden, um sich auf Marketing-Maßnahmen in diesen Regionen zu konzentrieren, oder sicherstellen, dass Ihr Site-Erlebnis in Regionen mit unterschiedlichen Hauptsprachen optimal ist. </p><p>Diese Vorlage verwendet die Dimensionen ID (Variablen/Land) und Regionen . </p> |
| **Besucherprofil** > **geografische Städte** | Zeigen Sie die Stadt an, aus der die Personen stammen, die Ihre Site besuchen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, aus welchen Städten die meisten Personen stammen, die Ihre Site besuchen.</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. die Daten verwenden, um sich auf Marketing-Maßnahmen in diesen Städten zu konzentrieren. </p><p>Diese Vorlage verwendet die Dimension Städte . </p> |
| **Besucherprofil** > **Geo US DMA** | Zeigen Sie die designierten Marketing-Gebiete (DMAs) in den USA an, aus denen die Personen stammen, die Ihre Site besuchen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, aus welchen Regionen die meisten Personen stammen, die Ihre Site besuchen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Daten verwenden, um sich auf Marketing-Maßnahmen in der erfolgreichsten Regionen zu konzentrieren. </p><!-- This template uses the --> |
| **Besucherprofil** > **Sprachen** | Zeigen Sie die häufigsten Sprachen an, in denen die Besuchenden den Inhalt anzeigen. <p>**Dies kann Ihnen dabei helfen**, die am häufigsten bevorzugten Sprachen der Besuchenden besser zu verstehen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Lokalisierungs- oder Marketing-Maßnahmen auf die beliebtesten Sprachen konzentrieren.</p><p>Diese Vorlage verwendet die Dimension Sprache .</p> |
| **Besucherprofil** > **Zeitzonen** | Zeigen Sie die wichtigsten Zeitzonen der Besucher an, die auf Ihre Site zugreifen. <p>**Dies kann Ihnen** helfen, besser zu verstehen, in welchen Zeitzonen Ihre Besucher leben.</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. die Site-Wartung zu Zeiten anpassen, die sich auf die geringste Anzahl von Personen auswirken.</p> |
| **Besucherprofil** > **Domänen** | Zeigen Sie die Top-Domänen der Besucher an, die auf Ihre Site zugreifen. <p>**Dies kann Ihnen** helfen, besser zu verstehen, von welchen Organisationen Ihre Besucher kommen.</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Ihren Inhalt auf Ihre größten Kunden ausrichten.</p> |
| **Besucherprofil** > **Domänen auf oberster Ebene** | Zeigen Sie die Domänen der Besucher auf oberster Ebene an, die auf Ihre Site zugreifen. <p>**Dies kann Ihnen** helfen, besser zu verstehen, von welchen Organisationen Ihre Besucher kommen.</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Ihren Inhalt auf Ihre größten Kunden ausrichten.</p> |
| **Besucherprofil** > **Technologie** > **Technologieübersicht** | <p>**Dies hilft Ihnen**, besser zu verstehen</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. </p><p>Diese Vorlage verwendet die </p> |
| **Besucherprofil** > **Technologie** > **Browser** | Zeigen Sie den Namen und die Version der wichtigsten Browser an, die für den Zugriff auf Ihre Site verwendet werden.<p>**Dies kann Ihnen dabei helfen**, die gängigsten Browser, die beim Besuch verwendet werden, besser zu verstehen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität durch Testen neuer Versionen Ihrer Site mit den wichtigsten Browsern verbessern. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.</p><p>Diese Vorlage verwendet die Dimension Browser . </p> |
| **Besucherprofil** > **Technologie** > **Browsertypen** | Zeigen Sie die Namen der Organisationen an, die die wichtigsten Browser erstellt haben, mit denen Personen auf Ihre Site zugreifen. Diese Vorlage unterscheidet sich insofern von der Vorlage „Browser“, als sie verschiedene Versionen desselben Browsers nicht als separate Dimensionselemente auflistet.<p>**Dies kann Ihnen** helfen, die gängigsten Browser, die Besucher verwenden, besser zu verstehen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität durch Testen neuer Versionen Ihrer Site mit den wichtigsten Browsern verbessern. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden. </p><p>Diese Vorlage verwendet die Dimension Browsertyp . </p> |
| **Besucherprofil** > **Technologie** > **Browserbreite** | Zeigen Sie die wichtigsten Browser-Breiten an, mit denen Benutzer auf Ihre Site zugreifen.<p>**Dies kann Ihnen** helfen, besser zu verstehen, wie Inhalte Besuchern angezeigt werden.</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Maßnahmen ergreifen, z. B. die Verbesserung der Site-Qualität durch Testen neuer Versionen Ihrer Site mit den am häufigsten verwendeten Browserbreiten. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.</p><p>Diese Vorlage verwendet die Dimension Browser . </p> |
| **Besucherprofil** > **Technologie** > **Browserhöhe** | Zeigen Sie die obersten Browserhöhen an, mit denen Benutzer auf Ihre Site zugreifen.<p>**Dies kann Ihnen** helfen, besser zu verstehen, wie Inhalte Besuchern angezeigt werden.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. die Site-Qualität verbessern, indem Sie neue Versionen Ihrer Site mit den gängigsten Browserhöhen testen. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.</p><p>Diese Vorlage verwendet die Dimension Browser . </p> |
| **Besucherprofil** > **Technologie** > **Betriebssystem** | Zeigen Sie den Namen der Betriebssysteme und die Version an, die Benutzer für den Zugriff auf Ihre Site verwenden.<p>**Dies kann Ihnen** helfen, die gängigsten Betriebssysteme und Versionen, die Besucher verwenden, besser zu verstehen.</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Maßnahmen ergreifen, z. B. die Verbesserung der Site-Qualität durch Testen neuer Versionen Ihrer Site mit den besten Betriebssystemen und Versionen. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.</p> |
| **Besucherprofil** > **Technologie** > **Betriebssystemtypen** | Zeigen Sie den Namen der Betriebssysteme an, mit denen Benutzer auf Ihre Site zugreifen.<p>**Dies kann Ihnen** helfen, die häufigsten Betriebssysteme, die Besucher verwenden, besser zu verstehen.</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Maßnahmen ergreifen, z. B. die Verbesserung der Site-Qualität durch Testen neuer Versionen Ihrer Site mit den besten Betriebssystemen. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.</p> |
| **Besucherprofil** > **Technologie** > [!UICONTROL **Mobilnetzbetreiber**] | Zeigen Sie das Telekommunikationsunternehmen an, das Mobilfunkverbindungen mit den Mobilgeräten bereitstellt, mit denen Benutzende auf Ihre Site zugreifen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Mobilnetzbetreiber bei Ihrer Benutzerbasis am beliebtesten sind.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Inhaltsbereitstellung auf Grundlage der Netzwerkfunktionen verschiedener Betreiber anpassen, um ein reibungsloses Anwendererlebnis zu gewährleisten.</p><p>Diese Vorlage verwendet die Dimension Mobilnetzbetreiber .</p> |
| **Besuchertreue** > **Rückkehrhäufigkeit** | Zeigen Sie das Telekommunikationsunternehmen an, das Mobilfunkverbindungen mit den Mobilgeräten bereitstellt, mit denen Benutzende auf Ihre Site zugreifen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Mobilnetzbetreiber bei Ihrer Benutzerbasis am beliebtesten sind.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Inhaltsbereitstellung auf Grundlage der Netzwerkfunktionen verschiedener Betreiber anpassen, um ein reibungsloses Anwendererlebnis zu gewährleisten.</p><p>Diese Vorlage verwendet die Dimension Mobilnetzbetreiber .</p> |
| **Besuchertreue** > **Erneute Besuche** | Zeigen Sie das Telekommunikationsunternehmen an, das Mobilfunkverbindungen mit den Mobilgeräten bereitstellt, mit denen Benutzende auf Ihre Site zugreifen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Mobilnetzbetreiber bei Ihrer Benutzerbasis am beliebtesten sind.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Inhaltsbereitstellung auf Grundlage der Netzwerkfunktionen verschiedener Betreiber anpassen, um ein reibungsloses Anwendererlebnis zu gewährleisten.</p><p>Diese Vorlage verwendet die Dimension Mobilnetzbetreiber .</p> |
| **Besuchertreue** > **Besuchsnummer** | Sehen Sie sich an, wie oft ein Besucher die Site besucht hat.<p>**Dies kann Ihnen** helfen, besser zu verstehen, wie engagiert Besucher sind, wenn sie zu Ihrer Site zurückkehren. Dies gilt für die Lebensdauer des Besuchers, unabhängig vom Datumsbereich des Projekts.</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. die Marketing-Bemühungen für häufige Besucher anpassen.</p><p>Diese Vorlage verwendet die Dimension Besuchsnummer .</p> |
| **Besuchertreue** > **Verkaufszyklus** > **Kundentreue** | Zeigen Sie die Anzahl der Besucher auf Ihrer Site an, die 0 frühere Käufe, 1 vorherigen Kauf, 2 vorherige Käufe oder mehr als 3 frühere Käufe getätigt haben. <p>**Dies kann Ihnen** helfen, besser zu verstehen, wie Ihre Site das Kaufverhalten beeinflusst. .</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Maßnahmen durchführen, z. B. den Fokus auf Besucher, die zum Kauf zurückkehren, sodass Sie ein ähnliches Verhalten für neue Besucher fördern können.</p><p>Diese Vorlage verwendet die Dimension Kundentreue .</p> |
| **Besuchertreue** > **Verkaufszyklus** > **Tage bis Erstkauf** | Zeigen Sie die Anzahl der Tage an, die zwischen dem ersten Sitebesuch eines Besuchers und dem ersten Kauf verstrichen sind. Wenn ein Besucher beispielsweise einen Tag nach dem ersten Besuch einen Kauf tätigt, gehören alle nachfolgenden Besuche und Ereignisse zum Dimensionselement „1 Tag“.<p>**Dies kann Ihnen** helfen, besser zu verstehen, wie lange es dauert, bis Besucher einen Kauf tätigen.</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Ihre Site aktualisieren, um eine schnellere Akquise zu fördern.</p><p>Diese Vorlage verwendet die Dimension Tage bis Erstkauf .</p> |
| **Besuchertreue** > **Verkaufszyklus** > **Tage seit letztem Kauf** | Zeigen Sie die Zeit an, die zwischen dem aktuellen Treffer des Besuchers und seinem letzten Kauf zu diesem Zeitpunkt verstrichen ist.<p>**Dies kann Ihnen** dabei helfen, das Besucherverhalten nach dem Kauf von etwas auf Ihrer Site besser zu verstehen.</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Ihre Site aktualisieren, um Folgekäufe zu fördern.</p><p>Diese Vorlage verwendet die Dimension Tage seit letztem Kauf .</p> |
| **Mobil** > **Mobilgeräte** | Zeigen Sie die Marke und das Modell von Mobilgeräten an, mit denen Benutzende auf Ihre Site zugreifen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Mobilgeräte bei Ihrer Benutzerbasis am beliebtesten sind.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. das Rendering Ihrer Site für die gängigsten Mobilgeräte optimieren.</p><p>Diese Vorlage verwendet die Dimension Mobilgerätename .</p> |
| **Mobil** > **Mobilgerätetyp** | Zeigen Sie die Mobilgerätetypen an, mit denen Benutzende auf Ihre Site zugreifen, z. B. Smartphones und Tablets.<p>**Dies kann Ihnen dabei helfen**, die verschiedenen Arten von Mobilgeräten besser zu verstehen, die für den Zugriff auf Ihre Site verwendet werden.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Site für die Mobilgerätetypen optimieren, die am häufigsten verwendet werden.</p><p>Diese Vorlage verwendet die Dimension Mobilgerätetyp .</p> |
| **Mobil** > **Hersteller** | Zeigen Sie an, welche Hersteller die Mobilgeräte herstellen, mit denen Benutzende auf Ihre Site zugreifen, z. B. Apple und Samsung.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Hersteller bei Ihrer Benutzerbasis am beliebtesten sind.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Inhaltsbereitstellung auf Grundlage der Fähigkeiten verschiedener Hersteller anpassen, um ein reibungsloses Anwendererlebnis zu gewährleisten.</p><p>Diese Vorlage verwendet die Dimension Mobilgerätehersteller .</p> |
| **Mobil** > **Bildschirmgröße** | Zeigen Sie die wichtigsten Bildschirmgrößen für Mobilgeräte an, mit denen Benutzer auf Ihre Site zugreifen.<p>**Dies kann Ihnen** helfen, besser zu verstehen, wie Inhalte Besuchern angezeigt werden.</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Maßnahmen ergreifen, z. B. die Verbesserung der Site-Qualität durch Testen neuer Versionen Ihrer Site mit den am häufigsten verwendeten Bildschirmgrößen für Mobilgeräte. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.</p> |
| **Mobil** > **Bildschirmhöhe** | Zeigen Sie die wichtigsten Mobilgerät-Bildschirmhöhen an, mit denen Benutzer auf Ihre Site zugreifen.<p>**Dies kann Ihnen** helfen, besser zu verstehen, wie Inhalte Besuchern angezeigt werden.</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Maßnahmen ergreifen, z. B. die Verbesserung der Site-Qualität durch Tests neuer Versionen Ihrer Site mit den am häufigsten verwendeten Mobilgerät-Bildschirmhöhen. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.</p> |
| **Mobil** > **Bildschirmbreite** | Zeigen Sie die oberen Mobilgerät-Bildschirmbreiten an, mit denen Benutzer auf Ihre Site zugreifen.<p>**Dies kann Ihnen** helfen, besser zu verstehen, wie Inhalte Besuchern angezeigt werden.</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Maßnahmen ergreifen, z. B. die Verbesserung der Site-Qualität durch Testen neuer Versionen Ihrer Site mit den am häufigsten verwendeten Mobilgerät-Bildschirmbreiten. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.</p> |
| **Mobil** > **Nutzung mobiler Apps** | Zeigen Sie die Anzahl der Benutzer, Starts und ersten Starts in Ihrer App sowie die durchschnittliche Sitzungslänge an.<p>**Dies kann Ihnen** helfen, besser zu verstehen, wie viel Ihre App verwendet wird. </p><p>**Je nachdem, was Sie lernen, können Sie** beliebig viele Dinge tun, z. B. die App-Leistung verbessern, damit sie auf die Nutzungsmenge skaliert werden kann.</p><!-- This template uses the --> |
| **Mobil** > **Journey für mobile Apps** | Zeigen Sie die markanten Nutzungsmuster für Ihre App an. <p>**Dies kann Ihnen** helfen, besser zu verstehen, wie Benutzer Ihre App verwenden. </p><p>**Basierend auf dem, was Sie lernen, können Sie** beliebig viele Dinge tun, z. B. die Verbesserung, wie Benutzer von einem Bildschirm zum anderen gelangen können, um die häufigsten Workflows auszuwählen. </p><!-- This template uses the --> |
| **Mobile** > **Mobile App-Metriken** | Zeigen Sie einige der häufigsten Mobile-App-Metriken an. <p>**Dies kann Ihnen** dabei helfen, die grundlegende Leistung Ihrer App besser zu verstehen.</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. die allgemeine Gesundheit und Leistung Ihrer App bewerten.</p><!-- This template uses the --> |
| **Mobile** > **Mobile App Messaging** | Zeigen Sie Leistungsdaten für In-App-Nachrichten und Push-Nachrichten für Ihre App an.<p>**Dies kann Ihnen** helfen, besser zu verstehen, wie Benutzer In-App-Messaging-Funktionen verwenden und wie effektiv Push-Benachrichtigungen Traffic zu Ihrer App leiten.</p><p>**Je nach Ihren Erkenntnissen können Sie** beliebig viele Dinge tun, z. B. die Verbesserung des Erlebnisses von In-App-Nachrichten-Push-Benachrichtigungen.</p><!-- This template uses the --> |
| **Mobile** > **Leistung der mobilen App** | Sehen Sie sich die Leistung Ihrer App an und erfahren Sie, wo Probleme bei Benutzern auftreten. <p>**Dies kann Ihnen** helfen, besser zu verstehen, ob Benutzer Ihrer App auf Langsamkeit oder eine beeinträchtigte Leistung stoßen. </p><p>**Je nachdem, was Sie erfahren, können Sie** eine beliebige Anzahl von Maßnahmen ergreifen, z. B. vorhandene Probleme beheben oder die App-Leistung verbessern, bevor Probleme auftreten.</p><!-- This template uses the --> |
| **Mobil** > **Beibehaltung mobiler Apps** | Zeigen Sie an, welche Benutzer die treuesten Benutzer Ihrer App sind und was sie in der App tun. <p>**Dies kann Ihnen** helfen, besser zu verstehen, wie Ihre treusten Benutzer Ihre App verwenden.</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Maßnahmen durchführen, z. B. Ihre Marketing-Bemühungen für die Funktionen verbessern, die Ihre treusten Benutzer verwenden.</p><!-- This template uses the --> |

### Akquise {#web-acquisition}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--marketing-channel-overview-template"
>title="Bei Verwendung der benutzerdefinierten Attribution zeigt diese Vorlage, wie Besuchende auf Ihre Site gelangen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Ihrer Marketing-Kanäle am effektivsten sind.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. intensiver in effektive Marketing-Kanäle investieren und weniger effektive Marketing-Kanäle aufgeben.<br/>Diese Vorlage verwendet die Dimension „ID(variables/marketingchannel)“ und die Metrik „Umsatz“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--firstouchChannelRankedReport"
>title="Zeigen Sie die ersten Marketing-Kanäle an, zu denen Besuchende während ihres Interaktionszeitraums (standardmäßig 30 Tage) passen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Marketing-Kanäle den anfänglichen Traffic zu Ihrer Site leiten.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf Bereiche konzentrieren, die am effektivsten sind.<br/>Diese Vorlage verwendet die Dimension „Erstkontaktkanal“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--firstouchChannelDetailRankedReport"
>title="Zeigen Sie Details zu den ersten Marketing-Kanälen an, zu denen Besuchende während ihres Interaktionszeitraums (standardmäßig 30 Tage) passen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, was dazu beigetragen hat, dass der Treffer zu einem Marketing-Kanal passte. Wenn beispielsweise ein Besucher zu Ihrer Site gelangt ist und mit dem Marketing-Kanal „Paid Search“ übereinstimmt, können Sie anhand des Kanaldetails sehen, welche Suchmaschine verwendet wurde oder nach welchem Schlüsselwort er gesucht hat.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf Bereiche konzentrieren, die am effektivsten sind.<br/>Diese Vorlage verwendet die Dimension „Detail des Erstkontaktkanals“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--campaignConversionReport"
>title="Kampagnenkonversionstrichter"
>abstract=""

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--retail-campaign-performance-template"
>title="Zeigen Sie Details zur Leistung Ihrer Marketing-Kampagnen an."
>abstract="**Dies kann Ihnen helfen**, mehr über die verschiedenen Erfolgsindikatoren zu erfahren, die mit Kampagnen verbunden sind, wie Umsatz, Produktansichten, Bestellungen usw.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf die Kampagnen konzentrieren, die den meisten Umsatz bringen. <br/>Diese Vorlage verwendet die Metrik „Umsatz“, die Metrik „Produktansichten“, die Metrik „Zusatz zum Warenkorb“, die Metrik „Bestellungen“ und die Metrik „Einheiten“. Außerdem werden die Dimension „Trackingcode“ und die Dimension „Verweisende Domain“ verwendet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobile-app-acquisition-template"
>title="Sehen Sie sich an, wie Ihre Website Besucher auf Mobilgeräten erhält."
>abstract="**Dies kann Ihnen helfen**, die verschiedenen Faktoren besser zu verstehen, die zur Akquise führen, wie Suchbegriffe, verweisende Domain usw.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf die effektivsten Kanäle konzentrieren.<br/>Diese Vorlage verwendet die Metrik „Bounce-Rate“ und die Metrik „Bounces“. Außerdem werden die Dimension „Suchmaschine“, die Dimension „Suchbegriff“, die Dimension „Einstiegsseite“, die Dimension „Verweisende Domain“, die Dimension „Trackingcode“ und die Dimension „Verweisende Stelle“ verwendet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--web-acquisition-template"
>title="Sehen Sie sich an, wie Ihre Website Besuchende erhält."
>abstract="**Dies kann Ihnen helfen**, die verschiedenen Faktoren besser zu verstehen, die zur Akquise führen, wie Suchbegriffe, verweisende Domain usw.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf die effektivsten Kanäle konzentrieren.<br/>Diese Vorlage verwendet die Metrik „Bounce-Rate“ und die Metrik „Bounces“. Außerdem werden die Dimension „Suchmaschine“, die Dimension „Suchbegriff“, die Dimension „Einstiegsseite“, die Dimension „Verweisende Domain“, die Dimension „Trackingcode“ und die Dimension „Verweisende Stelle“ verwendet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--advertisingAnalyticsPaidSearch"
>title="Zeigen Sie alle Ihre Google- und Bing Paid Search-Daten nebeneinander an."
>abstract="**Dies kann Ihnen** dabei helfen, den Umfang des an Ihre Site gesendeten Traffics besser zu verstehen und zu verstehen, ob Kunden konvertieren.<br/>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. die Kostenwirksamkeit einer Anzeigenkampagne schätzen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--searchKeywordRankedReport"
>title="Zeigen Sie die Keywords an, die Besuchende zum Erreichen Ihrer Site verwenden, unabhängig davon, ob es sich um Paid Search oder organische Suche handelt."
>abstract="**Dies kann Ihnen helfen**, die Keywords besser zu verstehen, die bei Suchvorgängen verwendet werden, die zu Sitetraffic führen. <br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. SEO-Lücken zwischen den verwendeten Keywords und den Keywords, die den Sitetraffic fördern, identifizieren und füllen.<br/>Diese Vorlage verwendet die Dimension „Suchbegriff“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--searchPaidKeywordRankedReport"
>title="Zeigen Sie die Suchbegriffe an, die Besuchende zum Erreichen Ihrer Site verwenden und die mit der Paid-Search-Erkennung übereinstimmen."
>abstract="**Dies kann Ihnen helfen**, die Keywords besser zu verstehen, die bei Suchvorgängen verwendet werden, die zu Sitetraffic führen. <br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. SEO-Lücken zwischen den verwendeten Keywords und den Keywords, die den Sitetraffic fördern, identifizieren und füllen. <br/>Diese Vorlage verwendet die Dimension „Suchbegriff – Paid“. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--searchNaturalKeywordRankedReport"
>title="Zeigen Sie die Suchbegriffe an, die Besuchende zum Erreichen Ihrer Site verwenden und die nicht mit der Paid-Search-Erkennung übereinstimmen."
>abstract="**Dies kann Ihnen helfen**, die Keywords besser zu verstehen, die bei Suchvorgängen verwendet werden, die zu Sitetraffic führen. <br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. SEO-Lücken zwischen den verwendeten Keywords und den Keywords, die den Sitetraffic fördern, identifizieren und füllen.<br/>Diese Vorlage verwendet die Dimension „Suchbegriff – Organisch“. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--searchRankedReport"
>title="Zeigen Sie die Suchmaschinen an, die Besuchende zum Erreichen Ihrer Site verwenden, unabhängig davon, ob dafür bezahlt wurde oder sie natürlich sind."
>abstract="**Dies kann Ihnen helfen**, die Suchmaschinen besser zu verstehen, die bei Suchvorgängen verwendet werden, die zu Sitetraffic führen. <br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre SEO-Bemühungen auf die Suchmaschinen konzentrieren, die den meisten Traffic zur Site leiten.<br/>Diese Vorlage verwendet die Dimension „Suchmaschine“. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--searchPaidRankedReport"
>title="Zeigen Sie die Suchmaschinen an, die Besuchende zum Erreichen Ihrer Site verwenden und die mit der Paid-Search-Erkennung übereinstimmen."
>abstract="**Dies kann Ihnen helfen**, die Suchmaschinen besser zu verstehen, die bei Suchvorgängen verwendet werden, die zu Sitetraffic führen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre SEO-Bemühungen auf die Suchmaschinen konzentrieren, die den meisten Traffic zur Site leiten. <br/>Diese Vorlage verwendet die Dimension „Suchmaschine – Paid“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--searchNaturalRankedReport"
>title="Zeigen Sie die Suchbegriffe an, die Besuchende zum Erreichen Ihrer Site verwenden und die nicht mit der Paid-Search-Erkennung übereinstimmen."
>abstract="**Dies kann Ihnen helfen**, die Suchmaschinen besser zu verstehen, die bei Suchvorgängen verwendet werden, die zu Sitetraffic führen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre SEO-Bemühungen auf die Suchmaschinen konzentrieren, die den meisten Traffic zur Site leiten.<br/>Diese Vorlage verwendet die Dimension „Suchmaschine – Organisch“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--searchEngineRankRankedReport"
>title="Zeigen Sie an, welche Seite mit Suchergebnissen ein Besucher zu Ihrer Site durchgeklickt hat. Wenn Ihre Site beispielsweise auf der zweiten Seite der Suchergebnisse einer Suchmaschine erscheint, ist das Dimensionselement für diese Variable &quot;Suchseite 2&quot;."
>abstract="**Dies kann Ihnen** helfen, besser zu verstehen, wie hoch die Rangfolge Ihrer Seiten in den Suchergebnissen ist.<br/>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen und Ihre SEO-Strategie verbessern, um sicherzustellen, dass Ihr Inhalt auf der ersten Seite der Suchergebnisse angezeigt wird."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--referringDomainRankedReport"
>title="Zeigen Sie an, durch welche Domains Besuchende sich klicken, um Ihre Site zu erreichen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Sites von Drittanbietern den meisten Traffic zu Ihrer Site leiten. (Auf der externen Site muss ein Link vorhanden sein und Besuchende müssen darauf klicken, damit das Dimensionselement angezeigt wird.)<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Inhalte erstellen oder anpassen, um sie besser an die Interessen der Besuchenden von den verweisenden Top-Domains anzupassen. <br/>Diese Vorlage verwendet die Dimension „Verweisende Domain“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--referringDomainOriginalRankedReport"
>title="Zeigen Sie die erste verweisende Domain an, durch die sich Personen zum Erreichen Ihrer Site geklickt haben. (Sobald sie festgelegt wurde, enthält sie denselben Wert für die gesamte Lebensdauer dieser Besucher-ID.)"
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Drittanbieter-Sites den Traffic ursprünglich zu Ihrer Site leiten.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Inhalte erstellen oder anpassen, um sie besser an die Interessen der Besuchenden von den ursprünglichen verweisenden Top-Domains anzupassen. <br/>Diese Vorlage verwendet die Dimension „Ursprünglich verweisende Domain“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--referrerRankedReport"
>title="Zeigen Sie an, auf welchen URLs sich die Besuchenden befanden, als sie sich zu Ihrer Site durchklickten. (Auf der externen URL muss ein Link vorhanden sein, und Besuchende müssen darauf klicken, damit das Dimensionselement angezeigt wird.)"
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche spezifischen URLs den meisten Traffic zu Ihrer Site leiten. <br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Inhalte erstellen oder anpassen, um sie besser an die Interessen der Besuchenden von den Top-URLs anzupassen. <br/>Diese Vorlage verwendet die Dimension „Verweisende Domain“.</p>"

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-template--referrerTypeRankedReport"
>title="Zeigen Sie an, durch welche generischen Kanäle Besuchende sich geklickt haben, um zu Ihrer Site zu gelangen. Adobe verwaltet die Regeln für jeden Kanal. Mögliche Kanäle sind Suchmaschinen, soziale Netzwerke, andere Websites, die Festplatte oder E-Mails."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Referrer-Typen den meisten Traffic zu Ihrer Site leiten. <br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Inhalte erstellen oder anpassen, um sie besser an die Interessen der Besuchenden von einem bestimmten Kanal anzupassen. <br/>Diese Vorlage verwendet die Dimension „Referrer-Typ“."

<!-- markdownlint-enable MD034 -->

Die folgenden Vorlagen sind verfügbar:

| Vorlagenname | Warum diese Vorlage <!-- What do you do with it? What can it help you learn? and What are the potential actions? --> verwenden |
| --- | --- | 
| [!UICONTROL **Marketingkanäle**] > [!UICONTROL **Marketingkanal-Übersichtsbericht**] | Bei Verwendung der benutzerdefinierten Attribution zeigt diese Vorlage, wie Besuchende auf Ihre Site gelangen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Ihrer Marketing-Kanäle am effektivsten sind.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. intensiver in effektive Marketing-Kanäle investieren und weniger effektive Marketing-Kanäle aufgeben.</p><p>Diese Vorlage verwendet die Dimension ID (Variablen/Marketing-Kanal) und die Metrik Umsatz .</p> |
| [!UICONTROL **Marketingkanäle**] > [!UICONTROL **Erstkontakt Marketingkanal**] | Zeigen Sie die ersten Marketing-Kanäle an, zu denen Besuchende während ihres Interaktionszeitraums (standardmäßig 30 Tage) passen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Marketing-Kanäle den anfänglichen Traffic zu Ihrer Site leiten.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf Bereiche konzentrieren, die am effektivsten sind.</p><p>Diese Vorlage verwendet die Dimension Erstkontakt Kanal .</p> |
| [!UICONTROL **Marketingkanäle**] > [!UICONTROL **Erstkontakt Marketingkanaldetail**] | Zeigen Sie Details zu den ersten Marketing-Kanälen an, zu denen Besuchende während ihres Interaktionszeitraums (standardmäßig 30 Tage) passen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, was dazu beigetragen hat, dass der Treffer zu einem Marketing-Kanal passte. Wenn beispielsweise ein Besucher zu Ihrer Site gelangt ist und mit dem Marketing-Kanal „Paid Search“ übereinstimmt, können Sie anhand des Kanaldetails sehen, welche Suchmaschine verwendet wurde oder nach welchem Schlüsselwort er gesucht hat.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf Bereiche konzentrieren, die am effektivsten sind.</p><p>Diese Vorlage verwendet die Dimension Erstkontakt Kanaldetail .</p> |
| [!UICONTROL **Marketingkanäle**] > [!UICONTROL **Letztkontakt Marketingkanal**] | Zeigen Sie den neuesten Marketing-Kanal an, mit dem ein Besucher während des Interaktionszeitraums des Besuchers übereinstimmt (standardmäßig 30 Tage).<p>**Dies kann Ihnen** helfen, besser zu verstehen, welche Marketing-Kanäle Traffic zu Ihrer Site leiten, der zu Konversionen führt.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf Bereiche konzentrieren, die am effektivsten sind.</p><p>Diese Vorlage verwendet die Dimension Letztkontakt Kanal .  </p> |
| [!UICONTROL **Marketingkanäle**] > [!UICONTROL **Letztkontakt Marketingkanaldetail**] | Details zum neuesten Marketing-Kanal anzeigen, mit dem ein Besucher während des Interaktionszeitraums des Besuchers (standardmäßig 30 Tage) übereinstimmt<p>**Dies kann Ihnen helfen**, besser zu verstehen, was dazu beigetragen hat, dass der Treffer zu einem Marketing-Kanal passte. Wenn beispielsweise ein Besucher zu Ihrer Site gelangt ist und mit dem Marketing-Kanal „Paid Search“ übereinstimmt, können Sie anhand des Kanaldetails sehen, welche Suchmaschine verwendet wurde oder nach welchem Schlüsselwort er gesucht hat.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf Bereiche konzentrieren, die am effektivsten sind. </p><p>Diese Vorlage verwendet die Dimension Letztkontakt Kanaldetail . </p> |
| [!UICONTROL **Kampagnen**] > [!UICONTROL **Kampagnen (Trackingcode)**] | Zeigen Sie die Namen der Trackingcodes auf Ihrer Site an. Sie können Links mit unterschiedlichen Abfragezeichenfolgenparameterwerten an verschiedenen Stellen im Internet platzieren.<p>**Dies kann Ihnen** helfen, besser zu verstehen, welche Links am erfolgreichsten zur Erhöhung des Traffics auf Ihre Site beigetragen haben. Abfragezeichenfolgen für Trackingcodes werden häufig in E-Mails, Anzeigen, Social-Media-Beiträgen und anderen Marketing-Maßnahmen verwendet, die Ihr Unternehmen verwendet</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Maßnahmen durchführen, z. B. Marketing-Maßnahmen auf die Kampagnen zu konzentrieren, die den meisten Umsatz bringen.</p><p>Diese Vorlage verwendet die Dimension Trackingcode . </p> |
| [!UICONTROL **Kampagnen**] > [!UICONTROL **Kampagnenkonversionstrichter**] | <p>**Dies hilft Ihnen**, besser zu verstehen</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. </p><p>Diese Vorlage verwendet die  </p> |
| [!UICONTROL **Kampagnen**] > [!UICONTROL **Kampagnenleistung**] | Zeigen Sie Details zur Leistung Ihrer Marketing-Kampagnen an.<p>**Dies kann Ihnen helfen**, mehr über die verschiedenen Erfolgsindikatoren zu erfahren, die mit Kampagnen verbunden sind, wie Umsatz, Produktansichten, Bestellungen usw.</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Maßnahmen durchführen, z. B. Marketing-Maßnahmen auf die Kampagnen zu konzentrieren, die den meisten Umsatz bringen. </p><p>Diese Vorlage verwendet die Metrik Umsatz , die Metrik Produktansichten , die Metrik Zusatz zum Warenkorb , die Metrik Bestellungen und Einheiten . Außerdem werden die Dimension „Trackingcode“ und die Dimension „Verweisende Domain“ verwendet. </p> |
| **Mobile Akquise** | Sehen Sie sich an, wie Ihre Site Besucher auf Mobilgeräten erhält.<p>**Dies kann Ihnen helfen**, die verschiedenen Faktoren besser zu verstehen, die zur Akquise führen, wie Suchbegriffe, verweisende Domain usw.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf die effektivsten Kanäle konzentrieren.</p><p>Diese Vorlage verwendet die Metrik Absprungrate und die Metrik Absprünge . Außerdem werden die Dimension „Suchmaschine“, die Dimension „Suchbegriff“, die Dimension „Einstiegsseite“, die Dimension „Verweisende Domain“, die Dimension „Trackingcode“ und die Dimension „Verweisende Stelle“ verwendet.  </p> |
| **Web-Akquise** | Sehen Sie sich an, wie Ihre Website Besuchende erhält.<p>**Dies kann Ihnen helfen**, die verschiedenen Faktoren besser zu verstehen, die zur Akquise führen, wie Suchbegriffe, verweisende Domain usw.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf die effektivsten Kanäle konzentrieren.</p><p>Diese Vorlage verwendet die Metrik Absprungrate und die Metrik Absprünge . Außerdem werden die Dimension „Suchmaschine“, die Dimension „Suchbegriff“, die Dimension „Einstiegsseite“, die Dimension „Verweisende Domain“, die Dimension „Trackingcode“ und die Dimension „Verweisende Stelle“ verwendet.  </p> |
| **Advertising Analytics: Gebührenpflichtige Suche** | Zeigen Sie alle Ihre Google- und Bing Paid Search-Daten nebeneinander an. <p>**Dies kann Ihnen** dabei helfen, den Umfang des an Ihre Site gesendeten Traffics besser zu verstehen und zu verstehen, ob Kunden konvertieren.</p><p>**Je nachdem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. die Kostenwirksamkeit einer Anzeigenkampagne schätzen.</p> |
| **Suchkeywords-all** | Zeigen Sie die Keywords an, die Besuchende zum Erreichen Ihrer Site verwenden, unabhängig davon, ob es sich um Paid Search oder organische Suche handelt. <p>**Dies kann Ihnen helfen**, die Keywords besser zu verstehen, die bei Suchvorgängen verwendet werden, die zu Sitetraffic führen.  </p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. SEO-Lücken zwischen den verwendeten Keywords und den Keywords, die den Sitetraffic fördern, identifizieren und füllen.</p><p>Diese Vorlage verwendet die Dimension Suchbegriff . </p> |
| **Suchkeywords-paid** | Zeigen Sie die Suchbegriffe an, die Besuchende zum Erreichen Ihrer Site verwenden und die mit der Paid-Search-Erkennung übereinstimmen.<p>**Dies kann Ihnen helfen**, die Keywords besser zu verstehen, die bei Suchvorgängen verwendet werden, die zu Sitetraffic führen. </p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. SEO-Lücken zwischen den verwendeten Keywords und den Keywords, die den Sitetraffic fördern, identifizieren und füllen. </p><p>Diese Vorlage verwendet die Dimension Suchbegriff - Gebührenpflichtig . </p> |
| **Suchkeywords-kostenlos** | Zeigen Sie die Suchbegriffe an, die Besuchende zum Erreichen Ihrer Site verwenden und die nicht mit der Paid-Search-Erkennung übereinstimmen.<p>**Dies kann Ihnen helfen**, die Keywords besser zu verstehen, die bei Suchvorgängen verwendet werden, die zu Sitetraffic führen. </p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. SEO-Lücken zwischen den verwendeten Keywords und den Keywords, die den Sitetraffic fördern, identifizieren und füllen.</p><p>Diese Vorlage verwendet die Dimension Suchbegriff - Kostenlos . </p> |
| **Suchmaschinen-Alle** | Zeigen Sie die Suchmaschinen an, die Besuchende zum Erreichen Ihrer Site verwenden, unabhängig davon, ob dafür bezahlt wurde oder sie natürlich sind. <p>**Dies kann Ihnen helfen**, die Suchmaschinen besser zu verstehen, die bei Suchvorgängen verwendet werden, die zu Sitetraffic führen. </p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre SEO-Bemühungen auf die Suchmaschinen konzentrieren, die den meisten Traffic zur Site leiten.</p><p>Diese Vorlage verwendet die Dimension Suchmaschine . </p> |
| **Suchmaschinen-bezahlt** | Zeigen Sie die Suchmaschinen an, die Besuchende zum Erreichen Ihrer Site verwenden und die mit der Paid-Search-Erkennung übereinstimmen.<p>**Dies kann Ihnen helfen**, die Suchmaschinen besser zu verstehen, die bei Suchvorgängen verwendet werden, die zu Sitetraffic führen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre SEO-Bemühungen auf die Suchmaschinen konzentrieren, die den meisten Traffic zur Site leiten. </p><p>Diese Vorlage verwendet die Dimension Suchmaschine - Gebührenpflichtig . </p> |
| **Suchmaschinen-kostenlos** | Zeigen Sie die Suchbegriffe an, die Besuchende zum Erreichen Ihrer Site verwenden und die nicht mit der Paid-Search-Erkennung übereinstimmen.<p>**Dies kann Ihnen helfen**, die Suchmaschinen besser zu verstehen, die bei Suchvorgängen verwendet werden, die zu Sitetraffic führen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre SEO-Bemühungen auf die Suchmaschinen konzentrieren, die den meisten Traffic zur Site leiten.</p><p>Diese Vorlage verwendet die Dimension Suchmaschine - Kostenlos . </p> |
| **Rangansicht aller Suchseiten** | Zeigen Sie an, welche Seite mit Suchergebnissen ein Besucher zu Ihrer Site durchgeklickt hat. Wenn Ihre Site beispielsweise auf der zweiten Seite der Suchergebnisse einer Suchmaschine erscheint, ist das Dimensionselement für diese Variable „Suchseite 2“.<p>**Dies kann Ihnen** helfen, besser zu verstehen, wie hoch die Rangfolge Ihrer Seiten in den Suchergebnissen ist.</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen und Ihre SEO-Strategie verbessern, um sicherzustellen, dass Ihr Inhalt auf der ersten Seite der Suchergebnisse angezeigt wird. </p> |
| **Referrerdomänen** | Zeigen Sie an, durch welche Domains Besuchende sich klicken, um Ihre Site zu erreichen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Sites von Drittanbietern den meisten Traffic zu Ihrer Site leiten. (Auf der externen Site muss ein Link vorhanden sein und Besuchende müssen darauf klicken, damit das Dimensionselement angezeigt wird.)</p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Inhalte erstellen oder anpassen, um sie besser an die Interessen der Besucher aus den Top-Referrer-Domänen anzupassen. </p><p>Diese Vorlage verwendet die Dimension Referrer-Domäne . </p> |
| **Ursprünglich Referrerdomänen** | Zeigen Sie die erste verweisende Domain an, durch die sich Personen zum Erreichen Ihrer Site geklickt haben. (Sobald sie festgelegt wurde, enthält sie denselben Wert für die gesamte Lebensdauer dieser Besucher-ID.)<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Drittanbieter-Sites den Traffic ursprünglich zu Ihrer Site leiten.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Inhalte erstellen oder anpassen, um sie besser an die Interessen der Besucher aus den ursprünglichen Referrerdomänen anzupassen. </p><p>Diese Vorlage verwendet die Dimension &quot;Ursprünglich verweisende Domäne&quot;. </p> |
| **Verweisende Stellen** | Zeigen Sie an, auf welchen URLs sich die Besuchenden befanden, als sie sich zu Ihrer Site durchklickten. (Auf der externen URL muss ein Link vorhanden sein, und Besuchende müssen darauf klicken, damit das Dimensionselement angezeigt wird.)  <p>**Dies kann Ihnen helfen**, besser zu verstehen, welche spezifischen URLs den meisten Traffic zu Ihrer Site leiten. </p><p>**Basierend auf dem, was Sie lernen, können Sie** eine beliebige Anzahl von Dingen ausführen, z. B. Inhalte erstellen oder anpassen, um sie besser an die Interessen der Besucher anzupassen, die von Top-URLs kommen. </p><p>Diese Vorlage verwendet die Dimension Referrerdomäne . </p><p>Diese Vorlage verwendet die Dimension Referrer . </p> |
| **Typen der verweisenden Stellen** | Zeigen Sie an, durch welche generischen Kanäle Besuchende sich geklickt haben, um zu Ihrer Site zu gelangen. Adobe verwaltet die Regeln für jeden Kanal. Mögliche Kanäle sind Suchmaschinen, soziale Netzwerke, andere Websites, die Festplatte oder E-Mails.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Referrer-Typen den meisten Traffic zu Ihrer Site leiten. </p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Inhalte erstellen oder anpassen, um sie besser an die Interessen der Besuchenden von einem bestimmten Kanal anzupassen. </p><p>Diese Vorlage verwendet die Dimension Referrer-Typ .</p> |