---
title: Besucheridentifizierung mit der Web SDK JavaScript-Bibliothek
description: Identifizieren Sie Besuchende beim Implementieren der Web SDK JavaScript-Bibliothek korrekt.
exl-id: e650d6b1-6e29-4a9c-98dd-8482f50968d1
TQID: https://experienceleague.adobe.com/R6O--qqR7SzlArrIDFCWunUEAduzmAS2Skm6BKyREnw
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 7d733a6375f6c6009563bc53f5a3ff090dbc48ed
workflow-type: tm+mt
source-wordcount: 192
ht-degree: 2%

---

# Besucheridentifizierung mit der Web SDK JavaScript-Bibliothek

Die Adobe Experience Platform Web SDK JavaScript Library (`alloy.js`) bietet einen einheitlichen, modernen Ansatz für die Datenerfassung für alle Adobe CX Enterprise-Anwendungen, einschließlich Adobe Analytics. Während die meisten Kundinnen und Kunden normalerweise die [Web SDK-Tag-Erweiterung](web-sdk-extension.md) implementieren, können Sie die Web SDK JavaScript-Bibliothek allein oder in einem Drittanbieter-Tag-Management-System verwenden. Unter [Alloy](https://github.com/adobe/alloy) auf GitHub finden Sie Informationen zum Herunterladen der neuesten Version der Bibliothek.

Identitätsdaten können mithilfe der `identityMap` von XDM erweitert werden, um benutzerdefinierte IDs und mehrere Namespaces zu unterstützen. Adobe empfiehlt die Verwendung des Adobe Experience Cloud ID-Service als primäre Kennung für Analytics sowie die Verwendung anderer Identitätsverwaltungsoptionen für erweiterte Szenarien.

Wenn Ihr Unternehmen die Web SDK JavaScript-Bibliothek verwendet, um Daten an Adobe Analytics zu senden, ist eine Mindestkonfiguration für die Besucheridentifizierung erforderlich. Der Besucher-ID-Dienst ist nativ in der Bibliothek integriert. Sie müssen lediglich **[!UICONTROL Edge Domain]** im `configure` festlegen. Wenn dieses Feld auf den gewünschten Wert eingestellt ist, funktioniert die Besucheridentifizierung ohne zusätzliche Konfiguration.
