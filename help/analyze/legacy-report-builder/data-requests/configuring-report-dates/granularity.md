---
description: 'Im Dialogfeld „Anforderungs-Assistent: Schritt 1“ können Sie angeben, welche Granularität eine Datenanforderung haben soll. Granularität gibt den Grad der zeitbasierten Details an, die im Bericht enthalten sind.'
title: Granularität
uuid: 948b3ff2-fcff-45fc-9e8c-8a025ac562b1
feature: Report Builder
role: User, Admin
exl-id: 96c3b93a-9adf-4993-b6fc-9146ee5be4bd
TQID: https://experienceleague.adobe.com/26j4Fernl4bfuYeyuVVzw1K5hZvNSD6pDUVOfEc0J8s
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 14%

---

# Granularität

{{legacy-arb}}

Im Anforderungs-Assistenten: Schritt 1: Sie können auf die Datenanforderung eine Granularitätsstufe anwenden. Granularität gibt den Grad der zeitbasierten Details an, die im Bericht enthalten sind.

Gültige Werte sind Stunde, Tag, Woche, Monat, Quartal, Jahr und aggregiert.

## Verarbeitung von Granularität in Report Builder

Angenommen, Sie wählen einen Datumsbereich für einen Monat mit [!UICONTROL Monat] Granularität. Anfragen zeigen Gesamtwerte für die Metrik basierend auf den Daten eines Monats an. Wenn der Datumsbereich Ihrer Anfrage sich über ein Quartal erstreckt, zeigt der Bericht drei Zahlen an: eine für jede Monatseinheit oder einen Bruchteil davon. Wenn heute der 18. März ist, gibt die Auswahl des letzten Quartals eine Zahl für den 1. Januar bis zum 31. Januar zurück, eine weitere Zahl für den 1. Februar bis zum 28. Februar und eine endgültige Zahl für den 1. März bis zum 17. März.
