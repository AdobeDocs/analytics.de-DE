---
description: Definiert allgemeine Einstellungen für eine E-Commerce-Website.
title: Handel
feature: Report Suite Settings
exl-id: 90e5d446-10b8-4d40-8bd0-8b13e1c2f603
source-git-commit: 9057cc83881a72fa039e9398ed3daaf4259ef2bf
workflow-type: ht
source-wordcount: '181'
ht-degree: 100%

---

# Handel

Definiert allgemeine Einstellungen für eine E-Commerce-Website.

| Konversionsvariablen | Typ | Subrelationen | Zuordnung | Gültigkeit | `s_code`-Variable |
|---|---|---|---|---|---|
| Interne Promotions | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar1` |
| Interne Suchbegriffe | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar2` |
| Merchandising-Kategorie | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar3` |
| Handelsvariable 4 | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar4` |
| Handelsvariable 5 | Zeichenfolge | Basis | Zuletzt verwendet (Letzter) | Besuch | `evar5` |

| Erfolgsereignisse | Typ | `s_code`-Variable |
|---|---|---|
| Registrierungen | Zähler (keine Subrelationen) | `event1` |
| Benutzerspezifische Ereignisse 1-5 | Zähler (keine Subrelationen) | `event1, event2, event3, event4, event5` |

| Benutzerdefinierte Insight-Variablen | `s_code`-Variable |
|---|---|
| Traffic-Eigenschaft 1-5 | `prop1, prop2, prop3, prop4, prop5` |

Die folgende Tabelle enthält eine Liste der Standard-Verkaufsereignisse. Die Anfangskonfiguration für diese Ereignisse ist in allen Report Suite-Vorlagen gleich. Ereignisse mit einer N/A Variablen „s_code“ müssen nicht eingestellt werden, da sie automatisch bereitgestellt werden.

| Standard-Verkaufsereignisse | Typ | `s_code`-Variable |
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
| Besuche | Zähler (keine Subrelationen) | nicht angegeben |
| Seitenansichten | Zähler (keine Subrelationen) | nicht angegeben |
| Unique Visitors pro Tag | Zähler (keine Subrelationen) | nicht angegeben |
| Unique Visitors | Zähler (keine Subrelationen) | nicht angegeben |
