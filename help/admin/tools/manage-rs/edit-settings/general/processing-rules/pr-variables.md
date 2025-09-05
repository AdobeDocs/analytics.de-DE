---
description: Die verfügbaren Dimensionen und Metriken, die Sie mithilfe von Verarbeitungsregeln lesen und schreiben können.
subtopic: Processing rules
title: Für Verarbeitungsregeln verfügbare Dimensionen und Metriken
feature: Processing Rules
role: Admin
exl-id: ffd7a1d6-2c9d-41e7-9c75-9e47b6f9c283
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 10%

---

# Für Verarbeitungsregeln verfügbare Dimensionen und Metriken

Die verfügbaren Dimensionen und Metriken, die Sie mithilfe von Verarbeitungsregeln lesen und schreiben können.

## Benutzerdefinierte Werte und Kontextdaten

| Wert | Lese-/Schreibstatus | Beschreibung |
| --- | --- | --- |
| **Benutzerdefinierter Wert** | Schreibgeschützt | Benutzerdefinierter Text oder Werte, die direkt in die Aktion einer Verarbeitungsregel eingegeben werden. |
| **Verketteter Wert** | Schreibgeschützt | Werte, die durch Kombinieren zweier Werte erstellt werden. Beispielsweise können Kanal und Seitenname kombiniert werden, um eine Unterkategorie zu erstellen. |

## Treffer-Attribute

| Attribut | Lese-/Schreibstatus | Beschreibung |
| --- | --- | --- |
| **Seiten-URL** | Lesen + Schreiben | Die Dimension [Seiten](/help/components/dimensions/page-url.md)URL. Linktracking-Treffer entfernen diese Dimension, bevor Verarbeitungsregeln erreicht werden. Wenn Sie einen Seiten-URL-Wert mithilfe von Verarbeitungsregeln erneut einfügen, wird der Treffer als [Seitenansicht](/help/components/metrics/page-views.md) anstatt als [Seitenereignis](/help/components/metrics/page-events.md) betrachtet. Adobe empfiehlt, in der Seitendimension nach einem Wert zu suchen, bevor Sie ihn ändern. |
| **Seitenname** | Lesen + Schreiben | Die Dimension [Seite](/help/components/dimensions/page.md) . Linktracking-Treffer entfernen diese Dimension, bevor Verarbeitungsregeln erreicht werden. Wenn Sie einen Seitenwert mithilfe von Verarbeitungsregeln erneut einfügen, wird der Treffer als [Seitenansicht“ ](/help/components/metrics/page-views.md) als [Seitenereignis](/help/components/metrics/page-events.md) betrachtet. Adobe empfiehlt, in der Seitendimension nach einem Wert zu suchen, bevor Sie ihn ändern. |
| **Report Suite-ID** | Schreibgeschützt | Die Report Suite, für die die Verarbeitungsregel ausgeführt wird. Diese Report Suite kann sich von der ursprünglich über AppMeasurement gesendeten Report Suite unterscheiden, z. B. bei Verwendung von VISTA-Regeln. |
| **AppMeasurement-Code-Version** | Schreibgeschützt | Die AppMeasurement-Bibliotheksversion, die zum Generieren der Bildanforderung verwendet wird. |
| **IP-Adresse** | Schreibgeschützt | Die IP-Adresse des Besuchers. |
| **Benutzeragent** | Schreibgeschützt | Der Benutzeragent des Besuchers. |
| **Referrer** | Schreibgeschützt | Die Dimension [Referrer](/help/components/dimensions/referrer.md). |
| **Parameter der Abfragezeichenfolge** | Schreibgeschützt | Der Wert eines angegebenen Abfragezeichenfolgenparameters in der aktuellen URL. |
| **Verweisender Abfragezeichenfolgen-Parameter** | Schreibgeschützt | Der Wert eines angegebenen Abfragezeichenfolgenparameters in der verweisenden URL oder eine leere Zeichenfolge, wenn keine vorhanden ist. |
| **Referrer-Domäne** | Schreibgeschützt | Die Seiten-Domain der verweisenden URL, einschließlich Subdomains. |
| **Verweisende Stammdomäne** | Schreibgeschützt | Die Seiten-Domain der verweisenden URL, ohne Subdomains. |
| **Seiten-Abfragezeichenfolge** | Schreibgeschützt | Alle Abfragezeichenfolgenparameter und deren Werte in der aktuellen URL. |
| **Verweisende Abfragezeichenfolge** | Schreibgeschützt | Alle Abfragezeichenfolgenparameter und deren Werte in der verweisenden URL. |
| **Seitenpfad** | Schreibgeschützt | Der Seitenpfad der aktuellen URL. Der Seitenpfad umfasst keine Protokoll-, Domain- oder Abfragezeichenfolgenparameter. |
| **Seiten-Domain** | Schreibgeschützt | Die Seiten-Domain der aktuellen URL, einschließlich Subdomains. Die Seiten-Domain enthält keine Seitenpfad- oder Abfragezeichenfolgenparameter. |
| **Seitenstamm-Domain** | Schreibgeschützt | Die Seiten-Domain der aktuellen URL, ohne Subdomains. |
| **Kundenperspektive** | Lesen + Schreiben | Eine Markierung, die bestimmt, ob der Treffer ein mobiler Hintergrundtreffer ist. |

## Konversionsvariablen

| Variable | Lese-/Schreibstatus | Beschreibung |
| --- | --- | --- |
| **eVar 1-250** | Lesen + Schreiben | [eVar](/help/components/dimensions/evar.md)-Dimensionen. |
| **Kampagne** | Lesen + Schreiben | Die Dimension [Trackingcode](/help/components/dimensions/tracking-code.md) . |
| **Kauf-ID** | Lesen + Schreiben | Die [`purchaseID`](/help/implement/vars/page-vars/purchaseid.md) Implementierungsvariable. |
| **Bundesland** | Lesen + Schreiben | (Retired) Die [`state`](/help/implement/vars/page-vars/state.md) Implementierungsvariable. |
| **Zip** | Lesen + Schreiben | Die Dimension [Postleitzahl](/help/components/dimensions/zip-code.md) . |
| **Währungscode** | Lesen + Schreiben | Die [`currencyCode`](/help/implement/vars/config-vars/currencycode.md) Implementierungsvariable. WICHTIG: Wenn Sie diese Variable auf einen ungültigen Wert setzen, wird der Treffer verworfen. |
| **Transaktions-ID** | Lesen + Schreiben | Die [`transactionID`](/help/import/data-sources/transactionid.md) Implementierungsvariable. |

>[!NOTE]
>Adobe unterstützt nicht das Festlegen der [`products`](/help/implement/vars/page-vars/products.md) Implementierungsvariable mithilfe von Verarbeitungsregeln.

## Traffic-Variablen

| Variable | Lese-/Schreibstatus | Beschreibung |
| --- | --- | --- |
| **prop 1-75** | Lesen + Schreiben | [Prop](/help/components/dimensions/prop.md)-Dimensionen. |
| **Hierarchie 1-5** | Lesen + Schreiben | (Eingestellt) [Hierarchie](/help/components/dimensions/hierarchy.md) Dimensionen. |
| **Server** | Lesen + Schreiben | Die Dimension [Server](/help/components/dimensions/server.md). |
| **Kanal** | Lesen + Schreiben | Die Dimension [Site](/help/components/dimensions/site-section.md) . |

## Kontextvariablen

Alle [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md), die diese Report Suite in den letzten 30 Tagen gesehen hat. Anwendungsbeispiele [ Sie unter Anwendungsfälle ](pr-use-cases.md) Verarbeitungsregeln .

>[!IMPORTANT]
>
>Wenn Verarbeitungsregeln eine bestimmte Kontextdatenvariable keiner anderen Variablen zuordnen (z. B. einer Prop oder eVar), geht der Wert in der Kontextdatenvariablen dauerhaft verloren.

## Erfolgsereignisse

Verarbeitungsregeln können Ereignisse festlegen, sie jedoch nicht als Bedingungen lesen. Legen Sie die Dropdown-Liste für die Regelaktion auf **[!UICONTROL Ereignis festlegen]** fest, um verfügbare Metriken anzuzeigen, deren Wert erhöht werden soll.

| Variable | Lese-/Schreibstatus | Beschreibung |
| --- | --- | --- |
| **Bestellungen** | Nur schreiben | Die [Bestellungen](/help/components/metrics/orders.md). |
| **Warenkorb** | Nur schreiben | Die Metrik [Warenkörbe](/help/components/metrics/carts.md). |
| **Warenkorbansicht** | Nur schreiben | Die [Warenkorbansichten](/help/components/metrics/cart-views.md) Metrik. |
| **Checkouts** | Nur schreiben | Die [Checkouts](/help/components/metrics/checkouts.md). |
| **Zusatz zum Warenkorb** | Nur schreiben | Die Metrik [Warenkorbhinzufügungen](/help/components/metrics/cart-additions.md). |
| **Entnahme aus Warenkorb** | Nur schreiben | Die Metrik [Warenkorbentnahmen](/help/components/metrics/cart-removals.md). |
| **Ereignis 1-1000** | Nur schreiben | [Benutzerspezifische Ereignisse](/help/components/metrics/custom-events.md). |
| **Produktansichten** | Nur schreiben | Die Metrik [Produktansichten](/help/components/metrics/product-views.md) . |
