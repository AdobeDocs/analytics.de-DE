---
description: Erfahren Sie, wie Sie eine Tabelle aus einer Quellarbeitsmappe in eine oder mehrere Zielarbeitsmappen kopieren.
title: Kopieren von Anfragen und Arbeitsblättern zwischen Arbeitsmappen
uuid: 6b2c4259-d8cb-430e-819f-38e213dd2661
feature: Report Builder
role: User, Admin
exl-id: 1a2363da-603e-4d1d-aefa-14ce71554247
source-git-commit: fcecc8a493852f5682fd7fbd5b9bb484a850922c
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 54%

---

# Anforderungen und Arbeitsblätter zwischen Arbeitsmappen kopieren

{{legacy-arb}}

Kopieren einer gesamten Tabelle in einer Quellarbeitsmappe in eine Tabelle in einer oder mehreren Zielarbeitsmappen. Dazu müssen mindestens zwei Arbeitsmappen in derselben Instanz von Excel geöffnet sein:

* Die erste Quellarbeitsmappe enthält ein Arbeitsblatt (Arbeitsblatt) mit Anfragen, die Zellen zugeordnet sind.

* Die zusätzlichen Ziel-Arbeitsmappen sind die Ziele. Für jede neue Zielarbeitsmappe sollten Sie sich bei derselben Report Suite wie die Quellarbeitsmappe anmelden, bevor Sie Tabellen mit Anfragen einfügen können.

>[!NOTE]
>
>Sie müssen sich bei der Zielarbeitsmappe mit derselben Report Suite wie die Quellarbeitsmappe anmelden. Die Anforderungen in beiden Arbeitsmappen müssen mit Hilfe derselben Report Suite erstellt werden.

1. Klicken Sie mit der rechten Maustaste auf das Arbeitsblatt in der Quellarbeitsmappe und wählen Sie **[!UICONTROL Arbeitsblatt mit Anforderungen kopieren]**.
1. Klicken Sie in der Zielarbeitsmappe mit der rechten Maustaste auf ein Arbeitsblatt und wählen Sie **[!UICONTROL Arbeitsblatt mit Anforderungen einfügen]**.

   Dieselbe Instanz von Excel bedeutet, dass auf dem Computer gerade nur ein einziger Excel-Prozess ([!DNL excel.exe]) ausgeführt wird. Wenn Sie zwei Instanzen von Excel starten und versuchen, ein Arbeitsblatt aus einer Arbeitsmappe in der ersten Instanz von Excel in eine Arbeitsmappe in der zweiten Instanz von Excel zu kopieren, bietet der Report Builder keine Möglichkeit, ein Arbeitsblatt in das Kontextmenü der zweiten Instanz von Excel einzufügen.

   Wenn Sie sich bei der Quell- und Zielarbeitsmappe für unterschiedliche Report Suites anmelden, sind als Ergebnis der Einfügeoperation in der Zielarbeitsmappe ausschließlich die Formatierungen sichtbar. Report Builder zeigt eine Meldung darüber an, dass die Informationen für die Anforderungen einer bestimmten Report Suite (in der Quellarbeitsmappe) nicht in der Zielarbeitsmappe verfügbar sind. Um die in die Zielarbeitsmappe eingefügten Anforderungen sichtbar zu machen, müssen Sie sich zuerst in der Zielarbeitsmappe für dieselbe Report Suite wie in der Quellarbeitsmappe anmelden.

   Sie können eine oder mehrere Anforderungen aus einem Arbeitsblatt in einer Arbeitsmappe kopieren und in ein Arbeitsblatt in einer anderen Arbeitsmappe einfügen, sofern die zweite Arbeitsmappe als weiteres Dokument in derselben Instanz von Excel geöffnet ist. Die Anforderungen in beiden Arbeitsmappen müssen mit Hilfe derselben Report Suite erstellt werden.
