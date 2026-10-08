---
title: Web SDK-Implementierung im Web SDK Upgrade Assistant
description: Überprüfen Sie die Web SDK-Aktionen, die der Upgrade-Assistent zu Ihren bestehenden Tag-Regeln hinzufügt.
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
source-wordcount: '311'
ht-degree: 0%
---
# Web SDK-Implementierung

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_websdkimplementation"
>title="Web SDK-Implementierung"
>abstract="Überprüfen Sie die Web SDK-Aktionen, die der Upgrade-Assistent zu Ihren Regeln hinzufügt. Ihre Adobe Analytics-Aktionen bleiben erhalten. Wählen Sie eine Komponente aus, um ihre aktuellen Konfigurationen und die von Web SDK nebeneinander zu vergleichen. Nur die Komponenten, die Sie in die Warteschlange stellen, werden der Migration hinzugefügt."

<!-- markdownlint-enable MD034 -->

Unter Verwendung der von Ihnen ausgewählten Komponenten und Ihrer [XDM-Zuordnung](xdm-mapping.md) fügt der Upgrade-Assistent direkt nach jeder Adobe Analytics-Aktion Web SDK-Aktionen zu Ihren Regeln hinzu. Die Analytics-Aktionen bleiben erhalten, sodass diese Regeln Daten sowohl an Adobe Analytics als auch an Web SDK senden. Die meisten Datenelemente übertragen sie unverändert, und die Regeln verweisen weiterhin auf sie nach Namen.

Die Spalte **[!UICONTROL Änderungstyp]** zeigt, was das Abschließen der Migration für jede Komponente bewirkt:

* **[!UICONTROL Web SDK-Aktionen hinzugefügt]**: Der Upgrade-Assistent fügt Web SDK-Aktionen zur Regel hinzu.
* **[!UICONTROL Keine Änderung]**: Die Komponente wird unverändert übernommen.
* **[!UICONTROL Blockiert]**: Die Komponente muss überprüft werden, bevor der Upgrade-Assistent Web SDK-Aktionen hinzufügen kann. Wählen Sie die Komponente aus, um zu sehen, was sie blockiert.

Wählen Sie eine Komponente aus, um ihre aktuelle Konfiguration Seite an Seite mit ihrer Web SDK-Konfiguration zu vergleichen. Wenn Sie mehr Kontext benötigen, verweist der Upgrade-Assistent auf die Komponente in der Tags-Benutzeroberfläche.

Komponenten, die Sie in die Warteschlange stellen, werden der Migration hinzugefügt. Um eine Komponente in die Warteschlange einzureihen, wählen Sie sie in der Liste aus oder wählen Sie **[!UICONTROL Warteschlange]** in den Details aus. Um ihn wieder zu entfernen, wählen Sie **[!UICONTROL Aus Warteschlange entfernen]** aus. Der Upgrade-Assistent ändert Ihre Tag-Eigenschaft erst, wenn Sie [die Migration abgeschlossen haben](final-review.md#finalize).

Der Upgrade-Assistent verwendet KI, um die Web-SDK-Aktionen zu generieren, und die Ergebnisse sind möglicherweise nicht genau oder vollständig. Beim Generieren der Aktionen wird nicht überprüft, wie sie sich auf Ihrer Site verhalten. Daher sollten Sie sie testen, bevor Sie die Bibliothek veröffentlichen.
