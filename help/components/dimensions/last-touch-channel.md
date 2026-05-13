---
title: Letztkontakt-Kanal
description: Der neueste Marketing-Kanal innerhalb des Interaktionsablaufs des Besuchers.
feature: Dimensions
exl-id: 62a47de5-ee1a-4394-aa63-75cdda92ba6a
TQID: https://experienceleague.adobe.com/wUNsv-0snBfk6EE6yeCEuT8-hGvBu9U8tjKDfxhVRA0
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: c80b99d6-98b9-4aeb-b5c4-933ef2ef705cid: f836f655-eebe-4b76-82bc-697955ec1ce3id: fab61dd8-112a-4e5e-ad5f-fb0240b7a60b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 337
ht-degree: 67%

---

# Letztkontakt-Kanal

Der „Letztkontakt-Kanal[ (Dimension](overview.md) zeigt den neuesten Marketing-Kanal an, dem ein Besucher während des Interaktionszeitraums dieses Besuchers entspricht (standardmäßig 30 Tage). Diese Dimension ist nützlich, um zu verstehen, welche Marketing-Kanäle den Traffic zu Ihrer Site leiten, der zu Konversionen führt, sodass Sie Ihre Marketing-Bemühungen auf Bereiche konzentrieren können, die am effektivsten sind.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist direkt auf die Kanalnamen, die Sie im [Marketing-Kanal-Manager](/help/admin/tools/manage-rs/edit-settings/marketing-channels/c-channels.md) definiert haben.

Jeder an die Datenerfassungs-Server von Adobe gesendete Treffer durchläuft die Verarbeitungsregeln für den Marketing-Kanal Ihrer Report Suite. Jede Regel wird in numerischer Reihenfolge durchlaufen, bis eine Übereinstimmung gefunden wird, in der dieser Marketing-Kanal mit dem Treffer verknüpft ist. Der Letztkontakt-Kanal bleibt so lange bestehen, bis der Besucher die Website länger als den Besucherinteraktionszeitraum (standardmäßig 30 Tage) nicht mehr besucht hat.

Führen Sie die folgenden Schritte aus, um diese Dimension auf einen bestimmten Wert zu setzen:

* Legen Sie das gewünschte Dimensionselement als Kanal im Marketing-Kanal-Manager unter den Report Suite-Einstellungen fest.
* Legen Sie eine Marketing-Kanalverarbeitungsregel fest, die die gewünschten Kriterien für den Treffer enthält.
* Der Treffer des Besuchers auf Ihrer Site muss den Kriterien entsprechen, die in der Marketing-Kanalverarbeitungsregel beschrieben sind.

>[!TIP]
>
>Die Verwendung dieser Dimension mit Metriken, die [Partizipationsattribution](/help/analyze/analysis-workspace/attribution/models.md) verwenden, kann `None` eine Gewichtung zuordnen, wenn andere Attributionsmodelle dies nicht tun. Teilnahmemetriken erfordern für eine Gutschrift einen Marketing[Kanal (](../metrics/instances.md)) innerhalb des Berichtsfensters. Wenn der Marketing-Kanal ursprünglich außerhalb des Reporting-Fensters festgelegt wurde und nur der persistierte Wert innerhalb des Reporting-Fensters vorhanden ist, weisen Teilnahmemetriken dem `None` eine Gutschrift zu. Andere Attributionsmodelle schreiben dem persistenten Wert eine Gutschrift zu. Wenn Sie in diesem Szenario eine Attribution an `None` vermeiden möchten, sollten Sie ein Nicht-Teilnahme-Attributionsmodell verwenden.

## Dimensionselemente

Die Dimensionenselemente umfassen alle Kanalnamen im Marketing-Kanal-Manager. Standardmäßig umfassen die Werte `"Paid search"`, `"Natural search"`, `"Display"`, `"Email"`, `"Affiliate"`, `"Direct"`, `"Internal"`, `"Social networks"` und `"Referring domains"`. Sie können Kanäle im Marketing-Kanal-Manager hinzufügen oder löschen, die sich auf die Werte dieser Dimension auswirken.
