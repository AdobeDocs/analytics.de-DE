---
title: Letztkontakt-Kanaldetail
description: Details zum neuesten Marketing-Kanal innerhalb des Interaktionsablaufs des Besuchers.
feature: Dimensions
exl-id: def03267-f3e5-4772-a707-5678c45eba6d
source-git-commit: e934de3938f013067d6bbd6b516b0444b0c9f782
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 80%

---

# Letztkontakt-Kanaldetail

Die Dimension „Detail des Letztkontaktkanals[&#x200B; zeigt Details zum &#x200B;](overview.md) Marketing-Kanal an, dem ein Besucher während des Interaktionszeitraums dieses Besuchers entspricht (standardmäßig 30 Tage). Diese Dimension ist nützlich, um zu verstehen, was dazu beigetragen hat, dass der Treffer einem Marketing-Kanal entsprach. Wenn beispielsweise ein Besucher zu Ihrer Site gelangt ist und mit dem Marketing-Kanal „Paid Search“ übereinstimmt, können Sie anhand des Kanaldetails sehen, welche Suchmaschine verwendet wurde oder nach welchem Schlüsselwort er gesucht hat.

## Füllen dieser Dimension mit Daten

Diese Dimension kopiert Werte aus anderen Variablen. Die verwendete Variable referenziert den Kanalwert in jeder [Marketing-Kanalverarbeitungsregel](/help/admin/tools/manage-rs/edit-settings/marketing-channels/mc-proc-rules.md). Wenn ein Treffer mit einer Marketing-Kanalverarbeitungsregel übereinstimmt, wird die Dimension [Letztkontakt-Kanal](last-touch-channel.md) auf den Kanalnamen festgelegt und diese Dimension auf den in der Regel festgelegten Kanalwert gesetzt.

Führen Sie die folgenden Schritte aus, um diese Dimension auf einen bestimmten Wert zu setzen:

* Achten Sie darauf, dass sich das gewünschte Dimensionselement in einem Trefferattribut oder einer benutzerdefinierten Variable befindet.
* Legen Sie eine Marketing-Kanalverarbeitungsregel fest, die die gewünschten Kriterien für den Treffer enthält.
* Wählen Sie in der Marketing-Kanal[!UICONTROL Verarbeitungsregel den gewünschten Dropdown-Wert unter &#x200B;]Kanalwert festlegen) aus.
* Der Treffer des Besuchers auf Ihrer Site muss den Kriterien entsprechen, die in der Marketing-Kanalverarbeitungsregel beschrieben sind.

## Dimensionselemente

Dimension-Elemente hängen vom Kanalwert ab, der in der Dropdown-Liste für die entsprechende Marketing-Kanal-Verarbeitungsregel aufgeführt ist. Wenn Sie beispielsweise den Wert des Kanals auf „Seiten-URL“ setzen, umfassen die Dimensionselemente die Seiten-URLs auf Ihrer Site. Wenn Sie den Wert des Kanals auf „Referrer-Domäne“ setzen, umfassen die Dimensionselemente die Domänen, auf die Besucher geklickt haben, um zu Ihrer Site zu gelangen. Diese Dimension aggregiert alle Detaildimensionselemente, unabhängig davon, auf welchem Kanal sie sich befinden.

Adobe empfiehlt, Kanalwerte für den Marketing-Kanal festzulegen, um Einblick in die Kanaldetails zu erhalten.
