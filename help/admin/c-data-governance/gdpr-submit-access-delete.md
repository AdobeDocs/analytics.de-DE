---
description: So fordern Sie Datenzugriff und -löschung in Adobe Analytics an.
title: Zugriffs- und Löschanfragen einreichen
feature: Data Governance
exl-id: bb94cedf-ac9b-4d38-9136-bd3da2acf018
source-git-commit: f135138de15f3fc788e637128daeb064d0d453af
workflow-type: tm+mt
source-wordcount: '1297'
ht-degree: 68%

---

# Zugriffs- und Löschanfragen einreichen

Wenn Ihre Kunden (Verbraucher/Datensubjekte) wissen möchten, welche Daten Sie über sie verwalten, oder entscheiden, dass sie aus Ihren Analytics-Eigenschaften gelöscht werden sollen, sind Sie als Datenverantwortlicher für die Beantwortung dieser Anfragen verantwortlich. Der Datenverantwortliche bestimmt, wie Ihr Unternehmen mit betroffenen Personen interagiert (z. B. über ein Benutzerportal für betroffene Personen), und verwaltet die Interaktionen mit der betroffenen Person. Es liegt auch in der Verantwortung des Datenverantwortlichen, die Schleife mit dem Datensubjekt zu schließen, wenn die Anfrage erfüllt wird. Mit anderen Worten: Adobe Experience Cloud als Datenverarbeiter akzeptiert keine Anforderungen direkt von betroffenen Personen oder gibt Daten direkt an diese zurück. Stattdessen erhält Adobe Anfragen von und gibt Daten nur als Datenverantwortlicher an Sie zurück.

Sie können auch sicherstellen, dass Ihre mobilen Apps und Websites über relevante Popup-Benachrichtigungen und unterstützende Materialien zu den Rechten der betroffenen Personen hinsichtlich ihrer direkt oder indirekt identifizierbaren Daten und anderen von Ihnen erfassten Daten verfügen.

## Kundeneinwilligung verwalten {#section_3012015E7E8942519FB9279CF7057EAB}

Als Datenverantwortlicher sind Sie dafür verantwortlich, die ausdrückliche Einwilligung von Ihren Datensubjekten einzuholen, bevor Sie Daten über sie erfassen (möglicherweise auch Adobe Analytics-Daten), und eine [Opt-out-Mechanismus](https://www.adobe.com/de/privacy/opt-out.html#customeruse) auf Ihrer Website. Auf diese Weise können sich Ihre betroffenen Personen von der künftigen Adobe Experience Cloud-Datenerfassung abmelden.

## Benutzer und ihre Daten validieren {#section_AFB2CC225AA94AF6A3CE9F24EF788358}

Als Datenverantwortlicher sind Sie dafür verantwortlich, zu überprüfen, ob das Datensubjekt die Person ist, für die es sich ausgibt, und dass es ein Recht auf die Daten hat, die von Ihnen angefordert werden. Außerdem müssen Sie sicherstellen, dass die richtigen Daten an die betroffene Person zurückgegeben werden und dass diese nicht versehentlich Daten über andere betroffene Personen erhält.

Dazu gehört das Überprüfen der von Adobe Analytics im Rahmen einer Datenschutz-Zugriffsanfrage zurückgegebenen Daten, bevor sie an die betroffene Person gesendet werden. Besonders vorsichtig sollten Sie sein, wenn Sie Personen-IDs verwenden und nicht nur Daten zurückgeben, in denen diese ID enthalten ist, sondern auch Daten für andere Hits auf gemeinsam genutzten Geräten, auf denen die entsprechende ID manchmal genutzt wurde. Siehe [ID-Erweiterung.](/help/admin/c-data-governance/gdpr-id-expansion.md)

Jede Datei kombiniert Daten von all Ihren Report Suites und entfernt automatisch zusätzliche Kopien replizierter Hits. Sie können entscheiden, welche dieser Dateien an die betroffene Person zurückgegeben werden soll. Oder Sie können einige dieser Daten extrahieren und mit Daten aus anderen Systemen kombinieren, bevor Sie sie an die betroffene Person zurücksenden.

## Anfragen einreichen  {#submit-requests}

Sie können Datenschutz-Zugriffs- und -Löschanfragen über unsere [Privacy Service-Benutzeroberfläche](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/overview.html?lang=de) oder unsere [Privacy Service-API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html?lang=de) senden.

>[!NOTE]
>
>Die Datenschutz-API unterstützt die Batch-Einsendung für mehrere Benutzer in einer einzelnen Anfrage. Die Unterstützungsgrenze liegt momentan bei 1000 separaten Benutzern (pro Benutzer können mehrere IDs vorliegen) in einer einzelnen JSON-Anfragedatei.

## JSON-Beispielanfrage  {#sample-json-request}

Hier sehen Sie den JSON-Abschnitt, der über die Datenschutz-API oder -UI eingereicht werden kann und mit dem die Datenschutzverarbeitung für drei Benutzer angefragt wird.

```
{ 
    "companyContexts": [ 
        { 
            "namespace": "imsOrgID", 
            "value": "5D7236525AA6D9580A495C6C@AdobeOrg" 
        } 
    ], 
    "users": [ 
        { 
            "key": "Data Privacy-1234", 
            "action": ["access"], 
            "userIDs": [ 
                { 
                    "namespace": "AAID", 
                    "namespaceId", 10, 
                    "type": "standard", 
                    "description": "Legacy Visitor ID", 
                    "value": "2D783E5885312539-4000010360000181", 
                } 
            ] 
        }, 
        { 
            "key": "Data Privacy-1235", 
            "action": ["access"], 
            "userIDs": [ 
                { 
                    "namespace": "ECID", 
                    "namespaceId": 4, 
                    "type": "standard", 
                    "description": "This is the ID generated by the Adobe ID service.", 
                    "value": "22470866493385587460528148368265592748", 
                } 
            ] 
        }, 
        { 
            "key": "Data Privacy-1236", 
            "action": ["access","delete"], 
            "userIDs": [ 
                { 
                    "namespace": "CRM-ID", 
                    "type": "analytics", 
                    "description": "namespace defined on eVar17 in some report suites", 
                    "value": "ACME-12345678"
                }, 
                { 
                    "namespace": "email address", 
                    "type": "analytics", 
                    "description": "namespace defined on eVar23 in some report suites", 
                    "value": "john@mail.com" 
                } 
            ] 
        } 
    ], 
    "expandIds": true 
} 
```

Beachten Sie, dass im Abschnitt des Benutzers drei Blöcke vorhanden sind, die drei separate Anforderungen darstellen, vermutlich für drei verschiedene Datensubjekte.

* Bei der ersten Anfrage handelt es sich um eine Zugriffsanfrage, in der eine herkömmliche Adobe Analytics-Cookie-ID (AAID) verwendet wird.
* Die zweite Anfrage ist ebenfalls eine Zugriffsanfrage, in der jedoch ein MCID-/ECID-Cookie verwendet wird.
* Die dritte Anfrage dient sowohl dem Zugriff als auch dem Löschen für die angegebenen IDs. Obwohl für alle Anfragen eine ID-Erweiterung angegeben ist, wird sie die größte Auswirkung auf die dritte Anfrage haben, weil dies die einzige Anfrage ist, für die Nicht-Cookie-IDs verwendet werden. Infolgedessen erkennt diese Anfrage auch Cookie-IDs, die beliebigen Geräten mit der angegebenen CRM-ID oder E-Mail-Adresse zugeordnet sind. Zudem wird die Anfrage erweitert, sodass sie auch diese IDs beinhaltet.

Bedenken Sie Folgendes

* Der Wert „5D7236525AA6D9580A495C6C@AdobeOrg“ im Abschnitt „companyContexts“ muss mit dem Wert Ihrer eigenen Experience Cloud-Organisation aktualisiert werden.
* Die Felder „type“ und „namespace“ werden im Abschnitt [Namespaces](/help/admin/c-data-governance/data-labeling/gdpr-namespaces.md) beschrieben.
* Die Felder „description“ werden ignoriert.
* Die Felder „key“ können beliebige Werte enthalten. Wenn Sie über eine interne ID zum Verfolgen von Datenschutzanfragen verfügen, können Sie hier den Wert ablegen, um die Zuordnung von Anfragen im Adobe-System zu denen in Ihren eigenen Systemen zu vereinfachen.

## Reaktionsdetails {#section_93F554F65DBB48A18B75EB5784056C96}

Diese Abschnitte enthalten Reaktionsdetails zum Zugriff und zum Löschen.

**Reaktionsdetails zum Zugriff**

Die für eine Zugriffsanfrage zurückgegebenen Daten enthalten eine URL, mit der Sie als Datenverantwortlicher eine ZIP-Datei herunterladen können, die einen Ordner für jedes Adobe-Produkt enthält, dessen Inhaber Sie sind. Im Analytics-Ordner können sich folgende Elemente befinden:

* Personendateien, abgeleitet aus Hits, die mit ID-PERSON übereinstimmen

   * Eine CSV-Datei mit einer Zeile für jeden passenden Treffer und einer Spalte für jedes Feld mit der Beschriftung ACC-ALL oder ACC-PERSON, sortiert nach Zeitstempel.
   * Eine HTML-Zusammenfassungsdatei mit einem Eintrag für jede ACC-ALL- oder ACC-PERSON-Beschriftung. Jeder Eintrag enthält alle eindeutigen Werte für das Feld sowie die Anzahl der jeweiligen Vorkommen. Felder mit Zeitstempeln werden gerundet, sodass nur eindeutige Tage angegeben werden.

* Gerätedateien, abgeleitet aus Treffern, in denen eines der Felder mit einer bestimmten ID-DEVICE, jedoch keines mit einer bestimmten ID-PERSON übereinstimmte

   * Eine CSV-Datei mit nur einer Zeile für jeden passenden Treffer und einer Spalte für jedes Feld mit der Beschriftung ACC-ALL, sortiert nach Zeitstempel.
   * HTML-Zusammenfassungsdatei mit einem Eintrag für jede ACC-ALL-Beschriftung. Jeder Eintrag enthält alle eindeutigen Werte für das Feld sowie die Anzahl der jeweiligen Vorkommen. Felder mit Zeitstempeln werden gerundet, sodass nur eindeutige Tage angegeben werden.

Jede Datei kombiniert Daten von all Ihren Report Suites und entfernt automatisch zusätzliche Kopien replizierter Hits.

Sie können entscheiden, welche dieser Daten an die betroffene Person zurückgegeben werden soll. Oder Sie können einige dieser Daten extrahieren und mit Daten aus anderen Systemen kombinieren, bevor Sie sie an die betroffene Person zurücksenden.

**Reaktionsdetails zum Löschen**

Bei Löschanfragen werden keine Daten zurückgegeben. Stattdessen wird ein Status an die Datenschutz-API übermittelt, der die erfolgreiche Bearbeitung der Anfrage angibt.

## Testen der Datenschutzverarbeitung Ihrer Daten {#section_FBA843DBFAE64D979D8DB8A3C56784D7}

In der Regel richten Analytics-Kunden einige Test-Report Suites ein, um die Funktionalität zu überprüfen, bevor sie Ressourcen der Öffentlichkeit zur Verfügung stellen. Bevor echter Traffic an die Produktions-Report Suites gesendet wird, senden Staging-Websites und -Apps die Daten an die entsprechenden Test-, Entwicklungs- oder QS-Report Suites, um zu überprüfen, wie sie nach Veröffentlichung des Codes funktionieren werden.

Mit einer normalen Konfiguration kann die Verarbeitung von DSGVO-Anfragen jedoch nicht erst an diesen Test-Report Suites getestet werden, bevor sie auf die Produktions-Report Suites angewendet wird. Grund hierfür ist, dass eine Datenschutzanfrage automatisch auf alle Report Suites in der Experience Cloud-Organisation angewendet wird, was häufig allen Report Suites für Ihr Unternehmen entspricht.

Es gibt jedoch einige Möglichkeiten, wie Sie Ihre Datenschutzverarbeitung vor der Anwendung auf all Ihre Report Suites testen können:

* Eine Option ist die Einrichtung einer separaten Experience Cloud-Organisation, die nur Test-Report Suites enthält. Verwenden Sie dann diese Experience Cloud-Organisation für Ihren Datenschutztest und Ihre normale Experience Cloud-Organisation für die eigentliche Datenschutzverarbeitung.
* Eine weitere Option ist es, den IDs in Ihren Test-Report-Suites andere Namespaces zuzuweisen als in den Produktions-Report-Suites.

   Sie können beispielsweise jedem Namespace in Ihren Test-Report Suites „qs-“ voranstellen. Wenn Sie Datenschutzanfragen senden, die nur Namespaces mit dem Präfix „qs-“ enthalten, werden diese Anfragen nur im Rahmen Ihrer Test-Report Suites ausgeführt. Wenn Sie die Anfragen später ohne das Präfix senden, werden sie auf Ihre Produktions-Report Suites angewendet. **Wir empfehlen diesen Ansatz, sofern Sie nicht die visitorId-, AAID-, ECID- oder customVisitorId-Namespaces verwenden, da diese fest codiert sind und Sie keine alternativen Namen in Ihren Test-Report Suites festlegen können**.
