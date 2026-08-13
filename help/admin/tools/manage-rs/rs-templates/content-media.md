---
description: Definiert allgemeine Einstellungen für eine Website, die Originalinhalte entwickelt und Artikel und Videos anzeigt.
title: Inhalte und Medien
feature: Report Suite Settings
exl-id: 9983ff86-9341-4b01-b4f3-41042874a9fb
TQID: https://experienceleague.adobe.com/AASIeik0YkTmYjhAff09KB38tsBsYXiKgIawb5e5tAc
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
subfeature_v2: id: fab61dd8-112a-4e5e-ad5f-fb0240b7a60b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 215
ht-degree: 57%

---

# Inhalte und Medien

Definiert allgemeine Einstellungen für eine Website, die Originalinhalte entwickelt und Artikel und Videos anzeigt.

| Konversionsvariablen | Typ | Subrelationen | Zuordnung | Gültigkeit | `s_code`-Variable |
|---|---|---|---|---|---|
| Interne Kampagne | Zeichenfolge | Einfach | Zuletzt verwendet (Letzter) | Besuch | `evar1` |
| Interne Suchbegriff | Zeichenfolge | Einfach | Zuletzt verwendet (Letzter) | Besuch | `evar2` |
| Commerce-Variable 3 | Zeichenfolge | Einfach | Zuletzt verwendet (Letzter) | Besuch | `evar3` |
| Commerce-Variable 4 | Zeichenfolge | Einfach | Zuletzt verwendet (Letzter) | Besuch | `evar4` |

| Erfolgsereignisse | Typ | `s_code`-Variable |
|---|---|---|
| Registrierungen | Zähler (keine untergeordneten Beziehungen) | `event1` |
| E-Mail-Registrierungen | Zähler (keine untergeordneten Beziehungen) | `event2` |
| Abonnements | Zähler (keine untergeordneten Beziehungen) | `event3` |
| Seitenansichten | Zähler (keine untergeordneten Beziehungen) | `event4` |
| Anzeigen-Impressions | Zähler (keine untergeordneten Beziehungen) | `event5` |
| Anzeigenklicks | Zähler (keine untergeordneten Beziehungen) | `event6` |

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
