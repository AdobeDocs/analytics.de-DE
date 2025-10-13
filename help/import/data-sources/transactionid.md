---
title: Transaktions-ID-Datenquellen
description: Verwenden Sie gespeicherte Werte aus einem Online-Treffer, um Offline-Treffer anzureichern, die eine Transaktions-ID gemeinsam haben.
feature: Data Sources
exl-id: 5f26b15c-8d9c-46d5-860f-13fdfa21af2e
role: Admin
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 8%

---

# Transaktions-ID-Datenquellen

Transaktions-ID-Datenquellen sind eine Variante von Zusammenfassungsdatenquellen, mit denen Sie aus einem Online-Treffer gespeicherte Werte auf Offline-Zeilen anwenden können, die dieselbe Transaktions-ID aufweisen. Dieser Ansatz ist nützlich, wenn Sie eine Transaktion online erfassen, aber Details später von einem anderen System erhalten. Primäre Beispiele sind Produktrücksendungen, Buchungsstornierungen oder Ergebnisse aus Callcenter-Interaktionen.

>[!NOTE]
>
>Bevor Sie Transaktions-ID-Datenquellen verwenden können, müssen Sie sie zunächst in [Allgemeine Kontoeinstellungen](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md) für die gewünschte Report Suite aktivieren.

## Funktionsweise

Das Konzept der Transaktions-IDs besteht aus zwei Teilen:

* **Online-Treffer**: Jeder vollständige Analytics-Treffer, der an eine Report Suite (AppMeasurement, Web SDK, API usw.) gesendet wird. Für diesen Treffer legen Sie die [`transactionID`](/help/implement/vars/page-vars/transactionid.md) Implementierungsvariable fest.
* **Offline-Treffer**: Eine Zeile, die über Datenquellen hochgeladen wurde. Fügen Sie in die Datei die Spalte `transactionID` mit einem Wert ein, der einem Online-Treffer entspricht.

Wenn Sie einen Online-Treffer senden, der die `transactionID` Implementierungsvariable enthält, erstellt Adobe eine „Momentaufnahme“ der folgenden Dimensionen, die zu diesem Zeitpunkt festgelegt oder beibehalten wurden:

* [Kategorie](/help/components/dimensions/category.md)
* [Tage bis Erstkauf](/help/components/dimensions/days-before-first-purchase.md)
* [Tage seit letztem Kauf](/help/components/dimensions/days-since-last-purchase.md)
* [eVars 1-250](/help/components/dimensions/evar.md)
* Funktionsspezifische Dimensionen, die in den [Report Suite-Einstellungen) aktiviert sind &#x200B;](/help/admin/tools/manage-rs/report-suites-admin.md) sich ähnlich wie eVars verhalten. Elementspezifische Dimensionen, die sich ähnlich wie Props verhalten, sind nicht enthalten.
* [Listenvariablen](/help/implement/vars/page-vars/list.md)
* [Marketing-Kanal](/help/components/dimensions/marketing-channel.md)
* [Details zum Marketing-Kanal](/help/components/dimensions/marketing-detail.md)
* [Mobilgerätedimensionen](/help/components/dimensions/mobile-dimensions.md)
* [Ursprüngliche Referrer-Domain](/help/components/dimensions/original-referring-domain.md)
* [Produkt](/help/components/dimensions/product.md)
* [Referrer-Domain](/help/components/dimensions/referring-domain.md)
* [Suchmaschine](/help/components/dimensions/search-engine.md)
* [Suchbegriff](/help/components/dimensions/search-keyword.md)
* [Trackingcode](/help/components/dimensions/tracking-code.md)
* [Besuchsnummer](/help/components/dimensions/visit-number.md)

>[!NOTE]
>
>Metriken (wie [Bestellungen](/help/components/metrics/orders.md) oder [Benutzerspezifische Ereignisse](/help/components/metrics/custom-events.md) sind nicht im „Snapshot“ enthalten.

Wenn Sie einen Offline-Treffer über Datenquellen hochladen, der eine übereinstimmende Transaktions-ID enthält, werden alle verfügbaren Dimensionen innerhalb der „Momentaufnahme“ automatisch an die Datenquellenzeile angehängt. Wenn eine bestimmte Dimension sowohl im Online- als auch im Offline-Treffer vorhanden ist, wird der Offline-Trefferwert verwendet.

>[!IMPORTANT]
>
>Das Konzept der Transaktions-ID-Datenquellen hilft nur beim Ausfüllen von Datenquellenzeilen (Offline-Treffer). Sie wirken sich nicht auf den Online-Treffer aus bzw. ändern ihn nicht.

## Überlegungen zur Transaktions-ID-Datenquelle

Transaktions-ID-Datenquellen haben die folgenden Eigenschaften:

* Die Online-Daten müssen zuerst erfasst und verarbeitet werden. Wenn eine Transaktions-ID-Datenquelle hochgeladen wird, bevor eine Report Suite einen Treffer verarbeitet, der mit dieser Transaktions-ID übereinstimmt, werden die Daten wie eine zusammenfassende Datenquelle behandelt.
* Transaktions-IDs, die aus Online-Treffern erfasst wurden, laufen nach 25 Monaten ab.
* Datenquellen, die mit einer abgelaufenen Transaktions-ID hochgeladen wurden, werden ähnlich wie Daten behandelt, die ohne Transaktions-ID hochgeladen wurden.
* Wenn Sie dieselbe Transaktions-ID für mehrere Online-Treffer festlegen, wird nur der „Schnappschuss“ des ersten Vorkommens verwendet. Nachfolgende doppelte Transaktions-ID-Online-Treffer werden so verarbeitet, als hätten sie keine Transaktions-ID.
* Nachdem Sie einen bestimmten `transactionID` ausgefüllt haben, wird der zugehörige „Schnappschuss“ als unveränderlich betrachtet, bis diese Transaktions-ID abläuft.
* Wenn Sie dieselbe Transaktions-ID in mehreren Datenquellenzeilen festlegen, werden alle verfügbaren Dimensionen aus dem Online-Treffer an jeden Offline-Treffer angehängt. Offline-Treffer für dieselbe Transaktions-ID wissen nichts voneinander. Daten werden nicht zwischen Offline-Treffern weitergeleitet.
