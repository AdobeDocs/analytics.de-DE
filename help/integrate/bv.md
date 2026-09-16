---
title: Markensichtbarkeit-Integration
description: Integrieren von Markensichtbarkeit mit Adobe Analytics
feature:
role: User
source-git-commit: 841b09d487fb965fb2a5fce4a39a7480a5b01012
workflow-type: tm+mt
source-wordcount: '2637'
ht-degree: 1%
---

# Adobe Brand Visibility-Integration

[Adobe Brand Visibility](https://experienceleague.adobe.com/de/docs/llm-optimizer/using/home) ist eine generative KI-First-Anwendung für die Optimierung von generativen Modulen, die Marken dabei hilft, ihre Sichtbarkeit, Genauigkeit und ihren Einfluss in KI-gestützten Suchumgebungen zu verbessern. Markensichtbarkeit bietet Einblicke in das Markenpräsenz in KI-generierte Antworten, bietet präskriptive Inhaltsempfehlungen und automatisiert Optimierungskorrekturen.

KI ist zu einem primären Erkennungskanal geworden. Agenten für große Sprachmodelle (LLM) wie ChatGPT, Claude, Copilot und Perplexity crawlen Markeninhalte.

>[!NOTE]
>
>Markensichtbarkeit wurde früher als **LLM Optimizer (LLMO)**. In einigen Adobe-Dokumentationen wird während der Umstellung möglicherweise weiterhin die frühere LLMO-Terminologie verwendet.


>[!PREREQUISITES]
>
>Sie müssen über ein gebührenpflichtiges Markensichtbarkeit-Angebot verfügen, das über den verwalteten Connector bereitgestellt und mit Ihrer Experience Platform-Konfiguration verbunden ist.


>[!IMPORTANT]
>
>Im Rahmen dieser Integration findet in den Vereinigten Staaten eine zeitweilige Verarbeitung von Markensichtbarkeit-Daten statt. Die Daten werden letztendlich in der von Ihnen festgelegten Region gespeichert, wie in Ihrem Adobe Analytics-Vertrag konfiguriert.

Wenn Sie Customer Journey Analytics als separate, umfassendere eingehende Integration verwenden, landet dieselben zugrunde liegenden CDN-Traffic-Daten über Adobe Experience Platform in Customer Journey Analytics. Diese Integration ist heute verfügbar. Siehe Integration von [Markensichtbarkeit mit Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/integrations/bv). Wenn Sie über Customer Journey Analytics verfügen, überprüfen Sie zunächst diese Integration, da sie mehr Felder verfügbar macht und die Verknüpfung von Markensichtbarkeit-Daten mit anderen Datensätzen unterstützt. Die in diesem Handbuch beschriebene Analytics-Integration wurde für Kunden entwickelt, die Adobe Analytics verwenden, ohne Zugriff auf oder eine Lizenz für Customer Journey Analytics zu haben.


## Anwendungsfälle

Die Integration zwischen Adobe Analytics und Markensichtbarkeit bietet zwei Möglichkeiten:

* **Eingehende Integration**: Verwenden Sie Markensichtbarkeit-Daten in Adobe Analytics, um den LLM-gesteuerten Traffic (Bot-Crawler, RAG-Anfragen, Agentenaktivität) neben vorhandenen Web- und Mobildaten zu messen. Sie können zum Beispiel:

  * Messen Sie den LLM-gesteuerten Traffic anhand der Agentenquelle neben herkömmlichen Kanälen.

  * Identifizieren Sie Inhalte, die stark von LLMs genutzt werden, aber bei der menschlichen Konversion unterdurchschnittlich abschneiden.

  * Erkennen, wo LLM-Agent-Anforderungen über kritische Pfade hinweg fehlschlagen.

  * Vergleichen Sie die LLM-Bot-Nachfrage für eine Seite mit den Konversionen und dem Umsatz dieser Seite in Ihren Web-Daten, abgeglichen auf der URL- und Host-Ebene.

* **Ausgehende Integration**: Senden Sie Adobe Analytics-Leistungsdaten an Markensichtbarkeit, damit Sie die KI-Sichtbarkeit für die LLM-Quellen optimieren können, die Ihnen wertvollen Traffic senden, z. B. ChatGPT oder Perplexity. Sie können zum Beispiel:

  * Erfahren Sie, welche LLM-Quellen menschliche Besucher senden, die anschließend konvertieren oder Umsatz generieren. Adobe Analytics misst dies anhand des referenzierten Web-Traffics und nicht anhand des Bot-Datensatzes.
  * Ordnen Sie die LLM-Quellen nach dem nachgelagerten Wert der von ihnen gesendeten menschlichen Besucher. Konzentrieren Sie dann Ihre Arbeit mit der KI-Sichtbarkeit auf die Quellen, die die besten Ergebnisse erzielen.


## Eingehende Integration

In diesem Abschnitt werden die Voraussetzungen und Einrichtungsschritte für die eingehende Integration von **Adobe Brand Visibility → Adobe Analytics** beschrieben.


Der eingehende Adobe Analytics-Connector wird für jede Report Suite über den **Report Suite Manager** konfiguriert, wie in Abschnitt 6 beschrieben.

>[!PREREQUISITES]
>
>CDN-Zugriffsprotokolle müssen für jeden Markensichtbarkeit-Standort bereits an Adobe Brand Visibility weitergeleitet und von diesem empfangen werden, bevor der Markensichtbarkeit → Adobe Analytics Connector aktiviert werden kann.
>
>Diese Anforderung gilt für **pro Markensichtbarkeit-Site**. Es sollte nicht davon ausgegangen werden, dass eine CDN-Konfiguration oder ein Protokoll-Feed für eine Site, Domain oder Subdomain eine andere Site abdeckt, es sei denn, Adobe bestätigt diese Abdeckung.
>
>
>Bevor Sie den Connector aktivieren, bestätigen Sie:
>
>1. Die entsprechende CDN- oder Protokoll-Pipeline ist so konfiguriert, dass die erforderlichen Zugriffsprotokolle an das von Adobe bereitgestellte Ziel weitergeleitet werden.
>1. Markensichtbarkeit hat bestätigt, dass Protokolle für die jeweilige Website empfangen und erkannt werden.
>1. Die Daten sind in Ihrem Markensichtbarkeit-Agent-Traffic-Dashboard für diese Website sichtbar.
>
>Die BYOCDN-Protokollweiterleitung stellt die Server-seitigen CDN-Anfragedaten bereit, die für die Analyse von Agent-Traffic verwendet werden. Die Daten hängen nicht von JavaScript-Tags ab, die in einem Browser ausgeführt werden. Ohne den erforderlichen CDN-Protokoll-Feed verfügt der Connector über keine Traffic-Daten, die in Ihre Report Suite eingebracht werden können.
>
>Weitere Informationen finden [&#x200B; unter „BYOCDN](https://experienceleague.adobe.com/en/docs/brand-visibility/using/log-forwarding/log-forwarding-overview)Protokollweiterleitungsreferenz“.


>[!IMPORTANT]
>
>Im Rahmen dieser Integration findet in den Vereinigten Staaten eine zeitweilige Verarbeitung von Markensichtbarkeit-Daten statt. Die Daten werden letztendlich in der von Ihnen festgelegten Region gespeichert, wie in Ihrem Adobe Analytics-Vertrag konfiguriert.


### Funktionsweise

Die Integration der eingehenden Markensichtbarkeit → Adobe Analytics fügt Ihrer Report Suite eine Reihe **reservierter**&quot; hinzu. Diese Variablen enthalten zusammengefasste Daten über den Traffic von Bots und automatisierten Agenten, der auf Ihrer Website erkannt wird, einschließlich LLM-basiertem Traffic, der von denselben CDN-Zugriffsprotokollen bezogen wird, die unter [&#x200B; beschrieben &#x200B;](#inbound-integration).

Dieser Traffic führt im Allgemeinen keine Browser-JavaScript-Tags aus und wird nicht über Ihre bestehende Adobe Analytics-Implementierung erfasst. Die reservierten Variablen ermöglichen es Ihnen, diesen Traffic innerhalb derselben Report Suite anzuzeigen, die Sie bereits für Ihre Site verwenden.

Die folgenden reservierten Variablen werden hinzugefügt, wenn der Connector aktiviert ist:

| Gemeldet als | Typ | Anmerkungen |
|---|---|---|
| URL | Dimension | Die mit der Anfrage verknüpfte Seiten-URL. |
| Bot-Typ | Dimension | Der Typ des Bots oder automatisierten Agenten, der die Anfrage gestellt hat (z. B. eine benannte KI-Crawler). |
| Benutzeragent | Dimension | Die vom Bot oder Agenten gemeldete Benutzeragenten-Zeichenfolge. |
| Status | Dimension | Der für die Anfrage zurückgegebene HTTP-Status-Code. |
| Referrer | Dimension | Der HTTP-Referrer-Wert für die Anfrage, falls vorhanden. |
| Anfragen | Metrik | Die Anzahl der sowohl- als auch der Agent-CDN-Anfragen. |


#### Abdeckung im Vergleich zu Customer Journey Analytics

Die CJA Inbound-Integration basiert auf einem umfassenderen CDN-Anfrage-Zusammenfassungsdatensatz und unterstützt zusätzliche Felder (z. B. Host und CDN-Provider) sowie die Verknüpfung mit anderen Datensätzen in Customer Journey Analytics. Die Adobe Analytics-Integration ist ein kleinerer, Report Suite-nativer Satz reservierter Variablen, die für die Verwendung im vorhandenen Datenmodell von Analytics entwickelt wurden. Wenn Ihre Reporting-Anforderungen über die oben aufgeführten Felder hinausgehen, sollten Sie die CJA-Integration bewerten.

#### Wichtige Einschränkungen

&#x200B;- Es sind keine Besucher-ID, ECID, Besuche oder Unique-User-Daten enthalten. Dies sind aggregierte, nicht besuchergebundene Zusammenfassungsdaten.
&#x200B;- Die reservierten Variablen unterstützen keine Einstellungen für den Zuordnungstyp oder den Ablauftyp, da sie nicht an einen Besucher gebunden sind.
&#x200B;- Daten können nicht auf dieselbe Weise mit anderen Analytics-Datensätzen oder -Dimensionen verbunden werden wie in Customer Journey Analytics.
&#x200B;- Verwenden Sie die Metrik **Anfragen**, um das sowohl- als auch das agentische Traffic-Volumen zu messen. Verwenden Sie sie nicht austauschbar mit besuchs- oder trefferbasierten Metriken an anderer Stelle in Ihrer Report Suite.

Der genaue Satz der verfügbaren Felder sollte hinsichtlich der Variablenkonfiguration Ihrer Report Suite bestätigt werden, nachdem der Connector aktiviert wurde.

### Zuständigkeiten

Die Einrichtung und Konfiguration des eingehenden Connectors geht mit Zuständigkeiten sowohl für [Adobe](#adobe-managed-responsibilities) als auch für [Sie als Kunde“ &#x200B;](#customer-owned-responsibilities).

#### Von Adobe verwaltete Zuständigkeiten

1. Erkennt und bestätigt CDN-Protokollweiterleitung für jede integrierte Markensichtbarkeit-Site.
2. Stellt die reservierten Variablen für die Bereitstellung zur Verfügung, sobald die BYOCDN-Protokollweiterleitung bestätigt wurde.
3. Führt die 90-tägige Aufstockung und laufende stündliche Synchronisierung aus, sobald der Connector für eine Report Suite aktiviert ist.

#### Eigene Zuständigkeiten des Kunden

1. Abschließen des Markensichtbarkeit-Onboarding und der BYOCDN-Protokollweiterleitung für jede Website.
2. Vor der Aktivierung des Connectors wird im Dashboard des Markensichtbarkeit-Agent-Traffics bestätigt, dass Daten angezeigt werden.
3. Auswählen der Report Suite, mit der jede Markensichtbarkeit-Site eine Verbindung herstellt (eine Site pro Report Suite).
4. Aktivieren des Connectors über Report Suite Manager.
5. Erstellen von Berichten, Segmenten oder Datenansichten (falls zutreffend), die die unter „Funktionsweise[&#x200B; aufgelisteten reservierten Variablen &#x200B;](#how-it-works).

### Vorbereitung

Bestätigen Sie Folgendes, bevor Sie den Connector aktivieren:

&#x200B;- Sie haben das Adobe Brand Visibility-Onboarding für die Site abgeschlossen, zu der Sie eine Verbindung herstellen möchten.
&#x200B;- Die BYOCDN-Protokollweiterleitung ist für diese Website eingerichtet und bestätigt (siehe [Voraussetzungen](#inbound-integration)).
&#x200B;- Daten werden in Ihrem Adobe Brand Visibility Agent Traffic-Dashboard für diese Website angezeigt.
&#x200B;- Sie wissen, mit welcher Report Suite Sie die Site verbinden möchten.

Jede Adobe Brand Visibility-Site ist mit genau einer Report Suite verbunden. Wenn Sie Daten für mehr als eine Markensichtbarkeit-Site importieren möchten, verbinden Sie jede Site mit einer separaten Report Suite.


### Aktivieren des Connectors

Der Connector wird über das Menü **Einstellungen bearbeiten** der Report Suite ein- und ausgeschaltet.

So öffnen Sie die Adobe Brand Visibility-Einstellungen für Ihre Report Suite:

1. Melden Sie sich bei Adobe Analytics an.
1. Navigieren Sie **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Wählen Sie die Report Suite aus, die Sie verbinden möchten.
1. Wählen Sie **[!UICONTROL Einstellungen bearbeiten]** aus.
1. Wählen Sie im Kontextmenü **[!UICONTROL Adobe Brand Visibility]** aus.

So stellen Sie den Connector bereit:

1. Wählen Sie **Adobe Brand Visibility Data Connector bereitstellen** aus.
1. Überprüfen Sie die Dimensionen und Metriken, die dieser Report Suite hinzugefügt werden (aufgeführt in [Funktionsweise](#how-it-works)).
1. Wählen **unter &quot;Adobe Brand Visibility-Site auswählen** die Site aus, mit der diese Report Suite verbunden werden soll. Sobald die Verbindung hergestellt ist, werden die Zusammenfassungsdaten der Site stündlich mit dieser Report Suite synchronisiert.
1. Wählen Sie **Aktivieren** aus.

   Nach der Aktivierung können diese Variablen nicht mehr aus dieser Report Suite entfernt werden. Durch Aktivierung des Connectors wird eine 90-tägige Aufstockung gestartet, wobei die Adobe Brand Visibility-Daten der letzten 90 Tage in diese Report Suite importiert werden.

   Bevor Sie den Connector aktivieren, überprüfen Sie, ob Sie die unter [Bevor Sie beginnen](#before-you-start) beschriebenen Schritte ausgeführt haben. Dazu gehört auch die Überprüfung, ob die Daten bereits in Ihrem Adobe Brand Visibility Agent-Traffic-Dashboard angezeigt werden.

Warten Sie nach der Aktivierung des Connectors, bis die erste Aufstockung und die erste stündliche Synchronisierung abgeschlossen sind. Bestätigen Sie dann, dass die unter [Funktionsweise“ erwähnten reservierten Variablen &#x200B;](#how-it-works) Ihre Report Suite eingefügt wurden. Siehe Abschnitt 8, Schritt 3).

### Deaktivieren des Connectors

>[!WARNING]
>
>Die Deaktivierung des Connectors **nicht rückgängig gemacht**. Durch Deaktivieren wird die stündliche Synchronisierung gestoppt und historische Adobe Brand Visibility-Daten für diese Report Suite gelöscht.

Deaktivieren des Connectors:

1. Navigieren Sie **Admin → Report Suites → Einstellungen → Adobe Brand Visibility bearbeiten**.
1. Wählen Sie **Bereitstellung von Adobe Brand Visibility Data Connector aufheben** aus.
1. Bestätigen Sie, dass Sie die aufgelistete Adobe Brand Visibility-Site trennen möchten.
1. Wählen Sie **Deaktivieren** aus.
1. Bestätigen Sie die Warnung zur Bestätigung.

Wenn Sie das Reporting nur vorübergehend anhalten möchten, deaktivieren Sie den Connector nicht. Wenden Sie sich an Ihr Adobe-Accountteam, um Optionen zum Anhalten von Berichten vor der Deaktivierung zu besprechen.

### Abschlusskriterien einrichten

Die eingehende Integration ist für das Reporting bereit, wenn alles Folgende bestätigt wird:

* CDN-Protokolle werden an Adobe Brand Visibility für die Site weitergeleitet und von diesem empfangen.
* Die Daten werden im Adobe Brand Visibility Agent Traffic-Dashboard der Site angezeigt.
* Der Connector wurde für die vorgesehene Report Suite über Report Suite Manager aktiviert.
* Die anfängliche Aufstockung und mindestens eine stündliche Synchronisierung wurden abgeschlossen.
* Die reservierten Variablen in Abschnitt 4 geben beim Reporting die erwarteten Werte zurück.

### Überprüfungsverfahren

Das Prüfverfahren umfasst die folgenden Schritte:

1. Bestätigen der Bereitschaft für Markensichtbarkeit-Site und CDN-Protokoll:

   * Bestätigen Sie die Website bzw. Domain, zu der Sie eine Verbindung herstellen möchten.
   * Bestätigen Sie, dass CDN-Protokolle für diese Site weitergeleitet werden und dass der Empfang durch die Markensichtbarkeit bestätigt wurde.
   * Bestätigen Sie, dass die Daten im Dashboard des Agentenverkehrs für diese Website sichtbar sind.

1. Bestätigen Sie, dass der Connector aktiviert ist:

   1. Gehen Sie **Admin → Report Suites → Einstellungen → Adobe Brand Visibility bearbeiten** für die Ziel-Report Suite.
   1. Bestätigen Sie, dass auf der Seite der Connector als aktiviert angezeigt wird und die verbundene Markensichtbarkeit-Site aufgeführt wird.

1. Bestätigen von Daten im Reporting:

   1. Öffnen Sie Analysis Workspace (oder Ihren standardmäßigen Reporting-Workflow) für die verbundene Report Suite.
   1. Erstellen Sie eine Tabelle oder Visualisierung mithilfe der Metrik **Anfragen** aufgeschlüsselt nach **Bot-Typ**.
   1. Das angefragte Volumen für einen aktuellen Datumsbereich wird angezeigt.
   1. Bestätigen Sie, **die Dimensionen** URL **, Benutzeragent**, **Status** und **Referer** erwartete Werte zurückgeben.

   Der genaue Zeitraum, der für das Anzeigen von Daten erforderlich ist, hängt vom Aufstockungs- und Synchronisierungszeitplan ab, der unter [Aktivieren des Connectors](#enable-the-connector) beschrieben ist.



### Fehlerbehebung

Informationen zu den folgenden Problemen und deren Behebung finden Sie unter.

| Problem | Fehlerbehebung |
|---|---|
| Der Connector wird nicht aktiviert oder die Site-Liste ist leer. | Prüfen, ob:<ul><li>Das Onboarding von Adobe Brand Visibility für die Site ist abgeschlossen.</li><li>Die BYOCDN-Protokollweiterleitung ist für die Site konfiguriert und bestätigt.</li><li>Sie arbeiten mit der richtigen Report Suite.</li><ul> |
| Der Connector ist aktiviert, es werden jedoch keine Daten angezeigt. | Prüfen, ob: <ul><li>Daten werden im Dashboard des Agentenverkehrs für die verbundene Website angezeigt (andernfalls liegt das Problem vor Analytics).</li><li>Es ist genügend Zeit für die anfängliche 90-tägige Aufstockung und mindestens eine stündliche Synchronisierung verstrichen.</li><li>- Der ausgewählte Datumsbereich in Ihrem Bericht enthält einen Zeitraum, nach dem der Connector aktiviert wurde.</li></ul> |
| Die Daten erscheinen unvollständig oder unerwartet. | Prüfen, ob: <ul><li>Es wird nicht erwartet, dass die Report Suite Daten für eine andere Markensichtbarkeit-Site erhält (jede Report Suite stellt eine Verbindung zu genau einer Site her).</li><li>Sie lesen die Metrik **Anfragen** anstatt Zeilen oder Treffer an anderer Stelle in der Report Suite zu zählen.</li><li>Die angezeigten Dimensionen entsprechen der Liste in Abschnitt 4. Nicht verwandte eVars oder Ereignisse in derselben Report Suite sind nicht Teil dieser Integration.</li></ul> |

>[!MORELIKETHIS]
>
>[Markensichtbarkeit/LLMO-Integrationsreferenz](https://experienceleague.adobe.com/en/docs/analytics-platform/using/integrations/bv)
>[Referenz zur BYOCDN-Protokollweiterleitung](https://experienceleague.adobe.com/en/docs/brand-visibility/using/log-forwarding/log-forwarding-overview)

&#x200B;---

## Entwurfsnotizen für Dokumente (nicht zu veröffentlichen)

Dieser Abschnitt dient der internen Überprüfung und sollte vor der Veröffentlichung entfernt werden.

&#x200B;- **Verwendete Source der Wahrheit:** Feldnamen, die Liste der reservierten Variablen und der Report Suite Manager-Workflow stammen aus [AN-468884](https://jira.corp.adobe.com/browse/AN-468884) (David Wardell, Status Neu ab 2026-08-28), das aktueller und spezifischer ist als die ursprüngliche Dokumentationsanfrage [AN-449989](https://jira.corp.adobe.com/browse/AN-449989) (Rob In der Maur, Status Neu). Die Seitenkopie für die Bildschirme „Bereitstellung/Aufhebung der Bereitstellung“ enthält die Wortverfeinerungen aus der internen Überprüfung 2026-08-28 (`2026-08-28-an468884-abv-report-suite-ui-review.md`), die die Abkürzung „ABV“ des unformatierten Tickets im kundenorientierten Text durch &quot;Adobe Brand Visibility&quot; ersetzt hat.
&#x200B;- **Feldsatzdiskrepanz, die vor der Veröffentlichung abgeglichen werden muss:** Die ursprüngliche Dimensionsliste von AN-449989 war Host, URL/Seitenpfad, CDN-Provider, Benutzeragent und LLM-Bot-Typ mit einer einzigen Metrik für die Anzahl der Agentenanfragen. Die tatsächliche Liste der reservierten Variablen von AN-468884 ist URL, Bot-Typ, Benutzeragent, Status und Referer mit einem einzigen Anforderungsereignis. Host und CDN-Anbieter sind in AN-468884 nicht als separate reservierte Variablen vorhanden. Status ist neu. Dieser Entwurf folgt an-468884 als autoritär gemäß dem eng-Ticket, aber die beiden sollten mit Aaron Kern / David Wardell abgestimmt werden, bevor dies finalisiert wird, da die Feldnamen, die Kunden sehen, möglicherweise nicht mit dem übereinstimmen, was Account-Teams in der älteren AN-449989-Sprache beschrieben haben.
&#x200B;- **Noch nicht bestätigt, geben Sie in der veröffentlichten Version nicht als Tatsache an:**
  &#x200B;- Exaktes GA-Datum. AN-431416 verfügt über FixVersion H2 2026 (Versionsfenster 2026-11-30) und befindet sich ab dem 01.09.2026 im Ausführungsstatus. AN-468884 (die Implementierung der reservierten Variablen) und AN-449989 (dieses Dokument) sind beide noch neu. Veröffentlichen Sie erst, wenn es ausgeliefert wird.
  &#x200B;- Ob Zuordnungstyp/Ablauftyp für die reservierten eVars in der Produktion vollständig unterdrückt sind. Die Überprüfung 2026-08-28 hat ergeben, dass eine Test-Report-Suite diese eVars derzeit anzeigt, wobei die Zuordnung auf „Zuletzt verwendet (Letzte)“ festgelegt ist. Dies kann eine Standardeinstellung sein, die gelöscht werden muss, anstatt das endgültige Verhalten zu bestätigen.
  &#x200B;- Der LLMO-API-Endpunkt für die Auflistung von ABV-Sites nach IMS-Organisation (füllt das Dropdown-Menü zur Site-Auswahl aus) und die API zum Aufheben der Bereitstellung/Deaktivieren standen zum Zeitpunkt des Ticketkommentars 2026/08/26 noch aus.
  &#x200B;- Der exakte Vergleich der Anzahl der CJA-Felder. Das ursprüngliche Ticket von AN-449989 besagt, dass CJA „9 zusätzliche Dimensionen“ und „5 zusätzliche Metriken“ hat, aber einige davon (LLM-Sitzungs-Bucket, LLM-Anzahl eindeutiger Sitzungen, LLM-Anzahl der Anforderungsduplikate) wurden zum Zeitpunkt der Überprüfung 2026-06-18 nicht bestätigt, dass sie in der Feldergruppe der bereitgestellten `cdn-requests-summary` vorhanden sind. In diesem Entwurf wird aus diesem Grund bewusst vermieden, bestimmte Zählungen im CJA-Vergleich anzugeben.
  &#x200B;- Die Synchronisierungskadenz für diesen AA-Pfad wird hier als stündlich angegeben, entsprechend der Ticketsprache von AN-468884 („stündliche Synchronisierungen ausführen“ / „stündlicher Synchronisierungsprozess„). Dies wurde nicht unabhängig anhand des Verhaltens von Data Sources in Produktions-AA auf die gleiche Weise wie die CJA-Kadenz validiert.


## Ausgehende Integration

Dieses Handbuch behandelt nur die Integration eingehender Markensichtbarkeit, durch die Traffic-Daten von Bots und automatisierten Agenten zu einer Analytics Report Suite hinzugefügt werden. In der veröffentlichten Integrationsdokumentation wird auch eine Richtung für den Ausgang beschrieben, in der Analytics-Leistungsdaten für das Markensichtbarkeit innerhalb des Markensichtbarkeit-Produkts verfügbar gemacht werden. Diese Richtung liegt außerhalb des Rahmens dieses Handbuchs. Weitere Informationen zur ausgehenden Integration finden [&#128279;](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/adobe-analytics-integration) in der Markensichtbarkeit-Dokumentation.