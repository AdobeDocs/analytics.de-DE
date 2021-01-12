---
description: Diese Adobe® Data Connectors™-E-Mail-Integration kombiniert Verhaltensdaten aus Analytics® mit Delivra-E-Mail-Marketing zum Schaffen eines leistungsfähigen Tools, um die Erfolgsmessung neu zu definieren und Zielgruppen mit relevanterem Messaging anzusprechen.
title: Delivra-Data Connector für Adobe Analytics
uuid: 9d56d39c-98e6-4e9b-b00d-515df02ea879
translation-type: tm+mt
source-git-commit: 3850dc3503ca57ba4f13f0de63e8420e484db501
workflow-type: tm+mt
source-wordcount: '982'
ht-degree: 98%

---


# Delivra-Data Connector für Adobe Analytics {#delivra-data-connector-for-adobe-analytics}

>[!IMPORTANT]
>
>Am 1. August 2021 werden wir die Adobe Data Connector-Technologie beenden. [Weitere Informationen ...](/help/import/data-connectors/data-connectors-eol.md)

Diese Adobe® Data Connectors™-E-Mail-Integration kombiniert Verhaltensdaten aus Analytics® mit Delivra-E-Mail-Marketing zum Schaffen eines leistungsfähigen Tools, um die Erfolgsmessung neu zu definieren und Zielgruppen mit relevanterem Messaging anzusprechen.

Die Bereitstellung relevanter E-Mail-Nachrichten für diese Marktsegmente kann zu völlig neuen Umsatzmöglichkeiten führen, wodurch die Konvertierung und der Umsatz neuer und vorhandener E-Mail-Kampagnen gesteigert werden. So hat zum Beispiel die Bereitstellung relevanter E-Mail-Nachrichten auf Grundlage von Produkten, die während eines Besuchs angesehen wurden, oder von Produkten, die in einem Warenkorb zurückgelassen wurden, nachweislich erhebliche Auswirkungen auf den Umsatz bei minimalen Auswirkungen auf die Kosten, weil dadurch lediglich die Daten Ihrer Websitebenutzer genutzt werden. Diese Steigerung der Marketingeffizienz ist einer der wichtigsten Vorteile der Integration von Analytics in Delivra. Darüber hinaus synchronisiert diese Integration E-Mail-Metriken automatisch mit Analytics-Daten stündlich für Closed-Loop-Berichte.

## Wesentliche Vorteile {#key-benefits}

Diese Integration umfasst die folgenden Hauptvorteile:

* Zusammenfassen von E-Mail-Marketing- und Analysedaten auf einer Berichtsoberfläche.
* Optimieren von E-Mail-Kampagnen nach Konversion und Beitrag zum Umsatz und zum Site-Erfolg.
* Auf dynamischen Marketingsegmenten basierendes Remarketing für wichtige Besucher und Marktsegmente.
* Synchronisation von E-Mail-Metriken nahezu in Echtzeit verglichen mit der einmal täglich durchgeführten Synchronisation

## Dynamische Marketingsegmente {#dynamic-marketing-segments}

Diese Data Connectors-E-Mail-Integration unterstützt dynamische Marketingsegmente, die Sie bei der Förderung Ihres Unternehmens unterstützen.

Diese Integration umfasst standardmäßig die folgenden Marketingsegmente:

* **Profile für Kauf**: Erhöhen Sie Nachbestellungen und den durchschnittlichen Bestellwert durch Kampagnen, die auf das Kaufverhalten der Besucher ausgerichtet sind.
* **Profil für das Verhalten der Produkt-/Inhaltsansicht**: Erreichen Sie potenzielle Kunden durch Marketingsegmente, die auf Produktansichten und Inhaltszugriffsprofilen basieren.
* **Profil für Warenkorbabbruch:** Mit auf sie speziell abgestimmten Kampagnen können Sie Besucher, die zögern, ihren Einkaufswagen abzuschließen, in Kunden umwandeln.
* Kunden können auch benutzerspezifische Remarketing-Segmente erstellen und planen, die speziell auf die Bedürfnisse ihrer Benutzer abgestimmt sind.

## Integrationsverfahren und -voraussetzungen {#integration-procedure-and-prerequisites}

Mit einem „Plug&amp;Play“-Assistenten nehmen Sie eine schrittweise Systemsynchronisation und Initialisierung der Integration vor.

Diese Data Connectors-Integration erfordert Folgendes:

### Adobe-Voraussetzungen {#section-bce14015fb7f41b3bc754da0eb7567bc}

* Adobe Data Warehouse
* Adobe Analytics-Konto.
* Verfügbare und konfigurierte Analytics-Variablen, darunter eVars und benutzerspezifische Ereignisse.

### Delivra-Voraussetzungen {#section-bcb904574ccf42308bcf7a15e45b4d58}

* Ein aktives Delivra-Konto auf Professional-Ebene (oder höher) mit aktivierter Option „Adobe Integration“.

## Preise {#pricing}

Diese Data Connectors-Integration umfasst Hinweise zu Preisen, die Ihnen bekannt sein müssen.

Weitere Informationen dazu finden Sie in den folgenden Abschnitten:

### Hinweise zu Adobe-Preisen {#section-2d1c79c895a5479bad8fdd97961ba6a3}

Diese Integration kann mit wiederkehrenden und Implementierungsgebühren verbunden sein. Details zu den Preisen erhalten Sie von Ihrem Adobe-Kundenbetreuer.

### Hinweise zu Delivra-Preisen {#section-c6afad08c34b43e3a7a3637eea3328c3}

Diese Integration kann mit Gebühren verbunden sein.

* Informationen zu den Preisen erhalten Sie von Ihrem Delivra-Kundenbetreuer.

## Wissenswertes vor der Aktivierung dieser Integration {#what-you-should-know-before-activating-this-integration}

Bevor Sie diese Integration aktivieren, überprüfen Sie die folgenden Elemente anhand Ihrer Implementierungen von Adobe Analytics® und Ihrer E-Mail-Software.

So wird sichergestellt, dass vor der Aktivierung die entsprechenden Best Practices oder Voraussetzungen vorhanden sind, was zu einer optimalen und erfolgreichen Integration führt.

### Adobe Analytics {#adobe-analytics}

Überprüfen Sie die folgenden Informationen zu dieser Data Connectors-Integration in Bezug auf Adobe Analytics:

* **Report Suite-spezifisch**: Beachten Sie, dass diese Integration Report Suite-spezifisch ist. Stellen Sie sicher, dass Sie die gewünschte Report Suite ausgewählt haben, bevor Sie die Integration aktivieren.
* **Beauftragter Vertreter**: Achten Sie darauf, dass Ihrer Firma aufgrund der Aktivierung dieser Integration möglicherweise Gebühren gemäß Ihrer Servicevereinbarung mit Adobe, Inc. oder Ihrer Servicevereinbarung mit einem der vertrauenswürdigen Partner von Adobe entstehen. Durch Aktivierung dieser Integration bestätigen Sie hiermit, dass Sie ein beauftragter Vertreter Ihrer Firma sind. Dergestalt ist Ihre Firma bereit, die in der oben beschriebenen Servicevereinbarung ggf. festgelegten Gebühren zu zahlen.
* **Data Warehouse™:** Für diese Integration muss Data Warehouse aktiviert sein, damit Remarketing-Segmente generiert werden können. Wenn Sie Data Warehouse nicht aktiviert haben, wenden Sie sich für weitere Informationen an Adobe.
* **Empfänger-ID:** Für die Integration muss eine „Besucher-ID“ in einer Analytics-Variablen (eVar) erfasst und gespeichert werden. Die Besucher-ID (häufig als „Empfänger-ID“ bezeichnet) ist eine kodierte oder numerische Darstellung einer E-Mail-Adresse aus dem Delivra-System. Diese „Empfänger-ID“ ist mit dem nachgelagerten Besucherverhalten auf der Site (Warenkorbabbrüche, Käufe usw.) verknüpft, wird in das Delivra-System übertragen und kann für Remarketing-Zecke genutzt werden. Während des Einrichtungsvorgangs müssen Sie eine eVar für diesen Zweck identifizieren, wenn Sie vom Assistenten dazu aufgefordert werden.
* **Externes Tracking**: Zum Gewährleisten einer erfolgreichen Integration sollten Sie die Best Practice zur Aktivierung des externen Trackings für jede gesendete E-Mail-Kampagne befolgen. Weitere Informationen finden Sie unten im Abschnitt „Delivra“.
* **Datenschutz-Compliance**: Sie sollten sich darüber im Klaren sein, dass durch die Aktivierung des Empfänger- oder Besucher-ID-Trackings diese Funktion persönliche Informationen Ihrer Site-Besucher verfolgen kann. Dies wirkt sich auf den Datenschutz aus, sodass Ihre Organisation entsprechende Verfahren implementieren muss, z. B. die Benachrichtigung und Zustimmung Ihrer Site-Besucher.

### Adobe Data Connectors-Integration für Delivra {#delivra-for-adobe-data-connectors-integration}

Überprüfen Sie die folgenden Informationen zu dieser Data Connectors-Integration in Bezug auf Delivra:

* **Gültiges Delivra-Konto:** Um die Data Connectors-E-Mail-Integration verwenden zu können, muss ein Client über ein gültiges Delivra-Konto verfügen.
* **Aktueller Kunde von Delivra:** Für diese Integration müssen Sie Adobe- und Delivra-Kunde sein. Wenn Sie noch kein Kunde von Delivra sind, verfügen Sie nicht über die zum Abschluss des Integrationsassistenten erforderlichen Informationen. Wenn Sie derzeit Delivra-Kunde sind, benötigen Sie Ihre Delivra-Konto-ID oder den Ihrer Organisation zugewiesenen Listennamen, um den Integrationsassistenten abzuschließen. Sie müssen Delivra den Firmennamen und die mit der Integration verknüpfte Konto-ID mitteilen, um Ihre Einrichtung abzuschließen.
