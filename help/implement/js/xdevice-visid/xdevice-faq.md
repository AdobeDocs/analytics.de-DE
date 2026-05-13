---
title: Häufig gestellte Fragen zur geräteübergreifenden Besucheridentifizierung
description: Häufig gestellte Fragen zur geräteübergreifenden Besucheridentifizierung
feature: Implementation Basics
exl-id: da972fee-fe6e-45b2-af01-50674989c375
role: Developer
TQID: https://experienceleague.adobe.com/h3kyR8lnSdl5rQKj9kmVXBt6rspjsALfUUaEh2-cAhM
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 204
ht-degree: 80%

---

# Häufig gestellte Fragen zur geräteübergreifenden Besucheridentifizierung

Häufig gestellte Fragen zur geräteübergreifenden Besucheridentifizierung.

+++Was ist der Unterschied zwischen geräteübergreifender Besucheridentifizierung und geräteübergreifender Analyse?
Bei der geräteübergreifenden Besucheridentifizierung wird die `visitorID`-Variable verwendet, um Geräte miteinander zu verbinden. Dabei gibt es einige wesentliche Einschränkungen. Eine der größten Einschränkungen dieser Identifizierungsmethode besteht darin, dass nicht authentifizierte Treffer isoliert werden, es sei denn, das Gerät wurde bereits erkannt. Diese nicht authentifizierten Treffer können die Zahl der Unique Visitors überhöhen.

Cross-Device Analytics ist die neueste Methode zur geräteübergreifenden Besucheridentifizierung von Adobe. Dabei werden der Experience Cloud ID-Service und das feldbasierte Stitching verwendet, um Besuche von verschiedenen Geräten rückwirkend zusammenzufügen. CDA erfordert die Verwendung der `setCustomerIDs`-Funktion, um zu ermitteln, welche Geräte von demselben Besucher verwendet werden.
+++

+++Wie behandelt die geräteübergreifende Besucheridentifizierung Segmente?
Die geräteübergreifende Besucheridentifizierung behandelt Segmente ähnlich wie andere Funktionen. Sie prüft jeden einzelnen Treffer, um zu sehen, ob er mit den Segmentkriterien übereinstimmt, und schließt diese Treffer in Ihre Daten ein, wenn sie übereinstimmen. Segmente, die besuchs- und besucherbasierte Behälter verwenden, betrachten weiterhin die Besucher-ID. Stellen Sie sicher, dass Ihre Implementierung nach Möglichkeit immer die Variable `visitorID` verwendet, um Unique Visitors für die Segmentierung konsistent zu identifizieren.
+++
