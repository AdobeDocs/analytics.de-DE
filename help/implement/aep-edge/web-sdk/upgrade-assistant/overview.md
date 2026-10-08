---
title: Web SDK-Aktualisierungsassistent
description: Planen Sie die Migration Ihrer Adobe Analytics-Tags-Erweiterung auf die Adobe Experience Platform Web SDK und führen Sie sie aus.
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
source-wordcount: '535'
ht-degree: 3%
---
# Web SDK-Aktualisierungsassistent

Der Web SDK Upgrade Assistant hilft Ihnen bei der Planung und Ausführung der Migration Ihrer Adobe Analytics Tags-Erweiterung auf die Adobe Experience Platform Web SDK. Dadurch wird die Migration in einem einzigen geführten Arbeitsbereich zusammengefasst, sodass Sie strukturiert und verfolgbar von Ihrer bestehenden Tag-Implementierung zum Web-SDK wechseln können.

## Funktionsweise des Upgrade-Assistenten {#how-it-works}

Jede Migration funktioniert mit der Adobe Analytics-Implementierung in einer Tag-Eigenschaft. Der Upgrade-Assistent fügt Ihren bestehenden Regeln Web SDK-Aktionen hinzu, ohne deren Adobe Analytics-Aktionen zu entfernen, sodass Ihre Implementierung weiterhin Daten zusammen mit der Web SDK an Adobe Analytics sendet.

Der Upgrade-Assistent konvertiert nur Adobe Analytics-Komponenten. Sie können Komponenten aus anderen Erweiterungen wie Adobe Target, Adobe Audience Manager oder Erweiterungen von Drittanbietern einbeziehen, der Upgrade-Assistent konvertiert sie jedoch nicht in die Web-SDK.

Der Upgrade-Assistent führt Sie durch die folgenden Schritte, wobei jeder Schritt auf den Entscheidungen aufbaut, die Sie im vorherigen Schritt getroffen haben:

1. **[Komponentenauswahl](component-selection.md)**: Wählen Sie die Regeln, Datenelemente und Erweiterungen aus, die in die Migration aufgenommen werden sollen.
1. **[Auditergebnisse](audit-findings.md)** Überprüfen Sie die optionalen Bereinigungsempfehlungen für die ausgewählten Komponenten.
1. **[Report Suite-Überprüfung](rs-verification.md)**: Überprüfen Sie die Analytics-Variablen in Ihren Report Suites und wählen Sie die weiterzuleitenden Variablen aus.
1. **[XDM-Zuordnung](xdm-mapping.md)**: Ordnen Sie Ihre Analytics-Variablen Feldern in einem XDM-Schema zu.
1. **[Web SDK-Implementierung](web-sdk-implementation.md)**: Überprüfen Sie die Web SDK-Aktionen, die der Upgrade-Assistent zu Ihren Regeln hinzufügt.
1. **[Abschließende Überprüfung](final-review.md)**: Wählen Sie eine Experience Platform-Sandbox aus, überprüfen Sie, was durch die Migration erstellt wird, und schließen Sie die Migration ab.

Mit jedem Schritt wird ein Teil der Migration konfiguriert. Sie können zu den abgeschlossenen Schritten zurückkehren, um sie beliebig oft zu überprüfen oder zu ändern. Der Upgrade-Assistent ändert Ihre Tags-Eigenschaft nicht und erstellt auch nichts in Experience Platform, bis Sie die Migration abgeschlossen haben. Wenn Sie den Vorgang abschließen, erstellt der Upgrade-Assistent alles auf einmal und fügt die Tag-Änderungen einer neuen Bibliothek hinzu. Anschließend testen Sie diese Bibliothek und veröffentlichen sie mithilfe des Tags-Veröffentlichungsflusses in der Produktion.

>[!IMPORTANT]
>
>Der Upgrade-Assistent verwendet künstliche Intelligenz (KI), um Empfehlungen wie XDM-Feldzuordnungen und Web SDK-Regelkonfigurationen zu generieren. Diese Empfehlungen sind möglicherweise nicht korrekt oder vollständig. Überprüfen Sie sie, bevor Sie Ihre Änderungen in der Produktionsumgebung veröffentlichen.

## Voraussetzungen {#prerequisites}

Bevor Sie eine Migration erstellen, stellen Sie Folgendes sicher:

* Die [Berechtigungen](#permissions) die der Upgrade-Assistent erfordert.
* Eine Tags-Eigenschaft, die die Adobe Analytics-Erweiterung verwendet.
* Eine Bibliothek in dieser Eigenschaft, die die Implementierung enthält, die Sie migrieren möchten. Die Bibliothek kann sich in jedem Status befinden, einschließlich „Veröffentlicht“. Siehe [Bibliotheken](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/publishing/libraries) im Benutzerhandbuch zu Tags.

### Berechtigungen {#permissions}

Der Upgrade-Assistent erfordert den folgenden Zugriff. Wenden Sie sich an den Experience Platform-Produktadministrator Ihres Unternehmens, um die fehlenden Berechtigungen zu erhalten.

| Zugriffstyp | erforderlich |
| --- | --- |
| [Berechtigungen für Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/home#permissions) | <ul><li>[!UICONTROL Anzeigen von Schemata]</li><li>[!UICONTROL Verwalten von Schemata]</li><li>[!UICONTROL Anzeigen von Datensätzen]</li><li>[!UICONTROL Datensätze verwalten]</li><li>[!UICONTROL Anzeigen von Identity-Namespaces]</li></ul> |
| Produktzugriff | <ul><li>Datenerfassung (Tags)</li><li>Adobe Analytics</li></ul> |
| [Tag-Rechte](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/administration/user-permissions) | [!UICONTROL Eigenschaften verwalten] |

Wenn Sie bereit sind, [&#x200B; Sie eine Migration &#x200B;](manager.md#create).
