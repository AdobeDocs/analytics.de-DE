---
title: Besucheridentifizierung mit der Web SDK JavaScript-Bibliothek
description: Identifizieren Sie Besuchende beim Implementieren der Web SDK JavaScript-Bibliothek korrekt.
exl-id: e650d6b1-6e29-4a9c-98dd-8482f50968d1
TQID: 'https://experienceleague.adobe.com/k9u260HKJg6hhs7REAQ3-uE4pHvrUPBv6x8yLjZ5tvc'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: e4f5f438-eabb-4c54-9133-b817e3d125f5
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: a947d2d7f45d4155a61cbfe0f8110851cca32e60
workflow-type: tm+mt
source-wordcount: 198
ht-degree: 2%

---

# Besucheridentifizierung mit der Web SDK JavaScript-Bibliothek

Die Adobe Experience Platform Web SDK JavaScript Library (`alloy.js`) bietet einen einheitlichen, modernen Ansatz für die Datenerfassung für alle Adobe CX Enterprise-Anwendungen, einschließlich Adobe Analytics. Während die meisten Kundinnen und Kunden normalerweise die [Web SDK-Tag-Erweiterung](web-sdk-extension.md) implementieren, können Sie die Web SDK JavaScript-Bibliothek allein oder in einem Drittanbieter-Tag-Management-System verwenden. Unter [Alloy](https://github.com/adobe/alloy) auf GitHub finden Sie Informationen zum Herunterladen der neuesten Version der Bibliothek.

Identitätsdaten können mithilfe der [`identityMap`](https://experienceleague.adobe.com/de/docs/experience-platform/collection/identity/identity-map) von XDM erweitert werden, um benutzerdefinierte IDs und mehrere Namespaces zu unterstützen. Adobe empfiehlt die Verwendung von ECID als primäre Kennung für Analytics sowie die Verwendung anderer Identitätsverwaltungsoptionen für erweiterte Szenarien.

Wenn Ihr Unternehmen die Web SDK JavaScript-Bibliothek verwendet, um Daten an Adobe Analytics zu senden, ist eine Mindestkonfiguration für die Besucheridentifizierung erforderlich. Der Experience Platform Identity Service wird nativ in die Bibliothek eingebettet. Sie müssen lediglich **[!UICONTROL Edge Domain]** im `configure` festlegen. Wenn dieses Feld auf den gewünschten Wert eingestellt ist, funktioniert die Besucheridentifizierung ohne zusätzliche Konfiguration.
