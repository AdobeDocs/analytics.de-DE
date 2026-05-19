---
description: Häufig gestellte Fragen zu den Funktionen, der Funktionalität und den Problemen bezüglich der serverseitigen Weiterleitung.
title: Häufig gestellte Fragen zur serverseitigen Weiterleitung
feature: Report Suite Settings
exl-id: 63103d2b-e2e8-42da-bdbd-be90abe305f7
role: Admin
TQID: https://experienceleague.adobe.com/3i6RY7JRPlJc-9NjsQXBPn5SEOn0m4JrtL85Kl84ilM
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: d3cdead0-685a-4489-9250-4bb709942f66id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 7d733a6375f6c6009563bc53f5a3ff090dbc48ed
workflow-type: tm+mt
source-wordcount: 707
ht-degree: 42%

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
| F.: Was passiert, wenn ich Report Suites mit Multi-Suite-Tags habe, die separaten CX Enterprise-Organisationen zugeordnet sind? | Sie sollten niemals Daten aus einem einzelnen Analytics-Treffer an zwei Report Suites senden, die zu separaten CX Enterprise-Organisationen gehören. In diesem Fall leiten wir den Treffer jedoch nur an die CX Enterprise-Organisation weiter, die der Identity Service-Einrichtung auf der Seite entspricht. |
| F.: Was passiert, wenn ich Multi-Suite-Tagging verwende und nur eine meiner Report Suites meiner CX Enterprise-Organisation zugeordnet ist und die andere nicht? | Wir leiten den Treffer an den entsprechenden Datenerfassungsserver für die CX Enterprise-Organisation in Ihrer zugeordneten Report Suite weiter. Da die nicht zugeordnete Report Suite jedoch keine zugeordnete Datenquelle in Audience Manager hat, werden keine Daten für die nicht zugeordnete Report Suite in Audience Manager aufgezeichnet. |
| F.: Was passiert, wenn ich eine Report Suite habe, die mehreren CX Enterprise-Organisationen zugeordnet ist? | Analytics betrachtet diese Report Suite als nicht zugeordnet und lässt keine Server-seitige Weiterleitung für diese Report Suite zu. Wenden Sie sich an die Kundenunterstützung, um dieses Zuordnungsproblem zu beheben. |
| F: Ist die Report Suite-basierte, serverseitige Weiterleitungsmethode langsamer als die Tracking-Server-basierte, serverseitige Weiterleitung? | Nein, die Antwortzeit ist dieselbe. |
| F.: Was passiert, wenn wir zwei CX Enterprise-Organisationen (oder Adobe Audience Manager-Instanzen) haben und Daten zwischen beiden CX Enterprise-Organisationen austauschen möchten? Kann ich einen einzelnen Analytics-Treffer Server-seitig an mehrere CX Enterprise-Organisationen weiterleiten? | Nein. Wenn Sie Daten, die unter einer CX Enterprise-Organisation erfasst wurden, für eine andere CX Enterprise-Organisation freigeben müssen, empfehlen wir, alle entsprechenden Zielgruppen mithilfe des Zielgruppen-Marketplaces von einer Audience Manager-Instanz zur anderen zu senden. |
| F: Führt die serverseitige Weiterleitung zu einer zusätzlichen Rechnungsstellung in Audience Manager oder Analytics? | In Analytics erfolgt keine zusätzliche Rechnungsstellung. In Audience Manager werden weitergeleitete Hits wie andere Hits behandelt und abgerechnet.  Daher ist es wichtig, dass DIL und die serverseitige Weiterleitung nicht gleichzeitig aktiviert sind. Dies könnte zu einer doppelten Rechnungsstellung und einer Duplizierung der Daten führen. |

>[!MORELIKETHIS]
>
>* [Serverseitige Weiterleitung](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf.md)
