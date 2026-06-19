---
title: Data Warehouse-Segmentkompatibilität
description: Erfahren Sie, welche Segmentdefinitionen in Data Warehouse gültig sind.
feature: Data Warehouse
exl-id: 66b86226-ef4c-4a1a-abe1-3c3accf419e5
TQID: https://experienceleague.adobe.com/7CrArNYD-8ZXVpfO86d1l42ySkTuv8V04PWJFeNWx3s
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2: id: a544b409-2610-410d-a842-474ac1d0d54eid: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: d4db20e3498d54162806b3fdef0b34f45c93a6ff
workflow-type: tm+mt
source-wordcount: 456
ht-degree: 9%

---

# Data Warehouse-Segmentkompatibilität

Nicht alle in Segment Builder erstellten Segmente können in Data Warehouse verwendet werden. Auf dieser Seite erfahren Sie, welche Segmentdefinitionen mit Data Warehouse kompatibel sind, sodass sie bei der Erstellung [ Data Warehouse-Anfrage ausgewählt werden ](/help/export/data-warehouse/create-request/t-dw-create-request.md).

Ein Segment ist nur dann mit Data Warehouse kompatibel **wenn** der folgenden Bedingungen erfüllt sind:

* **Unterstützte Komponenten**: Das Segment verwendet nur Dimensionen und Metriken, die von Data Warehouse unterstützt werden.
* **Unterstützte Struktur**: Die Segmentstruktur folgt den von Data Warehouse erzwungenen Regeln.

Wenn eine der Bedingungen nicht erfüllt ist, wird das Segment beim Erstellen einer Data Warehouse-Anfrage nicht als Option angezeigt und es wird ein Fehler angezeigt, wenn Sie eine Virtual Report Suite auswählen, die ein inkompatibles Segment enthält.

## Unterstützte Komponenten

Da ein Segment anhand derselben Daten ausgewertet wird wie die Anfrage, auf die es angewendet wird **wird (jede Komponente, die in einer Data Warehouse-Anfrage nicht unterstützt wird, wird auch in einem Segment nicht unterstützt.** Eine vollständige Liste der Dimensionen und Metriken, die Data Warehouse nicht unterstützt, finden Sie unter [Komponentenunterstützung in Data Warehouse](component-support.md).

Zusätzlich zu den unter [Komponentenunterstützung](component-support.md) aufgelisteten Dimensionen und Metriken sind in einer Data Warehouse-Anfrage verfügbar ** können **jedoch nicht in einer Segmentdefinition verwendet werden**:

* [[!UICONTROL Tag des Monats]](/help/components/dimensions/day-of-month.md)
* [[!UICONTROL Wochentag]](/help/components/dimensions/day-of-week.md)
* [[!UICONTROL Tag des Jahres]](/help/components/dimensions/day-of-year.md)
* [[!UICONTROL Stunde des Tages]](/help/components/dimensions/hour-of-day.md)
* [[!UICONTROL Marketing-Kanäle]](/help/components/dimensions/marketing-channel.md) (verwenden Sie [[!UICONTROL Letztkontakt-Kanal]](/help/components/dimensions/last-touch-channel.md))
* [[!UICONTROL Monat des Jahres]](/help/components/dimensions/month-of-year.md)
* [[!UICONTROL Seiten nicht gefunden]](/help/components/dimensions/pages-not-found.md) (stattdessen [[!UICONTROL Seitentyp-]](/help/components/dimensions/pages-not-found.md) verwenden)
* [[!UICONTROL Quartal des Jahres]](/help/components/dimensions/quarter-of-year.md)
* [[!UICONTROL Wochentag/Wochenende]](/help/components/dimensions/weekday-weekend.md)

## Unterstützte Struktur

Selbst wenn ein Segment nur unterstützte Komponenten verwendet, muss seine Struktur den von Data Warehouse erzwungenen Regeln entsprechen. Segmentstrukturen werden vollständig, teilweise unterstützt oder nicht unterstützt:

**Unterstützt**:

* **Segmentstapelung**: Eine Data Warehouse-Anfrage kann mehrere Segmente enthalten.
* **Verschachtelte Container**: Unterstützt, vorausgesetzt der Umfang verringert sich auf jeder Ebene (Besucher → Besuch → Treffer). Container, die den Umfang erweitern, werden nicht unterstützt.

**Teilweise unterstützt**:

* **Container ausschließen**: Wird nur auf der obersten Ebene unterstützt. Data Warehouse unterstützt nur Segmente, die als `A AND NOT B` ausgedrückt werden können, d. h. **diese Eigenschaft einschließen** und **diese Eigenschaft ausschließen**. Ausschließen von Containern, die in anderen Containern verschachtelt sind, werden nicht unterstützt.
* **UND/ODER-Logik**: Unterstützt mit Einschränkungen. Bei Verwendung eines `exclusion`- oder `without`-Containers in Kombination mit der UND/ODER-Logik werden nur Segmente unterstützt, die `A AND NOT B` neu geschrieben werden können.

**Nicht unterstützt**:

* **Sequenzielle Segmente**: Segmente, die den THEN-Operator zum Definieren geordneter Navigationssequenzen für Besucher verwenden, werden nicht unterstützt.
* **Operatoren „ist gleich eines von“ und „ist nicht gleich eines von**: Diese Operatoren werden in Data Warehouse-Segmenten nicht unterstützt.

## Segmente, die als Dimensionen verwendet werden

Wenn Sie ein Segment als Dimension in einem Data Warehouse-Bericht verwenden, gibt der Bericht eine Spalte zurück, die `"0"` oder `"1"` enthält:

* **`"0"`**: Das Dimensionselement entsprach nicht den Kriterien des Segments.
* **`"1"`**: Das Dimensionselement entsprach den Kriterien des Segments.
