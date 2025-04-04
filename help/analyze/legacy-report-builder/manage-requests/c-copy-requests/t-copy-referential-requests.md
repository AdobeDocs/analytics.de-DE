---
description: Erfahren Sie, wie Sie Referenzanfragen kopieren.
title: So kopieren Sie Referenzanfragen
feature: Report Builder
role: User, Admin
exl-id: 3cd77325-7461-4345-a672-64c03ea1ae5b
source-git-commit: fcecc8a493852f5682fd7fbd5b9bb484a850922c
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 80%

---

# Verweisanforderungen kopieren

{{legacy-arb}}

Eine Verweisanforderung verwendet Zellenwerte als Eingabe für Parameter, etwa als Daten- oder relationale Filter.

So übertragen oder kopieren Sie Verweisanforderungen und fügen diese in die Tabelle ein:

* Sie müssen mindestens eine gültige Anfrage in der Tabelle erstellen.

* Die von der Anfrage erzeugten Daten müssen eine Zelle enthalten, deren Wert entweder von einer Anfrage in einer anderen Zelle (mithilfe eines Aufschlüsselungs- oder Übereinstimmungsfilters) oder von einem Filter abhängt, der Eingaben aus in eine Zelle eingegebenen Daten übernimmt.

Sie können außerdem Anforderungen erstellen, die auf Eingabefilter von Anforderungen in unterschiedlichen Arbeitsblättern verweisen, aber nicht in unterschiedlichen Arbeitsmappen. Beispielsweise kann eine Report Suite in Blatt 2 eine Report Suite aus einer bestimmten Zelle in Blatt 1 und einen Datumsbereich aus einer Zelle in Blatt 2 verwenden. Die neue Ausgabe kann in einem der beiden Blätter oder in einem neuen Blatt innerhalb der Arbeitsmappe positioniert werden. Wenn Sie eine relative Anforderung einfügen und ein Eingabefilter sich auf einem anderen Arbeitsblatt befindet als die Ausgabe der kopierten Anforderung, wird der Filter als absoluter Filter eingefügt.

>[!NOTE]
>
>Es kann keine einzelne Anforderung in mehreren Arbeitsblättern ausgegeben werden. Darüber hinaus kann das System einige der kopierten Anfragen nicht in neue Arbeitsmappen einfügen, da die Anfragen Eingabefilter aus anderen Arbeitsblättern enthalten. Eingabefilter enthalten Report Suites aus Zellen, Datumsbereiche aus Zellen, Filter aus Zellen und andere zugehörige Parameter.

**So kopieren Sie Verweisanforderungen**

1. Wählen Sie die Zellen aus, die die zu kopierenden Anforderungen enthalten. Schließen Sie dabei die Eingabezelle oder die Zelle ein, auf die verwiesen wird.
1. Klicken Sie mit der rechten Maustaste auf die markierten Zellen und wählen Sie im Kontextmenü die Option **[!UICONTROL Anforderungen kopieren]** aus.

   Nach der Auswahl des Bereichs, in dem sich Anforderungen und Eingabezellen befinden, werden die Zellen mit diesen Elementen vom System hervorgehoben dargestellt.
1. Wählen Sie entweder eine Zelle oder einen Bereich angrenzender Zellen aus, in den die Anforderungen eingefügt werden sollen.

   Stellen Sie sicher, dass die ausgewählte Zelle bzw. der ausgewählte Bereich keine anderen Daten oder Anforderungen enthält.
1. Klicken Sie mit der rechten Maustaste auf die einzelne Zelle oder die oberste Zelle ganz links im Zellenbereich und wählen Sie **[!UICONTROL Anforderungen einfügen]** aus.

   Beim Einfügen von Anforderungen, die eine Eingabezelle enthalten, sind unter [!UICONTROL Anforderungen einfügen] folgende Optionen verfügbar:

   **Absolute Eingabezelle verwenden:** Hierdurch wird eine Kopie der Anforderung(en) und der mit den ausgewählten Zellen verknüpften Formatierung in den von Ihnen markierten Einfügebereich eingefügt. Die Eingabezelle (die Zelle, auf die in einer der ursprünglichen Anforderungen verwiesen wurde) wird nicht eingefügt. Stattdessen verbleibt die Eingabezelle an derselben Position wie zuvor.

   **Relative Eingabezelle verwenden:** Hierdurch wird eine Kopie der Anforderung(en) und der mit den ausgewählten Zellen verknüpften Formatierung in den von Ihnen markierten Einfügebereich, einschließlich einer Kopie der Eingabezelle, eingefügt. Die räumliche Beziehung der Anforderung(en) zur Eingabezelle ist wie bei der/den ursprünglichen Anforderung(en). Während allerdings die neu eingefügten Zellen jetzt über eine Kopie der Anforderungen verfügen, befinden sich darin anfangs keine Inhalte. Dies liegt daran, dass bei der erneuten Erstellung der Eingabezelle durch die Einfügeoperation keine Daten damit verknüpft sind. Um Daten für die neu eingefügte(n) Anforderung(en) anzuzeigen, müssen Sie einen Wert in die Eingabezelle eingeben und dann die Anforderungen aktualisieren.
