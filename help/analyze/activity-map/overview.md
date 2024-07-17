---
description: Linkaktivität mit visuellen Überlagerungen sortieren , um die Interaktion der Zielgruppe mit Ihren Webseiten zu überwachen.
title: Übersicht über Activity Map
feature: Activity Map
role: User, Admin
exl-id: 30a800f7-e2c8-443e-b5d4-36834ef0ba20
source-git-commit: 72b38970e573b928e4dc4a8c8efdbfb753be0f4e
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 4%

---

# Übersicht über Activity Map

Adobe Analytics Activity Map ist eine Funktion in Adobe Analytics, die eine visuelle Darstellung der Benutzerinteraktion auf Web-Seiten und in Mobile Apps bietet. Damit können Marketing-Experten und Analysten Benutzerinteraktionen wie Klicks und Scrollverhalten verfolgen und analysieren. Activity Map generiert Heatmaps und Überlagerungsberichte, die die beliebtesten Elemente auf einer Webseite zeigen und Ihnen so bei der Optimierung Ihrer digitalen Erlebnisse helfen.

Dieser Abschnitt der Dokumentation konzentriert sich auf die Activity Map-Überlagerung. Es gibt jedoch weitere wichtige Aspekte bei der Verwendung von Activity Map:

* **Report Suite-Einstellung**: Für eine Report Suite muss Activity Map aktiviert sein. Siehe [Activity Map Reporting](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/activity-map.md) in den Report Suite-Einstellungen.
* **Implementierung**: Die meisten Activity Map-Berichte sind standardmäßig verfügbar. Einige Websites erfordern jedoch möglicherweise eine zusätzliche Implementierung, um das Linktracking optimal zu nutzen. Die folgenden Implementierungsvariablen sind verfügbar:
   * [`ActivityMap.linkExclusions`](/help/implement/vars/config-vars/activitymap-linkexclusions.md): Filtern Sie Klickdaten nach Linknamen.
   * [`ActivityMap.regionExclusions`](/help/implement/vars/config-vars/activitymap-regionexclusions.md): Filtern Sie die Klickdaten nach dem Regionennamen.
   * [`ActivityMap.regionIDAttribute`](/help/implement/vars/config-vars/activitymap-regionidattribute.md): Ändern Sie das Attribut, mit dem die Dimension &quot;Activity Map-Region&quot;gefüllt wird.
   * [`ActivityMap.link`](/help/implement/vars/functions/activitymap-link.md): Passen Sie die Logik an, die Activity Map zum Füllen der Dimension &quot;Activity Map-Link&quot;verwendet.
   * [`ActivityMap.region`](/help/implement/vars/functions/activitymap-region.md): Passen Sie die Logik an, die Activity Map zum Füllen der Dimension &quot;Activity Map-Region&quot;verwendet.
* **Dimensionen**: Zusätzlich zur Überlagerungserweiterung bietet Activity Map mehrere Dimensionen, die Sie in Analysis Workspace verwenden können.
   * [Activity Map-Link](/help/components/dimensions/activity-map-link.md): Der Link-Name, auf den geklickt wurde.
   * [Activity Map Region](/help/components/dimensions/activity-map-region.md): Der Name der Region, auf die geklickt wurde.
   * [Activity Map-Seite](/help/components/dimensions/activity-map-page.md): Der Seitenname zum Zeitpunkt, zu dem auf den Link geklickt wurde.
   * [Activity Map-Link nach Region](/help/components/dimensions/activity-map-link-by-region.md): Ein verketteter Wert von Activity Map-Link und Activity Map-Region.

## Funktionen und Vorteile

* **Visualisierung der Benutzerinteraktion**: Activity Map bietet eine dynamische visuelle Darstellung des Benutzerverhaltens, sodass Sie genau sehen können, wo Benutzer klicken. Diese visuellen Daten erleichtern die Identifizierung von Mustern, Trends und Interessensgebieten. Anschließend können Sie fundierte Entscheidungen über Design, Inhaltsplatzierung und Benutzerfluss treffen.

* **Heatmaps**: Activity Map generiert Heatmaps, die die am häufigsten angeklickten oder interagierten Bereiche einer Webseite anzeigen. Bei Heatmaps wird die Interaktionsstufe mit Farbcodierung dargestellt, sodass Sie Hotspots identifizieren und die Aufmerksamkeit auf Bereiche mit hoher Auswirkung richten können. Diese Informationen können für die Optimierung von Aktionsaufruf-Schaltflächen, Links, Formularen oder anderen interaktiven Elementen nützlich sein.

* **Überlagerungsberichte**: Überlagerungsberichte in Activity Map bieten detaillierte Klickmetriken für bestimmte Elemente auf einer Webseite. Indem Sie die Clickthrough-Raten und Interaktionsstufen einzelner Elemente verstehen, können Sie Ihre Design- und Inhaltsstrategien zur Verbesserung der Benutzererlebnisse anpassen.

* **Segmentanalyse**: Sie können das Benutzerverhalten anhand verschiedener Segmente analysieren, z. B. Traffic-Quellen, demografische Daten oder Personas. Durch die Segmentierung der Daten können Sie wertvolle Einblicke in bestimmte Benutzergruppen gewinnen und so personalisierte Erlebnisse und zielgerichtete Marketingstrategien ermöglichen.

## Praktische Anwendungen

* **Website-Optimierung**: Mit der Activity Map können Sie Ihre Websites optimieren, indem Sie leistungsschwache Elemente identifizieren, die Navigation verbessern und das gesamte Benutzererlebnis verbessern. Durch die Analyse von Benutzerinteraktionen können Sie datengesteuerte Entscheidungen treffen, um Benutzerflüsse zu optimieren, Formulare zu vereinfachen oder die Inhaltsplatzierung so anzupassen, dass eine maximale Wirkung erzielt wird.

* **Optimierung der Konversionsrate**: Durch Visualisierung der Benutzerinteraktion und Analyse der Clickthrough-Raten spielt Activity Map eine entscheidende Rolle bei den CRO-Bemühungen. Sie können Hindernisse für die Konversion identifizieren und mit verschiedenen Designvarianten experimentieren, um Konversionstrichter, Landingpages und Checkout-Prozesse zu optimieren.

* **A/B-Tests**: Activity Map kann mit A/B-Tests kombiniert werden, um die Auswirkungen von Design- oder Inhaltsänderungen zu messen. Durch den Vergleich von Interaktionsmetriken zwischen verschiedenen Versionen einer Webseite können Sie feststellen, welche Varianten zu höherer Benutzerinteraktion, Konversionsrate oder Umsatz führen.

* **Optimieren mobiler Apps**: Activity Map ist nicht auf Websites beschränkt, sondern erweitert auch seine Funktionalität auf mobile Apps. Sie können Einblicke in Benutzerinteraktionen in Apps erhalten, sodass diese die Benutzerfreundlichkeit verbessern, die Navigation verbessern und Funktionen für ein nahtloses mobiles Erlebnis optimieren können.
