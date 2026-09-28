---
title: Identifizierter Status
description: Eine Markierung, die die Erkennung für das Zusammenfügen bestimmt.
feature: Dimensions
exl-id: 8c6e9003-96f8-460f-a490-203f67be6337
TQID: 'https://experienceleague.adobe.com/JUBtgXBDboIgX0xbvuflF5q-oEwqHx4vKvJd0Y5XMLY'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
    internal-label: Data configuration and collection
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
  - id: b22bc0f7-b089-4966-95a1-31e7b3b69b79
    internal-label: Dimensions
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: 9a50beeb0aa51cf9f4baf212566947c14029ce8e
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 46%
---
# Identifizierter Status

Der „Identifizierte Status[ (Dimension](overview.md) ist spezifisch für [geräteübergreifende Analyse](../cda/overview.md) Virtual Report Suites. Mit dieser Dimension wird angegeben, ob Treffer zum Zeitpunkt der Berichterstellung vom System identifiziert (zugeordnet) wurden oder nicht. Diese Dimension ist hilfreich, um zu verstehen, wie gut CDA Daten zusammenfügt oder „komprimiert“.

## Füllen dieser Dimension mit Daten

Diese Dimension wird von [Cross-Device Analytics](../cda/overview.md) zum Zeitpunkt der Ausführung eines Berichts berechnet, basierend darauf, ob jeder Treffer einer Person zugeordnet wurde. Sofern die geräteübergreifende Analyse für eine Virtual Report Suite konfiguriert ist, ist sie vorkonfiguriert, d. h. es gibt keine Variable zum Festlegen.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (berechnet durch geräteübergreifende Analyse) |
| **Feld Web SDK/XDM** | Keine (berechnet durch geräteübergreifende Analyse) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | nicht angegeben |

## Dimensionselemente

Zu den Dimensionselementen gehören `"Identified"` und `"Unidentified"`.

* **`"Identified"`**: Der Treffer wird einer Person zugeordnet.
* **`"Unidentified"`**: Der Treffer wird keiner Person zugeordnet und konnte mit keiner Attributionsmethode zugeordnet werden.
