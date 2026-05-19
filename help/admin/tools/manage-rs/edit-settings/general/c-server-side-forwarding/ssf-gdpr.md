---
description: Erläutert Optimierungen der Server-seitigen Weiterleitung, die durch die EU-Cookie-Richtlinie veranlasst wurden.
title: DSGVO/ePrivacy – Einhaltung und serverseitige Weiterleitung
feature: Report Suite Settings
exl-id: 54e43a16-8f15-4ee8-9aa2-579af30be2c9
role: Admin
TQID: https://experienceleague.adobe.com/Q4HJtRLxJvr4fy7bF5jxCW2FLH5sdKCU6rAUzN0yNv0
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: c2ae876122715b4fa6367326dc23479dd9648021
workflow-type: tm+mt
source-wordcount: 588
ht-degree: 41%

---

# DSGVO/ePrivacy – Einhaltung und serverseitige Weiterleitung

In diesem Abschnitt werden Optimierungen an der Server-seitigen Weiterleitung erläutert, die durch die [EU-Cookie-Richtlinie](https://wikis.ec.europa.eu/display/WEBGUIDE/04.+Cookies+and+similar+technologies) erforderlich wurden, die am 30. September 2017 in Kraft trat.

Die Server-seitige Weiterleitung wird verwendet, um Daten von Adobe Analytics in Echtzeit für andere CX Enterprise-Lösungen wie Audience Manager freizugeben. Wenn diese Option aktiviert ist, ermöglicht die Server-seitige Weiterleitung während des Datenerfassungsprozesses Analytics das Pushen von Daten an andere CX Enterprise-Lösungen und diese Lösungen das Pushen von Daten an Analytics.

Zuvor gab es bei der Server-seitigen Weiterleitung keine Möglichkeit zur Unterscheidung zwischen Ereignissen/Treffern vor und nach einer erfolgten Zustimmung. Seit dem 1. November 2018 haben Sie als Datenverantwortlicher (Adobe Analytics-Kunde) die Möglichkeit, Daten vor einer Zustimmung auf Adobe Analytics zu beschränken und die Weiterleitung an Adobe Audience Manager zu verhindern. Eine neue Variable im Implementierungskontext ermöglicht es, die Treffer zu kennzeichnen, bei denen noch keine Zustimmung erfolgt ist. Diese Variable verhindert, sofern festgelegt, dass diese Treffer vor einer Einwilligung an Adobe Audience Manager weitergeleitet werden.

Wenn diese neue Kontextvariable `cm.ssf=1` in einem Treffer vorhanden ist, wird dieser Treffer markiert und nicht Server-seitig an Adobe Audience Manager weitergeleitet. Wenn diese Zeichenfolge jedoch nicht in einem Treffer angezeigt wird, wird der Treffer an Adobe Audience Manager weitergeleitet.

Die Server-seitige Weiterleitung erfolgt bidirektional, d. h. wenn sie auf einen Treffer angewendet wird und dieser Treffer an Adobe Audience Manager weitergeleitet wird, empfängt Audience Analytics Segmentinformationen für diesen Treffer von Adobe Audience Manager und sendet sie zurück an Analytics. Daher werden alle Treffer, die nicht Server-seitig von Analytics an Adobe Audience Manager weitergeleitet werden, nicht mit der Liste der Segment-IDs von Adobe Audience Manager angereichert. Daher gibt es eine Untergruppe von Traffic/Treffern, die keine Segment-ID-Informationen von Adobe Audience Manager erhalten.

## Implementierungsdetails {#section_FFA8B66085BF469FAB5365C944FE38F7}

Führen Sie je nach Implementierungsmethode die folgenden Schritte aus.

| Implementierungsmethode | Schritte |
|--- |--- |
| Tags in Adobe Experience Platform | Wenn Sie die Adobe Analytics-Erweiterung installiert haben, fügen Sie dem benutzerdefinierten Code-Editor innerhalb der Aktionskonfiguration einer Regel die folgende Definition für Kontextdatenvariablen hinzu: <br/>`s.contextData['cm.ssf'] = '1'` <br/> Hinweis: Definieren Sie die Kontextdatenvariable und legen Sie dafür den Wert „1“ fest, wenn ein Kunde gezieltem Marketing nicht zustimmt. Legen Sie für die `contextdata`-Variable den Wert *0* für Kunden fest, die gezieltem Marketing zugestimmt haben. |
| AppMeasurement | Fügen Sie der Datei &quot;AppMeasurement.js“ die Definition der Kontextdatenvariablen hinzu: <br/>`s.contextData['cm.ssf'] = '1'` <br/>Hinweis: Definieren Sie die Kontextdatenvariable und setzen Sie sie auf 1, wenn ein Kunde gezieltem Marketing nicht zustimmt. Legen Sie für die Kontextdatenvariable den Wert „0“ für Kunden fest, die gezieltem Marketing zugestimmt haben. |

## Reporting (optional) {#section_6AD4028EC11C4DABA2A34469DDC99E89}

Sie können Adobe Analytics verwenden, um zu berichten, wie viel Ihres Traffics auf Einverständnis basiert und infolgedessen Server-seitig weitergeleitet wurde, im Vergleich dazu, wie viel Ihres Traffics nicht auf Einverständnis basiert und nicht an Adobe Audience Manager weitergeleitet wurde.

Um diesen Berichtstyp zu konfigurieren, ordnen Sie die neue Kontextvariable über Verarbeitungsregeln einer Custom Traffic Variable (Prop) zu. Gehen Sie dazu wie folgt vor

1. Implementieren Sie die Variable „cm.ssf“ (wie oben dargestellt.)
1. [Aktivieren der Eigenschaft.](/help/admin/tools/manage-rs/edit-settings/c-traffic-variables/traffic-var.md)
1. Verwenden Sie Verarbeitungsregeln, um die Kontextvariable der Eigenschaft zuzuordnen.

   1. Gehen Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**. Wählen Sie dann eine Report Suite aus.
   1. Klicken Sie auf **[!UICONTROL Report Suite bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Verarbeitungsregeln]**.
   1. Klicken Sie auf **[!UICONTROL Regel hinzufügen]**.
   1. Überschreiben Sie unter **[!UICONTROL Immer ausführen]** den Wert der über die Kontextvariable „cm.ssf(Context Data)“ aktivierten Kontextvariable.
   1. Klicken Sie auf **[!UICONTROL Speichern]**.
