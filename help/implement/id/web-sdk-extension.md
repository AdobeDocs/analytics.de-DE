---
title: Besucheridentifizierung mit der Tag-Erweiterung „Web SDK"
description: Identifizieren Sie Besuchende beim Implementieren der Tag-Erweiterung „Web SDK" korrekt.
source-git-commit: 3055a76f797438be71e82ea8f73800dc82ff4805
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# Besucheridentifizierung mit der Tag-Erweiterung „Web SDK&quot;

Die Web SDK-Tag-Erweiterung in der Adobe Experience Platform-Datenerfassung ermöglicht Unternehmen die Implementierung der Web-SDK über eine Tag-Management-Oberfläche. Erweiterte Szenarien wie Domain-übergreifende ID-Freigabe und Migration von Besucherprofilen können durch Erweiterungsregeln und Aktionen einfach konfiguriert werden. Durch die Verwendung von Web SDK ist Ihre Implementierung zukunftssicher und unterstützt nahtlose Upgrades auf Customer Journey Analytics.

Da der Besucher-ID-Dienst nativ in die Tag-Erweiterung eingebettet ist, müssen Sie nur **[!UICONTROL Edge Domain]** auf den gewünschten Wert setzen. Wenn dieses Feld richtig festgelegt ist, funktioniert die Besucheridentifizierung ohne zusätzliche Konfiguration.

>[!NOTE]
>
>Schließen Sie die Tag-Erweiterung „Visitor ID Service“ nicht ein, wenn Sie die Tag-Erweiterung „Web SDK&quot; verwenden. Die Tag-Erweiterung „Visitor ID Service“ ist nur erforderlich, wenn Sie die Erweiterung [Adobe Analytics verwenden](analytics-extension.md).
