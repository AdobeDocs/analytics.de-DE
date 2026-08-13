---
title: Implementieren mit AJAX
description: Erfahren Sie, wie Sie Adobe Analytics mit AJAX auf einer Website implementieren.
feature: Implementation Basics
exl-id: 3286bf97-3a66-4f68-9053-bf84269962fd
role: Developer
autotag-review: '2026-05-22T08:06:40.936Z'
TQID: 'https://experienceleague.adobe.com/M0MNFZRcHpPwxL-ZtTky67DHDr1A0fL-peaGKicXgIM'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: e4f5f438-eabb-4c54-9133-b817e3d125f5
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 373
ht-degree: 100%

---

# Implementieren mit AJAX

Bei AJAX werden JavaScript und HTML verwendet, um Inhalte zu löschen und zu generieren, ohne eine neue Seite zu laden.

Adobe Analytics verlässt sich normalerweise darauf, dass Seiten neu geladen werden, um das Analytics-Tracking-Objekt zurückzusetzen. Jedes Mal, wenn Sie zu einer anderen URL navigieren, werden alle Analytics-Variablen zurückgesetzt und können erneut definiert werden. Wenn Sie AJAX auf Ihrer Website verwenden, passen Sie Ihre Implementierung an das Fehlen von Seitenaktualisierungen an, um sicherzustellen, dass die Daten zwischen den Treffern nicht fälschlicherweise beibehalten werden.

Sobald Sie Maßnahmen zum Löschen von Variablenwerten getroffen haben, entspricht die Implementierung von Adobe Analytics auf Websites, die AJAX verwenden, größtenteils denen anderer Implementierungsmethoden.

## Interaktionen und Treffertypen festlegen

Da Seiten, die AJAX verwenden, in der Regel nicht neu geladen werden, gibt es mehrere Interaktionen, die ein Benutzer auf Ihrer Website ausführen kann. Achten Sie bei der Implementierung von Adobe Analytics darauf, Seitenansichten von Linktracking-Aufrufen zu unterscheiden. Berücksichtigen Sie die folgende Frage für jede Interaktion, die ein Benutzer auf Ihrer Website ausführen kann:

*Wenn ein Benutzer mit meiner Website interagiert, verändert diese Interaktion genug vom Inhalt der Seite, um als neue Seite zu gelten?*

* Wenn die Antwort **ja** ist, sollten Sie einen Tracking-Aufruf für Seitenansichten (`s.t()`) verwenden.
* Wenn die Antwort **nein** ist, sollten Sie diese Interaktion mit einem Linktracking-Aufruf (`s.tl()`) verfolgen.

>[!NOTE]
>
>Nicht alle Interaktionen oder Klicks müssen aufgezeichnet werden. Überlegen Sie genau, welche Aktionen am wichtigsten sind, um sie zu verfolgen, und senden Sie die Daten entsprechend an Adobe.

## Variablen auf jeder Seite löschen

Variablenwerte bleiben auf Seiten mit AJAX erhalten, da die Seite nicht neu geladen wird. Daher sind spezielle Vorkehrungen erforderlich, um Variablenwerte zu löschen, damit sie nicht fälschlicherweise über Treffer hinweg bestehen bleiben. Adobe bietet die [`clearVars`](../vars/functions/clearvars.md)-Funktion zum einfachen Löschen von Variablenwerten. Stellen Sie sicher, dass Sie diese Funktion verwenden, nachdem Sie jeden Treffer an Adobe gesendet haben und bevor Sie Variablenwerte für den nächsten Treffer festlegen.

>[!TIP]
>
>Die `clearVars()`-Funktion ist in H-Code nicht verfügbar. Wenn Sie noch nicht auf AppMeasurement aktualisiert haben, setzen Sie jeden Analytics-Variablenwert auf eine leere Zeichenfolge.

## Beispiele

Im folgenden Beispiel wird einfaches JavaScript verwendet, um vorhandene Variablenwerte zu löschen, neue Werte festzulegen und dann eine Bildanforderung an Adobe zu senden:

```js
s.clearVars();
s.pageName = "Example AJAX page";
s.eVar1="Example value";
void(s.t());
```

In dem folgenden Beispiel wird ein Tracking-Aufruf im Callback `done` der JQuery-`.ajax`-Funktion veranschaulicht:

```js
$.ajax({
  url: "example.html",
  dataType: "html"
})
  .done(function( response ) {
    $( "#content" ).html( response );
  s.clearVars();
  s.pageName = $( "h1:first" ).text();
  s.t();
  });
```
