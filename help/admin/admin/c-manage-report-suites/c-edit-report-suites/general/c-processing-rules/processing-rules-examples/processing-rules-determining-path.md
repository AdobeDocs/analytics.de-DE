---
description: Sie können den Wert einer eVar-Variable in eine Prop kopieren, um die Pfadsetzung zu aktivieren.
subtopic: Processing rules
title: Bestimmen eines Pfads durch Kopieren eines eVar-Werts in eine Eigenschaft
feature: Admin Tools
role: Admin
exl-id: 23c978b9-a159-4364-9214-561a255d23e4
source-git-commit: 429aaa43fdae669350bdb5a5a54a7d4b9b1c65f2
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 100%

---

# Bestimmen eines Pfads durch Kopieren eines eVar-Werts in eine Eigenschaft

Sie können den Wert einer eVar-Variable in eine Prop kopieren, um die Pfadsetzung zu aktivieren.

Beim Festlegen von Werten erhält die Variable links den Wert der Variable rechts (auch wenn dieser Wert leer ist).

| Regelsatz | Wert |
|---|---|
| Bedingung | Keine (immer ausführen) |
| Aktion | Wert von Prop1 durch eVar1 überschreiben |

Sie können diese Regel zur Einstellung des Werts von Prop1 nur dann modifizieren, wenn sie nicht bereits einen Wert ähnlich dem Folgenden enthält:

| Regelsatz | Wert |
|---|---|
| Bedingung | Wenn Prop1 nicht eingestellt ist |
| Aktion | Wert von Prop1 durch eVar1 überschreiben |

Beispiel:

![](assets/overwrite-empty-prop.png)
