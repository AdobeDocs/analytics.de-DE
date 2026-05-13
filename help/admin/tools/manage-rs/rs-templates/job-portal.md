---
description: Definiert allgemeine Einstellungen für ein Job-Portal oder eine Website zur Stellensuche.
title: Job-Portal
feature: Report Suite Settings
exl-id: d2a03139-7a5d-47bd-a287-fbe83f4a99fd
TQID: https://experienceleague.adobe.com/OVG4imjeOn6ZbW5BzTXVgGvmeNRF8soe1ODrKkIWBVk
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
subfeature_v2:
  - id: fab61dd8-112a-4e5e-ad5f-fb0240b7a60b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 178
ht-degree: 64%

---

# Job-Portal

Definiert allgemeine Einstellungen für ein Job-Portal oder eine Website zur Stellensuche.

| Konversionsvariablen | Typ | Subrelationen | Zuordnung | Gültigkeit | `s_code`-Variable |
|---|---|---|---|---|---|
| Interne Promotion | Zeichenfolge | Einfach | Zuletzt verwendet (Letzter) | Besuch | `evar1` |
| Interne Suchbegriff | Zeichenfolge | Einfach | Zuletzt verwendet (Letzter) | Besuch | `evar2` |
| Self-Service-Ereignistyp | Zeichenfolge | Einfach | Zuletzt verwendet (Letzter) | Besuch | `evar3` |

Von dieser Report Suite-Vorlage werden keine Erfolgsereignisse konfiguriert.

| Benutzerdefinierte Insight-Variablen | `s_code`-Variable |
|---|---|
| Sicher/Nicht sicher | `prop1` |
| Traffic-Eigenschaft 2-5 | `prop2, prop3, prop4, prop5` |

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
