---
description: Erfahren Sie, wie Sie Anfragen kopieren, einfügen und in einen anderen Teil des Arbeitsblatts verschieben können.
title: Kopieren angrenzender Anfragen
uuid: c8abec0d-6fbd-4a98-8672-ede81317487b
feature: Report Builder
role: User, Admin
exl-id: 99476ec5-f1f0-49f5-a2d8-354cec63c6b1
TQID: https://experienceleague.adobe.com/q1uVTribovAk-NJRXuAjW-kUIQfpquEPIbbOM9W8UmY
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 269
ht-degree: 31%

---

# Angrenzende Anforderungen kopieren

{{legacy-arb}}

Auf die gleiche Weise wie beim Kopieren und Einfügen von Anfragen können Sie Anfragen auch in einen anderen Teil des Arbeitsblatts verschieben, indem Sie [!UICONTROL Anfrage ausschneiden] aus dem Kontextmenü auswählen.

Wenn Sie eine Anforderung ausschneiden, wird sie von ihrer ursprünglichen Position entfernt. Erst nach Auswahl von [!UICONTROL Anforderung einfügen] wird die Anforderung an der neuen Position eingefügt. Wenn Sie sich nach dem Ausschneiden einer bestimmten Anforderung anders entscheiden und eine andere Anforderung aus einer anderen Zelle kopieren oder ausschneiden, belässt Report Builder die erste Auswahl in der ursprünglichen Zelle und reagiert nur auf die zweite Anforderung (kopieren oder ausschneiden).

>[!NOTE]
>
>Report Builder unterstützt nicht den Excel-Befehl zum Rückgängigmachen von Ausschneide- oder Einfügeanfragen.

Sie sind nicht darauf beschränkt, in dasselbe Blatt der Arbeitsmappe zu kopieren und einzufügen. Sie können eine Anforderung in ein Blatt kopieren und an eine Position in einem anderen Blatt in derselben Arbeitsmappe einfügen.

Es ist nicht möglich, jeweils nur eine Anfrage zu kopieren und einzufügen. Sie können mehrere Anfragen in der Tabelle auswählen und sie in einen leeren Bereich der Tabelle einfügen. Stellen Sie wie beim Kopieren und Einfügen einer Anfrage sicher, dass der Einfügebereich keine Zellen mit Anfragen enthält, die durch den Einfügevorgang ersetzt werden. Wenn das System feststellt, dass der Zielbereich zum Einfügen bereits eine oder mehrere Anforderungen enthält, zeigt Report Builder für kopierte oder ausgeschnittene Anforderungen das Menü [!UICONTROL Anforderungen einfügen] nicht an. Sie müssen eine andere Zelle als Ziel der Einfügeoperation wählen, damit sich die Anforderungen nicht überschneiden.
