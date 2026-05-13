---
description: Die Custom Insight-Konversionsvariable (oder eVar) wird auf ausgewählten Web-Seiten Ihrer Site in den Adobe-Code platziert. Ihr Hauptzweck besteht darin, Konversionserfolgsmetriken in benutzerspezifischen Marketing-Berichten zu segmentieren. Eine eVar kann besuchsbasiert sein und ähnlich wie Cookies funktionieren. In eVar-Variablen übergebene Werte folgen den Benutzenden für einen bestimmten Zeitraum.
keywords: eVar
title: Konversionsvariablen (eVar)
feature: Admin Tools
role: Admin
exl-id: 822ecaff-a06c-42e1-aee8-ef4a43df4230
TQID: https://experienceleague.adobe.com/rYLxVYB1oDyfEk8gQyesTSRRPHid-6zJ8QaqFG2b0Kc
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
subfeature_v2: id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 1740
ht-degree: 53%

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
>Nur ein einzelner Wert kann bei einer Bildanforderung in einer eVar gespeichert werden. Wenn ein eVar-Wert mehrere Werte enthalten soll, empfehlen wie die Implementierung von [Listenvariablen](/help/implement/vars/page-vars/page-variables.md).

### Konversionsvariablen – Beschreibungen {#section_7C317BB0287A4B8EB0A1A4ECC40627BF}

Beschreibungen der Felder, die beim [Bearbeiten von Konversionsvariablen](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/conversion-var-admin.md) verwendet werden.

| Element | Beschreibung |
| --- | --- |
| [!UICONTROL Name] | Der benutzerfreundliche Name der Konversionsvariablen. Dieser Name der eVar wird im allgemeinen Reporting und als Bericht-/Dimensionsname im Menü links genutzt. |
| [!UICONTROL Typ] (nur eVar) | Der Typ des Variablenwerts:<ul><li>**[!UICONTROL Textzeichenfolge]**: Erfasst die auf Ihrer Site verwendeten Textwerte. Dies ist der häufigste Typ von eVar und die Standardeinstellung. Es verhält sich ähnlich wie andere Variablen, wobei der darin enthaltene Wert eine statische Textzeichenfolge ist. Wenn Sie Dinge wie interne Kampagnen oder interne Suchbegriffe verfolgen, ist dies die empfohlene Einstellung.</li><li>**[!UICONTROL Zähler]**: Zählt, wie oft eine Aktion stattfindet, bevor sie zum Erfolg führt. Wenn Sie z. B. eine eVar verwenden, um interne Suchvorgänge auf Ihrer Seite zu verfolgen, bewirkt die Werteinstellung auf [!UICONTROL Textzeichenfolge], dass Suchbegriffe verfolgt werden. Stellen Sie diesen Wert auf [!UICONTROL Zähler] ein, um die Zahl der durchgeführten Suchen unabhängig von den verwendeten Suchbegriffen zu zählen. Sie können beispielsweise einen eVar-Zähler verwenden, um zu verfolgen, wie oft jemand Ihre interne Suche vor einem Kauf verwendet hat.</li></ul> |
| [!UICONTROL Zuordnung] | Legt fest, wie in Analytics Gutschriften für ein Erfolgsereignis zugewiesen werden, wenn eine Variable mehrere Werte vor dem Ereignis erhält. Folgende Werte werden unterstützt:<ul><li>**[!UICONTROL Zuletzt verwendet]**: Der letzte eVar-Wert erhält immer die Gutschrift für Erfolgsereignisse, bis diese eVar abläuft.</li><li>**[!UICONTROL Ausgangswert]**: Der erste eVar-Wert erhält immer die Gutschrift für Erfolgsereignisse, bis diese eVar abläuft.</li><li>**[!UICONTROL Linear]**: Weist Erfolgsereignisse gleichmäßig allen eVar-Werten zu. Da bei der linearen Zuweisung Werte nur innerhalb eines Besuchs genau verteilt werden, sollten Sie die lineare Zuweisung bei einem eVar-Ablauf von „Besuch“ verwenden.</li></ul> **Hinweis**: Beim Wechsel zu oder von linearen Werten wird unterbunden, dass historische Daten angezeigt werden. Das Mischen von Zuordnungstypen in der Reporting-Oberfläche kann zu falschen Daten in Berichten führen. Durch die lineare Zuordnung kann sich der Umsatz beispielsweise auf eine Reihe verschiedener eVar-Werte verteilen. Nach der Umstellung auf die letzte Zuordnung werden 100 % dieses Umsatzes dem neuesten Einzelwert zugeordnet. Dieser Zusammenhang kann zu falschen Schlussfolgerungen von Benutzern führen.<br><br>Um die Wahrscheinlichkeit von Missverständnissen beim Reporting zu verringern, macht Adobe Analytics die historischen Daten für die Oberfläche nicht verfügbar. Sie kann angezeigt werden, wenn Sie die angegebene eVar wieder in die ursprüngliche Zuordnungseinstellung ändern. Sie sollten die eVar-Zuordnungseinstellungen jedoch nicht ändern, nur um auf die Verlaufsdaten zuzugreifen. Adobe empfiehlt die Verwendung einer neuen eVar, wenn neue Zuordnungseinstellungen für bereits aufgezeichnete Daten gewünscht sind, anstatt die Zuordnungseinstellungen in einer eVar zu ändern, in der bereits eine erhebliche Menge an historischen Daten aufgebaut wurde. |
| [!UICONTROL Läuft ab nach] | Gibt einen Zeitraum oder ein Ereignis an, nach dem der eVar-Wert abläuft (wird nicht mehr für Erfolgsereignisse angerechnet). Falls nach Ablauf der eVar (d. h. wenn keine eVar aktiv ist) ein Erfolgsereignis eintritt, wird das Ereignis dem Wert „Keine“ zugeschrieben.  Wenn Sie den Ablauf über ein Ereignis festlegen, läuft die Variable nur ab, wenn das Ereignis eintritt. Tritt das Ereignis nicht ein, läuft die Variable auch nicht ab.  Die verfügbaren Ablaufoptionen können in vier Hauptkategorien eingeteilt werden.<ul><li>**Auf Seitenansichts- oder Besuchsebene.** Konversionsereignisse, die über die Seitenansicht oder den Besuch hinausgehen, sind nicht mit der eVar verbunden.</li><li>**Basierend auf einem Zeitraum, z. B. Tag, Woche, Monat oder Jahr.** Konversionsereignisse, die über den angegebenen Zeitraum hinausgehen, sind nicht mit der eVar verbunden. Der Gültigkeitszeitraum beginnt mit dem Festlegen der Variablen. eVars laufen basierend auf der Zeit ab, die sie festgelegt wurden, auf die Sekunde (Minute, Stunde, Tag, Monat usw.): <ul><li>MINUTE=60 Sekunden</li><li>STUNDE=3600 Sekunden (60 Minuten)</li><li>TAG=86400 Sekunden (24 Stunden)</li><li>WOCHE=604800 Sekunden (7 Tage)</li><li>MONTH=2678400 Sekunden (31 Tage)</li><li>QUARTER=8035200 Sekunden (93 Tage - 3 Monate mit 31 Tagen)</li><li>YEAR=31536000 Sekunden (365 Tage)</li><br>Wenn ein Besuch am Montag um :00 Uhr beginnt und bei diesem Besuch um 7 Uhr :15 ist, läuft diese wie folgt ab:<li>Tagesablauf: eVar läuft am Dienstag um :15 Uhr ab.</li><li>Ablauf der Woche: eVar läuft am darauffolgenden Montag um 7 :15 Uhr ab.</li><li>Monatsablauf: eVar läuft 31 Tage ab Montag um 7 :15 Uhr ab.</li></ul><li>**Spezifische Konversionsereignisse.** Alle anderen Konversionsereignisse, die nach dem bestimmten Ereignis ausgelöst werden, das mit der eVar verknüpft ist.</li><li>**nie.** Solange ein Besucher dieselbe Kennung verwendet, kann ein beliebiger Zeitraum zwischen der eVar und dem Ereignis verstreichen.</li></ul> |
| [!UICONTROL Status] (nur eVar) | Hiermit wird der [!UICONTROL eVar]-Status definiert:<ul><li>**Deaktiviert**: Deaktiviert die [!UICONTROL eVar]. Entfernt die [!UICONTROL eVar] aus der Liste der Konversionsvariablen.</li><li>**Keine untergeordneten Beziehungen**: Verhindert, dass die [!UICONTROL eVar] anhand einer Dimension unterteilt wird.</li><li>**Grundlegende untergeordnete Beziehungen**: Ermöglicht die Unterteilung einer eVar anhand einer vollständigen Dimension (z. B. „Produkte“ oder „Kampagnen“).</li></ul> |
| [!UICONTROL Zurücksetzen] | Hiermit werden alle Werte in der eVar zurückgesetzt. Verwenden Sie diese Einstellung, wenn Sie eine eVar neu verwenden, damit kein alter Wert in einen neuen Bericht gemischt wird. Durch das Zurücksetzen werden keine historischen Daten gelöscht. |
| [!UICONTROL Merchandising] (nur eVar) | Merchandisingvariablen können einer oder zwei Syntaxen folgen:<ul><li>**[!UICONTROL Produktsyntax]**: Hiermit wird einem Produkt der eVar-Wert zugewiesen. **Hinweis**: Wenn die [!UICONTROL Produktsyntax] ausgewählt ist, ist der Bereich [!UICONTROL „Merchandising-Binding-Ereignis“] deaktiviert und kann nicht für die Bearbeitung ausgewählt werden. Für diese Syntax können keine [!UICONTROL Binding-Ereignisse] angewendet werden.</li><li>**[!UICONTROL Syntax der Konversionsvariablen]**: Hierbei wird einem Produkt nur dann die eVar zugewiesen, wenn ein [!UICONTROL Binding-Ereignis] auftritt. In diesem Fall legen Sie fest, welche Ereignisse als [!UICONTROL Binding-Ereignisse] gelten.  Wenn Sie diese Einstellung ändern, ohne den JavaScript-Code zu aktualisieren, gehen Daten verloren. Siehe [Merchandising-Variablen](/help/components/dimensions/evar-merchandising.md).</li></ul> |
| [!UICONTROL Merchandising-Binding-Ereignis] (nur eVar) | Wenn „Merchandising“ auf [!UICONTROL Konversionsvariablensyntax] eingestellt ist, wird der aktuelle eVar-Wert durch die ausgewählten Ereignisse mit einem Produkt verbunden. Um ein [!UICONTROL Binding-Ereignis] zu verwenden, setzen Sie [!UICONTROL Zuordnung] auf [!UICONTROL Zuletzt verwendet]. Wenn [!UICONTROL Zuordnung] auf [!UICONTROL Ausgangswert] eingestellt ist, bleibt die erste eVar-Produktverbindung erhalten, bis die eVar abläuft. Sie können mehrere Ereignisse auswählen, indem Sie die Strg-Taste (Windows) oder die Cmd-Taste (Mac) gedrückt halten und auf mehrere Elemente in der Liste klicken. Sie können nur dann ein Ereignis auswählen, wenn [!UICONTROL Konversionsvariablensyntax] ausgewählt ist. |

### Gültigkeit

`eVars` laufen nach dem von Ihnen festgelegten Zeitraum ab. Nach dem Ablauf werden in der eVar keine Erfolgsereignisse mehr gezählt. eVars können auch so konfiguriert werden, dass sie bei Erfolgsereignissen ablaufen. Wenn beispielsweise eine interne Promotion am Ende eines Besuchs abläuft, werden der internen Promotion nur Käufe oder Registrierungen gutgeschrieben, die während des Besuchs stattfinden, bei dem sie aktiviert wurde.

Es gibt zwei Möglichkeiten, eine eVar ablaufen zu lassen:

* Sie können die eVar so einstellen, dass sie nach einem bestimmten Zeitraum oder Ereignis abläuft.
* Sie können das Ablaufen einer eVar erzwingen, indem Sie sie zurücksetzen (z. B. wenn eine Variable für einen anderen Zweck eingesetzt werden soll).

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
