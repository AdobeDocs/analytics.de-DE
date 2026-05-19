---
description: Informieren Sie sich über die IDs, die in Ihren Analytics-Daten erfasst werden, und entscheiden Sie, welche Sie für Datenschutzanfragen verwenden werden.
title: Best Practices für Beschriftungen
feature: Data Governance
role: Admin
exl-id: 00da58b0-d613-4caa-b9c1-421b1b541f47
TQID: https://experienceleague.adobe.com/btvouuszSZn1h7xDCInebbqYE9vb1bwcU4-DMW3l3oM
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
  - id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2:
  - id: c77ba355-6681-41fe-b719-563d3f507fdb
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 2340
ht-degree: 65%

---

# Best Practices für Beschriftungen

Die Beschriftung muss jedes Mal überprüft werden, wenn eine neue Report Suite erstellt oder in einer vorhandenen Report Suite eine neue Variable aktiviert wird. Sie müssen die Beschriftung möglicherweise auch dann überprüfen, wenn neue Lösungsintegrationen aktiviert werden, da sie neue Variablen zur Verfügung stellen können, für die eine Beschriftung erforderlich ist. Eine erneute Implementierung Ihrer Mobile Apps oder Websites kann die Art und Weise der Verwendung vorhandener Variablen ändern, was möglicherweise auch Aktualisierungen der Kennzeichnungen erforderlich macht.

Die Beschriftungen I1, I2, S1 und S2 haben die gleiche Bedeutung wie die entsprechend benannten DULE-Beschriftungen in Adobe Experience Platform. Sie werden jedoch für sehr unterschiedliche Zwecke verwendet. Innerhalb von Adobe Analytics werden mithilfe dieser Beschriftungen Felder identifiziert, die als Ergebnis einer Privacy Service-Anfrage anonymisiert werden sollten. In Adobe Experience Platform werden sie zur Zugriffssteuerung, Einverständnisverwaltung und Durchsetzung von Marketing-Einschränkungen für die gekennzeichneten Felder genutzt. Adobe Experience Platform unterstützt viele zusätzliche Beschriftungen, die nicht von Adobe Analytics verwendet werden. Wenn Sie Ihre Adobe Analytics-Daten über den Analytics Data Connector in Adobe Experience Platform importieren, sollten Sie sicherstellen, dass alle in Adobe Analytics angewendeten Beschriftungen vom Typ I1, I2, S1 und S2 auch auf die Schemata in Adobe Experience Platform angewendet werden, die von den importierten Report Suites verwendet werden.

## Direkt vs. indirekt identifizierbare IDs {#direct-vs-indirect}

Bevor Sie ermitteln, welche Beschriftungen den einzelnen Variablen und Feldern hinzugefügt werden müssen, sollten Sie zunächst die Grundlagen zu den IDs kennen, die Sie in Ihren Analytics-Daten erfassen, und entscheiden, welche hiervon Sie für Datenschutzanfragen verwenden wollen. Datenschutz erweitert den Umfang dessen, was als ID gilt. IDs lassen sich in zwei allgemeine Klassen einteilen: direkt identifizierbar (Identitätsbezeichnung: I1) und indirekt identifizierbar (Identitätsbezeichnung: I2).

* **Direkt identifizierbare Kennung (I1)**: Benennt die Person oder bietet eine direkte Möglichkeit, sie zu kontaktieren. Beispiele wären der Name einer Person (selbst ein gebräuchlicher Name wie John Smith, der von Hunderten von Personen geteilt werden kann), eine beliebige E-Mail-Adresse oder Telefonnummer usw. Eine Postanschrift ohne Namen kann als direkt identifizierbar angesehen werden, auch wenn sie nur einen Haushalt oder ein Unternehmen und nicht eine bestimmte Person innerhalb dieses Haushalts oder Unternehmens identifiziert.
* **Eine indirekt identifizierbare ID (I2)**: Ermöglicht nicht die Identifizierung einer Person selbst, kann aber mit anderen Informationen (die sich in Ihrem Besitz befinden können oder nicht) kombiniert werden, um eine Person zu identifizieren. Beispiele für indirekt identifizierbare IDs sind beispielsweise Kundentreuenummern oder im Unternehmens-CRM-System verwendete IDs, die für jeden Kunden oder jede Kundin eindeutig sind. Unter Datenschutz können die anonymen IDs, die in von Analytics verwendeten Tracking-Cookies gespeichert werden, als indirekt identifizierbar gelten, obwohl sie nur ein Gerät und keine Person identifizieren können. Auf einem gemeinsam genutzten Gerät können diese Cookies nicht zwischen den verschiedenen Nutzern des Systems unterscheiden. Das Cookie kann beispielsweise nicht dazu verwendet werden, einen Computer zu finden, der das Cookie enthält, jedoch kann eine Person, die auf den Computer zugreifen kann und das Cookie dort findet, das Analytics-Cookie auf den Computer zurückführen.

Auch eine IP-Adresse gilt als indirekt identifizierbar, da sie immer nur einem einzigen Gerät zugeordnet sein kann. ISPs können jedoch die IP-Adressen für die meisten Benutzer regelmäßig ändern, sodass im Laufe der Zeit eine IP-Adresse von einem ihrer Benutzer verwendet worden sein kann. Es ist auch nicht ungewöhnlich, dass viele Kunden eines ISP oder mehrere Mitarbeiter innerhalb eines Unternehmens im selben Intranet dieselbe externe IP-Adresse gemeinsam nutzen. Deswegen unterstützt Adobe die Verwendung von IP-Adressen nicht als IDs für Datenschutzanfragen. Wenn für eine Löschanfrage eine von uns unterstützte ID verwendet wird, löschen wir auch die IP-Adressen, die mit dieser ID erfasst wurden. Sie müssen ermitteln, ob andere IDs in dieser Kategorie (I1 oder I2) existieren, die sich aber nicht für die Verwendung als eindeutige IDs für Datenschutzanfragen eignen.

Selbst wenn Ihr Unternehmen innerhalb Ihrer Analytics-Daten viele verschiedene IDs erfasst, können Sie nur eine Teilmenge dieser IDs für Datenschutzanfragen verwenden. Gründe hierfür können sein:

* Innerhalb Ihrer eigenen Systeme können Sie eine der IDs (z. B. die E-Mail-Adresse) einer anderen ID (z. B. CRM-ID) zuordnen. Daraufhin verwenden Sie zur Einheitlichkeit nur die CRM-ID für Datenschutzanfragen in Ihrer Datenschutzverarbeitung.
* Es gibt keine Methode, um zu überprüfen, ob jemand tatsächlich die mit der ID verknüpfte Person ist. So kann es beispielsweise sehr schwierig sein zu überprüfen, ob eine IP-Adresse jemals nur von einer einzigen Person verwendet wurde und ob die Person, die die Anfrage sendet, tatsächlich diese Person ist.
* Manche IDs gelten möglicherweise für mehrere Personen, weshalb Sie vermeiden sollten, Informationen zu einer Person an eine andere Person mit derselben ID weiterzugeben. Selbst wenn Sie beispielsweise überprüfen können, ob der Name einer Person John Smith lautet, möchten Sie möglicherweise nicht alle Daten zu allen John Smiths in Ihrem System zurückgeben.
* Ein weiteres Beispiel ist eine Geräte-ID, z. B. die Analytics-Cookie-ID. Wenn die ID in einer Handy-App auftritt, können Sie festlegen, dass alle Interaktionen, die diese ID verwenden, für den Inhaber des Handys verfügbar sein sollten. Wenn es jedoch auf einem gemeinsam genutzten Gerät auftritt, z. B. auf einem Heimcomputer oder einem Computer in einer Bibliothek oder einem Internetcafé, können Sie möglicherweise entscheiden, dass Sie nicht zwischen den Benutzern dieses Geräts unterscheiden können. Das Risiko, Daten für einen anderen Benutzer zurückzugeben, ist zu groß, um die Verwendung dieses ID-Typs zu ermöglichen.

## Best Practices für Analytics-unterstützte IDs {#best-practices-an}

Anhand dieser Tabelle können Sie die ID-Typen bestimmen, mit deren Hilfe Sie Datenschutzanfragen an Analytics senden. Sobald Sie diese Informationen kennen, können Sie leichter die anderen Kennzeichnungen ermitteln, die Sie für Ihre Variablen verwenden sollten.

<table id="table_E25612E32A03449A8E5DA00B88FCEB9E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> ID-Typ </th> 
   <th colname="col2" class="entry"> Empfehlungen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Cookie-IDs </p> 
    <ul id="ul_CB43CEA3054E490585CBF3AB46F95B5B"> 
     <li id="li_9174CB3910AF4EF8BA7165DB537765A5"> <a href="https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-privacy.html?lang=de">Analytics-Cookie (Legacy)</a> </li> 
     <li id="li_7B6A9A788BBD47428315B3893FC07BC3"> <a href="https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de">Identity Service-Cookie</a> (ECID), zuvor als Marketing Cloud ID (MCID) bezeichnet </li> 
    </ul> </td> 
   <td colname="col2"> <p>Diese Cookies identifizieren ein Gerät oder genauer gesagt einen Browser für einen Benutzer eines Geräts. Bei einem gemeinsam genutzten Gerät, auf dem eine gemeinsame Anmeldung verwendet wird, kann diese ID für alle/jeden Benutzer des Geräts gelten. Adobe hat <a href="https://developer.adobe.com/experience-platform-apis/references/privacy-service/"> einheitlichen JavaScript-Code</a> entwickelt, den Sie in Ihre Website einfügen können, um diese Cookies zu erfassen, sofern Sie sie für Datenschutzanfragen zulassen möchten. </p> <p>Benutzer des mobilen Adobe Analytics-SDK verfügen auch über eine Experience Cloud ID (ECID). Im SDK sind API-Aufrufe enthalten, die diese ID auslesen. So können Sie Ihre App so erweitern, dass sie die ID für Datenschutzanfragen erfasst. </p> <p>Viele Unternehmen behandeln Browsercookie-IDs wie IDs gemeinsam genutzter Geräte. Daher könnten sie nach Rücksprache mit ihrer Rechtsabteilung beschließen, diese IDs nicht als zulässige IDs für Datenschutzanfragen zu verwenden. Alternativ könnten sie sich dafür entscheiden, bei Verwendung dieser IDs nur eine sehr begrenzte Menge an Daten zurückzugeben oder sie nur für Löschanfragen zu akzeptieren. </p> <p>Diese Cookies haben eine ID-DEVICE-Kennzeichnung, die nicht geändert werden kann (sowie I2- und DEL-DEVICE-Kennzeichnungen). Die standardmäßige Adobe Analytics-Konfiguration gibt nur allgemeine Informationen über das Gerät zurück, z. B. Gerätetyp, Betriebssystem, Browser usw. sowie die Zeit/das Datum, zu der/dem Ihre Website bei der Verwendung dieser IDs besucht wurde. Wenn Sie diese IDs jedoch wie unten erläutert für Datenschutzanfragen unterstützen möchten, können Sie ACC-ALL-Beschriftungen hinzufügen oder entfernen, um genau die Felder zu konfigurieren, die bei einer Datenschutz-Zugriffsanfrage zurückgegeben werden sollen. </p> <p>Wenn die Report Suite mit einer mobilen App verknüpft ist, die eine Anmeldung erfordert, könnten Sie die Experience Cloud-ID für das Gerät einem bestimmten Benutzenden zuweisen. In diesem Fall ist es empfehlenswert, zusätzliche Felder mit der Kennzeichnung ACC-ALL zu versehen, einschließlich der Namen der besuchten Seiten, der angezeigten Produkte usw. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>IDs in benutzerdefinierten Variablen </p> </td> 
   <td colname="col2"> <p>Manche Kunden speichern IDs in <a href="/help/implement/vars/page-vars/evar.md">benutzerspezifischen Traffic-Variablen (Props) oder benutzerspezifischen Konversionsvariablen (eVars)</a>. Zwar wird am häufigsten die CRM-ID verwendet, jedoch sind auch andere IDs möglich, darunter E-Mail-Adressen, Anmeldenamen, Treuenummern oder Hashes dieser Werte. </p> 
    <ul id="ul_0B9492CF786046BB97E31CCF83A85FEA"> 
     <li id="li_D35B61CC6A8B485A8E09358A46D3F598">Wenn Sie eine dieser IDs für Datenschutzanfragen verwenden wollen, müssen Sie das Feld, das sie enthält, mit einer ID-PERSON-Beschriftung versehen. </li> 
     <li id="li_94541340B054436297C5565F074413DC">(Deutlich seltener) Wenn eine ID in diesen benutzerspezifischen Variablen nur ein Gerät identifiziert, das möglicherweise von mehreren Benutzern gemeinsam genutzt wird, können Sie stattdessen die ID-DEVICE-Beschriftung verwenden. </li> 
     <li id="li_8115B999E8DA46CAB359BCF1F4A4DCAE">Diese Felder erfordern auch I1- oder I2-Kennzeichnungen und sollten eine DEL-PERSON- oder DEL-DEVICE-Kennzeichnung enthalten. In der Regel entspricht die Option PERSON/DEVICE der DEL-Kennzeichnung der Option PERSON/DEVICE der ID-Kennzeichnung. </li> 
    </ul> <p> Es kommt nur selten vor, dass eine Report Suite mehr als eine oder zwei benutzerdefinierte Variablen enthält, die IDs beinhalten, die Sie bei Datenschutzanfragen zur Identifikation von betroffenen Personen verwenden können. Sie können mehrere Variablen haben, denen I1- oder I2-Kennzeichnungen zugewiesen sind, aber normalerweise hätten nur eine oder zwei dieser Variablen auch ID-PERSON- oder ID-DEVICE-Kennzeichnungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Benutzerspezifische Besucher-ID </p> </td> 
   <td colname="col2"> <p>Obwohl dies nicht häufig verwendet wird, unterstützt Analytics auch eine Implementierung, bei der eine benutzerdefinierte Besucher-ID bereitgestellt werden kann, die, falls vorhanden, anstelle des Legacy-Tracking-Cookies von Analytics verwendet wird. Dieses Feld hat die Kennzeichnungen I2, ID-PERSON und DEL-PERSON. </p> <p>Viele Implementierungen leiten diese ID von einer CRM-ID ab, sodass sie nur dann vorhanden ist, wenn jemand auf ihrer Website angemeldet ist. Dadurch kann dieselbe benutzerdefinierte Besucher-ID geräteübergreifend verwendet werden. Ein technischer Nachteil ist, dass das Tracking, das vor der Anmeldung des Benutzers erfolgt, nicht mit dem Tracking verknüpft werden kann, das nach der Anmeldung erfasst wurde. Wenn Sie stattdessen die benutzerdefinierte Besucher-ID verwenden, um ein Gerät einfach zu identifizieren, sollten Sie die Kennzeichnungen „ID-PERSON“ und „DEL-PERSON“ in „ID-DEVICE“ bzw. „DEL-DEVICE“ ändern. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Best Practices für die Einrichtung von Löschkennzeichnungen {#best-practices-delete}

>[!NOTE]
>
>Bei Props spielt die Groß-/Kleinschreibung keine Rolle. eVars sind standardmäßig nicht von der Schreibweise abhängig, können jedoch über die Adobe-Kundenunterstützung entsprechend konfiguriert werden. Wenn Sie eVars verwenden, die von der Groß-/Kleinschreibung abhängig sind und eine ID enthalten, müssen Sie beim Einreichen von Datenschutzanfragen auf die richtige Schreibweise achten, damit sie mit der Schreibweise in den Hits übereinstimmt, die die entsprechenden IDs enthalten.

Die Löschbeschriftungen DEL-DEVICE und DEL-PERSON sollten sparsam eingesetzt werden. Wenn sie auf eine Variable angewendet werden, die keine ID enthält, die im Rahmen der Datenschutzanfrage verwendet wurde, ändern sich fast in allen Fällen die Werte (Metriken) in älteren Analytics-Berichten.

* Wir empfehlen, dass Sie eine dieser Beschriftungen auf jede Variable mit der Beschriftung „I1“, „I2“ oder „S1“ anwenden. Sie können nicht auf Variablen ohne die I1-, I2- oder S1-Beschriftung angewendet werden.
* Durch die DEL-Beschriftungen werden diese Variablen [anonymisiert](/help/admin/tools/privacy-labeling/labels.md#data-governance-labels) (die ID wird durch eine zufällige Zeichenfolge ersetzt, der „Datenschutz-“ vorangestellt wird). Derselbe anonymisierte Wert ersetzt alle Instanzen des ursprünglichen Werts in allen Treffern, die durch eine in der Anfrage verwendete ID identifiziert wurden. Wenn der ursprüngliche Wert in diesem Feld eine dieser IDs war, ändern sich die Berichtsmetriken nicht.
* Wenn ein Feld den Titel ID-DEVICE hat, sollten Sie im Allgemeinen auch den Titel DEL-DEVICE zuweisen.
* Wenn ein Feld den Titel ID-PERSON hat, sollten Sie auch den Titel DEL-PERSON zuweisen.
* Wenn für ein Feld keine ID-Beschriftung vorhanden ist, es jedoch identifizierbare Informationen enthält, die Sie anonymisieren wollen, ist die passende Beschriftung (DEVICE oder PERSON) von Ihrer Implementierung abhängig. Wenn Sie nur Cookie-IDs für Datenschutzanfragen verwenden, sollten Sie DEL-DEVICE verwenden.
* Wenn Sie benutzerdefinierte IDs in einem anderen Feld mit ID-PERSON-Beschriftung verwenden und Werte nur in Zeilen löschen wollen, in denen die ID auftritt, verwenden Sie DEL-PERSON.
* Beachten Sie, dass bei der Angabe einer DEL-DEVICE- oder DEL-PERSON-Beschriftung für eine beliebige Variable, die nicht zusätzlich als ID für die jeweilige Anfrage verwendet wird (einschließlich einer erweiterten ID), eindeutige Werte in der betreffenden Variable nur für Treffer anonymisiert werden, in denen eine bestimmte (oder erweiterte) ID vorkommt. Wenn andere Treffer denselben Wert enthalten, erfolgt unter den anderen Speicherorten keine Aktualisierung. Dies kann dazu führen, dass sich die Anzahl (Metriken) ändert.

  Wenn beispielsweise drei Treffer den Wert „foo“ in eVar7 enthalten, jedoch nur einer davon auch eine ID in einer anderen Variable beinhaltet, die einem Löschvorgang zugeordnet ist, wird der Wert „foo“ für diesen Treffer zu einem Wert wie „Datenschutz-123456789“ geändert, während er für die anderen beiden Treffer unverändert bleibt. In einem Bericht, der Aufschluss über die Anzahl eindeutiger Werte für eVar7 gibt, werden nun mehr eindeutige Werte angezeigt als zuvor. In einem Bericht mit den Höchstwerten für eVars ist „foo“ möglicherweise nur mit zwei Instanzen enthalten (anstatt zuvor mit 3), und der neue Wert wird ebenfalls mit einer einzelnen Instanz angezeigt.

## Best Practices für die Einrichtung von Zugriffskennzeichnungen {#best-practices-access}

Zwar verfügen nur wenige Felder über einige der anderen Beschriftungen, jedoch wird es häufig vorkommen, dass viele Felder ACC-Beschriftungen aufweisen. Die passenden Zugriffsbeschriftungen hängen von den IDs ab, die Sie für Datenschutzanfragen verwenden.

<table id="table_A5B834CC08C641D99E2691A2361997E4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Bei Verwendung von... </th> 
   <th colname="col2" class="entry"> …diese Recommendations verwenden </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Nur Geräte-IDs </p> </td> 
   <td colname="col2"> <p>Wenn Sie nur Cookie-IDs oder ID-DEVICE-Kennungen verwenden, sollten Sie nur die ACC-ALL-Kennzeichnung verwenden. </p> <p>Sie erhalten ein Dateienpaar pro Zugriffsanfrage: eine Datei mit einer Zeile für jeden passenden Treffer, die alle angegebenen ACC-ALL-Felder enthält, und eine Zusammenfassungsdatei mit einer Übersicht über diese Daten. </p> </td> 
  </tr> 
 </tbody> 
</table>
