---
title: Gerätediagramm
description: Machen Sie sich mit den Voraussetzungen und Einschränkungen der Datenzuordnung mithilfe des Gerätediagramms vertraut.
exl-id: b8408a7d-6aff-4fff-b535-f10d422bcf0d
feature: CDA
role: Admin
source-git-commit: cc0b8703d6b6488adf9a2ea41a51001538d1cbee
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 60%

---


# Gerätediagramm

{{available-existing-customers}}

Die geräteübergreifende Analyse kann das private Diagramm verwenden, um Daten miteinander zu verknüpfen. Das private Diagramm ist ein Repository mit gehashten Geräte-IDs, das speziell für Ihre Organisation gilt. Die geräteübergreifende Analyse kommuniziert regelmäßig mit dem Gerätediagramm, um Geräte miteinander zu verknüpfen.

## Besondere Voraussetzungen für das Gerätediagramm

Wenn Sie die geräteübergreifende Analyse mithilfe der Gerätediagrammmethode implementieren möchten, ist Folgendes erforderlich. Arbeiten Sie mit Teams in Ihrem Unternehmen und Ihrem Adobe-Account-Team zusammen, um sicherzustellen, dass Sie alle folgenden Voraussetzungen erfüllen.

>[!WARNING]
>
>Wenn nicht alle Voraussetzungen erfüllt sind, ist die Aktivierung der geräteübergreifenden Analyse unter Umständen nicht möglich oder die Ergebnisse bei der Datenzuordnung sind schlecht.
>

* Alle auf der [Übersichtsseite](overview.md) aufgeführten Voraussetzungen.
* Ihr Unternehmen muss das private Diagramm [Adobe Experience Platform Identity Service verwenden](https://business.adobe.com/products/experience-platform/identity-service.html). Siehe auch [Startseite](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=de) im Identity Service-Benutzerhandbuch.
* Ihre Implementierung muss die neueste Version des Experience Cloud-ID-Service (ECID) verwenden. Siehe die [Startseite](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de) im Benutzerhandbuch für den ID-Service. Bei den meisten Implementierungen mit [Tags](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=de) in Adobe Experience Platform ist der ID-Service wahrscheinlich bereits bereitgestellt.
* Ihre Implementierung muss die `setCustomerIDs`-Funktion (oder das SDK-Äquivalent) immer dann aufrufen, wenn eine Person identifiziert werden kann, z. B. wenn sich ein Benutzer anmeldet oder eine E-Mail öffnet. Diese Anforderung gilt für alle Plattformen, einschließlich mobiler Apps, wenn sie verwendet werden. Siehe [`setCustomerIDs`](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/methods/setcustomerids.html?lang=de) im ID-Service-Benutzerhandbuch.

## Besondere Einschränkungen für das Gerätediagramm

* Veraltete Analytics-IDs werden nicht unterstützt. Nur Besucher mit Experience Cloud IDs werden zugeordnet.
* Wenn Ihr Unternehmen ein privates Diagramm verwendet, dauert es bis zu 24 Stunden, bis neue Geräte zugeordnet werden.
* Gerätediagramme von Drittanbietern werden nicht unterstützt.

## Nächste Schritte

Sobald Ihre Organisation alle Anforderungen erfüllt und die Einschränkungen versteht, können Sie mit der [Einrichtung der geräteübergreifenden Analyse](setup.md) beginnen.
