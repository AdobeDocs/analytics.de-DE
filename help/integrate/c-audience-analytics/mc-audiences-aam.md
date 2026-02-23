---
description: Adobe Audience Manager (Adobe Audience Manager) ist eine leistungsstarke Datenverwaltungsplattform, mit der Sie eindeutige Zielgruppenprofile aus Datenintegrationen von Erstanbietern, Zweitanbietern/Partnern und Drittanbietern erstellen können. Für Werbetreibende tragen diese Zielgruppenprofile dazu bei, die wertvollsten Segmente zu definieren, die für alle digitalen Kanäle verwendet werden können.
solution: Experience Cloud
title: Audience Analytics-Übersicht
feature: Audience Analytics
exl-id: 1665a554-8a6f-4b20-99b7-bb3c2c4bf8cc
source-git-commit: 8b1e25b9633b6db3e49da079f7014e6b7b595474
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 9%

---

# Audience Analytics-Übersicht

Adobe Audience Manager (Adobe Audience Manager) ist eine leistungsstarke Datenverwaltungsplattform, mit der Sie eindeutige Zielgruppenprofile aus Datenintegrationen von Erstanbietern, Zweitanbietern/Partnern und Drittanbietern erstellen können. Für Werbetreibende tragen diese Zielgruppenprofile dazu bei, die wertvollsten Segmente zu definieren, die für alle digitalen Kanäle verwendet werden können.

Mit der Audience Analytics-Integration können Sie Zielgruppendaten von Adobe Audience Manager wie demografische Informationen (z. B. Geschlecht oder Einkommensstufe), psychografische Informationen (z. B. Interessen und Hobbys), CRM-Daten und Daten zu Anzeigenimpressionen in alle Analytics-Workflows integrieren.


>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Audience Analytics](https://experienceleague.adobe.com/de/docs/analytics-learn/tutorials/integrations/audience-manager/audience-analytics-integrate-aam-segments-into-analytics){target="_blank"} finden Sie ein Demovideo.

>[!ENDSHADEBOX]


## Wesentliche Vorteile  {#benefits}

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
