---
description: Ansicht der obersten Werte einer Dimension, bevor sie in einem Projekt verwendet wird.
title: Dimensionsvorschau
feature: Dimensions
role: User, Admin
exl-id: 897edc76-6744-4d8c-ab0e-20672838f7b3
source-git-commit: 9f040971d1198fe7774bc04f6c42cc4e2145b197
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 90%

---

# Dimensionsvorschau

Bewegen Sie den Cursor über das Informations-Symbol neben einer Dimension, um die obersten fünf Werte für nicht zeitabhängige Dimensionen (und 15 für zeitabhängige Dimensionen) anzuzeigen. Bisher waren diese Werte statisch (d. h. die fünf ausgewählten Werte blieben unverändert).

![](assets/dimension-preview.png)

Jetzt zeigen wir standardmäßig dynamische Werte anstelle von statischen an, mit der Option, diese in statische Werte umzuwandeln. Wissenswertes:

* Bei einer Aktualisierung Ihrer Daten werden die Spalten der dynamischen Dimension aktualisiert, um die aktuellen 5/15 Dimensionselemente anzuzeigen.
* Eine dynamische Dimensionsspalte, die kopiert oder bewegt wird, wird statisch.
* Wenn Sie mit dem Mauszeiger über eine statische Dimensionsspalte fahren, wird ein Schlosssymbol angezeigt, das angibt, dass es sich bei der Dimension um eine statische handelt.

![](assets/dimension_static.png)

## Anzeige von Dimensionselementen

Wenn Sie auf eine Dimension zeigen und auf den grauen, nach rechts zeigenden Pfeil daneben klicken, wird eine Liste der jeweiligen Dimensionselemente angezeigt. Dimensionselementlisten zeigen normalerweise die Top-Elemente der letzten 30 Tage an.

Wenn Sie nach unten zum unteren Rand der Liste scrollen, sehen Sie **[!UICONTROL Top-Elemente aus den letzten 18 Monaten anzeigen]**. Klicken Sie auf diese Option, um die Top-Dimensionselemente der letzten 547 Tage anzuzeigen.
