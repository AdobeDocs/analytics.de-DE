---
title: Implementieren mit AMP
description: Implementieren Sie Adobe Analytics auf AMP-Seiten.
feature: Implementation Basics
exl-id: 51a2662e-2a24-48f1-b17a-d1e1a57a394b
role: Developer
TQID: https://experienceleague.adobe.com/lEnXPmYFhMOlvL-au9C-MtGiKY5b84ojYska3urtH1M
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2:
  - id: e6c28e30-8689-4bf4-8fa8-561343d308a9
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: a947d2d7f45d4155a61cbfe0f8110851cca32e60
workflow-type: tm+mt
source-wordcount: 939
ht-degree: 66%

---

# Implementieren mit AMP

[AMP](https://amp.dev) ist ein Open-Source-HTML-Framework, um auf einfache Weise schnell und problemlos ladende Webseiten zu erstellen.

Da Adobe Analytics zum Kompilieren und Senden einer Bildanforderung eine JavaScript-Bibliothek verwendet, sind Anpassungen in Ihrer Implementierung erforderlich, um Daten auf Seiten mit AMP an Adobe zu senden.

## Festlegen der Methode zum Implementieren von Adobe Analytics auf Seiten mit AMP

Adobe bietet zwei Methoden zum Implementieren von Adobe Analytics auf Seiten mit AMP. Beide verwenden das HTML-Tag `<amp-analytics>`. Weitere Informationen finden Sie [amp](https://amp.dev/de/documentation/components/amp-analytics)analytics“ in der Dokumentation von AMP.

* **Verwenden der `"adobeanalytics"`-Vorlage**: Erstellen Sie die Analytics-Anfrage direkt auf der Seite
* **Verwenden der `"analytics_nativeConfig"`-Vorlage**: Verwenden Sie einen iframe, der denselben AppMeasurement-Code enthält, den Sie auf Ihrer normalen Site bereitstellen

In der folgenden Tabelle werden die beiden Methoden verglichen:

|   | **`"adobeanalytics"`Vorlage** | **`"adobeanalytics_nativeConfig"`Vorlage** |
|---|---|---|
| Besucher-/Besuchsanzahlen in bestehender Report Suite | Hohe Inflation | Minimale Inflation |
| Separate Report Suite verwenden | Empfohlen | Nicht erforderlich |
| Neue und wiederkehrende Besucher | Nicht unterstützt | Unterstützt |
| Besucher-ID-Dienst (`VisitorAPI.js`) | Nicht unterstützt | Unterstützt |
| Video- und Linktracking | Teilweise unterstützt | Noch nicht unterstützt |
| Schwierigkeiten bei der Umsetzung | diffizil | Relativ einfach |
| Adobe CX Enterprise-Integrationen | Nicht unterstützt | Teilweise unterstützt |

Wägen Sie die Vor- und Nachteile ab, sodass Sie die beste Implementierungsmethode für Ihr Unternehmen auswählen können.

>[!WARNING]
>
>Verwenden Sie mit AMP nicht sowohl die `"adobeanalytics"`- als auch die `"adobeanalytics_nativeConfig"`-Vorlage auf derselben Seite. Wenn Sie dies versuchen, können Sie Fehler in der Browser-Konsole erzeugen und Besucher doppelt zählen.

## Methode 1: Verwenden des `<amp-analytics>`-Tags mit der `"adobeanalytics"`

Die Tracking-Vorlage `"adobeanalytics"` nutzt das `<amp-analytics>`-HTML-Tag, um direkt eine Tracking-Anforderung zu erstellen. Sie können Trefferanforderungen angeben, die bei bestimmten Seitenereignissen ausgelöst werden, z. B. bei der Anzeige der Seite oder bei einem Klick. Klickereignisse können angepasst werden, um sie auf bestimmte Element-IDs oder Klassen anzuwenden, indem eine Auswahl angegeben wird. Sie können die Vorlage laden, indem Sie `type="adobeanalytics"` zum amp-analytics-Tag hinzufügen.

Im folgenden Code-Beispiel wurden zwei Auslöser definiert: `pageLoad` und `click`. Der Auslöser `pageLoad` erfolgt, wenn das Dokument sichtbar wird und die `pageName`-Variable, wie im `vars`-Abschnitt definiert, enthält. Der zweite Auslöser `click` erfolgt beim Klick auf eine Schaltfläche. Die `eVar1`-Variable wird für dieses Ereignis mit dem Wert `button clicked` festgelegt.

```html
<amp-analytics type="adobeanalytics">
  <script type="application/json">
    {
      "requests": {
        "myClick": "${click}&v1=${eVar1}",
      },
      "vars": {
        "host": "example.data.adobedc.net",
        "reportSuites": "reportSuiteID1,reportSuiteID2",
        "pageName": "Adobe Analytics Using amp-analytics tag"
      },
      "triggers": {
        "pageLoad": {
          "on": "visible",
          "request": "pageview"
        },
        "click": {
          "on": "click",
          "selector": "button",
          "request": "myClick",
          "vars": {
            "eVar1": "button clicked"
          }
        }
      }
    }
  </script>
</amp-analytics>
```

Das `<amp-analytics>`-Tag unterstützt Variablenersetzungen, damit AMP ihm bekannte Datenwerte bereitstellen kann. Weitere Informationen finden [&#x200B; unter „In `amp-analytics`](https://github.com/ampproject/amphtml/blob/main/extensions/amp-analytics/analytics-vars.md) unterstützte Variablen“ auf GitHub.

>[!NOTE]
>
>Bildanfragen, die mit dieser Methode an Adobe gesendet werden, enthalten keine Daten für viele Standardberichte (beispielsweise Browser, Bildschirmgröße oder Referrer). Wenn Sie diese Informationen in Treffer einbeziehen möchten, stellen Sie sicher, dass sie als Teil der Abfragezeichenfolge der Bildanforderung enthalten sind. Siehe [Datenerfassungs-Abfrageparameter](../validate/query-parameters.md) für eine vollständige Liste der Bildanforderungsparameter und der zugehörigen Variablen.

Adobe identifiziert Besucher mithilfe einer integrierten AMP-Funktion und setzt das `adobe_amp_id`-Cookie. Diese Besucher-ID ist eindeutig für jede andere ID, die von Adobe Analytics festgelegt wird. Für jedes CDN, von dem ein Besucher Inhalte abruft, wird ein anderer Unique Visitor gezählt, wodurch sich die Unique Visitor-Anzahl erhöhen kann. Die Verwendung einer separaten Report Suite für AMP-Seiten wird dringend empfohlen, da AMP Unique Visitors identifiziert. Der Besucher-ID-Dienst von Adobe wird nicht unterstützt.

Bei dieser Lösung muss der von Ihnen in der `host`-Eigenschaft festgelegte Trackingserver dem Trackingserver auf Ihrer Haupt-Website entsprechen, damit Ihre Datenschutzrichtlinien eingehalten werden. Andernfalls erstellen Sie eine separate Datenschutzrichtlinie für Seiten, die AMP verwenden.

## Methode 2: Verwenden des `<amp-analytics>`-Tags mit der `"adobeanalytics_nativeConfig"`

Das `"adobeanalytics_nativeConfig"`-Tag ist einfacher zu implementieren, da es dieselbe Tagging-Methode wie auf Ihren normalen Websites nutzt. Fügen Sie Ihrem `amp-analytics`-Tag Folgendes hinzu:

```html
<amp-analytics type="adobeanalytics_nativeConfig">
  <script type="application/json">
    {
      "requests": {
        "base": "https://${host}",
        "iframeMessage": "${base}/stats.html?campaign=${queryParam(campaign)}&pageURL=${ampdocUrl}&ref=${documentReferrer}"
      },
      "vars": {
        "host": "example.data.adobedc.net"
      },
      "extraUrlParams": {
      "pageName": "Example AMP page",
      "v1": "eVar1 example value"
      }
    }
 </script>
</amp-analytics>
```

Außerdem ist eine auf Ihren Webservern gehostete HTML-Seite erforderlich:

```html
<html>
  <head>
    <title>Stats Example</title>
    <script language="JavaScript" type="text/javascript" src="VisitorAPI.js"></script>
    <script language="JavaScript" type="text/javascript" src="AppMeasurement.js"></script>
  </head>
  <body>
    <script>
      var v_orgId = "INSERT-ORG-ID-HERE";
      var s_account = "examplersid1,examplersid2";
      var s_trackingServer = "example.data.adobedc.net";
      var visitor = Visitor.getInstance(v_orgId);
      visitor.trackingServer = s_trackingServer;
      var s = s_gi(s_account);
      s.account = s_account;
      s.trackingServer = s_trackingServer;
      s.visitorNamespace = s_visitorNamespace;
      s.visitor = visitor;
      s.pageName = s.Util.getQueryParam("pageName");
      s.eVar1 = s.Util.getQueryParam("v1");
      s.campaign = s.Util.getQueryParam("campaign");
      s.pageURL = s.Util.getQueryParam("pageURL");
      s.referrer = s.Util.getQueryParam("ref");
      s.t();
    </script>
  </body>
</html>
```

Bei diesem Ansatz werden Daten über Abfragezeichenfolgenparameter, die dem `iframeMessage`-Abfrageparameter hinzugefügt werden, an eine Dienstprogramm-Website gesendet. Diese Abfragezeichenfolgenparameter können beliebig benannt werden, solange Ihre `stats.html`-Seite so konfiguriert ist, dass sie die entsprechenden Daten daraus erfassen kann.

Die `"adobeanalytics_nativeConfig"` fügt auch Abfragezeichenfolgenparameter hinzu, die auf den im `extraUrlParams` des `<amp-analytics>`-Tags aufgelisteten Variablen basieren. Im obigen Beispiel werden die Parameter `pageName` und `v1` einbezogen.

>[!IMPORTANT]
>
>Ihre `stats.html`-Seite muss in einer anderen Unterdomäne als der Domain gehostet werden, in der AMP selbst gehostet wird. Das AMP-Framework lässt keine iFrames aus derselben Unterdomäne zu, in der sich die AMP-Seite selbst befindet. Wenn Ihr AMP beispielsweise auf `amp.example.com` gehostet wird, hosten Sie Ihre `stats.html`-Seite in einer anderen Unterdomäne wie `ampmetrics.example.com`.

Wenn ein Benutzer bei dieser Methode das Tracking auf Ihrer primären Website deaktiviert, wird das Tracking auf all Ihren AMPs ebenfalls deaktiviert. Die Verwendung dieser Service-Seite bedeutet auch, dass AMP den Besucher-ID-Service von Adobe unterstützen kann. Eine separate Report Suite ist nicht erforderlich.

Mit dieser Methode können Linktracking und die Video-Tracking nicht verwendet werden. Das `iframeMessage`-Tag in AMP kann nur einmal pro Seite geladen werden, sodass Sie keine anderen Bildanforderungen senden können, nachdem der Frame geladen wurde. Diese Methode erfordert auch mehr Verarbeitungsressourcen, was sich auf die Bildlaufleistung auswirken kann. Diese Methode hat keine Auswirkungen auf die Seitenladezeit, da alle Ressourcen asynchron geladen werden.

## Häufig gestellte Fragen

**Wie können AMP-Besucher in den Daten von anderen unterschieden werden?**

Die Dimension [!UICONTROL JavaScript-Version] erfasst für alle AMP-Seiten einen Wert ähnlich `AMP vX.X`. Sie können auch eine benutzerdefinierte Dimension auf „AMP“ festlegen, damit Sie diese Besucher segmentieren können.

**Wie ist diese Implementierungsmethode mit Facebook Instant Articles zu vergleichen?**

Facebook Instant Articles unterstützt eine ähnliche Lösung wie die `"adobeanalytics_nativeConfig"`-Methode. Die `stats.html`-Seite für diese Methode kann Ihre Analyseanforderungen für AMP und FIA gleichzeitig erfüllen. Weitere Informationen zur Tracking-Implementierung auf FIA finden Sie unter [Facebook Instant Articles](fb-instant-articles.md).
