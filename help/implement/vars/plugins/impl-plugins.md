---
title: Übersicht über Plug-ins
description: Fügen Sie Code auf Ihrer Website ein, um neue Funktionen einzuführen.
feature: Appmeasurement Implementation
exl-id: faae7963-078d-40ad-ba09-71efa0b90df1
role: Admin, Developer
TQID: https://experienceleague.adobe.com/ImzoBRU0DajPc99vRlu1698CteFNk9dOS2OZrN9DBZs
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: c069c44e-5426-4c1a-accc-8028662f2fdeid: df312454-73c4-43f6-a90e-18f5043f074cid: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 328
ht-degree: 96%

---

# Übersicht über Plug-ins

Plug-ins sind Codefragmente, die mehrere erweiterte Funktionen ausführen, um Ihre Analytics-Implementierung zu unterstützen. Diese Plug-ins erweitern den Funktionsumfang Ihrer JavaScript-Datei um Funktionen, die bei einer Basisimplementierung nicht vorhanden sind. Im Rahmen erweiterter Lösungen bietet Adobe noch andere Plug-ins an.

{{plug-in}}

Adobe bietet mehrere Möglichkeiten, ein bestimmtes Plug-in zu installieren:

* Verwenden der Erweiterung „Common Analytics Plugins“ mit der Adobe Analytics-Erweiterung
* Einfügen des Plug-in-Codes mit dem benutzerdefinierten Code-Editor
* Einfügen des Plug-in-Codes in Ihre `AppMeasurement.js`-Datei.

Jedes Unternehmen hat unterschiedliche Implementierungsanforderungen, sodass Sie entscheiden können, wie Sie sie in Ihre Implementierung einbeziehen möchten. Stellen Sie sicher, dass Sie die folgenden Kriterien erfüllen, wenn Sie den Code auf Ihrer Website einbeziehen:

1. Instanziieren Sie zuerst das Analytics-Tracking-Objekt (unter Verwendung von [`s_gi`](../functions/s-gi.md)).
   * Ihre für Tags aktivierte Site instanziiert das Tracking-Objekt automatisch, wenn Adobe Analytics geladen wird.
   * Implementierungen mit `AppMeasurement.js` initialisieren normalerweise das Tracking-Objekt am Anfang der JavaScript-Datei.
2. Fügen Sie als Zweites den Plug-in-Code ein.
   * Die Erweiterung „Common Analytics Plugins“ verfügt über eine Aktionskonfiguration, in der Sie Plug-ins initialisieren können.
   * Wenn Sie die Erweiterung nicht verwenden möchten, können Sie beim Konfigurieren der Analytics-Erweiterung den Plug-in-Code im Editor für benutzerdefinierten Code einfügen.
   * Wenn Ihre Implementierung keine Tags in Adobe Experience Platform verwendet, können Sie Plug-in-Code an einer beliebigen Stelle in `AppMeasurement.js` einfügen, nachdem Sie das Tracking-Objekt instanziiert haben.
3. Rufen Sie das Plug-in als Drittes auf.
   * Alle Implementierungen, sowohl innerhalb als auch außerhalb einer für Tags aktivierten Site, verwenden JavaScript, um Plug-ins aufzurufen. Rufen Sie das Plug-in in dem Format auf, das auf der Seite des Plug-ins beschrieben ist.
4. Validieren Sie Ihre Implementierung und veröffentlichen Sie sie.

Viele Unternehmen rufen Plug-ins über die [`doPlugins`](../functions/doplugins.md)-Funktion auf. Diese Funktion ist zwar nicht erforderlich, Adobe hält sie jedoch für eine Best Practice. AppMeasurement ruft diese Funktion kurz vor dem Kompilieren und Senden einer Bildanforderung auf. Dies ist ideal, da mehrere Plug-ins von anderen Analytics-Variablen abhängen.
