---
description: Definiert allgemeine Einstellungen für eine Website, die Inhalte zusammenträgt, z. B. ein Nachrichtenportal.
title: Aggregatorportal
feature: Report Suite Settings
exl-id: 48f57f27-289c-4e26-9fb2-e34d48c1f2e6
source-git-commit: 72bd67179e003b70233d863d34153fec77548256
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 100%

---

# Aggregatorportal

Definiert allgemeine Einstellungen für eine Website, die Inhalte zusammenträgt, z. B. ein Nachrichtenportal.

| Konversionsvariablen | Typ | Subrelationen | Zuordnung | Gültigkeit | `s_code`-Variable |
|---|---|---|---|---|---|
| Interne Kampagne | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar1` |
| Interne Suchbegriffe | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar2` |
| Referrer-Kategorie | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar3` |

| Erfolgsereignisse | Typ | `s_code`-Variable |
|---|---|---|
| Anmelden | Zähler (keine Subrelationen) | `event1` |
| Referrer-Ansicht | Zähler (keine Subrelationen) | `event2` |
| Referrer-Klicks | Zähler (keine Subrelationen) | `event3` |

| Benutzerdefinierte Insight-Variablen | `s_code`-Variable |
|---|---|
| Traffic-Eigenschaft 1-5 | `prop1, prop2, prop3, prop4, prop5` |

Die folgende Tabelle enthält eine Liste der Standard-Verkaufsereignisse. Die Anfangskonfiguration für diese Ereignisse ist in allen Report Suite-Vorlagen gleich. Ereignisse mit einer N/A Variablen „s_code“ müssen nicht eingestellt werden, da sie automatisch bereitgestellt werden.

| Standard-Verkaufsereignisse | Typ | `s_code`-Variable |
|---|---|---|
| Umsatz | Zähler | `purchase` |
| Bestellungen | Zähler | `purchase` |
| Einheiten | Zähler | `purchase` |
| Warenkorb | Zähler | `scOpen` |
| Warenkorbansichten | Zähler | `scView` |
| Instanzen | Zähler | nicht angegeben |
| Checkouts | Zähler | `scCheckout` |
| Zusatz zum Warenkorb | Zähler | `scAdd` |
| Entnahme aus Warenkorb | Zähler | `scRemove` |
| Besuche | Zähler (keine Subrelationen) | nicht angegeben |
| Seitenansichten | Zähler (keine Subrelationen) | nicht angegeben |
| Unique Visitors pro Tag | Zähler (keine Subrelationen) | nicht angegeben |
| Unique Visitors | Zähler (keine Subrelationen) | nicht angegeben |
