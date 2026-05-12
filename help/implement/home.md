---
title: Implementieren von Adobe Analytics
description: Implementieren Sie Adobe Analytics für Ihre Website, Eigenschaft oder Anwendung.
feature: Implementation Basics
exl-id: 2b629369-2d69-4dc6-861a-ff21a46d39e0
role: Admin, Developer, Leader, User
TQID: https://experienceleague.adobe.com/c1TZC9k-mu1n95Oq3jhQOvcBXFwx8oK28plhoNcJDK4
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2:
  - id: c77ba355-6681-41fe-b719-563d3f507fdb
  - id: c8add8f2-4250-4fd9-9cde-9707036c567d
  - id: df312454-73c4-43f6-a90e-18f5043f074c
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 197233b18a57ac67d4b56ddd34f296d88dd9c4b2
workflow-type: tm+mt
source-wordcount: 814
ht-degree: 83%

---

# Implementieren von Adobe Analytics

![Banner](../../assets/doc_banner_implement.png)

Adobe Analytics benötigt Code in Ihrer Website, App oder anderen Anwendung, um Daten an die Datenerfassungs-Server zu senden. Abhängig von der Plattform und den Anforderungen Ihres Unternehmens gibt es verschiedene Methoden, um diesen Code zu implementieren.

## Website-Implementierungsmethoden

Für Ihre **Website** sind die folgenden Implementierungsmethoden verfügbar:

### Client-seitig

* **Web SDK-Erweiterung**: Die standardisierte und empfohlene Methode zur Implementierung von Adobe Analytics für neue Kundinnen und Kunden. Fügen Sie die **Adobe Experience Platform Web SDK-Erweiterung** in den **Datenerfassungs-Tags** der Adobe Experience Platform hinzu und platzieren Sie dann ein Loader-Tag auf jeder Seite. Das Tag sendet Daten an das Adobe Experience Platform **Edge Network**, das diese Daten an Adobe Analytics weiterleitet.
  ![Web SDK-Erweiterung](./assets/websdk-extension-implementation.png)
Siehe [Implementieren von Adobe Analytics mit der Adobe Experience Platform Web SDK-Erweiterung.](./aep-edge/overview.md) in der Dokumentation.

* **Web SDK**: Wenn Sie nicht die Datenerfassung von Adobe Experience Platform verwenden möchten, können Sie die Web SDK-Bibliotheken auch manuell auf Ihre Site laden. Verweisen Sie auf jeder Seite auf die Web SDK-Bibliothek (`alloy.js`) und senden Sie die gewünschten Tracking-Aufrufe an das Adobe Experience Platform **Edge Network** in einem für Ihre Organisation geeigneten Format. Das Edge Network leitet die Daten an Adobe Analytics weiter.
  ![Web-SDK](./assets/websdk-implementation.png)
Weitere Informationen finden [&#x200B; unter „Implementieren von Adobe Analytics mit der Adobe Experience Platform Web](./aep-edge/overview.md)SDK&quot;.

* **Analytics-Erweiterung**: Fügen Sie die **Adobe Analytics-Erweiterung** in den **Datenerfassungs-Tags** von Adobe Experience Platform hinzu und platzieren Sie dann ein Loader-Tag auf jeder Seite. Das Tag sendet Daten direkt an Adobe Analytics. Nutzen Sie diese Implementierungsmethode, wenn Sie Tags, aber nicht die Edge Network-Infrastruktur verwenden möchten.
  ![Adobe Analytics-Erweiterung](./assets/analytics-extension-implementation.png)
Weitere Informationen finden [&#x200B; unter „Implementieren von Adobe Analytics mit &#x200B;](launch/overview.md) Analytics-Erweiterung“.

* **Legacy-JavaScript**: Die frühere manuelle Methode zur Implementierung von Adobe Analytics. Verweisen Sie auf jeder Seite auf die AppMeasurement-Bibliothek (`AppMeasurement.js`) und stellen Sie dann die Variablen und Einstellungen in JavaScript ein.
  ![Implementieren von Adobe Analytics mit Legacy-JavaScript](./assets/appmeasurement-implementation.png)
Diese Implementierungsmethode kann für Implementierungen mit benutzerdefiniertem Code nützlich sein und eignet sich ideal für Implementierungstypen, die an anderer Stelle nicht angeboten werden, z. B. für [AMP-Seiten](other/amp.md).

Das folgende Entscheidungsschema kann Ihnen bei der Auswahl einer Client-seitigen Implementierungsmethode helfen:

![Ein Entscheidungsbaum zur Auswahl einer Implementierungsmethode, wie in diesem Abschnitt beschrieben.](./assets/decision-tree.png)


>[!TIP]
>
>Wenden Sie sich an das Adobe-Accountteam, um Hinweise und Best Practices zu erhalten, die Ihnen bei der Entscheidung helfen können, welche Implementierung Sie in Ihrer aktuellen Situation wählen sollten.

### Server-seitig

Zur Server-seitigen Implementierung von Adobe Analytics stehen Ihnen die folgenden Optionen zur Verfügung:

* **Edge Network-API**: Sie implementieren Code auf dem Server, der das Adobe Experience Platform Edge Network-API verwendet, um über einen Datenstrom mit Adobe Analytics zu kommunizieren.
  ![Server-seitige Implementierung](assets/edge-network-server-api.png)
Weitere Informationen finden [&#x200B; unter „Implementieren von Adobe Analytics mit der Adobe Experience Platform](/help/implement/aep-edge/api/overview.md)Edge Network-API“.

* **(Bulk) Data Insertion-API**: Sie verwenden die (Bulk) Data Insertion-API von Adobe Analytics, um Daten Server-seitig direkt in Adobe Analytics zu erfassen.
  ![Dateneinfüge-APIs](assets/analytics-apis.png)
Weitere Informationen finden [&#x200B; unter &#x200B;](../import/c-data-insertion-api/c-data-insertion-api.md)Dateneinfüge-API“.

## Implementierungsmethoden für Mobile Apps

Für Ihre **Mobile App** sind die folgenden Implementierungsmethoden verfügbar:

* **Mobile SDK-Erweiterung**: Die standardisierte und empfohlene Methode zur Implementierung von Adobe Analytics in Ihrer App. Verwenden Sie spezifische Bibliotheken, um Daten aus Ihrer App ganz einfach an Adobe zu senden. Fügen Sie die **Adobe Experience Platform Mobile SDK-Erweiterung** in den **Datenerfassungs-Tags** von Adobe Experience Platform hinzu und implementieren Sie dann die Mobile SDK-Bibliothek in Ihre App. Sie können das SDK verwenden, um Bibliotheken zu importieren, Erweiterungen zu registrieren und die Tag-Konfiguration zu laden. Senden Sie Daten an das Adobe Experience Platform **Edge Network**. Edge leitet diese Daten dann an Adobe Analytics weiter.
  ![Mobile SDK-Erweiterung](./assets/mobilesdk-extension.png)

  Weitere Informationen finden Sie im Artikel [Implementieren von Adobe Analytics mit dem Adobe Experience Platform Mobile SDK](../implement/aep-edge/mobile-sdk/overview.md).

* **Analytics-Erweiterung**: Fügen Sie die **Adobe Analytics-Erweiterung** in den **Datenerfassungs-Tags** von Adobe Experience Platform hinzu und implementieren Sie die Mobile SDK-Bibliothek in Ihre App. Sie können das SDK verwenden, um Bibliotheken zu importieren, Erweiterungen zu registrieren und die Tag-Konfiguration zu laden. Diese Implementierungsmethode sendet Daten direkt an Adobe Analytics. Verwenden Sie diese Implementierungsmethode, wenn Sie den Komfort der Adobe Experience Platform-Datenerfassung wünschen, aber nicht die Netzwerkinfrastruktur von Adobe Experience Platform Edge nutzen möchten.
  ![Analytics-Erweiterung](./assets/mobilesdk-analytics-extension.png)

  Weitere Informationen finden Sie unter [Implementieren von Adobe Analytics mit der Analytics-Erweiterung](../implement/aep-edge/mobile-sdk/overview.md).


>[!CAUTION]
>
>Informationen zur Unterstützung älterer Versionen von Adobe Mobile SDKs finden Sie unter [Mitteilungen zum Ende der Unterstützung für SDKs](https://developer.adobe.com/client-sdks/resources/sdks-end-of-support/).

## Wichtige Artikel zur Analytics-Implementierung

* [Übernahme einer bestehenden Adobe Analytics-Implementierung](/help/implement/prepare/existing-implementation.md)
* [Adobe Debugger](validate/debugger.md)
* [Erstellen einer Tag-Eigenschaft in Experience Platform](launch/create-analytics-property.md)
* [AppMeasurement-Aktualisierungen](appmeasurement-updates.md)
* [Tutorial zum Einrichten von Adobe Analytics mit Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/applications-setup/setup-analytics.html?lang=de)
* [Tutorial zur Implementierung von Adobe Experience Cloud in Mobile Apps](https://experienceleague.adobe.com/docs/platform-learn/implement-mobile-sdk/overview.html?lang=de)


## Wichtige Analytics-Ressourcen

* [Kundenunterstützung kontaktieren](https://experienceleague.adobe.com/de?support-solution=Analytics&lang=de#support)
* [Adobe Analytics-Community in Experience League](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics/ct-p/adobe-analytics-community?profile.language=de)
* [Adobe Analytics-Ressourcen](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/adobe-analytics-resources/m-p/276666?profile.language=de)
* [Neueste Versionshinweise](../release-notes/latest.md)
