---
title: Besucheridentifizierung mit der Tag-Erweiterung „Web SDK"
description: Identifizieren Sie Besuchende beim Implementieren der Tag-Erweiterung „Web SDK" korrekt.
exl-id: 65de7fc3-a344-4f04-b523-1f5edf681d2f
TQID: https://experienceleague.adobe.com/W42VkHT5yCW0yO-FbiAFHHKM8dF5NgCveZYGFOs7sYk
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 192
ht-degree: 0%

---

# Besucheridentifizierung mit der Tag-Erweiterung „Web SDK&quot;

Die Web SDK-Tag-Erweiterung in der Adobe Experience Platform-Datenerfassung ermöglicht Unternehmen die Implementierung der Web-SDK über eine Tag-Management-Oberfläche. Erweiterte Szenarien wie Domain-übergreifende ID-Freigabe und Migration von Besucherprofilen können durch Erweiterungsregeln und Aktionen einfach konfiguriert werden. Durch die Verwendung von Web SDK ist Ihre Implementierung zukunftssicher und unterstützt ein nahtloses Upgrade auf Customer Journey Analytics.

Identitätsdaten können mithilfe der `identityMap` von XDM erweitert werden, um benutzerdefinierte IDs und mehrere Namespaces zu unterstützen. Adobe empfiehlt die Verwendung des Adobe Experience Cloud ID-Service als primäre Kennung für Analytics sowie die Verwendung anderer Identitätsverwaltungsoptionen für erweiterte Szenarien.

Da der Besucher-ID-Dienst nativ in die Tag-Erweiterung eingebettet ist, müssen Sie nur **[!UICONTROL Edge Domain]** auf den gewünschten Wert setzen. Wenn dieses Feld richtig festgelegt ist, funktioniert die Besucheridentifizierung ohne zusätzliche Konfiguration.

>[!NOTE]
>
>Schließen Sie die Tag-Erweiterung „Visitor ID Service“ nicht ein, wenn Sie die Tag-Erweiterung „Web SDK&quot; verwenden. Die Tag-Erweiterung „Visitor ID Service“ ist nur erforderlich, wenn Sie die Erweiterung [Adobe Analytics verwenden](analytics-extension.md).
