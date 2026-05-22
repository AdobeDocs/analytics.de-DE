---
description: Informationen zu Sonderzeichen, die im Daten-Feed verwendet werden.
keywords: Daten-Feed;Auftrag;Sonderzeichen;hit_data;Variablen mit mehreren Werten;events_list;products_list;mvvars
subtopic: data feeds
title: Sonderzeichen in Daten-Feeds
feature: Data Feeds
exl-id: b816ebc5-0b23-4420-aa8c-b88953d031e6
TQID: 'https://experienceleague.adobe.com/jNnPgkpVea1R-uUcOiV7UDRc8TdGjhov9yFCvgfitMA'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
subfeature_v2:
  - id: ede9f3ba-4ee4-4497-9d8e-e9da5848bda0
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 333
ht-degree: 90%

---

# Sonderzeichen in Daten-Feeds

Adobe verwendet eine Escape-Logik, um sicherzustellen, dass die an Datenerfassungsserver gesendeten Werte keine Daten-Feed-Dateien beschädigen oder negativ beeinflussen. Diese Zeichen sind von Adobe für folgende Zwecke in `hit_data.tsv` reserviert.

## Sonderzeichen in einer beliebigen Spalte

| Zeichen | Beschreibung |
|--- |--- |
| `\t` | Steht für eine Registerkarte. Markiert das Ende einer Spalte oder eines Datenfelds. |
| `\n` | Steht für einen Zeilenumbruch. Markiert das Ende einer Zeile oder eines Treffers. |
| `\` | Umgekehrter Schrägstrich. Escape-Zeichen, wenn sie im Zuge der Datenerfassung gesendet werden. |

Wenn diesen reservierten Werten ein umgekehrter Schrägstrich vorangestellt wird, wurden sie als Teil der Datenerfassung gesendet.

| Zeichen | Beschreibung |
|--- |--- |
| `\\t` | Der Wert „`\t`“ wurde während der Datenerfassung gesendet und von Adobe mit Escape-Zeichen versehen. |
| `\\n` | Der Wert „`\n`“ wurde während der Datenerfassung gesendet und von Adobe mit Escape-Zeichen versehen. |
| `\\` | Der Wert „`\`“ wurde während der Datenerfassung gesendet und von Adobe mit Escape-Zeichen versehen. |

Ein Besucher Ihrer Site nutzt beispielsweise die interne Suche und sucht nach `"search\nstring"`. Sie füllen eVar1 mit `"search\nstring"` und senden diesen Wert an Adobe. Adobe erhält diesen Treffer und versieht den in der Zeichenfolge enthaltenen Zeilenumbruch mit einem Escape-Zeichen. Der in den Rohdaten tatsächlich platzierte Wert ist `"search\\nstring"`.

## Sonderzeichen in Variablen mit mehreren Werten (events_list, products_list, mvvars)

Die folgenden Zeichen haben in Spalten, die mehrere Werte enthalten können, eine besondere Bedeutung.

| Zeichen | Beschreibung |
|--- |--- |
| `,` | Komma. Kennzeichnet das Ende eines einzelnen Werts. Trennt Produktzeichenfolgen, Ereignis-IDs oder andere Werte. |
| `;` | Semikolon. Kennzeichnet das Ende eines einzelnen Werts in `product_list`. Trennt Felder innerhalb einer einzelnen Produktzeichenfolge. |
| `=` | Gleich-Zeichen. Weist einem Ereignis in `product_list` einen Wert zu. |
| `^` | Caret. Escape-Zeichen, wenn sie im Zuge der Datenerfassung gesendet werden. |

Wenn diesen reservierten Werten ein Caret vorangeht, wurden sie im Zuge der Datenerfassung gesendet.

| Zeichen | Beschreibung |
|--- |--- |
| `^,` | Der Wert „`,`“ wurde während der Datenerfassung gesendet und von Adobe mit Escape-Zeichen versehen. |
| `^;` | Der Wert „`;`“ wurde während der Datenerfassung gesendet und von Adobe mit Escape-Zeichen versehen. |
| `^=` | Der Wert „`=`“ wurde während der Datenerfassung gesendet und von Adobe mit Escape-Zeichen versehen. |
| `^^` | Der Wert „`^`“ wurde während der Datenerfassung gesendet und von Adobe mit Escape-Zeichen versehen. |
