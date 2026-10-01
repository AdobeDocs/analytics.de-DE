---
description: Die Custom Insight-Konversionsvariable (oder eVar) wird auf ausgewählten Web-Seiten Ihrer Site in den Adobe-Code platziert. Ihr Hauptzweck besteht darin, Konversionserfolgsmetriken in benutzerspezifischen Marketing-Berichten zu segmentieren. Eine eVar kann besuchsbasiert sein und ähnlich wie Cookies funktionieren. In eVar-Variablen übergebene Werte folgen den Benutzenden für einen bestimmten Zeitraum.
keywords: eVar
title: Konversionsvariablen (eVar)
feature: Admin Tools
role: Admin
exl-id: 822ecaff-a06c-42e1-aee8-ef4a43df4230
TQID: https://experienceleague.adobe.com/rYLxVYB1oDyfEk8gQyesTSRRPHid-6zJ8QaqFG2b0Kc
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
    internal-label: Admin Tools
subfeature_v2:
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
    internal-label: Events
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: ca917b867cd84b09b899ce7b72586f0b15003106
workflow-type: tm+mt
source-wordcount: '1726'
ht-degree: 27%
---
# Konversionsvariablen (eVars)

Die Custom Insight-Konversionsvariable (oder eVar) wird auf ausgewählten Web-Seiten Ihrer Site in den Adobe-Code platziert. Ihr Hauptzweck besteht darin, Konversionserfolgsmetriken in benutzerspezifischen Marketing-Berichten zu segmentieren. Eine eVar kann besuchsbasiert sein und ähnlich wie Cookies funktionieren. In eVar-Variablen übergebene Werte folgen den Benutzenden für einen bestimmten Zeitraum.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Konversion]** > **[!UICONTROL Konversionsvariablen]**

## Konversionsvariablen (eVars) – Überblick

Eine Videoübersicht zu Konversionsvariablen finden Sie unter [Einführung in Konversionsvariablen](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/analysis-workspace/dimensions/introduction-to-conversion-variables-evars) im Handbuch Analytics-Tutorials .

Wenn eine eVar auf einen Wert für eine Besucherin oder einen Besucher festgelegt ist, speichert Adobe diesen Wert automatisch bis zu seinem Ablauf. Alle Erfolgsereignisse, auf die eine Besucherin oder ein Besucher trifft, während der eVar-Wert aktiv ist, werden für den eVar-Wert gezählt.

eVars werden am besten verwendet, um Ursache und Wirkung zu messen, z. B.:

* Welche internen Kampagnen den Umsatz beeinflusst haben
* Welche Bannerwerbung letztendlich zu einer Registrierung führte
* Die Häufigkeit, mit der eine interne Suche vor der Bestellung verwendet wurde

Wenn Traffic-Messungen oder -Pfade gewünscht werden, wird die Verwendung von Traffic-Variablen empfohlen.

>[!NOTE]
>
>Nur ein einzelner Wert kann bei einer Bildanforderung in einer eVar gespeichert werden. Wenn ein eVar-Wert mehrere Werte enthalten soll, verwenden Sie [Listenvariablen](/help/implement/vars/page-vars/page-variables.md).

### Konversionsvariablen – Beschreibungen {#section_7C317BB0287A4B8EB0A1A4ECC40627BF}

| Element | Beschreibung |
| --- | --- |
| [!UICONTROL Status] | Legt fest, ob die eVar aktiv ist:<ul><li>**[!UICONTROL Aktiviert]**: Die eVar ist aktiv.</li><li>**[!UICONTROL Deaktiviert]**: Deaktiviert die eVar und entfernt sie aus der Liste der Konversionsvariablen.</li></ul> |
| [!UICONTROL Beschreibung] | Eine optionale Beschreibung der eVar. Verwenden Sie sie, um zu dokumentieren, was die eVar erfasst und wie sie implementiert wird. |
| [!UICONTROL Name] | Der Anzeigename der Dimension der Konversionsvariablen. So wird der eVar in allgemeinen Berichten bezeichnet. |
| [!UICONTROL Zuordnung] | Legt fest, wie in Analytics Gutschriften für ein Erfolgsereignis zugewiesen werden, wenn eine Variable mehrere Werte vor dem Ereignis erhält. Folgende Werte werden unterstützt:<ul><li>**[!UICONTROL Zuletzt verwendet (Letzte)]**: Erfolgsereignisse werden immer dem letzten eVar-Wert zugeschrieben, bis dieser eVar abläuft.</li><li>**[!UICONTROL Ausgangswert (Erste)]**: Erfolgsereignisse werden immer dem ersten eVar gutgeschrieben, bis dieser eVar abläuft.</li><li>**[!UICONTROL Linear]**: Weist Erfolgsereignisse gleichmäßig allen eVar-Werten zu. Da bei der linearen Zuordnung Werte nur innerhalb eines Besuchs verteilt werden, sollten Sie die lineare Zuordnung mit einem eVar-Ablauf von „Besuch“ oder weniger verwenden. Diese Option ist nicht für Merchandising-eVars verfügbar.</li></ul>**Wichtig**: Adobe rät davon ab, zur oder von [!UICONTROL linearen] Zuordnung zu wechseln, da historische Daten in Berichten ausgeblendet werden, bis Sie zurückwechseln. Wenn Sie die Zuordnung für eine eVar mit einem signifikanten Verlauf ändern möchten, empfiehlt Adobe, stattdessen eine neue eVar zu verwenden. |
| [!UICONTROL Läuft ab nach] | Gibt an, wann der eVar-Wert abläuft (erhält keine Gutschrift mehr für Erfolgsereignisse). Falls nach Ablauf der eVar (d. h. wenn keine eVar aktiv ist) ein Erfolgsereignis eintritt, wird das Ereignis dem Wert „Keine“ gutgeschrieben. Folgende Werte werden unterstützt:<ul><li>**[!UICONTROL Besuch]**: Der Wert läuft am Ende des Besuchs ab.</li><li>**[!UICONTROL Treffer]**: Der Wert gilt nur für den Treffer, für den er festgelegt wurde.</li><li>**[!UICONTROL Minute]**, **[!UICONTROL Stunde]**, **[!UICONTROL Tag]**, **[!UICONTROL Woche]**, **[!UICONTROL Monat]**, **[!UICONTROL Quartal]** oder **[!UICONTROL Jahr]**: Der Wert läuft nach seiner Einstellung eine feste Zeitspanne ab, bis zur Sekunde:<ul><li>Minute = 60 Sekunden</li><li>Stunde = 3600 Sekunden (60 Minuten)</li><li>Tag = 86400 Sekunden (24 Stunden)</li><li>Woche = 604800 Sekunden (7 Tage)</li><li>Monat = 2678400 Sekunden (31 Tage)</li><li>Quartal = 8035200 Sekunden (93 Tage - 3 Monate mit 31 Tagen)</li><li>Jahr = 31536000 Sekunden (365 Tage)</li></ul>Wenn ein eVar beispielsweise am Montag um 7:15 Uhr festgelegt wird, endet die Gültigkeit [!UICONTROL Tag] am Dienstag um 7:15 Uhr, die Gültigkeit [!UICONTROL Woche] [!UICONTROL  endet am darauf folgenden Montag um 7:15 Uhr und die ] um 31 Tage später um 7:15 Uhr.</li><li>**[!UICONTROL Benutzerdefiniert]**: Der Wert läuft nach der Anzahl der Tage ab, die Sie eingeben (86400 Sekunden pro Tag).</li><li>**Ereignis** ([!UICONTROL Kauf], [!UICONTROL Produktansicht], [!UICONTROL Warenkorb geöffnet], [!UICONTROL Warenkorb-Kasse], [!UICONTROL Warenkorb hinzufügen], [!UICONTROL Warenkorb entfernen], [!UICONTROL Warenkorbansicht] oder ein benutzerspezifisches Ereignis): Der Wert läuft ab, wenn das ausgewählte Ereignis eintritt. Wenn das Ereignis nie auftritt, läuft der Wert nie ab.</li><li>**[!UICONTROL Nie]**: Solange ein Besucher dieselbe Kennung verwendet, kann ein beliebiger Zeitraum zwischen der eVar und dem Ereignis verstreichen.</li></ul> |
| [!UICONTROL Typ] | Der Typ des Variablenwerts:<ul><li>**[!UICONTROL Text-String]**: Erfasst Textwerte. Dies ist der häufigste Typ von eVar und die Standardeinstellung. Es verhält sich ähnlich wie andere Variablen, wobei der darin enthaltene Wert eine statische Textzeichenfolge ist. Wenn Sie Dinge wie interne Kampagnen oder interne Suchbegriffe verfolgen, wird diese Einstellung empfohlen.</li><li>**[!UICONTROL Zähler]**: Zählt, wie oft eine Aktion stattfindet, bevor sie zum Erfolg führt. Sie können beispielsweise die Anzahl der durchgeführten Suchen unabhängig von den verwendeten Suchbegriffen vor einem Erfolgsereignis zählen.</li></ul> |
| [!UICONTROL Zurücksetzen] | Beim Speichern laufen alle Server-seitigen persistierten Werte für diese Variable für alle Besucher sofort ab, einschließlich der Merchandising-Produktbindungen. Verwenden Sie [!UICONTROL Zurücksetzen] wenn Sie eine eVar neu verwenden, damit kein alter Wert in einen neuen Bericht gemischt wird. **Durch das Zurücksetzen werden keine historischen Daten gelöscht.** |
| [!UICONTROL Merchandising aktivieren] | Folgende Werte werden unterstützt:<ul><li>**[!UICONTROL Deaktiviert]**: Die eVar schreibt Erfolgsereignisse dem Wert zu, der für den Besucher beibehalten wird.</li><li>**[!UICONTROL Aktiviert]**: Die eVar wird zu einer Merchandising-eVar, die Werte an einzelne Produkte bindet. Erfolgsereignisse für jedes Produkt werden dem Wert gutgeschrieben, der an dieses Produkt gebunden ist. Durch die Aktivierung des Merchandisings werden die Einstellungen [!UICONTROL Merchandising] und [!UICONTROL Merchandising-Binding-Ereignis] angezeigt und die Zuordnung [!UICONTROL Linear] entfernt.</li></ul>Aktivieren Sie Merchandising nur für eVars, die beschreiben, wie Produkte gefunden oder gekauft werden. Eine Merchandising-eVar schreibt keine Erfolgsereignisse mehr zu, die nicht an ein Produkt gebunden sind. Siehe [eVar (Merchandising)](/help/components/dimensions/evar-merchandising.md). |
| [!UICONTROL Merchandising] | Bestimmt, woher der Wert für die Bindung an Produkte stammt:<ul><li>**[!UICONTROL Produktsyntax]**: Der Wert wird für jedes Produkt in der Variablen &quot;`products`&quot; festgelegt und bei diesem Treffer an dieses Produkt gebunden. Jedes Produkt kann einen anderen Wert haben. Binding-Ereignisse werden nicht verwendet, daher [!UICONTROL Merchandising-Binding-]) deaktiviert.</li><li>**[!UICONTROL Konversionsvariablensyntax]**: Der Wert wird in der eVar selbst festgelegt und bleibt als gestaffelter Wert bestehen, wobei immer der neueste Wert widergespiegelt wird, der unabhängig von der [!UICONTROL  gesendet wurde]. Der Wert wird nur dann an die Produkte in einem Treffer gebunden, wenn dieser Treffer ein ausgewähltes [!UICONTROL Merchandising-Binding-Ereignis“ ]. Jedes Produkt in diesem Treffer erhält denselben Wert.</li></ul>Wenn Sie diese Einstellung ändern, ohne die Implementierung entsprechend zu aktualisieren, gehen Daten verloren. Siehe [eVar (Merchandising-Variable)](/help/implement/vars/page-vars/evar-merchandising.md) für Implementierungsdetails. |
| [!UICONTROL Merchandising-Binding-Ereignis] | Nur verfügbar, wenn [!UICONTROL Merchandising] auf „Konversionsvariablensyntax[!UICONTROL  festgelegt ]. Bestimmt, welche Ereignisse oder eVars den Staging-Wert von eVar an die Produkte im selben Treffer binden. Wenn Sie kein Binding-Ereignis auswählen, wird [!UICONTROL Alle] verwendet. Folgende Werte werden unterstützt:<ul><li>**[!UICONTROL Alle]**: Jedes andere Ereignis oder jede andere eVar für die Trefferereignis-Trigger-Bindung. Diese Einstellung ist die Standardeinstellung.</li><li>**[!UICONTROL Kaufereignis]**, **[!UICONTROL Produktansichtsereignis]**, **[!UICONTROL Warenkorböffnungs-Ereignis]**, **[!UICONTROL Warenkorb-Checkout-Ereignis]**, **[!UICONTROL Warenkorbhinzufügungs-Ereignis]**, **[!UICONTROL Warenkorbentfernung-Ereignis]** oder **[!UICONTROL Warenkorbansichtsereignis]**: Bindung erfolgt bei Treffern, die das ausgewählte Ereignis enthalten.</li><li>**[!UICONTROL Kampagnenereignis]**: Die Bindung erfolgt bei Treffern, die eine Instanz der Dimension [Trackingcode](/help/components/dimensions/tracking-code.md) ([`campaign`](/help/implement/vars/page-vars/campaign.md)) enthalten.</li><li>**Benutzerspezifisches Ereignis**: Die Bindung erfolgt bei Treffern, die das ausgewählte benutzerspezifische Ereignis enthalten.</li><li>**Eine benutzerdefinierte eVar**: Die Bindung erfolgt bei Treffern, die die ausgewählte eVar festlegen.</li></ul>Props können keine Trigger-Bindung herstellen. Sie können mehrere Werte auswählen, indem Sie die Strg-Taste (Windows) bzw. die Befehlstaste (Mac) gedrückt halten und auf mehrere Elemente in der Liste klicken. Wenn ein bestimmtes Produkt, das bereits an eine eVar gebunden ist, eine andere Bindung mit derselben eVar erhält, bestimmt [!UICONTROL Zuordnung] welcher Wert beibehalten wird. |

### Gültigkeit

`eVars` laufen nach dem von Ihnen festgelegten Zeitraum ab. Nach dem Ablauf werden in der eVar keine Erfolgsereignisse mehr gezählt. eVars können auch so konfiguriert werden, dass sie bei Erfolgsereignissen ablaufen. Wenn beispielsweise eine interne Promotion am Ende eines Besuchs abläuft, werden der internen Promotion nur Käufe oder Registrierungen gutgeschrieben, die während des Besuchs stattfinden, bei dem sie aktiviert wurde.

Es gibt zwei Möglichkeiten, eine eVar ablaufen zu lassen:

* Sie können die eVar so einstellen, dass sie nach einem bestimmten Zeitraum oder Ereignis abläuft.
* Sie können den Ablauf einer eVar erzwingen, indem Sie sie zurücksetzen. Dies ist nützlich, wenn Sie eine Variable für andere Zwecke verwenden.

Wenn Sie beispielsweise den Ablauf einer eVar von 30 auf 90 Tage ändern, bleiben die erfassten eVar-Werte für die Dauer des neu eingestellten Ablaufzeitraums (in diesem Fall 90 Tage) erhalten. Das System prüft lediglich die aktuelle Ablaufeinstellung und den letzten festgelegten Zeitstempel des erfassten eVar-Werts, um den Ablauf zu bestimmen. Nur die Option **[!UICONTROL Zurücksetzen]** bewirkt ein unmittelbares Ablaufen von Werten.

Ein weiteres Beispiel: Wenn eine eVar im Mai dazu dienen soll, interne Werbeaktionen widerzuspiegeln (wobei sie nach 21 Tagen ablaufen soll) und im Juni dann eingesetzt wird, um interne Keywords zu erfassen, müssen Sie am 1. Juni ihren Ablauf erzwingen oder die Variable zurücksetzen. So verhindern Sie, dass die Werte zu der internen Werbeaktion vom Mai nicht im Bericht vom Juni auftauchen.

### Groß-/Kleinschreibung

Bei eVars wird nicht zwischen Groß- und Kleinschreibung unterschieden. Die Groß- oder Kleinschreibung, die für das Reporting verwendet wird, basiert auf dem ersten Wert, den das Backend-System registriert. Dieser Wert kann entweder die erste jemals erkannte Instanz sein oder je nach Zeitraum (z. B. monatlich) variieren, je nach der Vielfalt und Menge der mit der Report Suite verknüpften Daten.

### Zähler

eVars werden zwar meistens zum Speichern von Zeichenfolgenwerten verwendet, können aber auch so konfiguriert werden, dass sie als Zähler dienen. eVars sind nützlich als Zähler, wenn Sie versuchen, die Anzahl der Aktionen zu zählen, die eine Benutzerin oder ein Benutzer vor einem Ereignis ausführt. So können Sie eine eVar beispielsweise einsetzen, um die Anzahl der internen Suchvorgänge vor einem Kauf zu zählen. Bei jeder Suche sollte die eVar den Wert &quot;+1“ enthalten. Wenn ein Besucher vor einem Kauf viermal sucht, wird eine Instanz für jede Gesamtanzahl angezeigt: 1,00, 2,00, 3,00 und 4,00. Das Kaufereignis wird jedoch nur dem 4.00-Konto gutgeschrieben (Bestellungen und Umsatzmetriken). Als Werte eines eVar-Zählers sind nur positive Zahlen zulässig.

## Hinzufügen oder Bearbeiten von Konversionsvariablen

1. Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Wählen Sie eine Report Suite aus.
1. Klicken Sie auf **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Konversion]** > **[!UICONTROL Konversionsvariablen]**.
1. Klicken Sie auf der Seite [!UICONTROL Konversionsvariablen] auf das Symbol **[!UICONTROL Erweitern]** [+] neben der Konversionsvariablen, die Sie ändern möchten.

   Oder

   Klicken Sie auf **[!UICONTROL Neu hinzufügen]**, um eine noch nicht verwendete eVar zur Report Suite hinzuzufügen.
1. Wählen Sie die Konversionsvariablenfelder aus, die Sie ändern möchten.

   Siehe [Konversionsvariablen - ](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/conversion-var-admin.md#section_7C317BB0287A4B8EB0A1A4ECC40627BF). Bei einigen Feldern können Sie Text direkt in das Feld eingeben. Bei anderen können Sie aus einer Dropdown-Liste unterstützter Werte auswählen.
1. Klicken Sie auf **[!UICONTROL Speichern]**.
