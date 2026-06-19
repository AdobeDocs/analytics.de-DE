---
title: Besucheridentifizierung mit AppMeasurement
description: Identifizieren Sie Besuchende bei der Implementierung von Adobe Analytics mithilfe von AppMeasurement korrekt.
exl-id: 38797ca5-dc53-431e-95df-3c9e68aead94
TQID: https://experienceleague.adobe.com/vWLzF0HXreytCKr01H4-gKzNlO36ySHA2vbcHvT3cIw
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2:
  - id: c069c44e-5426-4c1a-accc-8028662f2fde
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: d4db20e3498d54162806b3fdef0b34f45c93a6ff
workflow-type: tm+mt
source-wordcount: 512
ht-degree: 0%

---

# Besucheridentifizierung mit AppMeasurement

AppMeasurement ist die alte JavaScript-Bibliothek von Adobe Analytics für die Datenerfassung. Während AppMeasurement allein eine native Möglichkeit bietet, Besuchende zu identifizieren, lehnen viele moderne Browser die Drittanbieter-Cookies ab, die es zu setzen versucht. Adobe empfiehlt dringend, in allen Implementierungen den Besucher-ID-Service von Adobe Experience Cloud zu verwenden, um modernen Datenschutzstandards für Browser zu entsprechen. Alle Versionen von AppMeasurement sind im Lieferumfang von `VisitorAPI.js` enthalten, der JavaScript-Bibliothek, die zur Implementierung des Besucher-ID-Service verwendet wird.

## Identifizieren von Besuchern mithilfe des Besucher-ID-Service (empfohlen)

Stellen Sie sicher, dass Sie mit Folgendem vorbereitet sind:

* Laden Sie die [neueste Version von AppMeasurement](https://github.com/adobe/appmeasurement) herunter. Die heruntergeladene Bibliothek enthält sowohl `AppMeasurement.js` als auch `VisitorAPI.js`.
* Eine Entwicklungs[Report Suite-ID](/help/admin/tools/manage-rs/new-rs/new-report-suite.md).
* Die gewünschte Edge-Domain für [`trackingServerSecure`](/help/implement/vars/config-vars/trackingserversecure.md).
* Ihre IMS-Organisations-ID:
   1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [&#128279;](https://experience.adobe.com)Adobe CX Enterprise an.
   1. Drücken Sie an einer beliebigen Stelle in der CX Enterprise-Benutzeroberfläche `[Cmd]` + `[I]` (iOS) oder `[Ctrl]` + `[I]` (Windows).
   1. Ein **[!UICONTROL User Data Debugger]** wird angezeigt. Wählen Sie die **[!UICONTROL Zugewiesene Organisationen]** aus.
   1. Erweitern Sie die gewünschte IMS-Organisation.
   1. Suchen Sie das Feld **[!UICONTROL ID]**.

Sobald Sie über die oben genannten Ressourcen verfügen, enthält die folgende einfache Beispielseite die erforderlichen Mindestaufrufe, um Daten an Adobe Analytics zu senden:

```html
<html>
  <head>
    <title>Example AppMeasurement implementation page</title>
    <script src="AppMeasurement.js"></script>
    <script src="VisitorAPI.js"></script>
  </head>
  <body>
    <h1>Hello world!</h1>
    <script>
      var s = s_gi("examplersid"); // Include development report suite ID here
      s.trackingServerSecure = "example.data.adobedc.net"; // Include edge domain here
      s.visitor = Visitor.getInstance("ADB3LETTERSANDNUMBERS@AdobeOrg"); // Include IMS org ID here
      s.pageName = document.title;
      s.t();
    </script>
  </body>
</html>
```

>[!TIP]
>
>Sie können verfolgen, ob ein Treffer den Besucher-ID-Service verwendet, indem Sie das Vorhandensein von `Visitor` einer benutzerdefinierten Variablen in [`doPlugins`](/help/implement/vars/functions/doplugins.md) zuweisen:
>
>```js
>s.doPlugins = function() {
>   s.prop1 = typeof(Visitor) != "undefined" ? "VisitorAPI present" : "VisitorAPI missing";
>};
>```

## Identifizieren von Besuchern mithilfe des `s_vi`-Cookies (nicht empfohlen)

>[!IMPORTANT]
>
>Adobe rät davon ab, diese Methode zur Besucheridentifizierung zu verwenden.

Wenn Ihr Unternehmen den Besucher-ID-Service nicht verwendet, verwendet AppMeasurement eine eigene Form der Besucheridentifizierung. Wenn ein Besucher zum ersten Mal auf Ihre Site gelangt, sucht die Bibliothek nach einem [`s_vi`](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/cookies/analytics) Cookie. Dieses Cookie wird auf den Domain-Matching-[`trackingServerSecure`](/help/implement/vars/config-vars/trackingserversecure.md) (für HTTPS) oder `trackingServer` (für HTTP) gesetzt.

* Wenn Sie am [Programm für verwaltete Zertifikate](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/adobe-managed-cert) teilnehmen, ist Ihr Tracking-Server normalerweise eine Erstanbieter-Domain, die `s_vi`-Cookies als Erstanbieter verwendet.
* Wenn Sie nicht am verwalteten Zertifikatprogramm teilnehmen, ist der Tracking-Server normalerweise eine Subdomain von `adobedc.net`, `omtrdc.net` oder `2o7.net`, wodurch das `s_vi`-Cookie zu einem Drittanbieter-Cookie wird. Aufgrund der modernen Datenschutzstandards von Browsern werden Drittanbieter-Cookies von den meisten Browsern abgelehnt. Nach der Ablehnung versucht AppMeasurement stattdessen, ein First-Party-Ausweich-Cookie (`fid`) festzulegen.

Wenn Sie `trackingServerSecure` richtig eingestellt haben, sind keine weiteren Maßnahmen zur Besucheridentifizierung erforderlich.

## Besucheridentifizierung mit `visitorID` (nicht empfohlen)

>[!IMPORTANT]
>
>Adobe rät davon ab, diese Methode zur Besucheridentifizierung zu verwenden.

Die Verwendung der [`visitorID`](/help/implement/vars/config-vars/visitorid.md) ermöglicht Ihrem Unternehmen eine vollständige unabhängige Kontrolle bei der Identifizierung von Besuchern. Beachten Sie bei Verwendung von `visitorID` die folgenden Einschränkungen:

* Jeder Treffer muss denselben `visitorID` enthalten, damit er als einzelner Besucher gezählt wird.
   * Bei Treffern, bei denen nicht angegeben wird, `visitorID` automatisch versucht wird, eine andere Besucheridentifizierungsmethode zu verwenden, und diese Treffer als separate Besucherin bzw. separater Besucher behandelt werden.
   * Treffer, die einen anderen `visitorID` als der vorherige Treffer enthalten, werden als separater Besucher behandelt.
   * Adobe bietet keine Möglichkeit, Treffer mithilfe verschiedener Besucher-IDs in Adobe Analytics zusammenzufügen.
* Freigegebene Zielgruppen, Analytics for Target und Kundenattribute werden nicht für Besucher unterstützt, die mithilfe von `visitorID` identifiziert wurden.

Siehe [`visitorID`](/help/implement/vars/config-vars/visitorid.md) für Implementierungsanweisungen unter Verwendung dieser Variablen.
