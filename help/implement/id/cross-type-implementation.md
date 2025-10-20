---
title: Tracking über verschiedene Implementierungstypen hinweg
description: Verwenden Sie unterschiedliche Implementierungstypen und verfolgen Sie Besucher nahtlos zwischen ihnen.
exl-id: 18aa5595-d2a7-4df2-a4ef-a5040c097483
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: 779ba5b0a1d71467aaaf3872fd707cc323ae8af2
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 59%

---

# Tracking über verschiedene Implementierungstypen hinweg

Die Hauptarchitektur einer Adobe Analytics-Implementierung ist über alle Implementierungstypen hinweg konsistent. Der Prozess umfasst die Definition von Variablen und die Kompilierung in eine Bildanforderung, die an die Datenerfassungs-Server von Adobe gesendet wird. Mit diesem Konzept können Sie nahtlos zwischen AppMeasurement, dem Web SDK und den entsprechenden Erweiterungen in der Adobe Experience Platform-Datenerfassung über verschiedene Seiten derselben Site hinweg wechseln.

Adobe empfiehlt, die Konsistenz der Implementierung einer Site zu wahren, indem auf allen Seiten derselbe Implementierungstyp verwendet wird. Wenn jedoch Teile Ihrer Site unterschiedliche Anforderungen haben, können Sie diese Seite verwenden, um sicherzustellen, dass Besucherinnen und Besucher konsistent zwischen Seiten verfolgt werden.

Wenn Sie mehr als einen Implementierungstyp verwenden (z. B. AppMeasurement und hartcodierte Bildanforderungen), stellen Sie sicher, dass die folgenden Variablen korrekt festgelegt sind und miteinander übereinstimmen.

>[!NOTE]
>
>Alle Implementierungstypen müssen denselben Besucheridentifizierungstyp verwenden (veraltete Analytics-ID oder Besucher-ID-Service). Adobe empfiehlt, nach Möglichkeit den Besucher-ID-Service in allen Implementierungen zu verwenden.

| Variable | AppMeasurement | Analytics-Erweiterung | Web SDK (Legierung) | Web SDK-Tag-Erweiterung | Fest programmierte Bildanforderung |
| --- | --- | --- | --- | --- | --- |
| Report Suite-ID | Zeichenfolgenargument in [`s_gi`](../vars/functions/s-gi.md) | [!UICONTROL Report Suites] im Abschnitt [!UICONTROL Bibliotheksverwaltung] beim [Konfigurieren der Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html?lang=de) | Hinzufügen von Adobe Analytics als Dienst beim [Konfigurieren eines Datenstroms](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=de) | Hinzufügen von Adobe Analytics als Dienst beim [Konfigurieren eines Datenstroms](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=de) | Teil des `pathname` der URL (nach `/b/ss/`) |
| ID-Service von Experience Cloud | Implementierung [`VisitorAPI.js`](appmeasurement.md) | Verwenden Sie die [Experience Cloud ID Service-Erweiterung](analytics-extension.md) | [Nativ enthalten](alloy.md) | [Nativ enthalten](web-sdk-extension.md) | Führen Sie einen [separaten Aufruf an den ID-Service](https://experienceleague.adobe.com/docs/id-service/using/implementation/direct-integration.html?lang=de) aus, um die gewünschte ID abzurufen und die `mid` in die Abfragezeichenfolge aufzunehmen |
| Edge-Domain | Die [`trackingServerSecure`](../vars/config-vars/trackingserversecure.md) Variable | [!UICONTROL SSL-Tracking] im Abschnitt [!UICONTROL Allgemein] beim [Konfigurieren der Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html?lang=de) | Die Eigenschaft `edgeDomain` beim [Konfigurieren des Web-SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=de) | Das Feld [!UICONTROL Edge Domain] beim [Konfigurieren der Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html?lang=de) | Der `hostname` der Bildanfrage-URL |

Wenn eine dieser Variablen nicht für jeden Implementierungstyp konsistent ist, kann Adobe sie als separate Besuchende betrachten. Wenn Besucherinnen und Besucher nicht nahtlos über Implementierungstypen auf Ihrer Site hinweg verfolgt werden, besteht der häufigste Grund darin, dass der ID-Service falsch konfiguriert ist. Stellen Sie sicher, dass jeder Implementierungstyp auf Ihrer Site korrekt dieselbe Experience Cloud ID (`mid`) erhält.
