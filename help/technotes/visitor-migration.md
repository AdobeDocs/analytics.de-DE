---
description: Beim Migrieren von Besuchern wird das Besucher-ID-Cookie von einer Domäne zu einer anderen migriert.
keywords: Analytics-Implementierung
title: Besuchermigration
topic-fix: Developer and implementation
uuid: af31928c-85d7-407f-a583-0c8f2852ceb3
exl-id: d44628c8-902f-4e60-b819-41d5537407d8
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 78%

---

# Besuchermigration

Beim Migrieren von Besuchern wird das Besucher-ID-Cookie von einer Domäne zu einer anderen migriert.

Besuchermigration lässt Sie die Cookies zur Identifizierung von Besuchern beibehalten, wenn Sie die Datenerfassungsdomänen ändern. Das Ändern von Datenerfassungsdomänen kann die folgenden Gründe haben:

* Wechsel von `2o7.net` zu `adobedc.net`.

* Sie implementieren den [Experience Cloud-Besucher-ID-Dienst](https://docs.adobe.com/content/help/de-DE/id-service/using/home.html) und wechseln von einer CNAME/Erstanbieter-Datenerfassungsdomäne zu `adobedc.net`, `2o7.net` oder `omtrdc.net`

* Wechsel zu einer Datenerfassung mit Namen/Erstanbietern ( [Erstanbieter-Cookies)](https://docs.adobe.com/content/help/de-DE/core-services/interface/ec-cookies/cookies-first-party.html).

* Wechsel von einem CNAME-Eintrag zu einem anderen (Domänenwechsel).

Wenn die Besuchermigration konfiguriert wurde und ein Benutzer die neue Domäne ohne einen Besucher-ID-Cookie besucht, führt der Server eine Umleitung zum vorherigen Datenerfassungs-Hostnamen aus, ruft jegliche verfügbaren Besucher-ID-Cookies ab und wechselt dann zurück zu der neuen Domäne. Wenn eine Besucher-ID unter dem früheren Hostnamen nicht gefunden werden kann, wird eine neue ID generiert. Dies erfolgt einmalig pro Besucher.

## Migrieren von Besuchern {#section_FF0C5C5CAEF343FFA1892B29311F7160}

In der folgenden Tabelle sind die Aufgaben aufgeführt, die für das Migrieren von Besuchern erforderlich sind:

<table id="table_7B2535FC3E264216A299686415C6B21C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Aufgabe </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Zu Beginn:</b> <a href="https://helpx.adobe.com/de/marketing-cloud/contact-support.html"  >Wenden Sie sich an den Kundendienst</a>, und teilen Sie die Domäne(n) mit, die migriert werden sollen, sowie den Migrationszeitraum, der aktiviert werden soll (30, 60 oder 90 Tage). Stellen Sie sicher, dass Sie die sicheren und nicht sicheren Domänen mit einbeziehen. </p> </td> 
   <td colname="col3"> <p>Erstellen Sie eine Liste mit der <i>exakten</i> Syntax für die Domänen, zu denen und von denen migriert werden soll. </p> 
    <ul id="ul_067EC5C7619141A6BDFBC209C9FD47E2"> 
     <li id="li_0723D948465A49C1871B81207AEDC4DC">example.112.2o7.net &gt; metrics.example.com </li> 
     <li id="li_B0CA15A593BD4AB9802E33A3FF037C7A">example.102.112.2o7.net &gt; smetrics.example.com </li> 
    </ul> <p>Die Migrations-Hostnamen werden auf dem Adobe-Datenerfassungsserver konfiguriert. Der Kundendienst teilt Ihnen mit, wann die Änderung erfolgt, sodass Sie für den nächsten Schritt planen können. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>6 und mehr Stunden nach dem Konfigurationswechsel</b>: Aktualisieren Sie die Variablen <code> s.trackingServer</code> und <code> s.trackingServerSecure</code> in Ihrem Analytics JavaScript-Code, um die neuen Datenerfassungsserver zu verwenden. </p> </td> 
   <td colname="col3"> <p>Nachdem Sie diese Änderung vorgenommen haben, überprüfen Sie mit dem <a href="https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=en">-Experience Cloud-Debugger</a>, ob die Analytics-Bildanforderung an den aktualisierten Datenerfassungsserver gesendet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Unmittelbar nach Aktualisierung Ihres Analytics-Code</b>: Testen Sie Ihre Website, um zu verifizieren, dass die Umleitung zur vorherigen Datenerfassungsdomäne erfolgt. </p> </td> 
   <td colname="col3"> <p>Verwenden Sie einen  <a href="../implement/validate/packet-monitor.md"> Paket-</a> Überwachung, um sicherzustellen, dass beim erstmaligen Zugriff auf Ihre Site oder nach dem Löschen von Cookies zwei 302-HTTP-Statuscodes (Umleitung) vor dem 200-HTTP-Statuscode (OK) angezeigt werden. Wenn eine dieser Umleitungen fehlschlägt, wenden Sie sich an den Kundendienst, um sicherzustellen, dass die Migration ordnungsgemäß konfiguriert wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Im gesamten Migrationszeitraum</b>: Belassen Sie den DNS-Eintrag für den vorherigen Hostnamen weiterhin aktiviert. </p> </td> 
   <td colname="col3"> <p>Der vorherige Hostname muss über DNS aufgelöst werden. Andernfalls wird die Cookie-Migration nicht ausgeführt. </p> </td> 
  </tr> 
 </tbody> 
</table>
