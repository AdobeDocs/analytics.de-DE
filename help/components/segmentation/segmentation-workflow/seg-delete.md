---
description: Führt einige Überlegungen auf, die Sie vor dem Löschen von Segmenten anstellen sollten.
title: Segmente löschen
feature: Segmentation
exl-id: 434b6fec-1dfa-4375-a9de-d47fad2c64bc
source-git-commit: 80e4a3ba4a5985563fcf02acf06997b4592261e4
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 39%

---

# Segmente löschen

In diesem Artikel werden einige Überlegungen aufgeführt, die Sie beachten sollten, bevor Sie Segmente löschen.

Wenn Sie ein Segment löschen:

* Terminierte Berichte und Dashboards, auf die dieses Segment angewendet wird, funktionieren weiterhin normal. Beispielsweise verwendet das Segment oder Dashboard weiterhin das gelöschte Segment.
* Terminierte Berichte werden nicht aktualisiert, wenn Sie ein Segment mit demselben Namen aktualisieren. Im Folgenden finden Sie ein Beispiel: Angenommen, Sie haben zwei Segmente mit demselben Namen in verschiedenen Report Suites:

  | Segmentname | Report Suite |
  |---|---|
  | Besuche aus Kalifornien | mainprod |
  | Besuche aus Kalifornien | maindev |

  Sie haben ein Lesezeichen, das auf das Segment für die Report Suite [!UICONTROL mainprod] verweist. Dann löschen Sie dieses Segment, da es sich um ein Duplikat handelt. Das Lesezeichen funktioniert weiterhin und referenziert die Definition des gelöschten Segments. Wenn Sie die Segmentdefinition des verbleibenden Segments ändern und „Catalina Island“ und „Tijuana Mexiko“ einfügen, wird das auf das Lesezeichen angewendete Segment nicht geändert. Das Segment verwendet die alte Definition. Um dies zu beheben, müssen Sie das Lesezeichen aktualisieren, damit es die neue Definition referenziert. Wenn Sie sich nicht sicher sind, ob ein Lesezeichen, ein Dashboard oder ein terminierter Bericht ein gelöschtes Segment verwendet, können Sie den Namen des verbleibenden Segments ändern, um anzugeben, ob das Lesezeichen das verbleibende Segment verwendet.
