---
description: Verwenden Sie Unterklassifizierungen mit dem Classification Rule Builder.
title: Unterklassifizierungen und der Regel-Builder
feature: Classifications
exl-id: 745d6149-bcb1-48ad-abbe-63a9d009fa27
TQID: https://experienceleague.adobe.com/Qlqt3scXHVUv6EODq57zzaF2007Vvf5x324CHjrsNE0
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 403
ht-degree: 44%

---

# Unterklassifizierungen und der Regel-Builder (veraltet)

{{classification-rulebuilder-deprecation}}

Sie können den Classification Rule Builder mit Unterklassifizierungen kombinieren, wenn Sie sicherstellen, dass jede Unterklassifizierung über einen übergeordneten Wert verfügt.

Die Kombination von Classification Rule Builder mit Unterklassifizierungen kann die Verwaltung von Klassifizierungen vereinfachen und die Anzahl der erforderlichen Regeln reduzieren. Dies empfiehlt sich zum Beispiel, wenn Ihr Trackingcode aus Codes besteht, die Sie einzeln klassifizieren möchten.

Grundlegende Informationen zu Unterklassifizierungen finden Sie unter [Unterklassifizierungen](/help/components/classifications/importer/subclassifications.md).

## Beispiel

Nehmen Sie als Beispiel den folgenden Trackingcode an:

`channel:broad_campaign:creative`

Mit einer Classification-Hierarchie können Sie eine Classification auf eine andere Classification (*`sub-classification`*) anwenden. Das bedeutet, dass Sie das Import-Tool wie eine relationale Datenbank mit mehreren Tabellen verwenden können. Eine Tabelle ordnet den Schlüsseln vollständige Trackingcodes zu und eine andere ordnet diese Schlüssel anderen Tabellen zu.

![](assets/sub_class_table.png)

Sobald Sie diese Struktur eingerichtet haben, können Sie den [Classifications Rule Builder) verwenden](/help/components/classifications/crb/classification-rule-builder.md) um kleine Dateien hochzuladen, die nur die Suchtabellen (die grünen und roten Tabellen im vorherigen Bild) aktualisieren. Anschließend können Sie den Regel-Builder verwenden, um die Hauptklassifizierungstabelle auf dem neuesten Stand zu halten.

Die folgende Aufgabe beschreibt, wie Sie dies erreichen.

## Einrichten von Unterklassifizierungen mit dem Regel-Builder

Beispielschritte, die beschreiben, wie Sie Unterklassifizierungen mit dem Regel-Builder hochladen können.

1. Erstellen Sie Klassifizierungen und Unterklassifizierungen im Classification Manager.

   Beispiel:

   ![Schritt-Info](/help/admin/tools/assets/sub_class_create.png)

1. Klassifizieren [ im Classifications](/help/components/classifications/crb/classification-rule-builder.md)Regel-Builder den Unterklassifizierungsschlüssel aus dem ursprünglichen Trackingcode.

   Verwenden Sie dazu einen regulären Ausdruck. In diesem Beispiel würde die Regel zum Ausfüllen von *`Broad Campaign code`* diesen regulären Ausdruck verwenden:

   | `#` | Regeltyp | Übereinstimmung | Classification auswählen | Hierzu |
   |---|---|---|---|---|
   |   | Regulärer Ausdruck | `[^\:]:([^\:]):([^\:])` | Code einer breiten Kampagne | `$1` |
   |   | Regulärer Ausdruck | `[^\:]:([^\:]):([^\:])` | Kreativer Code | `$2` |

   >[!NOTE]
   >
   >An dieser Stelle füllen Sie nicht die Unterklassifizierungen *`Campaign Type`* und *`Campaign Director`*.

1. Laden Sie eine Classification-Datei hoch, die ausschließlich die angegebenen Unter-Classifications enthält.

   Weitere Informationen finden Sie unter [Mehrstufige Klassifizierungen](/help/components/classifications/importer/subclassifications.md).

   Beispiel:

   | Schlüssel | Kanal | Code einer breiten Kampagne | Umfassender Kampagnen-Code&amp;Hat;Kampagnentyp | Umfassender Kampagnen-Code&amp;Hat;Kampagnen-Director | ... |
   |---|---|---|---|---|---|
   | &#42; |  | 111 | Marke | Suzanne |  |
   | &#42; |  | 222 | Marke | freimütig |  |

1. Laden Sie eine kleine Datei (siehe oben) hoch, um die Suchtabellen zu pflegen.

   Zum Beispiel würden Sie eine solche Datei hochladen, wenn ein neuer *`Broad Campaign code`* eingeführt wird. Diese Datei würde dann für bereits klassifizierte Werte gelten. Wenn Sie eine neue Unterklassifizierung erstellen (z. B. *`Creative Theme`* als Unterklassifizierung von *`Creative code`*), laden Sie nur die Unterklassifizierungsdatei und nicht die gesamte Klassifizierungsdatei hoch.

   Für die Berichterstellung funktionieren diese Unterklassifizierungen genau wie Klassifizierungen der obersten Ebene. Dies verringert den Verwaltungsaufwand für ihre Verwendung.
