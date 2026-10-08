---
title: Komponentenauswahl im Web-SDK-Upgrade-Assistenten
description: Wählen Sie aus, welche Tag-Regeln, Datenelemente und Erweiterungen in eine Web SDK-Migration einbezogen werden sollen.
feature: Implementation Basics
role: Admin, Developer, Leader
badge: Beta
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
  - id: a421fb65-2c82-457a-921c-28c46b697a39
    internal-label: Analytics basics
subfeature_v2:
  - id: e4f5f438-eabb-4c54-9133-b817e3d125f5
    internal-label: Use cases
  - id: c24fe15a-643a-47bd-8278-5e027df49785
    internal-label: Implementation basics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 629efca210346d32b8555c60f7db15d1d8285b20
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%
---
# Komponentenauswahl

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_componentselection"
>title="Komponentenauswahl"
>abstract="Wählen Sie die Regeln, Datenelemente und Erweiterungen aus, die in diese Migration einbezogen werden sollen. Komponenten, die aktiv zu Ihrer Adobe Analytics-Implementierung beitragen, sind standardmäßig ausgewählt. Spätere Schritte funktionieren nur mit den Komponenten, die Sie hier auswählen."

Die Komponentenauswahl ist der erste Schritt einer Migration. Verwenden Sie diese Option, um festzulegen, welche Regeln, Datenelemente und Erweiterungen aus Ihrer Tag-Eigenschaft in die Migration einbezogen werden sollen.

Der Upgrade-Assistent organisiert die Komponenten in Ihrer Tags-Eigenschaft in **[!UICONTROL Regeln]**, **[!UICONTROL Datenelemente]** und **[!UICONTROL Erweiterungen]**. Jede Registerkarte listet alle Komponenten der Eigenschaft dieses Typs auf, basierend auf dem Schnappschuss der Bibliothek, den der Upgrade-Assistent bei der Erstellung [ Migration erstellt ](manager.md#create). Standardmäßig werden nur die Komponenten ausgewählt, die aktiv zu Ihrer Adobe Analytics-Implementierung beitragen. Sie können eine beliebige Komponente auswählen oder löschen.

Die Spalte **[!UICONTROL Veröffentlicht]** zeigt an, ob jede Komponente Teil der von Ihnen ausgewählten Bibliothek ist. Komponenten, die nicht Teil der Bibliothek sind, sind in Ihrer Tags-Eigenschaft vorhanden, jedoch nicht in dieser Bibliothek. Um die Liste hiernach zu filtern, verwenden Sie den **[!UICONTROL Source]** Filter.

Sie können Komponenten einbeziehen, die nicht mit Adobe Analytics zusammenhängen, z. B. Komponenten für Adobe Target, Adobe Audience Manager oder Erweiterungen von Drittanbietern, die jedoch vom Upgrade-Assistenten nicht in die Web-SDK konvertiert werden.

Die von Ihnen ausgewählten Komponenten bestimmen, mit welchen späteren Schritten Sie arbeiten. Sie können beispielsweise Datenelemente einbeziehen, die durch nichts referenziert werden, sodass [Auditergebnisse](audit-findings.md) diese zur Bereinigung kennzeichnen können.

## Komponentendetails anzeigen {#details}

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_componentselection_tagsusage"
>title="Verwendung von Tags"
>abstract="Die Regeln, Datenelemente und Erweiterungen, die diese Komponente verwenden. Die Verwendung der Erweiterung deckt nur die Konfigurationseinstellungen von Erweiterungen ab. Die Verwendung innerhalb einer Regel wird unter „Regelverwendung“ angezeigt."

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_componentselection_analyticsusage"
>title="Analytics-Nutzung"
>abstract="Die Adobe Analytics-Variablen, denen diese Komponente zugewiesen ist, gruppiert nach Variablentyp."

<!-- markdownlint-enable MD034 -->

Wählen Sie den Namen einer Komponente aus, um ein Bedienfeld zu öffnen, das ihre Konfiguration und deren Verwendung anzeigt:

* **[!UICONTROL Verwendung von Tags]**: Die Regeln, Datenelemente und Erweiterungen, die die -Komponente verwenden. **[!UICONTROL Verwendung von Erweiterungen]** deckt nur die Konfigurationseinstellungen von Erweiterungen ab. Die Verwendung innerhalb einer Regel wird unter **[!UICONTROL Regelverwendung]** angezeigt.
* **[!UICONTROL Analytics-]**: Die Adobe Analytics-Variablen, denen die Komponente zugewiesen ist, gruppiert nach Variablentyp.

Um die Komponente in der Tags-Benutzeroberfläche anzuzeigen, wählen Sie oben im Bedienfeld ihren Namen aus.

Wenn Sie fertig sind, wählen Sie **[!UICONTROL Speichern und fortfahren]**, um zu [Audit-Ergebnissen](audit-findings.md) zu wechseln.