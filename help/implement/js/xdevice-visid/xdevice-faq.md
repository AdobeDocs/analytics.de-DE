---
title: Häufig gestellte Fragen zur geräteübergreifenden Besucheridentifizierung
description: Häufig gestellte Fragen zur geräteübergreifenden Besucheridentifizierung
feature: Implementation Basics
exl-id: da972fee-fe6e-45b2-af01-50674989c375
role: Developer
TQID: 'https://experienceleague.adobe.com/RBciiyfaq671zJ51QdJJDXcekFr-lfq0WPY0UAuWoVA'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: df312454-73c4-43f6-a90e-18f5043f074c
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
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
