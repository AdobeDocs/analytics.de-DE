---
title: Klassifizierungssätze – Überblick
description: Erfahren Sie, wie Sie Klassifizierungssätze zum Verwalten von Klassifizierungsdaten verwenden. Erfahren Sie, wie sich Klassifizierungssätze von veralteten Klassifizierungen unterscheiden.
exl-id: a139b298-1188-42ce-b52f-c71e0ff7c4e3
feature: Classifications
source-git-commit: 8a7dd06a26e6a4ad06c224543bc7fdda33ba7aaa
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Klassifizierungssätze – Überblick

Klassifizierungssätze bieten eine einzige Oberfläche zum Verwalten von Klassifizierungen und Regeln. Dieser Workflow kombiniert die Erstellung von Klassifizierungen in [Report Suite-Einstellungen](/help/admin/tools/manage-rs/report-suites-admin.md) mit dem [Classification Importer](/help/components/classifications/sets/manage-sets.md). Das Ergebnis ist eine einzige, intuitive Benutzeroberfläche zum Erstellen und Verwalten von Klassifizierungsdaten.


## Klassifizierungssätze im Vergleich zu veralteten Klassifizierungen

Der Hauptunterschied zwischen Klassifizierungssätzen und veralteten Klassifizierungen besteht darin, dass Klassifizierungssätze alle Funktionen in einer Benutzeroberfläche kombinieren, während veraltete Klassifizierungen auf drei Benutzeroberflächen angewiesen sind.

### Veraltete Klassifizierungen

![Veraltete Klassifizierung](/help/components/classifications/sets/assets/classifications-legacy.svg)

In veralteten Klassifizierungen verfügen ![Schemata](/help/assets/icons2/Schema.svg) für Klassifizierungen (z. B. für Traffic, Konversionen, Marketing-Kanäle usw.) jeweils über eine eigene Dimension (Schlüssel ![Schlüssel](/help/assets/icons2/Key.svg)). Diese Klassifizierungen werden als Teil Ihrer [Report Suite-Einstellungen](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/conversion-classifications.md) definiert.

Die Regeln ![BidRule](/help/assets/icons/BidRule.svg) werden separat in Regelsätzen als Teil der [Classification Rule Builder](/help/components/classifications/crb/classification-rule-builder.md)-Benutzeroberfläche definiert. In dieser Benutzeroberfläche wird ein Regelsatz einer oder mehreren Report Suites zugeordnet.

Mit dem [Classification Importer](/help/components/classifications/importer/c-working-with-saint.md) können Sie eine Vorlage ![DocumentFragment](/help/assets/icons/DocumentFragment.svg) herunterladen, Klassifizierungen ![UploadToCloud](/help/assets/icons/UploadToCloud.svg) in eine Kombination aus Report Suite und Schlüssel (Datensatz) importieren oder Klassifizierungen ![Download](/help/assets/icons/Download.svg) daraus exportieren.



### Klassifizierungssätze

![Klassifizierungssätze](./assets/classifications-sets.svg)

Klassifizierungssätze kombinieren alle veralteten Klassifizierungsschnittstellen in einer einzigen Oberfläche. Jeder Klassifizierungssatz definiert Folgendes:

* Ein oder mehrere Abonnements (die Kombination aus einer Report Suite ![Daten](/help/assets/icons2/Data.svg) und der Dimension ![Schlüssel](/help/assets/icons2/Key.svg) (Schlüssel)), die Sie klassifizieren möchten. Wenn Sie Produkte basierend auf einer Produkt-SKU klassifizieren möchten, können Sie alle Report Suites mit einer entsprechenden Produkt-SKU-Dimension definieren. Zudem müssen Sie Klassifizierungen nicht über Report Suites hinweg replizieren, wie es in der veralteten Benutzeroberfläche für Klassifizierungen der Fall war.
* Eine Liste der Klassifizierungen ![Schema](/help/assets/icons2/Schema.svg) (Schema) für den Schlüssel. Für Produktklassifizierungen können Sie beispielsweise Kategorie, Farbe, Größe, Geschlecht und mehr angeben. Sobald Sie Ihre Klassifizierungen definiert haben, können Sie eine Vorlage ![DocumentFragment](/help/assets/icons/DocumentFragment.svg) herunterladen, Klassifizierungsdaten ![UploadToCloud](/help/assets/icons/UploadToCloud.svg) hochladen, Klassifizierungsdaten ![Download](/help/assets/icons/Download.svg) herunterladen und mehr.
* Eine oder mehrere Regeln ![BidRule](/help/assets/icons/BidRule.svg), um die Klassifizierungen zu unterstützen.


Um über das Menü **[!UICONTROL Komponenten]** in der Adobe Analytics-Benutzeroberfläche auf **[!UICONTROL Klassifizierungssätze]** zuzugreifen, müssen Sie Produktadmin sein oder einem Produktprofil angehören, das das Berechtigungselement [!UICONTROL Report Suite-Tools] > [!UICONTROL Klassifizierungen] enthält. Beachten Sie, dass die veralteten Schnittstellen für die Klassifierungsverwaltung über das Menü **[!UICONTROL Admin]** verfügbar sind.

Klassifizierungssätze bestehen aus drei Funktionsbereichen:

* [**[!UICONTROL Klassifizierungssätze]**](manage-sets.md): Erstellen, bearbeiten und löschen Sie Klassifizierungssätze.
* [**[!UICONTROL Aufträge]**](job-manager.md): Zeigen Sie den Status der Aufträge für Klassifizierungssätze an.
* [**[!UICONTROL Konsolidierungen]**](consolidations/manage.md): Kombinieren Sie mehrere Klassifizierungssätze zu einem einzigen Klassifizierungssatz.


## Workflow

Der Workflow für Klassifizierungssätze umfasst normalerweise die folgenden Schritte:

1. Überlegen Sie, für welche Kombinationen aus Report Suite und Dimension Sie einen Klassifizierungssatz erstellen möchten. Ein Beispiel hierfür ist die Definition eines Produktklassifizierungssatzes, den Sie für jede Report Suite erstellen, für die Sie Produkte mit weiteren Details klassifizieren möchten. Dies können z. B. Details wie Kategorie und Farbe sein.
1. [Erstellen Sie einen Klassifizierungssatz](/help/components/classifications/sets/create-set.md) mit Abonnements für eine oder mehrere Kombinationen aus Report Suite und Schlüsseldimension, die Produkte identifizieren. Zum Beispiel:

   | Report Suite | Schlüsseldimension |
   |---|---|
   | Report Suite 1 | Produkt-ID |
   | Report Suite 2 | Produkt-SKU |

1. [Fügen Sie die Klassifizierungen hinzu](/help/components/classifications/sets/manage/schema.md#add), die Sie dem Klassifizierungssatz-Schema zugeordnet haben. Zum Beispiel:

   | Klassifizierungsname | Identitätsname |
   |---|---|
   | Kategorie | Kategorie |
   | Farbe | color |

1. Erstellen Sie manuell eine Datei, die Klassifizierungsdaten enthält. [Verwenden Sie eine Vorlage](/help/components/classifications/sets/manage/schema.md#template), um sicherzustellen, dass Sie das [unterstützte Dateiformat](data-files.md#classification-set-file-formats) und die Spalten für die Datei verwenden. Fügen Sie dann die Daten zur Vorlagendatei hinzu.

   Alternativ können Sie Daten in den [unterstützten Dateiformaten](data-files.md#classification-set-file-formats) direkt aus Ihrem Produktkatalog exportieren, wobei die Spalten der Vorlage entsprechen müssen. Beispielweise eine CSV-Datei wie:

   ```
   Key,Category,Color
   Adobe Nike Tech Fleece Full-Zip Hoodie - Men's,Men,Black
   Adobe Nike Tech Fleece Full-Zip Hoodie - Women's,Women,Black
   Men's North Face Adobe Jacket,Men,Black
   Nike Air Hybrid 2 Golf Bag,Equipment,Blue
   STITCH&reg; Ultimate Garment Bag,Equipment,Brown
   Adobe Analytics Training Tee - Navy,Men,Navy
   AirPods Pro 2,Electronics,White
   Adobe Analytics Training Tee - Green,Men,Green
   Women's North Face Adobe Jacket,Women,Blue
   Adobe Analytics Training Tee - Grey,Men,Gray
   Adobe Analytics One Million Views - Grey,Equipment,Grey
   Adobe and MGM Tee - White,Women,White
   Adobe and MGM Tee - Charcoal,Women,Charcoal
   ```

   In der Klassifizierungsdatendatei verweisen Sie unter Verwendung von `Key` auf die Schlüsseldimension für jede Report Suite (z. B. **[!UICONTROL Produkt-ID]** und **[!UICONTROL Produkt-SKU]**). Zudem verweisen Sie auf jede Klassifizierung unter Verwendung des **[!UICONTROL Klassifizierungsnamens]** (z. B. `Category` oder `Color`).

1. [Laden](/help/components/classifications/sets/manage/schema.md#upload) Sie die Datei, die die Klassifizierungsdaten enthält, in das Klassifizierungssatzschema hoch.

1. Legen Sie [Regeln](manage/rules.md) fest, um eingehende Daten und Daten aus der Vergangenheit automatisch zu klassifizieren.

1. [Automatisieren](/help/components/classifications/sets/manage/schema.md#automate) Sie den Aktualisierungsprozess Ihres Produktkatalogs, damit Aktualisierungen durch die Nutzung eines Cloud-Speicherorts in den Klassifizierungsdaten berücksichtigt werden.

1. [Laden](/help/components/classifications/sets/manage/schema.md#download) Sie Ihre Klassifizierungsdaten herunter, um den Inhalt zu validieren.

1. [Überprüfen Sie den Auftragsverlauf](/help/components/classifications/sets/job-manager.md), um die Ergebnisse Ihrer Aktionen (Hochladen, Herunterladen, Vorlage und mehr) für Klassifizierungen anzuzeigen.
1. Wenn Sie infolge einer Migration von der alten Klassifizierungsfunktionalität mehrere ähnliche Klassifizierungssätze haben, [konsolidieren](consolidations/manage.md) Sie diese Klassifizierungssätze.



## Verbesserungen

Die Backend-Architektur, die mit Klassifizierungssätzen veröffentlicht wurde, enthält einige wichtige Verbesserungen:

* Verkürzte Verarbeitungszeit (von 72 zurück auf 24 Stunden).
* Eine neu gestaltete Benutzeroberfläche zum Verwalten von Klassifizierungen.
* Die Option, Klassifizierungsdaten in Adobe Experience Platform über den [Adobe Analytics-Quell-Connector für Klassifizierungsdaten](https://experienceleague.adobe.com/de/docs/experience-platform/sources/connectors/adobe-applications/classifications) zu verwenden.

Die Backend-Architektur, die mit Klassifizierungssätzen veröffentlicht wurde, enthält auch einige wichtige Änderungen:

* Bei Verwendung des Browsers oder automatischen Imports ist **[!UICONTROL Bei Konflikt überschreiben]** immer aktiviert.
* Bei Verwendung des Browser- oder automatischen Imports wird die Option zum sofortigen Export nach dem Import nicht mehr unterstützt. Exporte müssen separat initiiert werden.
* Der Analytics 2.0-API-Endpunkt `GetDimensions` gibt jetzt Zeichenfolgenkennungen für Klassifizierungen anstelle numerischer Kennungen zurück. Numerische Kennungen können zwar weiterhin verwendet werden, es wird jedoch empfohlen, nach Möglichkeit die neuen Zeichenfolgenkennungen zu verwenden. Numerische Kennungen können mithilfe des Abfragezeichenfolgen-Parameters `?expansion=hidden` abgerufen werden.

>[!IMPORTANT]
>
>Die Leistung von Klassifizierungssätzen hängt hauptsächlich von der Anzahl der eindeutigen Schlüsselwerte ab, die Daten enthalten. Gehen Sie mit Sorgfalt vor, wenn Sie Variablen haben, die eine große Anzahl eindeutiger Werte enthalten. Dies gilt insbesondere dann, wenn Sie solche Variablen aus mehreren Report Suites und Dimensionen in einem einzigen Klassifizierungssatz kombinieren.

## Einschränkungen

* Klassifizierungssätze unterstützen noch keine Regeln. Die Regelfunktionalität wird zur Benutzeroberfläche für Klassifizierungssätze hinzugefügt, bevor die Funktionalität des alten [Regel-Builders](/help/components/classifications/crb/classification-rule-builder.md) nicht mehr verfügbar ist.
* Es erfolgt keine Migration von alten Klassifizierungsregeln und -konfigurationen zu Klassifizierungssätzen. Ein Migrationsdienstprogramm wird zur Schnittstelle für Klassifizierungssätze hinzugefügt, bevor die veraltete Klassifizierungsfunktion nicht mehr verfügbar ist.
