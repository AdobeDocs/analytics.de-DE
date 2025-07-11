---
description: Erfahren Sie, wie Sie Warnhinweise in Analysis Workspace erstellen.
title: Erstellen von Warnhinweisen
feature: Alerts
exl-id: 82e51357-4a32-4db1-bc56-95a72dbaa1be
source-git-commit: 7945499ab49b488985ff70956c0ee0cd521b1421
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 70%

---

# Erstellen von Warnhinweisen {#create-alerts}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_alerts_timegranularity"
>title="Zeitgranularität"
>abstract="Zeitgranularität bezieht sich darauf, wie oft der Warnhinweis überprüft wird."

<!-- markdownlint-enable MD034 -->

>[!NOTE]
>
>Die Verwendung von Warnhinweisen mit der Anomalieerkennung (auch als _intelligente Warnhinweise_ bezeichnet) ist nur für Organisationen mit einem Adobe Analytics Prime- oder Ultimate-Paket verfügbar.

Warnhinweise in Adobe Analytics ermöglichen es Ihnen, sich über geänderte Prozentsätze oder bestimmte Datenpunkte benachrichtigen zu lassen. Je nach Adobe Analytics-Paket können Sie auch Warnhinweise verwenden, die basierend auf Schwellenwerten für Anomalien ausgelöst werden. Warnhinweise zur Nutzung von Server-Aufrufen sind eine andere Art von Warnhinweisen, die nur Analytics-Admins zur Verfügung stehen. Diese Warnhinweise informieren Sie über das Risiko oder Auftreten einer Überschreitung bei Nutzung und Kontingent von Server-Aufrufen. Weitere Informationen finden Sie unter [Warnhinweise zur Nutzung von Server-Aufrufen](/help/admin/admin/c-server-call-usage/scu-alerts.md).

Weitere Informationen zu Warnhinweisen finden Sie unter [Warnhinweise - Übersicht](intellligent-alerts.md).

So erstellen Sie einen Warnhinweis:

1. Verwenden Sie eine der folgenden Möglichkeiten, um einen Warnhinweis zu erstellen:

   * Öffnen Sie ein Projekt in Analysis Workspace und wählen Sie **[!UICONTROL Komponenten]** > **[!UICONTROL Warnhinweis erstellen]** aus.
   * Öffnen Sie ein Projekt in Analysis Workspace und verwenden Sie dann den folgenden Tastaturbefehl: ***Befehlstaste + Umschalttaste + A*** (macOS) oder ***Strg + Umschalttaste + A*** (Windows).
   * Öffnen Sie ein Projekt in Analysis Workspace, wählen Sie ein oder mehrere Zeilenelemente in einer Freiformtabelle aus, klicken Sie mit der rechten Maustaste darauf und wählen Sie **[!UICONTROL Warnhinweis aus Auswahl erstellen]** aus. Durch diese Aktion wird der [Warnhinweiserstellung“ sofort vorausgefüllt](alert-builder.md) um einen Warnhinweis mit den richtigen Metriken und Filtern zu erstellen.
   * Erstellen Sie einen Warnhinweis [über den Warnhinweis-Manager](/help/components/c-alerts/alert-manager.md#create-alerts).

   Der Warnhinweis-Generator wird angezeigt. Diese Schnittstelle ist mit der Oberfläche zum Erstellen von Segmenten oder berechneten Metriken in Analytics vertraut.



## Warnhinweis-Generator

Die Benutzeroberfläche der Warnhinweiserstellung ähnelt der Oberfläche, die Sie zum Erstellen von Segmenten oder berechneten Metriken in Customer Journey Analytics verwenden:

![Benutzeroberfläche der Warnhinweiserstellung](assets/alert-builder.png)

Geben Sie die folgenden Details im Warnhinweis-Generator für einen Warnhinweis an:

| Element | Beschreibung |
|---------|----------|
| **[!UICONTROL Titel]** | Geben Sie einen Namen für den Warnhinweis an. Der Warnhinweisname könnte den Namen des Berichts oder den Schwellenwert einer Metrik enthalten. |
| **[!UICONTROL Beschreibung (optional)]** | Geben Sie eine Beschreibung für den Warnhinweis an. |
| **[!UICONTROL Zeitgranularität]** | Wählen Sie aus, wie oft die Metrik überprüft werden soll: täglich, wöchentlich oder monatlich.<p> |
| **[!UICONTROL Empfänger]** | Geben Sie an, wo der Warnhinweis hingeschickt werden soll. Ein Warnhinweis kann an einen Analyse-Benutzer, eine Analyse-Gruppe, eine E-Mail-Adresse oder eine Telefonnummer gesendet werden.<p><b>Wichtig</b>: Vor der Telefonnummer müssen eine `+` und eine [Ländercode“ ](https://countrycode.org/).</p><p>Beispiel einer E-Mail, die ein Benutzer erhält:</p><p>![Warninweis-E-Mail](assets/alerts-email.PNG)</p> |
| **[!UICONTROL Ablaufdatum]** | Legen Sie Datum und Uhrzeit fest, zu denen der Warnhinweis ablaufen soll. |
| **[!UICONTROL Verzögerung]** | Die Zeit, die erforderlich ist, bevor Daten vollständig sind und für die Berichterstellung in Customer Journey Analytics zur Verfügung stehen, variiert je nach Organisation und liegt in der Regel 3 bis 9 Stunden nach der Datenereigniszeit. Damit Warnhinweise genau sind, müssen Ereignisdaten für einen bestimmten Ereignisbereich vollständig sein. Das bedeutet, dass Adobe für den angegebenen Ereignisbereich keine Ereignisdaten mehr erhält.<p>Um diese Verzögerung bei der Aufnahmezeit zu berücksichtigen, haben Warnhinweise standardmäßig eine Verzögerung von 9 Stunden, bevor sie gesendet werden.</p><p>Sie können die Standardverzögerung von 9 Stunden auf einen Wert zwischen 0 und 24 Stunden anpassen. Wenn Sie die Verzögerung jedoch auf weniger als 9 Stunden verkürzen, kann dies bedeuten, dass für Berichte unvollständige Daten vorliegen, was zu ungenauen Warnhinweisinformationen führt.</p><p>Beachten Sie beim Verkürzen der Verzögerungszeit Folgendes:</p><ul><li>**Datenverfügbarkeit versus Datenvollständigkeit verstehen**: Alle Batch-Daten werden erst nach einem Zeitraum von 3 bis 9 Stunden in einen Experience Platform-Datensatz aufgenommen. Damit Warnhinweise korrekt sind, muss die Datenaufnahme vollständig sein, wobei alle Batch-Daten im Datensatz verfügbar sein müssen.</li><li>**Bestimmen Sie, wie lange es dauert, bis Ihre Daten vollständig und im Datensatz verfügbar sind**: Die Datenaufnahmezeiten variieren je nach Organisation. Stellen Sie sicher, dass die von Ihnen gewählte Verzögerungszeit für die Bereitstellung von Warnhinweisen genauso lang oder kürzer ist als die Zeit, die benötigt wird, bis die Batch-Daten im Platform-Datensatz verfügbar sind<!--add link? -->.</li><p>**Tipp:** Am genauesten können Sie ermitteln, wie viel Zeit erforderlich ist, damit alle Batch-Daten vollständig sind und in den Platform-Datensatz aufgenommen werden, wenn Sie sich dabei vom Data-Engineering-Team Ihrer Organisation helfen lassen.</p><p>Alternativ können Sie sich einen Überblick darüber verschaffen, wie lange es dauert, bis der Batch-Versand in Ihrer Organisation im Experience Platform-Datensatz verfügbar ist. Erstellen der folgenden Freiformtabelle in Analysis Workspace:</p><ol><li>Fügen Sie in einer Freiformtabelle in Analysis Workspace eine Metrik [!UICONTROL **Ereignisse**] und eine Dimension [!UICONTROL **Tag**] hinzu.</li><li>Schlüsseln Sie die Dimension [!UICONTROL **Tag**] mithilfe einer Dimension [!UICONTROL **Stunden**] auf.<p>Stunden ohne Daten werden als 0 angezeigt.</p></li></ol><li>**Berücksichtigung von Fehlern bei Ihren Berechnungen**: Wenn Sie die standardmäßige Verzögerungszeit verringern, konfigurieren Sie die Verzögerung für mindestens eine Stunde länger als die Zeit, die Ihr Unternehmen für die Vollständigkeit der Datenaufnahme benötigt. Wenn es beispielsweise eine Verzögerung von 3 Stunden gibt, bevor Ihre Datenaufnahme abgeschlossen ist, sollten Sie die Verzögerung auf 4 Stunden festlegen.</li> |
| **[!UICONTROL Einen Warnhinweis senden, wenn]** | [!UICONTROL **Auslösen einer dieser Metriken**]: Ziehen Sie Metriken (einschließlich berechneter Metriken) per Drag-and-Drop hierher, um Trigger für den Warnhinweis zu erstellen.<p>Wenn nicht alle Metriken, Dimensionen oder Segmente des Warnhinweises mit der aktuell ausgewählten Datenansicht kompatibel sind, wird die Meldung **Inkompatible Komponenten** angezeigt.</p><p>Legen Sie den Schwellenwert fest, den die Metrik überschreiten muss, damit ein Warnhinweis ausgegeben wird. Sie können diesen Wert auf einen Schwellenwert und anschließend auf eine der folgenden Bedingungen setzen:</p><ul><li>Anomalie vorhanden</li><li>Anomalie liegt über erwartetem Wert</li><li>Anomalie liegt unter erwartetem Wert</li><li>ist größer oder gleich</li><li>ist kleiner oder gleich</li><li>ändert sich um</li><li>Sie können einen Schwellenwert von 90 %, 95 %, 99 %, 99,75 % und 99,9 % festlegen.</li></ul><p>[!UICONTROL **Mit allen diesen Filtern**]: Ziehen Sie Segmente oder Dimensionen per Drag-and-Drop, um Filter zum Warnhinweis hinzuzufügen. Wenn Sie beispielsweise ein Segment *Nur Mobilgeräte* hinzufügen, bedeutet dies, dass die Regel-Trigger nur für Mobilgeräte gelten. Mit einer AND-Anweisung können Sie zusätzliche Filter hinzufügen. Per Klick auf das Zahnrad-Symbol können Sie AND- oder OR-Regeln hinzufügen.</p><p>Beispiele finden Sie unter [Warnhinweise – Anwendungsfälle](alerts-use-cases.md).</p> |
| **[!UICONTROL Vorschau]** | Die interaktive Warnhinweisvorschau zeigt an, wie oft ein Warnhinweis basierend auf früheren Erfahrungen ausgelöst wird.<p>Beispiel: Wenn Sie die Zeitgranularität auf „Stündlich“ festlegen, kann Ihnen die Vorschau verraten, dass der Warnhinweis zu einer bestimmten Metrik während der letzten 30 oder 31 Tage x-mal ausgelöst worden wäre.</p><p>Wenn Sie feststellen, dass zu viele Warnhinweise ausgelöst werden, können Sie den Schwellenwert im Abschnitt [Verwalten von Warnhinweisen“ ](alert-manager.md).</p><p>![](assets/alert-preview.png){width="50%"}</p> |

<!--

   ![](assets/alert-builder.png)

1. Specify the following options to configure the alert:

   | Option | Description | 
   |---------|----------|
   | [!UICONTROL **Title**]  | Specify a name for the alert. The alert name might contain the name of the report or the metrics threshold. | 
   | [!UICONTROL **Description (optional)**] | Specify a description for the alert. | 
   | [!UICONTROL **Time granularity**] | Select how often you want the metric to be checked: Hourly, Daily, Weekly, or Monthly.<p><b>Note:</b> For report suites with a custom calendar, monthly granularity in the Alert Builder is not supported.<!--true?--</p | 
   | [!UICONTROL **Recipients**] | Specify where the alert can be sent. An alert can be sent to an Analytics user, an Analytics group, a raw email address, or to a phone number.<p><b>Important:</b> The phone number must be preceded by `+` and a [country code](https://countrycode.org/).</p><p>The e-mail that a user would receive once an alert has been triggered looks similar to:</p><p>![](assets/alerts-email.PNG)</p> | 
   | [!UICONTROL **Expiration date**] | Set the date and time when you want the alert to expire. | 
   | [!UICONTROL **Send an alert when**] | [!UICONTROL **Any of these metrics trigger**]: Drag and drop metrics (including calculated metrics) here to create triggers for the alert.<p>An **"incompatible components"** message appears if not all the metrics, dimensions, or segments in the alert are compatible with the currently selected data view.</p><p>Determine the threshold that the metric must exceed before an alert is set. You can set this value to a threshold and then to one of the following conditions:</p><ul><li>anomaly exists</li><li>anomaly is above expected</li><li>anomaly is below expected</li><li>is above or equals</li><li>is below or equals</li><li>changes by</li><li>You can set a threshold of 90%, 95%, 99%, 99.75%, and 99.9%.</li></ul><p>[!UICONTROL **With all of these filters**]: Drag and drop segments or dimensions to add filters. For example, adding a *Mobile Devices Only* segment would mean that the rule triggers only for mobile devices. You can add additional filters by using an AND statement. You can add AND or OR rules by clicking the gear icon.</p><p>See [Alerts - use cases](/help/components/c-alerts/alerts-use-cases.md) for example.</p> | 
   | [!UICONTROL **Preview**] | The interactive alert preview shows you how often, approximately, an alert will fire based on past experience.<p>For example, if you set the time granularity to daily, the preview can tell you that the alert would have been triggered for a certain metric x times during the last 30 or 31 days. The preview approximation window is established by the alert frequency setting. For daily alert frequencies, the preview window approximates the previous 30 days. For weekly alert frequencies, the preview window approximates the last 12 weeks. For monthly alert frequencies, the preview window approximates the previous 12 months.</p><p>If you find that too many alerts will be triggered, you can adjust the threshold in the [Alert Manager](/help/components/c-alerts/alert-manager.md).</p><p>![](assets/alert_preview.png)</p> |

1. Select [!UICONTROL **Save**].

-->