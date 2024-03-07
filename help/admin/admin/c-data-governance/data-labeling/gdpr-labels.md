---
description: Beispiele für Datenschutzbezeichnungen für Adobe Analytics-Variablen
title: Datenschutzbezeichnungen für Analytics-Variablen
feature: Data Governance
role: Admin
exl-id: b8c2143a-6e8e-465a-979b-aa8176e8d4e8
source-git-commit: 750c4b0ffb52c3f2cf25abcd76ef149a4521109e
workflow-type: tm+mt
source-wordcount: '3569'
ht-degree: 97%

---

# Datenschutzbezeichnungen für Analytics-Variablen

## Grund für die Datenkennzeichnung {#why-label}

Die Kundinnen und Kunden von Adobe müssen als Datenverantwortliche sicherstellen, dass geltende Datenschutzgesetze wie die DSGVO und CCPA eingehalten werden. Sie sollten sich daher mit ihrer eigenen Rechtsabteilung beraten, um zu bestimmen, wie ihre Daten im Einklang mit den Datenschutzgesetzen verarbeitet werden sollen. Adobe weiß, dass jede Kundin und jeder Kunde individuelle Datenschutzanforderungen hat. Deshalb ermöglicht Adobe es auch, die gewünschten Datenschutzeinstellungen für die Datenverarbeitung anzupassen. So kann jeder Unique Customer Datenschutzanfragen so verarbeiten, wie es für seine Marke und seine Datensätze am sinnvollsten ist.

Adobe Analytics stellt Werkzeuge zur Verfügung, um Daten entsprechend ihrer Sensibilität und ihren vertraglichen Beschränkungen zu kennzeichnen. Kennzeichnungen sind ein wichtiger Schritt, um (1) die betroffenen Personen zu identifizieren, (2) zu bestimmen, welche Daten im Zuge der Auskunftspflicht zurückgegeben werden müssen, und (3) Datenfelder zu identifizieren, die im Rahmen einer Löschanfrage gelöscht werden müssen.

Bevor Sie ermitteln, welche Beschriftungen den einzelnen Variablen und Feldern hinzugefügt werden müssen, sollten Sie zunächst die [Grundlagen zu den IDs](/help/admin/admin/c-data-governance/data-labeling/gdpr-analytics-ids.md) kennen, die Sie in Ihren Analytics-Daten erfassen, und entscheiden, welche hiervon Sie für Datenschutzanfragen verwenden wollen.

Die Adobe Analytics-Datenschutzimplementierung unterstützt folgende Beschriftungen für Identitätsdaten, vertrauliche Daten und Data Governance.

## Kennzeichnungen für Identitätsdaten {#identity-data-labels}

Die Kennzeichnung für Identitätsdaten („I“) wird verwendet, um Daten zu kategorisieren, über die eine bestimmte Person identifiziert oder kontaktiert werden kann.

| Beschriftung | Definition | Weitere Anforderungen |
| --- | --- | --- |
| I1 | Direkt identifizierbar: Daten, die zur Identifikation von oder direkten Kontaktaufnahme mit Personen genutzt werden können, wie z. B. Name oder E-Mail-Adresse | <ul><li>Kann nicht für Ereignisse festgelegt werden</li><li>Kann nicht für Merchandising-eVars festgelegt werden</li></ul> |
| I2 | Indirekt identifizierbar: Daten, die in Kombination mit beliebigen anderen Daten dazu verwendet werden können, eine Person oder ein Gerät zu identifizieren oder direkt zu kontaktieren.  Ermöglicht nicht die direkte Identifikation einer Person, sondern muss mit anderen Informationen (ob in Ihrem Besitz oder nicht) kombiniert werden, um die Person zu bestimmen. Hierzu zählen beispielsweise Kundentreue- oder im Unternehmens-CRM-System verwendete IDs, die für jeden Kunden eindeutig sind. | <ul><li>Kann nicht für Ereignisse festgelegt werden</li><li>Kann nicht für Merchandising-eVars festgelegt werden</li></ul> |

{style="table-layout:auto"}

## Kennzeichnungen für vertrauliche Daten {#sensitive-data-labels}

Diese Kennzeichnung („S“) wird verwendet, um vertrauliche Daten, wie z. B. geografische Daten, zu kategorisieren. In Zukunft werden zusätzliche Datenkennzeichnungen verfügbar sein, um andere Arten vertraulicher Informationen zu kennzeichnen.

| Beschriftung | Definition |
| --- | --- |
| S1 | Präzise Geostandortdaten mit Längen- und Breitengrad, die verwendet werden können, um den genauen Standort eines Geräts zu ermitteln (mit einer Abweichung von 100 Metern oder weniger). |
| S2 | Geostandortdaten, die verwendet werden können, um weit gefasste Geofencing-Bereiche zu bestimmen. |

{style="table-layout:auto"}

## Data-Governance-Kennzeichnungen (Datenschutz) {#data-governance-labels}

Über Data Governance-Kennzeichnungen können Benutzende Daten klassifizieren, die datenschutzbezogene Überlegungen und vertragliche Bedingungen enthalten. Kundinnen und Kunden von Adobe werden so bei der Einhaltung von Verordnungen und Unternehmensrichtlinien unterstützt.

### Datenschutz – Auskunftskennzeichnungen

| Beschriftung | Definition | Weitere Anforderungen |
| --- | --- | --- |
| Keine | Wählen Sie diese Option aus, wenn diese Variable keine Daten enthält, die im Rahmen einer Datenschutz-Auskunftsanfrage in die an die betroffene Person zurückzugebenden Daten eingefügt werden müssen. | |
| ACC-ALL | Werte in diesem Feld sollten in allen Datenschutzanfragen enthalten sein. Wenn dieser Hit von einem Gerät stammt, das von mehreren Personen genutzt wird, können Sie als Datenverantwortlicher über diese Beschriftung festlegen, dass es zulässig ist, die Daten in diesem Feld an Personen mit Zugriff auf das gemeinsam genutzte Gerät zu übermitteln. | Felder mit dieser Beschriftung werden bei allen Datenschutzanfragen zurückgegeben. |
| ACC-PERSON | Werte in diesem Feld sollten nur zu Datenschutzanfragen hinzugefügt werden, wenn Sie sich ausreichend sicher sind, dass der Treffer von der betroffenen Person stammt. Dies gilt, wenn die ID einer Datenschutzanfrage mit dem Wert im Feld ID-PERSON übereinstimmt. | Sie müssen auch eine ID-PERSON-Beschriftung in einer Variablen innerhalb dieser Report Suite festgelegt haben und Anfragen mit der entsprechenden ID übermitteln. Andernfalls wird diese Beschriftung nie angewendet. |

{style="table-layout:auto"}

Obwohl nur wenige Variablen andere Kennzeichnungen erhalten werden, ist davon auszugehen, dass auf eine Vielzahl Ihrer Variablen Zugriffskennzeichnungen angewendet werden. Es obliegt jedoch Ihnen, nach Absprache mit Ihrer Rechtsabteilung zu entscheiden, welche der von Ihnen erfassten Daten für die betroffenen Personen freigegeben werden sollen.

### Datenschutz-Löschkennzeichnungen

Im Gegensatz zu anderen Beschriftungen schließen sich diese Löschbeschriftungen nicht gegenseitig aus. Sie können eine von ihnen, beide oder keine auswählen. Eine separate [!UICONTROL None]-Beschriftung ist nicht erforderlich, da [!UICONTROL None] einfach dadurch angezeigt wird, dass keine der Löschoptionen aktiviert wird.

Eine Löschkennzeichnung ist nur für Felder mit einem Wert erforderlich, der die Zuordnung eines Treffers zur betroffenen Person zulässt (d. h. der die Identifizierung der betroffenen Person ermöglicht). Andere persönliche Daten (Favoriten, Browser-/Einkaufsverlauf, Gesundheitszustand usw.) müssen nicht gelöscht werden, da die Zuordnung zur betroffenen Person entfernt wird.

| Beschriftung | Definition | Weitere Anforderungen |
| --- | --- | --- |
| DEL-DEVICE | Bei Datenschutz-Löschanfragen sollten Werte in diesem Feld nur bei Anfragen anonymisiert werden, bei denen eine bestimmte ID-DEVICE im Treffer vorhanden ist.  Wenn derselbe Wert in anderen Treffern auftritt, die nicht gelöscht werden, werden diese Instanzen nicht geändert. So ändern sich die Werte bei Berichten, die eindeutige Anzahlen in diesem Feld berechnen. Auf gemeinsam genutzten Geräten werden hierdurch möglicherweise IDs von anderen als nur der betroffenen Person entfernt.  Die Werte ändern sich nicht, wenn dieses Feld eine ID-DEVICE-Beschriftung enthält und der Wert in diesem Feld als ID für eine Datenschutzanfrage verwendet wurde. | <ul><li>Erfordert auch eine I1- oder I2-/S1-Beschriftung</li><li>Kann nicht für Ereignisse festgelegt werden</li><li>Kann nicht für Merchandising-eVars festgelegt werden</li></li><li>Kann nicht für Classifications festgelegt werden</li><li>Sie müssen Anfragen mit einer ID-DEVICE-Beschriftung senden oder „expandIDs“ auf „true“ festlegen. Andernfalls wird diese Beschriftung nie angewendet.</li></ul> |
| DEL-PERSON | Bei Datenschutz-Löschanfragen sollten Werte in diesem Feld nur bei Anfragen anonymisiert werden, bei denen eine bestimmte ID-PERSON im Treffer vorhanden ist.  Wenn derselbe Wert in anderen Treffern auftritt, die nicht gelöscht werden, werden diese Werte nicht geändert. Dies führt zu einer Änderung von Anzahlen bei Berichten, die eindeutige Anzahlen in diesem Feld berechnen. Die Werte ändern sich nicht, wenn dieses Feld eine ID-PERSON-Beschriftung enthält und der Wert in diesem Feld als ID für eine Datenschutzanfrage verwendet wurde. | <ul><li>Erfordert auch eine I1- oder I2-/S1-Beschriftung</li><li>Kann nicht für Ereignisse festgelegt werden</li><li>Kann nicht für Merchandising-eVars festgelegt werden</li></li><li>Kann nicht für Classifications festgelegt werden</li><li>Sie müssen Anfragen übermitteln, die eine ID-PERSON-Kennzeichnung verwenden, die in einer Variablen innerhalb dieser Report Suite festgelegt ist, und Anfragen unter Verwendung dieser ID übermitteln, sonst wird diese Kennzeichnung nie angewendet.</li></ul> |

{style="table-layout:auto"}

### Datenschutz-Identitätskennzeichnungen

| Beschriftung | Definition | Weitere Anforderungen |
| --- | --- | --- |
| Keine | Diese Variable enthält keine ID, die für Datenschutzanfragen verwendet wird. | Sie müssen eine dieser anderen Kennzeichnungen nur dann festlegen, wenn dieses Feld eine ID enthält, die Sie bei der Übermittlung von Zugriffs- oder Löschanfragen über die [Privacy Service-API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html?lang=de) oder die Benutzeroberfläche verwenden werden. |
| ID-DEVICE | Dieses Feld enthält eine ID, die Sie zur Identifizierung eines Geräts für eine Datenschutzanfrage verwenden können. Sie kann jedoch nicht zwischen den verschiedenen Benutzern eines gemeinsam genutzten Geräts unterscheiden.  Sie müssen diese Beschriftung nicht für alle Variablen angeben, die IDs enthalten (dazu dienen die I1/I2-Beschriftungen). Verwenden Sie diese Beschriftung, wenn Sie mithilfe von in dieser Variablen gespeicherten IDs Datenschutzanfragen senden und wenn Sie diese Variable für die angegebene ID suchen möchten. | Erfordert auch eine I1- oder I2-Beschriftung.<ul><li>Kann nicht für Ereignisse festgelegt werden</li><li>Kann nicht für Merchandising-eVars festgelegt werden</li><li>Kann nicht für Classifications festgelegt werden</li></ul> |
| ID-PERSON | Dieses Feld enthält eine ID, die verwendet werden kann, um einen authentifizierten Benutzer (eine bestimmte Person) für eine Datenschutzanfrage zu identifizieren.  Sie müssen diese Beschriftung nicht für alle Variablen angeben, die IDs enthalten (dazu dienen die I1/I2-Beschriftungen). Verwenden Sie diese Beschriftung, wenn Sie mithilfe von in dieser Variablen gespeicherten IDs Datenschutzanfragen senden und wenn Sie diese Variable für die angegebene ID suchen möchten. | <ul><li>Erfordert auch eine I1- oder I2-Beschriftung.</li><li>Kann nicht für Ereignisse festgelegt werden</li><li>Kann nicht für Merchandising-eVars festgelegt werden</li><li>Kann nicht für Classifications festgelegt werden</li></ul> |

{style="table-layout:auto"}

## Bereitstellen eines Namespace bei der Kennzeichnung einer Variablen als ID-DEVICE oder ID-PERSON {#provide-namespace}

Wenn Sie eine Variable als ID-DEVICE oder ID-PERSON beschriften, werden Sie zum Bereitstellen eines Namespace aufgefordert. Sie können entweder einen zuvor definierten Namespace verwenden oder einen neuen definieren.

### Verwenden eines zuvor definierten Namespace

Wenn Sie zuvor anderen Variablen in einer beliebigen Report Suite in Ihrem Anmeldeunternehmen eine ID-Beschriftung zugewiesen haben, können Sie einen dieser vorhandenen Namespaces auswählen. Sie sollten den Namespace wiederverwenden, wenn diese Variable denselben ID-Typ enthält wie andere Variablen, die bereits mit diesem Namespace beschriftet sind, und Sie beim Senden einer Anfrage alle Variablen durchsuchen wollen.

1. Klicken Sie auf **[!UICONTROL Namespace auswählen]**, und wählen Sie einen der vorhandenen Namespaces aus.
1. Klicken Sie auf **[!UICONTROL Übernehmen]**.

![](assets/namespace.png)

### Definieren eines neuen Namespace

Sie können auch einen neuen Namespace definieren. Es wird empfohlen, Namespace-Zeichenfolgen auf alphanumerische Zeichen sowie Unterstriche, Bindestriche und Leerzeichen zu beschränken. Alle Zeichen werden in Kleinschreibung konvertiert.

1. Klicken Sie auf **[!UICONTROL Namespace auswählen]**, und geben Sie den Namespace-Titel ein.

   ![](assets/namespace2.png)

1. Drücken Sie die **[!UICONTROL Eingabetaste]**, um diesen Namespace hinzuzufügen. Erst jetzt ist die Schaltfläche „Übernehmen“ aktiviert.
1. Klicken Sie auf **[!UICONTROL Übernehmen]**.

Die von Ihnen als Namespace angegebene Zeichenfolge ist dieselbe Zeichenfolge, die Sie beim Senden von Anfragen über die Datenschutz-API als Wert des Parameters „namespace“ verwenden sollten. Aufgrund der Anfrage durchsucht Adobe Analytics anschließend alle Variablen in allen Report Suites, in denen dieser Namespace verwendet wird, nach der ID, die Sie in der Anfrage angegeben haben.

Sie müssen die Kennzeichnungen ID-DEVICE oder ID-PERSON nicht für alle Variablen angeben, die IDs enthalten (dazu dienen die I1/I2-Kennzeichnungen). Verwenden Sie diese Beschriftung, wenn Sie mithilfe von in dieser Variablen gespeicherten IDs Datenschutzanfragen senden und wenn Sie diese Variable für die angegebene ID suchen möchten. Beispiel: eVar1 kann eine E-Mail-Adresse enthalten, während eVar2 einen Benutzernamen für die Anmeldung beinhaltet. Sie senden jedoch Anfragen ausschließlich mithilfe des Benutzernamens. In diesem Fall können Sie eVar1 als I1, ACC-PERSON, DEL-PERSON und eVar2 als I2, ACC-PERSON, DEL-PERSON, ID-PERSON mit dem Namespace „user name“ beschriften. Anschließend können Sie eine Anfrage mit einem JSON-Block für den Benutzerabschnitt senden, z. B.:

```
{
     "namespace": "user name",
     "type": "analytics",
     "value": "rocketman123"
}
```

Sie können denselben Namespace für verschiedene Variablen innerhalb derselben Report Suite verwenden. Bei einigen benutzerdefinierten Implementierungen wird beispielsweise eine CRM-ID in einem Prop- und einem eVar-Objekt gespeichert. Wenn die CRM-ID immer in einer der Variablen auftritt (z. B. in der eVar) und nur gelegentlich in der anderen (Prop) enthalten ist bzw. niemals in der Prop enthalten ist, wenn sie auch nicht in der eVar vorkommt, ist nur für das eVar-Objekt eine ID-Kennzeichnung und ein Namespace erforderlich, da Adobe nur diese eVar nach der ID durchsuchen kann. Wenn jedoch die CRM-ID manchmal in einer Variablen und manchmal in der anderen auftritt, sollten beide denselben Namespace haben. Adobe durchsucht dann beide Variablen nach Vorkommen der ID, die im Rahmen einer Datenschutzanfrage mit diesem Namespace angegeben wird. Sie sollten weiterhin DEL-Beschriftungen für all diese Variablen festlegen, damit der Wert anonymisiert wird, egal, wo er auftritt.

Als weiteres Beispiel dient der Fall, in dem Sie eine CRM-ID verwenden, die manchmal via eVar1 und manchmal via prop7 gesendet wird. Mithilfe einer Verarbeitungsregel wird der Wert auf eVar1 (sofern vorhanden) in eVar3 kopiert. Andernfalls wird der Wert von prop7 in eVar3 kopiert. In diesem Szenario enthält eVar3 immer die CRM-ID (sofern sie bekannt ist), sodass nur für eVar3 eine ID-PERSON-Kennzeichnung erforderlich ist.

>[!CAUTION]
>
>Die Namespaces „visitorId“ und „customVisitorId“ sind zur Identifikation des früheren Tracking-Cookies von Analytics und der benutzerdefinierten Besucher-ID von Analytics reserviert. Verwenden Sie diese Namespaces nicht für benutzerdefinierte Traffic-Variablen oder Konversionsvariablen.

## Variablentypen und unterstützte Datenschutzkennzeichnungen {#variable-types}

Datenschutzkennzeichnungen wirken sich auf vier Klassen von Analytics-Variablen aus. Nicht alle Variablen unterstützen alle Kennzeichnungen. Die folgende Tabelle zeigt, welche Variablen welche Kennzeichnungen unterstützen bzw. nicht unterstützen.

| Variablentyp | Unterstützte Beschriftungen | Nicht unterstützte Beschriftungen |
|--- |--- |--- |
| <ul><li>Benutzerspezifische Erfolgsereignisse</li><li>Merchandising-eVars</li><li>Mehrwertige Variablen (mvVars)</li><li>Hierarchievariablen</li></ul> | <ul><li>S1/S2</li><li>ACC-ALL, ACC-PERSON</li></ul> | <ul><li>I1/I2</li>  <li>ID-DEVICE, ID-PERSON</li><li>DEL-DEVICE, DEL-PERSON</li></ul> |
| Classifications | <ul><li>I1/I2, S1/S2</li><li>ACC-ALL, ACC-PERSON</li></ul> | <ul><li>ID-DEVICE, ID-PERSON</li><li>DEL-DEVICE, DEL-PERSON</li></ul> |
| <ul><li>Traffic-Variablen (Props)</li><li>Commerce-Variablen (Nicht-Merchandising-eVars)</li></ul> | Alle Beschriftungen | – |
| Die meisten anderen Variablen (*Siehe Tabelle unten mit Ausnahmen*) | ACC-ALL, ACC-PERSON | <ul><li>I1/I2, S1/S2</li><li>ID-DEVICE, ID-PERSON</li><li>DEL-DEVICE, DEL-PERSON)</li></ul> |

{style="table-layout:auto"}

## Variablen, bei denen andere Beschriftungen als ACC-ALL/ACC-PERSON zugewiesen/geändert werden können {#variables}

<table id="table_0972910DB2D7473588F23EA47988381D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Gruppe </th> 
   <th colname="col2" class="entry"> Variablen </th> 
   <th colname="col3" class="entry"> Änderbare Beschriftungen </th> 
   <th colname="col4" class="entry"> Kommentar </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" morerows="1"> 
    <ul id="ul_62FA1BAA3B9245909509566D8C03F900"> 
     <li id="li_38F7C4E18ECB42C292370713F502B8EB">Konversion-Dimensionen </li> 
     <li id="li_41CB61F927CB4402AAB4A62E219CD153">Benutzerspezifische Traffic-Dimensionen </li> 
    </ul> </td> 
   <td colname="col2"> <p>Alle außer Classifications </p> </td> 
   <td colname="col3"> <p>Alle </p> </td> 
   <td colname="col4"> </td> 
  </tr>
  <tr> 
   <td colname="col1"> <p>Traffic-Variablen </p> </td> 
   <td colname="col2"> <p>Listen-Props </p> </td> 
   <td colname="col3"> <p>None/S1/S2 </p> </td> 
   <td colname="col4"> <p>Listen-Props können mehrere Werte enthalten und sind nicht als Datenschutzbezeichner zulässig.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Classifications </p> </td> 
   <td colname="col3"> <p>None/I1/I2 </p> <p>None/S1/S2 </p> </td> 
   <td colname="col4"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Konversionsereignisse </p> </td> 
   <td colname="col2"> <p>Alle </p> </td> 
   <td colname="col3"> <p>None/S1/S2 </p> </td> 
   <td colname="col4"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lösungsdimensionen und Ereignisse </p> </td> 
   <td colname="col2"> <p>Activity Map-Link, </p> <p>Activity Map-Seite </p> </td> 
   <td colname="col3"> <p>None/I1/I2 </p> <p>None/DEL-DEVICE/DEL-PERSON </p> </td> 
   <td colname="col4"> <p>Variablen können URL-Parameter enthalten, die möglicherweise direkt oder indirekt identifizierbare Daten beinhalten. Wenn Ihre Implementierung keine direkt oder indirekt identifizierbaren Daten in diesen Variablen erfasst, benötigen sie keine Identitäts- oder Löschkennzeichnungen. </p> <p>Hinweis: Beim Löschen werden die URL-Parameter entfernt, aber die Basis-URL wird beibehalten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Datenverarbeitungsdimensionen </p> </td> 
   <td colname="col2"> <p>Benutzerspezifische Besucher-ID </p> </td> 
   <td colname="col3"> <p>ID-DEVICE/ID-PERSON </p> <p>DEL-DEVICE/DEL-PERSON </p> </td> 
   <td colname="col4"> <p>Die ID- oder DEL-Beschriftungen (mit „None“ festgelegt) können zwar nicht entfernt werden, Sie können sie aber je nach benutzerdefinierter ID-Implementierung in die DEVICE- oder PERSON-Variante ändern. </p> <p>Wenn Sie die benutzerdefinierte Besucher-ID nicht verwenden, hat die Einstellung keine Bedeutung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="1"> 
    <ul id="ul_5EB0193732D44A20AEA08CE9DFE01DBD"> 
     <li id="li_F70D969F83314A94BD8567449968EE2F">Standarddimensionen </li> 
     <li id="li_6046764B19FF4679B51E55671C2C0ADB">Datenverarbeitungsdimensionen </li> 
    </ul> </td> 
   <td colname="col2"> <p>IP-Adresse </p> <p>IP-Adresse 2 </p> </td> 
   <td colname="col3"> <p>DEL-DEVICE/DEL-PERSON </p> </td> 
   <td colname="col4"> <p>Sie können die DEL-Beschriftung zwar nicht ändern, Sie können sie jedoch zu DEL-DEVICE oder DEL-PERSON oder beidem ändern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>ClickMap-Aktion (Legacy), </p> <p>ClickMap-Kontext (Legacy), </p> <p>Seite, </p> <p>Seiten-URL, </p> <p>URL der ursprünglichen Entrypage, </p> <p>Verweisende Stelle, </p> <p>Besuchen der Startseiten-URL </p> </td> 
   <td colname="col3"> <p>None/I1/I2 </p> <p>None/DEL-DEVICE/DEL-PERSON </p> </td> 
   <td colname="col4"> <p>Variablen können URL-Parameter enthalten, die möglicherweise direkt oder indirekt identifizierbare Daten beinhalten. Wenn Ihre Implementierung keine direkt oder indirekt identifizierbaren Daten in diesen Variablen erfasst, benötigen sie keine Identitäts- oder Löschkennzeichnungen. </p> <p>Hinweis: Beim Löschen werden die URL-Parameter entfernt, aber die Basis-URL wird beibehalten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Löschverarbeitung {#deletion}

Die Adobe Analytics-Unterstützung für Datenschutz-Löschanfragen soll die Auswirkungen auf das Reporting minimieren. In den meisten Fällen sollten sich die in Berichten angezeigten Metriken nicht ändern. Ein Verlaufsbericht, der vor der Datenschutzlöschung ausgeführt wurde, stimmt mit dem Bericht nach der Löschung überein. Dies wird erreicht, indem die gelöschten Daten vollständig von der betroffenen Person getrennt werden, während nicht identifizierbare Daten beibehalten werden, damit die berichteten Werte konsistent bleiben.

Die folgende Tabelle zeigt, wie verschiedene Variablen „gelöscht“ werden. Die Liste ist nicht vollständig.

| Variablen | Löschmethode |
| --- | --- |
| <ul><li>Traffic-Variablen (Props)</li><li>Commerce-Variablen (eVars)</li></ul> | Der bestehende Wert wird durch einen neuen Wert der Form „Datenschutz-356396D55C4F9C7AB3FBB2F2FA223482“ ersetzt, wobei der 32-stellige Hexadezimalwert nach dem Präfix „Datenschutz-“ eine kryptografisch starke 128-Bit-Pseudozufallszahl ist.<p>Da der Wert im Wesentlichen durch eine zufällige Zeichenfolge ersetzt wird, gibt es keine Möglichkeit, den ursprünglichen Wert aus diesem neuen Wert zu bestimmen, und keine Möglichkeit, den neuen Wert abzuleiten, wenn der ursprüngliche Wert bekannt ist.  Wenn bei einer Variablen der ersetzte Wert auch in anderen Treffern auftritt, die im Rahmen derselben Datenschutzanfrage ebenfalls gelöscht werden, werden alle Instanzen dieses Werts durch den neuen Wert ersetzt.<p>Wenn einige Instanzen eines Werts mit einer Löschanfrage ersetzt werden und im Rahmen einer späteren Anfrage andere (neue) Instanzen des ursprünglichen Werts gelöscht werden, unterscheidet sich der neue Ersatzwert vom ursprünglichen Ersatzwert. |
| Kauf-ID | Der bestehende Wert wird durch einen neuen Wert der Form „G-7588FCD8642718EC50“ ersetzt, wobei der 18-stellige Hexadezimalwert nach dem Präfix „G-“ den ersten 18 Stellen einer kryptografisch starken 128-Bit-Pseudozufallszahl entspricht. Alle Kommentare, die sich auf das Löschen von Traffic- und Commerce-Variablen beziehen, gelten auch hier.<p>Die Kauf-ID ist eine Transaktions-ID, die primär sicherstellen soll, dass ein Kauf nicht zweimal berechnet wird, z. B. wenn jemand die Bestätigungsseite aktualisiert. Die ID selbst kann den Kauf mit einer Zeile in Ihrer eigenen Datenbank verknüpfen, wo der Kauf aufgezeichnet wird. In den meisten Fällen ist es nicht notwendig, diese ID zu löschen, sodass sie standardmäßig nicht gelöscht wird.<p>Wenn Sie nach der Datenschutz-Löschanfrage Ihrer eigenen Daten den Kauf noch an einen Benutzer binden können, müssen Sie dieses Feld möglicherweise löschen, damit die Analytics-Daten für diesen Besucher nicht an den Käufer gebunden werden können. |
| Besucher-ID | Der Wert ist eine 128-Bit-Ganzzahl und wird durch einen kryptographisch starken 128-Bit-Pseudozufallswert ersetzt. |
| <ul><li>MCID</li><li>Benutzerspezifische Besucher-ID</li><li>IP-Adresse</li><li>IP-Adresse 2 | Der Wert wird gelöscht (d. h. je nach Variablentyp entweder durch eine leere Zeichenfolge oder „0“ ersetzt). |
| <ul><li>ClickMap-Aktion (Legacy)</li><li>ClickMap-Kontext (Legacy)</li><li>Seite</li><li>Seiten-URL</li><li>URL der ursprünglichen Entrypage</li><li>Referrer</li><li>Besuchen der Startseiten-URL</li></ul> | Die URL-Parameter werden gelöscht/entfernt. Wenn der Wert nicht wie eine URL aussieht, wird der Wert gelöscht (auf die leere Zeichenfolge gesetzt). |
| <ul><li>Breitengrad</li><li>Längengrad</li></ul> | Die Genauigkeit wird auf maximal einen Kilometer reduziert. |

{style="table-layout:auto"}

## Variablen, die die erwarteten Löschkennzeichnungen möglicherweise nicht unterstützen {#no-delete-support}

Diese Abschnitt enthält Informationen zu Analytics-Variablen, die die Löschung möglicherweise nicht unterstützen. Manchmal werden diese Variablen von anderen Personen als Analytics-Benutzenden (z. B. von der Rechtsabteilung) gelöscht, die mit dem in der Variablen enthaltenen Datentyp nicht vertraut sind und deshalb anhand des Variablennamens von einer bestimmten Annahme ausgehen.

Es ist wichtig zu verstehen, welche Datentypen in den einzelnen Variablen enthalten sind, bevor Sie eine Entscheidung über die Kennzeichnung oder Löschung treffen, und sich nicht allein auf den Variablennamen zu verlassen. Im Folgenden finden Sie eine Liste dieser Variablen und erfahren, warum sie unter Umständen keine Löschung erfordern bzw. warum sie ggf. nicht über eine spezifische Löschkennzeichnung verfügen:

| Variable | Kommentare |
| --- | --- |
| [!UICONTROL Neue Besucher-ID] | „Neue Besucher-ID“ ist ein boolescher Wert, der beim ersten Auftreten der entsprechenden Besucher-ID „true“ lautet. Sie müssen den Wert nicht löschen, nachdem die Besucher-ID anonymisiert wurde. Nach der Anonymisierung entspricht der Wert dem ersten Auftritt der anonymisierten ID. |
| [!UICONTROL Postleitzahl]<p>[!UICONTROL Geo-Postleitzahl] | Postleitzahlen werden nur für Hits aus den USA festgelegt. Für Hits aus der EU werden sie nicht verwendet. Selbst wenn sie festgelegt werden, beschreiben sie nur einen breiten geografischen Bereich, der die Identifizierung der betroffenen Person schwierig gestaltet. |
| [!UICONTROL Geo-Breitengrad]<p>[!UICONTROL Geo-Längengrad] | Diese bieten einen ungefähren Standort, der aus der IP-Adresse abgeleitet wird. Die Genauigkeit ist im Allgemeinen ähnlich wie bei einer Postleitzahl, also einige Dutzend Kilometer vom tatsächlichen Standort. |
| [!UICONTROL Benutzeragent] | Der Benutzeragent identifiziert die Version des verwendeten Browsers. |
| [!UICONTROL Benutzer-ID] | Gibt die Analytics Report Suite (als Nummer) an, die die Daten enthält. |
| [!UICONTROL Report Suite-ID] | Gibt den Namen der Analytics Report Suite an, die die Daten enthält. |
| [!UICONTROL Besucher-ID]<p>[!UICONTROL MCID]/[!UICONTROL ECID] | Diese IDs haben eine DEL-DEVICE-Kennzeichnung, aber die DEL-PERSON-Kennzeichnung kann nicht hinzugefügt werden. Wenn Sie bei jeder Anfrage [!UICONTROL ID-Erweiterung] angeben, werden diese IDs automatisch bei allen Löschanfragen gelöscht, auch wenn eine ID-PERSON verwendet wird.<p>Wenn Sie die ID-Erweiterung nicht verwenden, aber diese Cookie-IDs in Hits anonymisieren wollen, die eine übereinstimmende ID in einer Prop oder eVar enthalten, können Sie diese Kennzeichnungsbeschränkung umgehen, indem Sie der Prop oder eVar eine ID-DEVICE-Kennzeichnung hinzufügen, selbst wenn sie eigentlich eine Person identifiziert (darüber hinaus müssen alle DEL-PERSON-Kennzeichnungen in DEL-DEVICE-Kennzeichnungen geändert werden). Da in diesem Fall nur einige Instanzen der Besucher-ID oder ECID anonymisiert werden, ändern sich die Zahlen der Unique Visitors im Verlaufsbericht. |
| [!UICONTROL AMO-ID] | Die Adobe Advertising Cloud ID ist eine Lösungsvariable, die über eine unveränderliche [!UICONTROL DEL-DEVICE]-Kennzeichnung verfügt. Sie wird über ein Cookie festgelegt, genau wie die Besucher-ID und die MCID. Sie sollte aus Hits gelöscht werden, wenn diese anderen IDs gelöscht werden. Weitere Informationen finden Sie in den Beschreibungen der entsprechenden Variablen. |

{style="table-layout:auto"}

## Datumsfelder für Zugriffsanfragen {#access-requests}

Es gibt fünf Standardvariablen, die Zeitstempel enthalten:

| Zeitstempel | Definition |
| --- | --- |
| Hit Time UTC | Der Zeitpunkt, zu dem der Treffer von Adobe Analytics empfangen wurde. |
| Custom Hit Time UTC | Der Zeitpunkt, zu dem der Treffer stattgefunden hat, der bei einigen mobilen Apps und anderen Implementierungen vor dem Zeitpunkt liegen kann, zu dem der Treffer empfangen wurde. Wenn beispielsweise eine Netzwerkverbindung zum Zeitpunkt des Auftretens nicht verfügbar war, kann die App den Treffer halten und übermitteln, wenn eine Verbindung verfügbar wird. |
| Date Time | Derselbe Wert wie „Custom Hit Time UTC“, jedoch in der Zeitzone der Report Suite und nicht in GMT. |
| First Hit Time GMT | Der „Custom Hit Time UTC“-Wert für den ersten Treffer, der für den Besucher-ID-Wert für diesen Treffer empfangen wurde. |
| Visit Start Time UTC | Der „Custom Hit Time UTC“-Wert für den ersten Treffer, der für den aktuellen Besuch für diese Besucher-ID empfangen wurde. |

{style="table-layout:auto"}

Für den Code zur Generierung der für Datenschutz-Zugriffsanfragen zurückgegebenen Dateien ist es erforderlich, dass mindestens eine der ersten drei Zeitstempelvariablen in die Zugriffsanfrage aufgenommen wird (mit einer ACC-Beschriftung, die für die Art der Anforderung gilt). Wenn keine davon enthalten ist, wird „Custom Hit Time UTC“ so behandelt, als hätte es eine „ACC-ALL“-Beschriftung.

Die CSV-Datei auf Trefferebene, die für Datenschutzanfragen zurückgegeben wird, konvertiert die Werte in diesen Feldern von Unix-Zeitstempeln in Datums-/Uhrzeitfelder des Formats `YYYY-MM-DD HH:MM:SS` (zum Beispiel: `2018-05-01 13:49:22`). In der Zusammenfassungs-HTML-Datei werden diese Zeitstempelwerte abgeschnitten, um nur das Datum, `YYYY-MM-DD`, um die Anzahl der eindeutigen Werte für diese Felder zu reduzieren.
