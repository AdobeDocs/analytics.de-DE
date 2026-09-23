---
title: Besucheridentifizierung mithilfe der Dateneinfüge-API
description: Identifizieren Sie Besucherinnen und Besucher für die Server-seitige und direkte Adobe Analytics-Datenerfassung mit der Dateneinfüge-API.
feature: Implementation Basics
role: Admin, Developer, Leader
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
subfeature_v2:
  - id: c069c44e-5426-4c1a-accc-8028662f2fde
    internal-label: Functions
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
    internal-label: Variables
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%
---
# Besucheridentifizierung mithilfe der Dateneinfüge-API

Die [Dateneinfüge-API](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/) sendet Treffer ohne Client-seitige Bibliothek wie AppMeasurement oder Web SDK an Adobe Analytics-Erfassungsserver. Da keine Bibliothek zur Identitätsverwaltung für Sie vorhanden ist, legen Sie die Besucherkennung selbst fest - im Browser für direkte Bildanfragen oder auf Ihrem Server für die Server-seitige Erfassung.

>[!NOTE]
>
>Auf dieser Seite wird die Besucheridentität behandelt. Informationen zum Erstellen und Senden der Anfragen selbst finden Sie in der [Dokumentation zur Dateneinfüge-API](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/) auf Adobe Developer.

Adobe identifiziert einen Besucher anhand der standardmäßigen [Reihenfolge der Vorgänge](overview.md): der `vid`, dann die `aid`, `mid`, `fid` und schließlich die IP-Adresse und den Benutzeragenten. Mit der Dateneinfüge-API legen Sie für gewöhnlich eine von drei Kennungen direkt fest: die ECID (`mid`), die Analytics-Besucher-ID (`aid`) oder eine benutzerdefinierte Besucher-ID (`vid`).

## Verwenden der ECID (empfohlen)

Die ECID (als `mid` gesendet) ist die moderne, lösungsübergreifende Besucherkennung, die für Adobe Analytics, Adobe Target und Adobe Audience Manager freigegeben ist. Adobe empfiehlt, sie nach Möglichkeit zu verwenden.

Abrufen der ECID mit dem [Besucher-ID-Service](https://experienceleague.adobe.com/de/docs/id-service/using/home) (`VisitorAPI.js`). Initialisieren Sie in einem Browser den Service mit Ihrer IMS-Organisations-ID mithilfe von [`getInstance`](https://experienceleague.adobe.com/en/docs/id-service/using/id-service-api/methods/getinstance) und lesen Sie dann die ECID mit [`getMarketingCloudVisitorID`](https://experienceleague.adobe.com/en/docs/id-service/using/id-service-api/methods/getmcvid):

```js
var visitor = Visitor.getInstance("YOUR_ORG_ID@AdobeOrg");
var ecid = visitor.getMarketingCloudVisitorID();
```

Senden Sie diesen Wert bei jedem Treffer als `mid` Abfrageparameter oder das `<marketingCloudVisitorId>` XML-Tag. Wenn Ihre Daten an Audience Manager weitergeleitet werden, senden Sie auch die Region von [`getLocationHint`](https://experienceleague.adobe.com/en/docs/id-service/using/id-service-api/methods/getlocationhint) als `aamlh` (oder `<imsRegion>`-Tag). Um Ihre eigenen Kundenkennungen mit dem Besucher zu verknüpfen, verwenden Sie [`setCustomerIDs`](https://experienceleague.adobe.com/en/docs/id-service/using/id-service-api/methods/setcustomerids).

Für die Server-seitige Erfassung rufen Sie die ECID auf dem Client ab und leiten Sie sie an Ihren Server weiter, um sie bei jedem Treffer zu senden. Um eine ECID vollständig Server-seitig ohne Client zu generieren, verwenden Sie die [direkte Integration](https://experienceleague.adobe.com/en/docs/id-service/using/implementation/direct-integration) des ID-Service.

## Verwenden der Analytics-Besucher-ID

Die Analytics-Besucher-ID (`aid`) wird im [`s_vi`](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/cookies/analytics)-Cookie gespeichert. Wenn ein Treffer ohne Kennung eingeht, weist der Erfassungs-Server eine `aid` zu und gibt sie im Antworttext zurück. Einige [Antworttypen](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/response-types) schließen diese Kennung auch in den Antworttext ein. Wer diese ID speichert und erneut sendet, ist der Unterschied zwischen den beiden Implementierungsstilen.

* **Client-seitig (direkte Bildanforderungen).** Der Browser speichert das vom Server zurückgegebene `s_vi`-Cookie und sendet es bei jeder späteren Anforderung an dieselbe Sammlungsdomäne, damit der Besucher automatisch erkannt wird. Dazu muss die Erfassungs-Domain in der Lage sein, das Cookie festzulegen und zu lesen — und einen First-Party-CNAME-Tracking-Server zu verwenden. Da dieses Modell von Cookies abhängt, wird es an der Stelle beeinträchtigt, an der Browser sie einschränken (Blockierung von Drittanbieter-Cookies, Intelligent Tracking Prevention); ECID wird für dauerhafte Identität bevorzugt.

  >[!NOTE]
  >
  >Wenn Sie die Besucher-ID direkt aus dem `s_vi`-Cookie lesen, legt das Cookie die ID in zusätzliche Daten (z. B. `[CS]v1|<id>[CE]`) um - nur den `<id>` Teil extrahieren. Beim Lesen der ID aus einer Besucherantwort wird sie direkt zurückgegeben, ohne dass eine Analyse erfolgt.

* **Server-seitig.** Ein Server hat keine Cookie-JAR-Datei, sodass Sie die `aid` selbst speichern und erneut senden, indem Sie sie an den Benutzer verschlüsseln:

  1. Suchen der gespeicherten `aid` für den Benutzer.
  1. Wenn Sie einen haben, senden Sie ihn als `aid` Abfrageparameter.
  1. Andernfalls senden Sie den Treffer ohne Kennung und fordern einen Antworttyp an, der die zugewiesene `aid` zurückgibt, und speichern Sie ihn dann für das nächste Mal.

  Der erste Treffer ohne Kennung wird bereits dem vom Server zurückgegebenen `aid` zugeordnet, sodass keine Daten verloren gehen, wenn er gesendet wird, bevor die Kennung angegeben wurde. Informationen zu den Antworttypen, die die ID (`3` für JavaScript, `11` für XML, `10` für JSON) und das Anfrageformat zurückgeben, finden Sie unter [Antworttyp](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/response-types) in der Dokumentation zur Dateneinfüge-API.

  Da eine Server-seitige Anfrage keine Besucher-Cookies enthält und die eigene IP-Adresse und der Benutzeragent zum Absender gehören, leiten Sie auch die tatsächliche IP-Adresse des Besuchers (den `X-Forwarded-For`-Header) und den Benutzeragenten (den `User-Agent`-Header) weiter, damit Treffer korrekt zugeordnet werden.

## Verwenden einer benutzerdefinierten Besucher-ID

Wenn Sie bereits über eine dauerhafte Kennung verfügen, die Sie vollständig steuern können, können Sie sie als [`visitorID`](/help/implement/vars/config-vars/visitorid.md) (`vid`) bei jedem Treffer und Ihrer eigenen Identität End-to-End senden. Dies eignet sich für Nicht-Browser-Plattformen, die eine stabile Gerätekennung bieten. Beispielsweise kann eine Unity-Anwendung ihre Geräte-ID als `vid` senden.

>[!IMPORTANT]
>
>Verwenden Sie `vid` nur, wenn Sie bei jedem Treffer einen stabilen Wert garantieren können:
>
>* **Browser passen nicht gut.** Ein Browser hat keine dauerhafte Kennung, die Sie zuverlässig ausfüllen können, sodass ein Browser-`vid` dazu neigt, zu fragmentieren oder zusammenzustoßen. Verwenden Sie stattdessen das Cookie-basierte Client-seitige Modell.
>* **Achten Sie auf Authentifizierungs-IDs.** Sie haben keine Kennung, bevor sich ein Benutzer anmeldet. Wenn sich der Benutzer abmeldet, werden spätere Treffer einem anderen Besucher zugeordnet. Mit diesen Aktionen wird die Aktivität einer Person auf mehrere Besucher aufgeteilt.

Unter [`visitorID`](/help/implement/vars/config-vars/visitorid.md) finden Sie das Format und die Einschränkungen einer benutzerdefinierten Besucher-ID.
