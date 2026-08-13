---
title: Algorithmische Zuordnung
description: Machen Sie sich mit den Details des algorithmischen Attributionsmodells vertraut.
feature: Attribution
role: User, Admin
exl-id: dd2b2a5b-9c36-4534-999f-f96604f29eab
TQID: 'https://experienceleague.adobe.com/jPLoQcRU8bpCGjKJ37mioUdZOFDUwNehmyBhdx7lj8c'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2: id: b3a8b8a0-1cc2-48a8-ac82-ffd9c66ccab4
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 38%

---

# Algorithmische Attribution

Das algorithmische [Attributionsmodell](models.md) in Analysis Workspace unterscheidet sich von anderen Modellen insofern, als es mithilfe statistischer Verfahren Gewichtungen über die Dimensionselemente in Ihrem Bericht oder Ihrer Freiform-Tabelle verteilt. Wie alle anderen Attributionsmodelle in Analysis Workspace kann die algorithmische Attribution für jede Dimension oder Metrik verwendet werden. Algorithmische Attribution unterstützt eine unbegrenzte Segmentierung und Aufschlüsselungen und verteilt 100 % der Konversionen auf eine oder mehrere Dimensionen in der Tabelle (auch als „fraktionelle“ Attribution bezeichnet).


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Algorithmische ](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/analysis-workspace/attribution-iq/algorithmic-model-in-attribution-iq){target="_blank"}) für ein Demovideo.

>[!ENDSHADEBOX]


Der für die Zuordnung verwendete Algorithmus basiert auf der Harsanyi-Dividende aus der kooperativen Spieltheorie. Die Harsanyi-Dividende ist eine Verallgemeinerung der Shapley-Value-Lösung (benannt nach Lloyd Shapley, einem Wirtschaftsnobelpreisträger), um in einem Spiel mit ungleichen Beiträgen zum Ergebnis Kredite unter den Spielern zu verteilen.

Auf allgemeiner Ebene wird bei der Attributionsberechnung der Konversion für jeden Touchpoint jeder der Marketing-Touchpoints innerhalb eines Lookback-Fensters als eine Koalition von Playern berücksichtigt. Dieser Koalition von Akteuren muss ein Überschuss gerecht verteilt werden. Die Überschussverteilung jeder Koalition wird aus dem Überschuss bestimmt, den jede Subkoalition zuvor rekursiv erzeugt hat.

Weitere Einzelheiten finden Sie in den Originalpapieren von John Harsanyi und Lloyd Shapley:

* Shapley, Lloyd S. (1953). A value for n-person games. *Contributions to the Theory of Games, 2(28)*, 307-317.
* Harsanyi, John C. (1963). A simplified bargaining model for the n-person cooperative game. *International Economic Review 4(2)*, 194-220.

>[!NOTE]
>
>Das Ergebnis der algorithmischen Attribution unterscheidet sich nur dann von anderen Modellen, wenn innerhalb des angegebenen Lookback-Fensters mehrere Touchpoints vorhanden sind. Konversionen mit einem einzigen Touchpoint erhalten eine Gewichtung von 100 % unabhängig vom Attributionsmodell.
