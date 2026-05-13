---
title: Analysieren von Marketing-Kanälen
description: Erfahren Sie, wie Sie die Dimensionen von Marketing-Kanäle in Workspace verwenden.
feature: Marketing Channels
exl-id: 7030e41a-4e92-45c7-9725-66a3ef019313
TQID: https://experienceleague.adobe.com/XWjRuwOusH-TsOb5rzG8rAIkye3faYxfZzyQOMrav3Q
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2: id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: b3a8b8a0-1cc2-48a8-ac82-ffd9c66ccab4id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 435
ht-degree: 77%

---

# Analysieren von Marketing-Kanälen

>[!NOTE]
>
>Um die Effektivität von Marketing-Kanälen für Attribution und Adobe Analytics zu maximieren, haben wir einige [überarbeitete Best Practices“ ](/help/components/c-marketing-channels/mchannel-best-practices.md).
>
>Analytics-Admins können Marketing-Kanäle für ihre Organisationen verwalten, wie unter [Verwalten von Marketing-Kanälen](/help/admin/tools/manage-rs/edit-settings/marketing-channels/c-channels.md) beschrieben.

Sie möchten wahrscheinlich wissen, welcher Ihrer Marketing-Kanäle der effektivste ist und bei wem, damit Sie Ihre Bemühungen gezielter ausrichten und eine bessere Rendite aus Ihrem Marketing-Budget erzielen können. In Adobe Analytics sind die Dimensionen und Metriken der Marketing-Kanäle in Workspace eines der Tools, mit denen Sie den Einfluss verschiedener Kanäle auf Ihre Bestellungen, Ihren Umsatz usw. verfolgen und nützliche Kanaleinblicke erhalten können. Hier sind die Dimensionen und Metriken, die Sie in Bezug auf Marketing-Kanäle verwenden können:

![](assets/mc-dims.png)

| Dimension/Metrik | Definition |
| --- | --- |
| Marketing-Kanal | Dies ist die empfohlene Dimension für Marketing-Kanäle. Attributionsmodelle können zur Laufzeit darauf angewendet werden. Diese Dimension verhält sich identisch mit den Dimensionen des Letztkontakt-Kanals, ist jedoch anders gekennzeichnet, um Verwirrung bei der Verwendung mit einem anderen Attributionsmodell zu vermeiden. |
| Letztkontakt-Kanal | Veraltete Dimension mit vorab angewendetem und unveränderlichem Letztkontakt-Attributionsmodell. |
| Erstkontakt-Kanal | Veraltete Dimension mit vorab angewendetem und unveränderlichem Erstkontakt-Attributionsmodell. |
| Marketing-Kanalinstanzen | Diese Metrik misst, wie oft ein Marketing-Kanal in einer Bildanforderung definiert wurde, einschließlich standardmäßiger Seitenansichten und benutzerspezifischer Link-Aufrufe. Enthält keine persistenten Werte. |
| Neue Interaktionen | Diese Metrik ähnelt Instanzen, wird jedoch nur inkrementiert, wenn in einer Bildanfrage ein Erstkontakt-Marketing-Kanal definiert wird. |

## Basisanalyse

Diese Freiform-Tabelle zeigt die Metriken „Online-Bestellungen“, „Online-Umsatz“ und „Konversionsrate“ für jeden Marketing-Kanal an:

![](assets/mc-viz1.png)

Hier sehen Sie die Online-Bestellungen und den Online-Umsatz der einzelnen Marketing-Kanäle in einem Ringdiagramm:

![](assets/mc-viz2.png)

Dieses Liniendiagramm zeigt die Trends bei Online-Bestellungen für verschiedene Kanäle im Zeitverlauf:

![](assets/mc-viz3.png)

## Erweiterte Analyse

Details zu Marketing-Kanälen gehen tiefer in jeden Kanal ein, um Ihnen spezifische Kampagnen, Platzierungen usw. zu zeigen. Sie können jeden Marketing-Kanal in Details aufschlüsseln:

![](assets/mc-viz4.png)

## Anwenden von Attributionsmodellen

Sie können [Attribution](/help/analyze/analysis-workspace/attribution/overview.md) verwenden, um verschiedene Attributionsmodelle sofort anzuwenden:

![](assets/mc-viz5.png)

Beachten Sie, dass dieselbe Metrik (Online-Bestellungen) unterschiedliche Ergebnisse generiert, wenn Sie verschiedene Attributionsmodelle anwenden.

## Tab-übergreifende Marketing-Analyse

Die älteren Firstkontakt- und Letztkontakt-Kanäle bieten einen hilfreichen Einblick in die Kanalinteraktionen:

![](assets/mc-viz6.png)

In diesem Video erfahren Sie mehr über tabellenübergreifende Marketing-Analyse: [Verwenden der tabellenübergreifenden Analyse zum Untersuchen der grundlegenden Marketing-Attribution in Analysis Workspace](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/attribution-iq/using-cross-tab-analysis-to-explore-basic-marketing-attribution-in-analysis-workspace.html?lang=de).
