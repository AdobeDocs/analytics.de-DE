---
description: Mithilfe der geräteübergreifenden Identifizierung erkennen Sie Ihre Besucher auch auf anderen Geräten wieder.
keywords: Analytics-Implementierung
subtopic: Visitors
title: Benutzer geräteübergreifend verbinden
feature: Implementation Basics
exl-id: dfe278db-01de-4bba-b07a-66d52de1dbe2
role: Developer
TQID: 'https://experienceleague.adobe.com/t4NC8Wdgldm6iFgdJ5EtrU13kOnUBuEGKhWnKExf614'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: df312454-73c4-43f6-a90e-18f5043f074c
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 389
ht-degree: 94%

---

# Benutzer geräteübergreifend verbinden

>[!IMPORTANT]
>
>Diese Methode zur geräteübergreifenden Identifizierung von Besuchern wird nicht mehr empfohlen. Weitere Informationen finden Sie unter [Cross-Device Analytics](/help/components/cda/overview.md) im Benutzerhandbuch zu den Komponenten.

Mithilfe der geräteübergreifenden Identifizierung erkennen Sie Ihre Besucher auch auf anderen Geräten wieder. Bei der geräteübergreifende Besucheridentifizierung werden Benutzer mithilfe der `visitorID`-Variablen geräteübergreifend zugeordnet. Die `visitorID`-Variable hat bei der Identifizierung von Unique Visitors die höchste Priorität.

Wenn Sie einen Treffer mit einer benutzerdefinierten Besucher-ID senden, sucht Adobe nach Besucherprofilen mit einer übereinstimmenden Besucher-ID. Existiert ein solches Profil, wird ab diesem Punkt das bereits im System vorhandene Besucherprofil genutzt und das vorherige Besucherprofil wird nicht mehr eingesetzt.

Die `visitorID`-Variable wird für gewöhnlich festgelegt, nachdem sich ein Besucher authentifiziert hat oder eine andere Aktion durchgeführt hat, an der er – unabhängig davon, welches Gerät er verwendet hat – identifiziert werden kann. Zu den wirksamen Kennungen gehören ein Hash ihres Benutzernamens, ihrer E-Mail-Adresse oder einer internen ID, die keine persönlichen Informationen enthält.

Nachdem sich der Kunde von jedem Gerät aus angemeldet hat, sind alle an dasselbe Benutzerprofil gebunden. Wenn sich der Besucher später auf einem Gerät abmeldet, gehört er weiterhin zum gleichen Besucherprofil, da Adobe erkennt, dass das Browser-Cookie auf jedem Gerät zum gleichen Besucherprofil gehört. Adobe empfiehlt, die `visitorID`-Variable wann immer möglich zu verwenden, falls das Browser-Cookie gelöscht wird.

## Einschränkungen

Die Verwendung eigener benutzerdefinierter Besucher-IDs gibt Ihnen mehr Kontrolle darüber, wie Besucher identifiziert werden, allerdings mit Einschränkungen.

* **Die Besucherdeduplizierung ist nicht rückwirkend**: Wenn ein Besucher Ihre Website zum ersten Mal aufruft und sich dann authentifiziert, werden zwei Unique Visitors gezählt. Ein Unique Visitor wird für die generische Analytics-ID gezählt, die automatisch generiert wird, und ein weiterer für die benutzerdefinierte Besucher-ID, wenn er sich anmeldet. Diese Duplizierung von Unique Visitors erfolgt immer dann, wenn ein Besucher ein neues Gerät verwendet oder seine Cookies löscht.
* **Inkompatibilität mit dem Experience Cloud ID-Dienst**: Seit der Einführung der geräteübergreifenden Besucheridentifizierung hat Adobe leistungsfähigere und zuverlässigere Methoden zum geräteübergreifenden Tracking von Besuchern eingeführt. Diese neuen Identifikationsmethoden sind nicht mit der Überschreibung der benutzerdefinierten Besucher-ID kompatibel. Wenn Sie beabsichtigen, den ID-Service oder die geräteübergreifende Analyse (Cross-Device Analytics, CDA) zu verwenden, empfiehlt Adobe dringend, nicht die `visitorID` Variable zu verwenden.
