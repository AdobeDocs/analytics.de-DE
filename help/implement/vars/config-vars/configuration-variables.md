---
title: Konfigurationsvariablen
description: Verwenden Sie Konfigurationsvariablen, um festzustellen, wie Daten erfasst werden.
feature: Appmeasurement Implementation
exl-id: 3f017a94-b71d-47da-8ab4-daf32475ed34
role: Admin, Developer
TQID: https://experienceleague.adobe.com/amtLWIgyADqWBOv38xdJ6AF4IjhJ0aGVrvYqXLckfkI
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: c069c44e-5426-4c1a-accc-8028662f2fde
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: a947d2d7f45d4155a61cbfe0f8110851cca32e60
workflow-type: tm+mt
source-wordcount: 383
ht-degree: 19%

---

# Übersicht über Konfigurationsvariablen

Konfigurationsvariablen bestimmen darüber, wie Daten bei der Berichterstellung erfasst und verarbeitet werden. Sie enthalten normalerweise keine Dimensions- oder Metrikwerte.

## Festlegen von Konfigurationsvariablen

Bei Implementierungen, die die Web SDK-Erweiterung oder Analytics-Erweiterung verwenden, befinden sich Konfigurationsvariablen normalerweise in den Einstellungen der Erweiterung:

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [&#128279;](https://experience.adobe.com/data-collection) Adobe Experience Platform-Datenerfassung an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Klicken Sie auf [!UICONTROL Erweiterungen] und dann unter der Erweiterung auf [!UICONTROL Konfigurieren].

Bei JavaScript-Implementierungen mit `AppMeasurement.js` werden die Konfigurationsvariablen normalerweise oben in der JS-Datei festgelegt.

>[!IMPORTANT]
>
>Stellen Sie sicher, dass alle Konfigurationsvariablen festgelegt sind, bevor Sie eine Tracking-Methode aufrufen ([`t()`](../functions/t-method.md) oder [`tl()`](../functions/tl-method.md)). Vermeiden Sie das Festlegen von Konfigurationsvariablen in der [`doPlugins()`](../functions/doplugins.md)-Funktion.

## Eingestellte Konfigurationsvariablen

Die folgenden Konfigurationsvariablen werden eingestellt. Sie werden hier als Referenz dokumentiert, wenn Sie sie in einer Legacy-Implementierung feststellen.

* **`account`**: Die Report Suite ermittelt, an die Daten gesendet wurden. Die Report Suite wird jetzt durch die Instanziierung von Tracking-Objekten (die [`s_gi()`](../functions/s-gi.md)-Methode) verarbeitet. Verwenden Sie die [`s.sa()`](../functions/sa-method.md)-Methode, wenn Sie die Report Suite nach der Instanziierung des Tracking-Objekts ändern müssen.
* **`cookieDomain`**: Die Domain bestimmt, in der AppMeasurement Cookies setzt. Aktuelle Versionen von AppMeasurement erkennen automatisch die richtige Cookie-Domain, wodurch diese Variable überholt ist.
* **`cookieDomainPeriods`**: Hilft AppMeasurement zu bestimmen, wo Cookies gespeichert werden sollen, wenn eine Domain mehrere Punkte enthält. Aktuelle Versionen von AppMeasurement erkennen automatisch die richtige Domain, sodass diese Variable veraltet ist.
* **`fpCookieDomainPeriods`**: Die Erstanbieter-Entsprechung von `cookieDomainPeriods`, mit der Cookies an der richtigen Stelle gesetzt werden, wenn das Suffix einer Erstanbieter-Domain einen zusätzlichen Punkt enthielt (z. B. `example.co.uk`). Aktuelle Versionen von AppMeasurement erkennen automatisch die richtige Domain, sodass diese Variable veraltet ist.
* **`trackingServer`**: Gibt die Domain an, die zum Senden von Daten an Adobe über HTTP verwendet wird. Sie wird zugunsten einer sicheren Datenerfassung über HTTPS nicht mehr unterstützt. Verwenden Sie stattdessen [`trackingServerSecure`](trackingserversecure.md).
* **`trackInlineStats`**: Frühere Versionen von [Activity Map aktiviert oder deaktiviert](/help/analyze/activity-map/overview.md).
* **`visitorMigrationKey`**: Schlüssel für die Migration von Besuchern von Drittanbieter-Cookies zu Erstanbieter-Cookies. Sie wird eingestellt, da moderne Bibliotheken ein First-Party-Ausweich-Cookie (`fid`) setzen und zur Identitätsfindung auf den Besucher-ID-Service angewiesen sind.
* **`visitorMigrationServer`**: Gibt den Server an, der während der Migration von Drittanbieter- zu Erstanbieter-Cookies verwendet wird.
* **`visitorMigrationServerSecure`**: Das HTTPS-Äquivalent von `visitorMigrationServer`.
* **`visitorNameSpace`**: Hilft bei der Bestimmung der Drittanbieter-Cookie-Domain. Sie wird zugunsten der Verwendung der [`trackingServerSecure`](trackingserversecure.md)-Variablen für Implementierungen außer Kraft gesetzt, die den Besucher-ID-Service nicht verwenden.
