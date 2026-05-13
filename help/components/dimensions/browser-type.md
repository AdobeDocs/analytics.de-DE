---
title: Browser-Typ
description: Die Organisation, die den Browser erstellt hat.
feature: Dimensions
exl-id: 2a88ebc6-879e-4e5b-a8e5-40a32d54ac1b
TQID: https://experienceleague.adobe.com/Qb4g-5RXrK42ui4xG86YEv3ozVqmqHrn9Bj5zqXmzPU
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: d2311670-43bd-4c2e-bc98-1da2aaba9cefid: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 156
ht-degree: 69%

---

# Browser-Typ

Die Dimension „Browser[Typ“ ](overview.md) die Organisationen auf, die den Browser erstellt haben, den der Besucher verwendet. Diese Dimension ist nützlich, wenn Sie sehen möchten, welche übergeordneten Browser von Besuchern verwendet werden. Sie ist insofern nützlicher als die Dimension „Browser“, als sie verschiedene Versionen desselben Browsers nicht als separate Dimensionselemente auflistet.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine interne Tabelle von Adobe. Der Wert basiert auf der HTTP-Kopfzeile `User-Agent` in den Bildanforderungen. Adobe arbeitet mit [DeviceAtlas](https://deviceatlas.com/) zusammen, um Suchen zwischen Benutzeragenten und Browser zu verwalten.

* Bei AppMeasurement-Implementierungen ist diese Dimension vorkonfiguriert.
* Aktivieren Sie für Web SDK-Implementierungen [!UICONTROL Gerätesuche] beim [Konfigurieren eines Datenstroms](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de).

## Dimensionselemente

Zu den Dimensionselementen gehören die Organisationen, die Browser erstellen. Zu den gängigen Dimensionselementen gehören `"Google"` (die Ersteller von [!DNL Chrome]), `"Apple"` (die Ersteller von [!DNL Safari]), `"Microsoft"` (die Ersteller von [!DNL Edge]) und `"Mozilla"` (die Ersteller von [!DNL Firefox]).
