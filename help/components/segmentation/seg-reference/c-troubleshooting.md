---
description: Erfahren Sie, wie Sie Probleme im Zusammenhang mit Segmenten beheben.
title: Fehlerbehebung
feature: Segmentation
exl-id: ca51110e-1ba7-4182-b5b2-baf9b0c017af
TQID: https://experienceleague.adobe.com/-9XPy2cFezGBFnygKW4gbHG2zuNBfn5Z29InEDF58ZM
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 181
ht-degree: 6%

---

# Fehlerbehebung

In diesem Artikel werden einige häufige Probleme mit Segmenten und deren Behebung aufgeführt.

<!--
Looks like this is not part anymore of the current UI.

## Error: "Incompatible elements in this segment" {#incompatible}

This error occurs when you try to save a segment in the Data Warehouse folder where the segment contains elements not compatible with Data Warehouse. To resolve this error, do one of two things:

* Save the segment in a different folder 
* Remove or change the incompatible portions of the segment.
-->

## Warum gibt mein Segment überhaupt keine Daten zurück? {#no-data}

Mögliche Gründe:

* Umgekehrte Verschachtelung - z. B. Verschachteln eines ![User](/help/assets/icons/User.svg)**[!UICONTROL Visitor]**-Containers unter einem ![Visit](/help/assets/icons/Visit.svg) **[!UICONTROL Visit]**-Container.
* Der Bericht unterstützt keine Segmentierung.
* Es gibt keine Daten, die den Segmentierungskriterien entsprechen.

## Warum kann ich das Segment, das ich erstellt habe, nicht im Segment-Manager sehen? {#invisible}

Mögliche Gründe:

* Einige Dimensionen sind nur in Data Warehouse und nicht im Segment-Manager verfügbar.
* Das Segment wird nur für eine bestimmte Report Suite überprüft.
* Ein freigegebenes Segment wurde möglicherweise von einem anderen Benutzer gelöscht.
* Segmente konnten aufgrund eines Problems mit dem Rechenzentrum oder dem Browser-Cache nicht geladen werden.
* Das Segment wurde nicht gespeichert.
* Die IP-Adresse kann auf Benutzerseite blockiert werden.

## Warum sind die Daten, die nach der Anwendung eines Segments angezeigt werden, falsch? {#page-data}

Mögliche Gründe:

* Regeln oder Operatoren sind für das erforderliche Ergebnis falsch.
* Falsche Verwendung von Containern im Segment.
* Traffic-Variablen, die zum Segmentieren verwendet werden, sind nicht ordnungsgemäß festgelegt oder abgelaufen.
