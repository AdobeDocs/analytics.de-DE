---
title: Einverständnisverwaltungs-Opt-out
description: Ermitteln Sie, von welchen Datenschutzeinstellungen sich ein Besucher bzw. eine Besucherin abgemeldet hat.
exl-id: 2bf4d22c-5b24-47fb-b489-49388fcca5b1
feature: Dimensions
TQID: https://experienceleague.adobe.com/tsMhHR84qhEUZIZjPTluCJOHMPc37-JRwLsipAycgJI
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 265
ht-degree: 93%

---

# Einverständnisverwaltungs-Opt-out

Die Dimension „Einverständnisverwaltungs-Opt[&#x200B; zeigt an](overview.md) welche Datenschutzeinstellungen ein Besucher ausdrücklich abgelehnt hat. Sie können diese Dimension verwenden, um Daten basierend auf Datenschutzeinstellungen zu filtern oder die häufigsten Gründe für ein Datenschutz-Opt-out anzuzeigen.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst Daten aus den folgenden [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md):

* `contextData.['cm.ssf']`, wenn auf `1` gesetzt. Wenn `cm.ssf` gleich `0` oder leer ist, hat diese Variable keine Auswirkung.
* `contextData.['opt.dmp']`, wenn auf `N` gesetzt. Wenn `opt.dmp` gleich `Y` ist, wird stattdessen die Dimension [Einverständnisverwaltungs-Opt-in](cm-opt-in.md) ausgefüllt.
* `contextData.['opt.sell']`, wenn auf `N` gesetzt. Wenn `opt.sell` gleich `Y` ist, wird stattdessen die Dimension [Einverständnisverwaltungs-Opt-in](cm-opt-in.md) ausgefüllt.

Ihr Unternehmen bestimmt die Logik zur Implementierung dieser Kontextdatenvariablen. Sie bleiben nicht über den Treffer hinaus erhalten, für den sie festgelegt wurden. Daher müssen Sie jede Kontextdatenvariable auf jeder Seite festlegen.

## Dimensionselemente

Zu den Dimensionselementen gehören die folgenden drei Werte:

* **`SSF`**: Der Besucher bzw. die Besucherin hat sich von der [Server-seitigen Weiterleitung](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf.md) abgemeldet. Dieses Dimensionselement ist vorhanden, wenn die Kontextdatenvariable `cm.ssf` gleich `1` ist. Weitere Informationen finden Sie im Benutzerhandbuch für Audience Manager im Abschnitt [Datenschutz – Übersicht](https://experienceleague.adobe.com/docs/audience-manager/user-guide/overview/data-privacy/data-privacy.html?lang=de). Der Treffer wird nicht an Adobe Audience Manager weitergeleitet.
* **`DMP`**: Der Besucher bzw. die Besucherin hat sich gegen die Freigabe für Datenverwaltungsplattformen entschieden. Dieses Dimensionselement ist vorhanden, wenn die Kontextdatenvariable `opt.dmp` gleich `N` ist. Ähnlich wie `SSF`, der Treffer wird nicht an Adobe Audience Manager weitergeleitet.
* **`SELL`**: Der Besucher bzw. die Besucherin widersprach der Freigabe oder dem Verkauf der Daten an Dritte. Diese Dimension ist vorhanden, wenn die Kontextdatenvariable `opt.sell` gleich `N` ist.
