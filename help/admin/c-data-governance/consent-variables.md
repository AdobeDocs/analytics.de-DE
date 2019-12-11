---
description: Variablen für Berichte beim Datenschutz.
title: Variablen für Datenschutzberichte
topic: Admin tools
translation-type: tm+mt
source-git-commit: faade4c02c48ad20e26a94fa39e14ed1d894ae00

---


# Variablen für Datenschutzberichte

Als zusätzliche Unterstützung bei der Verwaltung von Datenschutzdaten stehen eine Reihe reservierter Variablen zur Verfügung, die zusammen mit bestimmten Kontextdatenvariablen verwendet werden können.
Diese Variablen für die Datenschutzberichterstellung bieten ein benutzerfreundliches Framework zur Erfassung des Datenschutzstatus bei jedem Treffer in der Analyse.

## Variablen

* Einwilligungsmanagement Opt-out
   * Reservierte Variable: Listen-Prop
   * Typ: Kommagetrennte Zeichenfolge
   * Enthält:
      * `contextData.['cm.ssf']=1` angezeigt als SSF
      * `contextData.['opt.dmp']=N` angezeigt als DMP
      * `contextData.['opt.sell']=N` angezeigt als SELL

* Einwilligungsmanagement Opt-in
   * Reservierte Variable: Listen-Prop
   * Typ: Kommagetrennte Zeichenfolge
   * Enthält:
      * `contextData.['opt.dmp']=Y` angezeigt als DMP
      * `contextData.['opt.sell']=Y` angezeigt als SELL

## Berichterstellung

Sie können die Variablen für Datenschutzberichte über eine neue Datenschutzeinstellung der Analytics Admin Console aktivieren.

Jede Report Suite kann wie folgt konfiguriert werden:
1. Klicken Sie in „Reports &amp; Analytics“ auf **[!UICONTROL Admin &gt; Report Suites]**.
1. Wählen Sie die Report Suites aus, in denen Sie Mediendaten erfassen, und klicken Sie anschließend auf **[!UICONTROL Einstellungen bearbeiten &gt; Datenschutzmanagement]**.

   ![](assets/rsm-privacy-select.png)

1. Klicken Sie auf den Button **[!UICONTROL Datenschutzberichte aktivieren.]**

   > [!NOTE] Nach der Aktivierung können diese Variablen nicht mehr deaktiviert werden.

   ![](assets/rsm-privacy-enable.png)

1. Nach der Aktivierung wird eine Bestätigungsmeldung angezeigt.

   ![](assets/rsm-privacy-config.png)

1. Die reservierten Variablen stehen jetzt für die Berichterstellung zur Verfügung.  Siehe „Einwilligungsmanagement Opt-out und Opt-in“.

   ![](assets/rsm-privacy-reports.png)

## Implementierung

Drei Kontextdatenvariablen sind vordefiniert, um mit den vom Datenschutzmanagement reservierten Variablen zu arbeiten.  Die Bestimmung der Verwaltung und des Beibehaltens der Einstellung dieser Variablen liegt bei den einzelnen Implementierungstechnikern.

Allgemeine Anleitungen zur Implementierung von Kontextdatenvariablen finden Sie unter [Kontextdatenvariablen](https://docs.adobe.com/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/context-data-variables.html).

### SSF

* Kontextdaten: `contextData.['cm.ssf']`
* Akzeptierte Werte:
   * 1 – Wenn der Wert „1“gesendet wird, bedeutet dies, dass die serverseitige Weiterleitung einen Opt-out-Status aufweist. Der Wert „1“ in Verbindung mit dieser Variablen blockiert die Freigabe dieses Treffers für Adobe Audience Manager. Siehe [AAM-ePrivacy – Einhaltung](https://docs.adobe.com/help/en/analytics/integration/audience-analytics/audience-analytics-workflow/ssf-gdpr.html).
   * 0 - Optional. Verwenden Sie den Wert "0"für Kunden, die zielgerichtetem Marketing zugestimmt haben. Wenn Sie die Variable nicht festlegen, führt dies ebenfalls zu denselben Ergebnissen.

### DMP

* Kontextdaten: `contextData.['opt.dmp']`
* Akzeptierte Werte:
   * N – Wenn der Wert „N“ gesendet wird, deutet dies darauf hin, dass der Verbraucher die Freigabe für Daten-Management-Plattformen ablehnt. **Hinweis**: Wenn für diese Variable „N“ festgelegt ist, wird die Freigabe für AAM derzeit nicht blockiert. Jedoch wird Anfang 2020 das Blockieren von AAM-Aufrufen hinzugefügt. Adobe empfiehlt zunächst, das Einstellen sowohl von `c.cm.ssf=1` als auch `c.opt.dmp=N`, um das Senden von Treffern an AAM zu verhindern.
   * Y – Wenn der Wert „Y“ gesendet wird, deutet dies darauf hin, dass der Verbraucher die Freigabe für Daten-Management-Plattformen genehmigt.

### SELL

* Kontextdaten: `contextData.['opt.sell']`
* Akzeptierte Werte:
   * N – Wenn der Wert „N“ gesendet wird, deutet dies darauf hin, dass der Verbraucher die Freigabe oder den Verkauf der Daten an Dritte ablehnt.
   * Y – Wenn der Wert „Y“ gesendet wird, deutet dies darauf hin, dass der Verbraucher die Freigabe oder den Verkauf der Daten an Dritte genehmigt.
