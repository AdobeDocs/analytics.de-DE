---
title: Letztkontakt-Kanal
description: Der neueste Marketing-Kanal innerhalb des Interaktionsablaufs des Besuchers.
feature: Dimensions
exl-id: 62a47de5-ee1a-4394-aa63-75cdda92ba6a
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 90%

---

# Letztkontakt-Kanal

Der „Letztkontakt-Kanal[ (Dimension](overview.md) zeigt den neuesten Marketing-Kanal an, dem ein Besucher während des Interaktionszeitraums dieses Besuchers entspricht (standardmäßig 30 Tage). Diese Dimension ist nützlich, um zu verstehen, welche Marketing-Kanäle den Traffic zu Ihrer Site leiten, der zu Konversionen führt, sodass Sie Ihre Marketing-Bemühungen auf Bereiche konzentrieren können, die am effektivsten sind.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist direkt auf die Kanalnamen, die Sie im [Marketing-Kanal-Manager](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-channels.md) definiert haben.

Jeder an die Datenerfassungs-Server von Adobe gesendete Treffer durchläuft die Verarbeitungsregeln für den Marketing-Kanal Ihrer Report Suite. Jede Regel wird in numerischer Reihenfolge durchlaufen, bis eine Übereinstimmung gefunden wird, in der dieser Marketing-Kanal mit dem Treffer verknüpft ist. Der Letztkontakt-Kanal bleibt so lange bestehen, bis der Besucher die Website länger als den Besucherinteraktionszeitraum (standardmäßig 30 Tage) nicht mehr besucht hat.

Führen Sie die folgenden Schritte aus, um diese Dimension auf einen bestimmten Wert zu setzen:

* Legen Sie das gewünschte Dimensionselement als Kanal im Marketing-Kanal-Manager unter den Report Suite-Einstellungen fest.
* Legen Sie eine Marketing-Kanalverarbeitungsregel fest, die die gewünschten Kriterien für den Treffer enthält.
* Der Treffer des Besuchers auf Ihrer Site muss den Kriterien entsprechen, die in der Marketing-Kanalverarbeitungsregel beschrieben sind.

## Dimensionselemente

Die Dimensionenselemente umfassen alle Kanalnamen im Marketing-Kanal-Manager. Standardmäßig umfassen die Werte `"Paid search"`, `"Natural search"`, `"Display"`, `"Email"`, `"Affiliate"`, `"Direct"`, `"Internal"`, `"Social networks"` und `"Referring domains"`. Sie können Kanäle im Marketing-Kanal-Manager hinzufügen oder löschen, die sich auf die Werte dieser Dimension auswirken.
