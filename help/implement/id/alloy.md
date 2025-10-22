---
title: Besucheridentifizierung mit der Web SDK JavaScript-Bibliothek
description: Identifizieren Sie Besuchende beim Implementieren der Web SDK JavaScript-Bibliothek korrekt.
source-git-commit: 98e9dc4932bd23d3e0b632705945f56c243750c5
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---

# Besucheridentifizierung mit der Web SDK JavaScript-Bibliothek

Die Adobe Experience Platform Web SDK JavaScript Library (`alloy.js`) bietet einen einheitlichen, modernen Ansatz für die Datenerfassung für alle Adobe Experience Cloud-Programme, einschließlich Adobe Analytics. Während die meisten Kundinnen und Kunden normalerweise die [Web SDK-Tag-Erweiterung](web-sdk-extension.md) implementieren, können Sie die Web SDK JavaScript-Bibliothek allein oder in einem Drittanbieter-Tag-Management-System verwenden. Unter [Alloy](https://github.com/adobe/alloy) auf GitHub finden Sie Informationen zum Herunterladen der neuesten Version der Bibliothek.

Identitätsdaten können mithilfe der `identityMap` von XDM erweitert werden, um benutzerdefinierte IDs und mehrere Namespaces zu unterstützen. Adobe empfiehlt die Verwendung des Adobe Experience Cloud ID-Service als primäre Kennung für Analytics sowie die Verwendung anderer Identitätsverwaltungsoptionen für erweiterte Szenarien.

Wenn Ihr Unternehmen die Web SDK JavaScript-Bibliothek verwendet, um Daten an Adobe Analytics zu senden, ist eine Mindestkonfiguration für die Besucheridentifizierung erforderlich. Der Besucher-ID-Dienst ist nativ in der Bibliothek integriert. Sie müssen lediglich **[!UICONTROL Edge Domain]** im `configure` festlegen. Wenn dieses Feld auf den gewünschten Wert eingestellt ist, funktioniert die Besucheridentifizierung ohne zusätzliche Konfiguration.
