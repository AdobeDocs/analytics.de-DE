---
description: Erfahren Sie, wie Sie Referenzanfragen kopieren.
title: So kopieren Sie Referenzanfragen
feature: Report Builder
role: User, Admin
exl-id: 3cd77325-7461-4345-a672-64c03ea1ae5b
TQID: https://experienceleague.adobe.com/A-ef3rd0b7WMBRqBgmxFWpa35x8R7qYF1dMkF5gx5Ec
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 533
ht-degree: 40%

---

# Verweisanforderungen kopieren

{{legacy-arb}}

Eine Verweisanforderung verwendet Zellenwerte als Eingabe für Parameter, etwa als Daten- oder relationale Filter.

So übertragen oder kopieren Sie Verweisanforderungen und fügen diese in die Tabelle ein:

* Sie müssen mindestens eine gültige Anfrage in der Tabelle erstellen.

* Die von der Anfrage erzeugten Daten müssen eine Zelle enthalten, deren Wert entweder von einer Anfrage in einer anderen Zelle (mithilfe eines Aufschlüsselungs- oder Übereinstimmungsfilters) oder von einem Filter abhängt, der Eingaben aus in eine Zelle eingegebenen Daten übernimmt.

Sie können außerdem Anforderungen erstellen, die auf Eingabefilter von Anforderungen in unterschiedlichen Arbeitsblättern verweisen, aber nicht in unterschiedlichen Arbeitsmappen. Beispielsweise kann eine Anforderung in Blatt 2 eine Report Suite aus einer bestimmten Zelle in Blatt 1 und einen Datumsbereich aus einer Zelle in einer Anforderung in Blatt 2 verwenden. Die neue Ausgabe kann entweder in einem Blatt oder einem neuen Blatt innerhalb derselben Arbeitsmappe platziert werden. Wenn sich beim Einfügen einer relativen Anfrage ein Eingabefilter auf einem anderen Arbeitsblatt als dem Arbeitsblatt befindet, auf dem sich die kopierte Anfrageausgabe befindet, wird der Filter als absoluter Filter eingefügt.

>[!NOTE]
>
>Es kann keine einzelne Anforderung in mehreren Arbeitsblättern ausgegeben werden. Darüber hinaus kann das System einige der kopierten Anfragen nicht in neue Arbeitsmappen einfügen, da die Anfragen Eingabefilter aus anderen Arbeitsblättern enthalten. Zu den Eingabefiltern gehören Report Suites aus Zellen, Datumsbereiche aus Zellen, Filter aus Zellen und andere zugehörige Parameter.

**So kopieren Sie Referenzanfragen**

1. Wählen Sie die Zellen aus, die die zu kopierenden Anforderungen enthalten. Schließen Sie dabei die Eingabezelle oder die Zelle ein, auf die verwiesen wird.
1. Klicken Sie mit der rechten Maustaste auf die markierten Zellen und wählen Sie im Kontextmenü die Option **[!UICONTROL Anforderungen kopieren]** aus.

   Nach der Auswahl des Bereichs, in dem sich Anforderungen und Eingabezellen befinden, werden die Zellen mit diesen Elementen vom System hervorgehoben dargestellt.
1. Wählen Sie entweder eine Zelle oder einen Bereich angrenzender Zellen aus, in den die Anforderungen eingefügt werden sollen.

   Stellen Sie sicher, dass die ausgewählte Zelle bzw. der ausgewählte Bereich keine anderen Daten oder Anforderungen enthält.
1. Klicken Sie mit der rechten Maustaste auf die einzelne Zelle oder die oberste Zelle ganz links im Zellenbereich und wählen Sie **[!UICONTROL Anforderungen einfügen]** aus.

   Beim Einfügen von Anfragen, die eine Eingabezelle enthalten, umfassen die Optionen unter &quot;[!UICONTROL  einfügen] Folgendes:

   **Absolute Eingabezelle verwenden**: Fügt eine Kopie der Anforderung(en) und die Formatierung der ausgewählten Zellen in den hervorgehobenen Einfügebereich ein. Die Eingabezelle (die Zelle, auf die in einer der ursprünglichen Anforderungen verwiesen wurde) wird nicht eingefügt. Stattdessen verbleibt die Eingabezelle in der gleichen Position wie zuvor.

   **Relative Eingabezelle verwenden** Fügt eine Kopie der Anfrage(n) und die Formatierung, die mit den ausgewählten Zellen verknüpft ist, in den hervorgehobenen Bereich „Einfügen“ ein, einschließlich einer Kopie der Eingabezelle. Die räumliche Beziehung der Anforderung(en) zur Eingabezelle ist wie bei der/den ursprünglichen Anforderung(en). Während allerdings die neu eingefügten Zellen jetzt über eine Kopie der Anforderungen verfügen, befinden sich darin anfangs keine Inhalte. Dies liegt daran, dass bei der erneuten Erstellung der Eingabezelle durch die Einfügeoperation keine Daten damit verknüpft sind. Um Daten für die neu eingefügte(n) Anfrage(n) anzuzeigen, müssen Sie einen Wert in die Eingabezelle eingeben und dann die Anfrage(n) aktualisieren.
