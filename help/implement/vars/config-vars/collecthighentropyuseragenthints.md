---
title: collectHighEntropyUserAgentHints
description: Verwenden Sie die Variable „collectHighEntropyUserAgentHints“, um zu bestimmen, ob Adobe Hinweise mit hoher Entropie von Chromium-Browsern (z. B. Google Chrome und Microsoft Edge) anfordern soll.
exl-id: 97cfa0f9-b35d-4c73-822f-adf30d0b7efc
feature: Appmeasurement Implementation
role: Admin, Developer
TQID: https://experienceleague.adobe.com/jipxox--J6tVTjpES3YuOTOqL-SXvCMLSvvbpj620Q4
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 240
ht-degree: 100%

---

# collectHighEntropyUserAgentHints

Client-Hinweise mit hoher Entropie werden von Adobe Analytics verwendet, um die Geräte- und Browser-Identifizierung zu verbessern. Diese Option ist ab Version 2.23.0 von AppMeasurement.js verfügbar. Weitere Informationen zu Client-Hinweisen finden Sie in [diesem Überblick und diesen häufig gestellten Fragen](/help/technotes/client-hints.md) sowie im [Google-Blog](https://web.dev/user-agent-client-hints/).

## Erfassen von Hinweisen mit hoher Entropie über das Web SDK

Client-Hinweise mit hoher Entropie sind Teil der Web SDK-Kontextkategorien. Weitere Informationen finden Sie unter [Konfigurieren von Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=de).

## Erfassen von Hinweisen mit hoher Entropie über die Adobe Analytics-Erweiterung

**[!UICONTROL Benutzeragenten-Hinweise mit hoher Entropie erfassen]** ist ein Kontrollkästchen unter dem Akkordeon „Allgemein“ bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/#/@adobepm/data-collection?lang=de) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte [!UICONTROL Tag-Eigenschaft].
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf [!UICONTROL Konfigurieren].
1. Erweitern Sie das Akkordeon [!UICONTROL Allgemein], um das Kontrollkästchen [!UICONTROL Benutzeragenten-Hinweise mit hoher Entropie erfassen] anzuzeigen. Es ist standardmäßig deaktiviert.

## collectHighEntropyUserAgentHints in AppMeasurement

Die Variable `s.collectHighEntropyUserAgentHints` bestimmt, ob AppMeasurement Hinweise mit hoher Entropie von Chromium-Browsern (z. B. Google Chrome und Microsoft Edge) anfordern soll. Diese Hinweise werden von Adobe Analytics verwendet, um die Geräte- und Browser-Identifizierung zu verbessern.

Wenn sie auf `true` festgelegt ist, werden alle Hinweise mit hoher Entropie vom Browser angefordert.

```js
s.collectHighEntropyUserAgentHints = true;
```
