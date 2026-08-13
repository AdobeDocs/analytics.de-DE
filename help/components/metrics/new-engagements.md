---
title: Neue Interaktionen
description: Die Häufigkeit, mit der ein Erstkontakt-Kanal eingestellt wird.
feature: Metrics
exl-id: a419d048-9715-4d7b-9c24-d34129755371
TQID: https://experienceleague.adobe.com/UsPu31wUqpoDYQy5aT9wnzSUgJ6i9mHVZ8pAtFQgzGo
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 148
ht-degree: 83%

---

# Neue Interaktionen

Die „Metrik [&#x200B; Interaktionen“ &#x200B;](overview.md) an, wie oft eine Besucherin oder ein Besucher zum ersten Mal in ihrem bzw. seinem Interaktionszeitraum mit einem Marketing-Kanal übereinstimmt. Diese Metrik ist nützlich, wenn Sie eine beliebige Dimension mit einem Besucher vergleichen möchten, der zum ersten Mal mit einer Verarbeitungsregel für einen Marketing-Kanal übereinstimmt.

## Berechnung dieser Metrik

Während der Datenverarbeitung durchläuft jeder Treffer die [Verarbeitungsregeln für Marketing-Kanäle](/help/admin/tools/manage-rs/edit-settings/marketing-channels/mc-proc-rules.md). Wenn ein Treffer mit einer Marketing-Kanal-Verarbeitungsregel übereinstimmt und der Besucher noch keinen Erstkontakt-Kanal hat, handelt es sich bei dem Treffer um eine neue Interaktion. Wenn ein Treffer nicht mit den Verarbeitungsregeln für Marketing-Kanäle übereinstimmt oder wenn der Besucher bereits über einen Erstkontakt-Kanal verfügt, handelt es sich bei dem Treffer nicht um eine neue Interaktion.

Besucher können über mehr als eine neue Interaktion verfügen, wenn sie ihre Interaktionszeit ablaufen lassen.
