---
title: Besucheridentifizierung mit der Web SDK JavaScript-Bibliothek
description: Identifizieren Sie Besuchende beim Implementieren der Web SDK JavaScript-Bibliothek korrekt.
source-git-commit: 779ba5b0a1d71467aaaf3872fd707cc323ae8af2
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Besucheridentifizierung mit der Web SDK JavaScript-Bibliothek

Adobe Experience Platform Web SDK (`alloy.js`) bietet einen einheitlichen, modernen Ansatz für die Datenerfassung für alle Adobe Experience Cloud-Anwendungen, einschließlich Adobe Analytics. Identitätsdaten können mithilfe der `identityMap` von XDM erweitert werden, um benutzerdefinierte IDs und mehrere Namespaces zu unterstützen. Adobe empfiehlt die Verwendung des Adobe Experience Cloud ID-Service als primäre Kennung für Analytics sowie die Verwendung anderer Identitätsverwaltungsoptionen für erweiterte Szenarien.

Wenn Ihr Unternehmen die Web SDK JavaScript-Bibliothek verwendet, um Daten an Adobe Analytics zu senden, ist eine Mindestkonfiguration für die Besucheridentifizierung erforderlich. Der Besucher-ID-Dienst ist nativ in der Bibliothek integriert. Sie müssen lediglich **[!UICONTROL Edge Domain]** im `configure` festlegen. Wenn dieses Feld auf den gewünschten Wert eingestellt ist, funktioniert die Besucheridentifizierung ohne zusätzliche Konfiguration.
