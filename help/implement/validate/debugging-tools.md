---
title: Debugging-Tools für Analytics-Implementierungen
description: Überprüfen Sie die Daten, die Ihre Implementierung an Adobe sendet, mithilfe von Analytics-Debuggern, Browser-Entwickler-Tools und HTTP-Debugging-Proxys.
keywords: Paketanalysator, Paketmonitor, Paket-Sniffer, Debugger, Charles, NS_BINDING_ABORTED, sendBeacon
feature: Implementation Basics
exl-id: db077293-f72c-4933-8a30-f1e1963f332e
role: Admin, Developer, Leader
TQID: 'https://experienceleague.adobe.com/debgxI3FK1fp1Q02GY1-0H40z-L4G2HSmq11Tog97-Y'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: a421fb65-2c82-457a-921c-28c46b697a39
    internal-label: Analytics basics
subfeature_v2:
  - id: e992d880-33bc-4949-a648-aa7d410276cd
    internal-label: Validation
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
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 319f78bb5f8c2449a7263e3f1c378c49656889a7
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 3%
---
# Debugging-Tools für Analytics-Implementierungen

Mit Debuggingwerkzeugen, manchmal auch als Paketanalysatoren oder Paketschnüffler bezeichnet, können Sie die Daten überprüfen, die Ihre Implementierung an Adobe sendet. Diese können Ihnen dabei helfen, zu überprüfen, ob Anforderungen erfolgreich ausgelöst werden, die in diesen Anforderungen enthaltenen Variablen und Payloads zu überprüfen und ein unerwartetes Implementierungsverhalten zu beheben.

>[!NOTE]
>
>Die auf dieser Seite aufgelisteten Tools sind nicht vollständig. Sie stellen Tools dar, die Adobe Analytics-Kunden nützlich fanden. Mit Ausnahme der von Adobe bereitgestellten Tools unterstützt oder behebt Adobe diese Produkte nicht. Informationen zur Installation, Verwendung und zum Support erhalten Sie beim Herausgeber des Tools.

## Debugging-Tool auswählen

Die folgenden Kategorien können Ihnen bei der Auswahl eines Tools helfen, das auf dem basiert, was Sie untersuchen möchten.

| Tool-Typ | Nützlich, wenn |
| --- | --- |
| **Analytics- und Tag-Debugger** | Analytics-Variablen, Tags, Datenschichten oder Sammlungsanfragen sollen in einem für Menschen lesbaren Format interpretiert und dargestellt werden. |
| **Browser-Entwickler-Tools** | Sie debuggen eine Web-Implementierung und möchten Netzwerkanfragen direkt untersuchen, ohne eine separate Debugging-Anwendung zu installieren. |
| **HTTP(S)-Debugging-Proxys** | Sie möchten den HTTP-Traffic von Browsern, mobilen Apps, WebViews, APIs oder anderen Clients untersuchen oder benötigen Funktionen, die über Browser-Entwickler-Tools hinausgehen. |

## Analytics- und Tag-Debugger

Analytics- und Tag-Debugger erkennen Analytics-Technologien und interpretieren deren Anfragen. Diese Tools können die Identifizierung von Adobe Analytics-Variablen, Experience Platform Web SDK-Payloads, Tags und zugehörigen Implementierungsinformationen erleichtern, ohne Netzwerkanfragen manuell zu decodieren.

| Tool | Verfügbarkeit | Nützlich für | Zu beachten |
| --- | --- | --- | --- |
| **[Adobe Experience Platform Debugger](https://experienceleague.adobe.com/de/docs/experience-platform/debugger/home)** | Browser-Erweiterung | Debugging von Adobe Experience Platform- und CX Enterprise-Implementierungen, einschließlich Adobe Analytics, Tags, Datenschichten und Experience Platform Web SDK | Von Adobe bereitgestelltes Tool mit Fokus auf Adobe-Technologien |
| **[Omnibug](https://omnibug.io)** | Chromium-basierte Browser und Firefox | Dekodieren von Adobe Analytics, Experience Platform Web SDK, Adobe-Tags und Anfragen vieler anderer Analyse- und Marketing-Anbieter | Nützlich für Implementierungen, die Technologien verschiedener Anbieter enthalten |
| **[ObservePoint Debugger](https://www.observepoint.com/solutions/observepoint-debugger/)** | Chrome und Edge | Prüfen und Dekodieren von Analyse-, Marketing- und Messtags, einschließlich Adobe Analytics-Anfragen | Browser-basierter Debugger; ObservePoint bietet auch separate automatisierte Implementierungs-Validierungsprodukte |
| **[Adobe Experience Platform Assurance](https://experienceleague.adobe.com/de/docs/experience-platform/assurance/home)** | Web-Anwendung in CX Enterprise | Überprüfen und Validieren von Ereignissen aus mobilen SDK-Implementierungen und Ermitteln, wie Edge Network Ereignisse verarbeitet hat | Von Adobe bereitgestelltes Tool; App mit einer Assurance-Sitzung verbinden, um die Ereignisse anzuzeigen |

## Browser-Entwickler-Tools

Jeder moderne Browser verfügt über Entwickler-Tools, die Netzwerkanfragen untersuchen können, sodass Sie häufig kein separates Tool benötigen, um eine Web-Implementierung zu debuggen. Drücken Sie **F12** oder **Strg+Umschalt+I** (Windows und Linux) oder **Befehlstaste+Wahltaste+I** (macOS) und wählen Sie dann die Registerkarte **Netzwerk** aus. Aktivieren Sie in Safari zunächst die Entwicklerfunktionen in den Safari-Einstellungen **Erweitert**.

## HTTP(S)-Debugging-Proxys

HTTP-Debugging-Proxys fangen den HTTP- und HTTPS-Traffic zwischen einem Client und einem Server ab. Sie sind nützlich, wenn Browser-Entwickler-Tools keine ausreichende Sichtbarkeit bieten oder wenn die Implementierung außerhalb eines herkömmlichen Webbrowsers ausgeführt wird.

Die HTTPS-Inspektion erfordert im Allgemeinen, dass der Client so konfiguriert wird, dass er einem vom Debugging-Proxy bereitgestellten Zertifikat vertraut. Befolgen Sie die Sicherheitsrichtlinien Ihrer Organisation, wenn Sie Zertifikate installieren oder verschlüsselten Traffic abfangen.

| Tool | Nützlich für |
| --- | --- |
| **[Charles](https://www.charlesproxy.com/)** | Überprüfen von Browser-, Anwendungs-, Mobilgerät- und anderem HTTP(S)-Traffic |
| **[Fiddler Everywhere](https://www.telerik.com/fiddler/fiddler-everywhere)** | Erfassen und Überprüfen des HTTP(S)-Traffics über Anwendungen und Geräte hinweg. Unterscheiden Sie sich vom älteren Fiddler Classic-Produkt. |
| **[proxyman](https://proxyman.com/)** | Überprüfen und Ändern des HTTP(S)-Traffics von Browsern, Anwendungen und Mobilgeräten |
| **[HTTP-Toolkit](https://httptoolkit.com/)** | Untersuchen des Traffics von Anwendungen, APIs, Entwicklungsumgebungen und Mobilgeräten mit Workflows, die auf Anwendungs- und API-Debugging ausgerichtet sind |
| **[mitmProxy](https://www.mitmproxy.org/)** | Abfangen, Überprüfen und Ändern von skriptfähigen HTTP(S)-Abfragen über Befehlszeilen- und Web-Schnittstellen. Am besten geeignet für Benutzer, die mit Befehlszeilen-Workflows vertraut sind. |

## Adobe Analytics-Anfragen suchen

Bei Implementierungen, die Daten direkt an Adobe Analytics senden, z. B. AppMeasurement, filtern Sie Netzwerkanfragen nach:

```text
/ss/
```

Adobe Analytics-Sammlungsanfragen enthalten Analytics-Variablen in der Anfrage-URL oder Payload. Rohanfragen verwenden Abfrageparameternamen anstelle von Variablennamen. Beispielsweise wird eVar1 als `v1` und prop1 als `c1` angezeigt. Analytics-Debugger decodieren diese Namen für Sie. Informationen zum eigenständigen Decodieren finden Sie unter [Variablenverweis](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference) in der Dokumentation zur Dateneinfüge-API .

Die HTTP-Status-Codes, die die Analytics-Datenerfassungs-Server zurückgeben, finden Sie [HTTP-Antwort-Codes](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/troubleshooting#http-response-codes) in der Dokumentation zur Data Insertion API.

Für Implementierungen, die Adobe Experience Platform Web SDK verwenden, filtern Sie Netzwerkanfragen nach:

```text
/ee/
```

Wählen Sie die Anfrage aus und überprüfen Sie deren Payload, um die an Adobe Experience Platform Edge Network gesendeten Daten anzuzeigen. Web SDK sendet Daten an Edge Network, die dann Daten an Adobe Analytics und andere konfigurierte Services weiterleiten können. Die Überprüfung der Client-Anfrage überprüft, was der Browser an die Edge Network gesendet hat. Sie bestätigt nicht von sich aus, dass die Daten von jedem nachgelagerten Service erfolgreich verarbeitet wurden. Um zu sehen, wie Edge Network ein Ereignis verarbeitet hat, verwenden Sie [Adobe Experience Platform Assurance](https://experienceleague.adobe.com/de/docs/experience-platform/assurance/home).

## Abgebrochene Anfragen

Wenn eine Seite die Seite verlässt, kann der Browser Anfragen abbrechen, die noch in Bearbeitung sind. Firefox kennzeichnet diese Anfragen `NS_BINDING_ABORTED`; Chrome und Edge kennzeichnen sie `(canceled)`. Um Anfragen nach der Navigation sichtbar zu halten, aktivieren Sie **Protokoll beibehalten** (Chrome und Edge) oder **Protokolle beibehalten** (Firefox).

Eine abgebrochene Anfrage bedeutet nicht unbedingt, dass Daten verloren gegangen sind. Der Browser hat möglicherweise die vollständige Anfrage gesendet und nur auf die Antwort gewartet. Browser-Entwickler-Tools können den Unterschied normalerweise nicht anzeigen, ein HTTP-Debugging-Proxy jedoch schon.

Anfragen, die mit `navigator.sendBeacon()` gesendet werden, werden bei der Navigation nicht abgebrochen. AppMeasurement verwendet `sendBeacon` für Exitlinks und immer dann, wenn [`useBeacon`](/help/implement/vars/config-vars/usebeacon.md) aktiviert ist. Web SDK verwendet sie für Ereignisse, die mit [`documentUnloading`](https://experienceleague.adobe.com/de/docs/experience-platform/collection/js/commands/sendevent/documentunloading) gesendet werden. Wenn Linktracking-Anfragen häufig abgebrochen werden, verwenden Sie diese Optionen.
