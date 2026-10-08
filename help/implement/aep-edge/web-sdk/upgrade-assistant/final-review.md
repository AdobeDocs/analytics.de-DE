---
title: Abschließende Überprüfung im Web SDK Upgrade Assistant
description: Überprüfen und schließen Sie eine Web SDK-Migration ab und veröffentlichen Sie dann die resultierende Tag-Bibliothek in der Produktionsumgebung.
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
source-wordcount: '469'
ht-degree: 0%
---
# Abschließende Überprüfung

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_finalreview"
>title="Abschließende Überprüfung"
>abstract="Wählen Sie die zu verwendende Experience Platform-Sandbox aus und überprüfen Sie dann alles, was bei dieser Migration erstellt oder geändert wird. Es ändert sich nichts, bis Sie die Migration abgeschlossen haben. Wenn Sie die Migration abschließen, erstellt der Upgrade-Assistent alles auf einmal, fügt die Tag-Änderungen zu einer neuen Bibliothek hinzu und macht diese Migration schreibgeschützt. Sie veröffentlichen diese Bibliothek dann selbst in der Produktionsumgebung."

<!-- markdownlint-enable MD034 -->

Die abschließende Überprüfung ist der letzte Schritt einer Migration. Es werden alle Elemente angezeigt, die durch die Migration in Experience Platform und in Ihrer Tags-Eigenschaft erstellt werden oder sich ändern.

## Erfahren Sie, was durch die Migration entsteht {#review}

Wählen Sie zunächst die Experience Platform-Sandbox aus, in der die Migration die Ressourcen erstellt. Sie können die Migration erst abschließen, wenn Sie eine Sandbox auswählen.

Der Upgrade-Assistent listet dann alles auf, was durch den Abschluss der Migration erstellt oder geändert wird:

* **[!UICONTROL XDM]**: Ein neues Schema, das nach Ihrer XDM-Zuordnung benannt ist, zusammen mit den benutzerdefinierten Feldergruppen, die es benötigt. Standardfeldgruppen sind bereits vorhanden, sodass das Schema sie so verwendet, wie sie sind. Dieser Abschnitt wird nur angezeigt, wenn Sie in der XDM-[&#x200B; ein neues Schema erstellen &#x200B;](xdm-mapping.md#schema).
* **[!UICONTROL Datensätze]**: Zwei Datensätze, einer für Entwicklung und einer für Produktion. Jeder wird nach der Migration benannt, z. B. `My migration - Development`.
* **[!UICONTROL Datenströme]**: Zwei Datenströme, einer für die Entwicklung und einer für die Produktion, werden auf die gleiche Weise wie die Datensätze benannt.
* **[!UICONTROL Adobe Tags]**: Eine neue Bibliothek, die nach der Migration benannt wurde, z. B. `Library - "My migration"`. Die -Bibliothek enthält die Regeln und Datenelemente, die durch die Migration geändert werden, sowie die Erweiterungskonfiguration, die für die Web SDK-Aktionen erforderlich ist.

## Abschließen der Migration {#finalize}

Bis zum Abschluss der Migration ändert der Upgrade-Assistent Ihre Tags-Eigenschaft nicht und erstellt auch nichts in Experience Platform.

>[!IMPORTANT]
>
>Nachdem Sie eine Migration abgeschlossen haben, ist sie schreibgeschützt. Sie können es weiterhin über die Seite **[!UICONTROL Migrationen]** öffnen, um zu sehen, was es erstellt hat, aber Sie können es nicht ändern oder erneut abschließen. Da sich die neue Bibliothek noch in der Entwicklung befindet, können Sie die Tag-Änderungen in der Tag-Benutzeroberfläche bearbeiten oder entfernen, bevor Sie die Bibliothek veröffentlichen.

1. Wählen Sie **[!UICONTROL Artefakte erstellen]** aus.
1. Wählen **[!UICONTROL Dialogfeld „Diese Empfehlungen überprüfen]** die Option **[!UICONTROL Fortfahren]**.
1. Führen Sie in **[!UICONTROL Migration abschließen?]** wählen Sie im Dialogfeld **[!UICONTROL Abschließen]** aus.

Der Upgrade-Assistent erstellt alles auf einmal und zeigt den Fortschritt an. Er fügt die Tags-Änderungen zur neuen Bibliothek hinzu, veröffentlicht die Bibliothek jedoch nicht.

## Veröffentlichen der Änderungen {#publish}

Nachdem Sie die Migration abgeschlossen haben, verschieben Sie die neue Bibliothek durch den Veröffentlichungsablauf für Tags:

1. Erstellen und testen Sie die Bibliothek in Ihrer Entwicklungsumgebung, um sicherzustellen, dass Ihre Web SDK-Implementierung die erwarteten Daten sendet.
1. Bibliothek zur Genehmigung einreichen und in Ihrer Staging-Umgebung testen.
1. Genehmigen Sie die Bibliothek und veröffentlichen Sie sie in der Produktionsumgebung.

Siehe [Veröffentlichungsablauf](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/publishing/publishing-flow) im Benutzerhandbuch zu Tags.
