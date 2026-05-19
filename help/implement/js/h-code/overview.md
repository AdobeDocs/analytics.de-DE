---
title: Übersicht über die JavaScript-Implementierung mit H-Code
description: Erfahren Sie mehr über den Workflow zur Implementierung von H-Code auf Ihrer Website.
feature: Implementation Basics
exl-id: cf83d8fe-a3b1-4e65-a86a-7eeaf555651b
role: Developer
TQID: https://experienceleague.adobe.com/tcREdTxSH3L5XcCcu3W1aEQySJSDyAzrlQgyrutcUds
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 7d733a6375f6c6009563bc53f5a3ff090dbc48ed
workflow-type: tm+mt
source-wordcount: 388
ht-degree: 73%

---

# Übersicht über die JavaScript-Implementierung mit H-Code

>[!IMPORTANT]
>
>Diese Version der Datenerfassung wird nicht mehr unterstützt. Aktualisieren Sie auf entweder [Tags in Adobe Experience Platform](../../launch/overview.md) oder [AppMeasurement für JavaScript](../overview.md).

Sie müssen Zugriff auf Ihre Hostingserver haben, um eine Seite mit Code zur Datenerfassung erfolgreich implementieren zu können. Anhand der folgenden Schritte werden Sie durch eine grundlegende Analytics-Implementierung mit H-Code geführt.

>[!NOTE]
>
>Sie müssen bereits über eine vorhandene Kopie von `s_code.js` verfügen, um diese Anweisungen zu befolgen. Adobe bietet keine Möglichkeit mehr, H-Code im Code-Manager herunterzuladen.

1. **JS-Hauptdateivariablen aktualisieren**: Bearbeiten Sie die `s_code.js`-Datei und stellen Sie sicher, dass die folgenden Variablen aktualisiert werden:
   * `s_account` enthält die Report Suite-ID, an die Sie Daten senden möchten. Siehe
   * `s.trackingServer` enthält die Stelle, an der Cookies gespeichert werden. Siehe [trackingServer](../../vars/config-vars/trackingserver.md).
1. **Hosten Sie die `s_code.js`-Datei auf Ihrer Website**: Diese Datei befindet sich normalerweise zusammen mit anderen Skripten auf Ihrem Webserver.
1. **`s_code.js` auf allen Seiten referenzieren**: Stellen Sie sicher, dass alle einzelnen Seiten die JavaScript-Hauptdatei aufrufen, und zwar im HTML-`<body>`-Tag (nicht im `<head>`-Tag).

   >[!TIP]
   >
   >H-Code erfordert, dass das `s_code.js`-Skript innerhalb des `<body>`-Tags aufgerufen wird. Dies unterscheidet sich von anderen Implementierungsmethoden, bei denen die meisten Skriptverweise im `<head>`-Tag enthalten sein müssen.
1. **Seitenspezifische Variablen auf jeder Seite definieren**: Für jede Seite sollten einzelne Variablen definiert sein, z. B. Seitenname oder eVars. Einzelne Variablen werden normalerweise auf jeder Seite mit einem Inline-`<script>`-Tag definiert.
1. **Verwenden Sie den Debugger, um die Datenerfassung zu überprüfen**: Laden Sie den [CX Enterprise-Debugger herunter und installieren Sie &#x200B;](../../validate/debugger.md), um sicherzustellen, dass Daten an Adobe gesendet und Seitenvariablen korrekt definiert werden.

## Caching

Die JavaScript-Datei wird nach dem ersten Laden im Browser des Besuchers zwischengespeichert und normalerweise nicht mehr als einmal pro Sitzung heruntergeladen. Die Datei wird nicht auf jeder Seite heruntergeladen, auch wenn sie von jeder Seite der Website verwendet wird. Auf den meisten Websites haben Benutzer im Durchschnitt mehr als nur wenige Seitenansichten pro Sitzung. Daher kann die Übertragung von JavaScript, das mehrmals in dieser Datei verwendet wird, insgesamt zu weniger heruntergeladenen Daten führen.

## H-Code-Komprimierung

Wenn Sie sich wegen der Download-Größe der `s_code.js`-Datei Sorgen machen, empfiehlt Adobe, die `s_code.js`-Datei mit GZIP zu komprimieren. GZIP wird von allen gängigen Browsern unterstützt und bietet eine bessere Leistung als die JavaScript-Komprimierung. Siehe [Apache Module mod_deflate](https://httpd.apache.org/docs/current/mod/mod_deflate.html) in der Apache-Dokumentation.
