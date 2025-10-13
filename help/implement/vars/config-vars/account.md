---
title: account
description: (Eingestellt) Bestimmen Sie die Report Suite, an die Daten gesendet werden.
feature: Appmeasurement Implementation
exl-id: 075d20be-6109-4024-84c4-1d048678d2bd
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 38%

---

# account

>[!IMPORTANT]
>
>Diese Variable wurde eingestellt. Verwenden Sie die [`s.sa()`](../functions/sa-method.md)-Funktion, wenn Sie bei Ihrer Implementierung die Ziel-Report Suite ändern müssen.

In früheren Versionen von Adobe Analytics hat die `account`-Variable die Report Suite ermittelt, an die Sie Daten senden möchten. Zum Senden von Daten an Adobe Analytics ist eine Report Suite-ID erforderlich.

* Wenn Sie Web SDK verwenden, befinden sich Report Suites in den Adobe Analytics-Diensteinstellungen innerhalb des Datenstroms, an den die Web SDK Daten sendet.
* Wenn Sie die Adobe Analytics-Erweiterung verwenden, befinden sich die Report Suites beim Konfigurieren [!UICONTROL &#x200B; Adobe Analytics]Erweiterung im Akkordeon Bibliotheksverwaltung .
* Wenn Sie die Funktion [`s_gi()`](../functions/s-gi.md) verwenden, um ein Analytics-Tracking-Objekt zu instanziieren, sind die Report Suite-ID(s) bereits als erforderliches Argument in der Funktion vorhanden.
