---
title: Tracking über verschiedene Implementierungstypen hinweg
description: Verwenden Sie unterschiedliche Implementierungstypen und verfolgen Sie Besucher nahtlos zwischen ihnen.
exl-id: 18aa5595-d2a7-4df2-a4ef-a5040c097483
feature: Implementation Basics
role: Admin, Developer, Leader
TQID: https://experienceleague.adobe.com/FM6c33rpXxzy1huu8KE0VBkfe4FGIySczmVMrprFEUY
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2:
  - id: c069c44e-5426-4c1a-accc-8028662f2fde
  - id: df312454-73c4-43f6-a90e-18f5043f074c
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 444
ht-degree: 61%

---

# Tracking über verschiedene Implementierungstypen hinweg

Die Hauptarchitektur einer Adobe Analytics-Implementierung ist über alle Implementierungstypen hinweg konsistent. Der Prozess umfasst die Definition von Variablen und die Kompilierung in eine Bildanforderung, die an die Datenerfassungs-Server von Adobe gesendet wird. Mit diesem Konzept können Sie nahtlos zwischen AppMeasurement, dem Web SDK und den entsprechenden Erweiterungen in der Adobe Experience Platform-Datenerfassung über verschiedene Seiten derselben Site hinweg wechseln.

Adobe empfiehlt, die Konsistenz der Implementierung einer Site zu wahren, indem auf allen Seiten derselbe Implementierungstyp verwendet wird. Wenn jedoch Teile Ihrer Site unterschiedliche Anforderungen haben, können Sie diese Seite verwenden, um sicherzustellen, dass Besucherinnen und Besucher konsistent zwischen Seiten verfolgt werden.

Wenn Sie mehr als einen Implementierungstyp verwenden (z. B. AppMeasurement und hartcodierte Bildanforderungen), stellen Sie sicher, dass die folgenden Variablen korrekt festgelegt sind und miteinander übereinstimmen.

>[!NOTE]
>
>Alle Implementierungstypen müssen denselben Besucheridentifizierungstyp verwenden (veraltete Analytics-ID oder Besucher-ID-Service). Adobe empfiehlt, nach Möglichkeit den Besucher-ID-Service in allen Implementierungen zu verwenden.

| Variable | Web SDK-Tag-Erweiterung | Web SDK (Legierung) | Analytics-Erweiterung | AppMeasurement | Fest programmierte Bildanforderung |
|---|---|---|---|---|---|
| Report Suite-ID | Hinzufügen von Adobe Analytics als Dienst beim [Konfigurieren eines Datenstroms](https://experienceleague.adobe.com/de/docs/experience-platform/datastreams/configure) | Hinzufügen von Adobe Analytics als Dienst beim [Konfigurieren eines Datenstroms](https://experienceleague.adobe.com/de/docs/experience-platform/datastreams/configure) | [!UICONTROL Report Suites] im Abschnitt [!UICONTROL Bibliotheksverwaltung] beim [Konfigurieren der Erweiterung](https://experienceleague.adobe.com/de/docs/experience-platform/tags/extensions/client/analytics/overview) | Zeichenfolgenargument in [`s_gi`](../vars/functions/s-gi.md) | Teil des `pathname` der URL (nach `/b/ss/`) |
| ID-Service von Experience Cloud | [Nativ enthalten](web-sdk-extension.md) | [Nativ enthalten](alloy.md) | Verwenden Sie die [Experience Cloud ID Service-Erweiterung](analytics-extension.md) | Implementierung [`VisitorAPI.js`](appmeasurement.md) | Führen Sie einen [separaten Aufruf an den ID-Service](https://experienceleague.adobe.com/en/docs/id-service/using/implementation/direct-integration) aus, um die gewünschte ID abzurufen und die `mid` in die Abfragezeichenfolge aufzunehmen |
| Edge-Domain | Das Feld [!UICONTROL Edge Domain] beim [Konfigurieren der Erweiterung](https://experienceleague.adobe.com/de/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) | Die Eigenschaft `edgeDomain` beim [Konfigurieren des Web-SDK](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/overview) | [!UICONTROL SSL-Tracking] im Abschnitt [!UICONTROL Allgemein] beim [Konfigurieren der Erweiterung](https://experienceleague.adobe.com/de/docs/experience-platform/tags/extensions/client/analytics/overview) | Die [`trackingServerSecure`](../vars/config-vars/trackingserversecure.md) Variable | Der `hostname` der Bildanfrage-URL |

Wenn eine dieser Variablen nicht für jeden Implementierungstyp konsistent ist, werden sie von Adobe wahrscheinlich als separate Besucherinnen und Besucher betrachtet. Wenn Besucherinnen und Besucher nicht nahtlos über Implementierungstypen auf Ihrer Site hinweg verfolgt werden, besteht der häufigste Grund darin, dass der ID-Service falsch konfiguriert ist. Stellen Sie sicher, dass jeder Implementierungstyp auf Ihrer Site korrekt dieselbe Experience Cloud ID (`mid`) erhält.
