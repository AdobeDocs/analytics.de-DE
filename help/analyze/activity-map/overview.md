---
description: Sortieren Sie Link-Aktivitäten mithilfe von visuellen Überlagerungen, um die Interaktion der Zielgruppe mit Ihren Web-Seiten zu überwachen.
title: Übersicht über Activity Map
feature: Activity Map
role: User, Admin
exl-id: 30a800f7-e2c8-443e-b5d4-36834ef0ba20
source-git-commit: a7670fcda3e8e6af0c036c8b263746e142278255
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 4%

---

# Übersicht über Activity Map

Adobe Analytics Activity Map ist eine Funktion in Adobe Analytics, die eine visuelle Darstellung der Benutzerinteraktion auf Web-Seiten und in Mobile Apps bietet. Marketing-Experten und Analysten können damit Benutzerinteraktionen wie Klicks und Bildlaufverhalten verfolgen und analysieren. Activity Map generiert Heatmaps und Überlagerungsberichte, die die beliebtesten Elemente auf einer Web-Seite zeigen und Ihnen bei der Optimierung Ihrer digitalen Erlebnisse helfen.

Activity Map as a umfasst mehrere wichtige Komponenten:

* **Report Suite-Einstellung**: Für eine Report Suite muss Activity Map aktiviert sein, bevor Sie sie verwenden können. Siehe [Activity Map-](/help/admin/tools/manage-rs/edit-settings/activity-map.md) in den Report Suite-Einstellungen.
* **Implementierung**: Die meisten Activity Map-Berichte sind vorkonfiguriert verfügbar. Einige Websites benötigen jedoch möglicherweise zusätzliche Implementierungen, um das Linktracking optimal zu nutzen. Die folgenden Implementierungsvariablen sind verfügbar:
   * [`ActivityMap.linkExclusions`](/help/implement/vars/config-vars/activitymap-linkexclusions.md): Klickdaten nach Link-Namen filtern.
   * [`ActivityMap.regionExclusions`](/help/implement/vars/config-vars/activitymap-regionexclusions.md): Klickdaten nach Regionsnamen filtern.
   * [`ActivityMap.regionIDAttribute`](/help/implement/vars/config-vars/activitymap-regionidattribute.md): Ändern des Attributs, das die Dimension Activity Map-Region ausfüllt.
   * [`ActivityMap.link`](/help/implement/vars/functions/activitymap-link.md): Passen Sie die Logik an, die Activity Map zum Ausfüllen der Dimension &quot;Activity Map Link“ verwendet.
   * [`ActivityMap.region`](/help/implement/vars/functions/activitymap-region.md): Passen Sie die Logik an, die Activity Map zum Ausfüllen der Dimension Activity Map-Region verwendet.
* **Überlagerung**: Eine Browser-Erweiterung, mit der Sie Klickdaten auf Ihrer Website überlagert anzeigen können. Weitere Informationen finden Sie unter {[}Activity Map-Erweiterungsschnittstelle. &#x200B;](overlay/overview.md) Diese Funktion ist nicht für Web SDK-Implementierungen verfügbar.
* **Dimensionen**: Zusätzlich zur Überlagerungserweiterung stellt Activity Map mehrere Dimensionen bereit, die Sie in Analysis Workspace verwenden können.
   * [Activity Map-Link](/help/components/dimensions/activity-map-link.md): Der Link-Name, auf den geklickt wurde.
   * [Activity Map-Region](/help/components/dimensions/activity-map-region.md): Der Name der Region, auf die geklickt wurde.
   * [Activity Map Page](/help/components/dimensions/activity-map-page.md): Der Seitenname zum Zeitpunkt, an dem auf den Link geklickt wurde.
   * [Activity Map-Link nach Region](/help/components/dimensions/activity-map-link-by-region.md): Ein verketteter Wert von Activity Map Link und Activity Map-Region.

## Funktionen und Vorteile

* **Visualisierung der Benutzerinteraktion**: Activity Map bietet eine dynamische visuelle Darstellung des Benutzerverhaltens, sodass Sie genau sehen können, wo die Benutzer klicken. Diese visuellen Daten erleichtern die Identifizierung von Mustern, Trends und Interessenbereichen. Sie können dann fundierte Entscheidungen über Design, Inhaltsplatzierung und Benutzerfluss treffen.

* **Heatmaps**: Activity Map generiert Heatmaps, die die am häufigsten angeklickten oder interagierten Bereiche einer Web-Seite anzeigen. Heatmaps verwenden eine Farbcodierung, um den Grad der Interaktion darzustellen, sodass Sie Hotspots identifizieren und die Aufmerksamkeit auf Bereiche mit starken Auswirkungen konzentrieren können. Diese Informationen können für die Optimierung von call-to-action-Schaltflächen, Links, Formularen oder anderen interaktiven Elementen nützlich sein.

* **Überlagerungsberichte**: Überlagerungsberichte in Activity Map bieten detaillierte Klickmetriken für bestimmte Elemente auf einer Web-Seite. Indem Sie die Clickthrough-Raten und Interaktionsstufen einzelner Elemente verstehen, können Sie Ihre Design- und Inhaltsstrategien optimieren, um Benutzererlebnisse zu verbessern. Diese Funktion ist nicht für Web SDK-Implementierungen verfügbar.

* **Segmentanalyse**: Sie können das Benutzerverhalten basierend auf verschiedenen Segmenten analysieren, z. B. Traffic-Quellen, Demografie oder Personas. Durch die Segmentierung der Daten können Sie wertvolle Einblicke in bestimmte Benutzergruppen gewinnen, was personalisierte Erlebnisse und zielgerichtete Marketing-Strategien ermöglicht.

## Praktische Anwendungen

* **Website-Optimierung**: Mit Activity Map können Sie Ihre Websites optimieren, indem Sie leistungsschwache Elemente identifizieren, die Navigation verbessern und das Gesamterlebnis für Benutzende verbessern. Durch die Analyse von Benutzerinteraktionen können Sie datengesteuerte Entscheidungen treffen, um Benutzerflüsse zu optimieren, Formulare zu vereinfachen oder die Platzierung von Inhalten anzupassen, um eine maximale Wirkung zu erzielen.

* **Konversionsratenoptimierung**: Durch die Visualisierung der Benutzerinteraktion und die Analyse der Clickthrough-Raten spielt Activity Map eine entscheidende Rolle bei den CRO-Bemühungen. Sie können Konversionshindernisse identifizieren und mit verschiedenen Design-Varianten experimentieren, um Konversionstrichter, Landingpages und Checkout-Prozesse zu optimieren.

* **A/B-Tests**: Activity Map kann mit A/B-Tests kombiniert werden, um die Auswirkungen von Design- oder Inhaltsänderungen zu messen. Durch den Vergleich von Interaktionsmetriken zwischen verschiedenen Versionen einer Web-Seite können Sie bestimmen, welche Varianten zu höherer Benutzerinteraktion, höheren Konversionsraten oder mehr Umsatz führen.

