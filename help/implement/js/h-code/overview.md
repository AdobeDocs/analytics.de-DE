---
title: Übersicht über die JavaScript-Implementierung mit H-Code
description: Erfahren Sie mehr über den Workflow zur Implementierung von H-Code auf Ihrer Website.
feature: Implementation Basics
exl-id: cf83d8fe-a3b1-4e65-a86a-7eeaf555651b
role: Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 100%

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
1. **Debugger verwenden, um die Datenerfassung zu überprüfen**: Laden Sie den [Experience Cloud-Debugger](../../validate/debugger.md) herunter und installieren Sie ihn, um sicherzustellen, dass Daten an Adobe gesendet werden und dass die Seitenvariablen korrekt definiert sind.

## Caching

Die JavaScript-Datei wird nach dem ersten Laden im Browser des Besuchers zwischengespeichert und in der Regel nur ein Mal pro Sitzung heruntergeladen. Die Datei wird nicht für jede Seite erneut heruntergeladen, selbst wenn sie auf jeder Seite der Website verwendet wird. Auf den meisten Websites rufen Benutzer im Durchschnitt mehr als nur ein paar Seitenansichten pro Sitzung auf. Somit kann durch die Übertragung von mehrfach verwendetem JavaScript in diese Datei die insgesamt heruntergeladene Datenmenge reduziert werden.

## H-Code-Komprimierung

Wenn Sie sich wegen der Download-Größe der `s_code.js`-Datei Sorgen machen, empfiehlt Adobe, die `s_code.js`-Datei mit GZIP zu komprimieren. GZIP wird von allen gängigen Browsern unterstützt und bietet eine bessere Leistung als die JavaScript-Komprimierung. Siehe [Apache Module mod_deflate](https://httpd.apache.org/docs/current/mod/mod_deflate.html) in der Apache-Dokumentation.
