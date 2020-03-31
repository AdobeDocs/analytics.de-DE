---
title: eVar
description: Eine benutzerdefinierte Dimension, die Sie in Berichte verwenden können.
translation-type: tm+mt
source-git-commit: f18fbd091333523cd9351bfa461a11f0c3f17bef

---


# eVar

*Auf dieser Hilfeseite wird beschrieben, wie eVars als Dimension funktionieren. Weitere Informationen zur Implementierung von eVars finden Sie unter[eVars](/help/implement/vars/page-vars/evar.md)im Implementierungs-Benutzerhandbuch.*

eVars sind benutzerdefinierte Variablen, die Sie beliebig verwenden können. Wenn Sie über ein [Lösungsdesign-Dokument](/help/implement/prepare/solution-design.md)verfügen, werden die meisten unternehmensspezifischen Dimensionen als eVars bezeichnet. Standardmäßig bleiben eVars über den Treffer hinaus erhalten, auf dem sie eingestellt sind. Sie können ihren Ablauf und ihre Zuordnung unter [Konversionsvariablen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) in den Report Suite-Einstellungen anpassen.

## Funktionsweise von eVars

Wenn Sie Daten an Adobe Analytics senden, übersetzen die Datenerfassungsserver den Treffer in eine Datenzeile mit Hunderten von Spalten. Für jede eVar sind zwei Spalten vorgesehen. eine für die direkte Datenerfassung und die andere für die Beibehaltung von Werten.

* Eine Standardspalte enthält Daten, die von der Bildanforderung an Adobe gesendet werden.
* Eine Spalte &quot;Beitrag&quot;enthält beständige Daten, die vom Ablauf und der Zuordnung der eVar abhängen.

Unter fast allen Umständen wird die `post_evar` Spalte in Berichten verwendet.

### Verknüpfung von eVars mit Metriken

Erfolgreiche Ereignis und eVars werden häufig in verschiedenen Bildanforderungen definiert. In der `post_evar` Spalte können eVar-Werte sich mit Ereignissen verbinden und Daten in Berichte anzeigen. Gehen Sie zum Beispiel wie folgt vor:

1. Ein Besucher gelangt zu Ihrer Site auf Ihrer Startseite.
2. Sie suchen nach &quot;Katzen&quot;mithilfe der internen Suche Ihrer Site. Ihre Implementierung setzt eVar1 auf die interne Suche.
3. Sie haben ein Produkt Ansicht und fahren mit dem Kassengang fort.

Eine vereinfachte Version der Rohdaten würde wie folgt aussehen:

| `visitor_id` | `pagename` | `evar1` | `post_evar1` | `event_list` |
| --- | --- | --- | --- | --- |
| `examplevisitor_987` | `Home page` |  |  |  |
| `examplevisitor_987` | `Search results` | `cats` | `cats` | `event1` |
| `examplevisitor_987` | `Product page` |  | `cats` | `prodView` |
| `examplevisitor_987` | `Cart` |  | `cats` | `scAdd` |
| `examplevisitor_987` | `Checkout` |  | `cats` | `scCheckout` |
| `examplevisitor_987` | `Purchase confirmation` |  | `cats` | `purchase` |

* Die `visitor_id` Spalte verknüpft Treffer mit demselben Besucher. In den eigentlichen Rohdaten werden die verketteten Werte der Besucher-ID `visid_high` und `visid_low` bestimmt.
* Die `pagename` Spalte füllt die Dimension &quot;Seiten&quot;.
* Die `evar` Spalte bestimmt die Treffer, wenn eVar1 explizit festgelegt wurde.
* Der `post_evar1` vorherige Wert wird abhängig von der Zuordnung und dem Ablauf der Variablen in den Report Suite-Einstellungen übernommen.
* Die `event_list` Spalte enthält alle Metrikdaten. Bei diesem Beispiel `event1` handelt es sich um &quot;Suchen&quot;, bei den anderen Ereignissen um Standardmetriken zum Einkaufswagen. In den eigentlichen Rohdaten `event_list` enthält ein kommagetrennter Zahlensatz mit einer Nachschlagetabelle, die diese Zahlen an eine Metrik bindet.

### Übersetzen der Datenerfassung in Berichte

Die Tools in Adobe Analytics, z. B. Analyse Workspace, arbeiten von diesen erfassten Daten ab. Wenn Sie z. B. einen Bericht mit eVar1 als Dimension und Bestellungen als Metrik abrufen, wird ein Bericht ähnlich dem folgenden angezeigt:

| `Internal search term (eVar1)` | `Orders` |
| --- | --- |
| `cats` | `1` |

Analyse Workspace ruft diesen Bericht mit der folgenden Logik ab:

* Sehen Sie sich alle `event_list` Werte an und wählen Sie alle Treffer mit `purchase` ihnen aus.
* Zeigen Sie den `post_evar1` Wert aus diesen Treffern an.

### Bedeutung der Zuteilung und des Ablaufs

Da Zuordnung und Ablauf bestimmen, welche Werte beibehalten werden, sind sie entscheidend, um den größtmöglichen Nutzen aus einer Analytics-Implementierung zu ziehen. Adobe empfiehlt dringend, dass Sie innerhalb Ihres Unternehmens besprechen, wie mehrere Werte für jede eVar verarbeitet werden (Zuordnung) und wann eVars die Speicherung der Daten beenden (Ablauf).

* Standardmäßig verwendet eine eVar die letzte Zuordnung. Neue Werte überschreiben behaltene Werte.
* Standardmäßig verwendet eine eVar einen Ablauf des Besuchs. Nach Ende eines Besuchs werden Werte nicht mehr von Zeile zu Zeile in der `post_evar` Spalte kopiert.

Sie können die eVar-Zuordnung und den Ablauf unter [Konversionsvariablen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) in den Report Suite-Einstellungen ändern.
