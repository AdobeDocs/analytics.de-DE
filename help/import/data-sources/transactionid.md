---
title: Transaktions-ID-Datenquellen
description: Erfahren Sie mehr über den allgemeinen Workflow bei der Verwendung der Transaktions-ID-Datenquellen.
feature: Data Sources
exl-id: 5f26b15c-8d9c-46d5-860f-13fdfa21af2e
role: Admin
source-git-commit: 1d905aa47b4573a35012d56c0cf70fbc944bc972
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 7%

---

# Transaktions-ID-Datenquellen

Transaktions-ID-Datenquellen sind eine Variante von Zusammenfassungsdatenquellen, mit denen Sie Online- und Offline-Daten miteinander verknüpfen können. Dazu müssen Sie die [`transactionID`](/help/implement/vars/page-vars/transactionid.md)-Variablen in Ihrer Analytics-Implementierung verwenden.

* Wenn eine Zeile in einer Datenquellendatei eine Transaktions-ID enthält, die mit einer bereits von AppMeasurement erfassten Transaktions-ID übereinstimmt, werden die Dimensionen und Metriken an den Online-Treffer angehängt.
* Wenn eine Zeile in einer Datenquellendatei eine Transaktions-ID enthält, die keine Übereinstimmung enthält, wird die Zeile ähnlich wie Zusammenfassungsdatenquellen behandelt.

>[!NOTE]
>
>Bevor Sie Transaktions-ID-Datenquellen verwenden können, müssen Sie sie zunächst in [Allgemeine Kontoeinstellungen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md) für die gewünschte Report Suite aktivieren.

Wenn Sie einen Online-Treffer senden, der einen [`transactionID`](/help/implement/vars/page-vars/transactionid.md) enthält, erstellt Adobe eine „Momentaufnahme“ aller dann festgelegten oder persistierten Variablen. Wenn eine übereinstimmende Transaktions-ID gefunden wird, die über Datenquellen hochgeladen wurde, werden die Offline- und Online-Daten miteinander verknüpft.

Transaktions-ID-Datenquellen haben die folgenden Eigenschaften:

* Die Online-Daten müssen zuerst erfasst und verarbeitet werden. Wenn eine Transaktions-ID-Datenquelle hochgeladen wird, bevor eine Report Suite einen Treffer verarbeitet, der mit dieser Transaktions-ID übereinstimmt, werden die Daten nicht verknüpft.
* Über AppMeasurement erfasste Transaktions-IDs laufen nach 25 Monaten ab.
* Datenquellen, die mit einer abgelaufenen Transaktions-ID hochgeladen wurden, werden ähnlich wie Daten behandelt, die ohne Transaktions-ID hochgeladen wurden.
* Wenn dieselbe Variable sowohl im Online-Treffer als auch in der Transaktions-ID-Datenquelle enthalten ist, wird der Wert aus der Transaktions-ID-Datenquelle im Transaktions-Datenquellen-Treffer verwendet.
* Wenn eine Variable in einem Online-Treffer, aber nicht in einem übereinstimmenden Transaktions-ID-Datenquellen-Treffer enthalten ist, wird die Online-Treffervariable beibehalten.
* Wenn Sie dieselbe Transaktions-ID für mehrere Online-Treffer festlegen, wird nur das erste Vorkommen mit Daten aus einer übereinstimmenden Transaktions-ID-Datenquelle geändert.

Zum Beispiel:

1. Sie können eine Seitenansicht von AppMeasurement aus senden, wobei:
   * `eVar1` ist gleich `blue`
   * `eVar2` ist gleich `water`
   * `events` ist gleich `event1`
   * `transactionID` ist gleich `1256`
2. Nachdem der Treffer erfasst und verarbeitet wurde, laden Sie eine Transaktions-ID-Datenquelle hoch, in der:
   * `eVar1` ist gleich `yellow`
   * `eVar3` ist gleich `bird`
   * `events` ist gleich `event2`
   * `transactionID` ist gleich `1256`
3. Nachdem der Datenquellen-Treffer verarbeitet wurde, können Sie einen Bericht in Workspace anzeigen. Die Daten würden Folgendes zeigen:
   * `eVar1` ist gleich `yellow`
   * `eVar2` ist gleich `water`
   * `eVar3` ist gleich `bird`
   * `events` ist gleich `event2`

Der eVar1-`blue` und die `event1` Metrik sind in Berichten nicht vorhanden, da der Transaktions-ID-Treffer diese entsprechenden Werte überschrieben hat.
