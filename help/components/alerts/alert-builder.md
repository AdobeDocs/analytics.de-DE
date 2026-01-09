---
description: Erfahren Sie, wie Sie Warnhinweise in Analysis Workspace erstellen.
title: Erstellen von Warnhinweisen
feature: Alerts
exl-id: 82e51357-4a32-4db1-bc56-95a72dbaa1be
source-git-commit: f02b660b551f5291443b8f7c5c51179a06b22eb9
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 85%

---

# Erstellen von Warnhinweisen {#create-alerts}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_alerts_timegranularity"
>title="Zeitgranularität"
>abstract="Die Zeitgranularität bestimmt, wie oft der Warnhinweis überprüft wird. "

<!-- markdownlint-enable MD034 -->

>[!NOTE]
>
>Die Verwendung von Warnhinweisen mit der Anomalieerkennung (auch als _intelligente Warnhinweise_ bezeichnet) ist nur für Organisationen mit einem Adobe Analytics Prime- oder Ultimate-Paket verfügbar.

Warnhinweise in Adobe Analytics ermöglichen es Ihnen, sich über geänderte Prozentsätze oder bestimmte Datenpunkte benachrichtigen zu lassen. Je nach Adobe Analytics-Paket können Sie auch Warnhinweise verwenden, die basierend auf Schwellenwerten für Anomalien ausgelöst werden. Warnhinweise zur Nutzung von Server-Aufrufen sind eine andere Art von Warnhinweisen, die nur Analytics-Admins zur Verfügung stehen. Diese Warnhinweise informieren Sie über das Risiko oder Auftreten einer Überschreitung bei Nutzung und Kontingent von Server-Aufrufen. Weitere Informationen finden Sie unter [Warnhinweise zur Nutzung von Server-Aufrufen](/help/admin/tools/server-call-usage/scu-alerts.md).

Ausführlichere Informationen zu Warnhinweisen finden Sie unter [Warnhinweise – Überblick](alerts-overview.md).

So erstellen Sie einen Warnhinweis:

1. Verwenden Sie eine der folgenden Methoden, um einen Warnhinweis zu erstellen:

   * Öffnen Sie ein Projekt in Analysis Workspace und wählen Sie **[!UICONTROL Komponenten]** > **[!UICONTROL Warnhinweis erstellen]** aus.
   * Öffnen Sie ein Projekt in Analysis Workspace und verwenden Sie dann den folgenden Tastaturbefehl: ***Befehlstaste+Umschalttaste+A*** (macOS) oder ***Strg+Umschalttaste+A*** (Windows).
   * Öffnen Sie ein Projekt in Analysis Workspace, wählen Sie ein oder mehrere Zeilenelemente in einer Freiformtabelle aus, klicken Sie mit der rechten Maustaste darauf und wählen Sie **[!UICONTROL Warnhinweis aus Auswahl erstellen]** aus. Dadurch wird der [Warnhinweis-Generator](alert-builder.md) unmittelbar mit den entsprechenden Werten gefüllt, damit ein Warnhinweis mit den korrekten Metriken und Filtern erstellt werden kann.
   * Erstellen Sie einen Warnhinweis [über den Warnhinweis-Manager](/help/components/alerts/alert-manager.md#create-alerts).

   Der Warnhinweis-Generator wird angezeigt. Diese Oberfläche ähnelt der zum Erstellen von Segmenten oder berechneten Metriken in Analytics.



## Warnhinweis-Generator

Die Benutzeroberfläche des Warnhinweis-Generators ähnelt der Oberfläche, die Sie zum Erstellen von Segmenten oder berechneten Metriken in Customer Journey Analytics verwenden:

![Benutzeroberfläche des Warnhinweis-Generators](assets/alert-builder.png)

Geben Sie die folgenden Details im Warnhinweis-Generator für einen Warnhinweis an:

| Element | Beschreibung |
|---------|----------|
| **[!UICONTROL Titel]** | Geben Sie einen Namen für den Warnhinweis an. Der Name des Warnhinweises kann den Namen des Berichts oder den Schwellenwert für die Metriken enthalten. |
| **[!UICONTROL Beschreibung (optional)]** | Geben Sie eine Beschreibung für den Warnhinweis an. |
| **[!UICONTROL Zeitgranularität]** | Wählen Sie aus, wie oft die Metrik überprüft werden soll: täglich, wöchentlich oder monatlich.<p> |
| **[!UICONTROL Empfänger]** | Geben Sie an, wo der Warnhinweis hingeschickt werden soll. Ein Warnhinweis kann an einen Analytics-Benutzer, eine Analytics-Gruppe, eine unformatierte E-Mail-Adresse oder an eine Telefonnummer gesendet werden.<p><b>Wichtig:</b> Die Telefonnummer muss über ein vorangestelltes `+` und eine [Landesvorwahl](https://countrycode.org/) verfügen.</p><p>Beispiel-E-Mail an Benutzende:</p><p>![Warninweis-E-Mail](assets/alerts-email.PNG)</p> |
| **[!UICONTROL Ablaufdatum]** | Legen Sie Datum und Uhrzeit fest, zu denen der Warnhinweis ablaufen soll. |
| **[!UICONTROL Verzögerung]** | Die Zeit, die erforderlich ist, bevor Daten vollständig sind und für die Berichterstellung in Customer Journey Analytics zur Verfügung stehen, variiert je nach Organisation und liegt in der Regel 3 bis 9 Stunden nach der Datenereigniszeit. Damit Warnhinweise genau sind, müssen Ereignisdaten für einen bestimmten Ereignisbereich vollständig sein. Das bedeutet, dass Adobe für den angegebenen Ereignisbereich keine Ereignisdaten mehr erhält.<p>Um diese Verzögerung bei der Aufnahmezeit zu berücksichtigen, haben Warnhinweise standardmäßig eine Verzögerung von 9 Stunden, bevor sie gesendet werden.</p><p>Sie können die Standardverzögerung von 9 Stunden auf einen Wert zwischen 0 und 24 Stunden anpassen. Wenn Sie die Verzögerung jedoch auf weniger als 9 Stunden verkürzen, kann dies bedeuten, dass für Berichte unvollständige Daten vorliegen, was zu ungenauen Warnhinweisinformationen führt.</p><p>Beachten Sie beim Verkürzen der Verzögerungszeit Folgendes:</p><ul><li>**Unterschied zwischen Datenverfügbarkeit und Datenvollständigkeit:** Alle Batch-Daten werden erst nach 3 bis 9 Stunden in einen Experience Platform-Datensatz aufgenommen. Damit Warnhinweise korrekt sind, muss die Datenaufnahme vollständig sein, wobei alle Batch-Daten im Datensatz verfügbar sein müssen.</li><li>**Bestimmen Sie, wie lange es dauert, bis Ihre Daten vollständig und im Datensatz verfügbar sind**: Die Datenaufnahmezeiten variieren je nach Organisation. Stellen Sie sicher, dass die von Ihnen gewählte Verzögerungszeit für die Bereitstellung von Warnhinweisen genauso lang oder kürzer ist als die Zeit, die benötigt wird, bis die Batch-Daten im Platform-Datensatz verfügbar sind<!--add link? -->.</li><p>**Tipp:** Am genauesten können Sie ermitteln, wie viel Zeit erforderlich ist, damit alle Batch-Daten vollständig sind und in den Platform-Datensatz aufgenommen werden, wenn Sie sich dabei vom Data-Engineering-Team Ihrer Organisation helfen lassen.</p><p>Alternativ können Sie sich einen allgemeinen Überblick darüber verschaffen, wie lange es dauert, bis die Batch-Bereitstellung in Ihrer Organisation im Experience Platform-Datensatz verfügbar ist. Erstellen der folgenden Freiformtabelle in Analysis Workspace:</p><ol><li>Fügen Sie in einer Freiformtabelle in Analysis Workspace eine Metrik [!UICONTROL **Ereignisse**] und eine Dimension [!UICONTROL **Tag**] hinzu.</li><li>Schlüsseln Sie die Dimension [!UICONTROL **Tag**] mithilfe einer Dimension [!UICONTROL **Stunden**] auf.<p>Stunden ohne Daten werden mit dem Wert „0“ angezeigt.</p></li></ol><li>**Berücksichtigen Sie mögliche Fehler in Ihren Berechnungen**: Wenn Sie die standardmäßige Verzögerungszeit verringern, konfigurieren Sie sie so, dass die Verzögerung mindestens eine Stunde länger ist als die von Ihrer Organisation für eine vollständige Datenaufnahme benötigte Zeit. Wenn es beispielsweise eine Verzögerung von 3 Stunden gibt, bevor Ihre Datenaufnahme abgeschlossen ist, sollten Sie die Verzögerung auf 4 Stunden festlegen.</li> |
| **[!UICONTROL Einen Warnhinweis senden, wenn]** | [!UICONTROL **Trigger einer dieser Metriken**]: <ol><li>Ziehen Sie Metriken (einschließlich berechneter Metriken) per Drag-and-Drop in den entsprechenden Bereich, um Trigger für den Warnhinweis zu erstellen.<p>Eine *Inkompatible Komponenten*-Meldung wird angezeigt, wenn nicht alle Metriken, Dimensionen oder Segmente des Warnhinweises mit der aktuell ausgewählten Report Suite kompatibel sind.</p><p>Bestimmen Sie den Schwellenwert (für eine Anomalie), den die Metrik überschreiten muss, oder den Wert (im Fall von Über-, Unter-, Gleich- oder Prozentänderung), der verwendet werden soll, bevor ein Warnhinweis festgelegt wird.</li><li>Wählen Sie eine der folgenden Bedingungen aus:<ul><li>Anomalie vorhanden</li><li>Anomalie liegt über den Erwartungen</li><li>Anomalie liegt unter den Erwartungen</li><li>Ist über oder gleich</li><li>ist kleiner oder gleich</li><li>Änderungen von</li></ul></li><li>Wählen Sie einen Schwellenwert aus oder geben Sie einen Wert ein.</li></ol>[!UICONTROL **Mit allen diesen Filtern**]: Ziehen Sie Segmente oder Dimensionen per Drag-and-Drop, um dem Warnhinweis Filter hinzuzufügen. Wenn Sie zum Beispiel ein Segment vom Typ *Nur Mobilgeräte* hinzufügen, würde die Regel nur für Mobilgeräte ausgelöst werden. Mit einer AND-Anweisung können Sie zusätzliche Filter hinzufügen. Per Klick auf das Zahnrad-Symbol können Sie AND- oder OR-Regeln hinzufügen.</p><p>Beispiele finden Sie unter [Warnhinweise – Anwendungsfälle](alerts-use-cases.md).</p> |
| **[!UICONTROL Vorschau]** | Die interaktive Warnhinweisvorschau zeigt Ihnen basierend auf Daten aus der Vergangenheit, wie oft ein Warnhinweis in etwa ausgelöst wird.<p>Beispiel: Wenn Sie die Zeitgranularität auf „Stündlich“ festlegen, kann Ihnen die Vorschau verraten, dass der Warnhinweis zu einer bestimmten Metrik während der letzten 30 oder 31 Tage x-mal ausgelöst worden wäre.</p><p>Wenn Sie der Ansicht sind, dass Warnhinweise zu oft ausgelöst werden, können Sie den Schwellenwert unter [Warnhinweise verwalten](alert-manager.md) anpassen.</p><p>![](assets/alert-preview.png){width="50%"}</p> |
