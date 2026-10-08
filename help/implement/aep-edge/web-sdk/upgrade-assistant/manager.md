---
title: Verwalten von Migrationen im Web SDK Upgrade Assistant
description: Erstellen, Anzeigen und Öffnen von Migrationen im Web SDK Upgrade-Assistenten.
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
source-wordcount: '397'
ht-degree: 0%
---
# Verwalten von Migrationen

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_migrations"
>title="Migrationen"
>abstract="Bei jeder Migration wird die Adobe Analytics-Implementierung in einer Tags-Eigenschaft auf die Web-SDK aktualisiert. Öffnen Sie eine Migration, um dort fortzufahren, wo Sie aufgehört haben, oder wählen Sie „Neu“, um eine Migration zu starten."

Die **[!UICONTROL Migrationen]** ist der Ausgangspunkt für den Web SDK Upgrade-Assistenten. Es werden die Migrationen in Ihrer Organisation aufgelistet, einschließlich des Fortschritts, des Status und der Erstellerin bzw. des Erstellers jeder Migration. Verwenden Sie diese Seite, um eine Migration zu erstellen oder eine vorhandene zu öffnen.

## Erstellen einer Migration {#create}

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_newmigration"
>title="Neue Migration"
>abstract="Wählen Sie die Tags-Eigenschaft aus, die Sie migrieren möchten, und eine Bibliothek in dieser Eigenschaft. Der Upgrade-Assistent erstellt bei der Erstellung der Migration einen Schnappschuss der Bibliothek. Änderungen, die nach einem Migrationsschnappschuss an der Bibliothek vorgenommen wurden, sind nicht enthalten. Ihre Tags-Eigenschaft ändert sich erst, wenn Sie die Migration abgeschlossen haben."

<!-- markdownlint-enable MD034 -->

Bevor Sie eine Migration erstellen, stellen Sie sicher, dass Sie die [Voraussetzungen](overview.md#prerequisites) erfüllen.

1. Wählen Sie auf der **[!UICONTROL Migrationen]** die Option **[!UICONTROL Neu]** aus.
1. Geben Sie einen Namen für die Migration und optional eine Beschreibung ein.
1. Wählen Sie die Tags-Eigenschaft aus, die Sie migrieren möchten.
1. Wählen Sie eine Tag-Bibliothek aus. Wenn Sie die Migration erstellen, erstellt der Upgrade-Assistent einen Schnappschuss Ihrer Implementierung, so wie sie in dieser Bibliothek vorhanden ist. Änderungen, die Sie danach an der Bibliothek vornehmen, werden nicht in der Migration übernommen.
1. Wählen Sie **[!UICONTROL Erstellen]** aus.

Die neue Migration wird in der Liste angezeigt. Öffnen Sie sie, um [Komponentenauswahl](component-selection.md) zu starten.

## Öffnen einer Migration {#open}

Wählen Sie den Namen einer Migration aus, um sie zu öffnen. Die Schritte der Migration werden im linken Navigationsbereich angezeigt. Sie können zu jedem abgeschlossenen Schritt zurückkehren, um ihn beliebig oft zu überprüfen oder zu ändern, aber die Schritte, die Sie noch nicht erreicht haben, sind noch nicht verfügbar.

Der Upgrade-Assistent speichert Ihren Fortschritt, während Sie die Schritte durchlaufen, sodass Sie eine Migration beenden und später zu ihr zurückkehren können. Die konfigurierten Elemente werden erst wirksam, wenn Sie [die Migration abgeschlossen haben](final-review.md#finalize). Nach Abschluss des Vorgangs ist die Migration schreibgeschützt. Sie können es immer noch öffnen, um zu sehen, was es erstellt hat, aber Sie können es nicht ändern.

## Sonstige Migrationsaktionen {#actions}

Wählen Sie die Zeile einer Migration aus, um die dafür verfügbaren Aktionen anzuzeigen:

* **[!UICONTROL Fortfahren]**: Öffnet die Migration.
* **[!UICONTROL Ausführung duplizieren]**: Erstellt eine Kopie der Migration.
* **[!UICONTROL Umbenennen]**: Ändert den Namen und die Beschreibung der Migration.
* **[!UICONTROL Archivieren]**: Ändert den Migrationsstatus in &quot;**[!UICONTROL Archiviert]**.
* **[!UICONTROL Migration löschen]**: Löscht die Migration dauerhaft. Das kann man nicht rückgängig machen.
