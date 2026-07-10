---
title: Tracking über verschiedene Implementierungstypen hinweg
description: Verwenden Sie unterschiedliche Implementierungstypen und verfolgen Sie Besucher nahtlos zwischen ihnen.
exl-id: 18aa5595-d2a7-4df2-a4ef-a5040c097483
feature: Implementation Basics
role: Admin, Developer, Leader
TQID: https://experienceleague.adobe.com/FM6c33rpXxzy1huu8KE0VBkfe4FGIySczmVMrprFEUY
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7aid: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: c069c44e-5426-4c1a-accc-8028662f2fdeid: df312454-73c4-43f6-a90e-18f5043f074cid: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: a947d2d7f45d4155a61cbfe0f8110851cca32e60
workflow-type: tm+mt
source-wordcount: 612
ht-degree: 47%

---

# Tracking über verschiedene Implementierungstypen hinweg

Die Hauptarchitektur einer Adobe Analytics-Implementierung ist über alle Implementierungstypen hinweg konsistent. Der Prozess umfasst die Definition von Variablen und die Kompilierung in eine Bildanforderung, die an die Datenerfassungs-Server von Adobe gesendet wird. Mit diesem Konzept können Sie nahtlos zwischen AppMeasurement, dem Web SDK und den entsprechenden Erweiterungen in der Adobe Experience Platform-Datenerfassung über verschiedene Seiten derselben Site hinweg wechseln.

Adobe empfiehlt, die Konsistenz der Implementierung einer Site zu wahren, indem auf allen Seiten derselbe Implementierungstyp verwendet wird. Wenn jedoch Teile Ihrer Site unterschiedliche Anforderungen haben, können Sie diese Seite verwenden, um sicherzustellen, dass Besucherinnen und Besucher konsistent zwischen Seiten verfolgt werden.

Wenn Sie mehr als einen Implementierungstyp verwenden (z. B. AppMeasurement und hartcodierte Bildanforderungen), stellen Sie sicher, dass die folgenden Variablen korrekt festgelegt sind und miteinander übereinstimmen.

>[!NOTE]
>
>Alle Implementierungstypen müssen denselben Besucheridentifizierungstyp verwenden (alte Analytics-ID, Besucher-ID-Service oder Experience Platform Identity Service). Adobe empfiehlt, nach Möglichkeit in allen Implementierungen eine ECID zu verwenden.

| Variable | Web SDK-Tag-Erweiterung | Web SDK (Legierung) | Analytics-Erweiterung | AppMeasurement | Fest programmierte Bildanforderung |
|---|---|---|---|---|---|
| Report Suite-ID | Hinzufügen von Adobe Analytics als Dienst beim [Konfigurieren eines Datenstroms](https://experienceleague.adobe.com/de/docs/experience-platform/datastreams/configure) | Hinzufügen von Adobe Analytics als Dienst beim [Konfigurieren eines Datenstroms](https://experienceleague.adobe.com/de/docs/experience-platform/datastreams/configure) | [!UICONTROL Report Suites] im Abschnitt [!UICONTROL Bibliotheksverwaltung] beim [Konfigurieren der Erweiterung](https://experienceleague.adobe.com/de/docs/experience-platform/tags/extensions/client/analytics/overview) | Zeichenfolgenargument in [`s_gi`](../vars/functions/s-gi.md) | Teil des `pathname` der URL (nach `/b/ss/`) |
| Besucher-ID-Service | enthält nativ den [Experience Platform Identity Service](https://experienceleague.adobe.com/de/docs/experience-platform/identity/home); erfordert, dass [`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/idmigrationenabled) Cookies des Besucher-ID-Diensts lesen | enthält nativ den [Experience Platform Identity Service](https://experienceleague.adobe.com/de/docs/experience-platform/identity/home); erfordert [[!UICONTROL Migrieren von ECID von VisitorAPI zur Web-SDK]](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/identity), um Besucher-ID-Service-Cookies zu lesen | Verwenden Sie die Tag[Erweiterung [!UICONTROL Experience Cloud ID Service], ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/id-service/overview) den [Besucher-ID-Service) ](https://experienceleague.adobe.com/de/docs/id-service/using/home) | Implementieren des [Besucher-ID-Service](https://experienceleague.adobe.com/de/docs/id-service/using/home) (`VisitorAPI.js`) | Führen Sie einen [separaten Aufruf an den Besucher-ID-](https://experienceleague.adobe.com/en/docs/id-service/using/implementation/direct-integration) durch, um die gewünschte ID zu erhalten und den `mid` in die Abfragezeichenfolge aufzunehmen |
| Edge-Domain | Das Feld [!UICONTROL Edge Domain] beim [Konfigurieren der Erweiterung](https://experienceleague.adobe.com/de/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) | Die Eigenschaft `edgeDomain` beim [Konfigurieren des Web-SDK](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/overview) | [!UICONTROL SSL-Tracking] im Abschnitt [!UICONTROL Allgemein] beim [Konfigurieren der Erweiterung](https://experienceleague.adobe.com/de/docs/experience-platform/tags/extensions/client/analytics/overview) | Die [`trackingServerSecure`](../vars/config-vars/trackingserversecure.md) Variable | Der `hostname` der Bildanfrage-URL |

>[!NOTE]
>
>AppMeasurement-basierte Implementierungen (einschließlich der Analytics-Tag-Erweiterung) sind nicht mit dem [Experience Platform Identity Service](https://experienceleague.adobe.com/de/docs/id-service/using/home) kompatibel. Sie müssen die Besucheridentifizierung auf dem kleinsten gemeinsamen Nenner verwenden, um über Implementierungstypen hinweg zu synchronisieren, normalerweise der [Besucher-ID-Service](https://experienceleague.adobe.com/de/docs/id-service/using/home) (`VisitorAPI.js`).

Wenn eine dieser Variablen nicht für jeden Implementierungstyp konsistent ist, werden sie von Adobe wahrscheinlich als separate Besucherinnen und Besucher betrachtet. Wenn Besuchende nicht nahtlos über Implementierungstypen auf Ihrer Site hinweg verfolgt werden, besteht der häufigste Grund darin, dass die Besucheridentifizierung falsch konfiguriert ist. Stellen Sie sicher, dass jeder Implementierungstyp auf Ihrer Site korrekt dieselbe ECID (`mid` [Abfragezeichenfolge](/help/implement/validate/query-parameters.md)) erhält.
