---
description: Diese Änderungen an der Funktionsweise von berechneten Metriken in Analytics können sich auf Ihre Arbeit auswirken.
seo-description: Diese Änderungen an der Funktionsweise von berechneten Metriken in Analytics können sich auf Ihre Arbeit auswirken.
seo-title: Häufig gestellte Fragen
title: Häufig gestellte Fragen
uuid: 9b7f1cd1-b969-4b15-8af1-969d816b65b8
translation-type: tm+mt
source-git-commit: 57fe1f6d613b9f54a5191ac8684d36bccfebf4e5

---


# Häufig gestellte Fragen

These changes to the way calculated metrics work in [!DNL Analytics] may impact you.

[Wie greife ich auf den Generator für berechnete Metriken zu?](/help/components/c-calcmetrics/cm-transition.md#section_D9AE9A0ACF824BACB5D05F0C2F7E9CA1)

[Wie greife ich auf den Manager für berechnete Metriken zu?](/help/components/c-calcmetrics/cm-transition.md#section_DD0BD13E9EC940268EBE8BC88241A152)

[Warum werden so viele berechnete Metriken mit demselben Namen angezeigt?](/help/components/c-calcmetrics/cm-transition.md#section_E15C5B6CCC58498CAEC3FBDA8988F0A1)

[Was ist mit meinen globalen berechneten Metriken passiert?](/help/components/c-calcmetrics/cm-transition.md#section_7351D4C7361F4ABAA1B43F8E89AAD211)

[Was ist mit globalen berechneten Metriken passiert, die über Anmeldeunternehmen hinweg freigegeben wurden?](/help/components/c-calcmetrics/cm-transition.md#section_59E5CD948ED643AE9AD3D2E4277647F8)

[Was ist mit berechneten Metriken mit der Classification Numerisch oder Numerisch2 passiert?](/help/components/c-calcmetrics/cm-transition.md#section_71AFE6C4A7CD4AA19AB3A9D3C41D115B)

[Was ist mit Lebensdauermetriken passiert?](/help/components/c-calcmetrics/cm-transition.md#section_AEDB02EF24584DAD8731BED9DDCE4F48)

[Was muss ich über berechnete Metriken basierend auf Metriken für tägliche/wöchentliche/monatliche/vierteljährliche/jährliche Unique Visitor wissen?](/help/components/c-calcmetrics/cm-transition.md#section_E9A77EBB41CE4881B196CC1C282B2DF3)

[Was passiert mit berechneten Metriken, die mit den alten Report Suite-API-Methoden erstellt oder verwaltet wurden?](/help/components/c-calcmetrics/cm-transition.md#section_13ED1BAD02634674BDAEB479B060A4B6)

[Unterstützt „Aktuelle Daten“ alle Typen an berechneten Metriken?](/help/components/c-calcmetrics/cm-transition.md#section_1DAA718BB8DB4413BAF8AD4B4FAAFFA2)

[Was bedeutet „Kein Name angegeben“ im Zusammenhang mit migrierten berechneten Metriken?](/help/components/c-calcmetrics/cm-transition.md#section_C90CBB72A67644F38D583301981F8D03)

[Was passiert mit den berechneten Metriken eines Benutzers, wenn dieser Benutzer gelöscht wird?](/help/components/c-calcmetrics/cm-transition.md#section_42ED4C15830540879C4A161423690E5A)

[Warum werden "Unbekannte"berechnete Metriken angezeigt, die für andere Report Suites nicht "gültig"sind, obwohl sie erstellt und auf diese Report Suites angewendet werden können?](/help/components/c-calcmetrics/cm-transition.md#section_6772818EFDED46E9B7095D64C3B77211)

[Warum wurden Änderungen an meinen alten berechneten Metriken nicht gespeichert?](/help/components/c-calcmetrics/cm-transition.md#section_81CDEFCA1FD542579AF183DA1494EAF0)

[Warum werden meine berechneten Metriken nicht im Marketingkanalbericht angezeigt?](/help/components/c-calcmetrics/cm-transition.md#section_FC350359A775433AB5F43C7CAB304D62)

[Warum enthalten einige der berechneten Metriken Formeln ohne die Klammern, die ich hinzugefügt habe?](/help/components/c-calcmetrics/cm-transition.md#section_AC0D1E9714AD487F9A1C73359F518B5E)

[(Nur Ad Hoc Analysis) Werden berechnete Metriken mit eingebetteten oder Inline-Segmentdefinitionen weiterhin unterstützt?](/help/components/c-calcmetrics/cm-transition.md#section_B25C924A282F49388AB604E3D826F44C)

[(Nur Report Builder) Warum sind berechnete Metriken aus meinen Anforderungen verschwunden?](/help/components/c-calcmetrics/cm-transition.md#section_DA4792FE5D7945218CD5E6328DE08E82)

[Wie werden Gesamtwerte für berechnete Metriken ermittelt?](/help/components/c-calcmetrics/cm-transition.md#section_57BA3A299C7948ABB82B0392A9B0F33E)

## Wie greife ich auf den Generator für berechnete Metriken zu? {#section_D9AE9A0ACF824BACB5D05F0C2F7E9CA1}

* Klicken Sie oben im Manager für berechnete Metriken auf **[!UICONTROL + Hinzufügen]oder**
* Klicken Sie in einem beliebigen Analytics-Bericht auf das Metriksymbol ![](assets/metrics_icon.png) auf der linken Seite des Berichts, um die Metrikleiste anzuzeigen. Klicken Sie dann auf **[!UICONTROL Hinzufügen]**.

## Wie greife ich auf den Manager für berechnete Metriken zu? {#section_DD0BD13E9EC940268EBE8BC88241A152}

* Go to  **[!UICONTROL Analytics]** &gt; **[!UICONTROL Components]** in the left navigation. Klicken Sie anschließend auf **[!UICONTROL Berechnete Metriken]**.

* In any [!DNL Analytics] report, click the Metrics icon  ![](assets/metrics_icon.png) to the left of a report to bring up the Metrics rail, then click **[!UICONTROL Manage]**.

## Warum werden so viele berechnete Metriken mit demselben Namen angezeigt? {#section_E15C5B6CCC58498CAEC3FBDA8988F0A1}

(Bisher hatten globale berechnete Metriken keinen spezifischen Administrator als Inhaber und waren für alle Benutzer dieser Report Suite sichtbar. Die Metriken waren nach Report Suite eingeteilt. Wenn eine Metrik in einer Report Suite denselben Namen wie eine Metrik in einer anderen Report Suite hatte, wurde sie den Benutzern einfach als dieselbe Metrik angezeigt, wenn diese die Report Suite änderten.)

Jetzt werden Metriken nicht mehr nach Report Suites eingeteilt. Wenn eine Metrik in einer Report Suite denselben Namen wie eine Metrik in einer anderen Report Suite hat, sind beide Metriken im Generator für berechnete Metriken und in der Metrikauswahl sichtbar und können als doppelte Metriken angezeigt werden, obwohl sie möglicherweise nicht dieselbe Definition aufweisen.

You would see a number of calculated metrics with the same name (but created in different report suites) only if you unchecked the (Only `<report suite>`) checkbox as shown here:

![](assets/report_suite.png)

**Zu ergreifende Maßnahme**

Sie sollten berechnete Metriken mit ähnlichen Namen und Definitionen konsolidieren. Gehen Sie dabei aber vorsichtig vor. Sie können die Report Suite auf eine berechnete Metrik im Manager für berechnete Metriken prüfen, um die Original-Report Suite zu verifizieren. Sie sollten auch die Definitionen von Metriken prüfen, wenn sie potenzielle Duplikate löschen, um sicherzustellen, dass Sie Metriken korrekt konsolidieren.

> [!NOTE] Obwohl berechnete Metriken nicht mehr an eine bestimmte Report Suite gebunden sind und in jeder Report Suite verwendet werden können, die für das Anmeldeunternehmen sichtbar ist, ist die Report Suite, unter der die berechnete Metrik erstellt oder zuletzt gespeichert wurde, weiterhin im Manager für berechnete Metriken sichtbar.

> [!NOTE] Selbst wenn eine berechnete Metrik gelöscht wird, funktionieren alle Lesezeichen oder Dashboard-Berichte, die auf diese Metrik verweisen, weiterhin.

## Was ist mit meinen globalen berechneten Metriken passiert?{#section_7351D4C7361F4ABAA1B43F8E89AAD211}

Bisher konnte ein Administrator berechnete Metriken (als „globale berechnete Metriken“ oder „berechnete Report Suite-Metriken“ bezeichnet) in einer Report Suite über Admin Tools erstellen.

Der Inhaber von globalen berechneten Metriken ist jetzt der erste Administrator in der Administratorenliste des Anmeldeunternehmens. Sie werden standardmäßig für „Alle“ freigegeben. Dieses Muster folgt demselben Freigabemodell und denselben Migrationsplänen wie Segmente.

**Zu ergreifende Maßnahme**

Keine. Der neue Administrator sollte beim Ändern oder Löschen dieser berechneten Metriken allerdings mit Vorsicht vorgehen, da diese möglicherweise in Lesezeichenberichten und Dashboards verwendet werden.

> [!NOTE] Selbst wenn eine berechnete Metrik gelöscht wird, funktionieren alle Lesezeichen oder Dashboard-Berichte, die auf diese Metrik verweisen, weiterhin.

## Was ist mit globalen berechneten Metriken passiert, die über Anmeldeunternehmen hinweg freigegeben wurden? {#section_59E5CD948ED643AE9AD3D2E4277647F8}

Bisher konnte ein Administrator berechnete Metriken (als „globale berechnete Metriken“ oder „berechnete Report Suite-Metriken“ bezeichnet) in einer Report Suite über Admin Tools erstellen. Diese Metriken konnten dann über Anmeldeunternehmen hinweg „freigegeben“ werden, indem die Report Suite mehreren Anmeldeunternehmen hinzugefügt wurde.)

Globale berechnete Metriken können nun nicht mehr über Anmeldeunternehmen hinweg freigegeben werden. Sie sind nicht mehr an eine bestimmte Report Suite gebunden, sondern stattdessen an ein bestimmtes Anmeldeunternehmen. Berechnete Metriken, die über Anmeldeunternehmen hinweg freigegeben waren

* wurden auf alle Anmeldeunternehmen mit Zugriff auf diese Report Suite migriert.
* Standard ist "Für alle freigegeben".
* werden zu von allen anderen Anmeldeunternehmen unabhängigen Kopien.

> [!NOTE] Wenn die berechnete Metrik in einem Lesezeichen, Dashboard, Warnhinweis oder terminierten Bericht verwendet wurde, wirkt sich die Bearbeitung der neuen Kopie NICHT auf die alte beibehaltene berechnete Metrik aus.

## Was ist mit berechneten Metriken mit der Classification Numerisch oder Numerisch2 passiert?{#section_71AFE6C4A7CD4AA19AB3A9D3C41D115B}

(Previously, calculated metrics with a Numeric or Numeric2 classification were only visible in [!UICONTROL Reports &amp; Analytics], [!UICONTROL Report Builder], and the APIs.)

Now, calculated metrics with a Numeric or Numeric2 classification will continue to be visible in [!UICONTROL Reports &amp; Analytics], [!UICONTROL Report Builder], and the APIs. Sie werden allerdings in keinem Bericht mit einem angewendeten Segment unterstützt.

In addition, calculated metrics with a Numeric or Numeric2 classification will not be supported in the following components: [!UICONTROL Ad Hoc Analysis], [!UICONTROL Analysis Workspace], [!UICONTROL Real-Time] reports, [!UICONTROL Anomaly Detection], and [!UICONTROL Contribution Analysis]. Wenn Sie eine berechnete Metrik mit der Classification Numerisch oder Numerisch2 erstellen oder bearbeiten, wird eine Kompatibilitätswarnung angezeigt, dass die berechnete Metrik mit bestimmten Produktbereichen nicht kompatibel ist.

**Zu ergreifende Maßnahme**

Erstellen Sie keine berechnete Metrik mit der Classification Numerisch oder Numerisch2, wenn die Metrik mit einem Segment oder mit einer der nicht kompatiblen Komponenten verwenden werden soll.

## Was ist mit Lebensdauermetriken passiert?{#section_AEDB02EF24584DAD8731BED9DDCE4F48}

Life-Time metrics (a.k.a. all-time metrics) are no longer supported and no longer visible in the [!UICONTROL Reports &amp; Analytics] UI or any other UI. Sie können nicht von der Berichts-API abgefragt werden.

Alle Lesezeichen, Dashboards, terminierten Berichte oder Warnhinweise mit einer Lebensdauermetrik werden weiterhin ohne diese Metrik ausgeführt, solange noch mindestens eine andere gültige Metrik im Bericht enthalten ist. Wenn die einzige Metrik im Lesezeichen, Dashboard, terminierten Bericht oder Warnhinweis eine Lebensdauermetrik ist, wird der Bericht nicht mehr ausgeführt.

## Was muss ich über berechnete Metriken basierend auf Metriken für tägliche/wöchentliche/monatliche/vierteljährliche/jährliche Unique Visitor wissen?{#section_E9A77EBB41CE4881B196CC1C282B2DF3}

Calculated metrics based on Unique Visitor metrics will be visible in the following [!DNL Analytics] components: [!UICONTROL Reports &amp; Analytics], [!UICONTROL Report Builder], and Reporting API.

However, these metrics will not be supported in the following components: [!UICONTROL Segments], [!UICONTROL Analysis Workspace], [!UICONTROL Real-Time] reports, [!UICONTROL Anomaly Detection], and [!UICONTROL Contribution Analysis]. Wenn Sie eine berechnete Metrik erstellen oder bearbeiten, die auf Unique Visitors-Metriken basiert, wird eine Kompatibilitätswarnung angezeigt, dass die Metrik mit bestimmten Produktbereichen nicht kompatibel ist.

Sie verwenden eine Basis-Unique Visitor-Metrik in einem Bericht mit einem Segment. Sie können berechnete Metriken, die auf Unique Visitor-Metriken basieren, zwar erstellen, aber diese berechneten Metriken können nicht auf Berichte mit Segmenten angewendet werden. Außerdem können keine Segmente in diese berechneten Metriken eingebettet werden.

## Was passiert mit berechneten Metriken, die mit den alten Report Suite-API-Methoden erstellt oder verwaltet wurden? {#section_13ED1BAD02634674BDAEB479B060A4B6}

Das Speichern einer berechneten Metrik mit der API-Methode ReportSuite.SaveCalculatedMetrics (1.3 oder 1.4) war zuvor mit dem Erstellen oder Aktualisieren einer berechneten Metrik in der Admin Console identisch. Dasselbe galt für ReportSuite.DeleteCalculatedMetrics. Außerdem war die Liste der berechneten Metriken, die in der Admin Console oder beim Aufruf von ReportSuite.GetCalculatedMetrics angezeigt wurde, identisch.

Die ReportSuite CalculatedMetrics API-Methoden (1.3 oder 1.4) speichern, löschen und rufen nun berechnete Metriken mithilfe des alten Stores ab. Vorhandene berechnete Metriken werden migriert und im neuen Generator für berechnete Metriken angezeigt. **Neue berechnete Metriken, die mit den API-Methoden erstellt werden, sind nur in der API sichtbar. Sie können weiterhin in der Berichterstellungs-API verwendet werden.**

**Zu ergreifende Maßnahme**

Wenn Sie sowohl die API als auch den Generator für berechnete Metriken verwenden müssen, sollten Sie die ReportSuite CalculatedMetrics-API-Methoden nicht mehr verwenden und stattdessen die neuen CalculatedMetrics-API-Methoden (Get, Save, Delete und GetFunctions) nutzen.

## Unterstützt „Aktuelle Daten“ alle Typen an berechneten Metriken? {#section_1DAA718BB8DB4413BAF8AD4B4FAAFFA2}

Berechnete Metriken mit Segmenten oder statistischen Funktionen werden von „Aktuelle Daten“ nicht unterstützt. Lediglich einfache mathematische Funktionen wie Addition, Löschung, Multiplikation, Division und Negierung (-x) werden unterstützt.

## Was bedeutet „Kein Name angegeben“ im Zusammenhang mit migrierten berechneten Metriken? {#section_C90CBB72A67644F38D583301981F8D03}

„Kein Name angegeben“ bedeutet, dass kein Metrikname mit dieser migrierten Metrik verknüpft ist (lediglich eine Formel ohne einen beschreibenden Namen).

## Was passiert mit den berechneten Metriken eines Benutzers, wenn dieser Benutzer gelöscht wird? {#section_42ED4C15830540879C4A161423690E5A}

Alle von diesem Benutzer erstellten berechneten Metriken werden ebenfalls gelöscht. Gelöschte berechnete Metriken funktionieren aber weiterhin innerhalb von gespeicherten Lesezeichen, Dashboards oder terminierten Berichten.

## Why do I see "Unknown" calculated metrics that aren't 'valid' for other report suites even though they can be created and applied to those report suites? {#section_6772818EFDED46E9B7095D64C3B77211}

Die Benutzeroberfläche zeigt "unbekannt"an, wenn die berechnete Metrik Basismetriken oder Dimensionen enthält, die für die ausgewählte Report Suite nicht vorhanden sind.

## Warum wurden Änderungen an meinen alten berechneten Metriken nicht gespeichert? {#section_81CDEFCA1FD542579AF183DA1494EAF0}

Dazu kann es aufgrund der Zeit für die Migration in die neue Datenbank für berechnete Metriken kommen (vom 15. Juni 2015 bis zum 18. Juni 2015).

**Zu ergreifende Maßnahme**

Sie müssen die Änderungen an den alten Metriken erneut vornehmen.

## Why don't my calculated metrics show up in the Marketing Channels report? {#section_FC350359A775433AB5F43C7CAB304D62}

(Bisher wurden alle berechneten Metriken in der Metrikauswahl in Marketingkanalberichten mit der Option „Erstkontakt“ und „Letztkontakt“ aufgeführt.)

Jetzt sind nur die berechneten Metriken in der Metrikauswahl in Marketingkanalberichten verfügbar, deren Zuordnungstyp im Generator für berechnete Metriken spezifisch auf „Erstkontakt“ oder „Letztkontakt“ gesetzt wurde. Beachten Sie, dass alle berechneten Metriken, die bereits auf Marketingkanalberichte angewendet wurden, weiterhin angewendet werden und wie bisher funktionieren. Um eine berechnete Metrik für Marketingkanäle zu erstellen, klicken Sie im Metrikgenerator auf das Konfigurationssymbol und wählen Sie entweder „Erstkontakt“ oder „Letztkontakt“ als Zuordnungstyp. Denken Sie daran, dass dadurch die berechnete Metrik nur mit Marketingkanalberichten kompatibel ist und in keinem anderen Bericht verwendet werden kann.

## Warum enthalten einige der berechneten Metriken Formeln ohne die Klammern, die ich hinzugefügt habe? {#section_AC0D1E9714AD487F9A1C73359F518B5E}

Bei der Migration hat Adobe überflüssige Klammern aus einigen Formeln entfernt. Dabei wurden nur Klammern entfernt, die keinen Einfluss auf die Berechnung der Metrik haben. Das ändert nichts an den Daten - es vereinfacht nur die Formel.

## (Nur Ad Hoc Analysis) Werden berechnete Metriken mit eingebetteten oder Inline-Segmentdefinitionen weiterhin unterstützt? {#section_B25C924A282F49388AB604E3D826F44C}

In Ad Hoc Analysis erstellte berechnete Metriken konnten bisher Inline-Segmentdefinitionen enthalten. Dies ist nun nicht mehr möglich.

**Zu ergreifende Maßnahme**

Sie müssen das Segment explizit speichern. Vorhandene berechnete Metriken mit Inline-Segmentdefinitionen werden weiterhin ordnungsgemäß ausgeführt und können in Ad Hoc Analysis angezeigt werden. Sie können allerdings nicht gespeichert werden, ohne das Segment explizit zu speichern.

## (Nur Report Builder) Warum sind berechnete Metriken aus meinen Anforderungen verschwunden? {#section_DA4792FE5D7945218CD5E6328DE08E82}

Wenn die Anforderung in Version 5.2 erstellt wurde und berechnete Metriken enthält, sind diese Metriken in Version 5.1 (oder früheren Versionen) nicht sichtbar. Dies liegt daran, dass berechnete Metriken nun globale IDs (nicht Report Suite-spezifische IDs) verwenden.

**Zu ergreifende Maßnahme**

Sie müssen ein Upgrade auf Version 5.2 vornehmen, um diese Metriken sehen zu können.

## Wie werden Gesamtwerte für berechnete Metriken ermittelt? {#section_57BA3A299C7948ABB82B0392A9B0F33E}

When [!UICONTROL Reports &amp; Analytics] shows a calculated metrics total in [!UICONTROL Reports &amp; Analytics], it's just applying the formula to the total. Beispiel: Der Gesamtwert für die berechnete Metrik „Bestellungen/Besuch“ wird ermittelt, indem die Gesamtbestellungen durch die Gesamtbesuche dividiert werden. In einigen Fällen ist jedoch der Gesamtwert für eine berechnete Metrik nicht nur die Summe der Einzelposten, sondern ein Gesamtwert für die Site.

Beispiel 1: Besucher nach Suchbegriff: Ein einzelner Besucher hat ggf. nach mehreren Begriffen gesucht. In diesem Fall entspricht also die Gesamtanzahl der Besucher nicht dem Gesamtwert der Einzelposten.

Beispiel 2: Seitenansichten zu Produkten: Im Warenkorb können sich mehrere Produkte befinden, daher ergeben sich mehrere Seitenansichten für den Warenkorb. Weitere Informationen zum Vergleich der Summe von Einzelposten mit Berichtsgesamtwerten finden Sie in [diesem Artikel der Wissensdatenbank](https://helpx.adobe.com/analytics/kb/sum-line-items-different-from-total.html).
