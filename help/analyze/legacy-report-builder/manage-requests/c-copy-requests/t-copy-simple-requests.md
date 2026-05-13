---
description: Erfahren Sie, wie Sie eine einfache Anfrage kopieren.
title: Kopieren einfacher Anfragen
uuid: ff20560a-01ee-47e7-8bd1-b73edb010456
feature: Report Builder
role: User, Admin
exl-id: ceed28d5-cb7f-4343-96fd-2ce09f5a3515
TQID: https://experienceleague.adobe.com/Zd6s6l-sW40WlEtk2Z8AFcNLkC-l4wxcmo67XajqAJs
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 527
ht-degree: 40%

---

# Einfache Anforderungen kopieren

{{legacy-arb}}

Kopieren Sie eher eine einfache Anforderung als eine Verweisanforderung. Eine einfache Anfrage ist eine Anfrage, die keine Verweise auf eine andere Anfrage oder den Inhalt einer Zelle enthält.

Eine [Verweisanforderung](/help/analyze/legacy-report-builder/manage-requests/c-copy-requests/t-copy-referential-requests.md) verwendet Werte aus Zellen als Eingabe für Parameter, etwa als Daten- oder relationale Filter. Diese Filter verwenden entweder Übereinstimmungs- oder Trendwerte und basieren auf Ergebnissen einer vorherigen Anfrage oder auf dem vom Benutzer eingegebenen Inhalt einer Zelle, die als Eingabezelle bezeichnet wird.

So kopieren Sie eine einfache Anfrage

1. Es muss eine gültige Anforderung erstellt werden.
1. Klicken Sie mit der rechten Maustaste auf eine der Zellen, die der Anforderung zugeordnet ist, oder wählen Sie einen Bereich von Zellen aus, der Anforderungen enthält.

   Gehen Sie bei der Auswahl von zu kopierenden Zellen aus der Gruppe von Zellen, die von der Anforderung abgedeckt sind, einheitlich vor. Es bietet sich an, mit der Zelle ganz oben links in der Gruppe der Zellen, die von der Anforderung abgedeckt sind, zu beginnen und dann von links nach rechts weiterzumachen. Dies hat seine Ursache darin, dass ein Excel-Arbeitsblatt über hunderte von Spalten und tausende von Zeilen verfügt, die für die Erweiterung nach rechts und unten zur Verfügung stehen. Wenn Sie sich entscheiden, eine Anfragekopie aus der am weitesten rechts gelegenen oder unteren Zelle in einem mit einer Anfrage verknüpften Zellensatz zu starten, erlaubt Ihnen das System nicht, die Anfrage einzufügen, wenn die einzufügenden Zellen über den linken oder oberen Rand des Arbeitsblatts hinausgehen.
1. Wählen Sie **[!UICONTROL Anforderung kopieren]**.
1. Klicken Sie in einem anderen Bereich des Arbeitsblatts mit der rechten Maustaste auf eine leere Zelle (d. h. eine Zelle, die keine Anforderung enthält).

   Um zu verhindern, dass bereits erstellte Anforderungen verloren gehen oder beschädigt werden, können Sie Zellen mit Anforderungen nicht in Zellen einfügen, die derzeit Anforderungen zugeordnet sind. Wenn Sie Zellen mit Anforderungen kopieren oder ausschneiden, ist die Option [!UICONTROL Anforderungen einfügen] beim Rechtsklick auf Zellen (oder den Zellensatz) mit Anforderungen im Kontextmenü nicht verfügbar. Sie müssen eine andere Zelle als Ziel der Einfügeoperation wählen, damit sich die Anforderungen nicht überschneiden. Dies gilt unabhängig davon, ob Sie eine einzelne Zelle mit einer Einfügeanforderung oder einen Bereich von Zellen mit Anforderungen auswählen.
1. Klicken Sie auf **[!UICONTROL Anforderungen einfügen]**.

   Eine Kopie der ursprünglichen Anforderung wird in den Zellen in einer Position bzw. Positionen relativ zur ursprünglichen Anforderung abgelegt.

   >[!NOTE]
   >
   >Nur die Anforderungen werden kopiert, nicht die Zelleninhalte. Wenn Sie über andere Informationen verfügen, die nicht auf Anfragen basieren, aber für das Verständnis der in den Zellen angezeigten Daten relevant sind (z. B. Tabellenspaltenüberschriften oder Zeilenkennungen), verwenden Sie die Standardbefehle von Excel zum Kopieren und Einfügen.

   Da Excel zum Kopieren von Zelleninhalten und zum Kopieren von Anforderungen verschiedene Zwischenablagen verwendet, können Sie sowohl Nicht-Anfrage-Zelleninhalte als auch Anforderungen kopieren, indem Sie eine Kopier-/Einfüge- und Kopieranforderung/Einfügeanforderung in Reihe ausführen. Wenn Sie jedoch auf Anfragen im Arbeitsblatt Formatierungen anwenden und dann kopieren und einfügen, reproduziert Report Builder die Originalformatierung (z. B. Rahmen, Schriftarten usw.) Im Bereich Einfügen :

   Durch das Ändern einer Anforderung, die Sie kopiert oder in die Zwischenablage ausgeschnitten haben, wird die Anforderung aus der Zwischenablage entfernt. Um den ursprünglichen Zustand der Anfrage beizubehalten, dürfen Sie eine Anfrage daher nicht zwischen dem Kopieren und dem Einfügen ändern.
