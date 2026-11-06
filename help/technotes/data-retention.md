---
title: Richtlinie zur Datenaufbewahrung
description: Eine Richtlinie zur Datenspeicherung bestimmt, wie lange Adobe Ihre Daten speichert.
exl-id: f3bb02d2-380d-4eb7-8449-e0318fc8c0a6
feature: Data Governance
TQID: 'https://experienceleague.adobe.com/ymM-0bethfijutq5sprEuEfOFgw3Xn4gTsLNNgKTEio'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
    internal-label: Analysis Workspace
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
    internal-label: Admin Tools
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
    internal-label: Data configuration and collection
subfeature_v2:
  - id: ef60b66e-5984-4336-ba72-6d978b1b6f87
    internal-label: Report suites
  - id: f7fb4c71-5c39-4655-ba2d-b3b189287ab7
    internal-label: Data governance
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 0ba418a49e6a226540e0791f0138027566022d6f
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 92%
---
# Richtlinie zur Datenaufbewahrung

Von Adobe Analytics gesammelte Daten werden über einen bestimmten Zeitraum gespeichert. Der Zeitraum, über den Adobe diese Daten speichert, ist von Vertrag zu Vertrag unterschiedlich und wird in der Richtlinie zur Datenspeicherung des jeweiligen Unternehmens beschrieben. Diese Richtlinie gilt für die Daten selbst, was bedeutet, dass sie alle Analytics-Reporting-Funktionen (Analysis Workspace, Reporting-API usw.) betrifft.

**Die standardmäßige Datenaufbewahrungsrichtlinie für Adobe Analytics beträgt 25 Monate.** Die Aufbewahrungsrichtlinie Ihres Unternehmens kann je nach Vertrag unterschiedlich sein.

Die gespeicherten Daten basieren auf dem aktuellen Datum und dem Datum/der Uhrzeit der historischen Daten. Das bei Treffern aufgezeichnete Datum und die Uhrzeit können sich von dem Datum und der Uhrzeit unterscheiden, zu denen die Treffer bei Adobe eingegangen sind.

## Anpassen des standardmäßigen Datenspeicherzeitraums

Wenden Sie sich an Ihr Adobe Account-Team, wenn Sie den standardmäßigen Datenspeicherzeitraum verkürzen oder verlängern möchten.

* Für die Verkürzung des standardmäßigen Datenspeicherzeitraums fallen keine Gebühren an.
* Die Verlängerung der Datenspeicherung über den Standardzeitraum von 25 Monaten hinaus erfordert den Kauf von Erweiterungen, die in Schritten von jeweils einem Jahr verfügbar sind. Es können bis zu acht Erweiterungen erworben werden, für insgesamt zehn Jahre und einen Monat (zwei Jahre und ein Monat für die standardmäßige Aufbewahrung plus acht gebührenpflichtige Jahre).

## Datenaufbewahrung und Datenschutz

Adobe muss in seiner Rolle als Ihr Auftragsverarbeiter geeignete Maßnahmen ergreifen, um seinen Kunden und Kundinnen beim Erfüllen von Zugriffs-, Lösch- und anderen Anfragen von Einzelpersonen behilflich zu sein. Die Anwendung angemessener, sicherer und zeitnaher Richtlinien zur Löschung ist ein wichtiger Bestandteil der Erfüllung dieser Verpflichtung. Die DSGVO gilt für alle Kunden und Kundinnen, die an EU-Bürger vermarkten oder Informationen über EU-Bürger verarbeiten. Der CCPA gilt für alle Kunden und Kundinnen, die an Bürger Kaliforniens vermarkten oder Informationen über Bürger Kaliforniens verarbeiten. Somit stellt Datenschutz eine weltweite rechtliche Änderung dar.

## Datenlöschung

Sobald die Daten Ihre Datenaufbewahrungsrichtlinie überschreiten, behält Adobe das Recht, sie ohne Wiederherstellungsoption zu löschen. Sie müssen sicherstellen, dass alle Daten, die Sie speichern möchten, in der Datenaufbewahrungsrichtlinie Ihres Unternehmens enthalten sind.

## Anzeigen/Verwalten der aktuellen Datenspeicherungsrichtlinie

Der Data Governance-Dialog in [!UICONTROL Admin] Tools bietet einen Überblick darüber, welche Report Suites für Data Governance konfiguriert wurden. Es gibt auch an, ob sie einer Adobe-Organisation zugeordnet wurden und ob eine Richtlinie zur Datenaufbewahrung für diese Report Suite vorhanden ist.

## Häufig gestellte Fragen

+++ Wie entscheide ich mich für eine Datenspeicherfrist meines Unternehmens?

Ihr Unternehmen kann als Datenverantwortlicher Interessengruppen (wie beispielsweise Ihre Marketing-, Analyse- und Datenschutz-Teams) innerhalb der Organisation bestimmen, die Entscheidungen über die Datenaufbewahrung treffen. Ihr Unternehmen ist am besten in der Lage, den richtigen Zeitraum für die Datenspeicherung in Adobe Analytics zu bestimmen.

+++

+++ Wie berechne ich das Zeitfenster der Datenspeicherfrist?

In der Datenaufbewahrungsrichtlinie wird ein rollierendes Zeitfenster für die Datenaufbewahrung festgelegt, in dem vollständige Daten angezeigt und zur Berichterstellung verwendet werden können. Das Startdatum der Datenspeicherung wird durch das aktuelle Datum abzüglich des Datenspeicherungszeitraums bestimmt. Das Enddatum der Datenspeicherung wird vom aktuellen Datum bestimmt. Die Daten fallen in das Zeitfenster für die Datenaufbewahrung, wenn der Zeitstempel der Daten zwischen dem Start- und dem Enddatum liegt.

+++

+++ Kann ich eine Kopie meiner Daten anfordern, bevor sie gelöscht werden?

Ja. Adobe kann einen Dump historischer Rohdaten auf Trefferebene bereitstellen. Weitere Informationen finden Sie unter [Daten-Feeds](/help/export/analytics-data-feed/data-feed-overview.md) im Benutzerhandbuch zu Exporten. Wenden Sie sich an Ihr Adobe-Accountteam, wenn Ihre Anforderungen für den Datenexport außerhalb der Möglichkeiten der Benutzeroberfläche liegen. Hierfür können besondere Vorkehrungen getroffen werden. Die Kosten können variieren.

+++

+++ Wann löscht Adobe Daten?

Wenden Sie sich an Ihr Adobe Account-Team, um den konkreten Zeitpunkt zu erfahren, zu dem die Löschung Ihrer Daten geplant ist. Daten werden in der Regel nach einem rollierenden monatlichen Zeitplan gelöscht.

+++

