---
description: Mit Segment Builder können Sie Werte mithilfe ausgewählter Operatoren vergleichen und beschränken.
title: Vergleichsoperatoren für Segmente
feature: Segmentation
exl-id: 1ec1ff05-03a9-4151-8fcb-a72ebbce87dd
source-git-commit: 80e4a3ba4a5985563fcf02acf06997b4592261e4
workflow-type: tm+mt
source-wordcount: '1193'
ht-degree: 47%

---

# Vergleichsoperatoren für Segmente

Mit Segment Builder können Sie Werte mithilfe ausgewählter Operatoren vergleichen und beschränken. Es gibt drei Kategorien von Operatoren: Standard, Data Warehouse und Distinct Count.

Je nach ausgewähltem Operator:

* Sie können einen Wert eingeben
* Sie können einen Teil eines Werts eingeben und aus einem Dropdown-Menü auswählen (falls verfügbar).
* Wählen Sie sofort einen Wert aus dem Dropdown-Menü aus (falls verfügbar).

Wenn Sie einen Wert für einen Operator eingeben, der verfügbare Werte überprüft, z **[!UICONTROL B. &quot;]**&quot;, und der Wert nicht mit den für die Komponente verfügbaren Werten übereinstimmt, wird ein ![AlertRed](/help/assets/icons/AlertRed.svg)-Symbol angezeigt. Sie können entweder einen Wert aus dem Dropdown-Menü auswählen oder die Eingabetaste **[!UICONTROL _,_]** den Wert einzugeben.

![Segment ist gleich](assets/segment-operator-equals.png)

## Platzhalter

Das einzige unterstützte Platzhalterzeichen für Benutzer, die Platzhalter unterstützen, ist das Sternchen: `*`. Wenn Sie nach dem spezifischen &#42; suchen müssen, können Sie es mit einem umgekehrten Schrägstrich (z. B. `\*`) maskieren.

Beispiel: Sie haben einen Seitennamen mit dem Namen *Mein cooles Produkt*.

* Die Segmentregel **[!UICONTROL Seitenname]** **[!UICONTROL stimmt überein]** `* product` entspricht dem obigen Seitennamen.
* Die Regel **[!UICONTROL Seitenname]** **[!UICONTROL stimmt überein]** `My \* product` entspricht jedoch nur dem Seitennamen *Mein * Produkt*.

## Standardoperatoren

| Operator | Die ausgewählte Dimension, das ausgewählte Segment oder metrische Ereignis... |
|--- |--- |
| **[!UICONTROL gleich]** | Gibt Elemente mit einer exakten Entsprechung für numerische oder Zeichenfolgenwerte wieder. Hinweis: Wenn Sie Platzhalterzeichen verwenden, verwenden Sie den Operator **[!UICONTROL stimmt überein]**. |
| **[!UICONTROL nicht gleich]** | Gibt alle Elemente zurück, die keine exakte Übereinstimmung mit dem eingegebenen Wert enthalten.  Hinweis: Wenn Sie Platzhalterzeichen verwenden, verwenden Sie den Operator **[!UICONTROL stimmt nicht überein]**. |
| **[!UICONTROL Entspricht einem von]** | Gibt Elemente zurück, die exakt mit einem beliebigen Wert im Eingabefeld übereinstimmen (bis zu 500 Elemente). Wenn Sie beispielsweise `Search Results, Homepage` für die Dimension **[!UICONTROL Seitenname]** mit diesem Operator eingeben, stimmen *Suchergebnisse* und *Homepage* und zählen als zwei Elemente. Das Eingabefeld für diesen Operator ist kommagetrennt. |
| **[!UICONTROL Entspricht keinem von]** | Identifiziert Elemente, die exakt mit einem beliebigen Wert im Eingabefeld übereinstimmen, (bis zu 500 Elemente) und gibt dann nur Elemente ohne diese Werte zurück. Wenn Sie beispielsweise `Search Results, Homepage` mit diesem Operator für die Dimension **[!UICONTROL Seitenname]** eingeben, werden *Suchergebnisse* und *Homepage* identifiziert und dann **ausgeschlossen** aus den zurückgegebenen Elementen. Dieses Beispiel würde als 2 Elemente zählen. Das Eingabefeld für diesen Operator ist kommagetrennt. |
| **[!UICONTROL enthält]** | Gibt Elemente zurück, die mit den Unterzeichenfolgen der eingegebenen Werte vergleichbar sind. Wenn die Regel beispielsweise **[!UICONTROL Seitenname]** **[!UICONTROL enthält]** `Search` lautet, stimmt diese Regel mit allen Seiten überein, die die `Search` der Unterzeichenfolge enthalten, einschließlich *Suchergebnisse*, *Suche* und *Suchen*. Bei der Klausel „Enthält“ wird in Adobe Analytics nicht zwischen Groß- und Kleinschreibung unterschieden, in Customer Journey Analytics wird jedoch zwischen Groß- und Kleinschreibung unterschieden. |
| **[!UICONTROL enthält nicht]** | Gibt die Umkehrung der Regel **[!UICONTROL contains]** zurück. Insbesondere werden alle Elemente, die mit dem eingegebenen Wert übereinstimmen, aus den eingegebenen Werten ausgeschlossen. Wenn die Regel beispielsweise **[!UICONTROL Seitenname]** **[!UICONTROL Enthält nicht]** `Search` lautet, stimmt sie mit keiner Seite überein, die die `Search` der Unterzeichenfolge enthält, einschließlich *Suchergebnisse*, *Suche* und *Suchen*. Diese Werte werden aus den Ergebnissen ausgeschlossen. |
| **[!UICONTROL enthält alle von]** | Gibt Elemente zurück, die mit den Unterzeichenfolgen vergleichbar sind, einschließlich mehrerer miteinander verbundener Werte. Wenn Sie beispielsweise `Search Results` mit diesem Operator für die Dimension **[!UICONTROL Seitenname]** eingeben, stimmen *Suchergebnisse* und *Suchergebnisse* überein, jedoch nicht *Suche* oder *Ergebnisse*. Die Regel würde mit *Suche* UND *Ergebnisse* übereinstimmen. Das Eingabefeld für diesen Operator ist durch Leerzeichen getrennt (100 Wörter). |
| **[!UICONTROL enthält nicht alle von]** | Identifiziert Elemente im Vergleich zu Unterzeichenfolgen, einschließlich mehrerer miteinander verbundener Werte, und gibt dann nur Elemente ohne diese Werte zurück. Wenn Sie beispielsweise `Search Results` mit diesem Operator für die Dimension **[!UICONTROL Seitenname]** eingeben, werden *Suchergebnisse* und *Suchergebnisse* (aber nicht *Suche* oder *Ergebnisse* einzeln) identifiziert und diese Elemente ausgeschlossen. Das Eingabefeld für diesen Operator ist durch Leerzeichen getrennt (100 Wörter). |
| **[!UICONTROL enthält beliebige von]** | Gibt Elemente zurück, die mit den Unterzeichenfolgen vergleichbar sind, einschließlich mehrerer miteinander verbundener oder unabhängig erkannter Werte. Wenn Sie beispielsweise `Search Results` mit diesem Operator eingeben, stimmen *Suchergebnisse*, *Suchergebnisse*, *Suche* und *Ergebnisse*. Entweder würde er mit *Suche* ODER *Ergebnisse* übereinstimmen, die zusammen oder unabhängig gefunden wurden. Das Eingabefeld für diesen Operator ist durch Leerzeichen getrennt (100 Wörter). |
| **[!UICONTROL enthält keinen von]** | Ermittelt Elemente basierend auf Unterzeichenfolgen und gibt Werte zurück, die diese Zeichenfolgen nicht enthalten. Kann mehrfache zusammengefasste Werte oder unabhängig ermittelte Werte umfassen. Wenn Sie beispielsweise `Search Results` für die Dimension **[!UICONTROL Seitenname]** eingeben, stimmen *Suchergebnisse*, *Suchergebnisse von**, *Suche* und *Ergebnisse* überein, wobei entweder *Suche* oder *Ergebnis* gemeinsam oder unabhängig voneinander gefunden werden. Anschließend würden die Elemente ausgenommen, die diese Unterzeichenfolgen enthalten. Das Eingabefeld für diesen Operator ist durch Leerzeichen getrennt (100 Wörter). |
| **[!UICONTROL beginnt mit]** | Gibt Elemente zurück, die mit dem eingegebenen Zeichenfolgenwert beginnen. |
| **[!UICONTROL beginnt nicht mit]** | Gibt alle Elemente zurück, die nicht mit dem eingegebenen Zeichenfolgenwert beginnen. Dies ist das Gegenteil des Operators **[!UICONTROL Beginnt mit]**. |
| **[!UICONTROL endet mit]** | Gibt Elemente zurück, die mit eingegebenem Zeichenfolgenwert enden. |
| **[!UICONTROL endet nicht mit]** | Gibt alle Elemente zurück, die nicht mit dem eingegebenen Zeichenfolgenwert enden. Dies ist das Gegenteil des Operators **[!UICONTROL Endet mit]**. |
| **[!UICONTROL stimmt überein mit]** | Gibt Elemente mit einer exakten Entsprechung für gegebene numerische oder Zeichenfolgenwerte wieder. Bei **[!UICONTROL matches]**-Klausel wird in Adobe Analytics und in Customer Journey Analytics zwischen Groß- und Kleinschreibung unterschieden. **Hinweis**: Verwenden Sie diesen Operator bei der Verwendung von [Platzhalterfunktionen](#wildcards) (Globbing). Beispiele für „Globbing“:<ul><li>`a*e` würde übereinstimmen mit `ae`, `abcde`, `adobe` und `a whole sentence`</li><li>`adob*` würde übereinstimmen mit `adobe`, `adobe analytics` und `adobo recipe`</li><li>`*dobe` würde übereinstimmen mit `dobe`, `adobe` und `cute little dobe`</li></ul> |
| **[!UICONTROL stimmt nicht überein mit]** | Gibt alle Elemente zurück, die keine exakte Übereinstimmung mit dem eingegebenen Wert enthalten. Hinweis: Verwenden Sie diesen Operator bei der Verwendung [Platzhalter](#wildcards)-Funktionen (Globbing). |
| **[!UICONTROL vorhanden]** | Gibt die Anzahl der vorhandenen Elemente zurück. Wenn Sie beispielsweise die Dimension **[!UICONTROL Seiten nicht gefunden]** mit dem Operator **[!UICONTROL vorhanden]** auswerten, wird die Anzahl der vorhandenen Fehlerseiten zurückgegeben. |
| **[!UICONTROL nicht vorhanden]** | Gibt alle nicht vorhandenen Elemente zurück. Wenn Sie beispielsweise die Dimension **[!UICONTROL Seiten nicht gefunden]** mit dem Operator **[!UICONTROL Nicht vorhanden]** auswerten, wird die Anzahl der Seiten zurückgegeben, auf denen diese Fehlerseite nicht vorhanden war. |

## Data Warehouse-Operatoren

| Operator | Die ausgewählte Dimension, das ausgewählte Segment oder metrische Ereignis... |
| --- | --- |
| **[!UICONTROL kleiner als]** | Gibt Elemente zurück, deren numerische Anzahl kleiner als der eingegebene Wert ist. |
| **[!UICONTROL kleiner als oder gleich]** | Gibt Elemente zurück, deren numerische Anzahl kleiner als der eingegebene Wert ist oder damit übereinstimmt. |
| **[!UICONTROL größer als]** | Gibt Elemente zurück, deren numerische Anzahl größer als der eingegebene Wert ist. |
| **[!UICONTROL größer als oder gleich]** | Gibt Elemente zurück, deren numerische Anzahl größer als der eingegebene Wert ist oder damit übereinstimmt. |

## Distinct Count-Operatoren

Sie können nach einer bestimmten Anzahl von Elementen innerhalb einer Dimension segmentieren. Beispiele: *Besucher, die mehr als 5 verschiedene Produkte angesehen haben* oder *Besuche, bei denen mehr als 5 verschiedene Seiten angezeigt wurden*.

| Operator | Die ausgewählte Dimension, das ausgewählte Segment oder metrische Ereignis... |
| --- | --- |
| **[!UICONTROL gleich]** | Gibt Dimensionselemente zurück, deren eindeutige Anzahl dem eingegebenen Wert entspricht. |
| **[!UICONTROL nicht gleich]** | Gibt Dimensionselemente zurück, deren eindeutige Anzahl nicht dem eingegebenen Wert entspricht. |
| **[!UICONTROL größer als]** | Gibt Dimensionselemente zurück, deren eindeutige Anzahl größer als der eingegebene Wert ist. |
| **[!UICONTROL kleiner als]** | Gibt Dimensionselemente zurück, deren eindeutige Anzahl kleiner als der eingegebene Wert ist. |
| **[!UICONTROL größer als oder gleich]** | Gibt Dimensionselemente zurück, deren eindeutige Anzahl größer als der eingegebene Wert ist oder damit übereinstimmt. |
| **[!UICONTROL kleiner als oder gleich]** | Gibt Dimensionselemente zurück, deren eindeutige Anzahl kleiner als der eingegebene Wert ist oder damit übereinstimmt. |


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Distinct Dimension Counts](https://video.tv.adobe.com/v/27257?quality=12&learn=on){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]
