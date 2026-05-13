---
title: Übersetzungshandbuch für häufig verwendete Metriken anderer Plattformen
description: Erfahren Sie, wie Sie Metrikdaten für viele häufig verwendete Berichte abrufen können, indem Sie Terminologie verwenden, die Google Analytics-Anwendern besser bekannt ist.
feature: Third-party Integration
exl-id: e95b0530-8099-4a08-9e2b-75174546277d
TQID: https://experienceleague.adobe.com/0gpsqdwdU6kZjZGLy5YZ1h-b1C4lGUnEwOEKdzvjxyU
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2: id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b4dd41a7-ccf8-4e9d-918e-acaab534a307id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 507
ht-degree: 100%

---

# Übersetzungshandbuch für häufig verwendete Metriken anderer Plattformen

Auf anderen Plattformen wie Google Analytics verwenden viele Berichte eine Reihe gemeinsamer Metriken. Auf dieser Seite erfahren Sie, wie Sie die in vielen Berichten verwendeten Metriken nachbilden.

Um einer Freiformtabelle im Arbeitsbereich mehrere Metriken hinzuzufügen, ziehen Sie die Metrik aus dem Komponentenbereich neben der Metrikkopfzeile im Arbeitsbereich:

![Zusätzliche Metrik](/help/technotes/ga-to-aa/assets/new_metric.png)

## Akquise-Metriken

**Nutzer** ähnelt ungefähr **Unique Visitors** in Workspace. Weitere Informationen finden Sie im Abschnitt zur Dimension [Unique Visitors](/help/components/metrics/unique-visitors.md) im Benutzerhandbuch zu Komponenten.

**Neue Nutzer** erhalten Sie wie folgt:

1. Ziehen Sie die Metrik **Unique Visitors** in den Arbeitsbereich.
2. Ziehen Sie das Segment **Erstbesuche** über die Kopfzeilen der Metrik „Unique Visitors“:

   ![Erstbesuche](../assets/first_time_visits.png)

**Sitzungen** entsprechen ungefähr den **Besuchen** in Analysis Workspace. Weitere Informationen finden Sie im Abschnitt zur Dimension [Besuche](/help/components/metrics/visits.md) im Benutzerhandbuch zu Komponenten.

![Akquise-Metriken](../assets/acquisition_metrics.png)

## Verhaltensmetriken

Die **Absprungrate** steht in Analysis Workspace als Metrik zur Verfügung. Weitere Informationen finden Sie im Abschnitt zur Metrik [Absprungrate](/help/components/metrics/bounce-rate.md) im Benutzerhandbuch zu Komponenten.

**Seiten/Sitzung** ist eine berechnete Metrik. Sie erhalten sie wie folgt:

1. Wenn Sie diese berechnete Metrik bereits erstellt haben, suchen Sie sie unter „Metriken“ und ziehen Sie sie in den Arbeitsbereich.
2. Wenn Sie diese berechnete Metrik noch nicht erstellt haben, klicken Sie auf das Symbol **+** neben der Metrikliste, um den Builder für berechnete Metriken zu öffnen.
3. Geben Sie den Titel „Seitenansichten pro Besuch“ und ggf. eine Beschreibung ein.
4. Legen Sie das Format auf „Dezimal“ fest und setzen Sie die Anzahl der Dezimalstellen auf 2.
5. Ziehen Sie die Metriken **Seitenansichten** und **Besuche** in den Definitionsbereich.
6. Ordnen Sie die Definition so an, dass die Formel **Seitenansichten dividiert durch Besuche** lautet.

   ![Seitenansichten pro Besuch](/help/technotes/ga-to-aa/assets/page_views_per_visit.png)

7. Klicken Sie auf „Speichern“, um zu Ihrem Arbeitsbereich zurückzukehren.
8. Ziehen Sie die neu definierte berechnete Metrik in den Arbeitsbereich.

   Weitere Informationen zu [berechneten Metriken](/help/components/calculated-metrics/cm-overview.md) finden Sie im Benutzerhandbuch zu Komponenten.

**Durchschnittl. Sitzungsdauer** entspricht ungefähr der **Zeit pro Besuch (Sekunden)**. Weitere Informationen zu Metriken der [pro Besuch verbrachten Zeit](/help/components/metrics/time-spent-per-visit.md) finden Sie im Benutzerhandbuch zu Komponenten.

## Konversionsmetriken

**Zielvorhaben-Conversion-Rate**, **Zielvorhabenabschlüsse** und **Zielvorhabenwert** erfordern eine zusätzliche Implementierung auf beiden Plattformen. Wenn Ihre Implementierung bereits die Produktdimension und das Kaufereignis berücksichtigt, sollten Sie die folgenden Schritte beachten:

1. Ziehen Sie die Metriken **Bestellungen**, **Umsatz** und **Besuche** in den Arbeitsbereich.
1. Erstellen Sie eine berechnete Metrik aus **Bestellungen pro Besuch**. Halten Sie die Strg- (Windows) oder Befehlstaste (Mac) gedrückt und klicken Sie auf beide Metrikkopfzeilen, um sie zu markieren. Klicken Sie mit der rechten Maustaste auf eine der Kopfzeilen, wählen Sie **Metrik aus Auswahl erstellen** und klicken Sie dann auf **Teilen**. Diese neue Metrik ähnelt der Zielvorhaben-Konversionsrate.
1. Falls Dezimalstellen erforderlich sind, bearbeiten Sie die berechnete Metrik. Klicken Sie auf die Info-Schaltfläche in der Metrikkopfzeile und dann auf das Stiftsymbol. Fügen Sie im Fenster des Builders für berechnete Metriken eine oder zwei Dezimalstellen hinzu und klicken Sie dann auf „Speichern“.

   ![Bestellungen pro Besuch](/help/technotes/ga-to-aa/assets/orders_per_visit.png)

Wenn Ihre Implementierung noch keine Produkt- oder Konversionsdaten enthält, empfiehlt Adobe, mit einem Implementierungsberater zusammenzuarbeiten, um die Datenqualität und -integrität sicherzustellen.
