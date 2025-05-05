---
title: eVar (Dimension)
description: Eine benutzerdefinierte Dimension, die Sie in Berichten verwenden können.
feature: Dimensions
exl-id: ce7cc999-281d-4c52-b64d-d44cc320ab2d
source-git-commit: ec077b3404c6bff1198fae30a2d25321de8a58cd
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 82%

---

# eVar

*Auf dieser Hilfeseite wird beschrieben, wie eVars als [Dimension](overview.md) funktionieren. Weitere Informationen zur Implementierung von eVars finden Sie unter [eVars](/help/implement/vars/page-vars/evar.md) im Implementierungs-Benutzerhandbuch.*

eVars sind benutzerdefinierte Variablen, die Sie beliebig verwenden können. Wenn Sie über ein [Lösungsentwurfsdokument](/help/implement/prepare/solution-design.md) verfügen, werden die meisten für Ihr Unternehmen spezifischen Dimensionen als [!UICONTROL eVars] angezeigt. Weitere Informationen finden Sie unter Übersicht [&#128279;](overview.md) Dimensionen .

Standardmäßig bleiben eVars über den Treffer hinaus bestehen, für den sie festgelegt wurden. EVar Weitere Informationen zur Funktionsweise der [-Persistenz auf der Adobe-Architektur finden Sie ](#how-evars-tie-to-metrics) den Abschnitten [&#128279;](#how-evars-work)Funktionsweise von eVars“ und Verknüpfung von eVars mit Metriken . Sie können ihre Gültigkeit und Zuordnung unter [Konversionsvariablen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-var-admin.md) in den [!UICONTROL Report Suite-Einstellungen] anpassen. Die folgende Abbildung zeigt ein Beispiel für eVar-Definitionen in der Benutzeroberfläche „Konversionsvariablen“:

![eVar-Beispiele](assets/evars-sample.png)

Die Anzahl der verfügbaren eVars hängt von Ihrem Vertrag mit Adobe ab. Es sind bis zu 250 eVars verfügbar, wenn Ihr Vertrag mit Adobe dies unterstützt.

Die Groß- oder Kleinschreibung, die in Berichten verwendet wird, basiert auf dem ersten Wert, den Sie in einem bestimmten Kalendermonat senden. Die Groß-/Kleinschreibung kann sich je nach Berichtsfenster und dem Fall eines eVar-Werts ändern, der zuerst in diesem Zeitraum erfasst wurde.

## Füllen von eVars mit Daten

Jede eVar erfasst Daten aus der [`v1` – `v250`-Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in den Bildanforderungen. Beispielsweise erfasst der Abfragezeichenfolgenparameter `v1` Daten für eVar1, während der Abfragezeichenfolgenparameter `v222` Daten für eVar222 erfasst.

AppMeasurement, das JavaScript-Variablen in eine Bildanforderung für die Datenerfassung kompiliert, verwendet die Variablen `eVar1` – `eVar250`. Die Implementierungsrichtlinien finden Sie unter [eVar](/help/implement/vars/page-vars/evar.md) im Benutzerhandbuch zu Implementierungen.

## Dimensionselemente

Da eVars benutzerdefinierte Zeichenfolgen in Ihrer Implementierung enthalten, bestimmt Ihr Unternehmen, welche Dimensionselemente für jede eVar gelten. Stellen Sie sicher, dass Sie den Zweck jeder eVar und die typischen Dimensionselemente in einem [Solution-Design-Dokument](/help/implement/prepare/solution-design.md) festhalten.

## Funktionsweise von eVars

Wenn Sie Daten an Adobe Analytics senden, übersetzen die Datenerfassungs-Server den Treffer in eine Datenzeile mit Hunderten von Spalten. Für jede eVar sind zwei Spalten vorgesehen: eine für die direkte Datenerfassung und die andere für persistente Werte.

* Eine Standardspalte enthält Daten, die von der Bildanforderung an Adobe gesendet werden.
* Eine Spalte „Post“ enthält persistente Daten, die von der Gültigkeit und Zuordnung der eVar abhängen.

Die Spalte `post_evar` wird fast immer in Berichten verwendet.

### Verknüpfung von eVars mit Metriken

Erfolgsereignisse und eVars werden häufig zu unterschiedlichen Zeiten definiert. In der Spalte `post_evar` können eVar-Werte mit Ereignissen verknüpft werden, sodass Daten in Berichten angezeigt werden. Nehmen Sie zum Beispiel den folgenden Besuch:

1. Ein Besucher erreicht Ihre Site auf Ihrer Startseite.
2. Sie suchen mithilfe der internen Suche Ihrer Site nach „cats“. Ihre Implementierung verwendet eVar1 für die interne Suche.
3. Sie sehen sich ein Produkt an und schließen den Checkout-Prozess ab.

Eine vereinfachte Version der Rohdaten würde wie folgt aussehen:

| `visitor_id` | `pagename` | `evar1` | `post_evar1` | `event_list` |
| --- | --- | --- | --- | --- |
| `examplevisitor_987` | `Home page` | | | |
| `examplevisitor_987` | `Search results` | `cats` | `cats` | `event1` |
| `examplevisitor_987` | `Product page` | | `cats` | `prodView` |
| `examplevisitor_987` | `Cart` | | `cats` | `scAdd` |
| `examplevisitor_987` | `Checkout` | | `cats` | `scCheckout` |
| `examplevisitor_987` | `Purchase confirmation` | | `cats` | `purchase` |

* Die Spalte `visitor_id` verknüpft Treffer mit demselben Besucher. In den eigentlichen Rohdaten bestimmen die verketteten Werte von `visid_high` und `visid_low` Besucher-ID.
* Die Spalte `pagename` füllt die Dimension „Seiten“.
* Die Spalte `evar` bestimmt die Treffer, bei denen eVar1 explizit gesetzt wurde.
* `post_evar1` beinhaltet den vorherigen Wert, abhängig von der Zuordnung und Gültigkeit der Variablen in den Report Suite-Einstellungen.
* Die Spalte `event_list` enthält alle Metrikdaten. In diesem Beispiel ist `event1` „Suchen“. Die anderen Ereignissen sind standardmäßige Warenkorbmetriken. In den eigentlichen Rohdaten enthält `event_list` einen kommagetrennten Satz von Zahlen mit einer Zuordnungstabelle, die diese Zahlen mit einer Metrik verknüpft.

### Übersetzen der Datenerfassung in Berichte

Die Tools in Adobe Analytics wie Analysis Workspace verarbeiten diese erfassten Daten. Wenn Sie z. B. einen Bericht mit eVar1 als Dimension und Bestellungen als Metrik abrufen, wird ein Bericht ähnlich dem folgenden angezeigt:

| `Internal search term (eVar1)` | `Orders` |
| --- | --- |
| `cats` | `1` |

Analysis Workspace ruft diesen Bericht mit der folgenden Logik ab:

* Durchsuchen Sie alle `event_list` Werte und wählen Sie alle Zeilen mit `purchase` darin aus.
* Zeigen Sie von diesen Zeilen den `post_evar1` an.

Der resultierende Bericht zeigt jeden einzelnen Wert in `post_evar1` auf der linken Seite an und wie viele Bestellungen diesem Wert auf der rechten Seite zugeordnet wurden.

### Bedeutung von Zuordnung und Gültigkeit

Da Zuordnung und Gültigkeit bestimmen, welche Werte beibehalten werden, sind sie von entscheidender Bedeutung, um den größtmöglichen Nutzen aus einer Analyseimplementierung zu ziehen. Adobe empfiehlt dringend, dass Sie innerhalb Ihres Unternehmens besprechen, wie mehrere Werte für jedes eVar behandelt werden (Zuordnung) und wann eVars keine Daten mehr speichern (Gültigkeit).

* Standardmäßig verwendet ein eVar die letzte Zuordnung. Neue Werte überschreiben persistente Werte.
* Standardmäßig verwendet eine eVar eine Gültigkeit des Besuchs. Sobald ein Besuch endet, werden die Werte nicht mehr von Zeile zu Zeile in der Spalte `post_evar` kopiert.

Sie können die Gültigkeit und Zuordnung von eVars unter [Konversionsvariablen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-var-admin.md) in den Report Suite-Einstellungen ändern.

## Wert von eVars gegenüber Props

Adobe empfiehlt in den meisten Fällen die Verwendung von eVars. Dies stützt sich auf Folgendes:

* eVars sind in Berichten auf 255 Byte begrenzt. Props sind auf 100 Byte begrenzt.
* Props bleiben standardmäßig nicht über den festgelegten Treffer hinaus erhalten. eVars haben eine benutzerdefinierte Gültigkeit, mit der Sie feststellen können, wann einer eVar ein nachfolgendes Ereignis nicht mehr gutgeschrieben wird. Wenn Sie jedoch die [Berichtszeitverarbeitung](/help/components/vrs/vrs-report-time-processing.md) verwenden, können sowohl Props als auch eVars ein benutzerdefiniertes Zuordnungsmodell verwenden.
* Adobe unterstützt bis zu 250 eVars und nur 75 Props.

Weitere Vergleiche zwischen Props und eVars finden Sie unter [Prop](prop.md).
