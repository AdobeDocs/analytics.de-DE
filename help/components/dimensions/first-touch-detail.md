---
title: Erstkontakt-Kanaldetail
description: Details zum ersten Marketing-Kanal innerhalb des Interaktionsablaufs des Besuchers.
feature: Dimensions
exl-id: a155182d-7bc0-4c7d-9de7-680bfe2d6432
source-git-commit: 78cfb1f3c4d45fc983982a8da11b66f2b2c9ecbc
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 90%

---

# Erstkontakt-Kanaldetail

Die Dimension „Erstkontakt-Kanaldetail“ enthält Details zum ersten Marketing-Kanal, mit dem ein Besucher während der Interaktionszeit des Besuchers (standardmäßig 30 Tage) übereinstimmt. Diese Dimension ist nützlich, um zu verstehen, was dazu beigetragen hat, dass der Treffer einem Marketing-Kanal entsprach. Wenn beispielsweise ein Besucher zu Ihrer Site gelangt ist und mit dem Marketing-Kanal „Paid Search“ übereinstimmt, können Sie anhand des Kanaldetails sehen, welche Suchmaschine verwendet wurde oder nach welchem Schlüsselwort er gesucht hat.

## Füllen dieser Dimension mit Daten

Diese Dimension kopiert Werte aus anderen Variablen. Die verwendete Variable referenziert den Kanalwert in jeder [Marketing-Kanalverarbeitungsregel](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md). Wenn ein Treffer mit einer Marketing-Kanalverarbeitungsregel übereinstimmt, wird die Dimension [Letztkontakt-Kanal](last-touch-channel.md) auf den Kanalnamen festgelegt und diese Dimension auf den in der Regel festgelegten Kanalwert gesetzt.

Führen Sie die folgenden Schritte aus, um diese Dimension auf einen bestimmten Wert zu setzen:

* Achten Sie darauf, dass sich das gewünschte Dimensionselement in einem Trefferattribut oder einer benutzerdefinierten Variable befindet.
* Legen Sie eine Marketing-Kanalverarbeitungsregel fest, die die gewünschten Kriterien für den Treffer enthält.
* Wählen Sie den gewünschten Dropdown-Wert unter [!UICONTROL Kanalwert festlegen] innerhalb der Marketing-Kanal-Verarbeitungsregel.
* Der Treffer des Besuchers auf Ihrer Site muss den Kriterien entsprechen, die in der Marketing-Kanalverarbeitungsregel beschrieben sind, _und_ der erste Marketing-Kanalwert sein, auf den dies im Interaktionszeitraum des Besuchers zutrifft.

Wenn ein nachfolgender Treffer Kriterien unter einem anderen Marketing-Kanal erfüllt, wird diese Dimension nicht mit dem neuen Marketing-Kanal überschrieben.

## Dimensionselemente

Die Elemente der Dimension hängen vom Kanalwert ab, der in der Dropdownliste für die entsprechende Marketing-Kanalverarbeitungsregel aufgeführt ist. Wenn Sie beispielsweise den Wert des Kanals auf „Seiten-URL“ setzen, umfassen die Dimensionselemente die Seiten-URLs auf Ihrer Site. Wenn Sie den Wert des Kanals auf „Referrer-Domäne“ setzen, umfassen die Dimensionselemente die Domänen, auf die Besucher geklickt haben, um zu Ihrer Site zu gelangen. Diese Dimension aggregiert alle Detaildimensionselemente, unabhängig davon, auf welchem Kanal sie sich befinden.

Adobe empfiehlt, Kanalwerte für den Marketing-Kanal festzulegen, um Einblick in die Kanaldetails zu erhalten.
