---
description: Erläutert Optimierungen der Server-seitigen Weiterleitung, die durch die EU-Cookie-Richtlinie veranlasst wurden.
title: DSGVO/ePrivacy – Einhaltung und serverseitige Weiterleitung
feature: Server-Side Forwarding
exl-id: 54e43a16-8f15-4ee8-9aa2-579af30be2c9
source-git-commit: ee56267979979f8e03b1c6a0d849ccf994599024
workflow-type: ht
source-wordcount: '541'
ht-degree: 100%

---

# DSGVO/ePrivacy – Einhaltung und serverseitige Weiterleitung

In diesem Abschnitt werden Optimierungen an der Server-seitigen Weiterleitung erläutert, die durch die [EU-Cookie-Richtlinie](https://wikis.ec.europa.eu/display/WEBGUIDE/04.+Cookies+and+similar+technologies) erforderlich wurden, die am 30. September 2017 in Kraft trat.

Die serverseitige Weiterleitung wird verwendet, um Daten in Echtzeit von Adobe Analytics zu anderen [!DNL Experience Cloud Solutions] wie Audience Manager zu übertragen. Bei entsprechender Aktivierung ermöglicht die Server-seitige Weiterleitung während des Datenerfassungsprozesses Analytics das Übergeben von Daten an andere Experience Cloud-Lösungen und diesen Lösungen das Übergeben von Daten an Analytics.

Zuvor gab es bei der Server-seitigen Weiterleitung keine Möglichkeit zur Unterscheidung zwischen Ereignissen/Treffern vor und nach einer erfolgten Zustimmung. Ab dem 1. November 2018 hatten Sie als Datenverantwortlicher (Adobe Analytics-Kunde) die Möglichkeit, die vor einer erfolgten Zustimmung zugänglichen Daten auf Adobe Analytics zu beschränken sowie die serverseitige Weiterleitung an AAM zu unterbinden. Eine neue Variable im Implementierungskontext ermöglicht es, die Treffer zu kennzeichnen, bei denen noch keine Zustimmung erfolgt ist. Diese Variable, sofern festgelegt, verhindert, dass die Treffer vor einer Zustimmung an AAM weitergeleitet werden.

Wenn diese neue Kontextvariable `cm.ssf=1` bei einem Hit vorhanden ist, wird dieser Hit gekennzeichnet und nicht serverseitig an AAM weitergeleitet. Taucht die Zeichenfolge hingegen nicht bei einem Treffer auf, wird der Treffer an AAM weitergeleitet.

Die serverseitige Weiterleitung ist bidirektional, d. h. wenn sie auf einen Treffer angewendet und dieser Treffer an AAM weitergeleitet wird, erhält Audience Analytics Segmentinformationen für diesen Treffer von AAM und sendet diese zurück an Analytics. Aus diesem Grund werden Treffer, die nicht serverseitig von Analytics an AAM weitergeleitet werden, nicht mit der Liste von Segment-IDs aus AAM versehen. Aus diesem Grund gibt es einen Teilsatz von Traffic/Treffern, die keine Segment-ID-Informationen von AAM erhalten.

## Implementierungsdetails {#section_FFA8B66085BF469FAB5365C944FE38F7}

Befolgen Sie abhängig von Ihrer Implementierungsmethode die folgenden Schritte.

| Implementierungsmethode | Schritte |
|--- |--- |
| Tags in Adobe Experience Platform | Wenn Sie die Adobe Analytics-Erweiterung installiert haben, fügen Sie dem benutzerdefinierten Code-Editor innerhalb der Aktionskonfiguration einer Regel die folgende Definition für Kontextdatenvariablen hinzu: <br/>`s.contextData['cm.ssf']&nbsp;=&nbsp;'1' ` <br/> Hinweis: Definieren Sie die Kontextdatenvariable und legen Sie dafür den Wert „1“ fest, wenn ein Kunde gezieltem Marketing nicht zustimmt. Legen Sie für die `contextdata`-Variable den Wert *0* für Kunden fest, die gezieltem Marketing zugestimmt haben. |
| AppMeasurement | Fügen Sie die Kontextdatenvariablendefinition zur Datei „AppMeasurement.js“ hinzu:  <br/>`s.contextData['cm.ssf']&nbsp;=&nbsp;'1' ` <br/>Hinweis: Definieren Sie die Kontextdatenvariable und legen Sie dafür den Wert „1“ fest, wenn ein Kunde gezieltem Marketing nicht zustimmt. Legen Sie für die Kontextdatenvariable den Wert „0“ für Kunden fest, die gezieltem Marketing zugestimmt haben. |

## Reporting (optional) {#section_6AD4028EC11C4DABA2A34469DDC99E89}

Sie können Adobe Analytics verwenden, um Berichte dazu zu erstellen, wie viel von Ihrem Traffic zustimmungsbasiert ist und somit serverseitig weitergeleitet wurde, im Vergleich zu wie viel von Ihrem Traffic nicht zustimmungsbasiert ist und nicht an AAM weitergeleitet wurde.

Um diese Art der Berichterstellung zu konfigurieren, weisen Sie die neue Kontextvariable über Verarbeitungsregeln einer benutzerdefinierten Traffic-Variable (Eigenschaft) hinzu. Gehen Sie dazu wie folgt vor

1. Implementieren Sie die Variable „cm.ssf“ (wie oben dargestellt.)
1. [Aktivieren Sie die Eigenschaft.](/help/admin/admin/c-traffic-variables/traffic-var.md)
1. Weisen Sie die Kontextvariable über Verarbeitungsregeln der Eigenschaft hinzu.

   1. Gehen Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**. Wählen Sie dann eine Report Suite aus.
   1. Klicken Sie auf **[!UICONTROL Report Suite bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Verarbeitungsregeln]**.
   1. Klicken Sie auf **[!UICONTROL Regel hinzufügen]**.
   1. Überschreiben Sie unter **[!UICONTROL Immer ausführen]** den Wert der über die Kontextvariable „cm.ssf(Context Data)“ aktivierten Kontextvariable.
   1. Klicken Sie auf **[!UICONTROL Speichern]**.
