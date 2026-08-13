---
title: Kundenperspektive
description: Gibt an, ob ein Mobile-App-Treffer aufgetreten ist, während sich die App im Vordergrund oder Hintergrund befand.
feature: Appmeasurement Implementation
role: Admin, Developer
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: d4db20e3498d54162806b3fdef0b34f45c93a6ff
workflow-type: tm+mt
source-wordcount: 199
ht-degree: 0%

---

# Kundenperspektive

Die Variable &quot;`customerPerspective`&quot; gibt an, ob ein Mobile-App-Treffer aufgetreten ist, während sich die Mobile App im Vordergrund oder Hintergrund befand. Sie wird als `cp` Abfrageparameter an die Adobe-Datenerfassung gesendet und füllt die Dimension [Treffertyp](/help/components/dimensions/hit-type.md) auf.

## Gültige Werte

`customerPerspective` akzeptiert die folgenden Zeichenfolgenwerte:

* `foreground`: Der Treffer trat auf, während die App aktiv verwendet wurde.
* `background`: Der Treffer trat auf, während die App im Hintergrund ausgeführt wurde, z. B. eine Standortaktualisierung oder ein Treffer, der durch eine Push-Benachrichtigung ausgelöst wurde.

## Festlegen dieser Variablen

Adobe Mobile SDK (Version 4.13.6 und höher) legt `customerPerspective` automatisch fest. Normalerweise erfolgt die Einstellung nicht manuell. Treffer, die von einem Browser über AppMeasurement gesendet werden, werden immer als `foreground` gemeldet. Wenn die Variable in einem Treffer fehlt, wird dieser Treffer als Vordergrundtreffer behandelt.

## Auswirkungen auf das Reporting

Die Unterscheidung zwischen Vordergrund und Hintergrund wirkt sich auf die Verarbeitung von Besuchen aus:

* Besuche werden nur gezählt, wenn sie mindestens einen Vordergrundtreffer enthalten.
* Hintergrundtreffer können nach wie vor Konversionsereignissen zugeordnet und über [&#x200B; kontextbezogene Sitzungen in Virtual Report &#x200B;](/help/components/vrs/vrs-mobile-visit-processing.md) analysiert werden. Dieses Verhalten ist nützlich, wenn Sie die Effektivität von Push-Benachrichtigungen messen.
