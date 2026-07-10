---
title: Besucheridentifizierung mit der Tag-Erweiterung „Web SDK"
description: Identifizieren Sie Besuchende beim Implementieren der Tag-Erweiterung „Web SDK" korrekt.
exl-id: 65de7fc3-a344-4f04-b523-1f5edf681d2f
TQID: 'https://experienceleague.adobe.com/4PVDioBDa-1VXg9Fpy0wA8-RZZYSXzVijj-b2kdEALQ'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
subfeature_v2: id: b3e5f43e-2e2f-43c0-810a-044a5f91e31a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d00e9f03-e50b-4162-b143-0c0817c937c2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: a947d2d7f45d4155a61cbfe0f8110851cca32e60
workflow-type: tm+mt
source-wordcount: 197
ht-degree: 0%

---

# Besucheridentifizierung mit der Tag-Erweiterung „Web SDK&quot;

Die Web SDK-Tag-Erweiterung in der Adobe Experience Platform-Datenerfassung ermöglicht Unternehmen die Implementierung der Web-SDK über eine Tag-Management-Oberfläche. Erweiterte Szenarien wie Domain-übergreifende ID-Freigabe und Migration von Besucherprofilen können durch Erweiterungsregeln und Aktionen einfach konfiguriert werden. Durch die Verwendung von Web SDK ist Ihre Implementierung zukunftssicher und unterstützt ein nahtloses Upgrade auf Customer Journey Analytics.

Identitätsdaten können mithilfe der [`identityMap`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/identity/identity-map) von XDM erweitert werden, um benutzerdefinierte IDs und mehrere Namespaces zu unterstützen. Adobe empfiehlt die Verwendung von ECID als primäre Kennung für Analytics sowie die Verwendung anderer Identitätsverwaltungsoptionen für erweiterte Szenarien.

Da der Besucher-ID-Dienst nativ in die Tag-Erweiterung eingebettet ist, müssen Sie nur **[!UICONTROL Edge Domain]** auf den gewünschten Wert setzen. Wenn dieses Feld richtig festgelegt ist, funktioniert die Besucheridentifizierung ohne zusätzliche Konfiguration.

>[!NOTE]
>
>Schließen Sie die Tag-Erweiterung „Visitor ID Service“ nicht ein, wenn Sie die Tag-Erweiterung „Web SDK&quot; verwenden. Die Tag-Erweiterung „Visitor ID Service“ ist nur erforderlich, wenn Sie die Erweiterung [Adobe Analytics verwenden](analytics-extension.md).
