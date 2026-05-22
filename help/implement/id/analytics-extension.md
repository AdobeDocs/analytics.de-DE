---
title: Besucheridentifizierung mit der Tag-Erweiterung "Adobe Analytics"
description: Identifizieren Sie Besuchende beim Implementieren der Adobe Analytics-Tag-Erweiterung korrekt.
exl-id: de534c69-0f43-45eb-86da-20d3cd3f363d
TQID: 'https://experienceleague.adobe.com/i38Vo-39aUwJOp3HoS-bb2jqwSSV0oqeR0lkjOJqcgs'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: e4f5f438-eabb-4c54-9133-b817e3d125f5
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 301a0341e725ca15f1700046528ea5f42969add4
workflow-type: tm+mt
source-wordcount: 499
ht-degree: 2%

---

# Besucheridentifizierung mit der Tag-Erweiterung &quot;Adobe Analytics&quot;

Die Tag-Erweiterung von Adobe Analytics bietet die Möglichkeit, AppMeasurement mithilfe einer Tag-Management-Oberfläche zu implementieren. Da es sich bei dieser Tag-Erweiterung im Wesentlichen um AppMeasurement handelt, bietet sie ähnliche Methoden zum Identifizieren von Besuchern und erfordert eine separate Tag-Erweiterung für den Besucher-ID-Service.

## Identifizieren von Besuchern mithilfe des Besucher-ID-Service (empfohlen)

Um den Besucher-ID-Dienst mit der Adobe Analytics-Tag-Erweiterung zu verwenden, fügen Sie die Tag-Erweiterung &quot;Experience Cloud ID Service“ in Ihre Tag-Eigenschaft ein.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [&#128279;](https://experience.adobe.com)Adobe CX Enterprise an.
1. Navigieren Sie **[!UICONTROL Datenerfassung]** > **[!UICONTROL Tags]**.
1. Suchen Sie die gewünschte Tag-Eigenschaft.
1. Navigieren Sie zu **[!UICONTROL Erweiterungen]** und wählen Sie dann die Registerkarte **[!UICONTROL Katalog]** aus.
1. Suchen Sie nach der Erweiterung **[!UICONTROL Experience Cloud ID Service]** und wählen Sie **[!UICONTROL Installieren]** aus.

Die Tag-Erweiterung ruft automatisch Ihre IMS-Organisations-ID ab, sodass keine zusätzliche Konfiguration erforderlich ist.

## Identifizieren von Besuchern mithilfe des `s_vi`-Cookies (nicht empfohlen)

>[!IMPORTANT]
>
>Adobe rät davon ab, diese Methode zur Besucheridentifizierung zu verwenden.

Wenn Ihr Unternehmen die Tag-Erweiterung „Visitor ID Service“ nicht verwendet, verwendet die Tag-Erweiterung von Adobe Analytics eine eigene Form der Besucheridentifizierung. Wenn ein Besucher zum ersten Mal auf Ihre Site gelangt, sucht die Erweiterung nach einem [`s_vi`](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/cookies/analytics) Cookie. Dieses Cookie wird bei der Konfiguration der Tag **[!UICONTROL Erweiterung auf die Domain gesetzt, die mit SSL-Tracking-Server]** (für HTTPS) oder **[!UICONTROL Tracking-Server]** (für HTTP[&#x200B; übereinstimmt](https://experienceleague.adobe.com/de/docs/experience-platform/tags/extensions/client/analytics/overview).

* Wenn Sie am [Programm für verwaltete Zertifikate](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/adobe-managed-cert) teilnehmen, ist Ihr Tracking-Server normalerweise eine Erstanbieter-Domain, die `s_vi`-Cookies als Erstanbieter verwendet.
* Wenn Sie nicht am Programm für verwaltete Zertifikate teilnehmen, ist der Tracking-Server normalerweise eine Subdomain von `adobedc.net`, `omtrdc.net` oder `2o7.net`, wodurch das `s_vi`-Cookie zu einem Drittanbieter-Cookie wird. Aufgrund der modernen Datenschutzstandards von Browsern werden Drittanbieter-Cookies von den meisten Browsern abgelehnt. Nach der Ablehnung versucht AppMeasurement stattdessen, ein First-Party-Ausweich-Cookie (`fid`) festzulegen.

Wenn Sie [!UICONTROL SSL-Tracking-Server] richtig eingestellt haben, sind keine weiteren Maßnahmen zur Besucheridentifizierung erforderlich.

## Besucheridentifizierung mit `visitorID` (nicht empfohlen)

>[!IMPORTANT]
>
>Adobe rät davon ab, diese Methode zur Besucheridentifizierung zu verwenden.

Die Verwendung der **[!UICONTROL Besucher-ID]**-Variablen ermöglicht Ihrem Unternehmen die vollständige unabhängige Kontrolle bei der Identifizierung von Besuchern. Wenn Sie [!UICONTROL Besucher-ID] mithilfe eines Datenelements festlegen, beachten Sie die folgenden Einschränkungen:

* Jeder Treffer muss denselben Wert [!UICONTROL Besucher-ID] enthalten, damit er als einzelner Besucher gezählt wird.
   * Bei Treffern, bei denen das [!UICONTROL Besucher-ID]-Datenelement ausgelassen wird, wird automatisch versucht, eine andere Besucheridentifizierungsmethode zu verwenden, wobei sie als separater Besucher behandelt werden.
   * Treffer, die einen anderen [!UICONTROL Besucher-ID]-Wert als ein vorheriger Treffer enthalten, werden als separater Besucher behandelt.
   * Adobe bietet keine Möglichkeit, Treffer mithilfe verschiedener Besucher-IDs in Adobe Analytics zusammenzufügen.
* Freigegebene Zielgruppen, Analytics for Target und Kundenattribute werden nicht für Besucher unterstützt, die mit der [!UICONTROL Besucher-ID] identifiziert wurden.

Siehe [`visitorID`](/help/implement/vars/config-vars/visitorid.md) für Implementierungsanweisungen unter Verwendung dieser Variablen.
