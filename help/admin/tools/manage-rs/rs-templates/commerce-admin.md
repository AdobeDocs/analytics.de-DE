---
description: Definiert allgemeine Einstellungen für eine E-Commerce-Website.
title: Handel
feature: Report Suite Settings
exl-id: 90e5d446-10b8-4d40-8bd0-8b13e1c2f603
TQID: https://experienceleague.adobe.com/l1-8tv-5dvKi4rx9-2tRoN4hK9ROr-ajWgKm0uFggrI
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
subfeature_v2: id: fab61dd8-112a-4e5e-ad5f-fb0240b7a60b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 188
ht-degree: 58%

---

# Handel

Definiert allgemeine Einstellungen für eine E-Commerce-Website.

| Konversionsvariablen | Typ | Subrelationen | Zuordnung | Gültigkeit | `s_code`-Variable |
|---|---|---|---|---|---|
| Interne Promotions | Zeichenfolge | Einfach | Zuletzt verwendet (Letzter) | Besuch | `evar1` |
| Interne Suchbegriff | Zeichenfolge | Einfach | Zuletzt verwendet (Letzter) | Besuch | `evar2` |
| Merchandising-Kategorie | Zeichenfolge | Einfach | Zuletzt verwendet (Letzter) | Besuch | `evar3` |
| Commerce-Variable 4 | Zeichenfolge | Einfach | Zuletzt verwendet (Letzter) | Besuch | `evar4` |
| Commerce-Variable 5 | Zeichenfolge | Einfach | Zuletzt verwendet (Letzter) | Besuch | `evar5` |

| Erfolgsereignisse | Typ | `s_code`-Variable |
|---|---|---|
| Registrierungen | Zähler (keine untergeordneten Beziehungen) | `event1` |
| Benutzerspezifische Ereignisse 1-5 | Zähler (keine untergeordneten Beziehungen) | `event1, event2, event3, event4, event5` |

| Benutzerdefinierte Insight-Variablen | `s_code`-Variable |
|---|---|
| Traffic-Eigenschaft 1-5 | `prop1, prop2, prop3, prop4, prop5` |

Die folgende Tabelle enthält eine Liste der Standard-Commerce-Ereignisse. Die Erstkonfiguration für diese Ereignisse ist in allen Report Suite-Vorlagen identisch. Ereignisse mit der Variablen s_code vom Typ N/A müssen nicht festgelegt werden, sondern werden automatisch bereitgestellt.

| Commerce-Standardereignisse | Typ | `s_code`-Variable |
|---|---|---|
| Umsatz | Zähler | `purchase` |
| Bestellungen | Zähler | `purchase` |
| Einheiten | Zähler | `purchase` |
| Warenkörbe | Zähler | `scOpen` |
| Warenkorbansichten | Zähler | `scView` |
| Instanzen | Zähler | nicht angegeben |
| Checkouts | Zähler | `scCheckout` |
| Zusatz zum Warenkorb | Zähler | `scAdd` |
| Entnahme aus Warenkorb | Zähler | `scRemove` |
| Besuche | Zähler (keine untergeordneten Beziehungen) | nicht angegeben |
| Seitenansichten | Zähler (keine untergeordneten Beziehungen) | nicht angegeben |
| Unique Visitors pro Tag | Zähler (keine untergeordneten Beziehungen) | nicht angegeben |
| Unique Visitors | Zähler (keine untergeordneten Beziehungen) | nicht angegeben |
