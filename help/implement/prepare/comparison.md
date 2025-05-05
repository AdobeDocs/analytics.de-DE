---
title: Vergleich von Implementierungsmethoden
description: Erfahren Sie mehr über die Vorteile jeder Methode zum Datenversand an Adobe Analytics.
exl-id: 19353255-6356-4426-a2ef-5a2672a00eca
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: c476a1a19ae514f75fce8bd8e6d447d85de67a84
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 41%

---

# Vergleich von Implementierungsmethoden

Hier finden Sie einen Vergleich der Implementierungsmethoden von Adobe Analytics. Mithilfe dieser Tabellen können Sie für Ihr Unternehmen die optimale Methode zum Senden von Daten an Adobe ermitteln. Klicken Sie auf die einzelnen Spalten, um genauere Informationen anzuzeigen.

## Web

| | [AppMeasurement](/help/implement/js/overview.md) | [Adobe Analytics-Erweiterung](/help/implement/launch/overview.md) | [Web SDK](/help/implement/aep-edge/web-sdk/overview.md#web-sdk) | [Web SDK-Erweiterung](/help/implement/aep-edge/web-sdk/overview.md#web-sdk-extension) |
| --- | --- | --- | --- | --- |
| Implementierungsanforderungen | Referenzieren Sie `AppMeasurement.js` auf jeder Seite, definieren Sie Variablen, senden Sie Daten mit `s.t()` an Adobe Analytics | Referenzieren Sie Tag-Lader auf jeder Seite, verwenden Sie die Datenerfassungs-Benutzeroberfläche, um Variablen zu definieren und Daten an Adobe Analytics zu senden | Referenzieren Sie `Alloy.js` auf jeder Seite, verwenden Sie `alloy("sendEvent",{})`, um XDM-Objekte zu erstellen und die gewünschten Daten mithilfe von Edge Network an Adobe Analytics zu senden | Referenzieren Sie Tag-Lader auf jeder Seite, verwenden Sie die Datenerfassungs-Benutzeroberfläche, um XDM-Objekte zu erstellen und die gewünschten Daten mithilfe von Edge Network an Adobe Analytics zu senden |
| Datenziel | Direkt an Adobe Analytics gesendet | Direkt an Adobe Analytics gesendet | An Adobe Experience Platform Edge gesendet, von wo die Daten an Adobe Analytics weitergeleitet werden | An Adobe Experience Platform Edge gesendet, von wo die Daten an Adobe Analytics weitergeleitet werden |
| Schwierigkeiten bei der Anpassung der Implementierung | Erfordert bei jeder Implementierungsänderung Zugriff auf den Website-Code | Ändern Sie den Website-Code einmal, um das Lader-Tag zu installieren. Alle weiteren Implementierungsaktualisierungen können in der Datenerfassungs-Benutzeroberfläche vorgenommen werden | Erfordert bei jeder Implementierungsänderung Zugriff auf den Website-Code | Ändern Sie den Website-Code einmal, um das Lader-Tag zu installieren. Alle weiteren Implementierungsaktualisierungen können in der Datenerfassungs-Benutzeroberfläche vorgenommen werden |
| Handhabung von A4T | A4T-Aufrufe sind in Treffern enthalten, die an Adobe gesendet werden | A4T-Aufrufe sind in Treffern enthalten, die an Adobe gesendet werden | A4T-Aufrufe werden als separate Treffer gesendet | A4T-Aufrufe werden als separate Treffer gesendet |
| Kontextdaten | Verwenden Sie `s.contextData`. | Verwenden von `s.contextData` in benutzerdefinierten Code-Blöcken | Alle nicht zugeordneten Felder werden automatisch `a.x.*` Kontextdatenvariablen gesendet. | Alle nicht zugeordneten Felder werden automatisch `a.x.*` Kontextdatenvariablen gesendet. |

{style="table-layout:auto"}

## Mobile und andere

>[!CAUTION]
>
>Die Unterstützung für Mobile SDKs Version 4 endete am 31. August 2021. Weitere Informationen finden Sie in den Häufig gestellten Fragen zum Ende der Nutzungsdauer [&#128279;](https://experienceleague.adobe.com/docs/discontinued/using/mobile-services.html?lang=de)Adobe Mobile Services).


| | [Mobile SDK](/help/implement/aep-edge/mobile-sdk/overview.md) | [Server-API](/help/implement/aep-edge/server-api/overview.md) |
| --- | --- | --- |
| Implementierungsanforderungen | Referenzieren Sie Tag-Lader in der App und verwenden Sie dann direkte API-Aufrufe oder Regeln in der Datenerfassungs-Benutzeroberfläche, um XDM-Objekte zu erstellen und die gewünschten Daten mithilfe von Edge Network an Adobe Analytics zu senden | Verwenden Sie Edge Network-Server-APIs, um XDM-Objekte zu erstellen und die gewünschten Daten mithilfe von Edge Network an Adobe Analytics zu senden |
| Datenziel | An Adobe Experience Platform Edge gesendet, von wo die Daten an Adobe Analytics weitergeleitet werden | An Adobe Experience Platform Edge gesendet, von wo die Daten an Adobe Analytics weitergeleitet werden |
| Schwierigkeiten bei der Anpassung der Implementierung | Ändern Sie den App-Code, an dem direkte API-Aufrufe durchgeführt werden, oder nehmen Sie Änderungen an der Datenerfassungs-Benutzeroberfläche vor | Erfordert bei jeder Implementierungsänderung Zugriff auf den Anwendungs-Code |
| Handhabung von A4T | A4T-Aufrufe werden als separate Treffer gesendet | A4T-Aufrufe werden als separate Treffer gesendet |
| Kontextdaten | Alle nicht zugeordneten Felder werden automatisch `a.x.*` Kontextdatenvariablen gesendet. | Alle nicht zugeordneten Felder werden automatisch `a.x.*` Kontextdatenvariablen gesendet |

{style="table-layout:auto"}
