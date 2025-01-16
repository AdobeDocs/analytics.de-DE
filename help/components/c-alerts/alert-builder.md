---
description: Verwenden Sie Warnhinweise in Analysis Workspace.
title: Übersicht über die Warnhinweiserstellung
feature: Alerts
exl-id: 82e51357-4a32-4db1-bc56-95a72dbaa1be
source-git-commit: 75d8705170169a0ef9f1ee59b12e4bb2c3afac7a
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 32%

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
>Die Verwendung von Warnhinweisen mit Anomalieerkennung (auch _intelligente Warnhinweise_ genannt) ist nur für Unternehmen mit einem Adobe Analytics Prime- oder Ultimate-Paket verfügbar.

Warnhinweise in Adobe Analytics ermöglichen die Benachrichtigung anhand geänderter Prozentsätze oder bestimmter Datenpunkte. Je nach Adobe Analytics-Paket können Sie auch Warnhinweise verwenden, die auf der Grundlage von Anomalieschwellen ausgelöst werden. Warnhinweise zur Nutzung von Server-Aufrufen sind eine andere Art von Warnhinweis, der nur für Analytics-Admins verfügbar ist. Diese Warnhinweise informieren Sie über das Risiko oder Auftreten eines Überschusses in den Daten über den Verbrauch und die Zusage von Server-Aufrufen. Weitere Informationen finden Sie unter [Warnhinweise zur Nutzung von Server-Aufrufen](/help/admin/admin/c-server-call-usage/scu-alerts.md).

Weitere Übersichtsinformationen zu Warnhinweisen finden Sie unter [Warnhinweise - Übersicht](/help/components/c-alerts/intellligent-alerts.md).

So erstellen Sie einen Warnhinweis:

1. Beginnen Sie mit der Erstellung eines Warnhinweises, indem Sie auf die Warnhinweiserstellung zugreifen. Sie können auf eine der folgenden Arten auf die Warnhinweiserstellung zugreifen:

   * Öffnen Sie ein Projekt in Analysis Workspace und wählen Sie **[!UICONTROL Komponenten]** > **[!UICONTROL Warnhinweis erstellen]**.
   * Öffnen Sie ein Projekt in Analysis Workspace und verwenden Sie dann den folgenden Tastaturbefehl: ***Strg (oder Befehl) + Umschalt + a***.
   * Öffnen Sie ein Projekt in Analysis Workspace, wählen Sie ein oder mehrere Zeilenelemente in einer Freiformtabelle aus, klicken Sie mit der rechten Maustaste darauf und wählen Sie **[!UICONTROL Warnhinweis aus Auswahl erstellen]**. Durch diese Aktion wird die Warnhinweiserstellung sofort vorab ausgefüllt, um einen Warnhinweis mit den richtigen Metriken und Filtern zu erstellen.
   * Erstellen eines Warnhinweises [aus dem Warnhinweis-Manager](/help/components/c-alerts/alert-manager.md#create-alerts).

   Die Warnhinweiserstellung wird angezeigt. Diese Schnittstelle ist mit der Oberfläche zum Erstellen von Segmenten oder berechneten Metriken in Analytics vertraut:

   ![](assets/alert-builder.png)

1. Geben Sie die folgenden Optionen zum Konfigurieren des Warnhinweises an:

   | Option | Beschreibung |
   |---------|----------|
   | [!UICONTROL **Titel**] | Geben Sie einen Namen für den Warnhinweis an. Der Warnhinweisname könnte den Namen des Berichts oder den Schwellenwert einer Metrik enthalten. |
   | [!UICONTROL **Beschreibung (optional)**] | Geben Sie eine Beschreibung für den Warnhinweis an. |
   | [!UICONTROL **Zeitgranularität**] | Wählen Sie aus, wie oft die Metrik überprüft werden soll: stündlich, täglich, wöchentlich oder monatlich.<p><b>Hinweis:</b> Bei Report Suites mit einem benutzerdefinierten Kalender wird die monatliche Granularität im Warnhinweis-Builder nicht unterstützt.<!--true?--></p> |
   | [!UICONTROL **Empfänger**] | Geben Sie an, wo der Warnhinweis hingeschickt werden soll. Ein Warnhinweis kann an einen Analyse-Benutzer, eine Analyse-Gruppe, eine E-Mail-Adresse oder eine Telefonnummer gesendet werden.<p><b>Wichtig:</b> Vor der Telefonnummer müssen `+` und eine [Landesvorwahl](https://countrycode.org/) stehen.</p><p>Die E-Mail-Adresse, die ein Benutzer erhalten würde, sobald ein Warnhinweis ausgelöst wurde, sieht in etwa so aus:</p><p>![](assets/alerts-email.PNG)</p> |
   | [!UICONTROL **Ablaufdatum**] | Datum und Uhrzeit festlegen, zu der der Warnhinweis ablaufen soll. |
   | [!UICONTROL **Warnhinweis senden, wenn**] | [!UICONTROL **Trigger einer dieser Metriken**]: Ziehen Sie Metriken (einschließlich berechneter Metriken) per Drag-and-Drop hierher, um Trigger für den Warnhinweis zu erstellen.<p>Eine **Meldung „Inkompatible Komponenten** wird angezeigt, wenn nicht alle Metriken, Dimensionen oder Segmente im Warnhinweis mit der aktuell ausgewählten Datenansicht kompatibel sind.</p><p>Legen Sie den Schwellenwert fest, den die Metrik überschreiten muss, damit ein Warnhinweis ausgegeben wird. Sie können diesen Wert auf einen Schwellenwert und anschließend auf eine der folgenden Bedingungen setzen:</p><ul><li>Anomalie vorhanden</li><li>Anomalie liegt über erwartetem Wert</li><li>Anomalie liegt unter erwartetem Wert</li><li>ist größer oder gleich</li><li>ist kleiner oder gleich</li><li>ändert sich um</li><li>Sie können einen Schwellenwert von 90 %, 95 %, 99 %, 99,75 % und 99,9 % festlegen.</li></ul><p>[!UICONTROL **Mit allen diesen Filtern**]: Ziehen Sie Segmente oder Dimensionen per Drag-and-Drop, um Filter hinzuzufügen. Wenn Sie beispielsweise das Segment „Nur Mobilgeräte“ hinzufügen, bedeutet dies, dass die Regel-Trigger nur für Mobilgeräte gelten. Mit einer AND-Anweisung können Sie zusätzliche Filter hinzufügen. Per Klick auf das Zahnrad-Symbol können Sie AND- oder OR-Regeln hinzufügen.</p><p>Siehe [Warnhinweise - Anwendungsfälle](/help/components/c-alerts/alerts-use-cases.md) zum Beispiel.</p> |
   | [!UICONTROL **Vorschau**] | Die interaktive Warnhinweisvorschau zeigt Ihnen basierend auf Daten aus der Vergangenheit, wie oft damit zu rechnen ist, dass ein Warnhinweis ausgelöst wird.<p>Beispiel: Wenn Sie die Zeitgranularität auf „Stündlich“ festlegen, kann Ihnen die Vorschau verraten, dass der Warnhinweis zu einer bestimmten Metrik während der letzten 30 oder 31 Tage x-mal ausgelöst worden wäre.</p><p>Wenn Sie feststellen, dass zu viele Warnhinweise ausgelöst werden, können Sie den Schwellenwert im [Warnhinweis-Manager“ ](/help/components/c-alerts/alert-manager.md).</p><p>![](assets/alert_preview.png)</p> |

1. Wählen Sie [!UICONTROL **Speichern**] aus.
