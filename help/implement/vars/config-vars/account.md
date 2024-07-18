---
title: account
description: (Veraltet) Bestimmen Sie die Report Suite, an die Daten gesendet werden.
feature: Variables
exl-id: 075d20be-6109-4024-84c4-1d048678d2bd
role: Admin, Developer
source-git-commit: 75ae77c1da1b578639609888e794e13d965ef669
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 38%

---

# account

>[!IMPORTANT]
>
>Diese Variable wurde eingestellt. Verwenden Sie die [`s.sa()`](../functions/sa-method.md)-Funktion, wenn Sie bei Ihrer Implementierung die Ziel-Report Suite ändern müssen.

In früheren Versionen von Adobe Analytics hat die `account`-Variable die Report Suite ermittelt, an die Sie Daten senden möchten. Zum Senden von Daten an Adobe Analytics ist eine Report Suite-ID erforderlich.

* Wenn Sie das Web SDK verwenden, befinden sich die Report Suites in den Einstellungen des Adobe Analytics-Dienstes innerhalb des Datastreams, an den das Web SDK Daten sendet.
* Wenn Sie die Adobe Analytics-Erweiterung verwenden, befinden sich Report Suites beim Konfigurieren der Adobe Analytics-Erweiterung unter dem Akkordeon [!UICONTROL Bibliotheksverwaltung] .
* Wenn Sie die Funktion [`s_gi()`](../functions/s-gi.md) zum Instanziieren eines Analytics-Tracking-Objekts verwenden, sind die Report Suite-ID(s) bereits als erforderliches Argument in der Funktion vorhanden.
