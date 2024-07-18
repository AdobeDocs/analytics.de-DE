---
title: Nachverfolgen des Abmeldegrunds
description: Vorschau der ausgeschlossenen Daten durch Aktivierung der Datenschutzeinstellungen
feature: Dimensions
exl-id: f0521f4f-b11e-4ce3-b0fe-60788be6b120
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 7%

---

# Nachverfolgen des Abmeldegrunds

*Diese Seite bezieht sich auf die Dimension [2}, mit der Sie die potenziellen Auswirkungen der Aktivierung bestimmter Report Suite-Einstellungen auf die Daten sehen können. ](overview.md) Sie ist nicht mit dem [Adobe Experience Cloud ID-Opt-in-Dienst](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html?lang=de) verknüpft.*

Die Dimension &quot;Tracking-Opt-out-Grund&quot;dient als Vorschau auf Daten, die ausgeschlossen würden, wenn Sie Datenschutzeinstellungen aktiviert hätten. Diese Dimension wird hauptsächlich verwendet, um zu ermitteln, ob Ihre Implementierung negative Auswirkungen hätte, wenn Sie unter &quot;Report Suite-Einstellungen&quot;die Option [Datenschutzeinstellungen](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/browser-cookie-settings.html) aktiviert haben.

Typische Implementierungen sehen 1 % oder weniger des gesamten Report Suite-Traffics unter dieser Dimension, wenn die Datenschutzeinstellungen noch nicht aktiviert wurden. Prozentsätze über 1 % des gesamten Traffics deuten auf ein potenzielles Implementierungsproblem hin, das verhindert, dass AppMeasurement Erstanbieter-Cookies setzt.

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert, die die [Datenschutzeinstellungen](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/browser-cookie-settings.html) noch nicht aktiviert haben. Wenn Ihre Organisation die Einstellung **[!UICONTROL Benutzer entfernen, die alle Cookies blockiert haben]** bereits für Desktop- und mobile Browser aktiviert hat, enthält diese Dimension keine Daten.

## Dimensionselemente

Zu den Dimensionselementen gehören `"Cookies disabled by Desktop Browser"` und `"Cookies disabled by Mobile Browser"`.

* **Cookies vom Desktop-Browser deaktiviert**: Der Besucher hat Cookies über einen Desktop-Browser blockiert und **[!UICONTROL Benutzer, die alle Cookies in Desktopbrowsern blockiert haben, wurden entfernt]** ist deaktiviert.
* **Cookies vom mobilen Browser deaktiviert**: Der Besucher hat Cookies über einen mobilen Browser blockiert und **[!UICONTROL Benutzer, die alle Cookies in mobilen Browsern blockiert haben, wurden entfernt]** ist deaktiviert.
