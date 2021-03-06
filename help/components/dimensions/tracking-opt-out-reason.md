---
title: Nachverfolgen des Abmeldegrunds
description: Vorschau der ausgeschlossenen Daten durch Aktivierung der Datenschutzeinstellungen
feature: Dimensions
exl-id: f0521f4f-b11e-4ce3-b0fe-60788be6b120
source-git-commit: b7209b914695423099266f5c507eaa34c2b98bc5
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 9%

---

# Nachverfolgen des Abmeldegrunds

*Diese Seite bezieht sich auf die Dimension, mit der Sie die potenziellen Auswirkungen der Aktivierung bestimmter Report Suite-Einstellungen auf die Daten sehen können. Sie ist nicht mit dem [Adobe Experience Cloud ID-Opt-in-Dienst](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html?lang=de).*

Die Dimension &quot;Tracking-Opt-out-Grund&quot;dient als Vorschau auf Daten, die ausgeschlossen würden, wenn Sie Datenschutzeinstellungen aktiviert hätten. Diese Dimension wird hauptsächlich verwendet, um festzustellen, ob Ihre Implementierung negativ beeinflusst wird, wenn Sie [Datenschutzeinstellungen](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/browser-cookie-settings.html) unter Report Suite-Einstellungen.

Typische Implementierungen sehen 1 % oder weniger des gesamten Report Suite-Traffics unter dieser Dimension, wenn die Datenschutzeinstellungen noch nicht aktiviert wurden. Prozentsätze über 1 % des gesamten Traffics deuten auf ein potenzielles Implementierungsproblem hin, das AppMeasurement daran hindert, Erstanbieter-Cookies zu setzen.

## Diese Dimension mit Daten füllen

Diese Dimension ist bei allen Implementierungen, die noch nicht aktiviert sind, vorkonfiguriert. [Datenschutzeinstellungen](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/browser-cookie-settings.html). Wenn Ihr Unternehmen die Funktion **[!UICONTROL Entfernen von Benutzern, die alle Cookies blockiert haben]** -Einstellung für sowohl Desktop- als auch mobile Browser festlegen, enthält diese Dimension keine Daten.

## Dimensionselemente

Zu den Dimensionselementen gehören `"Cookies disabled by Desktop Browser"` und `"Cookies disabled by Mobile Browser"`.

* **Cookies vom Desktop-Browser deaktiviert**: Der Besucher blockierte Cookies mithilfe eines Desktop-Browsers und **[!UICONTROL Entfernen von Benutzern, die in Desktopbrowsern sämtliche Cookies blockiert haben]** deaktiviert ist.
* **Cookies durch mobilen Browser deaktiviert**: Der Besucher blockierte Cookies mithilfe eines mobilen Browsers und **[!UICONTROL Entfernen von Benutzern, die alle Cookies in mobilen Browsern blockiert haben]** deaktiviert ist.
