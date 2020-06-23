---
title: account
description: Verwenden Sie Variable „account“, um die Report Suite zu bestimmen, an die Daten gesendet werden.
translation-type: ht
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# account

>[!IMPORTANT] Diese Variable wurde eingestellt. Verwenden Sie die [`s.sa()`](../functions/sa-method.md)-Funktion, wenn Sie bei Ihrer Implementierung die Ziel-Report Suite ändern müssen.

In früheren Versionen von Adobe Analytics hat die `account`-Variable die Report Suite ermittelt, an die Sie Daten senden möchten. Zum Senden von Daten an Adobe Analytics ist eine Report Suite-ID erforderlich.

* Wenn Sie Adobe Experience Platform Launch verwenden, befinden sich die Report Suites beim Konfigurieren der Adobe Analytics-Erweiterung im Akkordeon [!UICONTROL Bibliotheksverwaltung].
* Wenn Sie die [`s_gi()`](../functions/s-gi.md)-Funktion zum Instanziieren eines Analytics-Tracking-Objekts verwenden, sind die Report Suite-IDs bereits als erforderliches Argument in der Funktion vorhanden.
