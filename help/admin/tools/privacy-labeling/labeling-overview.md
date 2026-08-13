---
description: Die Beschriftung von Report Suite-Daten bedeutet, dass Sie jeder Variablen in Ihren Report Suites Beschriftungen zu Identität, Vertraulichkeit und Data Governance zuweisen.
title: Übersicht über Datenschutzkennzeichnungen
feature: Data Governance
role: Admin
exl-id: d1bd833c-3fd4-4572-a5dc-d7bab8a79cb8
TQID: https://experienceleague.adobe.com/xEs37qiYjTVJWRDKa7HwJqfTtyBYKstA6ehq1-0qKt0
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
  - id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
subfeature_v2:
  - id: b22bc0f7-b089-4966-95a1-31e7b3b69b79
  - id: b99602d0-836e-4dbb-979f-c0dec53f883c
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 534
ht-degree: 94%

---

# Übersicht über Datenschutzkennzeichnungen

Die Beschriftung von Report Suite-Daten bedeutet, dass Sie jeder Variablen in Ihren Report Suites Beschriftungen zu Identität, Vertraulichkeit und Data Governance zuweisen. Machen Sie sich hierzu zunächst mit den [Kennzeichnungen und ihren Definitionen vertraut](/help/admin/tools/privacy-labeling/labels.md).

>[!NOTE]
>
>Beachten Sie, dass die Beschriftung jedes Mal überprüft werden muss, wenn eine neue Report Suite erstellt wird oder in einer vorhandenen Report Suite eine neue Variable aktiviert wird. Sie müssen die Beschriftung möglicherweise auch dann überprüfen, wenn neue Lösungsintegrationen aktiviert werden, da sie neue Variablen zur Verfügung stellen können, für die eine Beschriftung erforderlich ist. Eine erneute Implementierung Ihrer Mobile Apps oder Websites kann die Art und Weise der Verwendung vorhandener Variablen ändern, was möglicherweise auch Aktualisierungen der Kennzeichnungen erforderlich macht.

## Zuweisen oder Bearbeiten von Report-Suite-Datenschutzkennzeichnungen {#assign-edit}

**Beispiel**: Als für die Datenverarbeitung verantwortliche Person planen Sie, E-Mail-Adressen und Cookie-IDs von betroffenen Personen zu sammeln, um deren Datenschutzanfragen zu bearbeiten. Diese Cookie-IDs werden in einer Adobe Analytics Report Suite gespeichert.

1. Navigieren Sie in Adobe Analytics zu **[!UICONTROL Admin]** > **[!UICONTROL Alle Administratoren]** > **[!UICONTROL Datenkonfiguration und -erfassung]** > **[!UICONTROL Data Governance]**.

   ![Datenschutzkennzeichnung](assets/privacy_rs_settings.png)

1. Wählen Sie eine Report Suite aus der obigen **[!UICONTROL Report Suite]**-Auswahl.

1. Wählen Sie links im Filterabschnitt aus, welche Variablengruppen Sie kennzeichnen möchten. Sie können jeweils nur eine Gruppe von Variablen beschriften.

   * **Standardkomponenten** – Standardkomponenten sind native Analytics-Dimensionen und -Metriken, die standardmäßig bei einer Analytics-Implementierung erfasst werden.
   * **Konversionsvariablen** – die Custom-Insight-Konversionsvariable (oder eVar) wird auf ausgewählten Web-Seiten Ihrer Site in den Adobe-Code platziert. Ihr Hauptzweck besteht darin, Konversionserfolgsmetriken in benutzerspezifischen Marketing-Berichten zu segmentieren. Eine eVar kann auf Besuchen basieren und ähnlich wie Cookies funktionieren. In eVar-Variablen übergebene Werte folgen den Benutzenden für einen bestimmten Zeitraum.
   * **Listenvariablen** – Listenvariablen sind benutzerdefinierte Variablen, die Sie beliebig verwenden können. Sie funktionieren ähnlich wie eVars, allerdings können sie mehrere Werte im selben Treffer enthalten. Listenvariablen haben keine Zeichenbeschränkung.
   * **Traffic-Variablen** – Custom-Insight-Traffic-Variablen (oder Props) ermöglichen die Korrelation von benutzerdefinierten Daten mit spezifischen Traffic-bezogenen Ereignissen. Die Eigenschaftsvariablen sind in den Implementierungs-Code auf jeder Seite der Website eingebunden.
   * **Erfolgsereignisse** – Erfolgsereignisse (auch Konversionsereignisse oder benutzerdefinierte Ereignisse genannt) sind Aktionen, die verfolgt werden können. Sie legen fest, was ein Erfolgsereignis ist. Wenn eine Besucherin oder ein Besucher beispielsweise einen Artikel kauft, kann das Kaufereignis als Erfolgsereignis betrachtet werden.
   * **Klassifizierungen** – Klassifizierungsaufschlüsselungen werden zur Zuordnung von Analytics-Berichtsdaten zu bestimmten Eigenschaften eingesetzt. Klassifizierungen können für zahlreiche Zwecke eingesetzt werden, werden jedoch meistens dazu verwendet, um Kampagnen-Trackingcodes (sowohl interne als auch externe) und Produkt-IDs zu klassifizieren.

1. Wählen Sie eine Variable aus, indem Sie das entsprechende Kontrollkästchen aktivieren, und klicken Sie dann auf **[!UICONTROL Datenschutzkennzeichnungen bearbeiten]** auf der blauen Leiste unten auf dem Bildschirm.

   ![Bearbeiten](assets/edit-label.png)

   In diesem Bildschirm werden die aktuell angewendeten Kennzeichnungen angezeigt und Sie können zusätzliche Kennzeichnungen anwenden. Je nach Komponente können Sie möglicherweise nicht alle Kennzeichnungen anwenden oder ändern.

   ![Angewandte Kennzeichnungen](assets/edit-labels2.png)

1. Wenn sämtliche Kennzeichnungen bereit sind, klicken Sie auf **[!UICONTROL Übernehmen]**.

