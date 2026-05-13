---
description: Überblick über die Funktionen von Adobe Analytics zur Nutzung von Server-Aufrufen.
title: Übersicht zur Nutzung von Server-Aufrufen
feature: Server Call Usage
exl-id: d3d64f1e-f01b-4b9e-9aee-c14e574fc40b
role: Admin
TQID: https://experienceleague.adobe.com/-IIz9r-K-flZq85Dz3lhYuo9-Ko0zt0KoJJ7DtI5Mz4
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: e93b8c4c-c5f7-45f8-9abe-9b710f53f502id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 1015
ht-degree: 43%

---

# Nutzung von Server-Aufrufen

Die Nutzung von Adobe Analytics-Server-Aufrufen adressiert Ihre Anfragen zur Transparenz der Nutzungsdaten von Browser- und Mobile-Server-Aufrufen. Damit können Sie auf Folgendes zugreifen:

* Ein Dashboard zur Nutzung von Server-Aufrufen, das Ihre Daten zur Nutzung von Server-Aufrufen verfolgt und mit Ihren vertraglichen Beschränkungen vergleicht. (Wählen Sie in Adobe Analytics > [!UICONTROL **Admin**] > [!UICONTROL **Nutzung der Server-Aufrufe**])
* Ein Warnhinweistyp zur Nutzung von Server-Aufrufen in der Warnhinweiserstellung, mit dem Sie Warnhinweise einrichten können, um Überlastungen zu verhindern (wählen Sie in Adobe Analytics [!UICONTROL **Komponenten**] > [!UICONTROL **Warnhinweise**])

Zu den wichtigsten Vorteilen der Nutzung von Server-Aufrufen gehören:

* **Einblick** in Ihre Daten zur Nutzung und Zusage von Server-Aufrufen, einschließlich des Mobilfunkverbrauchs über Ihre vertragliche Nutzungsbeschränkung für Server-Aufrufe.
* **Warnhinweise** um Sie über das Risiko oder das Auftreten eines Überschusses zu informieren und sich auf die Möglichkeit des Eintretens von Überschüssen vorzubereiten bzw. darauf zu reagieren.

## Voraussetzungen {#section_49AE590FFC7C4E8A83C640C4AAA581AA}

* **Berechtigungen:** Um auf das Dashboard zur Nutzung von Server-Aufrufen und die Warnhinweiserstellung oder den Warnhinweis-Manager zugreifen zu können, müssen Sie ein Adobe Analytics-Administrator sein.
* **Berechtigungen:** Administratoren können Benutzern ohne Administratorrechte Zugriff gewähren: Die Berechtigung lautet **[!UICONTROL Nutzung der Server-Aufrufe]**. Siehe [Berechtigung zur Nutzung von Server-Aufrufen](#server-call-usage-permission).

## Wichtige Terminologie {#terminology}

Die folgenden Begriffe sind für das Verständnis der Nutzung von Server-Aufrufen wichtig:

<table id="table_4E97F85F13344A2C962FA4FA5A51642E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Begriff </th> 
   <th colname="col2" class="entry"> Definition </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Server-Aufruf </p> </td> 
   <td colname="col2"> <p>Ein Server-Aufruf, auch als „Treffer“ oder „Bildanforderung“ bezeichnet, ist eine Instanz, in der Daten zur Verarbeitung an Adobe-Server gesendet werden. Der häufigste Server-Aufruf ist eine Seitenansicht. Bei einem Seitenaufruf betrachtet der Besucher eine Seite Ihrer Website. Es wird dann ein Server-Aufruf an Adobe generiert, wobei Informationen erfasst, verarbeitet und in Ihre Berichtsmetriken aufgenommen werden. </p> <p>Weitere Typen von Server-Aufrufen sind Exitlinks und Dateidownloads, bei denen Daten für eine Verarbeitung an Adobe gesendet werden. Diese Daten werden aber nicht als neuer Seitenaufruf aufgezeichnet. Selbst „ausgeschlossene“ Seitenansichten (die beispielsweise aufgrund eines von Ihnen konfigurierten IP-Adressbereichs aus Ihren Berichten ausgeschlossen sind) sind Server-Aufrufe, da sie von Adobe empfangen und verarbeitet, aber nie in Ihren Berichten angezeigt werden. </p> <p><b>Primärer Server-Aufruf</b>: Anforderungen, die direkt von den Browsern der Website-Besucher oder von der Dateneinfüge-API empfangen werden. Umfasst Primäre Treffer (Seitenansichten), Primäre benutzerspezifische Ereignisse, Primäre Download-Ereignisse und Primäre Exit-Ereignisse. </p> <p><b>Sekundärer Server-Aufruf</b>: Kopien von Primärserver-Aufrufen, die von Multi-Suite-Tags erstellt oder von einer VISTA-Regel kopiert/verschoben wurden. Wenn ein sekundärer Server-Aufruf durch eine VISTA-Regel in eine andere Report Suite verschoben (nicht kopiert) wurde, werden die kumulierten sekundären Aufrufe von den primären Server-Aufrufen abgezogen. </p> <p><b>Mobile Primäre Server-</b> </p> <p>Anforderungen, die direkt von einem der Mobile-SDKs empfangen wurden. Beinhaltet trackAction, trackState, trackApp Crashes, trackActionFromBackground, trackLocation, trackBeacon, trackPushMessageClickThrough, trackTimedActionBacklog, trackLifetimeValueIncrease.</p> <p><b>Sekundärer mobiler Server-Aufruf</b> </p> <p>Kopien der primären Server-Aufrufe, die von Multi-Suite-Tags erstellt oder von einer VISTA-Regel kopiert/verschoben wurden. Wenn ein sekundärer Server-Aufruf durch eine VISTA-Regel in eine andere Report Suite verschoben (nicht kopiert) wurde, werden die kumulierten sekundären Aufrufe von den primären Server-Aufrufen abgezogen. </p> <p>Hinweis: Falls Ihr Unternehmen vertraglich nur zu mobilen Server-Aufrufen (primär oder sekundär) berechtigt ist, werden sowohl die Web- als auch die Mobilnutzung gegen Ihre Mobilzusage aufgerechnet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Abrechnungsunternehmen (Abrechnungs-ID) </p> </td> 
   <td colname="col2"> <p>Die rechtliche Organisation, der die Server-Aufrufe in Rechnung gestellt werden. Zum Beispiel adobe.com. Jede Abrechnungsunternehmen hat eine Abrechnungs-ID, die verwendet wird, um den Abrechnungskunden eindeutig zu identifizieren. Eine Abrechnungs-ID kann mit mehreren Experience Cloud-Organisationen verknüpft sein. Es besteht nicht immer eine 1:1-Beziehung zwischen einer Organisation und einer Abrechnungs-ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Anmeldeunternehmen </p> </td> 
   <td colname="col2"> <p>Ein Abrechnungsunternehmen kann über <a href="https://helpx.adobe.com/de/analytics/kb/multiple-login-companies.html">mehrere Anmeldeunternehmen</a> verfügen. Eine Unternehmensanmeldung ist eine Sammlung von Report Suites, die von Ihrer Organisation verwendet werden. Einige Organisationen verfügen über mehrere Unternehmensanmeldungen, die für verschiedene Teile der Organisation gelten. Dies ist besonders für große Organisationen nützlich, die mit verschiedenen Geschäftsbereichen arbeiten, in denen viele Report Suites nicht für andere im Unternehmen gelten. </p> <p>Oft sind das regionale Niederlassungen eines Unternehmens. Dieses Beispiel zeigt Anmeldeunternehmen und die zugehörigen Report Suites: </p> 
    <ul id="ul_8C756C7972D04F5E89D6E32BB06D26C3"> 
     <li id="li_EA6257FED7854B6FAA071926D0F8A07C">adobe.world: RS1, RS2, RS3, RS4 </li> 
     <li id="li_3EAFB556849E4CCC9D96D5A3492EC898">adobe.us: RS1, RS2 </li> 
     <li id="li_572FFB3F4BF545BDB13102D82CE5E50C">adobe.in: RS3 </li> 
     <li id="li_B6ACBA35E18A427AA83F76BD38E502D7">adobe.de: RS4 </li> 
    </ul> <p>Hinweis: Die Nutzungsdaten von Server-Aufrufen für <u>alle</u> Report Suites innerhalb eines Abrechnungsunternehmens sind für alle Benutzer mit der entsprechenden <a href="/help/admin/tools/server-call-usage/overage-overview.md">Berechtigung</a> einsehbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Cloud-Organisation </p> </td> 
   <td colname="col2"> <p>Eine Organisation ist die Einheit, die es einem Administrator ermöglicht, Gruppen und Benutzer zu konfigurieren und das Single-Sign-on in der Experience Cloud zu steuern. Die Organisation agiert als zentrale Anmeldestelle, die sämtliche Experience Cloud-Produkte und -Lösungen umfasst. </p> <p>Normalerweise besitzt eine Organisation den Namen Ihres Unternehmens. Ein Unternehmen kann jedoch über mehrere Organisationen verfügen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verbindlichkeit für Server-Aufrufe </p> </td> 
   <td colname="col2"> <p>Wenn Ihr Unternehmen einen Vertrag mit Adobe abschließt, dann stellt das Sales-Team von Adobe zusammen mit Ihnen, dem Kunden, fest, welche Arten (primär, sekundär, primär mobil, sekundär mobil) und schätzungsweise welche Menge an Server-Aufrufen von Ihnen über die Dauer des Vertrags zu erwarten sind. Dies ist die Gesamtverpflichtung für Server-Aufrufe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nutzungsdauer </p> </td> 
   <td colname="col2"> <p>Für die Überwachung der Nutzung der Server-Aufrufe wird diese Gesamtverpflichtung für Server-Aufrufe in kleinere Nutzungszeiträume (z. B. 3 Monate) unterteilt, um Vergleiche von einem Jahr zum anderen zu ermöglichen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vertragslaufzeit </p> </td> 
   <td colname="col2"> <p>Die Vertragsdauer kann mehrere Jahre betragen. Nehmen wir an, dass Ihr Unternehmen eine Zusage für Server-Aufrufe von 6 Millionen Aufrufen während einer Vertragsdauer von 3 Jahren erhalten hat. Um die Nutzung der Server-Aufrufe besser überwachen zu können, wird dieser Zeitraum von 3 Jahren in kleinere Nutzungsperioden aufgeteilt, um so einfacher Jahresvergleiche durchzuführen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Berechtigung zur Nutzung von Server-Aufrufen {#permission}

Die Berechtigung zur Nutzung von Server-Aufrufen wird automatisch Analytics-Administrierenden erteilt. Damit können Nutzer das Dashboard einsehen und Warnhinweise zu Server-Aufrufen erstellen. Administratoren können Benutzern ohne Administratorrechte diese Berechtigung erteilen.

>[!NOTE]
>
>Ihr Unternehmen kann auswählen, welche Anmeldeunternehmen Zugriff auf die Nutzung von Server-Aufrufen haben.

<table id="table_86256AD8B4554F369439A8FDF2F545E1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Berechtigungsname </th> 
   <th colname="col3" class="entry"> Berechtigung erteilen, wenn Sie bei Adobe Analytics angemeldet sind (veraltete Anmeldung) </th> 
   <th colname="col4" class="entry"> Berechtigung erteilen, wenn Sie bei Adobe Experience Cloud angemeldet sind </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Nutzung von Server-Aufrufen </p> </td> 
   <td colname="col3"> 
    <ol id="ol_13A984328D264488B7045DC7521A5F55"> 
     <li id="li_ACDA518C7D184084AC1DFA7B38C67314">Melden Sie sich über sc.omniture.com bei Analytics an. </li> 
     <li id="li_066D90AB071941C3869EDAFCE981707A">Navigieren Sie zu <span class="ignoretag"> <span class="uicontrol"> Admin </span> &gt; <span class="uicontrol"> Alle </span> &gt; <span class="uicontrol"> User Management </span> &gt; <span class="uicontrol"> Gruppen </span> &gt; <span class="uicontrol"> Alle Berichtzugriffe bearbeiten </span> &gt; <span class="uicontrol"> Analytics-Tools </span> &gt; <span class="uicontrol"> </span> anpassen &gt; <span class="uicontrol"> Server-Aufruf </span> </span> </li> 
    </ol> </td> 
   <td colname="col4"> 
    <ol id="ol_518673ED323A4C5993A3B9F4BA09E405"> 
     <li id="li_56FF685A3B454ECEA5F16BB591A60034">Melden Sie sich bei login.experiencecloud.adobe.com an.</li> 
     <li id="li_FA1AE0F19DEF4AB2AA77B22CCA2995F9">Klicken Sie auf <span class="uicontrol">Analytics</span>. </li> 
     <li id="li_22A4CBB84B5A451780873BBE67E6E6EF">Navigieren Sie zu <span class="ignoretag"> <span class="uicontrol"> Produkte </span> &gt; <span class="uicontrol"> Produktprofil </span> &gt; <span class="uicontrol"> Berechtigungen </span> &gt; <span class="uicontrol"> Analytics-Tools </span> &gt; <span class="uicontrol"> Server-Aufruf-Nutzung </span> </span> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>
