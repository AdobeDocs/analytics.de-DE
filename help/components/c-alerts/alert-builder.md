---
description: Verwenden Sie Warnhinweise in Analysis Workspace.
title: Warnhinweiserstellung - Übersicht
feature: Alerts
exl-id: 82e51357-4a32-4db1-bc56-95a72dbaa1be
source-git-commit: 815e50e30fa6a0bce1bf78f33843070f96f52de8
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 36%

---

# Erstellen von Warnhinweisen

>[!NOTE]
>
>Die Verwendung von Warnhinweisen mit Anomalieerkennung (auch _Intelligente Warnhinweise_ genannt) ist nur für Unternehmen mit einem Adobe Analytics Select-, Prime- oder Ultimate-Paket verfügbar.

Warnhinweise in Adobe Analytics ermöglichen es Ihnen, über geänderte Prozentsätze oder bestimmte Datenpunkte benachrichtigt zu werden. Je nach Adobe Analytics-Package können Sie Warnhinweise auch verwenden, die basierend auf Anomalieschwellen ausgelöst werden. (Warnhinweise zur Nutzung von Server-Aufrufen sind eine andere Art von Warnhinweisen, die nur für Analytics-Administratoren verfügbar sind. Diese Warnhinweise informieren Sie über das Risiko oder das Auftreten einer Überschreitung der Verbrauchs- und Zusagedaten für Server-Aufrufe. Weitere Informationen finden Sie unter [Warnhinweise zur Nutzung von Server-Aufrufen](/help/admin/admin/c-server-call-usage/scu-alerts.md).)

Detaillierte Übersichtsinformationen zu Warnhinweisen finden Sie unter [Warnhinweise - Übersicht](/help/components/c-alerts/intellligent-alerts.md).

So erstellen Sie einen Warnhinweis:

1. Beginnen Sie mit der Erstellung eines Warnhinweises, indem Sie auf die Warnhinweiserstellung zugreifen. Sie haben folgende Möglichkeiten, auf den Warnhinweiserstellung zuzugreifen:

   * Öffnen Sie ein Projekt in Analysis Workspace und wählen Sie dann **[!UICONTROL Komponenten]** > **[!UICONTROL Warnhinweis erstellen]** aus.
   * Öffnen Sie ein Projekt in Analysis Workspace und verwenden Sie dann die folgende Verknüpfung:

     `ctrl (or cmd) + shift + a`
   * Öffnen Sie ein Projekt in Analysis Workspace, wählen Sie mindestens ein Zeilenelement in einer Freiformtabelle aus, klicken Sie mit der rechten Maustaste darauf und wählen Sie **[!UICONTROL Warnhinweis aus Auswahl erstellen]** aus.

     Dadurch wird der Warnhinweiserstellung sofort vorausgefüllt, um einen Warnhinweis mit den richtigen Metriken und Filtern zu erstellen.
   * Erstellen Sie einen Warnhinweis [ vom Warnhinweis-Manager](/help/components/c-alerts/alert-manager.md#create-alerts).

   Die Warnhinweiserstellung wird angezeigt. Diese Benutzeroberfläche ist mit jenen vertraut, die Segmente oder berechnete Metriken in Analytics erstellt haben:

   ![](assets/alert-builder.png)

1. Geben Sie die folgenden Optionen zum Konfigurieren des Warnhinweises an:

   | Option | Beschreibung |
   |---------|----------|
   | [!UICONTROL **Titel**] | Geben Sie einen Namen für den Warnhinweis an. Der Warnhinweisname könnte den Namen des Berichts oder den Schwellenwert einer Metrik enthalten. |
   | [!UICONTROL **Beschreibung (optional)**] | Geben Sie eine Beschreibung für den Warnhinweis an. |
   | [!UICONTROL **Zeitgranularität**] | Wählen Sie aus, wie oft die Metrik überprüft werden soll: täglich, wöchentlich oder monatlich.<p><b>Hinweis:</b>Bei Datenansichten mit einem benutzerdefinierten Kalender wird die monatliche Granularität in der Warnhinweiserstellung nicht unterstützt.<!--true?--></p> |
   | [!UICONTROL **Empfänger**] | Geben Sie an, wo der Warnhinweis hingeschickt werden soll. Ein Warnhinweis kann an einen Analyse-Benutzer, eine Analyse-Gruppe, eine E-Mail-Adresse oder eine Telefonnummer gesendet werden.<p><b>Wichtig:</b>Der Telefonnummer muss ein &quot;+&quot;- und ein &quot;[Ländercode](https://countrycode.org/)&quot; vorangestellt werden.</p><p>Die E-Mail, die ein Benutzer erhalten würde, sobald ein Warnhinweis ausgelöst wurde, sieht in etwa so aus:</p><p>![](assets/alerts-email.PNG)</p> |
   | [!UICONTROL **Ablaufdatum**] | Legen Sie Datum und Uhrzeit für den Ablauf des Warnhinweises fest. |
   | [!UICONTROL **Warnhinweis senden, wenn**] | [!UICONTROL **Jeder dieser Metriken Trigger**]: Ziehen Sie Metriken (einschließlich berechneter Metriken) hierher, um Trigger für den Warnhinweis zu erstellen.<p>Wenn nicht alle Metriken, Dimensionen oder Segmente im Warnhinweis mit der aktuell ausgewählten Datenansicht kompatibel sind, wird die Meldung **&quot;Nicht kompatible Komponenten&quot;** angezeigt.</p><p>Legen Sie den Schwellenwert fest, den die Metrik überschreiten muss, damit ein Warnhinweis ausgegeben wird. Sie können diesen Wert auf einen Schwellenwert und anschließend auf eine der folgenden Bedingungen setzen:</p><ul><li>Anomalie vorhanden</li><li>Anomalie liegt über erwartetem Wert</li><li>Anomalie liegt unter erwartetem Wert</li><li>ist größer oder gleich</li><li>ist kleiner oder gleich</li><li>ändert sich um</li><li>Sie können einen Schwellenwert von 90 %, 95 %, 99 %, 99,75 % und 99,9 % festlegen.</li></ul><p>[!UICONTROL **Mit all diesen Filtern**]: Ziehen Sie Segmente oder Dimensionen per Drag-and-Drop, um Filter hinzuzufügen. Wenn Sie beispielsweise das Segment &quot;Nur Mobilgeräte&quot;hinzufügen, würde die Regel nur für Mobilgeräte Trigger. Mithilfe einer AND-Anweisung können Sie weitere Filter hinzufügen. Per Klick auf das Zahnrad-Symbol können Sie AND- oder OR-Regeln hinzufügen.</p><p>Siehe [Warnhinweise - Anwendungsbeispiele](/help/components/c-alerts/alerts-use-cases.md) .</p> |
   | [!UICONTROL **Vorschau**] | Die interaktive Warnhinweisvorschau zeigt Ihnen basierend auf Daten aus der Vergangenheit, wie oft damit zu rechnen ist, dass ein Warnhinweis ausgelöst wird.<p>Beispiel: Wenn Sie die Zeitgranularität auf „Stündlich“ festlegen, kann Ihnen die Vorschau verraten, dass der Warnhinweis zu einer bestimmten Metrik während der letzten 30 oder 31 Tage x-mal ausgelöst worden wäre.</p><p>Wenn Sie feststellen, dass Warnhinweise zu oft ausgelöst werden würden, können Sie den Schwellenwert im [Warnhinweis-Manager](/help/components/c-alerts/alert-manager.md) anpassen.</p><p>![](assets/alert_preview.png)</p> |

1. Wählen Sie [!UICONTROL **Speichern**] aus.
