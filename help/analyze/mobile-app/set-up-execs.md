---
description: Ausführende Benutzende benötigen möglicherweise zusätzliche Hilfe, um auf die App zuzugreifen und sie zu verwenden. Dieser Abschnitt enthält Informationen, die Sie bei der Bereitstellung dieser Hilfe unterstützen.
title: Einrichten von ausführenden Benutzenden für die App
feature: Analytics Dashboards
role: User, Admin
exl-id: 0e858407-2852-4a5f-a0df-3ba290fcca8f
TQID: https://experienceleague.adobe.com/mejoGlgRAOHkpBAXtlVef4LcheWPXtg9TT7hHYIPtHU
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
    internal-label: Analysis Workspace
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
    internal-label: Dashboards
subfeature_v2:
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
    internal-label: Components
  - id: ef60b66e-5984-4336-ba72-6d978b1b6f87
    internal-label: Report suites
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
source-git-commit: 0ba418a49e6a226540e0791f0138027566022d6f
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 96%
---
# Einrichten von Benutzern für das Programm

In einigen Fällen benötigen ausführende Benutzende möglicherweise zusätzliche Hilfe, um auf die App zuzugreifen und sie zu verwenden. Dieser Abschnitt enthält Informationen, die Sie bei der Bereitstellung dieser Hilfe unterstützen.

## Sicherstellen, dass Mobile-App-Benutzer Zugriff auf Adobe Analytics haben

1. Richten Sie neue Benutzende in der [CX Enterprise Admin Console](/help/admin/admin-console/permissions/product-profile.md) ein.

1. Um Scorecards freigeben zu können, müssen Sie Mobile-App-Benutzern Berechtigungen für den Zugriff auf Scorecard-Komponenten wie Analysis Workspace, die Report Suites, auf denen Scorecards basieren, sowie Segmente, Metriken und Dimensionen gewähren.

## Systemanforderungen von Mobile-App-Benutzern

Damit ausführende Benutzende Zugriff auf Ihre Scorecards in der App haben, müssen folgende Voraussetzungen gegeben sein:

* Auf ihren Geräten muss mindestens iOS-Version 10 oder Android-Version 4.4 (KitKat) installiert sein.
* Sie verfügen über eine gültige Anmeldung bei Adobe Analytics.
* Sie haben die mobilen Scorecards für Ihre Benutzer korrekt erstellt und freigegeben.
* Ihre Benutzer müssen Zugriff auf die Komponenten haben, die die Scorecard enthält. Sie können bei der Freigabe Ihrer Scorecards eine Option auswählen, um **[!UICONTROL eingebettete Komponenten freizugeben]**.

## Ausführenden Benutzern helfen, die Mobile App herunterzuladen und zu installieren

**Für ausführende Benutzer mit iOS-Geräten:**

Klicken Sie auf den folgenden Link (auch in Analytics unter **[!UICONTROL Tools]** > **[!UICONTROL Analytics-Dashboards (mobile App)]** verfügbar) und befolgen Sie die Anweisungen zum Herunterladen, Installieren und Öffnen der Applikation:

`[iOS link](https://apple.co/2zXq0aN)`

**Für ausführende Benutzer mit Android-Geräten:**

Klicken Sie auf den folgenden Link (auch in Analytics unter **[!UICONTROL Tools]** > **[!UICONTROL Analytics-Dashboards (mobile App)]** verfügbar) und befolgen Sie die Anweisungen zum Herunterladen, Installieren und Öffnen der Applikation:

`[Android link](https://bit.ly/2LM38Oo)`

Nach dem Herunterladen und der Installation können sich ausführende Benutzende mit ihren vorhandenen Adobe Analytics-Anmeldedaten bei der App anmelden. Adobe- und Enterprise/Federated-IDs werden unterstützt.

![Willkommensbildschirm der App](assets/welcome.png)

## Ausführenden Benutzern helfen, auf Ihre Scorecard zuzugreifen

1. Fordern Sie die ausführenden Benutzer auf, sich bei der Mobile App anzumelden.

   Der Bildschirm **[!UICONTROL Unternehmen auswählen]** wird angezeigt. Auf diesem Bildschirm werden die Anmeldeunternehmen angezeigt, zu denen die bzw. der ausführende Benutzer gehört.

1. Fordern Sie sie auf, den Namen des Anmeldeunternehmens oder der Adobe-Organisation anzutippen, der bzw. die für die von Ihnen freigegebene Scorecard gilt.

   Die Scorecard-Liste zeigt dann alle Scorecards an, die für die bzw. den ausführende Benutzende unter diesem Anmeldeunternehmen freigegeben wurden.

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

Wenn sich die bzw. der ausführende Benutzende anmeldet und eine Meldung angezeigt wird, dass nichts freigegeben wurde:

![Nichts freigegeben](assets/nothing.png)

* Die bzw. der ausführende Benutzende hat möglicherweise die falsche Analytics-Instanz ausgewählt oder
* Die Scorecard wurde möglicherweise nicht für die bzw. den ausführende Benutzende freigegeben.

Vergewissern Sie sich, dass sich die bzw. der ausführende Benutzende bei der richtigen Adobe Analytics-Instanz anmelden kann und dass die Scorecard freigegeben wurde.

>[!IMPORTANT]
>
>Seit Oktober 2020 führt Adobe schrittweise eine Reihe von Verbesserungen durch, um die Leistung der App „Adobe Analytics-Dashboards“ zu optimieren. Diese Erweiterungen konzentrieren sich auf das Caching historischer Analytics-Daten, die zum Ausfüllen von Scorecards mit Datumsangaben (außer dem aktuellen Tag) verwendet werden. Diese Daten werden bis zu 24 Stunden lang in einem sicheren Microsoft Azure-Speicherkonto in der öffentlichen Cloud zwischengespeichert. Bitte wenden Sie sich an Ihr Adobe-Accountteam, wenn Sie diese Funktionen zur Leistungsverbesserung abwählen (Opt-out) möchten.
