---
title: Nachverfolgen des Abmeldegrunds
description: Sie können in einer Vorschau anzeigen, welche Daten ausgeschlossen werden, wenn Sie die Datenschutzeinstellungen aktivieren.
feature: Dimensions
exl-id: f0521f4f-b11e-4ce3-b0fe-60788be6b120
TQID: https://experienceleague.adobe.com/mFYYrj4iBWBi87sErHnWTYXce3lUhV0pwUt63x3vfnY
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 281
ht-degree: 11%

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
