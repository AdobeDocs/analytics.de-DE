---
description: Adobe Audience Manager (Adobe Audience Manager) ist eine leistungsstarke Datenverwaltungsplattform, mit der Sie eindeutige Zielgruppenprofile aus Datenintegrationen von Erstanbietern, Zweitanbietern/Partnern und Drittanbietern erstellen können. Für Werbetreibende tragen diese Zielgruppenprofile dazu bei, die wertvollsten Segmente zu definieren, die für alle digitalen Kanäle verwendet werden können.
solution: Experience Cloud
title: Audience Analytics-Übersicht
feature: Audience Analytics
exl-id: 1665a554-8a6f-4b20-99b7-bb3c2c4bf8cc
TQID: https://experienceleague.adobe.com/WPB1fEJx1MaWpUNRCZ48ghAVyKyc5IwoGOdgQQ-tPhI
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: df401a2a-327d-468c-a5e4-b7b7ccd071a0id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 522
ht-degree: 11%

---

# Audience Analytics-Übersicht

Adobe Audience Manager (Adobe Audience Manager) ist eine leistungsstarke Datenverwaltungsplattform, mit der Sie eindeutige Zielgruppenprofile aus Datenintegrationen von Erstanbietern, Zweitanbietern/Partnern und Drittanbietern erstellen können. Für Werbetreibende tragen diese Zielgruppenprofile dazu bei, die wertvollsten Segmente zu definieren, die für alle digitalen Kanäle verwendet werden können.

Mit der Audience Analytics-Integration können Sie Zielgruppendaten von Adobe Audience Manager wie demografische Informationen (z. B. Geschlecht oder Einkommensstufe), psychografische Informationen (z. B. Interessen und Hobbys), CRM-Daten und Daten zu Anzeigenimpressionen in alle Analytics-Workflows integrieren.


>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Audience Analytics](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/integrations/audience-manager/audience-analytics-integrate-aam-segments-into-analytics){target="_blank"} finden Sie ein Demovideo.

>[!ENDSHADEBOX]


## Wesentliche Vorteile {#benefits}

Die Audience Analytics-Integration bietet die folgenden Hauptvorteile:

* Es handelt sich um die erste produktbezogene Integration zwischen einer Daten-Management-Plattform (DMP) und einer Analyse-Engine auf dem Markt.
* Segmente werden von Adobe Audience Manager in Echtzeit für Analytics freigegeben, um Informationen zu Zielgruppenerkennung, Segmentierung und Optimierung zu erhalten.
* Alle Adobe Audience Manager-Segmente werden standardmäßig freigegeben, wodurch die Kundenprofile in Analytics vollständig erweitert werden.
* Lösungsadministratoren können die Integration über die Benutzeroberfläche aktivieren, wobei nur minimale Code-Änderungen erforderlich sind.
* Es werden nur Segmente freigegeben, die den Audience Manager-Datenexportsteuerelementen entsprechen.

## Funktionsweise von Audience Analytics {#works}

![](assets/mc-aud-dataflow.png)

1. Jedes Mal, wenn ein Besucher zu Ihren digitalen Eigenschaften kommt, werden Treffer erfasst und an Analytics gesendet.
1. Bei [Server-seitigen Weiterleitung](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf.md) wird jeder Treffer, den Analytics erhält, automatisch in Echtzeit an Adobe Audience Manager gesendet.
1. Durch die Audience Analytics-Integration wird für jeden Treffer die Zielgruppenzugehörigkeit eines Besuchers in Adobe Audience Manager nachgeschlagen und eine Liste der Segment-IDs zur Verarbeitung in Echtzeit an Analytics zurückgegeben.

Da Adobe Audience Manager-Segmente auf der Basis desselben Treffers eingefügt werden, können Sie sicher sein, dass alle in Adobe Audience Manager verfügbaren Daten über einen Besucher nicht verpasst werden und für diesen Treffer auf dem neuesten Stand sind. Dies ist einem AppMeasurement-Plug-in überlegen, da ein Plug-in diese Segmente nur beim nächsten Treffer (und nicht beim aktuellen Treffer) verfügbar machen kann.

Darüber hinaus klassifizieren wir die Segment-IDs von Adobe Audience Manager automatisch anhand der Anzeigenamen für Sie, sodass Sie sich keine alphanumerischen IDs in Analytics-Berichten ansehen müssen.

## Voraussetzungen {#prerequisites}

Stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

* Sie sind sowohl Kunde von Audience Manager als auch von Adobe Analytics.
* Sie sind ein Audience Manager-Administrator.
* Sie verwenden den Identitätsdienst v1.5 oder höher.
* Adobe Audience Manager und Adobe Analytics Report Suites sind derselben Experience Cloud-Organisation zugeordnet.
* Sie nutzen [die serverseitige Weiterleitung](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf.md) und haben das [Zielgruppen-Management-Modul](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/audience-management-module.html?lang=de) AppMeasurement 1.5 oder höher (kein DIL-Code) implementiert.

Diese Voraussetzungen werden im [Audience Analytics-Workflow](/help/integrate/c-audience-analytics/c-workflow/audiences-workflow.md) beschrieben.
