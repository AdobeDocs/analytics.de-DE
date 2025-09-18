---
description: Erfahren Sie mehr über die Standardvorlagen in Analysis Workspace und wie Sie diese Standardvorlagen verwenden.
title: Verwenden von Vorlagen
feature: Analysis Workspace
role: User, Admin
exl-id: 9e5d1b35-e2b3-4fa5-af12-67bb913675bc
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: ht
source-wordcount: '18674'
ht-degree: 100%

---

# Verwenden von Vorlagen

Vorlagen (oder Unternehmensvorlagen) in Analysis Workspace bieten Quick Insights in die gängigsten Berichtsszenarien. Im Folgenden finden Sie einige Beispiele für Fragen, die Sie mit Vorlagen beantworten können:

* Wie viele Personen Ihre Website besuchen
* Wie viele dieser Besucher Unique Visitors darstellen (d. h. nur ein Mal gezählt werden)
* Wie diese zu Ihrer Site gelangten (ob sie einem Link folgen oder Ihre Site direkt aufrufen)
* Welche Keywords die Besucher zum Browsen des Site-Inhalts einsetzen
* Wie lange sie auf einer bestimmten Seite oder der gesamten Website verweilen
* Welche Links von Besuchern angeklickt wurden und wann diese die Seite verlassen haben
* Welche Marketingkanäle am wirksamsten zu Umsatz oder Konversion-Ereignissen führen
* Wie viel Zeit sie mit dem Anschauen eines Videos verbracht haben
* Welche Browser und Geräte zum Besuch der Seite genutzt wurden

Im Folgenden wird beschrieben, wie Sie über die Registerkarte [!UICONTROL Vorlagen] in Analysis Workspace auf Vorlagen zugreifen und sie nutzen können.

## Zugriff auf und Verwendung einer Vorlage

1. Wählen Sie in Analysis Workspace die Registerkarte [!UICONTROL **Workspace**].

   <!--update screenshot -->

   ![Registerkarte „Berichte“](assets/view-prebuilt-templates-full.png)

1. Wählen Sie im Abschnitt [!UICONTROL **Vorlagen**] eine der folgenden Registerkarten aus:

   * **[!UICONTROL Adobe-Vorlagen]**: Zeigt alle von Adobe bereitgestellten Vorlagen an.

   * **[!UICONTROL _Unternehmens_Anmeldename _-Vorlagen]**: Zeigt alle Unternehmensvorlagen an, die für Ihre Organisation erstellt wurden.

     Nur Admins können Unternehmensvorlagen erstellen. Weitere Informationen zum Erstellen einer Unternehmensvorlage finden Sie unter [Erstellen und Verwalten von Vorlagen](/help/analyze/analysis-workspace/templates/create-templates.md).

1. Verwenden Sie eine der folgenden Optionen, um die Anzeige der verfügbaren Vorlagen zu ändern:

   * Wählen Sie aus, ob Vorlagen in einer Spaltenansicht oder einer Kartenansicht angezeigt werden sollen, indem Sie entweder die Spaltenansicht ![ViewColumn](/help/assets/icons/ViewColumn.svg) oder das Kartenansichtssymbol ![Card](/help/assets/icons/Card.svg) auswählen.

   * Wenn Sie die Kartenansicht ![Card](/help/assets/icons/Card.svg) verwenden, wählen Sie aus den folgenden Sortierreihenfolgen: **[!UICONTROL Zuletzt verwendet]**, **[!UICONTROL Am beliebtesten]**, **[!UICONTROL Alphabetisch]**, **[!UICONTROL Nach Kategorie]**.

1. Geben Sie im Suchfeld den Namen der Vorlage ein, die Sie finden möchten, und wählen Sie sie dann aus der Liste der Vorlagen aus. Sie können in der Liste der Vorlagen auch nach Eigenschaft, eVar und Ereignisnummer suchen. <!-- still true? --> 

   Oder

   Wählen Sie die Vorlagenkategorie, die Sie anzeigen möchten, und dann die Vorlage aus der Liste der Vorlagen aus.

   >[!TIP]
   >
   >Um mithilfe der Pfeiltasten durch das Menü zu navigieren, drücken Sie die Schrägstrich-Taste (/) und dann die Nach-unten-Taste. Drücken Sie die Eingabetaste, um die ausgewählte Vorlage zu laden.

   Eine Liste der verfügbaren Vorlagen finden Sie im Abschnitt [Verfügbare Vorlagen](#available-reports) unten.

## Erstellen eines Projekts basierend auf einer Vorlage {#use-reports}

Eine Vorlage erfüllt möglicherweise nicht genau Ihre Anforderungen, kann Sie jedoch näher ans Ziel bringen. In diesen Fällen können Sie die Vorlage als Ausgangspunkt verwenden und sie dann bestmöglich an Ihre spezifischen Zwecke anpassen.

Wenn Sie von einer Vorlage wegnavigieren, nachdem Sie sie geändert haben, werden Sie aufgefordert, Ihre Änderungen zu speichern oder zu verwerfen. Wenn Änderungen an einer Vorlage gespeichert werden, wird die Vorlage als neues Projekt gespeichert.

So passen Sie eine Vorlage an und speichern sie als Projekt:

1. Wählen Sie in Adobe Analytics die Registerkarte [!UICONTROL **Workspace**] aus.

1. Wählen Sie die Registerkarte [!UICONTROL **Vorlagen**] aus.

1. Wählen Sie die Vorlage aus, die Sie anzeigen möchten. Wählen Sie zum Beispiel unter [!UICONTROL **Am beliebtesten**] die Vorlage [!UICONTROL **Seiten**] aus.

   ![Bericht zu Seiten](assets/pages-report.png)

1. Die Seitenvorlage, wie in Analysis Workspace angezeigt, zeigt zwei [Visualisierungen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md) ([Balkendiagramm](/help/analyze/analysis-workspace/visualizations/bar.md) und [Zusammenfassungszahl](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)) sowie eine [Freiformtabelle](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md) an. Die verwendete Metrik ist „Vorkommen“.
1. Führen Sie einen der folgenden Schritte aus:

   * Zeigen Sie die Vorlage an.
   * Sie können ein oder mehrere Segmente oben in den Ablagebereich ziehen. Ziehen Sie beispielsweise das Segment [!UICONTROL **Mobile-Kunden**] und sehen Sie sich die Ergebnisse an.
   * Ändern Sie den Datumsbereich, indem Sie zum Kalender oben rechts gehen.
   * Fügen Sie Dimensionsaufschlüsselungen hinzu, ziehen Sie andere Metriken hinzu und passen Sie die Vorlage allgemein entsprechend Ihren Anforderungen an.

1. (Optional) Speichern Sie die Vorlage als Projekt, indem Sie [!UICONTROL **Projekt**] > [!UICONTROL **Speichern**] auswählen.

   Dadurch wird die Vorlage als neues Projekt gespeichert. Die vorhandene Vorlage wird dabei nicht geändert. Weitere Informationen zum Speichern von Projekten finden Sie unter [Speichern von Projekten](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md).

## Verfügbare Vorlagen

So greifen Sie auf alle verfügbaren vorkonfigurierten Vorlagen zu:

1. Wählen Sie in Adobe Analytics die Registerkarte [!UICONTROL **Arbeitsbereich**] und dann die Registerkarte [!UICONTROL **Vorlagen**] aus.

   Vorkonfigurierte Vorlagen sind nach Kategorie sortiert.

   <!--add screenshot-->

1. Wählen Sie eine Kategorie aus, um die darin enthaltenen Vorlagen anzuzeigen.

   Die folgenden Abschnitte entsprechen den verfügbaren Kategorien und enthalten Informationen zu den einzelnen Vorlagen.

   * **[[!UICONTROL Am beliebtesten]](#most-popular)**

   * **[[!UICONTROL Interaktion]](#engagement)**

### Am beliebtesten {#most-popular}

<!--AA only-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--unitsOvertimeReport"
>title="Zeigen Sie Gesamtanzahl der bei allen Bestellungen gekauften Einheiten an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie Verkäufe von Einheiten im Laufe der Zeit zu- oder abnehmen. Sie können ein Segment anwenden, um zu erfahren, welche Kundinnen und Kunden oder Regionen die meisten Einheiten kaufen und wie der Trend bei den Verkäufen dieser Einheiten im Laufe der Zeit aussieht.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne bewerten, indem Sie Verkäufe von Einheiten vor und nach dem Start der Kampagne vergleichen. Oder Sie vergleichen jährliche Verkäufe von Einheiten während der Feiertage.<br/>Diese Vorlage verwendet die Dimension „Tag“ und die Metrik „Einheit“."

<!-- markdownlint-enable MD034 -->

<!--both AA and CJA-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--training"
>title="Schulungsanleitung"
>abstract="Erfahren Sie mehr über die gängige Terminologie und die Schritte zum Erstellen Ihrer ersten Analyse in Analysis Workspace."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--pagesRankedReport"
>title="Identifizieren Sie die beliebtesten und unbeliebtesten Seiten."
>abstract="**Dies kann Ihnen helfen**, Ihre Zielgruppe und die Art von Informationen, die sie am meisten interessiert, besser zu verstehen.<br/>**Basierend auf dem, was Sie erfahren, können Sie** eine Reihe von Schritten ausführen, z. B. Seitenmetadaten anpassen, um die Sichtbarkeit auf seltener angezeigten Seiten zu erhöhen, oder Zeit in die Verbesserung des Inhalts Ihrer am häufigsten angezeigten Seiten investieren.<br/>Diese Vorlage verwendet die Dimension „Seite“ und die Metrik „Seitenansichten“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--pageViewsOvertimeReport"
>title="Zeigen Sie die Gesamtanzahl der Seitenansichten an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. "
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie der Traffic auf Ihrer Site im Laufe der Zeit möglicherweise zu- oder abnimmt.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne bewerten, indem Sie den Sitetraffic vor und nach dem Start der Kampagne vergleichen. Oder Sie vergleichen den jährlichen Feiertags-Traffic.<br/>Diese Vorlage verwendet die Dimension „Tag“ und die Metrik „Seitenansichten“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--visitsOvertimeReport"
>title="Zeigen Sie die Gesamtanzahl der Besuche an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie der Traffic auf Ihrer Site im Laufe der Zeit möglicherweise zu- oder abnimmt.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne bewerten, indem Sie den Sitetraffic vor und nach dem Start der Kampagne vergleichen. Oder Sie vergleichen den jährlichen Feiertags-Traffic.<br/>Diese Vorlage verwendet die Dimension „Tag“ und die Metrik „Besuche“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--visitorsOvertimeReport"
>title="Zeigen Sie die Gesamtanzahl der Unique Visitors an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. "
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie die Reichweite und die Zielgruppengröße Ihrer Site im Laufe der Zeit oder im Vergleich mit einem früheren Zeitraum zu- oder abnimmt.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob eine kürzlich gestartete Marketing-Kampagne erfolgreich darin war, neue Personen auf die Site zu locken, indem Sie Unique Visitors vor und nach dem Start der Kampagne vergleichen. Oder Sie können die Anzahl der Personen vergleichen, die die Site jedes Jahr während der Feiertage besuchen.<br/>Diese Vorlage verwendet die Dimension „Tag“ und die Metrik „Unique Visitors“. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--keyMetricsReport"
>title="Zeigen Sie einen Bericht an, der die Metriken „Seitenansichten“, „Besuche“ und „Unique Visitors“ nebeneinander anzeigt. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen."
>abstract="**Dies kann Ihnen helfen**, diese wichtigen Metriken zu vergleichen, um ein vollständigeres Bild über die Anzahl der Unique Visitors auf der Site, die Anzahl der Seitenbesuche und die Anzahl der Sitzungen zu erhalten.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die durchschnittliche Anzahl der Seiten bewerten, die jede Person während eines Besuchs auf der Site in einer bestimmten Woche oder in einem bestimmten Monat angesehen hat, und ermitteln, wie sich dies während bestimmter Zeiten des Jahres oder vor und nach der Durchführung von Marketing-Kampagnen verändert hat. <br/>Diese Vorlage verwendet die Dimension „Tag“, die Metrik „Seitenansichten“, die Metrik „Besuche“ und die Metrik „Unique Visitors“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--siteSectionRankedReport"
>title="Zeigen Sie die beliebtesten oder leistungsstärksten Bereiche Ihrer Site an."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Bereiche Ihrer Site am häufigsten besucht werden.<br>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, welche Ihrer Produkte oder Services das meiste Interesse generieren.<br/>Diese Vorlage verwendet die Dimension „Site-Bereich“ und die Metrik „Besuche“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--next-page-report"
>title="Sehen Sie sich die Bereiche an, die Personen am häufigsten direkt nach dem Besuch einer bestimmten Seite aufrufen."
>abstract="**Dies kann Ihnen helfen**, das Benutzerverhalten nach dem Besuch einer bestimmten Seite besser zu verstehen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob das Seiten-Design oder -Layout optimiert werden kann, um Personen zu wünschenswerteren Seiten zu leiten, etwa zu einer Seite, auf der sie einen Kauf tätigen oder eine Bewertung abgeben.<br/>Diese Vorlage verwendet die Dimension „Seite“ und die Metrik „Ereignisse“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--previous-page-report"
>title="Sehen Sie sich die Bereiche an, die Personen am häufigsten direkt vor dem Besuch einer bestimmten Seite aufrufen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Seiten den meisten Traffic zu einer bestimmten Seite leiten.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob Seiten, die nicht als vorherige Seiten angezeigt werden, markantere Links zur aktuellen Seite benötigen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--campaignRankedReport"
>title="Zeigen Sie die Links an, die am erfolgreichsten Traffic auf Ihre Site geleitet haben."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Trackingcodes (und Links, mit denen sie verknüpft sind) am häufigsten beim Zugriff auf Ihre Site verwendet wurden.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Strategie anpassen, wo Sie Links zu Ihrer Site hinzufügen.<br/>Diese Vorlage verwendet die Dimension „Trackingcode“ und die Metrik „Besuche“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--productsRankedReport"
>title="Zeigen Sie die Anzahl der Bestellungen nach Produkt an. Daten werden für einen bestimmten Zeitraum angezeigt."
>abstract="**Dies kann Ihnen helfen**, zu verstehen, welche Produkte die höchste oder die geringste Nachfrage aufweisen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Marketing-Strategien so anpassen, dass sie leistungsstarke Produkte bewerben oder Produkte mit schlechter Leistung verbessern oder einstellen. Sie könnten auch Ihren Produktbestand auf Grundlage Ihrer Datenanalyse anpassen.<br/>Diese Vorlage verwendet die Dimension „Produkt“ und die Metrik „Bestellungen“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--lastTouchChannelRankedReport"
>title="Zeigen Sie die neuesten Marketing-Kanäle an, zu denen Besuchende während ihres Interaktionszeitraums (standardmäßig 30 Tage) passen."
>abstract="**Dies kann Ihnen dabei helfen**, zu verstehen, welche Marketing-Kanäle am effektivsten waren, um Personen zu Ihrer Site zu leiten und um Konversionen zu erreichen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. mehr Ressourcen für leistungsstarke Kanäle oder weniger Ressourcen für leistungsschwache Kanäle zuweisen.<br/>Diese Vorlage verwendet die Dimension „Letztkontaktkanal“ und die Metrik „Unique Visitors“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--lastTouchChannelDetailRankedReport"
>title="Zeigen Sie Details zu den neuesten Marketing-Kanälen an, zu denen Besuchende während ihres Interaktionszeitraums (standardmäßig 30 Tage) passen."
>abstract="**Dies kann Ihnen dabei helfen**, nicht nur zu verstehen, welche Marketing-Kanäle am effektivsten waren, um Personen zu Ihrer Site zu leiten und Konversionen zu erreichen, sondern Sie erhalten auch Details zu diesen Marketing-Kanälen. Wenn beispielsweise eine Besucherin oder ein Besucher zu Ihrer Site gelangt ist und mit dem Marketing-Kanal „Paid Search“ übereinstimmt, können Sie anhand des Kanaldetails sehen, welche Suchmaschine verwendet wurde oder nach welchem Keyword die Person gesucht hat.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. mehr Ressourcen für leistungsstarke Kanäle oder weniger Ressourcen für leistungsschwache Kanäle zuweisen.<br/>Diese Vorlage verwendet die Dimension „Details des Letztkontaktkanals“ und die Metrik „Unique Visitors“. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--revenueOvertimeReport"
>title="Zeigen Sie den Geldbetrag der bei allen Bestellungen gekauften Produkte an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen."
>abstract="**Dies kann Ihnen helfen**, zu verstehen, wie der Umsatz im Laufe der Zeit zu- oder abnimmt. Sie können diese Metrik mit einer beliebigen Dimension kombinieren, um zu erfahren, welche Dimensionselemente zum Umsatz beigetragen haben.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. zukünftige Umsätze basierend auf früheren Trends planen. Sie können auch eine weitere Dimension hinzufügen, z. B. die Dimension „Trackingcode“, um zu erfahren, welche Kampagnen den meisten Umsatz generieren.<br/>Diese Vorlage verwendet die Dimension „Tag“ und die Metrik „Umsatz“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--ordersOvertimeReport"
>title="Zeigen Sie die Gesamtanzahl der Kaufereignisse an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie das Interesse an Ihren Produkten und Services im Laufe der Zeit zu- oder abnimmt. Sie können ein Segment anwenden, um zu erfahren, welche Kundinnen und Kunden oder Regionen die meisten Bestellungen aufgeben und wie der Trend bei diesen Bestellungen im Laufe der Zeit aussieht.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne durch den Vergleich der Bestellungen vor und nach dem Start der Kampagne bewerten. Oder Sie vergleichen die jährlichen Bestellungen zu Feiertagen.<br/>Diese Vorlage verwendet die Dimension „Tag“ und die Metrik „Bestellungen“."

<!-- markdownlint-enable MD034 -->

Die folgenden Vorlagen sind verfügbar:

| Vorlagenname | Warum diese Vorlage verwenden? <!-- What do you do with it? What can it help you learn? and What are the potential actions? --> |
| --- | --- | 
| [!UICONTROL **Anleitungsvideo**] | Erfahren Sie mehr über die gängige Terminologie und die Schritte zum Erstellen Ihrer ersten Analyse in Analysis Workspace |
| [!UICONTROL **Seiten**] | <!--duplicated in Engagement section--> Identifizieren Sie die beliebtesten und unbeliebtesten Seiten. <p>**Dies kann Ihnen helfen**, Ihre Zielgruppe und die Art von Informationen, die sie am meisten interessiert, besser zu verstehen.</p><p>**Basierend auf dem, was Sie erfahren, können Sie** eine Reihe von Schritten ausführen, z. B. Seitenmetadaten anpassen, um die Sichtbarkeit auf seltener angezeigten Seiten zu erhöhen, oder Zeit in die Verbesserung des Inhalts Ihrer am häufigsten angezeigten Seiten investieren.</p><p>Diese Vorlage verwendet die [Dimension „Seite“](/help/components/dimensions/page.md) und die [Metrik „Seitenansichten“](/help/components/metrics/page-views.md).</p> |
| [!UICONTROL **Seitenansichten**] | <!--duplicated in Engagement section--> Zeigen Sie die Gesamtanzahl der Seitenansichten an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, wie der Traffic auf Ihrer Site im Laufe der Zeit möglicherweise zu- oder abnimmt.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne bewerten, indem Sie den Sitetraffic vor und nach dem Start der Kampagne vergleichen. Oder Sie vergleichen den jährlichen Feiertags-Traffic.</p><p>Diese Vorlage verwendet die [Dimension „Tag“](/help/components/dimensions/day.md) und die [Metrik „Seitenansichten“](/help/components/metrics/page-views.md).</p> |
| [!UICONTROL **Besuche**] | <!--duplicated in Engagement section--> Zeigen Sie die Gesamtanzahl der Besuche an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, wie der Traffic auf Ihrer Site im Laufe der Zeit möglicherweise zu- oder abnimmt.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne bewerten, indem Sie den Sitetraffic vor und nach dem Start der Kampagne vergleichen. Oder Sie vergleichen den jährlichen Feiertags-Traffic.</p><p>Diese Vorlage verwendet die [Dimension „Tag“](/help/components/dimensions/day.md) und die [Metrik „Besuche“](/help/components/metrics/visits.md).</p> |
| [!UICONTROL **Besucher**] | <!--duplicated in Engagement section--> Zeigen Sie die Gesamtanzahl der Unique Visitors an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, wie die Reichweite und die Zielgruppengröße Ihrer Site im Laufe der Zeit oder im Vergleich mit einem früheren Zeitraum zu- oder abnimmt.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob eine kürzlich gestartete Marketing-Kampagne erfolgreich darin war, neue Personen auf die Site zu locken, indem Sie Unique Visitors vor und nach dem Start der Kampagne vergleichen. Oder Sie können die Anzahl der Personen vergleichen, die die Site jedes Jahr während der Feiertage besuchen.</p><p>Diese Vorlage verwendet die [Dimension „Tag“](/help/components/dimensions/day.md) und die [Metrik „Unique Visitors“](/help/components/metrics/unique-visitors.md).</p> |
| [!UICONTROL **Schlüsselmetriken**] | <!--duplicated in Engagement section--> Zeigen Sie einen Bericht an, der die Metriken „Seitenansichten“, „Besuche“ und „Unique Visitors“ nebeneinander anzeigt. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, diese wichtigen Metriken zu vergleichen, um ein vollständigeres Bild über die Anzahl der Unique Visitors auf der Site, die Anzahl der Seitenbesuche und die Anzahl der Sitzungen zu erhalten.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die durchschnittliche Anzahl der Seiten bewerten, die jede Person während eines Besuchs auf der Site in einer bestimmten Woche oder in einem bestimmten Monat angesehen hat, und ermitteln, wie sich dies während bestimmter Zeiten des Jahres oder vor/nach der Durchführung von Marketing-Kampagnen verändert hat.  </p><p>Diese Vorlage verwendet die [Dimension „Tag“](/help/components/dimensions/day.md), die [Metrik „Seitenansichten“](/help/components/metrics/page-views.md), die [Metrik „Besuche“](/help/components/metrics/visits.md) und die [Metrik „Unique Visitors“](/help/components/metrics/unique-visitors.md).</p> |
| [!UICONTROL **Site-Bereiche**] | Zeigen Sie die beliebtesten oder leistungsstärksten Bereiche Ihrer Site an. <p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Bereiche Ihrer Site am häufigsten besucht werden.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, welche Ihrer Produkte oder Services das meiste Interesse generieren.</p> <p>Diese Vorlage verwendet die [Dimension „Site-Bereich“](/help/components/dimensions/site-section.md) und die [Metrik „Besuche“](/help/components/metrics/visits.md).</p> |
| [!UICONTROL **Tracking-Code**] | Zeigen Sie die Links an, die am erfolgreichsten Traffic auf Ihre Site geleitet haben. <p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Trackingcodes (und Links, mit denen sie verknüpft sind) am häufigsten beim Zugriff auf Ihre Site verwendet wurden.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Strategie anpassen, wo Sie Links zu Ihrer Site hinzufügen.</p><p>Diese Vorlage verwendet die [Dimension „Tracking-Code“](/help/components/dimensions/tracking-code.md) und die [Metrik „Besuche“](/help/components/metrics/visits.md).</p> |
| [!UICONTROL **Nächste Seite**] | Sehen Sie sich die Bereiche an, die Personen am häufigsten direkt nach dem Besuch einer bestimmten Seite aufrufen. <p>**Dies kann Ihnen helfen**, das Benutzerverhalten nach dem Besuch einer bestimmten Seite besser zu verstehen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob das Seiten-Design oder -Layout optimiert werden kann, um Personen zu wünschenswerteren Seiten zu leiten, etwa zu einer Seite, auf der sie einen Kauf tätigen oder eine Bewertung abgeben.</p> <p>Diese Vorlage verwendet die Dimension „Seite“ und die Metrik „Ereignisse“.</p> |
| [!UICONTROL **Vorherige Seite**] | Sehen Sie sich die Bereiche an, die Personen am häufigsten direkt vor dem Besuch einer bestimmten Seite aufrufen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Seiten den meisten Traffic zu einer bestimmten Seite leiten.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob Seiten, die nicht als vorherige Seiten angezeigt werden, markantere Links zur aktuellen Seite benötigen.</p><p>Diese Vorlage verwendet die Dimension „Seite“ und die Metrik „Ereignisse“.</p> |
| [!UICONTROL **Produkte**] | Zeigen Sie die Anzahl der Bestellungen nach Produkt an. Daten werden für einen bestimmten Zeitraum angezeigt. <p>**Dies kann Ihnen helfen**, zu verstehen, welche Produkte die höchste oder die geringste Nachfrage aufweisen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Marketing-Strategien so anpassen, dass sie leistungsstarke Produkte bewerben oder Produkte mit schlechter Leistung verbessern oder einstellen. Sie könnten auch Ihren Produktbestand auf Grundlage Ihrer Datenanalyse anpassen.</p><p>Diese Vorlage verwendet die [Dimension „Produkt“](/help/components/dimensions/product.md) und die [Metrik „Bestellungen“](/help/components/metrics/orders.md).</p> |
| [!UICONTROL **Letztkontaktkanal**] | Zeigen Sie die neuesten Marketing-Kanäle an, zu denen Besuchende während ihres Interaktionszeitraums (standardmäßig 30 Tage) passen.<p>**Dies kann Ihnen dabei helfen**, zu verstehen, welche Marketing-Kanäle am effektivsten waren, um Personen zu Ihrer Site zu leiten und um Konversionen zu erreichen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. mehr Ressourcen für leistungsstarke Kanäle oder weniger Ressourcen für leistungsschwache Kanäle zuweisen.</p><p>Diese Vorlage verwendet die [Dimension „Letztkontaktkanal“](/help/components/dimensions/last-touch-channel.md) und die [Metrik „Unique Visitors“](/help/components/metrics/unique-visitors.md).</p> |
| [!UICONTROL **Detail des Letztkontaktkanals**] | Zeigen Sie Details zu den neuesten Marketing-Kanälen an, zu denen Besuchende während ihres Interaktionszeitraums (standardmäßig 30 Tage) passen.<p>**Dies kann Ihnen dabei helfen**, nicht nur zu verstehen, welche Marketing-Kanäle am effektivsten waren, um Personen zu Ihrer Site zu leiten und Konversionen zu erreichen, sondern Sie erhalten auch Details zu diesen Marketing-Kanälen. Wenn beispielsweise eine Besucherin oder ein Besucher zu Ihrer Site gelangt ist und mit dem Marketing-Kanal „Paid Search“ übereinstimmt, können Sie anhand des Kanaldetails sehen, welche Suchmaschine verwendet wurde oder nach welchem Keyword die Person gesucht hat.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. mehr Ressourcen für leistungsstarke Kanäle oder weniger Ressourcen für leistungsschwache Kanäle zuweisen.</p><p>Diese Vorlage verwendet die [Dimension „Detail des Letztkontaktkanals“](/help/components/dimensions/last-touch-detail.md) und die [Metrik „Unique Visitors“](/help/components/metrics/unique-visitors.md).</p> |
| [!UICONTROL **Umsatz**] | Zeigen Sie den Geldbetrag der bei allen Bestellungen gekauften Produkte an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen.<p>**Dies kann Ihnen helfen**, zu verstehen, wie der Umsatz im Laufe der Zeit zu- oder abnimmt. Sie können diese Metrik mit einer beliebigen Dimension kombinieren, um zu erfahren, welche Dimensionselemente zum Umsatz beigetragen haben.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. zukünftige Umsätze basierend auf früheren Trends planen. Sie können auch eine weitere Dimension hinzufügen, z. B. die Dimension „Trackingcode“, um zu erfahren, welche Kampagnen den meisten Umsatz generieren.</p><p>Diese Vorlage verwendet die [Dimension „Tag“](/help/components/dimensions/day.md) und die [Metrik „Umsatz“](/help/components/metrics/revenue.md).</p> |
| [!UICONTROL **Bestellungen**] | Zeigen Sie die Gesamtanzahl der Kaufereignisse an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, wie das Interesse an Ihren Produkten und Services im Laufe der Zeit zu- oder abnimmt. Sie können ein Segment anwenden, um zu erfahren, welche Kundinnen und Kunden oder Regionen die meisten Bestellungen aufgeben und wie der Trend bei diesen Bestellungen im Laufe der Zeit aussieht.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne durch den Vergleich der Bestellungen vor und nach dem Start der Kampagne bewerten. Oder Sie vergleichen die jährlichen Bestellungen zu Feiertagen.</p><p>Diese Vorlage verwendet die [Dimension „Tag“](/help/components/dimensions/day.md) und die [Metrik „Bestellungen“](/help/components/metrics/orders.md).</p> |
| [!UICONTROL **Einheiten**] | Zeigen Sie Gesamtanzahl der bei allen Bestellungen gekauften Einheiten an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, wie Verkäufe von Einheiten im Laufe der Zeit zu- oder abnehmen. Sie können ein Segment anwenden, um zu erfahren, welche Kundinnen und Kunden oder Regionen die meisten Einheiten kaufen und wie der Trend bei den Verkäufen dieser Einheiten im Laufe der Zeit aussieht.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne bewerten, indem Sie Verkäufe von Einheiten vor und nach dem Start der Kampagne vergleichen. Oder Sie vergleichen jährliche Verkäufe von Einheiten während der Feiertage.</p><p>Diese Vorlage verwendet die [Dimension „Tag“](/help/components/dimensions/day.md) und die [Metrik „Einheiten“](/help/components/metrics/units.md).</p> |

### Interaktion {#web-engagement}

<!--AA only-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--real-time"
>title="Zeigen Sie die Dimensionen und Metriken an, die derzeit auf Ihrer Site erfasst werden."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, was auf Ihrer Site im Trend liegt.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. auf die Leistung Ihrer aktuellen Marketing-Inhalte und -Kampagnen reagieren und diese aktiv verwalten."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--timeSpentVisitOvertimeReport"
>title="Zeigen Sie die durchschnittliche Zeit an, die Besuchende während jedes Besuchs auf Ihrer Site verbringen. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen."
>abstract="**Dies kann Ihnen helfen**, die Interaktionsstufen der Besucherinnen und Besucher besser zu verstehen und herauszufinden, wie viel Zeit sie auf der Site verbringen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob Änderungen an Ihrer Site dazu führen, dass Besuchende mehr Zeit auf der Site verbringen.<br/>Diese Vorlage verwendet die Dimension „Tag“ und die Metrik „Pro Besuch aufgewendete Zeit (Sekunden)“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--timePriorRankedReport"
>title="Zeigen Sie die durchschnittliche Zeit an, die Benutzende vor einem Erfolgsereignis auf der Site verbringen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie viel Zeit Besuchende benötigen, um eine gewünschte Aktion durchzuführen, z. B. einen Kauf.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob Änderungen an Ihrer Site es den Besuchenden erleichtert, schnell ein Erfolgsereignis zu erreichen.<br/>Diese Vorlage verwendet die Dimension „Zeit vor Ereignis“ und die Metrik „Unique Visitors“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--falloutReport"
>title="Zeigen Sie an, wo Personen die Site verlassen oder über eine vordefinierte Seitensequenz fortfahren."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wo Personen aus der Benutzer-Journey aussteigen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Konversionsraten durch bestimmte Prozesse auf Ihrer Site (wie etwa Kauf- oder Registrierungsprozesse) oder Korrelationen zwischen Ereignissen auf Ihrer Site analysieren. (Zum Beispiel, welcher Prozentsatz der Personen, die sich die Datenschutzrichtlinien angesehen haben, danach ein Produkt kauften.) Sie können diese Vorlage auch verwenden, um zwei verschiedene Segmente im selben Bericht nebeneinander zu vergleichen.<br/>Diese Vorlage verwendet die Visualisierung „Fallout“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--cross-device-analysis"
>title="Zeigen Sie an, welche Geräte von Personen in allen Phasen der Journey verwendet werden."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie viele Personen mit Ihrer Marke interagieren, welche Arten von Geräten sie verwenden und wie die Verwendung mehrerer Geräte ihr Erlebnis beeinflusst. Wie oft beginnen Personen beispielsweise mit einer Aufgabe auf einem Mobilgerät und wechseln dann zu einem Desktop, um die Aufgabe abzuschließen? Welche sind die häufigsten Pfade, die Benutzer beim Wechsel von einem Gerät zum anderen verwenden? Wo steigen sie aus? Wo sind sie erfolgreich? Und so weiter.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bestimmte Abschnitte der Benutzer-Journey für mobile Erlebnisse optimieren.<br/>Diese Vorlage verwendet die Visualisierung „Fluss“, die Visualisierung „Fallout“, die Analyse „Kohorte“, die „Metrik für Personen“ und die Metrik „Eindeutige Geräte“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--web-retention"
>title="Zeigen Sie an, wer Ihre treuen Benutzenden sind und was sie auf Ihrer Site tun."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie oft eine durchschnittliche Person Ihre Site besucht, mit welcher Häufigkeit Personen zur Site zurückkehren und wie viele Tage zwischen wiederkehrenden Besuchen vergehen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. analysieren, welcher Inhalt am effektivsten dazu beiträgt, dass Personen zur Site zurückkehren.<br/>Diese Vorlage verwendet die Dimension „Besuche“ und die Metrik „Unique Visitors“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--audio-consumption-template"
>title="Zeigen Sie Trends und Top-Metriken des Konsums von Audiomedien über alle digitalen Geräte hinweg an."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie Besuchende Audioinhalte auf Ihrer Site konsumieren.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. analysieren, welcher Inhalt am meisten konsumiert wird.<br/>Diese Vorlage verwendet die Dimension „Besuche“ und die Metrik „Unique Visitors“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--media-recency-frequency-loyalty"
>title="Zeigen Sie Trends und Top-Metriken des Medienkonsums über alle digitalen Geräte hinweg an."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie oft eine durchschnittliche Person Ihre Site besucht, mit welcher Häufigkeit Personen zur Site zurückkehren und wie viele Tage zwischen wiederkehrenden Besuchen vergehen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. analysieren, welcher Inhalt am effektivsten dazu beiträgt, dass Personen zur Site zurückkehren.<br/>Diese Vorlage verwendet die Dimension „Besuche“ und die Metrik „Unique Visitors“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--reloadsRankedReport"
>title="Zeigen Sie an, wie oft ein Dimensionselement während eines Neuladens vorhanden war. Ein Besucher, der seinen Browser aktualisiert, stellt die häufigste Methode dar, eine Neuladung auszulösen."
>abstract="**Dies kann Ihnen helfen**, festzustellen, wann Probleme auf einer bestimmten Seite auftreten können, die Besuchende dazu auffordern würden, die Seite neu zu laden.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, auf welchen Seiten Probleme auftreten, die behoben werden müssen.<br/>Diese Vorlage verwendet die Metrik „Neuladungen“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--timeSpentPageRankedReport"
>title="Zeigen Sie die durchschnittliche Zeit an, die Besuchende während jedes Besuchs auf Ihrer Site verbringen. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen."
>abstract="**Dies kann Ihnen helfen**, die Interaktionsstufen der Besucherinnen und Besucher besser zu verstehen und herauszufinden, wie viel Zeit sie auf der Site verbringen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob Änderungen an Ihrer Site dazu führen, dass Besuchende mehr Zeit auf der Site verbringen.<br/>Diese Vorlage verwendet die Dimension „Tag“ und die Metrik „Pro Besuch aufgewendete Zeit (Sekunden)“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--entryPageOriginalRankedReport"
>title="Zeigen Sie die wichtigsten Seiten an, auf die Personen beim ersten Besuch Ihrer Site während ihrer Lebensdauer zugreifen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Seiten den meisten Traffic zu Ihrer Site leiten, oder mehr über die ersten Eindrücke zu erfahren, die Besuchende auf Ihrer Site haben.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. das erste Erlebnis optimieren, das Personen auf der Site haben, oder sicherstellen, dass die Seiten, die Personen beim Eintritt in Ihre Site zuerst sehen, einladend sind und die erforderlichen Links zu anderen Bereichen Ihrer Site bereitstellen.<br/>Diese Vorlage verwendet die Metrik „Sitzungen“. Außerdem werden die Visualisierungen „Balken“ und „Freiformtabelle“ verwendet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--singlePageVisitsRankedReport"
>title="Zeigen Sie die Anzahl der Besuche an, die aus einer einzigen eindeutigen Seite bestanden."
>abstract="**Dies kann Ihnen helfen**, die Interaktionsstufen der Besuchenden besser zu verstehen und herauszufinden, wie viel Zeit Besuchende auf der Site verbringen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob Änderungen an Ihrer Site dazu führen, dass Besuchende mehr Zeit auf der Site verbringen.<br/>Diese Vorlage verwendet die Dimension „Einzelseitenbesuche“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--sitePerformanceOverview"
>title="Zeigen Sie Leistungsdaten für Ihre Adobe Experience Manager-Site an."
>abstract="**Dies kann Ihnen helfen**, die Wertrealisierung von Adobe Experience Manager besser zu verstehen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Einstellungen von Experience Manager optimieren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--formsPerformanceOverview"
>title="Zeigen Sie Leistungsdaten für Ihre Adobe Experience Manager Forms-Version an."
>abstract="**Dies kann Ihnen helfen**, die Wertrealisierung von Adobe Experience Manager besser zu verstehen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Einstellungen von Experience Manager optimieren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--itp-impact"
>title="Zeigen und analysieren Sie die Auswirkungen von Intelligent Tracking Prevention (ITP) auf die Datenerfassung und Reporting an und analysieren Sie sie."
>abstract="**Dies kann Ihnen helfen**, potenzielle Datenverluste aufgrund von durch ITP auferlegte Cookie-Beschränkungen besser zu verstehen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihr Analyse-Setup so anpassen, dass die Auswirkungen von ITP minimiert werden."

<!-- markdownlint-enable MD034 -->

<!--Both AA and CJA-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template_time_spent"
>title="Zeigen Sie die durchschnittliche Besuchszeit auf Ihrer Site während jedes Besuchs sowie die durchschnittliche Besuchszeit vor einem Erfolgsereignis an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen."
>abstract="**Dies kann Ihnen helfen**, die Interaktionsstufen der Besuchenden besser zu verstehen und herauszufinden, wie viel Zeit Besuchende benötigen, um eine gewünschte Aktion durchzuführen, z. B. einen Kauf.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob Änderungen an Ihrer Site es den Besuchenden erleichtert, schnell ein Erfolgsereignis zu erreichen.<br/>Diese Vorlage verwendet die Dimension „Tag“, die Metrik „Pro Besuch aufgewendete Zeit (Sekunden)“, die Dimension „Tag“ und die Metrik „Pro Besuch aufgewendete Zeit (Sekunden)“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--web-content-consumption"
>title="Zeigen Sie an, welche Web-Inhalte am häufigsten genutzt werden und für Benutzende interessant sind."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wo Personen beim ersten Aufrufen der Site hingehen, welche Bereiche der Site von Personen am häufigsten besucht werden und welche Seiten Personen am wahrscheinlichsten von der Site wegführen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, welche Pfade auf der Site Personen zu den wichtigsten Seiten führen und welche Seiten Personen wahrscheinlicher von der Site wegführen.<br/>Diese Vorlage verwendet die Dimension „Seite“ und die Metrik „Seitenansichten“, die Metrik „Besuche“, die Metrik „Unique Visitors“, die Metrik „Eintrittsrate“, die Metrik „Bounce-Rate“, die Metrik „Ausstiegsrate“ und die Metrik „Contentgeschwindigkeit“. Außerdem werden die Visualisierungen „Fluss“ für Eintritts-, Ausstiegs- und Top-Abschnitte verwendet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--media-content-consumption"
>title="Zeigen Sie an, welche Medieninhalte am häufigsten genutzt werden und für Benutzende interessant sind."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wo Personen beim ersten Aufrufen der Site hingehen, welche Bereiche der Site von Personen am häufigsten besucht werden und welche Seiten Personen am wahrscheinlichsten von der Site wegführen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, welche Pfade auf der Site Personen zu den wichtigsten Seiten führen und welche Seiten Personen wahrscheinlicher von der Site wegführen.<br/>Diese Vorlage verwendet die Dimension „Seite“ und die Metrik „Seitenansichten“, die Metrik „Besuche“, die Metrik „Unique Visitors“, die Metrik „Eintrittsrate“, die Metrik „Bounce-Rate“, die Metrik „Ausstiegsrate“ und die Metrik „Contentgeschwindigkeit“. Darüber hinaus werden die Visualisierungen „Fluss“ für Eintritts-, Ausstiegs- und Top-Abschnitte verwendet. Eine Streudiagrammvisualisierung zeigt die Seitenansichten für die gängigsten Seiten an. Eine Balkenvisualisierung zeigt die Seitenansichten nach zusammengefasster Zeit an. Eine Linienvisualisierung stellt eine Trend-Ansicht der durchschnittlichen Besuchszeit auf der Site dar."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--flowreport"
>title="Sehen Sie sich die Bereiche an, die Personen am häufigsten direkt nach einem Besuch oder unmittelbar vor dem Besuch eines bestimmten Bereichs aufrufen."
>abstract="**Dies kann Ihnen dabei helfen**, zu verstehen, wie sich der Traffic von einer bestimmten Seite zu anderen Teilen Ihrer Site bewegt. Außerdem können Sie die Pfade verstehen, die Personen nehmen, um zu einer bestimmten Seite zu gelangen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob das Seiten-Design oder -Layout optimiert werden kann, um Personen zu wünschenswerteren Seiten zu leiten, z. B. zu einer Seite, auf der sie einen Kauf tätigen oder eine Rezension abgeben. Oder bewerten Sie, ob die Informationen auf der aktuellen Seite wahrscheinlich die Richtung oder die Aktionen angeben, nach denen Personen suchen, wenn sie von vorherigen Seiten kommen. Sie könnten auch bewerten, ob Seiten, die nicht als vorherige Seiten angezeigt werden, markantere Links zur aktuellen Seite benötigen.<br/>Diese Vorlage verwendet das Panel „Nächstes oder vorheriges Objekt“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--page-summary-report"
>title="Zeigen Sie wichtige Informationen zu einer Seite in Ihren Eigenschaften an. Zeigt Seitenansichten, eine Trend-Linie, eine Flussvisualisierung und mehr an."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie Personen mit einer bestimmten Seite interagieren.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Leistung der Seite über einen bestimmten Zeitraum analysieren oder besser verstehen, was den Traffic zur Seite bringt.<br/>Diese Vorlage verwendet die Metrik „Seitenansichten“. Außerdem werden die Visualisierungen „Linie“ und „Fluss“ verwendet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--entryPageRankedReport"
>title="Zeigen Sie die wichtigsten Seiten an, auf die Personen beim ersten Besuch Ihrer Site zugreifen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Seiten den meisten Traffic zu Ihrer Site leiten, oder mehr über die ersten Eindrücke zu erfahren, die Besuchende auf Ihrer Site haben.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. das erste Erlebnis optimieren, das Personen auf der Site haben, oder sicherstellen, dass die Seiten, die Personen beim Eintritt in Ihre Site zuerst sehen, einladend sind und die erforderlichen Links zu anderen Bereichen Ihrer Site bereitstellen.<br/>Diese Vorlage verwendet die Metrik „Sitzungen“. Außerdem werden die Visualisierungen „Balken“ und „Freiformtabelle“ verwendet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--exitPageRankedReport"
>title="Zeigen Sie die wichtigsten Seiten an, auf die Personen unmittelbar vor dem Verlassen Ihrer Site zugreifen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Seiten Personen von der Site wegführen. <br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. gängige Exitpages aktualisieren, um das Erlebnis zu optimieren, das Personen vor dem Verlassen haben, oder Inhalte oder Links aufnehmen, um Personen dazu aufzufordern, auf Ihrer Site zu bleiben.<br/>Diese Vorlage verwendet die Metrik „Sitzungen“. Außerdem werden die Balkenvisualisierung und die Freiformtabellenvisualisierung verwendet."

<!-- markdownlint-enable MD034 -->

Die folgenden Vorlagen sind verfügbar:

| Vorlagenname | Warum diese Vorlage verwenden?<!-- What do you do with it? What can it help you learn? and What are the potential actions? --> |
| --- | --- | 
| [!UICONTROL **Schlüsselmetriken**] | <!--duplicated in Most popular section--> Zeigen Sie einen Bericht an, der die Metriken „Seitenansichten“, „Besuche“ und „Unique Visitors“ nebeneinander anzeigt. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, diese wichtigen Metriken zu vergleichen, um ein vollständigeres Bild über die Anzahl der Unique Visitors auf der Site, die Anzahl der Seitenbesuche und die Anzahl der Sitzungen zu erhalten.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die durchschnittliche Anzahl der Seiten bewerten, die jede Person während eines Besuchs auf der Site in einer bestimmten Woche oder in einem bestimmten Monat angesehen hat, und ermitteln, wie sich dies während bestimmter Zeiten des Jahres oder vor/nach der Durchführung von Marketing-Kampagnen verändert hat.  </p><p>Diese Vorlage verwendet die [Dimension „Tag“](/help/components/dimensions/day.md), die [Metrik „Seitenansichten“](/help/components/metrics/page-views.md), die [Metrik „Besuche“](/help/components/metrics/visits.md) und die [Metrik „Unique Visitors“](/help/components/metrics/unique-visitors.md).</p> |
| [!UICONTROL **Seitenansichten**] | <!--duplicated in Most popular section-->Zeigen Sie die Gesamtanzahl der Seitenansichten an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, wie der Traffic auf Ihrer Site im Laufe der Zeit möglicherweise zu- oder abnimmt.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne bewerten, indem Sie den Sitetraffic vor und nach dem Start der Kampagne vergleichen. Oder Sie vergleichen den jährlichen Feiertags-Traffic.</p><p>Diese Vorlage verwendet die [Dimension „Tag“](/help/components/dimensions/day.md) und die [Metrik „Seitenansichten“](/help/components/metrics/page-views.md).</p> |
| [!UICONTROL **Seiten**] | <!--duplicated in Most popular section-->Identifizieren Sie die beliebtesten und unbeliebtesten Seiten. <p>**Dies kann Ihnen helfen**, Ihre Zielgruppe und die Art von Informationen, die sie am meisten interessiert, besser zu verstehen.</p><p>**Basierend auf dem, was Sie erfahren, können Sie** eine Reihe von Schritten ausführen, z. B. Seitenmetadaten anpassen, um die Sichtbarkeit auf seltener angezeigten Seiten zu erhöhen, oder Zeit in die Verbesserung des Inhalts Ihrer am häufigsten angezeigten Seiten investieren.</p><p>Diese Vorlage verwendet die [Dimension „Seite“](/help/components/dimensions/page.md) und die [Metrik „Seitenansichten“](/help/components/metrics/page-views.md).</p> |
| [!UICONTROL **Besuche**] | <!--duplicated in Most popular section-->Zeigen Sie die Gesamtanzahl der Besuche an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, wie der Traffic auf Ihrer Site im Laufe der Zeit möglicherweise zu- oder abnimmt.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne bewerten, indem Sie den Sitetraffic vor und nach dem Start der Kampagne vergleichen. Oder Sie vergleichen den jährlichen Feiertags-Traffic.</p><p>Diese Vorlage verwendet die [Dimension „Tag“](/help/components/dimensions/day.md) und die [Metrik „Besuche“](/help/components/metrics/visits.md).</p> |
| [!UICONTROL **Besucher**] | <!--duplicated in Most popular section-->Zeigen Sie die Gesamtanzahl der Unique Visitors an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, wie die Reichweite und die Zielgruppengröße Ihrer Site im Laufe der Zeit oder im Vergleich mit einem früheren Zeitraum zu- oder abnimmt.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob eine kürzlich gestartete Marketing-Kampagne erfolgreich darin war, neue Personen auf die Site zu locken, indem Sie Unique Visitors vor und nach dem Start der Kampagne vergleichen. Oder Sie können die Anzahl der Personen vergleichen, die die Site jedes Jahr während der Feiertage besuchen.</p><p>Diese Vorlage verwendet die [Dimension „Tag“](/help/components/dimensions/day.md) und die [Metrik „Unique Visitors“](/help/components/metrics/unique-visitors.md).</p> |
| [!UICONTROL **Zeit pro Besuch**] | Zeigen Sie die durchschnittliche Zeit an, die Besuchende während jedes Besuchs auf Ihrer Site verbringen. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, die Interaktionsstufen der Besucherinnen und Besucher besser zu verstehen und herauszufinden, wie viel Zeit sie auf der Site verbringen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob Änderungen an Ihrer Site dazu führen, dass Besuchende mehr Zeit auf der Site verbringen.</p><p>Diese Vorlage verwendet die [Dimension „Tag“](/help/components/dimensions/day.md) und die [Metrik „Pro Besuch aufgewendete Zeit (Sekunden)“](/help/components/metrics/time-spent-per-visit.md).</p> |
| [!UICONTROL **Zeit vor Ereignis**] | Zeigen Sie die durchschnittliche Zeit an, die Benutzende vor einem Erfolgsereignis auf der Site verbringen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, wie viel Zeit Besuchende benötigen, um eine gewünschte Aktion durchzuführen, z. B. einen Kauf.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob Änderungen an Ihrer Site es den Besuchenden erleichtert, schnell ein Erfolgsereignis zu erreichen.</p><p>Diese Vorlage verwendet die [Dimension „Zeit vor Ereignis“](/help/components/dimensions/time-prior-to-event.md) und die [Metrik „Unique Visitors“](/help/components/metrics/unique-visitors.md).</p> |
| [!UICONTROL **Site-Bereiche**] | <!--duplicated in Most popular section-->Zeigen Sie die beliebtesten oder leistungsstärksten Bereiche Ihrer Site an. <p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Bereiche Ihrer Site am häufigsten besucht werden.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, welche Ihrer Produkte oder Services das meiste Interesse generieren.</p> <p>Diese Vorlage verwendet die [Dimension „Site-Bereich“](/help/components/dimensions/site-section.md) und die [Metrik „Besuche“](/help/components/metrics/visits.md).</p> |
| [!UICONTROL **Echtzeit**] | Zeigen Sie die Dimensionen und Metriken an, die derzeit auf Ihrer Site erfasst werden. <p>**Dies kann Ihnen helfen**, besser zu verstehen, was auf Ihrer Site im Trend liegt.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** auf die Leistung Ihrer aktuellen Marketing-Inhalte und -Kampagnen reagieren und diese aktiv verwalten.</p> <p>Diese Vorlage verwendet den [Echtzeitbericht](/help/admin/tools/manage-rs/edit-settings/realtime/realtime.md).</p> |
| [!UICONTROL **Konsum von Web-Inhalten**] | Zeigen Sie an, welche Web-Inhalte am häufigsten genutzt werden und für Benutzende interessant sind.<p>**Dies kann Ihnen helfen**, besser zu verstehen, wo Personen beim ersten Aufrufen der Site hingehen, welche Bereiche der Site von Personen am häufigsten besucht werden und welche Seiten Personen am wahrscheinlichsten von der Site wegführen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, welche Pfade auf der Site Personen zu den wichtigsten Seiten führen und welche Seiten Personen wahrscheinlicher von der Site wegführen.</p> <p>Diese Vorlage verwendet die [Dimension „Seite“](/help/components/dimensions/page.md) und die [Metrik „Seitenansichten“](/help/components/metrics/page-views.md), die [Metrik „Besuche“](/help/components/metrics/visits.md), die [Metrik „Unique Visitors“](/help/components/metrics/unique-visitors.md), die [Metrik „Eintrittsrate“](/help/components/metrics/entries.md), die Metrik [„Bounce-Rate“](/help/components/metrics/bounce-rate.md), die [Metrik „Ausstiegsrate“](/help/components/metrics/exits.md) und die [Metrik „Inhaltsgeschwindigkeit“](/help/components/metrics/content-velocity.md). Außerdem werden [Flussvisualisierungen](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) für Eintritts-, Ausstiegs- und Top-Abschnitte verwendet.</p> |
| [!UICONTROL **Konsum von Medieninhalten**] | Zeigen Sie an, welche Medieninhalte am häufigsten genutzt werden und für Benutzende interessant sind.<p>**Dies kann Ihnen helfen**, besser zu verstehen, wo Personen beim ersten Aufrufen der Site hingehen, welche Bereiche der Site von Personen am häufigsten besucht werden und welche Seiten Personen am wahrscheinlichsten von der Site wegführen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, welche Pfade auf der Site Personen zu den wichtigsten Seiten führen und welche Seiten Personen wahrscheinlicher von der Site wegführen.</p> <p>Diese Vorlage verwendet die [Dimension „Seite“](/help/components/dimensions/page.md) und die [Metrik „Seitenansichten“](/help/components/metrics/page-views.md), die [Metrik „Besuche“](/help/components/metrics/visits.md), die [Metrik „Unique Visitors“](/help/components/metrics/unique-visitors.md), die [Metrik „Eintrittsrate“](/help/components/metrics/entries.md), die Metrik [„Bounce-Rate“](/help/components/metrics/bounce-rate.md), die [Metrik „Ausstiegsrate“](/help/components/metrics/exits.md) und die [Metrik „Inhaltsgeschwindigkeit“](/help/components/metrics/content-velocity.md). Darüber hinaus werden [Flussvisualisierungen](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) für Eintritts-, Ausstiegs- und Top-Abschnitte verwendet. Eine [Streudiagrammvisualisierung](/help/analyze/analysis-workspace/visualizations/scatterplot.md) zeigt die Seitenansichten für die gängigsten Seiten an. Eine [Balkenvisualisierung](/help/analyze/analysis-workspace/visualizations/bar.md) zeigt die Seitenansichten nach zusammengefasster Zeit an. Eine [Linienvisualisierung](/help/analyze/analysis-workspace/visualizations/line.md) stellt eine Trend-Ansicht der durchschnittlichen Besuchszeit auf der Site dar.</p> |
| [!UICONTROL **Nächster und vorheriger Navigationspfad**] | Zeigen Sie die Bereiche an, die Personen am häufigsten vor oder nach dem Besuch eines bestimmten Bereichs aufrufen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, wo Personen beim ersten Aufrufen der Site hingehen, welche Bereiche der Site von Personen am häufigsten besucht werden und welche Seiten Personen am wahrscheinlichsten besuchen, bevor sie die Site verlassen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, welche Pfade auf der Site Personen zu den wichtigsten Seiten führen und welche Seiten Personen wahrscheinlicher von der Site wegführen.</p> <p>Diese Vorlage verwendet die [Dimension „Seite“](/help/components/dimensions/page.md) und die [Metrik „Seitenansichten“](/help/components/metrics/page-views.md), die [Metrik „Besuche“](/help/components/metrics/visits.md), die [Metrik „Unique Visitors“](/help/components/metrics/unique-visitors.md), die [Metrik „Eintrittsrate“](/help/components/metrics/entries.md), die Metrik [„Bounce-Rate“](/help/components/metrics/bounce-rate.md), die [Metrik „Ausstiegsrate“](/help/components/metrics/exits.md) und die [Metrik „Inhaltsgeschwindigkeit“](/help/components/metrics/content-velocity.md). Darüber hinaus werden [Flussvisualisierungen](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) für Eintritts-, Ausstiegs- und Top-Abschnitte verwendet. Eine [Streudiagrammvisualisierung](/help/analyze/analysis-workspace/visualizations/scatterplot.md) zeigt die Seitenansichten für die gängigsten Seiten an. Eine [Balkenvisualisierung](/help/analyze/analysis-workspace/visualizations/bar.md) zeigt die Seitenansichten nach zusammengefasster Zeit an. Eine [Linienvisualisierung](/help/analyze/analysis-workspace/visualizations/line.md) stellt eine Trend-Ansicht der durchschnittlichen Besuchszeit auf der Site dar.</p> |
| [!UICONTROL **Fallout**] | Zeigen Sie an, wo Personen die Site verlassen oder über eine vordefinierte Seitensequenz fortfahren.<p>**Dies kann Ihnen helfen**, besser zu verstehen, wo Personen aus der Benutzer-Journey aussteigen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Konversionsraten durch bestimmte Prozesse auf Ihrer Site (wie etwa Kauf- oder Registrierungsprozesse) oder Korrelationen zwischen Ereignissen auf Ihrer Site analysieren. (Zum Beispiel, welcher Prozentsatz der Personen, die sich die Datenschutzrichtlinien angesehen haben, danach ein Produkt kauften.) Sie können diese Vorlage auch verwenden, um zwei verschiedene Segmente im selben Bericht nebeneinander zu vergleichen.</p> <p>Diese Vorlage verwendet die [Visualisierung „Fallout“](/help/analyze/analysis-workspace/visualizations/fallout/fallout-flow.md).</p> |
| [!UICONTROL **Geräteübergreifende Analyse**] | Zeigen Sie an, welche Geräte von Personen in allen Phasen der Journey verwendet werden.<p>**Dies kann Ihnen helfen**, besser zu verstehen, wie viele Personen mit Ihrer Marke interagieren, welche Arten von Geräten sie verwenden und wie die Verwendung mehrerer Geräte ihr Erlebnis beeinflusst. Wie oft beginnen Personen beispielsweise mit einer Aufgabe auf einem Mobilgerät und wechseln dann zu einem Desktop, um die Aufgabe abzuschließen? Welche sind die häufigsten Pfade, die Benutzer beim Wechsel von einem Gerät zum anderen verwenden? Wo steigen sie aus? Wo sind sie erfolgreich? Und so weiter.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bestimmte Abschnitte der Benutzer-Journey für mobile Erlebnisse optimieren.</p> <p>Diese Vorlage verwendet die [Flussvisualisierung](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md), die [Fallout-Visualisierung](/help/analyze/analysis-workspace/visualizations/fallout/fallout-flow.md), die [Kohortenanalyse](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md), die [Metrik „Personen“](/help/components/metrics/people.md) und die [Metrik „Eindeutige Geräte](/help/components/metrics/unique-devices.md)“.</p> |
| [!UICONTROL **Web-Bindung**] | Zeigen Sie an, wer Ihre treuen Benutzenden sind und was sie auf Ihrer Site tun.<p>**Dies kann Ihnen helfen**, besser zu verstehen, wie oft eine durchschnittliche Person Ihre Site besucht, mit welcher Häufigkeit Personen zur Site zurückkehren und wie viele Tage zwischen wiederkehrenden Besuchen vergehen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. analysieren, welcher Inhalt am effektivsten dazu beiträgt, dass Personen zur Site zurückkehren.<p>Diese Vorlage verwendet die [Metrik „Besuche“](/help/components/metrics/visits.md) und die [Metrik „Unique Visitors“](/help/components/metrics/unique-visitors.md).</p> |
| [!UICONTROL **Nutzung von Streaming-Medien**] | Zeigen Sie Trends und Top-Metriken des Konsums von Audiomedien über alle digitalen Geräte hinweg an.<p>**Dies kann Ihnen helfen**, besser zu verstehen, wie Besuchende Audioinhalte auf Ihrer Site konsumieren.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. analysieren, welcher Inhalt am meisten konsumiert wird.<p>Diese Vorlage verwendet die [Metrik „Besuche“](/help/components/metrics/visits.md) und die [Metrik „Unique Visitors“](/help/components/metrics/unique-visitors.md).</p> |
| [!UICONTROL **Medien-Neuigkeit, -Häufigkeit, -Treue**] | Zeigen Sie Trends und Top-Metriken des Medienkonsums über alle digitalen Geräte hinweg an.<p>**Dies kann Ihnen helfen**, besser zu verstehen, wie oft eine durchschnittliche Person Ihre Site besucht, mit welcher Häufigkeit Personen zur Site zurückkehren und wie viele Tage zwischen wiederkehrenden Besuchen vergehen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. analysieren, welcher Inhalt am effektivsten dazu beiträgt, dass Personen zur Site zurückkehren.<p>Diese Vorlage verwendet die [Metrik „Besuche“](/help/components/metrics/visits.md) und die [Metrik „Unique Visitors“](/help/components/metrics/unique-visitors.md).</p> |
| **[!UICONTROL Seitenanalyse]** > [!UICONTROL **Seitenzusammenfassung**] | Zeigen Sie die durchschnittliche Zeit an, die Besuchende während jedes Besuchs auf Ihrer Site verbringen. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, die Interaktionsstufen der Besucherinnen und Besucher besser zu verstehen und herauszufinden, wie viel Zeit sie auf der Site verbringen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob Änderungen an Ihrer Site dazu führen, dass Besuchende mehr Zeit auf der Site verbringen.</p><p>Diese Vorlage verwendet die [Dimension „Tag“](/help/components/dimensions/day.md) und die [Metrik „Pro Besuch aufgewendete Zeit (Sekunden)“](/help/components/metrics/time-spent-per-visit.md).</p> |
| **[!UICONTROL Seitenanalyse]** > [!UICONTROL **Neuladungen**] | Zeigen Sie an, wie oft ein Dimensionselement während eines Neuladens vorhanden war. Ein Besucher, der seinen Browser aktualisiert, stellt die häufigste Methode dar, eine Neuladung auszulösen. <p>**Dies kann Ihnen helfen**, festzustellen, wann Probleme auf einer bestimmten Seite auftreten können, die Besuchende dazu auffordern würden, die Seite neu zu laden.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, auf welchen Seiten Probleme auftreten, die behoben werden müssen.</p><p>Diese Vorlage verwendet die [Metrik „Neuladungen“](/help/components/metrics/reloads.md).</p> |
| **[!UICONTROL Seitenanalyse]** > [!UICONTROL **Besuchszeit pro Seite**] | Zeigen Sie die durchschnittliche Zeit an, die Besuchende während jedes Besuchs auf Ihrer Site verbringen. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, die Interaktionsstufen der Besucherinnen und Besucher besser zu verstehen und herauszufinden, wie viel Zeit sie auf der Site verbringen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob Änderungen an Ihrer Site dazu führen, dass Besuchende mehr Zeit auf der Site verbringen.</p><p>Diese Vorlage verwendet die [Dimension „Tag“](/help/components/dimensions/day.md) und die [Metrik „Pro Besuch aufgewendete Zeit (Sekunden)“](/help/components/metrics/time-spent-per-visit.md).</p> |
| **[!UICONTROL Einstiege und Ausstiege]** > [!UICONTROL **Einstiegsseiten**] | Zeigen Sie die wichtigsten Seiten an, auf die Personen beim ersten Besuch Ihrer Site während einer bestimmten Sitzung zugreifen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Seiten den meisten Traffic zu Ihrer Site leiten, oder mehr über die ersten Eindrücke zu erfahren, die Besuchende auf Ihrer Site haben.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. das erste Erlebnis optimieren, das Personen auf der Site haben, oder sicherstellen, dass die Seiten, die Personen beim Eintritt in Ihre Site zuerst sehen, einladend sind und die erforderlichen Links zu anderen Bereichen Ihrer Site bereitstellen.</p><p>Diese Vorlage verwendet die Metrik „Sitzungen“. Außerdem werden die Balkenvisualisierung und die Freiformtabellenvisualisierung verwendet.</p> |
| **[!UICONTROL Einstiege und Ausstiege]** > [!UICONTROL **Ursprüngliche Einstiegsseiten**] | Zeigen Sie die wichtigsten Seiten an, auf die Personen beim ersten Besuch Ihrer Site während ihrer Lebensdauer zugreifen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Seiten den meisten Traffic zu Ihrer Site leiten, oder mehr über die ersten Eindrücke zu erfahren, die Besuchende auf Ihrer Site haben.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. das erste Erlebnis optimieren, das Personen auf der Site haben, oder sicherstellen, dass die Seiten, die Personen beim Eintritt in Ihre Site zuerst sehen, einladend sind und die erforderlichen Links zu anderen Bereichen Ihrer Site bereitstellen.</p><p>Diese Vorlage verwendet die Metrik „Sitzungen“. Außerdem werden die Balkenvisualisierung und die Freiformtabellenvisualisierung verwendet.</p> |
| **[!UICONTROL Einstiege und Ausstiege]** > [!UICONTROL **Einzelseitenbesuche**] | Zeigen Sie die Anzahl der Besuche an, die aus einer einzigen eindeutigen Seite bestanden. <p>**Dies kann Ihnen helfen**, die Interaktionsstufen der Besuchenden besser zu verstehen und herauszufinden, wie viel Zeit Besuchende auf der Site verbringen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. bewerten, ob Änderungen an Ihrer Site dazu führen, dass Besuchende mehr Zeit auf der Site verbringen.</p><p>Diese Vorlage verwendet die [Dimension „Einzelseitenbesuche“](/help/components/dimensions/single-page-visits.md).</p> |
| **[!UICONTROL Einstiege und Ausstiege]** > [!UICONTROL **Ausstiegsseiten**] | Zeigen Sie die wichtigsten Seiten an, auf die Personen unmittelbar vor dem Verlassen Ihrer Site zugreifen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, durch welche Seiten Personen sich von der Site wegführen lassen.  </p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. gängige Exitpages aktualisieren, um das Erlebnis zu optimieren, das Personen vor dem Verlassen haben, oder Inhalte oder Links aufnehmen, um Personen dazu aufzufordern, auf Ihrer Site zu bleiben.</p><p>Diese Vorlage verwendet die Metrik „Sitzungen“. Außerdem werden die Balkenvisualisierung und die Freiformtabellenvisualisierung verwendet.</p> |
| [!UICONTROL **Adobe Experience Manager**] > [!UICONTROL **Übersicht über die Site-Performance**] > [!UICONTROL **AEM-Site-Performance**] | Zeigen Sie Leistungsdaten für Ihre Adobe Experience Manager-Site an.  <p>**Dies kann Ihnen helfen**, die Wertrealisierung von Adobe Experience Manager besser zu verstehen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Einstellungen von Experience Manager optimieren.</p> |
| [!UICONTROL **Adobe Experience Manager**] > [!UICONTROL **Übersicht über die AEM-Formularleistung**] > [!UICONTROL **AEM-Formularleistung**] | Zeigen Sie Leistungsdaten für Ihre Adobe Experience Manager Forms-Version an.  <p>**Dies kann Ihnen helfen**, die Wertrealisierung von Adobe Experience Manager besser zu verstehen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Einstellungen von Experience Manager optimieren.</p> |
| [!UICONTROL **Auswirkungen von ITP**] | Zeigen und analysieren Sie die Auswirkungen von Intelligent Tracking Prevention (ITP) auf die Datenerfassung und Reporting an und analysieren Sie sie. <p>**Dies kann Ihnen helfen**, potenzielle Datenverluste aufgrund von durch ITP auferlegte Cookie-Beschränkungen besser zu verstehen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihr Analyse-Setup so anpassen, dass die Auswirkungen von ITP minimiert werden.</p> |

### Konversion  {#web-conversion}

<!--AA only-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--categoryRankedReport"
>title="Zeigen Sie die Anzahl der Besuche an, die mit jeder Produktkategorie auf Ihrer Site verknüpft sind. Dies ist nützlich für Implementierungen, bei denen die Produktvariable genutzt wird und Metriken zur Produktkategorie angezeigt werden sollen. Die Dimension, die diese Vorlage auffüllt, kann absichtlich leer sein, wenn Sie keine Produkte auf Ihrer Site haben."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Produkte sich am besten verkaufen und am häufigsten aufgerufen werden. &lt;/br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität einer Marketing-Kampagne für ein bestimmtes Produkt messen.<br/>Diese Vorlage verwendet die Dimension „Kategorie“ und die Metrik „Besuche“. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--commerce-and-marketing-management"
>title="Zeigen Sie vorkonfigurierte Einzelhändler-Erkenntnisse in Ihren Handelsaktivitäten an, die Ihnen helfen können, den Absatz zu steigern. Dies richtet sich vor allem an Benutzende von Adobe Commerce, die Vorlage steht aber dem gesamten Online-Einzelhandel zur Verfügung."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie Ihre Handelsaktivitäten zu den Absatzzahlen beitragen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Budgets an Aktivitäten anpassen, die den größten ROI erzielen."

<!-- markdownlint-enable MD034 -->

<!--Both AA and CJA-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--productConversionReport"
>title="Zeigen Sie die Produktkonversion in einer Trichtervisualisierung mit Warenkörben, Checkouts und Bestellungen an. Sie können auch Konversionsprozentsätze sowie Durchschnittswerte von Umsätzen, Einheiten und Bestellungen anzeigen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie Personen den Konversionsvorgang durchlaufen und daraus aussteigen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Website verbessern und so reibungslosere Checkouts ermöglichen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--retail-products-template"
>title="Zeigen Sie die Produkte mit der höchsten Leistung."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Produkte am erfolgreichsten sind.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Finanzierung für erfolgreiche Produkte erhöhen und für weniger erfolgreiche Produkte verringern.<br/>Diese Vorlage verwendet die Metriken „Produktansichten“, „Zusatz zum Warenkorb“, „Bestellungen“, „Umsatz“ und „Einheiten“. Außerdem wird die Dimension „Produkt“ verwendet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--cartConversionReport"
>title="Sehen Sie sich an, wie oft Personen wichtige Checkout-Ereignisse ausgeführt haben, z. B. Hinzufügen von Artikeln zum Warenkorb, Anzeigen des Warenkorbs, Entfernen von Artikeln aus dem Warenkorb und Checkout-Vorgänge."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Teile des Checkout-Prozess-Trichters zu einer Konversion führen und welche eher zum Warenkorbabbruch führen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Reibung bei bestimmten Schritten des Checkout-Prozesses reduzieren.<br/>Diese Vorlage verwendet die"

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--cartsOvertimeReport"
>title="Zeigen Sie die Anzahl der Personen an, die ein Produkt zum Warenkorb hinzugefügt haben."
>abstract="**Dies kann Ihnen dabei helfen**, die Anzahl der Personen besser zu verstehen, die ein Produkt zum Warenkorb hinzufügen, im Gegensatz zur Gesamtzahl der Produkte, die zum Warenkorb hinzugefügt werden.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität Ihrer Produktseiten messen.<br/>Diese Vorlage verwendet die Metrik „Warenkörbe“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--cartViewsOvertimeReport"
>title="Zeigen Sie an, wie oft Personen ihren Warenkorb angezeigt haben."
>abstract="**Dies kann Ihnen dabei helfen**, das Checkout-Erlebnis besser zu verstehen, um die Warenkorbabbruch-Raten zu reduzieren oder die Zeit zwischen Warenkorbergänzungen und Checkouts für verschiedene Produkte zu analysieren.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Aktionen für Produkte anbieten, die am längsten im Warenkorb bleiben und das größte Risiko für einen Abbruch aufweisen.<br/>Diese Vorlage verwendet die Metrik „Warenkorbansichten“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--cartAdditionsOvertimeReport"
>title="Zeigen Sie an, wie häufig Personen etwas zum Warenkorb hinzugefügt haben."
>abstract="**Dies kann Ihnen helfen**, den Teil des Konversionstrichters besser zu verstehen, in dem das Kundeninteresse an einem Produkt so hoch ist, dass es zum Warenkorb hinzugefügt wird.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Produktempfehlungen für alle Kundinnen und Kunden verbessern. Dazu können Sie analysieren, welche Produkte häufig den gleichen Warenkörben hinzugefügt werden, und ähnliche Produkte auf der Grundlage von Artikeln vorschlagen, die bereits im Warenkorb enthalten sind."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--cartRemovalsOvertimeReport"
>title="Zeigen Sie an, wie oft Personen etwas aus dem Warenkorb entfernt haben."
>abstract="**Dies kann Ihnen dabei helfen**, den Teil des Konversionstrichters besser zu verstehen, in dem Kundschaft kein Interesse mehr an einem Produkt hat, oder zu verstehen, wo im Checkout-Prozess möglicherweise Probleme auftreten.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. potenzielle Barrieren beseitigen, die im Checkout-Prozess bestehen könnten, wie ein kompliziertes Kundenerlebnis.<br/>Diese Vorlage verwendet die Metrik „Entnahmen aus Warenkorb“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--purchaseConversionReport"
>title="Zeigen Sie die Kaufkonversion in einer Trichtervisualisierung mit Sitzungen, Warenkörben und Bestellungen an. Sie können auch Konversionsprozentsätze sowie Durchschnittswerte von Umsätzen, Einheiten und Bestellungen anzeigen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie Personen den Konversionsvorgang durchlaufen und daraus aussteigen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Website verbessern und so reibungslosere Checkouts ermöglichen."

<!-- markdownlint-enable MD034 -->

Die folgenden Vorlagen sind verfügbar:

| Vorlagenname | Warum diese Vorlage verwenden?<!-- What do you do with it? What can it help you learn? and What are the potential actions? --> |
| --- | --- | 
| [!UICONTROL **Produktkonversionstrichter**] | Zeigen Sie die Produktkonversion in einer Trichtervisualisierung mit Warenkörben, Checkouts und Bestellungen an. Sie können auch Konversionsprozentsätze sowie Durchschnittswerte von Umsätzen, Einheiten und Bestellungen anzeigen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, wie Personen den Konversionsvorgang durchlaufen und daraus aussteigen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Website verbessern und so reibungslosere Checkouts ermöglichen.</p> |
| **Produkte** | Zeigen Sie an, welche Produkte für Schlüsselmetriken verantwortlich sind, z. B. am häufigsten verkaufte oder angezeigte Produkte. <p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Produkte am erfolgreichsten sind.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Finanzierung für erfolgreiche Produkte erhöhen und für weniger erfolgreiche Produkte verringern.</p><p>Diese Vorlage verwendet die Metrik „Bestellungen“ und die Dimension „Produkt“. |
| **Produktleistung** | Zeigen Sie die Produkte mit der höchsten Leistung.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Produkte am erfolgreichsten sind.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Finanzierung für erfolgreiche Produkte erhöhen und für weniger erfolgreiche Produkte verringern.</p><p>Diese Vorlage verwendet die Metriken „Produktansichten“, „Zusatz zum Warenkorb“, „Bestellungen“, „Umsatz“ und „Einheiten“. Außerdem wird die Dimension „Produkt“ verwendet. |
| **Kategorien** | Zeigen Sie die Anzahl der Besuche an, die mit jeder Produktkategorie auf Ihrer Site verknüpft sind. Dies ist nützlich für Implementierungen, bei denen die Produktvariable genutzt wird und Metriken zur Produktkategorie angezeigt werden sollen. Die Dimension, die diese Vorlage auffüllt, kann absichtlich leer sein, wenn Sie keine Produkte auf Ihrer Site haben.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Produkte sich am besten verkaufen und am häufigsten aufgerufen werden.  </p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität einer Marketing-Kampagne für ein bestimmtes Produkt messen.</p><p>Diese Vorlage verwendet die Dimension „Kategorie“ und die Metrik „Besuche“. |
| **Warenkorbkonversionstrichter** | Sehen Sie sich an, wie oft Personen wichtige Checkout-Ereignisse ausgeführt haben, z. B. Hinzufügen von Artikeln zum Warenkorb, Anzeigen des Warenkorbs, Entfernen von Artikeln aus dem Warenkorb und Checkout-Vorgänge. <p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Teile des Checkout-Prozess-Trichters zu einer Konversion führen und welche eher zum Warenkorbabbruch führen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Reibung bei bestimmten Schritten des Checkout-Prozesses reduzieren.</p><p>Diese Vorlage verwendet die |
| **Warenkörbe** | Zeigen Sie die Anzahl der Personen an, die ein Produkt zum Warenkorb hinzugefügt haben.<p>**Dies kann Ihnen dabei helfen**, die Anzahl der Personen besser zu verstehen, die ein Produkt zum Warenkorb hinzufügen, im Gegensatz zur Gesamtzahl der Produkte, die zum Warenkorb hinzugefügt werden.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität Ihrer Produktseiten messen.</p><p>Diese Vorlage verwendet die Metrik „Warenkörbe“. |
| **Warenkorbansichten** | Zeigen Sie an, wie oft Personen ihren Warenkorb angezeigt haben. <p>**Dies kann Ihnen dabei helfen**, das Checkout-Erlebnis besser zu verstehen, um die Warenkorbabbruch-Raten zu reduzieren oder die Zeit zwischen Warenkorbergänzungen und Checkouts für verschiedene Produkte zu analysieren.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Aktionen für Produkte anbieten, die am längsten im Warenkorb bleiben und das größte Risiko für einen Abbruch aufweisen.</p><p>Diese Vorlage verwendet die Metrik „Warenkorbansichten“. |
| **Zusatz zum Warenkorb** | Zeigen Sie an, wie häufig Personen etwas zum Warenkorb hinzugefügt haben. <p>**Dies kann Ihnen helfen**, den Teil des Konversionstrichters besser zu verstehen, in dem das Kundeninteresse an einem Produkt so hoch ist, dass es zum Warenkorb hinzugefügt wird.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Produktempfehlungen für alle Kundinnen und Kunden verbessern. Dazu können Sie analysieren, welche Produkte häufig demselben Warenkorb hinzugefügt werden, und ähnliche Produkte auf der Grundlage von Artikeln vorschlagen, die bereits im Warenkorb enthalten sind. |
| **Entnahme aus Warenkorb** | Zeigen Sie an, wie oft Personen etwas aus dem Warenkorb entfernt haben.<p>**Dies kann Ihnen dabei helfen**, den Teil des Konversionstrichters besser zu verstehen, in dem Kundschaft kein Interesse mehr an einem Produkt hat, oder zu verstehen, wo im Checkout-Prozess möglicherweise Probleme auftreten.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. potenzielle Barrieren beseitigen, die im Checkout-Prozess bestehen könnten, wie ein kompliziertes Kundenerlebnis.</p><p>Diese Vorlage verwendet die Metrik „Entnahme aus Warenkorb“. |
| **Einkaufskonversionstrichter** | Zeigen Sie die Kaufkonversion in einer Trichtervisualisierung mit Sitzungen, Warenkörben und Bestellungen an. Sie können auch Konversionsprozentsätze sowie Durchschnittswerte von Umsätzen, Einheiten und Bestellungen anzeigen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, wie Personen den Konversionsvorgang durchlaufen und daraus aussteigen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Website verbessern und so reibungslosere Checkouts ermöglichen.</p> |
| **Umsatz** | <!--duplicated in Most popular section-->Zeigen Sie den Geldbetrag der bei allen Bestellungen gekauften Produkte an. <p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Dimensionen zum Umsatz beigetragen haben, indem Sie die Metrik „Umsatz“ mit beliebigen Dimensionen kombinieren. Sie könnten beispielsweise die wichtigsten Kampagnen sehen (mithilfe der Dimension „Trackingcode“), die zum Umsatz beigetragen haben. </p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Kampagnen anpassen, die Ihre erwarteten Umsatzziele nicht erreichen.</p><p>Diese Vorlage verwendet die Metrik „Umsatz“. |
| **Bestellungen** | <!--duplicated in Most popular section-->Zeigen Sie die Gesamtzahl der Kaufereignisse auf Ihrer Site an.  <p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Dimensionselemente zu einer Bestellung beigetragen haben, indem Sie die Metrik „Bestellungen“ mit beliebigen Dimensionen kombinieren. Sie könnten beispielsweise die wichtigsten Kampagnen sehen (mithilfe der Dimension „Trackingcode“), die zu Käufen beigetragen haben.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Kampagnen anpassen, die Ihre erwarteten Kaufziele nicht erreichen. </p><p>Diese Vorlage verwendet die Metrik „Bestellungen“. |
| [!UICONTROL **Einheiten**] | Zeigen Sie Gesamtanzahl der bei allen Bestellungen gekauften Einheiten an. Die Daten werden für einen bestimmten Zeitraum angezeigt und mit früheren Zeiträumen verglichen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, wie Verkäufe von Einheiten im Laufe der Zeit zu- oder abnehmen. Sie können ein Segment anwenden, um zu erfahren, welche Kundinnen und Kunden oder Regionen die meisten Einheiten kaufen und wie der Trend bei den Verkäufen dieser Einheiten im Laufe der Zeit aussieht.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität einer kürzlich gestarteten Marketing-Kampagne bewerten, indem Sie Verkäufe von Einheiten vor und nach dem Start der Kampagne vergleichen. Oder Sie vergleichen jährliche Verkäufe von Einheiten während der Feiertage.</p><p>Diese Vorlage verwendet die [Dimension „Tag“](/help/components/dimensions/day.md) und die [Metrik „Einheiten“](/help/components/metrics/units.md).</p> |
| [!UICONTROL **Magento: Marketing und Commerce**] | Zeigen Sie vorkonfigurierte Einzelhändler-Erkenntnisse in Ihren Handelsaktivitäten an, die Ihnen helfen können, den Absatz zu steigern. Dies richtet sich vor allem an Benutzende von Adobe Commerce, die Vorlage steht aber dem gesamten Online-Einzelhandel zur Verfügung. <p>**Dies kann Ihnen helfen**, besser zu verstehen, wie Ihre Handelsaktivitäten zu den Absatzzahlen beitragen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Budgets an Aktivitäten anpassen, die den größten ROI erzielen.</p> |

### Zielgruppe {#web-audience}

<!--AA only-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--people"
>title="Zeigen Sie die Anzahl der Personen an, die mit Ihrer Marke interagieren."
>abstract="**Dies kann Ihnen helfen**, die Nutzungs-Trends auf Ihrer Site besser zu verstehen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität der letzten Marketing-Maßnahmen beim Generieren von neuen Besuchenden auf Ihrer Site messen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--bots"
>title="Zeigen Sie Seitenansichten und Trends in Bezug auf den Bottraffic auf Ihrer Site an."
>abstract="**Dies kann Ihnen helfen**, die Menge an Bottraffic besser zu verstehen, der aus Ihren Berichten gemäß den von Ihnen konfigurierten Bot-Regeln gefiltert wird.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Bot-Aktivität weiter überwachen, um neue Muster zu erkennen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--firstvsrepeatvisitors"
>title="Zeigen Sie einen Vergleich zwischen erstmaligen und wiederkehrenden Besuchenden an."
>abstract="**Dies kann Ihnen helfen**, die Effektivität Ihrer Site bei der Kundenbindung oder die Rate, mit der Sie neue Kundschaft gewinnen, besser zu verstehen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. erstmaligen Besuchenden Anreize für zukünftige Käufe anbieten, um sie zur Rückkehr zu bewegen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--personid"
>title="Zeigen Sie das individuelle Benutzerverhalten über verschiedene Kanäle hinweg an."
>abstract="**Dies kann Ihnen helfen**, die gesamte Customer Journey und alle Interaktionen Touchpoint-übergreifend besser zu verstehen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Marketing-Maßnahmen genauer auf Benutzervorlieben ausrichten."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--timeZoneRankedReport"
>title="Zeigen Sie die wichtigsten Zeitzonen der Besuchenden an, die auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, in welchen Zeitzonen Ihre Besuchenden leben.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Wartungsarbeiten an der Site so planen, dass sich diese auf möglichst wenige Personen auswirken."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--location"
>title="Zeigen Sie eine Übersicht der Besuchsstandorte in einer Kartenvisualisierung an."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wo sich die Personen, die Ihre Site besuchen, befinden. <br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Ressourcen auf die Standorte konzentrieren, wo Sie das größte Interesse und die meisten Chancen sehen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--domainRankedReport"
>title="Zeigen Sie die Top-Domains der Besuchenden an, die auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, von welchen Organisationen Ihre Besuchenden kommen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihren Inhalt auf Ihre größten Kundinnen und Kunden ausrichten."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--topLevelDomainRankedReport"
>title="Zeigen Sie die Top-Domains der Besuchenden an, die auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, von welchen Organisationen Ihre Besuchenden kommen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihren Inhalt auf Ihre größten Kundinnen und Kunden ausrichten."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--browserWidthRankedReport"
>title="Zeigen Sie die wichtigsten Browser-Breiten an, mit denen Personen auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie Inhalte Besuchenden angezeigt werden.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität durch Testen neuer Versionen Ihrer Site mit den gängigsten Browser-Breiten verbessern. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.<br/>Diese Vorlage verwendet die Dimension „Browser“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--browserHeightRankedReport"
>title="Zeigen Sie die wichtigsten Browser-Höhen an, mit denen Personen auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie Inhalte Besuchenden angezeigt werden.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität durch Testen neuer Versionen Ihrer Site mit den gängigsten Browser-Höhen verbessern. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.<br/>Diese Vorlage verwendet die Dimension „Browser“. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--operatingSystemRankedReport"
>title="Zeigen Sie den Namen der Betriebssysteme und die Version an, die Personen für den Zugriff auf Ihre Site verwenden."
>abstract="**Dies kann Ihnen helfen**, die gängigsten Betriebssysteme und Versionen, die beim Besuch verwendet werden, besser zu verstehen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität durch Testen neuer Versionen Ihrer Site mit den wichtigsten Betriebssystemen und deren wichtigsten Versionen verbessern. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--operatingSystemTypeRankedReport"
>title="Zeigen Sie die Namen der Betriebssysteme an, mit denen Personen auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen helfen**, die gängigsten Betriebssysteme, die beim Besuch verwendet werden, besser zu verstehen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität durch Testen neuer Versionen Ihrer Site mit den wichtigsten Betriebssystemen verbessern. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden."

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
>title="Zeigen Sie an, wie oft eine Besucherin bzw. ein Besucher die Site besucht hat."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie sehr Besuchende interagieren, wenn sie zu Ihrer Site zurückkehren. Das gilt für die Lebensdauer des Besuchenden, unabhängig vom Datumsbereich des Projekts.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Marketing-Aufwände für häufige Besuchende anpassen.<br/>Diese Vorlage verwendet die Dimension „Anzahl der Besuche“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--customerLoyaltyRankedReport"
>title="Zeigen Sie die Anzahl der Besuchenden auf Ihrer Site an, die 0 frühere Käufe, 1 früheren Kauf, 2 frühere Käufe oder mehr als 3 frühere Käufe getätigt haben."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie sich Ihre Site auf das Kaufverhalten auswirkt.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. sich auf Besuchende konzentrieren, die für einen Kauf zurückkehren, sodass Sie ein ähnliches Verhalten bei neuen Besuchenden fördern können.<br/>Diese Vorlage verwendet die Dimension „Kundentreue“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--daysBeforeFirstPurchaseRankedReport"
>title="Zeigen Sie die Anzahl der Tage an, die zwischen dem ersten Besuch einer neuen Kundin bzw. eines neuen Kunden auf Ihrer Site und dem ersten getätigten Kauf vergehen. Wenn ein Besucher beispielsweise einen Tag nach dem ersten Besuch einen Kauf tätigt, gehören alle nachfolgenden Besuche und Ereignisse zum Dimensionselement „1 Tag“."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie lange es dauert, bis Besuchende einen Kauf tätigen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Site aktualisieren, um schnellere Akquise zu fördern.<br/>Diese Vorlage verwendet die Dimension „Tage bis Erstkauf“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--daysSinceLastPurchaseRankedReport"
>title="Zeigen Sie die Zeitdauer an, die zwischen dem aktuellen Treffer der Besucherin bzw. des Besuchers und ihrem bzw. seinem letzten Kauf zu diesem Zeitpunkt verstrichen ist."
>abstract="**Dies kann Ihnen helfen**, das Besucherverhalten nach dem Kauf eines Artikels auf Ihrer Site besser zu verstehen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site aktualisieren, um Folgekäufe zu bewirken.<br/>Diese Vorlage verwendet die Dimension „Tage seit letztem Kauf“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobileScreenSizeRankedReport"
>title="Zeigen Sie die wichtigsten Bildschirmgrößen von Mobilgeräte an, mit denen Personen auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie Inhalte den Besuchenden angezeigt werden.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität durch Testen neuer Versionen Ihrer Site mit den gängigsten Bildschirmgrößen von Mobilgeräten verbessern. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobileScreenHeightRankedReport"
>title="Zeigen Sie die häufigsten Bildschirmhöhen von Mobilgeräten an, mit denen Personen auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie Inhalte den Besuchenden angezeigt werden.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität durch Testen neuer Versionen Ihrer Site mit den gängigsten Bildschirmhöhen von Mobilgeräte verbessern. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobileScreenWidthRankedReport"
>title="Zeigen Sie die häufigsten Bildschirmbreiten von Mobilgeräten an, mit denen Personen auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie Inhalte den Besuchenden angezeigt werden.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität durch Testen neuer Versionen Ihrer Site mit den gängigsten Bildschirmbreiten von Mobilgeräte verbessern. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden."

<!-- markdownlint-enable MD034 -->

<!--Both AA and CJA-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--countryGeoReport"
>title="Zeigen Sie das Land an, aus dem die Personen stammen, die Ihre Site besuchen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, aus welchen Ländern die meisten Personen stammen, die Ihre Site besuchen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Daten nutzen, um sich auf Marketing-Maßnahmen in diesen Ländern zu konzentrieren, oder sicherstellen, dass Ihr Site-Erlebnis in Ländern mit unterschiedlichen Hauptsprachen optimal ist.<br/>Diese Vorlage verwendet die Dimension „Länder“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--stateGeoReport"
>title="Zeigen Sie den Bundesstaat (in den USA) an, aus dem die Personen stammen, die Ihre Site besuchen. Diese Vorlage ähnelt der Vorlage für geografische Regionen, allerdings ist sie spezifisch für die USA."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, aus welchen US-Bundesstaaten die meisten Personen stammen, die Ihre Site besuchen. <br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Daten verwenden, um sich auf Marketing-Maßnahmen in diesen Bundesstaaten zu konzentrieren.<br/>Diese Vorlage verwendet die Dimension „USA“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--regionGeoReport"
>title="Zeigen Sie die geografische Region an, aus der die Personen stammen, die Ihre Site besuchen. Eine Region ist ein geografischer Bereich, der kleiner als ein Land, jedoch größer als eine Stadt ist. In einigen Ländern ist eine Region ein Bundesland, eine Provinz oder eine Präfektur. In anderen Gebieten handelt es sich um einen Landesteil, ein Departement oder eine großstädtische Region. "
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, aus welchen Regionen die meisten Personen stammen, die Ihre Site besuchen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Daten nutzen, um sich auf Marketing-Maßnahmen in diesen Regionen zu konzentrieren, oder sicherstellen, dass Ihr Site-Erlebnis in Regionen mit unterschiedlichen Hauptsprachen optimal ist. <br/>Diese Vorlage verwendet die Dimensionen „ID(variables/geocountry)“ und „Regionen“. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--cityGeoReport"
>title="Zeigen Sie die Stadt an, aus der die Personen stammen, die Ihre Site besuchen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, aus welchen Städten die meisten Personen stammen, die Ihre Site besuchen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Daten verwenden, um sich auf Marketing-Maßnahmen in diesen Städten zu konzentrieren. <br/>Diese Vorlage verwendet die Dimension „Städte“"

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--dmaGeoReport"
>title="Zeigen Sie die designierten Marketing-Gebiete (DMAs) in den USA an, aus denen die Personen stammen, die Ihre Site besuchen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, aus welchen Regionen die meisten Personen stammen, die Ihre Site besuchen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Daten verwenden, um sich auf Marketing-Maßnahmen in der erfolgreichsten Regionen zu konzentrieren. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--languageRankedReport"
>title="Zeigen Sie die häufigsten Sprachen an, in denen die Besuchenden den Inhalt anzeigen."
>abstract="**Dies kann Ihnen dabei helfen**, die am häufigsten bevorzugten Sprachen der Besuchenden besser zu verstehen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Lokalisierungs- oder Marketing-Maßnahmen auf die beliebtesten Sprachen konzentrieren.<br/>Diese Vorlage verwendet die Dimension „Sprache“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--web-technology-template"
>title="Zeigen Sie Informationen zu der Technologie an, mit der Personen auf Ihre Site zugreifen, z. B. zu Betriebssystemen, Browsern und Geräten."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, mit welchen Technologien am häufigsten auf Ihre Site zugegriffen wird.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Site für die verwendeten Technologien optimieren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--browserRankedReport"
>title="Zeigen Sie den Namen und die Version der wichtigsten Browser an, die für den Zugriff auf Ihre Site verwendet werden."
>abstract="**Dies kann Ihnen dabei helfen**, die gängigsten Browser, die beim Besuch verwendet werden, besser zu verstehen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität durch Testen neuer Versionen Ihrer Site mit den wichtigsten Browsern verbessern. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.<br/>Diese Vorlage verwendet die Dimension „Browser“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--browserTypeRankedReport"
>title="Zeigen Sie die Namen der Organisationen an, die die wichtigsten Browser erstellt haben, mit denen Personen auf Ihre Site zugreifen. Diese Vorlage unterscheidet sich insofern von der Vorlage „Browser“, als sie verschiedene Versionen desselben Browsers nicht als separate Dimensionselemente auflistet."
>abstract="**Dies kann Ihnen dabei helfen**, die gängigsten Browser, die Besuchende verwenden, besser zu verstehen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität verbessern, indem Sie neue Versionen Ihrer Site mit den wichtigsten Browsern testen. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden. <br/>Diese Vorlage verwendet die Dimension „Browsertyp“. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobileappscreens"
>title="Zeigen Sie die Anzahl der Ereignisse, Sitzungen und Personen anzeigen, die mit jedem Bildschirm in der App verknüpft sind."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Bildschirme auf Ihrer Site am beliebtesten sind.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Inhalte auf den beliebtesten Bildschirmen verbessern."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobileappactions"
>title="Zeigen Sie die Aktionen an, die Personen mit Ihrer Mobile App durchführen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie Personen Ihre App verwenden und welchen Nutzen sie daraus ziehen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Funktionen entwickeln, die die beliebtesten Features ergänzen oder verbessern."

<!-- markdownlint-enable MD034 -->

<!--CJA only-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobile-lifecycle-metrics-app-usage-template"
>title="Zeigen Sie die Anzahl der Benutzenden, Starts und ersten Starts der App sowie die durchschnittliche Sitzungslänge an."
>abstract="**Dies kann Ihnen helfen**, die Nutzungszeiten Ihrer App genauer zu überblicken. <br/>**Basierend auf Ihren Erkenntnissen können Sie** verschiedene Maßnahmen ergreifen, z. B. die App-Leistung verbessern, damit sie entsprechend der Nutzungsintensität skaliert werden kann."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobile-app-journeys"
>title="Zeigen Sie die meistverbreiteten Nutzungsmuster für Ihre Mobile App an."
>abstract="**Dies kann Ihnen helfen**, besser zu überblicken, wie Benutzende Ihre App verwenden. <br/>**Basierend auf Ihren Erkenntnissen können Sie** verschiedene Maßnahmen ergreifen, z. B. die Art und Weise verbessern, wie die Benutzenden von einem Bildschirm zum anderen gelangen, um die gängigsten Workflows zu optimieren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobile-app-key-metrics"
>title="Zeigen Sie einige der häufigsten Mobile App-Metriken an."
>abstract="**Dies kann Ihnen helfen**, die allgemeine Leistung Ihrer App besser zu verstehen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. den allgemeinen Zustand und die allgemeine Leistung Ihrer App bewerten."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobile-app-messaging"
>title="Zeigen Sie Leistungsdaten für In-App- und Push-Nachrichten für Ihre App an."
>abstract="**Dies kann Ihnen helfen**, besser zu überblicken, wie Benutzende In-App-Messaging-Funktionen verwenden und wie effektiv Push-Benachrichtigungen Traffic zu Ihrer App leiten.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. das Push-Benachrichtigungs-Erlebnis bei In-App-Nachrichten verbessern."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobile-app-performance-template"
>title="Zeigen Sie die Leistung Ihrer App an und finden Sie heraus, wo Probleme bei Benutzenden auftreten."
>abstract="**Dies kann Ihnen helfen**, zu überblicken, ob Benutzende Ihrer App eine langsame oder sonstwie beeinträchtigte Leistung erleben. <br/>**Basierend auf Ihren Erkenntnissen können Sie** verschiedene Maßnahmen ergreifen, z. B. vorhandene Probleme beheben oder die App-Leistung verbessern und so Problemen vorbeugen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobile-app-retention"
>title="Zeigen Sie an, welche Benutzenden Ihrer App die treuesten sind und was sie in der App tun."
>abstract="**Dies kann Ihnen helfen**, die Nutzungsweisen Ihrer App durch Ihre treuesten Benutzenden zu überblicken.<br/>**Basierend auf Ihren Erkenntnissen können Sie** verschiedene Maßnahmen ergreifen, z. B. intensivere Marketing-Maßnahmen für die Funktionen, die Ihre treusten Benutzenden verwenden."

<!-- markdownlint-enable MD034 -->

Die folgenden Vorlagen sind verfügbar:

| Vorlagenname | Warum diese Vorlage verwenden?<!-- What do you do with it? What can it help you learn? and What are the potential actions? --> |
| --- | --- | 
| [!UICONTROL **Metrik „Personen“**] | Zeigen Sie die Anzahl der Personen an, die mit Ihrer Marke interagieren. <p>**Dies kann Ihnen helfen**, die Nutzungs-Trends auf Ihrer Site besser zu verstehen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Effektivität der letzten Marketing-Maßnahmen beim Generieren von neuen Besuchenden auf Ihrer Site messen.</p> |
| **Besucherprofil** > **Standortübersicht** | Zeigen Sie eine Übersicht der Besuchsstandorte in einer Kartenvisualisierung an.<p>**Dies kann Ihnen helfen**, besser zu verstehen, wo sich die Personen befinden, die Ihre Site besuchen. </p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Ressourcen auf die Standorte konzentrieren, wo Sie das größte Interesse und die meisten Chancen sehen.</p><!-- This template uses the --> |
| **Besucherprofil** > **Geo-Segmentierung** > **Geo-Länder** | Zeigen Sie das Land an, aus dem die Personen stammen, die Ihre Site besuchen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, aus welchen Ländern die meisten Personen stammen, die Ihre Site besuchen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Daten nutzen, um sich auf Marketing-Maßnahmen in diesen Ländern zu konzentrieren, oder sicherstellen, dass Ihr Site-Erlebnis in Ländern mit unterschiedlichen Hauptsprachen optimal ist.</p><p>Diese Vorlage verwendet die Dimension „Länder“. </p> |
| **Besucherprofil** > **Geo-Segmentierung** > **Geo-Bundesstaaten der USA** | Zeigen Sie den Bundesstaat (in den USA) an, aus dem die Personen stammen, die Ihre Site besuchen. Diese Vorlage ähnelt der Vorlage für geografische Regionen, allerdings ist sie spezifisch für die USA.<p>**Dies kann Ihnen helfen**, besser zu verstehen, aus welchen US-Bundesstaaten die meisten Personen stammen, die Ihre Site besuchen. </p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Daten verwenden, um sich auf Marketing-Maßnahmen in diesen Bundesstaaten zu konzentrieren.</p><p>Diese Vorlage verwendet die Dimension „USA-Bundesstaaten“. </p> |
| **Besucherprofil** > **Geo-Segmentierung** > **Geo-Regionen** | Zeigen Sie die geografische Region an, aus der die Personen stammen, die Ihre Site besuchen. Eine Region ist ein geografischer Bereich, der kleiner als ein Land, jedoch größer als eine Stadt ist. In einigen Ländern ist eine Region ein Bundesland, eine Provinz oder eine Präfektur. In anderen Gebieten handelt es sich um einen Landesteil, ein Departement oder eine großstädtische Region. <p>**Dies kann Ihnen helfen**, besser zu verstehen, aus welchen Regionen die meisten Personen stammen, die Ihre Site besuchen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Daten nutzen, um sich auf Marketing-Maßnahmen in diesen Regionen zu konzentrieren, oder sicherstellen, dass Ihr Site-Erlebnis in Regionen mit unterschiedlichen Hauptsprachen optimal ist. </p><p>Diese Vorlage verwendet die Dimensionen „ID(variables/geocountry)“ und „Regionen“. </p> |
| **Besucherprofil** > **Geo-Segmentierung** > **Geo-Städte** | Zeigen Sie die Stadt an, aus der die Personen stammen, die Ihre Site besuchen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, aus welchen Städten die meisten Personen stammen, die Ihre Site besuchen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Daten verwenden, um sich auf Marketing-Maßnahmen in diesen Städten zu konzentrieren. </p><p>Diese Vorlage verwendet die Dimension „Städte“ </p> |
| **Besucherprofil** > **Geo-Segmentierung** > **DMA zu Geo-USA** | Zeigen Sie die designierten Marketing-Gebiete (DMAs) in den USA an, aus denen die Personen stammen, die Ihre Site besuchen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, aus welchen Regionen die meisten Personen stammen, die Ihre Site besuchen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Daten verwenden, um sich auf Marketing-Maßnahmen in der erfolgreichsten Regionen zu konzentrieren. </p><!-- This template uses the --> |
| **Besucherprofil** > **Sprachen** | Zeigen Sie die häufigsten Sprachen an, in denen die Besuchenden den Inhalt anzeigen. <p>**Dies kann Ihnen dabei helfen**, die am häufigsten bevorzugten Sprachen der Besuchenden besser zu verstehen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Lokalisierungs- oder Marketing-Maßnahmen auf die beliebtesten Sprachen konzentrieren.</p><p>Diese Vorlage verwendet die Dimension „Sprache“.</p> |
| **Besucherprofil** > **Zeitzonen** | Zeigen Sie die wichtigsten Zeitzonen der Besuchenden an, die auf Ihre Site zugreifen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, in welchen Zeitzonen Ihre Besuchenden leben.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Wartungsarbeiten an der Site so planen, dass sich diese auf möglichst wenige Personen auswirken.</p> |
| **Besucherprofil** > **Domains** | Zeigen Sie die Top-Domains der Besuchenden an, die auf Ihre Site zugreifen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, von welchen Organisationen Ihre Besuchenden kommen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihren Inhalt auf Ihre größten Kundinnen und Kunden ausrichten.</p> |
| **Besucherprofil** > **Top-Level-Domains** | Zeigen Sie die Top-Level-Domains der Besuchenden an, die auf Ihre Site zugreifen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, von welchen Organisationen Ihre Besuchenden kommen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihren Inhalt auf Ihre größten Kundinnen und Kunden ausrichten.</p> |
| **Besucherprofil** > **Technologie** > **Technologieübersicht** | Zeigen Sie Informationen zu der Technologie an, mit der Personen auf Ihre Site zugreifen, z. B. zu Betriebssystemen, Browsern und Geräten. <p>**Dies kann Ihnen helfen**, besser zu verstehen, mit welchen Technologien am häufigsten auf Ihre Site zugegriffen wird.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Site für die verwendeten Technologien optimieren.</p> |
| **Besucherprofil** > **Technologie** > **Browser** | Zeigen Sie den Namen und die Version der wichtigsten Browser an, die für den Zugriff auf Ihre Site verwendet werden.<p>**Dies kann Ihnen dabei helfen**, die gängigsten Browser, die beim Besuch verwendet werden, besser zu verstehen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität durch Testen neuer Versionen Ihrer Site mit den wichtigsten Browsern verbessern. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.</p><p>Diese Vorlage verwendet die Dimension „Browser“. </p> |
| **Besucherprofil** > **Technologie** > **Browser-Typen** | Zeigen Sie die Namen der Organisationen an, die die wichtigsten Browser erstellt haben, mit denen Personen auf Ihre Site zugreifen. Diese Vorlage unterscheidet sich insofern von der Vorlage „Browser“, als sie verschiedene Versionen desselben Browsers nicht als separate Dimensionselemente auflistet.<p>**Dies kann Ihnen dabei helfen**, die gängigsten Browser, die von Besuchenden verwendet werden, besser zu verstehen</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität durch Testen neuer Versionen Ihrer Site mit den wichtigsten Browsern verbessern. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden. </p><p>Diese Vorlage verwendet die Dimension „Browser-Typ“. </p> |
| **Besucherprofil** > **Technologie** > **Browser-Breite** | Zeigen Sie die wichtigsten Browser-Breiten an, mit denen Personen auf Ihre Site zugreifen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, wie Inhalte Besuchenden angezeigt werden.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität durch Testen neuer Versionen Ihrer Site mit den gängigsten Browser-Breiten verbessern. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.</p><p>Diese Vorlage verwendet die Dimension „Browser“. </p> |
| **Besucherprofil** > **Technologie** > **Browser-Höhe** | Zeigen Sie die wichtigsten Browser-Höhen an, mit denen Personen auf Ihre Site zugreifen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, wie Inhalte Besuchenden angezeigt werden.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität durch Testen neuer Versionen Ihrer Site mit den gängigsten Browser-Höhen verbessern. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.</p><p>Diese Vorlage verwendet die Dimension „Browser“. </p> |
| **Besucherprofil** > **Technologie** > **Betriebssystem** | Zeigen Sie den Namen der Betriebssysteme und die Version an, die Personen für den Zugriff auf Ihre Site verwenden.<p>**Dies kann Ihnen helfen**, die gängigsten Betriebssysteme und Versionen, die beim Besuch verwendet werden, besser zu verstehen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität durch Testen neuer Versionen Ihrer Site mit den wichtigsten Betriebssystemen und deren wichtigsten Versionen verbessern. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.</p> |
| **Besucherprofil** > **Technologie** > **Betriebssystemtypen** | Zeigen Sie die Namen der Betriebssysteme an, mit denen Personen auf Ihre Site zugreifen.<p>**Dies kann Ihnen helfen**, die gängigsten Betriebssysteme, die beim Besuch verwendet werden, besser zu verstehen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität durch Testen neuer Versionen Ihrer Site mit den wichtigsten Betriebssystemen verbessern. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.</p> |
| **Besucherprofil** > **Technologie** > [!UICONTROL **Mobilnetzbetreiber**] | Zeigen Sie das Telekommunikationsunternehmen an, das Mobilfunkverbindungen mit den Mobilgeräten bereitstellt, mit denen Benutzende auf Ihre Site zugreifen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Mobilnetzbetreiber bei Ihrer Benutzerbasis am beliebtesten sind.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Inhaltsbereitstellung auf Grundlage der Netzwerkfunktionen verschiedener Betreiber anpassen, um ein reibungsloses Anwendererlebnis zu gewährleisten.</p><p>Diese Vorlage verwendet die Dimension „Mobilnetzbetreiber“.</p> |
| **Besuchertreue** > **Rückkehrhäufigkeit** | Zeigen Sie das Telekommunikationsunternehmen an, das Mobilfunkverbindungen mit den Mobilgeräten bereitstellt, mit denen Benutzende auf Ihre Site zugreifen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Mobilnetzbetreiber bei Ihrer Benutzerbasis am beliebtesten sind.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Inhaltsbereitstellung auf Grundlage der Netzwerkfunktionen verschiedener Betreiber anpassen, um ein reibungsloses Anwendererlebnis zu gewährleisten.</p><p>Diese Vorlage verwendet die Dimension „Mobilnetzbetreiber“.</p> |
| **Besucherbindung** > **Rückkehrende Besuchende** | Zeigen Sie das Telekommunikationsunternehmen an, das Mobilfunkverbindungen mit den Mobilgeräten bereitstellt, mit denen Benutzende auf Ihre Site zugreifen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Mobilnetzbetreiber bei Ihrer Benutzerbasis am beliebtesten sind.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Inhaltsbereitstellung auf Grundlage der Netzwerkfunktionen verschiedener Betreiber anpassen, um ein reibungsloses Anwendererlebnis zu gewährleisten.</p><p>Diese Vorlage verwendet die Dimension „Mobilnetzbetreiber“.</p> |
| **Besucherbindung** > **Besuchszahlen** | Zeigen Sie an, wie oft eine Besucherin bzw. ein Besucher die Site besucht hat.<p>**Dies kann Ihnen helfen**, besser zu verstehen, wie sehr Besuchende interagieren, wenn sie zu Ihrer Site zurückkehren. Das gilt für die Lebensdauer des Besuchenden, unabhängig vom Datumsbereich des Projekts.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Marketing-Aufwände für häufige Besuchende anpassen.</p><p>Diese Vorlage verwendet die Dimension „Besuchszahlen“.</p> |
| **Besucherbindung** > **Verkaufszyklus** > **Kundentreue** | Zeigen Sie die Anzahl der Besuchenden auf Ihrer Site an, die 0 frühere Käufe, 1 früheren Kauf, 2 frühere Käufe oder mehr als 3 frühere Käufe getätigt haben. <p>**Dies kann Ihnen helfen**, besser zu verstehen, wie sich Ihre Site auf das Kaufverhalten auswirkt.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. sich auf Besuchende konzentrieren, die für einen Kauf zurückkehren, sodass Sie ein ähnliches Verhalten bei neuen Besuchenden fördern können.</p><p>Diese Vorlage verwendet die Dimension „Kundentreue“.</p> |
| **Besucherbindung** > **Verkaufszyklus** > **Tage bis Erstkauf** | Zeigen Sie die Anzahl der Tage an, die zwischen dem ersten Besuch einer neuen Kundin bzw. eines neuen Kunden auf Ihrer Site und dem ersten getätigten Kauf vergehen. mandWenn ein Besucher beispielsweise einen Tag nach dem ersten Besuch einen Kauf tätigt, gehören alle nachfolgenden Besuche und Ereignisse zum Dimensionselement „1 Tag“.<p>**Dies kann Ihnen helfen**, besser zu verstehen, wie lange es dauert, bis Besuchende einen Kauf tätigen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Site aktualisieren, um schnellere Akquise zu fördern.</p><p>Diese Vorlage verwendet die Dimension „Tage bis Erstkauf“.</p> |
| **Besuchertreue** > **Verkaufszyklus** > **Tage seit letztem Kauf** | Zeigen Sie die Zeitdauer an, die zwischen dem aktuellen Treffer der Besucherin bzw. des Besuchers und ihrem bzw. seinem letzten Kauf zu diesem Zeitpunkt verstrichen ist.<p>**Dies kann Ihnen helfen**, das Besucherverhalten nach dem Kauf eines Artikels auf Ihrer Site besser zu verstehen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site aktualisieren, um Folgekäufe zu bewirken.</p><p>Diese Vorlage verwendet die Dimension „Tage seit letztem Kauf“.</p> |
| **Mobile** > **Geräte** | Zeigen Sie die Marke und das Modell von Mobilgeräten an, mit denen Benutzende auf Ihre Site zugreifen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Mobilgeräte bei Ihrer Benutzerbasis am beliebtesten sind.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. das Rendering Ihrer Site für die gängigsten Mobilgeräte optimieren.</p><p>Diese Vorlage verwendet die Dimension „Mobilgerätename“.</p> |
| **Mobile** > **Gerätetyp** | Zeigen Sie die Mobilgerätetypen an, mit denen Benutzende auf Ihre Site zugreifen, z. B. Smartphones oder Tablets.<p>**Dies kann Ihnen dabei helfen**, die verschiedenen Arten von Mobilgeräten besser zu verstehen, die für den Zugriff auf Ihre Site verwendet werden.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Site für die Mobilgerätetypen optimieren, die am häufigsten verwendet werden.</p><p>Diese Vorlage verwendet die Dimension „Mobilgerätetyp“.</p> |
| **Mobile** > **Hersteller** | Zeigen Sie an, welche Hersteller die Mobilgeräte herstellen, mit denen Benutzende auf Ihre Site zugreifen, z. B. Apple und Samsung.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Hersteller bei Ihrer Benutzerbasis am beliebtesten sind.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Inhaltsbereitstellung auf Grundlage der Fähigkeiten verschiedener Hersteller anpassen, um ein reibungsloses Anwendererlebnis zu gewährleisten.</p><p>Diese Vorlage verwendet die Dimension „Mobilgerätehersteller“.</p> |
| **Mobile** > **Bildschirmgröße** | Zeigen Sie die wichtigsten Bildschirmgrößen von Mobilgeräte an, mit denen Personen auf Ihre Site zugreifen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, wie Inhalte den Besuchenden angezeigt werden.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität durch Testen neuer Versionen Ihrer Site mit den gängigsten Bildschirmgrößen von Mobilgeräten verbessern. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.</p> |
| **Mobile** > **Bildschirmhöhe** | Zeigen Sie die häufigsten Bildschirmhöhen von Mobilgeräten an, mit denen Personen auf Ihre Site zugreifen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, wie Inhalte den Besuchenden angezeigt werden.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität durch Testen neuer Versionen Ihrer Site mit den gängigsten Bildschirmhöhen von Mobilgeräte verbessern. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.</p> |
| **Mobile** > **Bildschirmbreite** | Zeigen Sie die häufigsten Bildschirmbreiten von Mobilgeräten an, mit denen Personen auf Ihre Site zugreifen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, wie Inhalte den Besuchenden angezeigt werden.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Site-Qualität durch Testen neuer Versionen Ihrer Site mit den gängigsten Bildschirmbreiten von Mobilgeräte verbessern. Auf diese Weise können die Maßnahmen zur Qualitätssicherung maximiert werden.</p> |
| **Mobile** > **Mobile-App-Nutzung** | Zeigen Sie die Anzahl der Benutzenden, Starts und ersten Starts der App sowie die durchschnittliche Sitzungslänge an.<p>**Dies kann Ihnen helfen**, die Nutzungszeiten Ihrer App genauer zu überblicken. </p><p>**Basierend auf Ihren Erkenntnissen können Sie** verschiedene Maßnahmen ergreifen, z. B. die App-Leistung verbessern, damit sie entsprechend der Nutzungsintensität skaliert werden kann.</p><!-- This template uses the --> |
| **Mobile** > **Mobile App – Journeys** | Zeigen Sie die meistverbreiteten Nutzungsmuster für Ihre Mobile App an. <p>**Dies kann Ihnen helfen**, besser zu überblicken, wie Benutzende Ihre App verwenden.  </p><p>**Basierend auf Ihren Erkenntnissen können Sie** verschiedene Maßnahmen ergreifen, z. B. die Art und Weise verbessern, wie die Benutzenden von einem Bildschirm zum anderen gelangen, um die gängigsten Workflows zu optimieren. </p><!-- This template uses the --> |
| **Mobile** > **Mobile-App-Metriken** | Zeigen Sie einige der häufigsten Mobile-App-Metriken an. <p>**Dies kann Ihnen helfen**, die allgemeine Leistung Ihrer App besser zu verstehen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. den allgemeinen Zustand und die allgemeine Leistung Ihrer App bewerten.</p><!-- This template uses the --> |
| **Mobile** > **Mobile-App-Messaging** | Zeigen Sie Leistungsdaten für In-App- und Push-Nachrichten für Ihre App an.<p>**Dies kann Ihnen helfen**, besser zu überblicken, wie Benutzende In-App-Messaging-Funktionen verwenden und wie effektiv Push-Benachrichtigungen Traffic zu Ihrer App leiten.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. das Push-Benachrichtigungs-Erlebnis bei In-App-Nachrichten verbessern.</p><!-- This template uses the --> |
| **Mobile** > **Mobile-App-Leistung** | Zeigen Sie die Leistung Ihrer App an und finden Sie heraus, wo Probleme bei Benutzenden auftreten. <p>**Dies kann Ihnen helfen**, zu überblicken, ob Benutzende Ihrer App eine langsame oder sonstwie beeinträchtigte Leistung erleben.  </p><p>**Basierend auf Ihren Erkenntnissen können Sie** verschiedene Maßnahmen ergreifen, z. B. vorhandene Probleme beheben oder die App-Leistung verbessern und so Problemen vorbeugen.</p><!-- This template uses the --> |
| **Mobile** > **Mobile-App-Bindung** | Zeigen Sie an, welche Benutzenden Ihrer App die treuesten sind und was sie in der App tun. <p>**Dies kann Ihnen helfen**, die Nutzungsweisen Ihrer App durch Ihre treuesten Benutzenden zu überblicken.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** verschiedene Maßnahmen ergreifen, z. B. intensivere Marketing-Maßnahmen für die Funktionen, die Ihre treusten Benutzenden verwenden.</p><!-- This template uses the --> |
| **Bots** | Zeigen Sie Seitenansichten und Trends in Bezug auf den Bottraffic auf Ihrer Site an. <p>**Dies kann Ihnen helfen**, die Menge an Bottraffic besser zu verstehen, der aus Ihren Berichten gemäß den von Ihnen konfigurierten Bot-Regeln gefiltert wird.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Bot-Aktivität weiter überwachen, um neue Muster zu erkennen.</p><!-- This template uses the --> |

### Akquise {#web-acquisition}

<!--AA only-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--mobile-app-acquisition-template"
>title="Zeigen Sie an, wie Ihre Website Besuchende auf Mobilgeräten erhält."
>abstract="**Dies kann Ihnen helfen**, die verschiedenen Faktoren besser zu verstehen, die zur Akquise führen, wie Suchbegriffe, verweisende Domain usw.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf die effektivsten Kanäle konzentrieren.<br/>Diese Vorlage verwendet die Metrik „Bounce-Rate“ und die Metrik „Bounces“. Außerdem werden die Dimension „Suchmaschine“, die Dimension „Suchbegriff“, die Dimension „Einstiegsseite“, die Dimension „Verweisende Domäne“, die Dimension „Trackingcode“ und die Dimension „Verweisende Stelle“ verwendet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--advertisingAnalyticsPaidSearch"
>title="Zeigen Sie alle Paid-Search-Daten von Google Ads und Microsoft Advertising nebeneinander an."
>abstract="**Dies kann Ihnen helfen**, den Umfang des an Ihre Site gesendeten Traffics besser zu verstehen und ob Kundinnen und Kunden konvertieren.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Kostenwirksamkeit einer Anzeigenkampagne schätzen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa-template--searchEngineRankRankedReport"
>title="Zeigen Sie an, durch welche Seiten der Suchergebnisse sich Besuchende geklickt haben, um Ihre Site zu erreichen. Wenn Ihre Site beispielsweise auf der zweiten Seite der Suchergebnisse einer Suchmaschine erscheint, ist das Dimensionselement für diese Variable „Suchseite 2“."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, an welcher Stelle der Suchergebnisse Ihre Seiten angezeigt werden.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre SEO-Strategie verbessern, um sicherzustellen, dass Ihr Inhalt auf der ersten Seite der Suchergebnisse angezeigt wird."

<!-- markdownlint-enable MD034 -->

<!--Both AA and CJA-->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--marketing-channel-overview-template"
>title="Bei Verwendung der benutzerdefinierten Attribution zeigt diese Vorlage, wie Besuchende auf Ihre Site gelangen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Ihrer Marketing-Kanäle am effektivsten sind.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. intensiver in effektive Marketing-Kanäle investieren und weniger effektive Marketing-Kanäle aufgeben.<br/>Diese Vorlage verwendet die Dimension „ID(variables/marketingchannel)“ und die Metrik „Umsatz“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--firstouchChannelRankedReport"
>title="Zeigen Sie die ersten Marketing-Kanäle an, zu denen Besuchende während ihres Interaktionszeitraums (standardmäßig 30 Tage) passen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Marketing-Kanäle den anfänglichen Traffic zu Ihrer Site leiten.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf Bereiche konzentrieren, die am effektivsten sind.<br/>Diese Vorlage verwendet die Dimension „Erstkontaktkanal“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--firstouchChannelDetailRankedReport"
>title="Zeigen Sie Details zu den ersten Marketing-Kanälen an, zu denen Besuchende während ihres Interaktionszeitraums (standardmäßig 30 Tage) passen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, was dazu beigetragen hat, dass der Treffer zu einem Marketing-Kanal passte. Wenn beispielsweise eine Besucherin oder ein Besucher zu Ihrer Site gelangt ist und mit dem Marketing-Kanal „Paid Search“ übereinstimmt, können Sie anhand des Kanaldetails sehen, welche Suchmaschine verwendet wurde oder nach welchem Keyword die Person gesucht hat.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf Bereiche konzentrieren, die am effektivsten sind.<br/>Diese Vorlage verwendet die Dimension „Detail des Erstkontaktkanals“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--campaignConversionReport"
>title="Zeigen Sie die Anzahl der Clickthroughs und Checkouts für Ihre Kampagnen an."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, wie Marketing-Kampagnen die Konversion fördern.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. ermitteln, welche Marketing-Kampagnen den größten ROI erzielen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--retail-campaign-performance-template"
>title="Zeigen Sie Details zur Leistung Ihrer Marketing-Kampagnen an."
>abstract="**Dies kann Ihnen helfen**, mehr über die verschiedenen Erfolgsindikatoren zu erfahren, die mit Kampagnen verbunden sind, wie Umsatz, Produktansichten, Bestellungen usw.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf die Kampagnen konzentrieren, die den meisten Umsatz bringen. <br/>Diese Vorlage verwendet die Metrik „Umsatz“, die Metrik „Produktansichten“, die Metrik „Zusatz zum Warenkorb“, die Metrik „Bestellungen“ und die Metrik „Einheiten“. Außerdem werden die Dimension „Trackingcode“ und die Dimension „Referrer Domain“ verwendet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--web-acquisition-template"
>title="Sehen Sie sich an, wie Ihre Website Besuchende erhält."
>abstract="**Dies kann Ihnen helfen**, die verschiedenen Faktoren besser zu verstehen, die zur Akquise führen, wie Suchbegriffe, verweisende Domain usw.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf die effektivsten Kanäle konzentrieren.<br/>Diese Vorlage verwendet die Metrik „Bounce-Rate“ und die Metrik „Bounces“. Außerdem werden die Dimension „Suchmaschine“, die Dimension „Suchbegriff“, die Dimension „Einstiegsseite“, die Dimension „Verweisende Domäne“, die Dimension „Trackingcode“ und die Dimension „Verweisende Stelle“ verwendet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--searchKeywordRankedReport"
>title="Zeigen Sie die Suchbegriffe an, die Besuchende zum Erreichen Ihrer Site verwenden, unabhängig davon, ob es sich um gebührenpflichtige oder organische Suchbegriffe handelt."
>abstract="**Dies kann Ihnen helfen**, die Keywords besser zu verstehen, die bei Suchvorgängen verwendet werden, die zu Sitetraffic führen. <br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. SEO-Lücken zwischen den verwendeten Keywords und den Keywords, die den Sitetraffic fördern, identifizieren und schließen.<br/>Diese Vorlage verwendet die Dimension „Suchbegriff“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--searchPaidKeywordRankedReport"
>title="Zeigen Sie die Suchbegriffe an, die Besuchende zum Erreichen Ihrer Site verwenden und die mit der Paid-Search-Erkennung übereinstimmen."
>abstract="**Dies kann Ihnen helfen**, die Keywords besser zu verstehen, die bei den Suchvorgängen verwendet werden, die zu Sitetraffic führen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. SEO-Lücken zwischen den verwendeten Keywords und den Keywords, die den Sitetraffic fördern, identifizieren und schließen. <br/>Diese Vorlage verwendet die Dimension „Suchbegriff – Paid“. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--searchNaturalKeywordRankedReport"
>title="Zeigen Sie die Suchbegriffe an, die Besuchende zum Erreichen Ihrer Site verwenden und die nicht mit der Paid-Search-Erkennung übereinstimmen."
>abstract="**Dies kann Ihnen helfen**, die Keywords besser zu verstehen, die bei Suchvorgängen verwendet werden, welche zu Sitetraffic führen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. SEO-Lücken zwischen den verwendeten Keywords und den Keywords, die den Sitetraffic fördern, identifizieren und schließen.<br/>Diese Vorlage verwendet die Dimension „Suchbegriff – Organisch“. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--searchRankedReport"
>title="Zeigen Sie die Suchmaschinen an, die Besuchende zum Erreichen Ihrer Site verwenden, unabhängig davon, ob es sich um gebührenpflichtige oder organische Suchbegriffe handelt."
>abstract="**Dies kann Ihnen helfen**, die Suchmaschinen besser zu verstehen, die bei Suchvorgängen verwendet werden, die zu Sitetraffic führen. <br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre SEO-Bemühungen auf die Suchmaschinen konzentrieren, die den meisten Traffic zur Site leiten.<br/>Diese Vorlage verwendet die Dimension „Suchmaschine“. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--searchPaidRankedReport"
>title="Zeigen Sie die Suchmaschinen an, die Besuchende zum Erreichen Ihrer Site verwenden und die mit der Paid-Search-Erkennung übereinstimmen."
>abstract="**Dies kann Ihnen helfen**, die Suchmaschinen besser zu verstehen, die bei Suchvorgängen verwendet werden, die zu Sitetraffic führen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre SEO-Bemühungen auf die Suchmaschinen konzentrieren, die den meisten Traffic zur Site leiten. <br/>Diese Vorlage verwendet die Dimension „Suchmaschine – Paid“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--searchNaturalRankedReport"
>title="Zeigen Sie die Suchbegriffe an, die Besuchende zum Erreichen Ihrer Site verwenden und die nicht mit der Paid-Search-Erkennung übereinstimmen."
>abstract="**Dies kann Ihnen helfen**, die Suchmaschinen besser zu verstehen, die bei Suchvorgängen verwendet werden, die zu Sitetraffic führen.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre SEO-Bemühungen auf die Suchmaschinen konzentrieren, die den meisten Traffic zur Site leiten.<br/>Diese Vorlage verwendet die Dimension „Suchmaschine – Organisch“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--referringDomainRankedReport"
>title="Zeigen Sie an, durch welche Domains Besuchende sich klicken, um Ihre Site zu erreichen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Sites von Drittanbietern den meisten Traffic zu Ihrer Site leiten. (Auf der externen Site muss ein Link vorhanden sein und Besuchende müssen darauf klicken, damit das Dimensionselement angezeigt wird.)<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Inhalte erstellen oder anpassen, um sie genauer auf die Interessen der Besuchenden von Top-Referrer-Domains auszurichten. <br/>Diese Vorlage verwendet die Dimension „Verweisende Domain“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--referringDomainOriginalRankedReport"
>title="Zeigen Sie die erste verweisende Domain an, durch die sich Personen zum Erreichen Ihrer Site geklickt haben. (Sobald sie festgelegt wurde, enthält sie denselben Wert für die gesamte Lebensdauer dieser Besucher-ID.)"
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Drittanbieter-Sites den Traffic ursprünglich zu Ihrer Site leiten.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Inhalte erstellen oder anpassen, um sie besser an die Interessen der Besuchenden von den ursprünglichen verweisenden Top-Domains anzupassen. <br/>Diese Vorlage verwendet die Dimension „Ursprünglich verweisende Domain“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--referrerRankedReport"
>title="Zeigen Sie an, auf welchen URLs sich die Besuchenden befanden, als sie sich zu Ihrer Site durchklickten. (In der externen URL muss ein Link vorhanden sein und Besuchende müssen darauf klicken, damit das Dimensionselement angezeigt wird.)"
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche spezifischen URLs den meisten Traffic zu Ihrer Site leiten.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Inhalte erstellen oder anpassen, um sie besser an die Interessen der Besuchenden von den Top-URLs anzupassen. <br/>Diese Vorlage verwendet die Dimension „Verweisende Domain“.</p>"

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--referrerTypeRankedReport"
>title="Zeigen Sie an, durch welche generischen Kanäle Besuchende sich geklickt haben, um zu Ihrer Site zu gelangen. Adobe verwaltet die Regeln für jeden Kanal. Mögliche Kanäle sind Suchmaschinen, soziale Netzwerke, andere Websites, die Festplatte oder E-Mails."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Referrer-Typen den meisten Traffic zu Ihrer Site leiten.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Inhalte erstellen oder anpassen, um sie besser an die Interessen der Besuchenden von einem bestimmten Kanal anzupassen.<br/>Diese Vorlage verwendet die Dimension „Referrer-Typ“."

<!-- markdownlint-enable MD034 -->

Die folgenden Vorlagen sind verfügbar:

| Vorlagenname | Warum diese Vorlage verwenden?<!-- What do you do with it? What can it help you learn? and What are the potential actions? --> |
| --- | --- | 
| [!UICONTROL **Marketing-Kanäle**] > [!UICONTROL **Kanalübersichtsbericht**] | Bei Verwendung der benutzerdefinierten Attribution zeigt diese Vorlage, wie Besuchende auf Ihre Site gelangen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Ihrer Marketing-Kanäle am effektivsten sind.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. intensiver in effektive Marketing-Kanäle investieren und weniger effektive Marketing-Kanäle aufgeben.</p><p>Diese Vorlage verwendet die Dimension „ID(variables/marketingchannel)“ und die Metrik „Umsatz“.</p> |
| [!UICONTROL **Marketing-Kanäle**] > [!UICONTROL **Erstkontaktkanal**] | Zeigen Sie die ersten Marketing-Kanäle an, zu denen Besuchende während ihres Interaktionszeitraums (standardmäßig 30 Tage) passen. <p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Marketing-Kanäle den anfänglichen Traffic zu Ihrer Site leiten.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf Bereiche konzentrieren, die am effektivsten sind.</p><p>Diese Vorlage verwendet die Dimension „Erstkontaktkanal“.</p> |
| [!UICONTROL **Marketing-Kanäle**] > [!UICONTROL **Detail des Erstkontaktkanals**] | Zeigen Sie Details zu den ersten Marketing-Kanälen an, zu denen Besuchende während ihres Interaktionszeitraums (standardmäßig 30 Tage) passen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, was dazu beigetragen hat, dass der Treffer zu einem Marketing-Kanal passte. Wenn beispielsweise eine Besucherin oder ein Besucher zu Ihrer Site gelangt ist und mit dem Marketing-Kanal „Paid Search“ übereinstimmt, können Sie anhand des Kanaldetails sehen, welche Suchmaschine verwendet wurde oder nach welchem Keyword die Person gesucht hat.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf Bereiche konzentrieren, die am effektivsten sind.</p><p>Diese Vorlage verwendet die Dimension „Detail des Erstkontaktkanals“.</p> |
| [!UICONTROL **Marketing-Kanäle**] > [!UICONTROL **Letztkontaktkanal**] | Zeigen Sie den letzten Marketing-Kanal an, der einer Person während ihres Interaktionszeitraums (standardmäßig 30 Tage) entspricht.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Marketing-Kanäle zu Ihrer Site Traffic leiten, der zu Konversionen führt.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf Bereiche konzentrieren, die am effektivsten sind.</p><p>Diese Vorlage verwendet die Dimension „Letztkontaktkanal“.  </p> |
| [!UICONTROL **Marketing-Kanäle**] > [!UICONTROL **Detail des Letztkontaktkanals**] | Zeigen Sie Details zum letzten Marketing-Kanal an, der einer Person während ihres Interaktionszeitraums (standardmäßig 30 Tage) entspricht.<p>**Dies kann Ihnen helfen**, besser zu verstehen, was dazu beigetragen hat, dass der Treffer zu einem Marketing-Kanal passte. Wenn beispielsweise eine Besucherin oder ein Besucher zu Ihrer Site gelangt ist und mit dem Marketing-Kanal „Paid Search“ übereinstimmt, können Sie anhand des Kanaldetails sehen, welche Suchmaschine verwendet wurde oder nach welchem Keyword die Person gesucht hat.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf Bereiche konzentrieren, die am effektivsten sind. </p><p>Diese Vorlage verwendet die Dimension „Detail des Letztkontaktkanals“. </p> |
| [!UICONTROL **Kampagnen**] > [!UICONTROL **Kampagnen-Konversionstrichter**] | Zeigen Sie die Anzahl der Clickthroughs und Checkouts für Ihre Kampagnen an. <p>**Dies kann Ihnen helfen**, besser zu verstehen, wie Marketing-Kampagnen die Konversion fördern.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. ermitteln, welche Marketing-Kampagnen den größten ROI erzielen.</p> |
| [!UICONTROL **Kampagnen**] > [!UICONTROL **Kampagnenleistung**] | Zeigen Sie Details zur Leistung Ihrer Marketing-Kampagnen an.<p>**Dies kann Ihnen helfen**, mehr über die verschiedenen Erfolgsindikatoren zu erfahren, die mit Kampagnen verbunden sind, wie Umsatz, Produktansichten, Bestellungen usw.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf die Kampagnen konzentrieren, die den meisten Umsatz bringen. </p><p>Diese Vorlage verwendet die Metrik „Umsatz“, die Metrik „Produktansichten“, die Metrik „Zusatz zum Warenkorb“, die Metrik „Bestellungen“ und die Metrik „Einheiten“. Außerdem werden die Dimension „Trackingcode“ und die Dimension „Referrer Domain“ verwendet. </p> |
| [!UICONTROL **Kampagnen**] > [!UICONTROL **Trackingcode**] | Zeigen Sie die Namen der Trackingcodes auf Ihrer Site an. Sie können Links mit verschiedenen Abfragezeichenfolgenparameterwerten an verschiedenen Stellen im Internet platzieren.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Links am erfolgreichsten dazu beigetragen haben, den Traffic auf Ihre Site zu lenken. Das Anhängen von Trackingcode-Abfragezeichenfolgen erfolgt häufig in E-Mails, Anzeigen, Social Media-Posts und anderen Marketing-Maßnahmen Ihrer Organisation</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf die Kampagnen konzentrieren, die den meisten Umsatz bringen. </p><p>Diese Vorlage verwendet die Dimension „Trackingcode“. </p> |
| **Web-Akquise** | Sehen Sie sich an, wie Ihre Website Besuchende erhält.<p>**Dies kann Ihnen helfen**, die verschiedenen Faktoren besser zu verstehen, die zur Akquise führen, wie Suchbegriffe, verweisende Domain usw.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf die effektivsten Kanäle konzentrieren.</p><p>Diese Vorlage verwendet die Absprungratenmetrik und die Metrik „Bounces“. Außerdem werden die Dimension „Suchmaschine“, die Dimension „Suchbegriff“, die Dimension „Einstiegsseite“, die Dimension „Verweisende Domäne“, die Dimension „Trackingcode“ und die Dimension „Verweisende Stelle“ verwendet.  </p> |
| **Mobile-Akquise** | Zeigen Sie an, wie Ihre Site Besuchende auf Mobilgeräten erhält.<p>**Dies kann Ihnen helfen**, die verschiedenen Faktoren besser zu verstehen, die zur Akquise führen, wie Suchbegriffe, verweisende Domain usw.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Marketing-Maßnahmen auf die effektivsten Kanäle konzentrieren.</p><p>Diese Vorlage verwendet die Absprungratenmetrik und die Metrik „Bounces“. Außerdem werden die Dimension „Suchmaschine“, die Dimension „Suchbegriff“, die Dimension „Einstiegsseite“, die Dimension „Verweisende Domäne“, die Dimension „Trackingcode“ und die Dimension „Verweisende Stelle“ verwendet.  </p> |
| **Advertising Analytics: Paid Search** | Zeigen Sie alle Paid-Search-Daten von Google Ads und Microsoft Advertising nebeneinander an. <p>**Dies kann Ihnen helfen**, den Umfang des an Ihre Site gesendeten Traffics besser zu verstehen und ob Kundinnen und Kunden konvertieren.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. die Kostenwirksamkeit einer Anzeigenkampagne schätzen.</p> |
| **Suchbegriffe – Alle** | Zeigen Sie die Suchbegriffe an, die Besuchende zum Erreichen Ihrer Site verwenden, unabhängig davon, ob es sich um gebührenpflichtige oder organische Suchbegriffe handelt. <p>**Dies kann Ihnen helfen**, die Keywords besser zu verstehen, die bei Suchvorgängen verwendet werden, welche zu Sitetraffic führen. </p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. SEO-Lücken zwischen den verwendeten Keywords und den Keywords, die den Sitetraffic fördern, identifizieren und schließen.</p><p>Diese Vorlage verwendet die Dimension „Suchbegriff“. </p> |
| **Suchbegriffe – Paid** | Zeigen Sie die Suchbegriffe an, die Besuchende zum Erreichen Ihrer Site verwenden und die mit der Paid-Search-Erkennung übereinstimmen.<p>**Dies kann Ihnen helfen**, die Keywords besser zu verstehen, die bei den Suchvorgängen verwendet werden, die zu Sitetraffic führen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. SEO-Lücken zwischen den verwendeten Keywords und den Keywords, die den Sitetraffic fördern, identifizieren und schließen. </p><p>Diese Vorlage verwendet die Dimension „Suchbegriff – Bezahlt“. </p> |
| **Suchbegriffe – Natürlich** | Zeigen Sie die Suchbegriffe an, die Besuchende zum Erreichen Ihrer Site verwenden und die nicht mit der Paid-Search-Erkennung übereinstimmen.<p>**Dies kann Ihnen helfen**, die Keywords besser zu verstehen, die bei Suchvorgängen verwendet werden, welche zu Sitetraffic führen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. SEO-Lücken zwischen den verwendeten Keywords und den Keywords, die den Sitetraffic fördern, identifizieren und schließen.</p><p>Diese Vorlage verwendet die Dimension „Keyword – Natürlich“. </p> |
| **Suchmaschinen – Alle** | Zeigen Sie die Suchmaschinen an, die Besuchende zum Erreichen Ihrer Site verwenden, unabhängig davon, ob es sich um gebührenpflichtige oder organische Suchbegriffe handelt. <p>**Dies kann Ihnen helfen**, die Suchmaschinen besser zu verstehen, die bei Suchvorgängen verwendet werden, die zu Sitetraffic führen. </p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre SEO-Bemühungen auf die Suchmaschinen konzentrieren, die den meisten Traffic zur Site leiten.</p><p>Diese Vorlage verwendet die Dimension „Suchmaschine“. </p> |
| **Suchmaschinen – Paid** | Zeigen Sie die Suchmaschinen an, die Besuchende zum Erreichen Ihrer Site verwenden und die mit der Paid-Search-Erkennung übereinstimmen.<p>**Dies kann Ihnen helfen**, die Suchmaschinen besser zu verstehen, die bei Suchvorgängen verwendet werden, die zu Sitetraffic führen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre SEO-Bemühungen auf die Suchmaschinen konzentrieren, die den meisten Traffic zur Site leiten. </p><p>Diese Vorlage verwendet die Dimension „Suchmaschine – Paid“. </p> |
| **Suchmaschinen – Natürlich** | Zeigen Sie die Suchbegriffe an, die Besuchende zum Erreichen Ihrer Site verwenden und die nicht mit der Paid-Search-Erkennung übereinstimmen.<p>**Dies kann Ihnen helfen**, die Suchmaschinen besser zu verstehen, die bei Suchvorgängen verwendet werden, die zu Sitetraffic führen.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre SEO-Bemühungen auf die Suchmaschinen konzentrieren, die den meisten Traffic zur Site leiten.</p><p>Diese Vorlage verwendet die Dimension „Suchmaschine – Natürlich“. </p> |
| **Rangansicht aller Suchseiten** | Zeigen Sie an, durch welche Seiten der Suchergebnisse sich Besuchende geklickt haben, um Ihre Site zu erreichen. Wenn Ihre Site beispielsweise auf der zweiten Seite der Suchergebnisse einer Suchmaschine erscheint, ist das Dimensionselement für diese Variable „Suchseite 2“.<p>**Dies kann Ihnen helfen**, besser zu verstehen, an welcher Stelle der Suchergebnisse Ihre Seiten angezeigt werden.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre SEO-Strategie verbessern, um sicherzustellen, dass Ihr Inhalt auf der ersten Seite der Suchergebnisse angezeigt wird. </p> |
| **Verweisende Domains** | Zeigen Sie an, durch welche Domains Besuchende sich klicken, um Ihre Site zu erreichen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Sites von Drittanbietern den meisten Traffic zu Ihrer Site leiten. (Auf der externen Site muss ein Link vorhanden sein und Besuchende müssen darauf klicken, damit das Dimensionselement angezeigt wird.)</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Inhalte erstellen oder anpassen, um sie genauer auf die Interessen der Besuchenden von Top-Referrer-Domains auszurichten.  </p><p>Diese Vorlage verwendet die Dimension „Referrer Domain“. </p> |
| **Ursprünglich verweisende Domains** | Zeigen Sie die erste verweisende Domain an, durch die sich Personen zum Erreichen Ihrer Site geklickt haben. (Sobald sie festgelegt wurde, enthält sie denselben Wert für die gesamte Lebensdauer dieser Besucher-ID.)<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Drittanbieter-Sites den Traffic ursprünglich zu Ihrer Site leiten.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Inhalte erstellen oder anpassen, um sie genauer auf die Interessen der Besuchenden von ursprünglichen Top-Referrer-Domains auszurichten.  </p><p>Diese Vorlage verwendet die Dimension „Ursprünglich verweisende Domain“. </p> |
| **Verweisende Stellen** | Zeigen Sie an, auf welchen URLs sich die Besuchenden befanden, als sie sich zu Ihrer Site durchklickten. (In der externen URL muss ein Link vorhanden sein und Besuchende müssen darauf klicken, damit das Dimensionselement angezeigt wird.)  <p>**Dies kann Ihnen helfen**, besser zu verstehen, welche spezifischen URLs den meisten Traffic zu Ihrer Site leiten.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Inhalte erstellen oder anpassen, um sie genauer auf die Interessen der Besuchenden von Top-URLs auszurichten.  </p><p>Diese Vorlage verwendet die Dimension „Referrer Domain“. </p><p>Diese Vorlage verwendet die Dimension „Verweisende Stelle“. </p> |
| **Typen der verweisenden Stellen** | Zeigen Sie an, durch welche generischen Kanäle Besuchende sich geklickt haben, um zu Ihrer Site zu gelangen. Adobe verwaltet die Regeln für jeden Kanal. Mögliche Kanäle sind Suchmaschinen, soziale Netzwerke, andere Websites, die Festplatte oder E-Mails.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Referrer-Typen den meisten Traffic zu Ihrer Site leiten.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Inhalte erstellen oder anpassen, um sie genauer auf die Interessen der Besuchenden von einem bestimmten Kanal auszurichten. </p><p>Diese Vorlage verwendet die Dimension „Typ der verweisenden Stelle“.</p> |

### Mobile {#mobile-not-ready-for-use}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobileCarrierRankedReport"
>title="Zeigen Sie das Telekommunikationsunternehmen an, das Mobilfunkverbindungen mit den Mobilgeräten bereitstellt, mit denen Benutzende auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Mobilnetzbetreiber bei Ihrer Benutzerbasis am beliebtesten sind.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Inhaltsbereitstellung auf Grundlage der Netzwerkfunktionen verschiedener Betreiber anpassen, um ein reibungsloses Anwendererlebnis zu gewährleisten.<br/>Diese Vorlage verwendet die Dimension „Mobilnetzbetreiber“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobileDeviceNameRankedReport"
>title="Zeigen Sie die Marke und das Modell von Mobilgeräten an, mit denen Benutzende auf Ihre Site zugreifen."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Mobilgeräte bei Ihrer Benutzerbasis am beliebtesten sind.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. das Rendering Ihrer Site für die gängigsten Mobilgeräte optimieren.<br/>Diese Vorlage verwendet die Dimension „Mobilgerätename“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobileDeviceTypeRankedReport"
>title="Zeigen Sie die Mobilgerätetypen an, mit denen Benutzende auf Ihre Site zugreifen, z. B. Smartphones oder Tablets."
>abstract="**Dies kann Ihnen dabei helfen**, die verschiedenen Arten von Mobilgeräten besser zu verstehen, die für den Zugriff auf Ihre Site verwendet werden.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Site für die Mobilgerätetypen optimieren, die am häufigsten verwendet werden.<br/>Diese Vorlage verwendet die Dimension „Mobilgerätetyp“."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="template--mobileManufacturerRankedReport"
>title="Zeigen Sie an, welche Hersteller die Mobilgeräte herstellen, mit denen Benutzende auf Ihre Site zugreifen, z. B. Apple und Samsung."
>abstract="**Dies kann Ihnen helfen**, besser zu verstehen, welche Hersteller bei Ihrer Benutzerbasis am beliebtesten sind.<br/>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Inhaltsbereitstellung auf Grundlage der Fähigkeiten verschiedener Hersteller anpassen, um ein reibungsloses Anwendererlebnis zu gewährleisten.<br/>Diese Vorlage verwendet die Dimension „Mobilgerätehersteller“."

<!-- markdownlint-enable MD034 -->

Die folgenden Vorlagen sind verfügbar:

| Vorlagenname | Warum diese Vorlage verwenden?<!-- What do you do with it? What can it help you learn? and What are the potential actions? --> |
| --- | --- | 
| [!UICONTROL **Mobilnetzbetreiber**] | Zeigen Sie das Telekommunikationsunternehmen an, das Mobilfunkverbindungen mit den Mobilgeräten bereitstellt, mit denen Benutzende auf Ihre Site zugreifen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Mobilnetzbetreiber bei Ihrer Benutzerbasis am beliebtesten sind.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Inhaltsbereitstellung auf Grundlage der Netzwerkfunktionen verschiedener Betreiber anpassen, um ein reibungsloses Anwendererlebnis zu gewährleisten.</p><p>Diese Vorlage verwendet die Dimension „Mobilnetzbetreiber“.</p> |
| **Geräte** | Zeigen Sie die Marke und das Modell von Mobilgeräten an, mit denen Benutzende auf Ihre Site zugreifen.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Mobilgeräte bei Ihrer Benutzerbasis am beliebtesten sind.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. das Rendering Ihrer Site für die gängigsten Mobilgeräte optimieren.</p><p>Diese Vorlage verwendet die Dimension „Mobilgerätename“.</p> |
| **Gerätetyp** | Zeigen Sie die Mobilgerätetypen an, mit denen Benutzende auf Ihre Site zugreifen, z. B. Smartphones oder Tablets.<p>**Dies kann Ihnen dabei helfen**, die verschiedenen Arten von Mobilgeräten besser zu verstehen, die für den Zugriff auf Ihre Site verwendet werden.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Site für die Mobilgerätetypen optimieren, die am häufigsten verwendet werden.</p><p>Diese Vorlage verwendet die Dimension „Mobilgerätetyp“.</p> |
| **Hersteller** | Zeigen Sie an, welche Hersteller die Mobilgeräte herstellen, mit denen Benutzende auf Ihre Site zugreifen, z. B. Apple und Samsung.<p>**Dies kann Ihnen helfen**, besser zu verstehen, welche Hersteller bei Ihrer Benutzerbasis am beliebtesten sind.</p><p>**Basierend auf Ihren Erkenntnissen können Sie** eine Reihe von Schritten ausführen, z. B. Ihre Inhaltsbereitstellung auf Grundlage der Fähigkeiten verschiedener Hersteller anpassen, um ein reibungsloses Anwendererlebnis zu gewährleisten.</p><p>Diese Vorlage verwendet die Dimension „Mobilgerätehersteller“.</p> |


