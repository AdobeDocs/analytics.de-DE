---
title: Benutzervoreinstellungen
description: Erfahren Sie, wie Sie allgemeine und Projektvoreinstellungen für Benutzer festlegen.
feature: Workspace Basics
role: User, Admin
exl-id: f32e3061-f396-4730-96e1-d251b00e32f0
source-git-commit: 6cec1085093404235e29319db984d4389c68c31e
workflow-type: tm+mt
source-wordcount: '3461'
ht-degree: 80%

---

# Benutzervoreinstellungen

Sie können für alle neu erstellten Projekte oder Bedienfelder die auf Analysis Workspace und die zugehörigen Komponenten anzuwendenden Einstellungen verwalten. Bestehende Projekte und Bedienfelder sind davon nicht betroffen.


>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Verwalten von Voreinstellungen](https://video.tv.adobe.com/v/332600/?quality=12&learn=on){target="_blank"} finden Sie ein Demovideo.

>[!ENDSHADEBOX]

## Aktualisieren von Voreinstellungen

Sie können Ihre Voreinstellungen wie folgt aktualisieren:

- Wählen Sie ![UserAdmin](/help/assets/icons/UserAdmin.svg) **[!UICONTROL Voreinstellungen bearbeiten]** in der Hauptbenutzeroberfläche von Workspace aus.
- Wählen Sie bei der Arbeit an einem Workspace-Projekt im Menü **[!UICONTROL Projekt]** > **[!UICONTROL Benutzervoreinstellungen]** aus.
- Wählen Sie in der oberen Menüleiste von Customer Journey Analytics **[!UICONTROL Komponenten]** > **[!UICONTROL Voreinstellungen]** aus (nur für Produktadmins verfügbar).

## Konfigurieren von Voreinstellungen

Sie können die folgenden Voreinstellungen konfigurieren:


## Allgemeine Voreinstellungen

Sie können die allgemeinen Voreinstellungen für alle neuen Projekte anpassen, die Sie in Analysis Workspace erstellen. Informationen zum Zugriff auf diese Voreinstellungen finden Sie unter [Aktualisieren von Voreinstellungen](#update-preferences).

| Voreinstellung | Optionen |
| --- | --- |
| Landingpage | Wählen Sie aus, welche Seite beim Zugriff auf Adobe Analytics als Standardseite angezeigt werden soll: <ul><li>Projektliste (Standard)</li><li>Leeres Projekt</li><li>Bestimmtes Projekt, das aus einer Liste ausgewählt wurde</li></ul> |
| Tipps anzeigen | Zeigt Tipps in einem blauen Feld im rechten unteren Bereich von Analysis Workspace an. <p>Standardmäßig ist diese Option aktiviert.</p> |
| Komponenten, die in Gruppen auf der linken Leiste angezeigt werden | Wählen Sie aus, wie viele Komponenten im Komponentenmenü in der linken Leiste angezeigt werden sollen. <p>Wenn Sie „0“ auswählen, kann die Komponente nicht mehr über die linke Leiste Ihrer Arbeitsbereiche aufgerufen werden.</p><p>Standardmäßig werden für jede der folgenden Objekte fünf Komponenten angezeigt:</p> <ul><li>Dimensionen</li><li>Metriken</li><li>Filter</li><li>Datumsbereiche</li></ul> <p>Weitere Informationen zu Komponenten in Analysis Workspace finden Sie unter [Komponentenübersicht](/help/analyze/analysis-workspace/components/analysis-workspace-components.md).</p> |

## Unternehmensvoreinstellungen {#company-preferences}

>[!CONTEXTUALHELP]
>id="workspace_prefs_shareonlyworkspace"
>title="Freigabe nur für Workspace-Benutzende zulassen"
>abstract="Wenn diese Option aktiviert ist, ist die Option **[!UICONTROL Für alle freigeben]** nicht mehr für Benutzende verfügbar, wenn ein Analysis Workspace-Projekt freigegeben wird. Personen, die zuvor über diese Freigabeoption Zugriff auf ein Projekt erhalten haben, können nicht mehr auf das Projekt zugreifen."

>[!CONTEXTUALHELP]
>id="workspace_prefs_requireexperiencecloudauth"
>title="Experience Cloud-Authentifizierung verlangen"
>abstract="Wenn diese Option aktiviert ist, müssen sich Personen, die über die Option **[!UICONTROL Für alle freigeben]** in Analysis Workspace Zugriff auf ein Projekt erhalten haben, mit ihren Anmeldedaten von Experience Cloud authentifizieren."

>[!CONTEXTUALHELP]
>id="workspace_prefs_projectcommenting"
>title="Kommentieren in Projekten zulassen"
>abstract="Wenn diese Option aktiviert ist, wird in der rechten Leiste jedes Projekts in Analysis Workspace ein Kommentarbereich verfügbar."


Sie können Unternehmensvoreinstellungen aktualisieren, die für alle Benutzerinnen und Benutzer sowie Projekte in Ihrer Organisation gelten. Informationen zum Zugriff auf diese Voreinstellungen finden Sie unter [Aktualisieren von Voreinstellungen](#update-preferences).

| Abschnitt | Voreinstellung | Optionen |
| --- | --- | --- |
| **Registerkarte „Vorlagen“** | | |
|  | Registerkarte „Vorlagen“ ausblenden | Blendet die Registerkarte Vorlagen für alle Benutzer in Ihrer Organisation aus. |
| **Projektfreigabe** | | |
| | Freigabe nur für Workspace-Benutzende zulassen | Wenn diese Option aktiviert ist, können Benutzende in Ihrer Organisation im Menü **[!UICONTROL Freigeben]** die Option **[!UICONTROL Für alle freigeben]** nicht sehen. Benutzer können keine Projekte für Personen freigeben, die in Ihrem Unternehmen kein Analysis Workspace-Konto haben, wie unter [Freigeben eines Projekts für alle (keine Anmeldung erforderlich)](/help/analyze/analysis-workspace/curate-share/share-projects.md#share-public-link) beschrieben.<br/>Diese Option ist standardmäßig für alle Organisationen deaktiviert, mit Ausnahme von Kunden, die Healthcare Shield lizenziert haben. <p>Beachten Sie beim Aktivieren oder Deaktivieren dieser Option Folgendes:<ul><li>Wenn Sie diese Option aktivieren, können Personen, die zuvor über die Freigabeoption **[!UICONTROL Für alle freigeben]** Zugriff auf ein Projekt erhalten haben, nicht mehr auf das Projekt zugreifen.</li><li>Wenn diese Option aktiviert ist (um die Freigabe nur für Workspace-Benutzende zuzulassen) und später deaktiviert wird (um die Freigabe für andere zuzulassen), erhalten Personen, die zuvor über die Freigabeoption **[!UICONTROL Für alle freigeben]** Zugriff auf ein Projekt erhalten hatten, nicht automatisch wieder Zugriff auf das Projekt. In diesem Fall muss der Benutzer, der das Projekt freigegeben hat, die Option [!UICONTROL **Link ist aktiv**] aktivieren, die verfügbar ist, wenn ein Projekt für alle freigegeben wird **([!UICONTROL Freigeben]** > **[!UICONTROL Für alle freigeben]**), wie unter [Projekt für alle freigeben (keine Anmeldung erforderlich)](/help/analyze/analysis-workspace/curate-share/share-projects.md#share-public-link).</li><li>**Für Kundinnen und Kunden, die Healthcare Shield lizenzieren:** Diese Option ist standardmäßig aktiviert und kann nicht deaktiviert werden. Bevor Sie diese Option deaktivieren können, damit die Benutzenden die Freigabeoption **[!UICONTROL Für alle freigeben]** verwenden können, müssen Sie zunächst in der Adobe Admin Console die Berechtigung [!UICONTROL Projekt-Links für alle freigeben] (unter [!UICONTROL Reporting-Tools]) hinzufügen. Nachdem die Berechtigung hinzugefügt wurde, können Sie diese Option deaktivieren und dann den resultierenden rechtlichen Hinweis akzeptieren. Informationen zum Hinzufügen einer Berechtigung zur Admin Console finden Sie unter [Verwalten von Produktberechtigungen in der Admin Console](https://helpx.adobe.com/de/enterprise/using/manage-permissions-and-roles.html).</li></ul> |
| | Experience Cloud-Authentifizierung verlangen | Wenn diese Option aktiviert ist, müssen sich Personen, die über die Option **[!UICONTROL Für alle freigeben]** in Analysis Workspace Zugriff auf ein Projekt erhalten, mit ihren Experience Cloud-Anmeldeinformationen authentifizieren.<p>Wenn diese Option aktiviert ist, wird jedes Mal, wenn eine Person ein Projekt mithilfe der Freigabeoption **[!UICONTROL Für alle freigeben]** teilt, die Option **[!UICONTROL Experience Cloud-Authentifizierung verlangen]** im Freigabedialogfeld aktiviert und kann von der Person, die das Projekt freigegeben hat, nicht deaktiviert werden. Informationen dazu, wie Benutzer Projekte für andere freigeben können, finden Sie unter [Freigeben eines Projekts für andere (keine Anmeldung erforderlich)](/help/analyze/analysis-workspace/curate-share/share-projects.md#share-public-link). <p> <p>Beachten Sie beim Aktivieren dieser Option Folgendes: <ul><li>Wenn Sie diese Option aktivieren, werden alle Projekte, die zuvor mit der Freigabeoption **[!UICONTROL Für alle freigeben]** freigegeben wurden und für die die Option [!UICONTROL Experience Cloud-Authentifizierung verlangen] nicht aktiviert ist, deaktiviert.<p>Wenn diese Option aktiviert ist (d. h., eine Experience Cloud-Authentifizierung erforderlich ist) und später deaktiviert wird (damit alle Benutzenden mit dem Link auf das Projekt zugreifen können), können Personen, die zuvor über die Freigabeoption **[!UICONTROL Für alle freigeben]** Zugriff auf ein Projekt erhalten haben, nicht automatisch wieder auf das Projekt zugreifen. In diesem Fall muss der Benutzer, der das Projekt freigegeben hat, die Option [!UICONTROL Link ist aktiv] aktivieren, die verfügbar ist, wenn ein Projekt für alle freigegeben wird **([!UICONTROL Freigeben]** > **[!UICONTROL Für alle freigeben]** > **[!UICONTROL Link ist aktiv]**), wie unter [Projekt für alle freigeben (keine Anmeldung erforderlich)](/help/analyze/analysis-workspace/curate-share/share-projects.md#share-public-link) beschrieben.</li><li>Diese Option ist nur verfügbar, wenn SSO in Ihrem Unternehmen implementiert ist. Informationen dazu, wie System-Admins SSO für Ihre Organisation aktivieren können, finden Sie unter [Einrichten von Identität und Single Sign-on](https://helpx.adobe.com/de/enterprise/using/set-up-identity.html).</p><p>Wenn SSO für Ihre Organisation konfiguriert ist, überprüfen Sie, ob in der Konsole eine automatische Kontoerstellung implementiert ist. Normalerweise richten System-Admins dies ein, wie unter [Aktivieren der automatischen Kontoerstellung](https://helpx.adobe.com/de/enterprise/using/automatic-account-creation.html) beschrieben wird.</li><li>Wenn Ihre Organisation eine Lizenz für Healthcare Shield besitzt, ist diese Option standardmäßig aktiviert und kann nicht deaktiviert werden.</li></ul> |

{style="table-layout:auto"}

## Voreinstellungen für Projekte und Analysen {#project-analyses-preferences}

>[!CONTEXTUALHELP]
>id="workspace_prefs_categoricalpalette"
>title="Kategorische Palette"
>abstract="Wird auf viele Visualisierungen in Analysis Workspace und geführte Analysen angewendet. Jede Farbe steht für einen Wert einer Kategorie."

>[!CONTEXTUALHELP]
>id="workspace_prefs_divergingpalette"
>title="Divergierende Palette"
>abstract="Wird auf die Kohortentabelle in Analysis Workspace und die geführte Analyse von Benutzerwachstum angewendet. Durch diese Palette werden die Zahlen zwischen zwei Extremwerten dargestellt, getrennt durch eine Basislinie in der Mitte."

>[!CONTEXTUALHELP]
>id="workspace_prefs_sequentialpalette"
>title="Sequenzielle Palette"
>abstract="Wird bei der geführten Analyse der Frequenz-Trends angewendet (gestapelte Balken). In dieser Palette werden Zahlen durch die Helligkeitsabstufungen von hell bis dunkel dargestellt."

Sie können die Projektvoreinstellungen für alle neuen Projekte anpassen, die Sie in Analysis Workspace erstellen. Informationen zum Zugriff auf diese Voreinstellungen finden Sie unter [Aktualisieren von Voreinstellungen](#update-preferences).

Einige dieser Voreinstellungen können auch für einzelne Projekte angepasst werden, wie unter &quot;[&quot; ](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md).

Klicken Sie auf die verlinkten Voreinstellungstitel, um weitere Informationen und Kontext zu den einzelnen Voreinstellungen zu erhalten.

| Abschnitt | Voreinstellung | Optionen |
| --- | --- | --- |
| **Anzeigen** | | |
|  | [Dichte anzeigen](https://experienceleague.adobe.com/de/docs/analytics/analyze/analysis-workspace/build-workspace-project/view-density) | Wählen Sie aus, wie viel Inhalt auf dem Bildschirm angezeigt werden soll, indem Sie den vertikalen Abstand der linken Schiene, der Freiformtabellen und der Kohortentabellen verkleinern. <ul><li>Kompakt</li><li>Komfortabel</li><li>Erweitert (Standard)</li></ul> |
| | [Farbpalette](https://experienceleague.adobe.com/de/docs/analytics/analyze/analysis-workspace/build-workspace-project/color-palettes) | Wählen Sie die in Analysis Workspace verwendeten Farbpaletten für die Visualisierung aus.<ul><li>**Kategorische Palette**: Wird auf viele Visualisierungen in Analysis Workspace angewendet. Jede Farbe stellt einen bestimmten kategorischen Wert dar. Wählen Sie aus den von Adobe bereitgestellten Optionen oder geben Sie eine benutzerdefinierte Palette ein, die durch kommagetrennte Hexadezimalwerte definiert ist.</li><li>**Divergente Palette**: Wird auf die Kohortentabelle in Analysis Workspace angewendet. Diese Palette enthält eine numerische Bedeutung mit zwei Extremen und einer Grundlinie in der Mitte.</li><li>**Sequenzielle Palette**: Wird auf die geführte Analyse der Häufigkeits-Trends (gestapelter Balken) angewendet. Diese Palette hat eine numerische Bedeutung von hell bis dunkel.</li></ul> |
| **Daten** | | |
|  | [Report Suite](https://experienceleague.adobe.com/de/docs/analytics/analyze/analysis-workspace/panels/panels) | Wählen Sie aus, von wo Tabellen und Visualisierungen ihre Daten beziehen sollen. <ul><li>Zuletzt verwendet (Standard)</li><li>Spezifische Report Suite, die aus einer Liste ausgewählt wurde</li></ul> |
|  | [Kalender](https://experienceleague.adobe.com/de/docs/analytics/analyze/analysis-workspace/panels/panels) | Wählen Sie aus einer Liste, die Folgendes enthält: <ul><li>Von Adobe bereitgestellte Bereiche (Standard ist „Diesen Monat“)</li><li>Benutzerdefinierte Bereiche</li></ul> |
|  | [Typ des Bedienfelds](https://experienceleague.adobe.com/de/docs/analytics/analyze/analysis-workspace/panels/panels) | <ul><li>Freiform (Standard)</li><li>Leer</li><li>Quick Insights</li></ul> |
|  | Wiederholte Instanzen zählen | Diese Einstellung legt fest, ob wiederholte Instanzen in Berichten gezählt werden sollen. Beispielsweise werden mit dieser Einstellung (wenn aktiviert) mehrere aufeinanderfolgende Aufrufe derselben Seite wie mehrere Seitenaufrufe gezählt. Ist diese Einstellung deaktiviert, werden sie als nur ein einziger Seitenaufruf gezählt. <p>**Hinweis:** Diese Einstellung wirkt sich nur auf bestimmte Metriken aus (z. B. Einzelseitenbesuche) und nicht auf Fluss- oder Fallout-Visualisierungen.</p> |
|  | Zahlenformat | <ul><li>1.000,00 (Standard)</li><li>1.000,00</li><li>1 000,00</li></ul> |
|  | CSV-Trennzeichen | <ul><li>Komma (Standard)</li><li>Semikolon</li><li>Doppelpunkt</li><li>Verkettungszeichen</li><li>Zeitraum</li><li>Leerzeichen</li><li>Tab</li></ul> |
|  | Anmerkungen anzeigen | Wählen Sie aus, ob Anmerkungen in Ihren Projekten sichtbar sein sollen. Weitere Informationen zu Anmerkungen finden Sie unter [Anmerkungen – Überblick](/help/analyze/analysis-workspace/components/annotations/overview.md). |

## Voreinstellungen für Freiformtabellen {#freeform-table-preferences}

>[!CONTEXTUALHELP]
>id="workspace_prefs_showanomalies"
>title="Anomalien anzeigen"
>abstract="Wenn Sie **[!UICONTROL Anomalien zeigen]** auswählen, wird die Anomalieerkennung automatisch für die erste Metrik-Spalte ausgeführt, die zu einer Freiformtabellen-Visualisierung der Zeitreihe hinzugefügt wurde."

>[!CONTEXTUALHELP]
>id="workspace_prefs_showforecast"
>title="Prognose anzeigen"
>abstract="Wenn Sie **[!UICONTROL Prognose anzeigen]** auswählen, wird die Prognose automatisch für die erste Metrik-Spalte ausgeführt, die zu einer Freiformtabellen-Visualisierung der Zeitreihe hinzugefügt wurde."


>[!CONTEXTUALHELP]
>id="workspace_prefs_defaulttablemetric"
>title="Standard-Tabellenmetrik"
>abstract="Wählen Sie die Standardmetrik aus, die für Freiformtabellen verwendet werden soll. Wenn die ausgewählte Datenansicht die ausgewählte Standardmetrik nicht enthält, wechselt die Tabelle automatisch zu einer anderen primären Metrik."


Sie können die Voreinstellungen für Freiformtabellen für alle neuen Projekte anpassen, die Sie in Analysis Workspace erstellen. Informationen zum Zugriff auf diese Voreinstellungen finden Sie unter [Aktualisieren von Voreinstellungen](#update-preferences).

Einige dieser Voreinstellungen können auch für einzelne Tabellen angepasst werden.

Klicken Sie auf die verlinkten Abschnittstitel, um weitere Informationen und den Kontext zu den verfügbaren Voreinstellungen anzuzeigen.

| Abschnitt | Voreinstellung | Optionen |
| --- | --- | --- |
| **Tabelle** | | |
| | Tabellentyp | <ul><li>Freiform</li><li>Tabellen-Builder</li></ul> |
| | Standard-Tabellenmetrik | <ul><li>Vorkommen</li><li>Unique Visitors</li><li>Besuche</li></ul> |
| | Standarddimension der Tabelle | Wählen Sie zwischen Minute, Stunde, Tag, Woche, Monat, Quartal oder Jahr. |
| | Datum ausrichten | Wählen Sie diese Option, um die Daten in allen Spalten so auszurichten, dass sie alle in derselben Zeile beginnen. |
| **[Spalte](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md)** | | |
| | Kopfzeilentext umbrechen | Lassen Sie den Kopfzeilentext in Freiformtabellen umbrechen, damit Kopfzeilen besser lesbar und Tabellen einfacher freizugeben sind. Ein Umbruch ist beim PDF-Rendern und für Metriken mit langen Namen nützlich. Standardmäßig aktiviert. |
| | Summen anzeigen | Diese Summe entspricht in der Regel der Gesamtsumme oder einer Teilmenge [!UICONTROL Gesamtsumme]. Er spiegelt alle Tabellenfilter wider, die innerhalb der Freiformtabelle angewendet werden, einschließlich der Option [!UICONTROL Keine einschließen]. |
| | Gesamtsummen anzeigen | Dieser Gesamtwert stellt alle erfassten Treffer dar, manchmal auch als „Report Suite *Gesamtsumme*. Wenn ein Segment entweder auf Bedienfeldebene oder in der Freiformtabelle angewendet wird, passt sich diese Summe an, um alle Treffer wiederzugeben, die den Segmentkriterien entsprechen. Gesamtsumme wird für Tabellen oder Aufschlüsselungen mit [statischen Zeilen](/help/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.md) nicht unterstützt. |
| | Sparkline anzeigen | Liniendiagramme am unteren Rand des Diagramms anzeigen oder ausblenden. Wenn sie ausgeblendet sind, wird die Legende so geändert, dass sie keinen visuellen Bezug mehr zu den Linien hat. |
| | Nummer | Definition, ob in einer Zelle der numerische Wert der Metrik angezeigt wird oder nicht. Wenn es sich bei der Metrik beispielsweise um Seitenansichten handelt, ist der numerische Wert die Anzahl der Seitenansichten für das Zeilenelement. |
| | Prozent | Definition, ob in einer Zelle der Prozentwert der Metrik angezeigt wird oder nicht. Ist die Metrik beispielsweise „Seitenansichten“, ist der Prozentwert die Anzahl an Seitenansichten für dieses Zeilenelement geteilt durch die Gesamtanzahl der Seitenansichten für diese Spalte. Hinweis: Um genauer zu sein: Prozentsätze über 100% werden manchmal angezeigt. Die obere Begrenzung wird auf 1.000 % verschoben, um sicherzustellen, dass Spalten in Breiten zu groß werden können. |
| | Anomalien anzeigen | Gibt an, ob die Anomalieerkennung für die Werte dieser Spalte ausgeführt wird |
| | Null nicht als Wert interpretieren | Definition, ob in Zellen mit 0-Wert eine 0 oder nichts angezeigt wird. Diese Option ist praktisch, wenn Sie die Daten für einzelne Tage eines Monats anzeigen und einige Tage noch in der Zukunft liegen.  Statt für in der Zukunft liegende Daten eine 0 anzuzeigen, kann die entsprechende Zelle auch leer angezeigt werden. Diagramme berücksichtigen auch diese Einstellung (d. h. sie zeigen keine Linie oder Balken mit 0 Werten an, wenn diese Einstellung aktiviert ist). |
| | Hintergrund | Gibt an, ob in einer Zelle alle Zellformatierungen ein-/ausgeblendet werden, einschließlich Balkendiagramm und bedingter Formatierung <ul><li>Balkendiagramm</li> Ein horizontales Balkendiagramm, das den Wert der Zelle im Verhältnis zur Gesamtgröße der Spalte darstellt. <li>Bedingte Formatierung</li>Weitere Informationen zur bedingten Formatierung finden Sie unter „Bedingte Formatierung“ in den [Spalteneinstellungen](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md).</ul> |
| | Zellenvorschau | Zeigt die jeweiligen Zellen mit allen ausgewählten Formatierungsoptionen in einer Vorschau an. |
| **[Zeile ](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/table-settings.md)** | | |
| | Aufschlüsselung nach Position | Wählen Sie diese Option aus, wenn die Aufschlüsselung bei der Position des Elements und nicht beim Element selbst bleiben soll. Weitere Informationen zur Aufschlüsselungen finden Sie unter [Dimensionen aufschlüsseln](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md). |
| | Prozentuale Berechnung | <ul><li>Spalte</li><li>Zeile</li></ul> |
| | Spaltensummen (nur statische Zeilen) | <ul><li>Summe der Zeilen anzeigen: Zeigt die Summe der einzelnen Zeileneinträge an </li><li>Gesamtsumme anzeigen: Zeigt die deduplizierte Summe der Zeilen an.</li></ul> |

## Voreinstellungen für Visualisierungen

Sie können die Voreinstellungen für Visualisierungen für alle in Analysis Workspace neu erstellten Projekte aktualisieren. Informationen zum Zugriff auf diese Voreinstellungen finden Sie unter [Aktualisieren von Voreinstellungen](#update-preferences).

Einige dieser Voreinstellungen können auch für individuelle Visualisierungen angepasst werden.

Klicken Sie auf die verlinkten Abschnittstitel, um weitere Informationen und den Kontext zu den verfügbaren Voreinstellungen anzuzeigen.

| Abschnitt | Voreinstellung | Optionen |
| --- | --- | --- |
| **Allgemeine Standardeinstellungen** | | |
| | Prozentsatz | Zeigt für alle Visualisierungen Werte in Prozentsätzen an. |
| | Legende sichtbar | Ermöglicht für alle Visualisierungen das Ausblenden des detaillierten Legendentextes. |
| | Grenzwert für max. Anzahl von Elementen | Reduziert für alle Visualisierungen die Anzahl der Elemente auf der X-Achse. Dies kann bei großen Datensätzen nützlich sein. |
| | Zwei Achsen anzeigen (falls anwendbar) | Gilt nur, wenn Sie zwei Metriken haben - Sie können eine Y-Achse links (für eine Metrik) und eine rechts (für die andere Metrik) haben. Diese Einstellung ist hilfreich, wenn grafisch dargestellte Metriken sehr unterschiedliche Größenordnungen aufweisen. |
| | Normalisierung (falls anwendbar) | Erzwingt Metriken für gleiche Anteile. Diese Einstellung ist hilfreich, wenn grafisch dargestellte Metriken sehr unterschiedliche Größenordnungen aufweisen. |
| | Y-Achse bei null verankern | Wenn alle im Diagramm dargestellten Werte deutlich über Null liegen, wird das untere Ende der Y-Achse durch die Standardeinstellung des Diagramms als NICHT-Null festgelegt. Ist dieses Ankreuzfeld markiert, wird die Y-Achse auf Null gesetzt (und das Diagramm wird neu gezeichnet). |
| | Skalierung der Y-Achse durch Anomalien zulassen | Wenn ein Diagramm mehrere Metriken enthält, bewegen Sie den Mauszeiger über die einzelnen Anomalien, damit das Konfidenzband für diese Metrik eingeblendet wird. Damit die Visualisierung besser lesbar ist, wird die Y-Achse nicht automatisch durch das Konfidenzintervall der Anomalieerkennung skaliert. Mit dieser Option kann die Visualisierung durch das Konfidenzintervall skaliert werden. <p>Weitere Informationen finden Sie unter [Anzeige von Anomalien in Analysis Workspace](/help/analyze/analysis-workspace/c-anomaly-detection/view-anomalies.md).</p> |
| **[Linie](/help/analyze/analysis-workspace/visualizations/line.md)** | | |
| | Prozentsatz | Zeigt in Linienvisualisierungen Werte in Prozentsätzen an. |
| | Legende sichtbar | Blenden Sie den detaillierten Legendentext für die Linienvisualisierung aus. |
| | Grenzwert für max. Anzahl von Elementen | Verringert die Anzahl der Elemente auf der X-Achse in der Linienvisualisierung. Diese Einstellung ist nützlich, wenn Sie über einen großen Datensatz verfügen. |
| | Zwei Achsen anzeigen (falls anwendbar) | Gilt nur, wenn Sie zwei Metriken haben - Sie können eine Y-Achse links (für eine Metrik) und eine rechts (für die andere Metrik) haben. Diese Einstellung ist hilfreich, wenn grafisch dargestellte Metriken sehr unterschiedliche Größenordnungen aufweisen. |
| | Normalisierung (falls anwendbar) | Erzwingt Metriken für gleiche Anteile. Diese Einstellung ist hilfreich, wenn grafisch dargestellte Metriken sehr unterschiedliche Größenordnungen aufweisen. |
| | X-Achse anzeigen | Zeigt die X-Achse im Liniendiagramm an. |
| | Y-Achse anzeigen | Zeigt die Y-Achse im Liniendiagramm an. |
| | Y-Achse verankern | Wenn alle im Diagramm dargestellten Werte deutlich über Null liegen, wird das untere Ende der Y-Achse durch die Standardeinstellung des Diagramms als NICHT-Null festgelegt. Ist dieses Ankreuzfeld markiert, wird die Y-Achse auf Null gesetzt (und das Diagramm wird neu gezeichnet). |
| | Min. anzeigen | Überlagern Sie eine Kennzeichnung für den Mindestwert ein, um die Täler einer Metrik schnell hervorzuheben. Hinweis: Die Minimalwerte werden von den sichtbaren Datenpunkten in der Visualisierung abgeleitet, nicht von dem vollständigen Satz von Werten innerhalb einer Dimension. |
| | Max. anzeigen | Überlagern Sie eine Kennzeichnung für den Maximalwert ein, um die Spitzen einer Metrik schnell hervorzuheben. Hinweis: Die Maximalwerte werden von den sichtbaren Datenpunkten in der Visualisierung abgeleitet, nicht von dem vollständigen Satz von Werten innerhalb einer Dimension. |
| | Trendlinie anzeigen | Zeigen Sie zu Ihrer Linienserie eine Regressions-Trendlinie oder eine Trendlinie mit angepasstem Durchschnittswert an. Trendlinien helfen, ein Muster in den Daten besser darzustellen. |
| **[Kohorte](/help/analyze/analysis-workspace/visualizations/cohort-table/t-cohort.md)** | | |
| | Granularität | Für Trend-Visualisierungen können Sie die Zeitgranularität ändern (Tag, Woche, Monat, Quartal oder Jahr). Diese Änderung gilt auch für die Datenquellentabelle. |
| | Nur Prozentwert anzeigen | Entfernt den Zahlenwert und zeigt nur den Prozentsatz an. |
| | Prozentwert auf nächste Ganzzahl runden | Rundet den Prozentwert auf den nächsten ganzzahligen Wert, anstatt den Dezimalwert anzuzeigen. |
| | Zeile mit durchschnittlichem Prozentwert anzeigen | Fügt oben in der Tabelle eine neue Zeile ein und fügt dann den Spaltendurchschnitt der Werte hinzu. |
| | Kohortenvorschau | Eine Vorschau davon, wie die Farbpalette in der Kohortenvisualisierung aussieht. |
| | Kohortenpalette | Die in der Kohortenvisualisierung verwendete Farbpalette. |
| **[Kombinationsdiagramme](/help/analyze/analysis-workspace/visualizations/combo-charts.md)** | | |
| | X-Achse anzeigen | Zeigt die X-Achse im Kombinationsdiagramm an. |
| | Y-Achse anzeigen | Zeigt die Y-Achse im Kombinationsdiagramm an. |
| | Hanteln auf Linien anzeigen | Zeigt Hanteln auf Linien im Kombinationsdiagramm. |
| **[Zusammenfassung einer Schlüsselmetrik](/help/analyze/analysis-workspace/visualizations/key-metric.md)** | | |
| | Zusammenfassung des Anzeigetyps | <ul><li>Prozentuale Veränderung hervorheben</li><li>Zahlenwert hervorheben</li></ul> |
| | Sparklines anzeigen | Liniendiagramme am unteren Rand des Diagramms anzeigen oder ausblenden. Wenn sie ausgeblendet sind, wird die Legende so geändert, dass sie keinen visuellen Bezug mehr zu den Linien hat. |
| | Max. und Min. auf Sparklines anzeigen | Einblenden von Minimal- und Maximalwerten in Primär- und Vergleichsliniendiagrammen. |
| | Vergleich anzeigen | Anzeigen von Vergleichsdaten. Wenn diese Option ausgeblendet ist, werden sowohl das Vergleichs-Liniendiagramm als auch die Zusammenfassungsänderung der Objekte ausgeblendet. |
| | Zahlenwert-Optionen | Im Abschnitt [!UICONTROL **Zusammenfassung der Schlüsselmetriken**] <ul><li>Prozentuale Veränderung anzeigen</li><li>Rohdifferenz anzeigen</li>Rohdifferenz zwischen dem Gesamtwert der Metrik im primären Datumsbereich und im sekundären Datumsbereich</ul> |
| **[Fallout](/help/analyze/analysis-workspace/visualizations/fallout/configuring-fallout.md)** | | |
| | Container | Zur Analyse der Besucherpfade zwischen Besuch und Besucher wechseln. Die Standardeinstellung lautet „Besucher“. Mithilfe dieser Einstellungen können Sie Einblicke in Besucheraktivitäten auf der Besucherebene (besuchsübergreifend) erhalten oder die Analyse auf einen einzelnen Besuch einschränken. <p>Die folgenden Optionen sind verfügbar:</p> <ul><li>Besuch</li><li>Besucher</li></ul> |
| **[Fluss](/help/analyze/analysis-workspace/visualizations/c-flow/create-flow.md)** | | |
| | Container | Im Abschnitt [!UICONTROL **Fluss**] <ul><li>Besuch</li><li>Besucher</li></ul> |
| | Beschriftungen umbrechen | Die Beschriftungen der Flusselemente werden üblicherweise aus Platzgründen auf dem Bildschirm abgeschnitten. Aktivieren Sie dieses Kontrollkästchen, um die gesamte Beschriftung anzuzeigen. Standard = deaktiviert. |
| | Wiederholungsinstanzen einschließen | Flussvisualisierungen basieren auf Instanzen einer Dimension. Diese Einstellung gibt Ihnen die Möglichkeit, wiederholte Instanzen ein- oder auszuschließen, z. B. Seitenneuladungen. Wiederholungen können jedoch nicht aus Flussvisualisierungen entfernt werden, die Dimensionen mit mehreren Werten enthalten, wie listVars, listProps, s.product, Merchandising-eVars usw. Standard = deaktiviert. |
| | QuickInfos anzeigen | Legt fest, ob QuickInfos mit Knotendaten angezeigt werden, wenn Sie den Mauszeiger über einzelne Knoten in einer Flussvisualisierung bewegen. |
| | Anzahl der Spalten | Gibt an, wie viele Spalten Sie in Ihrem Flussdiagramm anzeigen möchten. |
| | Erweiterte Elemente pro Spalte | Wie viele Elemente Sie in jeder Spalte anzeigen möchten. |
| **Stapeldiagramme** | | |
| | 100 % gestapelt | Mit dieser Einstellung für die Visualisierungen „Bereich gestapelt“, „Balken gestapelt“ und „Horizontalbalken gestapelt“ wandeln Sie Diagramme in „zu 100 % gestapelte“ Visualisierungen um. <p>Weitere Informationen finden Sie unter [Balken und gestapelte Balken](/help/analyze/analysis-workspace/visualizations/bar.md).</p> |
| **[Histogramm](/help/analyze/analysis-workspace/visualizations/histogram.md)** | | |
| | Anzahl der Buckets | Wählen Sie die Anzahl der Datenbereiche (Buckets) in der Visualisierung aus. Maximal 50 Buckets sind möglich. <p>Weitere Informationen finden Sie unter [Histogramm](/help/analyze/analysis-workspace/visualizations/histogram.md).</p> |
| | Zählmethode | Wählen Sie aus den folgenden Optionen: <ul><li>Treffer</li><li>Besuch</li><li>Besucher</li></ul> <p>Bei Verwendung mit Seitenansichten können Sie beispielsweise Seitenansichten pro Besucher, Seitenansichten pro Besuch oder Seitenansichten pro Treffer auswählen. Für Treffer wird in einer Freiformtabelle „Vorkommen“ als Metrik der Y-Achse verwendet.</p> |
| **[Zuordnung](/help/analyze/analysis-workspace/visualizations/map-visualization.md)** | | |
| | Plotting-Dimension | <ul><li>Breitengrad/Längengrad für Mobile</li><li>Geografische Dimension</li></ul> |
| | Zuordnungstyp | <ul><li>Blasen</li><li>Heatmap</li></ul> |
| | Farbschema | Wählen Sie aus Korallentönen, Rottönen, Grüntönen, Blautönen, Heatmap und Positiv/Negativ aus. |
| | Zuordnungsstil | Wählen Sie aus Einfach, Straßen, Hell, Licht, Dunkel und Satellit aus. |
| **[Änderung der Zusammenfassung](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)** | | |
| | Wert | <!-- Seem to be basically the same options as in "Number value options" --> <ul><li>Prozentuale Veränderung</li><li>Rohdifferenz</li></ul> |
| | Prozentsatz | Zeigt Werte in Prozent für die Visualisierungen der Zusammenfassungsänderung an. |
| | Legende sichtbar | Ermöglicht das Ausblenden des detaillierten Legendentextes für die Visualisierung der Zusammenfassungsänderung. |
| | Wert abkürzen | Wenn ausgewählt, geben Sie die Anzahl der Dezimalstellen an. |
| **[Zusammenfassungszahl](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)** | | |
| | Prozentsatz | Zeigt Werte in Prozent für die Visualisierungen der Zusammenfassungszahl an. |
| | Legende sichtbar | Ermöglicht das Ausblenden des detaillierten Legendentextes für die Visualisierung der Zusammenfassungszahl. |
| | Zusammenfassungswert nach | Wählen Sie aus „Max“, „Min“, „Mittel“, „Median“ und „Summe“ aus. |
| | Wert abkürzen | Wenn ausgewählt, geben Sie die Anzahl der Dezimalstellen an. |
| **[Treemap](/help/analyze/analysis-workspace/visualizations/treemap.md)** | | |
| | Prozentsatz | Zeigt für die Treemap-Visualisierungen Werte in Prozentsätzen an. |
| | Grenzwert für max. Anzahl von Elementen | Verringert die Anzahl der Elemente auf der X-Achse in der Treemap-Visualisierung. Dies kann bei großen Datensätzen nützlich sein. |
| **[Venn](/help/analyze/analysis-workspace/visualizations/venn.md)** | | |
| | Legende sichtbar | Ermöglicht das Ausblenden des detaillierten Legendentextes für die Venn-Visualisierung. |
| **[Streuung](/help/analyze/analysis-workspace/visualizations/scatterplot.md)** | | |
| | Prozentsatz | Zeigt Werte in Prozent für die Streuvisualisierungen an. |
| | Legende sichtbar | Ermöglicht das Ausblenden des detaillierten Legendentextes für die Streuvisualisierung. |
| | Grenzwert für max. Anzahl von Elementen | Verringert die Anzahl der Elemente auf der X-Achse in der Streuvisualisierung. Dies kann bei großen Datensätzen nützlich sein. |
| | Y-Achse bei null verankern | Wenn alle im Diagramm dargestellten Werte deutlich über Null liegen, wird das untere Ende der Y-Achse durch die Standardeinstellung des Diagramms als NICHT-Null festgelegt. Ist dieses Ankreuzfeld markiert, wird die Y-Achse auf Null gesetzt (und das Diagramm wird neu gezeichnet). |

## Standardeinstellungen wiederherstellen

Sie können alle Ihre Benutzervoreinstellungen auf die Systemstandardwerte zurücksetzen. Diese Option wirkt sich nicht auf die Administratoreinstellungen auf der Registerkarte **[!UICONTROL Unternehmen]** aus. Diese Aktion kann nicht rückgängig gemacht werden.

1. Wählen Sie in Adobe Analytics [!UICONTROL **Komponenten**] **>** [!UICONTROL **Voreinstellungen**] aus dem oberen Menü aus. Oder wählen Sie im Workspace-Menü **[!UICONTROL Projekt]** > **[!UICONTROL Benutzereinstellungen]** aus.

1. Wählen Sie oben rechts **[!UICONTROL Standardeinstellungen wiederherstellen]** aus.

1. Wählen Sie unter **[!UICONTROL Standardeinstellungen des Systems wiederherstellen]** die Option **[!UICONTROL Standardeinstellungen wiederherstellen]** aus. 

## [!UICONTROL Dunkles Design]

Wenn Sie einen dunklen Hintergrund für Ihre Customer Journey Analytics-Benutzeroberfläche bevorzugen, können Sie zu [!UICONTROL Dunkles Thema] wechseln.

1. Wählen Sie oben rechts das Experience Cloud-Benutzersymbol aus.

   ![dark-theme](assets/dark-theme.png)

1. Aktivieren Sie **[!UICONTROL Dunkles Design]**.

