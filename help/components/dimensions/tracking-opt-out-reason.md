---
title: Nachverfolgen des Abmeldegrunds
description: Sie können in einer Vorschau anzeigen, welche Daten ausgeschlossen werden, wenn Sie die Datenschutzeinstellungen aktivieren.
feature: Dimensions
exl-id: f0521f4f-b11e-4ce3-b0fe-60788be6b120
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 7%

---

# Nachverfolgen des Abmeldegrunds

*Diese Seite bezieht sich auf die [Dimension](overview.md) mit der Sie potenzielle Auswirkungen der Aktivierung bestimmter Report Suite-Einstellungen auf Daten sehen können. Sie steht in keiner Verbindung zum Opt-in-Dienst für die Adobe Experience Cloud ID [&#128279;](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html?lang=de).*

Die Dimension „Tracking-Opt-out-Grund“ dient als Vorschau auf Daten, die bei Aktivierung der Datenschutzeinstellungen ausgeschlossen würden. Diese Dimension wird in erster Linie verwendet, um zu bestimmen, ob Ihre Implementierung negativ beeinflusst würde, wenn Sie [Datenschutzeinstellungen](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/browser-cookie-settings.html) unter Report Suite-Einstellungen aktivieren.

Bei typischen Implementierungen wird bis zu 1 % des gesamten Traffics der Report Suite unter dieser Dimension angezeigt, wenn die Datenschutzeinstellungen noch nicht aktiviert wurden. Prozentsätze über 1 % des gesamten Traffics deuten auf ein potenzielles Implementierungsproblem hin, das AppMeasurement daran hindert, Erstanbieter-Cookies zu setzen.

## Füllen dieser Dimension mit Daten

Diese Dimension ist für alle Implementierungen vorkonfiguriert, die noch nicht aktiviert sind [Datenschutzeinstellungen](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/browser-cookie-settings.html). Wenn Ihr Unternehmen die Einstellung **[!UICONTROL Benutzer entfernen, die alle Cookies blockiert haben]** sowohl für Desktop- als auch für mobile Browser bereits aktiviert hat, enthält diese Dimension keine Daten.

## Dimensionselemente

Zu den Dimensionselementen gehören `"Cookies disabled by Desktop Browser"` und `"Cookies disabled by Mobile Browser"`.

* **Cookies durch Desktop-Browser deaktiviert**: Der Besucher hat Cookies mithilfe eines Desktop-Browsers blockiert und **[!UICONTROL Entfernen Sie Benutzer, die alle Cookies in Desktop-Browsern blockiert haben]** ist deaktiviert.
* **Cookies durch mobilen Browser deaktiviert**: Der Besucher blockiert Cookies mithilfe eines mobilen Browsers und **[!UICONTROL Entfernen Sie Benutzer, die alle Cookies in mobilen Browsern blockiert haben]** ist deaktiviert.
