---
title: Verarbeitungsreihenfolge für Daten in Adobe Analytics
description: Erfahren Sie mehr zur Reihenfolge der Komponenten und Services, die Daten in Adobe Analytics verarbeiten.
exl-id: a8dc9c12-07d3-4dc8-b2df-136f7a7a1e77
feature: Data Configuration and Collection
source-git-commit: 6c947812d4fd8bc2ee951a5933c6e3b6d8ca1a6b
workflow-type: tm+mt
source-wordcount: '1040'
ht-degree: 35%

---

# Verarbeitungsreihenfolge für Daten in Adobe Analytics

Adobe bietet viele Möglichkeiten, Daten zu verändern oder zu bearbeiten, bevor sie in Berichten angezeigt werden. Auf dieser Seite wird die Reihenfolge angezeigt, in der verschiedene Funktionen von Adobe Analytics Daten verarbeiten. Sie können diese Liste verwenden, um Dateninkonsistenzen zu beheben oder die beste Funktion zu bestimmen, die bei notwendigen Datenanpassungen verwendet werden sollte.

![Bild der Verarbeitungsreihenfolge](assets/processing-order.png)

## Daten vor ihrem Senden an Adobe

Bevor Daten an Adobe gesendet werden, werden sie normalerweise Client-seitig mit einer der folgenden Methoden kompiliert:

* **AppMeasurement**: Eine auf Ihrer Site gehostete und auf jeder Seite referenzierte JavaScript-Datei. Daten werden direkt an Adobe Analytics gesendet.
* **Adobe Experience Platform Web SDK**: Eine auf Ihrer Site gehostete und auf jeder Seite referenzierte JavaScript-Datei. Daten werden an die Adobe Experience Platform Edge Network gesendet.
* **Tags in der Adobe Experience Platform-Datenerfassung**: Eine auf jeder Seite referenzierte JavaScript-Datei mit Regeln, die in der Datenerfassungs-Benutzeroberfläche erstellt wurden. Die Adobe Analytics-Erweiterung bietet eine einfachere Möglichkeit der Implementierung von AppMeasurement. Die Web SDK-Erweiterung bietet eine einfachere Möglichkeit, das Web SDK zu implementieren.
* **API**: Sowohl AppMeasurement als auch Edge Network bieten programmgesteuerte Methoden zum Senden von Daten an Adobe. AppMeasurement bietet die [Dateneinfüge-](https://developer.adobe.com/analytics-apis/docs/1.4/guides/data-insertion/)) und die [Bulk-Dateneinfüge-](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/)); Edge Network bietet die [Datenerfassungs-API](https://developer.adobe.com/data-collection-apis/docs/).

Wenn Sie Daten an Edge Network senden, können Sie diese so konfigurieren, dass Daten an Adobe Analytics (sowie an viele andere Adobe Experience Cloud-Lösungen) weitergeleitet werden. Unabhängig von der Implementierungsmethode gelangen die erfassten Trefferdaten schließlich in einem Format an die Adobe Analytics-Verarbeitungs-Server, das sie analysieren können.

## Vorab-Bearbeitung in der Adobe Analytics-Sammlung

Wenn Daten in Adobe Analytics eingehen, treten sie in eine Vorverarbeitungsphase ein:

1. [**Dynamische Variablen**](/help/implement/vars/page-vars/dynamic-variables.md): Wenn eine dynamische Variable in einem beliebigen Teil einer Bildanforderung angezeigt wird, wird der Wert kopiert und ab dann als unabhängiger Wert gehandhabt.
1. [**IP-Verschleierung (letztes Oktett)**](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md): Wenn Ihre Report Suite so konfiguriert ist, dass nur das letzte Oktett verschleiert wird, gilt diese Verschleierung hier. Beachten Sie, dass die IP-Verschleierung (IP entfernen) später in der Verarbeitungs-Pipeline auftritt.
1. **Suchtabellen**: Dimensionen, die auf Adobe-internen Suchtabellen basieren (z. B. die Dimension [Browser](/help/components/dimensions/browser.md)) werden dem entsprechenden Wert zugeordnet.
1. [**IP-Ausschluss**](/help/admin/tools/exclude-ip.md): Alle IP-Adressen, die Sie explizit aus dem Reporting ausschließen, werden in diesem Schritt gekennzeichnet.
1. [**Bot-Regeln**](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md): Verwenden Sie standardmäßige oder benutzerdefinierte Bot-Filter, um diese Daten aus dem Reporting auszuschließen.
1. **Geolokalisierungsdaten**: Dimensionen, die auf der Suche nach IP-Adressen basieren (z. B. die Dimension [Land](/help/components/dimensions/countries.md)), werden befüllt.
1. [**Verarbeitungsregeln**](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md): Benutzerdefinierte Regeln, die von Ihrer Organisation auf Ihre Daten angewendet werden. Umfasst die Zuordnung von [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md) zu den jeweiligen Analytics-Variablen.
1. [**VISTA-Regeln**](vista.md): Benutzerdefinierte flexible Regeln, die von einer Person des Adobe-Berater-Teams auf Ihre Daten angewendet werden. VISTA-Regeln können je nach den Anforderungen Ihres Unternehmens vor oder nach den Verarbeitungsregeln ausgeführt werden. VISTA-Regeln werden meist nach den Verarbeitungsregeln ausgeführt, aber jede Organisation ist anders eingerichtet. Wenden Sie sich an Ihr Adobe Account Team , um weitere Informationen zu bestehenden VISTA-Regeln zu erhalten.
1. **Währungsumrechnung**: Wenn der Treffer eine andere [`currencyCode`](/help/implement/vars/config-vars/currencycode.md) als die Report Suite-Währung enthält, werden alle anwendbaren Währungsvariablen mithilfe des Wechselkurses des aktuellen Tages umgerechnet.
1. [**Postleitzahl**](/help/components/dimensions/zip-code.md): Die Dimension „Postleitzahl“ wird basierend auf den Report Suite-Einstellungen ausgefüllt.

## Schritt „Mittelwert“ der Datenerfassungs-Pipeline

Wenn die Vorverarbeitung abgeschlossen ist, verwenden mehrere Funktionen diese teilweise verarbeitete Form von Daten, die als „Mittelwerte“ bezeichnet wird. Bevor diese Daten an eine beliebige Stelle gesendet werden, wird eine für den mittleren Wert spezifische Verarbeitung angewendet:

1. [**Verarbeitungsregeln für Marketing-Kanäle auf Trefferebene**](/help/admin/tools/manage-rs/edit-settings/marketing-channels/mc-proc-rules.md): Diese Verarbeitungsregeln werden speziell für den Analytics Source Connector ausgeführt. Da es noch keinen Kontext auf Besuchs- oder Besucherebene gibt, gehen diese Verarbeitungsregeln davon aus, dass ein Treffer nicht der erste Treffer eines Besuchs ist. Die Ergebnisse der Ausführung der Verarbeitungsregeln für einen Treffer sind in `channel.typeAtSource` und `channel._id` verfügbar.
1. [**IP-Verschleierung (IP entfernen)**](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md): Wenn Ihre Report Suite so konfiguriert ist, dass eine IP-Adresse vollständig verschleiert wird, gilt diese Verschleierung hier (nur für Mittelwerte).

Zu diesem Zeitpunkt werden Mittelwertdaten an die entsprechende Funktion gesendet:

* [**Livestream-API**](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/livestream/): Verbinden Sie eine Anwendung mit dem Livestream-Service von Adobe, um einen Datenfluss zum Zeitpunkt der Erfassung zu erhalten.
* [**Analytics Source Connector**](https://experienceleague.adobe.com/de/docs/experience-platform/sources/connectors/adobe-applications/analytics): Aufnehmen von Adobe Analytics Report Suite-Daten in einen Adobe Experience Platform-Datensatz.
* [**Echtzeit-Reporting**](/help/components/c-real-time-reporting/realtime.md): Bietet bis zu drei konfigurierbare Echtzeit-Berichte in Analysis Workspace.

## Verarbeitung auf Besuchs- und Besucherebene

Bis zu diesem Zeitpunkt hat ein bestimmter Treffer keine Kenntnis oder keinen Kontext von Treffern, die vor oder nach ihm erfasst wurden. In diesem Verarbeitungsschritt werden Felder auf Besuchs- und Besucherebene ausgefüllt.

1. [**Besuch + Besucherdefinition**](/help/implement/id/overview.md): Der Treffer wird anhand der enthaltenen Besuchervariablen identifiziert.
1. [**Besuchsnummer**](/help/components/dimensions/visit-number.md): Basierend auf anderen Besuchen für den identifizierten Besucher wird die Besuchsnummer berechnet.
1. **Ereignisdeduplizierung**: Wenn der Treffer eine doppelte [`purchaseID`](/help/implement/vars/page-vars/purchaseid.md) oder [Ereignis-Serialisierung](/help/implement/vars/page-vars/events/event-serialization.md) enthält, werden diese IDs überprüft bzw. gekennzeichnet.
1. [**Verarbeitungsregeln für Marketing-Kanäle auf Besuchsebene**](/help/admin/tools/manage-rs/edit-settings/marketing-channels/mc-proc-rules.md): Jeder Treffer wird durch Verarbeitungsregeln für Marketing-Kanäle ausgeführt, und die Details für Kanal und Kanal werden bestimmt, wenn der Treffer mit einer Regel übereinstimmt. Mit diesen Regeln werden die Dimensionen [Marketing-](/help/components/dimensions/marketing-channel.md)) und [Marketing-Kanal-Details](/help/components/dimensions/marketing-detail.md) ausgefüllt, die in Analysis Workspace verfügbar sind.
1. **Variablenpersistenz**: Für Dimensionen mit Persistenz (z. B[ eVars](/help/components/dimensions/evar.md)) wird dieser Wert in diesem Schritt bestimmt. Im Allgemeinen werden hier die meisten `post` festgelegt.
1. **Transaktions-**: Wenn der Treffer einen neuen [`transactionID`](/help/implement/vars/page-vars/transactionid.md) enthält, wird eine „Momentaufnahme“ aller unterstützten Werte gespeichert. Wenn ein Datenquellen-Upload eine übereinstimmende Transaktions-ID enthält, sind alle unterstützten Werte aus diesem Snapshot in dieser Datenquellenzeile enthalten.
1. [**IP-Verschleierung (IP entfernen)**](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md): Wenn Ihre Report Suite so konfiguriert ist, dass eine IP-Adresse vollständig verschleiert wird, wird diese Verschleierung hier angewendet, nachdem alle anderen Verarbeitungsschritte abgeschlossen sind.

Zu diesem Zeitpunkt wird der einzelne Treffer in den Report Suite-Datentabellen aufgezeichnet. Nach der standardmäßigen [Latenzzeit](latency.md) ist er in Berichten verfügbar.

## Ändern von Daten nach ihrer Verarbeitung

Die Daten in Adobe Analytics sind größtenteils unveränderlich. Es gibt jedoch einige Funktionen, die eine selektive Datenanpassung oder -löschung ermöglichen:

* [**Datenreparatur-API**](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/data-repair/): Bearbeiten Sie bestimmte Spalten oder löschen Sie die gewünschten Datenzeilen.
* [**Data Governance**](/help/technotes/privacy/privacy-overview.md): Erfüllen Sie Datenschutzanfragen, um Daten dauerhaft zu löschen.
* [**Klassifizierungen**](/help/components/classifications/classifications-overview.md): Erstellen Sie Dimensionen anhand von Regeln oder hochgeladenen Daten, um eine unterschiedliche Organisation der Daten zu ermöglichen. Die zugrunde liegenden Report Suite-Daten werden nicht geändert, sodass Sie Klassifizierungsdaten frei bearbeiten oder überschreiben können.
* [**Virtual Report Suites**](/help/components/vrs/vrs-about.md): Erstellen Sie eine alternative Report Suite-Ansicht, durch die die maximale Wartezeit bei einem Besuch geändert werden kann.
