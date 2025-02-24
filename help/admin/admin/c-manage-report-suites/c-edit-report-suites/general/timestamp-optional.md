---
description: Kombinieren Sie sowohl Daten mit als auch ohne Zeitstempel in einer einzigen Report Suite.
title: Zeitstempel optional
feature: Admin Tools
uuid: 0fa63658-1cc2-4adc-8d51-a0662d0aa941
exl-id: 4d64225a-5eb8-4b7b-ba13-3cdc12dd6651
role: Admin
source-git-commit: def7d071de1765acf524a638a8f8d13ae69e1a1f
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 89%

---

# Zeitstempel optional

Kombinieren Sie sowohl Daten mit als auch ohne Zeitstempel in einer einzigen Report Suite.

„Zeitstempel optional“ bietet folgende Möglichkeiten:

* Sie können auch Daten mit und Daten ohne Zeitstempel gemeinsam in einer globalen Report Suite verwenden.
* Senden Sie Daten mit Zeitstempel von einer mobilen App an eine globale Report Suite.
* Aktualisieren Sie Apps, um die Offline-Nachverfolgung zu verwenden, ohne eine neue Report Suite erstellen zu müssen.

>[!WARNING]
>
>Wenn Sie „Zeitstempel optional“ verwenden, dürfen Sie für bereits mit einem Zeitstempel versehene Daten [s.visitorID](/help/implement/vars/config-vars/visitorid.md) nicht festlegen. Diese Festlegung kann zu Unordnung in den Daten führen und sich negativ auf Zeitberechnungen (wie Besuchszeitwerte), die Attribution (eVar-Persistenz), Besuchsnummer/Besuchsanzahl und Pfadsetzungsberichte auswirken.

>[!NOTE]
>
>Mit Zeitstempel versehene Daten werden bis zu 92 Tage gespeichert. Das bedeutet, dass ein Besuch/eine Sitzung 92 Tage lang „offen gehalten“ wird, während jeder zusätzliche Hit – also keine 30 Minuten nach dem vorherigen Hit (in der Hit-Zeit) – noch in denselben Besuch/dieselbe Sitzung einbezogen werden kann. Alle „alten“ Treffer, die nicht in der richtigen Reihenfolge empfangen werden, führen zu „unbekannten“ Ergebnissen, da eine Reihe von Faktoren (Segmentierung, Zuordnung, Gültigkeit usw.) beeinflussen, ob diese Treffer in Berichte aufgenommen werden oder nicht.

## Neue Report Suites {#section_095A7CFBD280494593B9BEC1592B73A6}

* Wenn sie aus einer Vorlage erstellt wird, gilt für eine neue Report Suite die Standardeinstellung „Zeitstempel optional“.

  (Sie können eine neue Report Suite über **Admin > Report Suites > Neu erstellen > Report Suite** aus einer Vorlage erstellen.)
* Wenn sie aus einer vorhandenen Report Suite kopiert wird, erbt die neue Report Suite die Zeitstempeleinstellung des Originals, einschließlich:

   * **Keine Zeitstempel zulässig** (Einstellung „s.visitorID“ wird unterstützt)
   * **Zeitstempel erforderlich** (Einstellung „s.visitorID“ wird nicht unterstützt)
   * **Zeitstempel optional** (Einstellung „s.visitorID“ wird unterstützt, aber nicht für Zeitstempeltreffer)

## Änderung vorhandener Report Suites in „Zeitstempel optional“  {#section_40BCD3B4639241DEA716F7640ED33E72}

1. Wechseln Sie zu **Admin > Report Suites > Einstellungen bearbeiten > Allgemein > Zeitstempelkonfiguration**.
1. Aktivieren Sie **Ausgewählte Report Suites in „Zeitstempel optional“ konvertieren**.

   Damit wird die Report Suite in „Zeitstempel optional“ geändert.

>[!NOTE]
>
>Wurde eine Report Suite auf **Zeitstempel optional** festgelegt, müssen Sie sich an die Adobe-Kundenunterstützung wenden, um diese oder andere Einstellungen zu ändern.
