---
title: Implementieren von Adobe Analytics mit der Adobe Experience Platform Edge Network-API
description: Verwenden Sie die Adobe Experience Platform Edge Network-API, um Daten an Adobe Analytics zu senden.
exl-id: 1ede95b7-4f17-4d69-aba6-62b253b6693a
feature: Implementation Basics
role: Admin, Developer, Leader
TQID: 'https://experienceleague.adobe.com/lvnplKx6dPwmmbZWgSShGvZXD2TtUoigi-HNiKutZSg'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: fd307ce7-56f5-4ee3-af68-a7833ff6e85eid: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
subfeature_v2: id: b3e5f43e-2e2f-43c0-810a-044a5f91e31a
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 332
ht-degree: 43%

---

# Implementieren von Adobe Analytics mit der Adobe Experience Platform Edge Network-API

Normalerweise verwenden Sie die Experience Platform Edge Network-API , um Daten Server-seitig und nicht Client-seitig zu erfassen, und wenn Sie Daten von Geräten wie IoT-Geräten, Set-Top-Boxen und Desktop-Programmen erfassen. Dann senden Sie diese Daten an das Edge-Netzwerk und an Services wie Adobe Analytics.

Erwägen Sie auch die Edge Network-API, wenn vertrauliche Daten sicher erfasst und über das Netzwerk authentifiziert werden sollen. Weitere Informationen finden [ unter ](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/authentication.html)Authentifizierung“.

Ein allgemeiner Überblick über die Implementierungsaufgaben:

![Workflow von Adobe Analytics mit der Analytics-Erweiterung](../../assets/edge-network-server-api-annotated.png)

<table style="width:100%">

<tr>
<th style="width:5%"></th><th style="width:60%"><b>Aufgabe</b></th><th style="width:35%"><b>Weitere Informationen</b></th>
</tr>

<tr>
<td>1</td>
<td>Stellen Sie sicher, dass Sie <b>eine Report Suite definiert haben</b>.</td>
<td><a href="../../../admin/tools/manage-rs/report-suites-admin.md">Report Suite Manager</a></td>
</tr>

<tr>
<td>2</td>
<td><b>Schemata einrichten</b>. Um die Datenerfassung für die Verwendung in allen Anwendungen zu standardisieren, die Adobe Experience Platform nutzen, hat Adobe das offene und öffentlich dokumentierte Standard Experience-Datenmodell (XDM) erstellt.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=de">Übersicht über die Benutzeroberfläche von Schemata</a></td>
</tr>

<tr>
<td>3</td>
<td><b>Konfigurieren eines Datenstroms</b>. Ein Datenstrom stellt die Server-seitige Konfiguration bei Verwendung der APIs aus der Adobe Experience Platform Edge Network-API dar.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de">Konfigurieren eines Datenstroms<a></td> 
</tr>

<tr>
<td>4</td>
<td><b>Implementieren und testen Sie </b> Datenerfassung mithilfe der APIs für die Erfassung von Einzelereignisdaten und die Batch-Ereignisdatenerfassung.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=de">Datenerfassung für Einzelereignisse</a><br/><a href="https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/non-interactive-data-collection.html">Batch-Ereignisdatenerfassung</a>
</tr>

<td>5</td>
<td><b>Fügen Sie einen Adobe Analytics-Service</b> in Ihrem Datenstrom hinzu. Mit diesem Service wird gesteuert, ob und wie Daten an Adobe Analytics gesendet werden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/interacting-other-adobe-solutions/interacting-adobe-analytics.html?lang=de">Interagieren mit Adobe Analytics</a></td>
</tr>


</table>

Weitere Informationen finden Sie in der Dokumentation ](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=de) Edge Network-APIs.[

