---
description: Kombinieren Sie sowohl Daten mit als auch ohne Zeitstempel in einer einzigen Report Suite.
title: Konfiguration von Zeitstempeln
feature: Admin Tools
uuid: 0fa63658-1cc2-4adc-8d51-a0662d0aa941
exl-id: 4d64225a-5eb8-4b7b-ba13-3cdc12dd6651
role: Admin
source-git-commit: 2d5348a4a6377313f5aab229214d97a02c826939
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 5%

---

# Konfiguration von Zeitstempeln

Auf der [!UICONTROL Konfiguration von Zeitstempeln] können Sie **[!UICONTROL Zeitstempel optional]** für eine oder mehrere Report Suites aktivieren. Mit dieser Einstellung können Sie Daten mit und ohne Zeitstempel in einer einzigen Report Suite kombinieren.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Zeitstempel optional]**

## Aktuelle Zeitstempeleinstellung

In diesem Abschnitt wird Ihre aktuelle Zeitstempelkonfiguration für die ausgewählte Report Suite angezeigt. Dies kann einer von drei möglichen Werten sein:

* **Zeitstempel nicht zulässig (Einstellung `visitorID` unterstützt)**
* **Zeitstempel erforderlich (Einstellung `visitorID` nicht unterstützt)**
* **Zeitstempel optional (Einstellung `visitorID` unterstützt, aber nicht bei Treffern mit Zeitstempel)**

Unter diesem Text befindet sich das Kontrollkästchen **[!UICONTROL Ausgewählte Report Suites in Zeitstempel konvertieren optional]**. Wenn Sie dieses Kontrollkästchen aktivieren und dann **[!UICONTROL Speichern]** aktivieren, [!UICONTROL Zeitstempel optional] für die ausgewählten Report Suites.

## Zeitstempel nicht zulässig

Wenn Sie mit dieser Zeitstempelkonfiguration Daten an eine Report Suite senden, wird der Zeitstempel verwendet, wenn die Verarbeitungs-Server von Adobe den Treffer erhalten. Wenn Sie versuchen, die [`timestamp`](/help/implement/vars/page-vars/timestamp.md) Variable festzulegen, wird der Treffer dauerhaft gelöscht.

## Zeitstempel erforderlich

Wenn Sie mit dieser Zeitstempelkonfiguration Daten an eine Report Suite senden, muss jeder Treffer die [`timestamp`](/help/implement/vars/page-vars/timestamp.md) Variable enthalten. Wenn in einem Treffer eine `timestamp` Implementierungsvariable fehlt, wird der Treffer dauerhaft gelöscht.

Mit Zeitstempel versehene Daten werden bis zu 92 Tage gespeichert. Mit anderen Worten: Ein Besuch wird 92 Tage lang „offen gehalten“, sodass alle zusätzlichen Treffer in denselben Besuch/dieselbe Sitzung aufgenommen werden können. Sie können zwar Daten zu vorhandenen Sitzungen hinzufügen, Adobe empfiehlt jedoch, Treffer in der richtigen Reihenfolge pro Besucher hinzuzufügen. Treffer, die pro Besucher nicht in der richtigen Reihenfolge empfangen werden, können zu unerwarteten Berichtsergebnissen führen. Viele dieser Einschränkungen werden jedoch durch die Verarbeitung zur Berichtszeit verringert.

## Zeitstempel optional

Die Einstellung [!UICONTROL Zeitstempel optional] ermöglicht die Integration und Berichterstellung über mehrere Report Suites hinweg mit oder ohne die Variable [`timestamp`](/help/implement/vars/page-vars/timestamp.md) . Ideale Anwendungsfälle für [!UICONTROL Zeitstempel optional] sind:

* Kombination von Daten mit und ohne Zeitstempel in derselben globalen Report Suite
* Senden von Daten mit Zeitstempel von einer Mobile App an eine globale Report Suite
* Aktualisieren von Apps auf die Verwendung des Offline-Trackings, ohne dass eine neue Report Suite erstellt werden muss

Diese Einstellung ist standardmäßig für alle neuen Report Suites aktiviert, es sei denn, die neue Report Suite wurde aus einer Report Suite mit einer anderen Zeitstempelkonfigurationseinstellung kopiert.

>[!WARNING]
>
>Wenn Sie [!UICONTROL Zeitstempel optional] verwenden, legen Sie keine [`visitorID`](/help/implement/vars/config-vars/visitorid.md) für Daten mit Zeitstempel fest. Diese Aktion kann zu fehlerhaften Daten führen und sich negativ auf Zeitberechnungen (z. B. Besuchszeit), Attribution, Anzahl der Besuche/Besuche und Pfadberichte auswirken.

Nachdem Sie [!UICONTROL Zeitstempel optional] aktiviert haben, können Sie sie in dieser Benutzeroberfläche nicht mehr deaktivieren. Wenden Sie sich in dem unwahrscheinlichen Fall, dass Sie zu einer anderen Zeitstempelkonfigurationseinstellung zurückkehren möchten, an die Adobe-Kundenunterstützung.
