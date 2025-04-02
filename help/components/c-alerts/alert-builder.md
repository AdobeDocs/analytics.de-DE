---
description: Verwenden Sie Warnhinweise in Analysis Workspace.
title: Überblick über den Warnhinweis-Generator
feature: Alerts
exl-id: 82e51357-4a32-4db1-bc56-95a72dbaa1be
source-git-commit: 966bd9a05e6c344a62ce3f0b12df8a99ff3d7ece
workflow-type: ht
source-wordcount: '695'
ht-degree: 100%

---

# Erstellen von Warnhinweisen {#create-alerts}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_alerts_timegranularity"
>title="Zeitgranularität"
>abstract="Zeitgranularität bezieht sich sowohl darauf, wie oft der Warnhinweis überprüft wird, als auch darauf, was eingeschlossen wird"

<!-- markdownlint-enable MD034 -->

>[!NOTE]
>
>Die Verwendung von Warnhinweisen mit der Anomalieerkennung (auch als _intelligente Warnhinweise_ bezeichnet) ist nur für Organisationen mit einem Adobe Analytics Prime- oder Ultimate-Paket verfügbar.

Warnhinweise in Adobe Analytics ermöglichen es Ihnen, sich über geänderte Prozentsätze oder bestimmte Datenpunkte benachrichtigen zu lassen. Je nach Adobe Analytics-Paket können Sie auch Warnhinweise verwenden, die basierend auf Schwellenwerten für Anomalien ausgelöst werden. Warnhinweise zur Nutzung von Server-Aufrufen sind eine andere Art von Warnhinweisen, die nur Analytics-Admins zur Verfügung stehen. Diese Warnhinweise informieren Sie über das Risiko oder Auftreten einer Überschreitung bei Nutzung und Kontingent von Server-Aufrufen. Weitere Informationen finden Sie unter [Warnhinweise zur Nutzung von Server-Aufrufen](/help/admin/admin/c-server-call-usage/scu-alerts.md).

Weitere Übersichtsinformationen zu Warnhinweisen finden Sie unter [Warnhinweise – Überblick](/help/components/c-alerts/intellligent-alerts.md).

So erstellen Sie einen Warnhinweis:

1. Beginnen Sie mit der Erstellung eines Warnhinweises, indem Sie auf den Warnhinweis-Generator zugreifen. Sie können den Warnhinweis-Generator mit einer der folgenden Möglichkeiten aufrufen:

   * Öffnen Sie ein Projekt in Analysis Workspace und wählen Sie **[!UICONTROL Komponenten]** > **[!UICONTROL Warnhinweis erstellen]** aus.
   * Öffnen Sie ein Projekt in Analysis Workspace und verwenden Sie dann den folgenden Tastaturbefehl: ***Strg (bzw. Befehlstaste)+Umschalt+a***.
   * Öffnen Sie ein Projekt in Analysis Workspace, wählen Sie ein oder mehrere Zeilenelemente in einer Freiformtabelle aus, klicken Sie mit der rechten Maustaste darauf und wählen Sie **[!UICONTROL Warnhinweis aus Auswahl erstellen]** aus. Dadurch wird der Warnhinweis-Generator unverzüglich mit den entsprechenden Werten aufgefüllt, um einen Warnhinweis mit den korrekten Metriken und Filtern zu erstellen.
   * Erstellen Sie einen Warnhinweis [über den Warnhinweis-Manager](/help/components/c-alerts/alert-manager.md#create-alerts).

   Der Warnhinweis-Generator wird angezeigt. Diese Oberfläche ähnelt der zum Erstellen von Segmenten oder berechneten Metriken in Analytics:

   ![](assets/alert-builder.png)

1. Geben Sie die folgenden Optionen zum Konfigurieren des Warnhinweises an:

   | Option | Beschreibung |
   |---------|----------|
   | [!UICONTROL **Titel**] | Geben Sie einen Namen für den Warnhinweis an. Der Warnhinweisname könnte den Namen des Berichts oder den Schwellenwert einer Metrik enthalten. |
   | [!UICONTROL **Beschreibung (optional**] | Geben Sie eine Beschreibung für den Warnhinweis an.  |
   | [!UICONTROL **Zeitgranularität**] | Wählen Sie aus, wie oft die Metrik überprüft werden soll: stündlich, täglich, wöchentlich oder monatlich.<p><b>Hinweis:</b> Bei Report Suites mit einem benutzerdefinierten Kalender wird die monatliche Granularität im Warnhinweis-Generator nicht unterstützt.<!--true?--></p> |
   | [!UICONTROL **Empfänger**] | Geben Sie an, wo der Warnhinweis hingeschickt werden soll. Ein Warnhinweis kann an einen Analyse-Benutzer, eine Analyse-Gruppe, eine E-Mail-Adresse oder eine Telefonnummer gesendet werden.<p><b>Wichtig:</b> Die Telefonnummer muss über ein vorangestelltes Pluszeichen (`+`) und eine [Landesvorwahl](https://countrycode.org/) verfügen.</p><p>Die E-Mail, die eine Person erhalten würde, sobald ein Warnhinweis ausgelöst wird, sieht in etwa so aus:</p><p>![](assets/alerts-email.PNG)</p> |
   | [!UICONTROL **Ablaufdatum**] | Legen Sie Datum und Uhrzeit fest, zu denen der Warnhinweis ablaufen soll. |
   | [!UICONTROL **Einen Warnhinweis senden, wenn**] | [!UICONTROL **Auslösen einer dieser Metriken**]: Ziehen Sie Metriken (einschließlich berechneter Metriken) per Drag-and-Drop hierher, um Trigger für den Warnhinweis zu erstellen.<p>Wenn nicht alle Metriken, Dimensionen oder Segmente des Warnhinweises mit der aktuell ausgewählten Datenansicht kompatibel sind, wird die Meldung **„Inkompatible Komponenten“** angezeigt.</p><p>Legen Sie den Schwellenwert fest, den die Metrik überschreiten muss, damit ein Warnhinweis ausgegeben wird. Sie können diesen Wert auf einen Schwellenwert und anschließend auf eine der folgenden Bedingungen setzen:</p><ul><li>Anomalie vorhanden</li><li>Anomalie liegt über erwartetem Wert</li><li>Anomalie liegt unter erwartetem Wert</li><li>ist größer oder gleich</li><li>ist kleiner oder gleich</li><li>ändert sich um</li><li>Sie können einen Schwellenwert von 90 %, 95 %, 99 %, 99,75 % und 99,9 % festlegen.</li></ul><p>[!UICONTROL **Mit allen diesen Filtern**]: Ziehen Sie Segmente oder Dimensionen per Drag-and-Drop in dieses Feld, um Filter hinzuzufügen. Wenn Sie zum Beispiel ein Segment vom Typ „Nur Mobilgeräte“ hinzufügen, würde die Regel nur für Mobilgeräte ausgelöst werden. Mit einer AND-Anweisung können Sie zusätzliche Filter hinzufügen. Per Klick auf das Zahnrad-Symbol können Sie AND- oder OR-Regeln hinzufügen.</p><p>Ein Beispiel finden Sie unter [Warnhinweise – Anwendungsszenarien](/help/components/c-alerts/alerts-use-cases.md).</p> |
   | [!UICONTROL **Vorschau**] | Die interaktive Warnhinweisvorschau zeigt Ihnen basierend auf Daten aus der Vergangenheit, wie oft damit zu rechnen ist, dass ein Warnhinweis ausgelöst wird.<p>Beispiel: Wenn Sie die Zeitgranularität auf „Stündlich“ festlegen, kann Ihnen die Vorschau verraten, dass der Warnhinweis zu einer bestimmten Metrik während der letzten 30 oder 31 Tage x-mal ausgelöst worden wäre. Das Vorschaufenster mit der ungefähren Anzahl der Warnhinweise wird durch die Einstellung des Warnungsintervalls festgelegt. Für tägliche Warnungsintervalle beinhaltet das Vorschaufenster die ungefähre Anzahl der Warnhinweise der vorherigen 30 Tage. Für wöchentliche Warnungsintervalle beinhaltet das Vorschaufenster die ungefähre Anzahl der Warnhinweise der letzten 12 Wochen. Für monatliche Warnungsintervalle beinhaltet das Vorschaufenster die ungefähre Anzahl der Warnhinweise der vorherigen 12 Monate.</p><p>Wenn Sie feststellen, dass Warnhinweise zu oft ausgelöst werden, können Sie den Schwellenwert im [Warnhinweis-Manager](/help/components/c-alerts/alert-manager.md) anpassen.</p><p>![](assets/alert_preview.png)</p> |

1. Wählen Sie [!UICONTROL **Speichern**] aus.
