---
title: „AppMeasurement“ mit iFrames verwenden
description: Greifen Sie auf Adobe Analytics-Variablen innerhalb eines IFrame oder einer übergeordneten Seite zu, während Sie sich in einem IFrame befinden.
feature: Implementation Basics
exl-id: 59b9cd4f-8599-41ee-8b54-a6a556198ecd
role: Admin, Developer, Leader
TQID: https://experienceleague.adobe.com/og9yeHUn5BJVm8-22V2l1frcpluXdlI-f0LnyjFacnk
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 319
ht-degree: 100%

---

# „AppMeasurement“ mit iFrames verwenden

Sie können „AppMeasurement“-Variablen sowohl von untergeordneten als auch von übergeordneten iFrames aus referenzieren. Es ist erforderlich, alle Variablen am selben Speicherort zu definieren, an dem sich die „AppMeasurement“-Bibliothek befindet. In den folgenden Beispielen wird erläutert, wie Sie einfache „AppMeasurement“-Variablen und -Methoden innerhalb und außerhalb eines iFrames festlegen.

Wenn Sie Tags in Adobe Experience Platform verwenden, sollten Sie sicherstellen, dass das Tracker-Objekt global verfügbar ist. Siehe [Adobe Analytics-Erweiterung – Übersicht](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html?lang=de).

>[!CAUTION]
>
>Vermeiden Sie, „AppMeasurement“-Bibliotheken sowohl auf einer übergeordneten Seite als auch in einem IFrame zu verwenden. Dadurch entstehen Risiken beim Senden mehrerer Bildanfragen, wodurch die Größe der Berichte und die Anzahl der gebührenpflichtigen Server-Aufrufe steigt.

## Zugriff auf „AppMeasurement“ in einem IFrame

Sie können über das IFrame-Objekt auf „AppMeasurement“-Variablen zugreifen. In diesen Beispielen wird [pageName](../vars/page-vars/pagename.md) gesetzt und die [t()-Methode](../vars/functions/t-method.md) mit zwei verschiedenen Referenzierungsarten des IFrame-Objekts aufgerufen.

```js
// Reference AppMeasurement code that resides within an iframe and send an image request
document.getElementById('targetFrame').contentWindow.s.pageName="Page name within iframe";
document.getElementById('targetFrame').contentWindow.s.t();

// An alternate method to the above if there's only one iframe on the page
window.frames[0].contentWindow.s.pageName = "Page name within iframe";
window.frames[0].contentWindow.s.t();
```

## Zugriff auf „AppMeasurement“ innerhalb eines IFrame

Sie können innerhalb eines IFrame auf „AppMeasurement“-Variablen auf einer übergeordneten Seite zugreifen. In diesem Beispiel wird [pageName](../vars/page-vars/pagename.md) gesetzt und die [t()-Methode](../vars/functions/t-method.md) mit der [`parent`](https://www.w3schools.com/jsref/prop_win_parent.asp)-Eigenschaft aufgerufen.

```js
// Reference AppMeasurement code on a parent page from within an iframe and send an image request
parent.s.pageName = "Page Name on Hosted Window";
parent.s.t();
```

## Verwenden von `postMessage`- und Ereignis-Listenern

Alternativ können Sie Variablen mit `postMessage`- und Ereignis-Listenern festlegen. Für diese Methode ist kein direkter Verweis auf einen IFrame erforderlich.

```js
// Place this code in your parent window
function listenMessage(e) {
    if(e.data == "Example page view call") {
        s.pageName = "Page name using postMessage";
        s.t();
    }
}
window.addEventListener("message", listenMessage, false);

// Place this code in the iframe
window.top.postMessage("Example page view call","https://example.com");
```

## Einschränkungen

* Wie bei anderen JavaScript-Codes können iFrames nur dann kommunizieren, wenn Domains und Protokolle übereinstimmen. Diese Beispiele funktionieren nicht, wenn sich der IFrame-Inhalt in einer anderen Domain als die übergeordnete Domain befindet.
* Wenn sich „AppMeasurement“ in einem IFrame befindet, wird die [`referrer`](../vars/page-vars/referrer.md)-Variable auf die übergeordnete URL festgelegt und nicht auf die tatsächlich verweisende URL. Sie können zur Lösung dieses Problems die `referrer`-Variable manuell festlegen.
* Der [Adobe Experience Cloud-Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=de) erkennt keine Bildanforderungen, die innerhalb von iFrames ausgelöst werden.
* Activity Map zeigt die Heatmap nicht über Links an, auf die innerhalb von iFrames geklickt wurde. Stattdessen wird der gesamte IFrame hervorgehoben.
