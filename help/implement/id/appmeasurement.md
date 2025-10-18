---
title: Besucheridentifizierung mit AppMeasurement
description: Identifizieren Sie Besuchende bei der Implementierung von Adobe Analytics mithilfe von AppMeasurement korrekt.
source-git-commit: 5bd1914dc52c664348f30793761f0fc347343156
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 0%

---

# Besucheridentifizierung mit AppMeasurement

AppMeasurement ist die alte JavaScript-Bibliothek von Adobe Analytics für die Datenerfassung. Während AppMeasurement allein eine native Möglichkeit bietet, Besuchende zu identifizieren, lehnen viele moderne Browser die Cookies ab, die es zu setzen versucht. Adobe empfiehlt dringend, in allen Implementierungen den Besucher-ID-Service von Adobe Experience Cloud zu verwenden, um modernen Datenschutzstandards für Browser zu entsprechen. Alle Versionen von AppMeasurement sind im Lieferumfang von `VisitorAPI.js` enthalten, der JavaScript-Bibliothek, die zur Implementierung des Besucher-ID-Service verwendet wird.

## Identifizieren von Besuchern mithilfe des Besucher-ID-Service (empfohlen)

Verwenden Sie diesen Abschnitt, um eine Basisintegration zwischen Adobe Analytics und dem Besucher-ID-Service zu erstellen. Stellen Sie sicher, dass Sie mit Folgendem vorbereitet sind:

* Laden Sie die [neueste Version von AppMeasurement](https://github.com/adobe/appmeasurement) herunter. Die heruntergeladene Bibliothek enthält sowohl `AppMeasurement.js` als auch `VisitorAPI.js`.
* Eine Entwicklungs[Report Suite-ID](/help/admin/tools/manage-rs/new-rs/new-report-suite.md).
* Die gewünschte Domain für [`trackingServerSecure`](/help/implement/vars/config-vars/trackingserversecure.md).
* Ihre IMS-Organisations-ID:
   1. Melden Sie sich mit Ihren Adobe ID[Anmeldeinformationen bei &#x200B;](https://experience.adobe.com)experience.adobe.com) an.
   1. Drücken Sie an einer beliebigen Stelle in der Experience Cloud-Benutzeroberfläche `[Cmd]` + `[I]` (iOS) oder `[Ctrl]` + `[I]` (Windows).
   1. Ein **[!UICONTROL User Data Debugger]** wird angezeigt. Wählen Sie die **[!UICONTROL Zugewiesene Organisationen]** aus.
   1. Erweitern Sie die gewünschte IMS-Organisation.
   1. Suchen Sie das Feld **[!UICONTROL ID]**.

Sobald Sie über die oben genannten Ressourcen verfügen, sehen Sie sich die folgende einfache Beispielseite an, die die erforderlichen Mindestaufrufe zum Senden von Daten an Adobe Analytics enthält:

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
>Sie können verfolgen, ob ein Treffer den Besucher-ID-Service verwendet, indem Sie das Vorhandensein von `Visitor` einer benutzerdefinierten Variablen zuweisen:
>
>```js
>s.prop1 = typeof(Visitor) != "undefined" ? "VisitorAPI Present" : "VisitorAPI Missing";
>```

## Identifizieren von Besuchern mithilfe des `s_vi`-Cookies (nicht empfohlen)

>[!IMPORTANT]
>
>Adobe rät davon ab, diese Methode zur Besucheridentifizierung zu verwenden.

Wenn Ihr Unternehmen den Besucher-ID-Service nicht verwendet, verwendet AppMeasurement eine eigene Form der Besucheridentifizierung. Wenn ein Besucher zum ersten Mal auf Ihre Site gelangt, sucht die Bibliothek nach einem [`s_vi`](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/cookies/analytics) Cookie. Dieses Cookie wird auf den Domain-Matching-[`trackingServerSecure`](/help/implement/vars/config-vars/trackingserversecure.md) (für HTTPS) oder [`trackingServer`](/help/implement/vars/config-vars/trackingserver.md) (für HTTP) gesetzt.

* Wenn Sie am [Programm für verwaltete Zertifikate](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/adobe-managed-cert) teilnehmen, ist Ihr Tracking-Server normalerweise eine Erstanbieter-Domain, die `s_vi`-Cookies als Erstanbieter verwendet.
* Wenn Sie nicht am verwalteten Zertifikatprogramm teilnehmen, ist der Tracking-Server normalerweise eine Subdomain von `adobedc.net`, `omtrdc.net` oder `2o7.net`, wodurch das `s_vi`-Cookie zu einem Drittanbieter-Cookie wird. Aufgrund der modernen Datenschutzpraktiken von Browsern werden Drittanbieter-Cookies von den meisten Browsern abgelehnt. Nach der Ablehnung versucht AppMeasurement stattdessen, ein First-Party-Ausweich-Cookie (`fid`) festzulegen.

Wenn Sie `trackingServerSecure` richtig eingestellt haben, sind keine weiteren Maßnahmen zur Besucheridentifizierung erforderlich.

## Besucheridentifizierung mit `visitorID` (nicht empfohlen)

>[!IMPORTANT]
>
>Adobe rät davon ab, diese Methode zur Besucheridentifizierung zu verwenden.

Die Verwendung der [`visitorID`](/help/implement/vars/config-vars/visitorid.md) ermöglicht Ihrem Unternehmen eine vollständige unabhängige Kontrolle bei der Identifizierung von Besuchern. Beachten Sie bei Verwendung von `visitorID` die folgenden Einschränkungen:

* Jeder Treffer muss denselben `visitorID` enthalten, damit er als einzelner Besucher gezählt wird.
   * Bei Treffern, bei denen nicht angegeben wird, `visitorID` automatisch versucht wird, eine andere Besucheridentifizierungsmethode zu verwenden, und diese Treffer als separate Besucherin bzw. separater Besucher behandelt werden.
   * Treffer, die einen anderen `visitorID` als der vorherige Treffer enthalten, werden als separater Besucher behandelt.
   * Adobe bietet keine Möglichkeit, Treffer mithilfe verschiedener Besucher-IDs zusammenzufügen.
* Freigegebene Zielgruppen, Analytics for Target und Kundenattribute werden nicht für Besucher unterstützt, die mithilfe von `visitorID` identifiziert wurden.

Siehe [`visitorID`](/help/implement/vars/config-vars/visitorid.md) für Implementierungsanweisungen unter Verwendung dieser Variablen.
