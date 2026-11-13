---
title: Datenschicht erstellen
description: Erfahren Sie, wie eine Datenschicht Ihre Analytics-Implementierung unterstützt, warum Adobe die Adobe-Client-Datenschicht empfiehlt und wie Sie Datenschichtwerte mit jeder Implementierungsmethode lesen können.
feature: Implementation Basics
exl-id: 271dd8fa-3ba1-4a7f-b16a-c48a736a5bb5
role: Admin, Developer, Leader
TQID: 'https://experienceleague.adobe.com/JmxM3-AVA5--7Xt4kuES35KFtYbicdGO9JZXsygzuuE'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
  - id: a421fb65-2c82-457a-921c-28c46b697a39
    internal-label: Analytics basics
subfeature_v2:
  - id: df312454-73c4-43f6-a90e-18f5043f074c
    internal-label: Tags
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
    internal-label: Variables
  - id: c24fe15a-643a-47bd-8278-5e027df49785
    internal-label: Implementation basics
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 7151dca7425bfb99271db71a3132485f85941a5e
workflow-type: tm+mt
source-wordcount: '1063'
ht-degree: 7%
---
# Datenschicht erstellen

Eine Datenschicht ist eine JavaScript-Struktur auf Ihrer Site, die die von Ihrer Analytics-Implementierung erfassten Daten wie Seitennamen, Produktdetails und Auftrags-IDs verfügbar macht. Ihr Site-Code schreibt in die Datenschicht, und Ihre Implementierung liest daraus, um Analytics-Variablen festzulegen. Da Ihre Implementierung nicht von der HTML der Seite abhängt, können Sie Ihre Site neu gestalten, ohne die Datenerfassung zu unterbrechen.

## Voraussetzungen

[Lösungsentwurfsdokument erstellen](solution-design.md): Es ist wichtig, dass Ihr Unternehmen die Tracking-Anforderungen erfüllt. Stellen Sie sicher, dass Sie ein Solution-Design-Dokument vorbereitet haben, bevor Sie sich an die Entwicklungsteams in Ihrer Organisation wenden. Die Daten, die für Ihr Lösungsdesign erforderlich sind, bestimmen, was Ihre Datenschicht enthält.

## Datenschichtspezifikation auswählen {#specifications}

Adobe empfiehlt die [Adobe Client Data Layer](https://experienceleague.adobe.com/en/docs/experience-platform/collection/acdl/overview) (ACDL) für neue oder umstrukturierte Implementierungen. ACDL ist eine Open-Source-JavaScript-Bibliothek, die Ihrer Site eine Standardmethode zum Übertragen von Daten und Ereignissen in ein globales `adobeDataLayer`-Array bietet. Tags, der Web-SDK und AppMeasurement können alle daraus lesen, und Adobe Experience Manager-Kernkomponenten können es automatisch füllen.

Ihr Unternehmen kann andere Spezifikationen verwenden, z. B. die [Customer Experience Digital Data Layer](https://www.w3.org/2013/12/ceddl-201312.pdf) (CEDDL), die Daten in einem globalen `digitalData` speichert, oder eine benutzerdefinierte Spezifikation. Das Wichtigste ist, dass Ihr Unternehmen eine Spezifikation anwendet, die seinen Anforderungen entspricht.

In der folgenden Tabelle wird ACDL mit objektbasierten Datenschichten wie CEDDL verglichen:

| | Adobe Client-Datenschicht (`adobeDataLayer`) | Objektbasierte Datenschicht, z. B. CEDDL (`digitalData`) |
| --- | --- | --- |
| Schreiben von Daten durch Website-Code | Push-Objekte: `adobeDataLayer.push({ page: { name: "Home" } })` | Setzt Eigenschaften: `digitalData.page.pageInfo.pageName = "Home"` |
| Wie Ihre Implementierung einen Wert liest | `adobeDataLayer.getState("page.name")` oder ein Datenelement **berechneter Status der Datenschicht** aus der Adobe Client-Datenschicht-Tag-Erweiterung | `digitalData.page.pageInfo.pageName` oder ein Datenelement der **JavaScript** Variable aus der Core-Tag-Erweiterung |
| Wie Ihre Implementierung weiß, dass die Daten bereit sind | Der Site-Code überträgt ein Ereignis, z. B. `{ event: "page view" }`, und Ihre Implementierung überwacht es. Listener werden auch auf Ereignisse ausgeführt, die gepusht wurden, bevor sie hinzugefügt wurden. | Ihre Implementierung muss das -Objekt lesen, nachdem der Site-Code es vollständig ausgefüllt hat, z. B. mithilfe einer Direktaufruf-Regel. |

## Beispiel für eine Datenschicht {#example}

ACDL erfordert keine bestimmte Datenstruktur. Entwerfen Sie die Struktur um Ihr Lösungs-Design-Dokument und dokumentieren Sie es für alle, die in die Datenschicht schreiben oder aus ihr lesen. Die Beispiele in diesem Handbuch verwenden die folgende Struktur.

Beim Laden einer Seite überträgt der Site-Code die Daten der Seite und ein Seitenansichtsereignis:

```js
window.adobeDataLayer = window.adobeDataLayer || [];
window.adobeDataLayer.push({
  event: "page view",
  page: {
    name: "Home",
    section: "Products",
    url: "https://example.com/products",
    referrer: "https://example.com/"
  }
});
```

Wenn ein Besucher einen Kauf abschließt, überträgt der Site-Code die Bestelldetails und ein Kaufereignis:

```js
window.adobeDataLayer.push({
  event: "purchase",
  transaction: { id: "ABC123" },
  products: [
    { name: "Example product", category: "Example category", quantity: 1, price: 25 }
  ]
});
```

ACDL führt jeden Push in einem einzigen Objekt, dem so genannten berechneten Status, zusammen, das Ihre Implementierung liest. Ereignisobjekte teilen Ihrer Implementierung mit, wann sie sie lesen soll. Siehe [Daten und der berechnete Status](https://experienceleague.adobe.com/en/docs/experience-platform/collection/acdl/concepts/computed-state) und [Ereignisse](https://experienceleague.adobe.com/en/docs/experience-platform/collection/acdl/concepts/events).

## Workflow {#workflow}

Die Implementierung von Adobe Analytics mit einer Datenschicht folgt normalerweise diesen Schritten:

1. **Arbeiten Sie mit Ihrem Site-Entwicklungs-Team zusammen, um eine Datenschicht zu implementieren**: Ihr Site-Entwicklungs-Team ist in erster Linie dafür verantwortlich, sicherzustellen, dass die Datenschicht korrekte Werte enthält. Gehen Sie diese Seite mit Ihrem Website-Entwicklungsteam durch, um sicherzustellen, dass die Erwartungen zwischen den Teams abgestimmt sind. Siehe [Installieren der Adobe Client-Datenschicht](https://experienceleague.adobe.com/en/docs/experience-platform/collection/acdl/install).
1. **Datenschicht mithilfe einer Browser-Konsole validieren**: Öffnen Sie die Entwicklerkonsole Ihres Browsers, was in den meisten Browsern mit der `F12` möglich ist. Führen Sie `adobeDataLayer.getState()` aus, um den berechneten Status anzuzeigen, oder `adobeDataLayer.getState("page.name")`, um einen einzelnen Wert anzuzeigen. Siehe [Überprüfen der Installation](https://experienceleague.adobe.com/en/docs/experience-platform/collection/acdl/install#verify).
1. **Verbinden der Datenschicht mit Adobe Analytics**: Dieser Schritt variiert je nach Implementierungsmethode Ihres Unternehmens. Siehe [Verbinden der Datenschicht mit Adobe Analytics](#connect).

## Verbinden der Datenschicht mit Adobe Analytics {#connect}

Die folgende Tabelle zeigt, wie jede Implementierungsmethode aus der Adobe-Client-Datenschicht liest:

| Implementierungsmethode | Lesen der Datenschicht | Weitere Informationen |
| --- | --- | --- |
| Web SDK Tag-Erweiterung | Trigger-Regeln mit dem **Datenschicht-Push**-Ereignis aus der Adobe Client-Datenschicht-Erweiterung. Ordnen Sie Datenschichtwerte XDM-Feldern oder dem `data`-Objekt mit der Aktion „Variable aktualisieren **von Web SDK zu** senden Sie sie dann mit der Aktion **Ereignis senden** . | [Senden von Adobe Client-Datenschichtdaten mit der Web-](https://experienceleague.adobe.com/en/docs/experience-platform/collection/acdl/web-sdk), [XDM-Objektfeldzuordnung](../aep-edge/xdm-var-mapping.md) und [Datenobjektfeldzuordnung](../aep-edge/data-var-mapping.md) |
| Web SDK JavaScript-Bibliothek | Überwachen Sie mit `addEventListener()` auf Datenschichtereignisse und legen Sie XDM- oder `data`-Felder aus der Datenschicht fest, wenn Sie `sendEvent` aufrufen. | [Senden von Adobe Client-Datenschichtdaten mit der Web-](https://experienceleague.adobe.com/en/docs/experience-platform/collection/acdl/web-sdk), [XDM-Objektfeldzuordnung](../aep-edge/xdm-var-mapping.md) und [Datenobjektfeldzuordnung](../aep-edge/data-var-mapping.md) |
| Analytics-Erweiterung | Trigger-Regeln mit dem **Datenschicht-Push**-Ereignis und Erstellen von **Datenschicht-Status berechnet**-Datenelementen aus der Adobe Client-Datenschichterweiterung. Weisen Sie die Datenelemente den Analytics-Variablen in der Aktion **Variablen festlegen** zu und senden Sie dann die Daten mit der Aktion **Beacon senden**. | [Zuordnen von Datenschichtobjekten zu Datenelementen](../launch/layer-to-elements.md) und [Zuordnen von Datenelementen zu Analytics-Variablen](../launch/elements-to-variable.md) |
| AppMeasurement | Lesen Sie Werte mit `getState()`, nachdem ACDL geladen wurde, und rufen Sie dann `s.t()` auf. | [Lesen der Datenschicht mit AppMeasurement](#appmeasurement) |

### Lesen der Datenschicht mit AppMeasurement {#appmeasurement}

ACDL fügt seine `getState()` Methode dem `adobeDataLayer`-Array hinzu, wenn die Bibliothek geladen wird. Um sicherzustellen, dass die Bibliothek geladen wurde und der berechnete Status die neuesten Daten enthält, lesen Sie Werte in einem Ereignis-Listener:

```js
window.adobeDataLayer = window.adobeDataLayer || [];
window.adobeDataLayer.push(function(dl) {
  dl.addEventListener("page view", function(event) {
    s.pageName = dl.getState("page.name");
    s.channel = dl.getState("page.section");
    s.t();
  });
});
```

Der Listener wird einmal für jedes `page view`-Ereignis ausgeführt, einschließlich der Ereignisse, die gepusht wurden, bevor der Listener hinzugefügt wurde. Die Variablenseiten in diesem Handbuch, z. B. [`pageName`](../vars/page-vars/pagename.md), zeigen, wie einzelne Werte mit `getState()` gelesen werden. Verwenden Sie diese Beispiele in einem Listener wie diesem oder im benutzerdefinierten Code-Editor einer Analytics-Erweiterungsregel, die ein „Datenschicht **Push-Ereignis**.

Wenn Ihre Implementierung mehr als einen Treffer pro Seite sendet, z. B. in einem Einzelseitenprogramm, verwenden Sie [`clearVars()`](../vars/functions/clearvars.md), damit die Werte von einem Treffer nicht zum nächsten beibehalten werden.

## Nächste Schritte

* [Zuordnen von Datenschichtobjekten zu Datenelementen](../launch/layer-to-elements.md): Verwenden Sie die Datenschicht Ihrer Site in Adobe Experience Platform-Tags.
* [Dokumentation zur Adobe Client-Datenschicht](https://experienceleague.adobe.com/en/docs/experience-platform/collection/acdl/overview): Erfahren Sie mehr über alle ACDL-Methoden, -Ereignisse und Best Practices.
