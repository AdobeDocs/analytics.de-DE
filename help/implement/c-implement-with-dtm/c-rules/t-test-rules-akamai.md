---
description: Wenn Sie Akamai-Hosting verwenden, testen Sie nicht veröffentlichte Regeln über Ihre Konsole.
keywords: Dynamic Tag Management;Regel;Switch-Plug-in;Akamai;Akamai testen;Nicht veröffentlichte Regeln;Nicht veröffentlichte Regeln testen;Regel debuggen
seo-description: Wenn Sie Akamai-Hosting verwenden, testen Sie nicht veröffentlichte Regeln über Ihre Konsole.
seo-title: Testen unveröffentlichter Regeln für Akamai-Hosting
solution: Experience Cloud, Analytics, Target, Dynamic Tag Management
title: Testen unveröffentlichter Regeln für Akamai-Hosting
uuid: 979e3d74-8d96-47d0-b581-cf5371248434
translation-type: tm+mt
source-git-commit: 8c4c368a84ba5499d85f0b7512c99de47ddb14c2

---


# Testen unveröffentlichter Regeln für Akamai-Hosting

Wenn Sie Akamai-Hosting verwenden, testen Sie nicht veröffentlichte Regeln über Ihre Konsole.

Mit dem Switch-Plugin sind die Tests meist am einfachsten durchzuführen. Weitere Informationen finden Sie unter [Search Discovery-Plugins](https://marketing.adobe.com/resources/help/en_US/dtm/search_discovery_plugins.html) in der Produktdokumentation für das Dynamic Tag Management.

Führen Sie die folgenden Schritte zum Testen ohne Switch-Plug-in aus:

1. Greifen Sie auf die Webkonsole auf Ihrer Website zu und geben Sie `localStorage.setItem('sdsat_stagingLibrary', true)`.
1. Drücken Sie die **[!UICONTROL Eingabetaste]**.
1. Geben Sie `_satellite.setDebug(true)` ein und drücken Sie dann die **[!UICONTROL Eingabetaste]**.
1. Aktualisieren Sie die Seite.

   Mit dieser Aktion wird Ihre Staging-Bibliothek geladen und der Debugger festgelegt, sodass Sie Details aller verfügbaren (veröffentlichten/nicht veröffentlichten) Regeln sehen können, die auf der Seite ausgelöst werden.
1. Führen Sie abschließend `localStorage.setItem('sdsat_stagingLibrary', false)` aus und drücken Sie die **[!UICONTROL Eingabetaste]**.

   Schritt Ergebnis
