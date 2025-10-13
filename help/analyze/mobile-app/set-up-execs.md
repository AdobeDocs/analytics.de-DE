---
description: In einigen Fällen benötigen die Benutzer möglicherweise zusätzliche Hilfe, um auf die Mobile App zuzugreifen und sie zu verwenden. Dieser Abschnitt enthält Informationen, die Sie bei der Bereitstellung dieser Hilfe unterstützen.
title: Einrichten von Benutzern für das Programm
feature: Analytics Dashboards
role: User, Admin
exl-id: 0e858407-2852-4a5f-a0df-3ba290fcca8f
source-git-commit: 34ba0e09cd909951a777b0ad3da080958633f97e
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 100%

---

# Einrichten von Benutzern für das Programm

In einigen Fällen benötigen die ausführenden Benutzer möglicherweise zusätzliche Hilfe, um auf die App zuzugreifen und sie zu verwenden. Dieser Abschnitt enthält Informationen, die Sie bei der Bereitstellung dieser Hilfe unterstützen.

## Sicherstellen, dass Mobile-App-Benutzer Zugriff auf Adobe Analytics haben

1. Richten Sie neue Benutzer in der [Experience Cloud Admin Console](/help/admin/admin-console/permissions/product-profile.md) ein.

1. Um Scorecards freigeben zu können, müssen Sie Mobile-App-Benutzern Berechtigungen für den Zugriff auf Scorecard-Komponenten wie Analysis Workspace, die Report Suites, auf denen Scorecards basieren, sowie Segmente, Metriken und Dimensionen gewähren.

## Systemanforderungen von Mobile-App-Benutzern

Damit ausführende Benutzer Zugriff auf Ihre Scorecards in der Mobile App haben, müssen folgende Voraussetzungen gegeben sein:

* Auf ihren Geräten muss mindestens iOS-Version 10 oder Android-Version 4.4 (KitKat) installiert sein.
* Ihre Adobe Analytics-Anmeldeinformationen müssen gültig sein.
* Sie haben die mobilen Scorecards für Ihre Benutzer korrekt erstellt und freigegeben.
* Ihre Benutzer müssen Zugriff auf die Komponenten haben, die die Scorecard enthält. Sie können bei der Freigabe Ihrer Scorecards eine Option auswählen, um **[!UICONTROL eingebettete Komponenten freizugeben]**.

## Ausführenden Benutzern helfen, die Mobile App herunterzuladen und zu installieren

**Für ausführende Benutzer mit iOS-Geräten:**

Klicken Sie auf den folgenden Link (auch in Analytics unter **[!UICONTROL Tools]** > **[!UICONTROL Analytics-Dashboards (mobile App)]** verfügbar) und befolgen Sie die Anweisungen zum Herunterladen, Installieren und Öffnen der Applikation:

`[iOS link](https://apple.co/2zXq0aN)`

**Für ausführende Benutzer mit Android-Geräten:**

Klicken Sie auf den folgenden Link (auch in Analytics unter **[!UICONTROL Tools]** > **[!UICONTROL Analytics-Dashboards (mobile App)]** verfügbar) und befolgen Sie die Anweisungen zum Herunterladen, Installieren und Öffnen der Applikation:

`[Android link](https://bit.ly/2LM38Oo)`

Nach dem Herunterladen und der Installation können sich ausführende Benutzer mit ihren vorhandenen Adobe Analytics-Anmeldeinformationen bei der App anmelden. Adobe und Enterprise/Federated IDs werden unterstützt.

![Willkommensbildschirm der App](assets/welcome.png)

## Ausführenden Benutzern helfen, auf Ihre Scorecard zuzugreifen

1. Fordern Sie die ausführenden Benutzer auf, sich bei der Mobile App anzumelden.

   Der Bildschirm **[!UICONTROL Unternehmen auswählen]** wird angezeigt. Auf diesem Bildschirm werden die Unternehmensanmeldungen angezeigt, die der ausführende Benutzer verwenden kann.

1. Fordern Sie sie auf, den Namen der Unternehmensanmeldung oder die Experience Cloud-Organisation für die von Ihnen freigegebene Scorecard anzutippen.

   Die Scorecard-Liste zeigt alle Scorecards an, die für den ausführenden Benutzer mit dieser Unternehmensanmeldung freigegeben wurden.

1. Helfen Sie den Benutzern, diese Liste ggf. nach der **[!UICONTROL zuletzt geänderten Scorecard]** zu sortieren.

1. Fordern Sie sie auf, den Namen der Scorecard anzutippen, die angezeigt werden soll.

   ![Unternehmen auswählen](assets/accesscard.png)


### Scorecard-Benutzeroberfläche erläutern

Erklären Sie dem ausführenden Benutzer, wie die Kacheln in den von Ihnen freigegebenen Scorecards dargestellt werden.

![Kacheln erklären](assets/newexplain.png)

![Beispiel-Scorecard](assets/intro_scorecard.png)

Zusätzliche Informationen zu Kacheln:

* Die Granularität der Sparklines hängt von der Länge des Datumsbereichs ab:
* Für einen Tag wird ein stündlicher Trend angezeigt.
   * Für mehr als einen Tag und weniger als ein Jahr wird ein täglicher Trend angezeigt.
   * Für ein Jahr oder mehr wird ein wöchentlicher Trend angezeigt.
   * Die Formel für die Änderung des Prozentwerts ist: Gesamtwert der Metrik (aktueller Datumsbereich) – Gesamtwert der Metrik (Vergleichsdatumsbereich) / Gesamtwert der Metrik (Vergleichsdatumsbereich).
   * Sie können den Anzeigebereich nach unten ziehen, um die Scorecard zu aktualisieren.


1. Tippen Sie auf eine Kachel, um zu zeigen, wie eine detaillierte Aufschlüsselung für die Kachel funktioniert.

   ![Aufschlüsselungsansicht](assets/sparkline.png)

   * Tippen Sie auf einen beliebigen Punkt auf einer Sparkline, um Daten anzuzeigen, die diesem Punkt auf der Linie zugeordnet sind.

   * In einer Tabelle werden Daten zu den der Kachel hinzugefügten Dimensionen angezeigt. Tippen Sie auf den Abwärtspfeil, um Dimensionen auszuwählen. Wenn der Kachel keine Dimension hinzugefügt wurde, werden in der Tabelle Diagrammdaten angezeigt.

1. Um die Datumsbereiche für die Scorecard zu ändern, tippen Sie auf die Kopfzeile „Datum“ und wählen Sie die gewünschte Kombination aus Primär- und Vergleichsdatumsbereich aus.

   ![Datum ändern](assets/changedate.png)

## Mobile-App-Voreinstellungen ändern

Um die Voreinstellungen zu ändern, tippen Sie auf die Option **[!UICONTROL Voreinstellungen]** oben. In den Voreinstellungen können Sie die biometrische Anmeldung aktivieren oder Sie können die App wie folgt für den Dunkelmodus einstellen:

![Dunkelmodus](assets/darkmode.png)

## Fehlerbehebung

Wenn sich der ausführende Benutzer anmeldet und eine Meldung angezeigt wird, dass nichts freigegeben wurde, kann das folgende Gründe haben:

![Nichts freigegeben](assets/nothing.png)

* Der ausführende Benutzer hat möglicherweise die falsche Analytics-Instanz ausgewählt oder
* eventuell wurde die Scorecard nicht für den ausführenden Benutzer freigegeben.

Vergewissern Sie sich, dass sich der ausführende Benutzer bei der richtigen Adobe Analytics-Instanz anmelden kann und dass die Scorecard freigegeben wurde.

>[!IMPORTANT]
>
>Seit Oktober 2020 führt Adobe schrittweise eine Reihe von Verbesserungen durch, um die Leistung der Applikation „Adobe Analytics-Dashboards“ zu optimieren. Diese Erweiterungen konzentrieren sich auf das Caching historischer Analytics-Daten, die zum Ausfüllen von Scorecards mit Datumsangaben (außer dem aktuellen Tag) verwendet werden. Diese Daten werden bis zu 24 Stunden lang in einem sicheren öffentlichen Microsoft Azure-Konto in der Cloud zwischengespeichert. Bitte wenden Sie sich an Ihr Adobe Account Team, wenn Sie diese Funktionen zur Leistungsverbesserung nicht in Anspruch nehmen möchten.
