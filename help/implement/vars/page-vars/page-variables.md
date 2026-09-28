---
title: Seitenvariablen
description: Legen Sie Werte auf einer einzelnen Seite fest.
feature: Appmeasurement Implementation
exl-id: 321d0db2-61a3-478e-ab51-8e06c7b2bb7b
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/mWfMumcPTklFPKUiGIOatDbC0WKW5RDYH56rXTFk3ZY'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
subfeature_v2:
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
    internal-label: Variables
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
    internal-label: Events
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
    internal-label: Appmeasurement implementation
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
source-git-commit: 9a50beeb0aa51cf9f4baf212566947c14029ce8e
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 47%
---
# Übersicht zu Seitenvariablen

Seitenvariablen bestimmen die Werte für Dimensionen und Metriken in Berichten.

Die folgende Liste enthält die häufig in Implementierungen verwendeten Variablen:

* [`pageName`](pagename.md): Der Name der Seite.
* [`campaign`](campaign.md): Legen Sie diese Variable auf einen Abfragezeichenfolge-Parameter zum Tracken von Kampagnen fest.
* [`events`](events/events-overview.md): Füllen Sie Metriken zur Verwendung in Berichten.
* [`products`](products.md): Wenn Sie eine E-Commerce-Site haben, legen Sie diese Variable fest, wenn ein Besucher ein Produkt ansieht oder kauft.

## Eingestellte Seitenvariablen

Die folgenden Seitenvariablen werden eingestellt. Sie werden hier als Referenz dokumentiert, wenn Sie sie in einer Legacy-Implementierung feststellen.

* **`hier`**: Hierarchievariablen implementiert (`hier1`-`hier5`), um die Struktur einer Site für das Reporting zu erfassen. Sie ist veraltet und keine verfügbare Dimension mehr in Analysis Workspace. Verwenden Sie stattdessen [eVars](evar.md) und Klassifizierungen.
* **`state`**: Erfasst den US-Bundesstaat, in den ein Besucher eingetreten ist, normalerweise über ein Versand- oder Rechnungsformular. Verwenden Sie stattdessen [[!UICONTROL  Dimension ]](/help/components/dimensions/us-states.md)US-Bundesstaaten“, mit der Adobe automatisch vom geografischen Standort des Besuchers ausfüllt.
