---
description: Häufig gestellte Fragen zu den Funktionen, der Funktionalität und den Problemen bezüglich der serverseitigen Weiterleitung.
title: Häufig gestellte Fragen zur serverseitigen Weiterleitung
feature: Report Suite Settings
exl-id: 63103d2b-e2e8-42da-bdbd-be90abe305f7
role: Admin
TQID: https://experienceleague.adobe.com/3i6RY7JRPlJc-9NjsQXBPn5SEOn0m4JrtL85Kl84ilM
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 707
ht-degree: 75%

---

# Häufig gestellte Fragen zur serverseitigen Weiterleitung

Häufig gestellte Fragen zu den Funktionen, der Funktionalität und den Problemen bezüglich der serverseitigen Weiterleitung.

## Tracking-Server {#section_28E5BECC2034484AB9726E513F2CCFB7}

| Frage | Antwort |
|--- |--- |
| F: Wie verhält es sich, wenn ich derzeit die alte, Tracking-Server-basierte, serverseitige Weiterleitung verwende? | Die alte Server-seitige Weiterleitungsmethode für Tracking-Server leitet Daten weiterhin von Analytics an Audience Manager weiter. Wenn Sie jedoch Audience Manager-Segmente an Analytics senden möchten, ist die neue Server-seitige Weiterleitung auf Report Suite erforderlich. Außerdem schadet es nicht, eine Report Suite zusätzlich zu Ihrer Tracking-Server-Konfiguration für die Server-seitige Weiterleitung zu aktivieren. Die neue Einstellung für die Server-seitige Weiterleitung bei Report Suites wird verwendet, wenn ein Konflikt auftritt. |
| F: Sollte ich eine Migration von meiner alten Tracking-Server-basierten, serverseitigen Weiterleitung auf die neue Report Suite-basierte, serverseitige Weiterleitung durchführen? | Wir werden die Tracking-Server-basierte Server-seitige Weiterleitung in absehbarer Zeit weiterhin unterstützen. Wenn Sie jedoch die Integration von Audience Manager zu Analytics (Segmentfreigabe für Analytics) nutzen möchten, müssen Sie die neue Report Suite-basierte Server-seitige Weiterleitung für alle anwendbaren Report Suites aktivieren. Es gibt jedoch keinen dringenden Grund, die auf dem alten Tracking-Server basierende Server-seitige Weiterleitung zu deaktivieren. |

## Taggen und Berichterstellung {#section_71391BA901AC47B9A2286281644FF281}

| Frage | Antwort |
|--- |--- |
| F: Wie verhält es sich, wenn ich auf meiner Site Multi-Suite-Tagging verwende? Werden meine Serveraufrufe an Audience Manager durch die serverseitige Weiterleitung verdoppelt? | Nein, ein von Analytics an Audience Manager weitergeleiteter Hit wird nur einmal an Audience Manager weitergeleitet. Die Anzahl der Report Suites des Hits ist dabei unerheblich. Wenn Sie für die einzelnen Report Suites des Hits über entsprechende Datenquellen in Audience Manager verfügen, wird jede davon entsprechend aus diesem einen Hit ausgefüllt.  Beachten Sie jedoch, dass Sie die Serveraufrufe an Audience Manager verdoppeln, wenn Sie momentan die clientseitige Datenerfassung (DIL) verwenden und Sie die serverseitige Weiterleitung aktivieren, ohne das Zielgruppen-Management-Modul zu installieren. Dabei ist die Anzahl der Report Suites im Analytics-Hit unerheblich. |
| F: Wie verhält es sich, wenn ich mit mehreren Suites getaggte Report Suites verwende, die separaten Experience Cloud-Org. zugewiesen sind? | Sie sollten nie Daten aus einem einzelnen Analytics-Hit an zwei Report Suites senden, die zu separaten Experience Cloud-Org. gehören. Tritt dieser Fall jedoch ein, wird der Hit nur an die Experience Cloud-Org. weitergeleitet, die mit der Identity Service-Konfiguration auf der Seite übereinstimmt. |
| F: Wie verhält es sich, wenn ich das Multi-Suite-Taggen verwende und nur eine meiner Report Suites meiner Experience Cloud-Org. zugewiesen ist und die andere nicht? | Der Hit wird an den entsprechenden Datenerfassungsserver für die Experience Cloud-Org. der zugewiesenen Report Suite weitergeleitet. Da die nicht zugewiesene Report Suite jedoch keine zugeordnete Datenquelle in Audience Manager hat, werden für die nicht zugewiesene Report Suite in Audience Manager keine Daten aufgezeichnet. |
| F: Wie verhält es sich, wenn ich eine Report Suite verwende, die mehreren Experience Cloud-Org. zugewiesen ist? | Analytics betrachtet diese Report Suite als nicht zugeordnet und lässt keine Server-seitige Weiterleitung für diese Report Suite zu. Wenden Sie sich an die Kundenunterstützung, um dieses Zuordnungsproblem zu beheben. |
| F: Ist die Report Suite-basierte, serverseitige Weiterleitungsmethode langsamer als die Tracking-Server-basierte, serverseitige Weiterleitung? | Nein, die Antwortzeit ist dieselbe. |
| F: Wie verhält es sich, wenn ich zwei Experience Cloud-Organisationen (oder Adobe Audience Manager-Instanzen) verwende und Daten zwischen beiden Experience Cloud-Organisationen freigeben möchte? Kann ich einen einzelnen Analytics-Hit mithilfe der serverseitigen Methode an mehrere Experience Cloud-Org. weiterleiten? | Nein. Wenn Sie unter einer Experience Cloud-Org. erfasste Daten für eine andere Experience Cloud-Org. freigeben müssen, wird empfohlen, die relevanten Zielgruppen mithilfe des Audience Marketplace aus einer Audience Manager-Instanz an eine andere zu senden. |
| F: Führt die serverseitige Weiterleitung zu einer zusätzlichen Rechnungsstellung in Audience Manager oder Analytics? | In Analytics erfolgt keine zusätzliche Rechnungsstellung. In Audience Manager werden weitergeleitete Hits wie andere Hits behandelt und abgerechnet.  Daher ist es wichtig, dass DIL und die serverseitige Weiterleitung nicht gleichzeitig aktiviert sind. Dies könnte zu einer doppelten Rechnungsstellung und einer Duplizierung der Daten führen. |

>[!MORELIKETHIS]
>
>* [Serverseitige Weiterleitung](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf.md)
