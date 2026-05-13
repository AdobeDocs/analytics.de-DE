---
description: Erfahren Sie, wie Sie eine Tabelle aus einer Quellarbeitsmappe in eine oder mehrere Zielarbeitsmappen kopieren.
title: Kopieren von Anfragen und Arbeitsblättern zwischen Arbeitsmappen
uuid: 6b2c4259-d8cb-430e-819f-38e213dd2661
feature: Report Builder
role: User, Admin
exl-id: 1a2363da-603e-4d1d-aefa-14ce71554247
TQID: https://experienceleague.adobe.com/0GVqb80fMIVJlip2dWGgzllmCGG2Hc8368WZlThzzh0
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
source-wordcount: 379
ht-degree: 21%

---

# Anforderungen und Arbeitsblätter zwischen Arbeitsmappen kopieren

{{legacy-arb}}

Kopieren einer gesamten Tabelle in einer Quellarbeitsmappe in eine Tabelle in einer oder mehreren Zielarbeitsmappen. Dazu müssen mindestens zwei Arbeitsmappen in derselben Instanz von Excel geöffnet sein:

* Die erste Quellarbeitsmappe enthält ein Arbeitsblatt (Arbeitsblatt) mit Anfragen, die Zellen zugeordnet sind.

* Die zusätzlichen Ziel-Arbeitsmappen sind die Ziele. Für jede neue Zielarbeitsmappe sollten Sie sich bei derselben Report Suite wie die Quellarbeitsmappe anmelden, bevor Sie Tabellen mit Anfragen einfügen können.

>[!NOTE]
>
>Sie müssen sich bei der Zielarbeitsmappe mit derselben Report Suite wie die Quellarbeitsmappe anmelden. Die Anfragen in beiden Arbeitsmappen müssen mit derselben Report Suite-Anmeldung erstellt werden.

1. Klicken Sie mit der rechten Maustaste auf das Arbeitsblatt in der Quellarbeitsmappe und wählen Sie **[!UICONTROL Arbeitsblatt mit Anforderungen kopieren]**.
1. Klicken Sie in der Zielarbeitsmappe mit der rechten Maustaste auf ein Arbeitsblatt und wählen Sie **[!UICONTROL Arbeitsblatt mit Anforderungen einfügen]**.

   Dieselbe Instanz von Excel bedeutet, dass auf dem Computer gerade nur ein einziger Excel-Prozess ([!DNL excel.exe]) ausgeführt wird. Wenn Sie zwei Instanzen von Excel starten und versuchen, ein Arbeitsblatt aus einer Arbeitsmappe in der ersten Instanz von Excel in eine Arbeitsmappe in der zweiten Instanz von Excel zu kopieren, bietet Report Builder keine Möglichkeit, ein Arbeitsblatt in das Kontextmenü der zweiten Instanz von Excel einzufügen.

   Wenn Sie sich mit verschiedenen Report Suites bei den Quell- und Ziel-Arbeitsmappen anmelden, werden beim Einfügevorgang nur die Ergebnisse angezeigt, die sich auf die Formatierung der Ziel-Arbeitsmappe auswirken. Report Builder zeigt eine Meldung darüber an, dass die Informationen für die Anforderungen einer bestimmten Report Suite (in der Quellarbeitsmappe) nicht in der Zielarbeitsmappe verfügbar sind. Um die in die Zielarbeitsmappe eingefügten Anforderungen anzuzeigen, müssen Sie sich bei der Zielarbeitsmappe mit derselben Report Suite wie bei der Quellarbeitsmappe anmelden.

   Sie können eine oder mehrere Anforderungen aus einem Arbeitsblatt in eine Arbeitsmappe kopieren und in ein Arbeitsblatt in einer anderen Arbeitsmappe einfügen, solange die zweite Arbeitsmappe als ein anderes Dokument in derselben Instanz von Excel geöffnet ist. Die Anfragen in beiden Arbeitsmappen müssen mit derselben Report Suite-Anmeldung erstellt werden.
