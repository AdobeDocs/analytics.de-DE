---
description: Führt einige Überlegungen auf, die Sie vor dem Löschen von Segmenten anstellen sollten.
title: Segmente löschen
feature: Segmentation
exl-id: 434b6fec-1dfa-4375-a9de-d47fad2c64bc
source-git-commit: b96210a478c46f5d9cbf49c6288b698dc47d64fe
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 91%

---

# Segmente löschen

Führt einige Überlegungen auf, die Sie vor dem Löschen von Segmenten anstellen sollten.

Wenn Sie ein Segment löschen, hat dies folgende Auswirkungen:

* Terminierte Berichte und Dashboards, auf die dieses Segment angewendet wird, funktionieren weiter normal, d. h., das Segment bzw. das Dashboard verwendet weiterhin das gelöschte Segment.
* Terminierte Berichte werden nicht aktualisiert, wenn Sie ein Segment mit demselben Namen aktualisieren. Ein Beispiel: Angenommen, Sie haben 2 Segmente mit demselben Namen in unterschiedlichen Report Suites:

  | Segmentname | Report Suite |
  |---|---|
  | Besuche aus Kalifornien | mainprod |
  | Besuche aus Kalifornien | maindev |


  Sie haben ein Lesezeichen, das auf das Segment für die `mainprod` Report Suite verweist. Dann löschen Sie das Segment, weil es sich um ein Duplikat handelt. Das Lesezeichen funktioniert weiterhin und referenziert die Definition des gelöschten Segments. Wenn Sie die Segmentdefinition des verbleibenden Segments ändern und „Catalina Island“ und „Tijuana Mexiko“ einfügen, wird das auf das Lesezeichen angewendete Segment nicht geändert. Es verwendet weiterhin die alte Definition. Um dies zu beheben, müssen Sie das Lesezeichen aktualisieren, damit es die neue Definition referenziert. Wenn Sie nicht sicher sind, ob ein Lesezeichen, ein Dashboard oder ein terminierter Bericht ein gelöschtes Segment verwendet, können Sie den Namen des Segments ändern, damit deutlich wird, ob das Lesezeichen das Segment verwendet.
