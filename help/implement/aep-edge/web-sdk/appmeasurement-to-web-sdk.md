---
title: Migration von AppMeasurement zum Web SDK
description: Aktualisieren Sie Ihre Adobe Analytics-Implementierung von der AppMeasurement JavaScript-Bibliothek auf die Web SDK JavaScript-Bibliothek.
exl-id: c90246e8-0f04-4655-9204-33c0ef611b13
source-git-commit: 05690cc8c1ea0364cbab86f35666df1cc1b13e69
workflow-type: tm+mt
source-wordcount: '1334'
ht-degree: 7%

---

# Migration von AppMeasurement zum Web SDK

Dieser Implementierungspfad umfasst einen methodischen Migrationsprozess, um von einer AppMeasurement-Implementierung zu einer Web SDK JavaScript-Bibliotheksimplementierung zu wechseln. Andere Implementierungspfade werden auf separaten Seiten behandelt:

* [Analytics-Erweiterung auf Web SDK-Erweiterung](analytics-extension-to-web-sdk.md): Verwenden Sie einen reibungslosen und methodischen Ansatz, um von der Adobe Analytics-Tag-Erweiterung zur Web SDK-Tag-Erweiterung zu wechseln. Dieser Ansatz unterdrückt die Notwendigkeit, XDM zu verwenden, bis Ihr Unternehmen für die Verwendung von Adobe Experience Platform-Diensten wie Customer Journey Analytics bereit ist. Verwenden Sie das Objekt `data` anstelle des Objekts `xdm` , um Daten an Adobe zu senden.
* [Web SDK JavaScript Library](web-sdk-javascript-library.md): Eine neue Web SDK-Installation mit der Web SDK JavaScript Library (`alloy.js`). Verwalten Sie die Implementierung selbst, anstatt die Tags-Benutzeroberfläche zu verwenden. Dazu ist die Adobe Analytics ExperienceEvent-Feldergruppe erforderlich, die typische Analytics-Variablen enthält, die in Ihr XDM-Schema aufgenommen werden sollen.
* [Web SDK tag extension](web-sdk-tag-extension.md): Eine neue Web SDK-Installation, bei der Sie die Implementierung mithilfe von Tags in der Adobe Experience Platform-Datenerfassung verwalten. Dazu ist die Adobe Analytics ExperienceEvent-Feldergruppe erforderlich, die typische Analytics-Variablen enthält, die in Ihr XDM-Schema aufgenommen werden sollen.

## Vorteile und Nachteile dieses Implementierungspfads

Die Verwendung dieses Migrationsansatzes hat sowohl Vor- als auch Nachteile. Legen Sie bei jeder Option sorgfältig ab, welcher Ansatz für Ihr Unternehmen am besten geeignet ist.

| Vorteile | Nachteile |
| --- | --- |
| <ul><li>**Nutzt Ihre vorhandene Implementierung**: Dieser Ansatz erfordert zwar einige Implementierungsänderungen, aber keine völlig neue Implementierung. Sie können Ihre vorhandene Datenschicht und Ihren Code mit minimalen Änderungen an der Implementierungslogik verwenden.</li><li>**Kein Schema erforderlich**: Für diese Phase der Migration zum Web SDK benötigen Sie kein XDM-Schema. Stattdessen können Sie das Objekt `data` ausfüllen, das Daten direkt an Adobe Analytics sendet. Nachdem die Migration zum Web SDK abgeschlossen ist, können Sie ein Schema für Ihre Organisation erstellen und die Datastraam-Zuordnung verwenden, um die entsprechenden XDM-Felder auszufüllen. Wenn in dieser Phase des Migrationsprozesses ein Schema erforderlich ist, muss Ihr Unternehmen ein Adobe Analytics-XDM-Schema verwenden. Die Verwendung dieses Schemas erschwert es Ihrem Unternehmen, in Zukunft Ihr eigenes Schema zu verwenden.</li></ul> | <ul><li>**Implementierungsänderungen erfordern die Intervention des Entwicklers**: Wenn Sie Änderungen an Ihrer Web SDK-Implementierung vornehmen möchten, müssen Sie sich an Ihr Entwicklungsteam wenden, um den Code auf Ihrer Site zu bearbeiten. Der Ansatz, bei dem [zur Web SDK-Tag-Erweiterung](analytics-extension-to-web-sdk.md) migriert, vermeidet diesen Nachteil.</li><li>**Technische Schulden bei der Implementierung**: Da dieser Ansatz eine modifizierte Form Ihrer bestehenden Implementierung verwendet, kann es schwieriger sein, die Implementierungslogik zu verfolgen und bei Bedarf zukünftige Änderungen vorzunehmen.</li><li>**Erfordert eine Zuordnung zum Senden von Daten an Platform**: Wenn Ihre Organisation für die Verwendung von Customer Journey Analytics bereit ist, müssen Sie Daten an einen Datensatz in Adobe Experience Platform senden. Diese Aktion erfordert, dass jedes Feld im `data` -Objekt ein Eintrag im Tool für die Datenasterzuordnung ist, der ihn einem XDM-Schemafeld zuordnet. Die Zuordnung muss nur einmal für diesen Workflow durchgeführt werden. Implementierungsänderungen sind nicht erforderlich. Es handelt sich jedoch um einen zusätzlichen Schritt, der beim Senden von Daten in ein XDM-Objekt nicht erforderlich ist.</li></ul> |

Adobe empfiehlt, diesem Implementierungspfad in den folgenden Szenarien zu folgen:

* Sie verfügen über eine vorhandene Implementierung mithilfe der Adobe Analytics AppMeasurement JavaScript-Bibliothek. Wenn Sie über eine Implementierung mit der Adobe Analytics-Tag-Erweiterung verfügen, folgen Sie stattdessen dem Befehl &quot;[Migrieren von der Adobe Analytics-Tag-Erweiterung zur Web SDK-Tag-Erweiterung](analytics-extension-to-web-sdk.md)&quot;.
* Sie beabsichtigen in Zukunft Customer Journey Analytics zu verwenden, möchten Ihre Analytics-Implementierung jedoch nicht von Grund auf durch eine Web SDK-Implementierung ersetzen. Die Ersetzung Ihrer Implementierung durch das Web SDK erfordert den größten Aufwand, bietet aber auch die praktikabelste langfristige Implementierungsarchitektur. Wenn Ihr Unternehmen bereit ist, die Implementierung eines sauberen Web SDK durchzuführen, finden Sie weitere Informationen unter [Aufnehmen von Daten über das Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk) im Customer Journey Analytics-Benutzerhandbuch.

## Schritte für die Migration zum Web SDK

Die folgenden Schritte enthalten konkrete Ziele, auf die wir hinarbeiten müssen. Klicken Sie auf jeden Schritt, um detaillierte Anweisungen dazu zu erhalten.

+++**1. Erstellen und Konfigurieren eines Datastreams**

Erstellen Sie einen Datenspeicher in der Adobe Experience Platform-Datenerfassung. Wenn Sie Daten an diesen Datastream senden, leitet er Daten an Adobe Analytics weiter. Künftig leitet derselbe Datenspeicher Daten an Customer Journey Analytics weiter.

1. Navigieren Sie zu [experience.adobe.com](https://experience.adobe.com) und melden Sie sich mit Ihren Anmeldedaten an.
1. Verwenden Sie die Startseite oder die Produktselektor oben rechts, um zur **[!UICONTROL Datenerfassung]** zu navigieren.
1. Wählen Sie im linken Navigationsbereich **[!UICONTROL Datenspeicher]** aus.
1. Wählen Sie **[!UICONTROL Neuer Datenstrom]** aus.
1. Geben Sie den gewünschten Namen ein und wählen Sie dann **[!UICONTROL Speichern]** aus.
1. Nachdem der Datastream erstellt wurde, wählen Sie **[!UICONTROL Dienst hinzufügen]** aus.
1. Wählen Sie im Dropdown-Menü &quot;Dienst&quot;die Option **[!UICONTROL Adobe Analytics]**.
1. Geben Sie dieselbe Report Suite-ID ein wie die Site, an die Sie derzeit Analysedaten senden. Klicken Sie auf **[!UICONTROL Speichern]**.

![Hinzufügen des Adobe Analytics-Dienstes](assets/datastream-rsid.png) {style="border:1px solid lightslategray"}

Ihr Datastream kann jetzt Daten empfangen und an Adobe Analytics weitergeben. Notieren Sie die Datastream-ID, da diese ID für die Konfiguration des Web SDK im Code erforderlich ist.

+++

+++**2. Installieren der Web SDK JavaScript-Bibliothek**

Referenzieren Sie die neueste Version von `alloy.js` , damit die zugehörigen Methodenaufrufe verwendet werden können. Weitere Informationen und zu verwendende Codeblöcke finden Sie unter [Installieren des Web SDK mit der JavaScript-Bibliothek](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/install/library) .

+++

+++**3. Web SDK** konfigurieren

Richten Sie Ihre Implementierung so ein, dass sie auf den im vorherigen Schritt erstellten Datastream verweist, indem Sie den Web SDK-Befehl [`configure`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/overview) verwenden. Der Befehl `configure` muss auf jeder Seite festgelegt sein, damit Sie ihn neben den Bibliotheksinstallationscode einfügen können.

Verwenden Sie die Eigenschaften [`datastreamId`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/datastreamid) und [`orgId`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/orgid) im Web SDK `configure` -Befehl:

* Stellen Sie `datastreamId` auf die aus dem vorherigen Schritt abgerufene Datastream-ID ein.
* Stellen Sie die `orgId` auf die IMS-Organisation Ihres Unternehmens ein.

```js
alloy("configure", {
    datastreamId: "ebebf826-a01f-4458-8cec-ef61de241c93",
    orgId: "ADB3LETTERSANDNUMBERS@AdobeOrg"
});
```

Sie können optional andere Eigenschaften im Befehl [`configure`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/overview) entsprechend den Implementierungsanforderungen Ihres Unternehmens festlegen.

+++

+++**4. Aktualisieren der Code-Logik zur Verwendung einer JSON-Payload**

Ändern Sie Ihre Analytics-Implementierung so, dass sie nicht auf `AppMeasurement.js` oder das `s` -Objekt angewiesen ist. Legen Sie stattdessen Variablen in ein korrekt formatiertes JavaScript-Objekt fest, das beim Senden an Adobe in ein JSON-Objekt konvertiert wird. Die Festlegung einer [Datenschicht](../../prepare/data-layer.md) auf Ihrer Site ist bei der Festlegung von Werten äußerst hilfreich, da Sie weiterhin auf dieselben Werte verweisen können.

Um Daten an Adobe Analytics zu senden, muss die Web SDK-Payload `data.__adobe.analytics` verwenden, wobei alle Analysevariablen in diesem Objekt festgelegt sind. Variablen in diesem Objekt verwenden identische Namen und Formate wie ihre AppMeasurement-Variablen-Entsprechungen. Wenn Sie beispielsweise die Variable `products` festlegen, teilen Sie sie nicht wie bei XDM in einzelne Objekte. Fügen Sie ihn stattdessen als Zeichenfolge ein, die genau ist, wenn Sie die Variable `s.products` festlegen:

```json
{
  "data": {
    "__adobe": {
      "analytics": {
        "products": "Shoes,Men's sneakers,1,49.99"
      }
    }
  }
}
```

Letztlich enthält diese Payload alle gewünschten Werte und alle Verweise auf das `s` -Objekt in Ihrer Implementierung werden entfernt. Sie können alle von JavaScript bereitgestellten Ressourcen verwenden, um dieses Payload-Objekt festzulegen, einschließlich der Punktnotation zum Festlegen einzelner Werte.

```js
// Define the payload and set objects within it
var dataObj = {data: {__adobe: {analytics: {}}}};
dataObj.data.__adobe.analytics.pageName = window.document.title;
dataObj.data.__adobe.analytics.eVar1 = "Example value";

// Alternatively, set values in an object and use a spread operator to achieve identical results
var a = new Object;
a.pageName = window.document.title;
a.eVar1 = "Example value";
var dataObj = {data:{__adobe:{analytics:{...a}}}};
```

+++

+++**5. Methodenaufrufe für die Verwendung des Web SDK aktualisieren**

Aktualisieren Sie alle Instanzen, in denen Sie [`s.t()`](../../vars/functions/t-method.md) und [`s.tl()`](../../vars/functions/tl-method.md) aufrufen, und ersetzen Sie sie durch den Befehl [`sendEvent`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/sendevent/overview) . Es gibt drei Szenarien, die zu berücksichtigen sind:

* **Seitenansichts-Tracking**: Ersetzen Sie den Seitenansichts-Tracking-Aufruf durch den Web SDK `sendEvent` -Befehl:

  ```js
  // If your current implementation has this line of code:
  s.t();
  
  // Replace it with this line of code. The dataObj object contains the variables to send.
  alloy("sendEvent", dataObj);
  ```

* **Automatische Linktracking**: Die Konfigurationseigenschaft [`clickCollectionEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) ist standardmäßig aktiviert. Es werden automatisch die richtigen Linktracking-Variablen festgelegt, um Daten an Adobe Analytics zu senden. Wenn Sie das automatische Linktracking deaktivieren möchten, legen Sie diese Eigenschaft im Befehl [`configure`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/overview) auf `false` fest.

* **Manuelles Linktracking**: Das Web SDK verfügt nicht über separate Befehle zwischen Seitenansichts- und Nicht-Seitenansichtsaufrufen. Geben Sie diese Unterscheidung im Payload-Objekt an.

  ```js
  // If your current implementation has this line of code:
  s.tl(true,"o","Example custom link");
  
  // Replace it with these lines of code. Add the required fields to the dataObj object.
  dataObj.data.__adobe.analytics.linkName = "Example custom link";
  dataObj.data.__adobe.analytics.linkType = "o";
  dataObj.data.__adobe.analytics.linkURL = "https://example.com";
  alloy("sendEvent", dataObj);
  ```

+++

+++**6. Validieren und Veröffentlichen von Änderungen**

Nachdem Sie alle Verweise auf AppMeasurement und das Objekt `s` entfernt haben, veröffentlichen Sie Ihre Änderungen in Ihrer Entwicklungsumgebung, um zu überprüfen, ob die neue Implementierung funktioniert. Nachdem Sie überprüft haben, ob alles ordnungsgemäß funktioniert, können Sie Ihre Aktualisierungen in der Produktion veröffentlichen.

Bei richtiger Migration ist `AppMeasurement.js` nicht mehr auf Ihrer Site erforderlich und alle Verweise auf dieses Skript können entfernt werden.

+++

Zu diesem Zeitpunkt befindet sich Ihre Analytics-Implementierung vollständig im Web SDK und ist angemessen darauf vorbereitet, in Zukunft zu Customer Journey Analytics zu wechseln.
