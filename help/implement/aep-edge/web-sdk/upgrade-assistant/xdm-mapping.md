---
title: XDM-Zuordnung im Web SDK Upgrade-Assistenten
description: Ordnen Sie Ihre Adobe Analytics-Variablen im Rahmen einer Web SDK-Migration Feldern in einem XDM-Schema zu.
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
source-wordcount: '419'
ht-degree: 3%
---
# XDM-Zuordnung

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_xdmmapping"
>title="XDM-Zuordnung"
>abstract="Ordnen Sie die von Ihnen ausgewählten Analytics-Variablen Feldern in einem XDM-Schema zu. Der Upgrade-Assistent kann ein neues Schema mit von KI vorgeschlagenen Zuordnungen erstellen oder Sie können Variablen einem Schema zuordnen, das Sie bereits haben. Überprüfen Sie alle Zuordnungen, bevor Sie fortfahren."

<!-- markdownlint-enable MD034 -->

Web SDK sendet Daten mithilfe von [Experience-Datenmodell (XDM)](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/home). Daher benötigt jede Analytics-Variable, die Sie von der [Report Suite-Überprüfung](rs-verification.md) übertragen, ein übereinstimmendes Feld in einem XDM-Schema. In diesem Schritt wählen Sie ein Schema aus und ordnen Ihre Variablen seinen Feldern zu.

## Auswählen eines Schemas {#schema}

Sie können die Zuordnung auf zwei Arten erstellen:

* **Neues Schema erstellen**: Der Upgrade-Assistent analysiert Ihre Analytics-Variablen und schlägt für jede Variablen ein XDM-Feld vor. Anschließend generiert er ein Schema aus diesen Vorschlägen, das Sie überprüfen können.
* **Vorhandenes Schema verwenden**: Wählen Sie ein Schema aus, das bereits in Experience Platform vorhanden ist, und ordnen Sie dann jede Variable selbst einem Feld zu.

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_xdmmapping_fieldgroups"
>title="Voreinstellung für Feldergruppen"
>abstract="Wählen Sie aus, welchen Typ von Feldergruppe der Upgrade-Assistent beim Erstellen Ihres Schemas bevorzugen soll. Standardfeldgruppen werden von Adobe definiert. Benutzerdefinierte Feldergruppen werden von Ihrer Organisation definiert."

<!-- markdownlint-enable MD034 -->

Beim Erstellen eines neuen Schemas können Sie auch auswählen, ob der Upgrade-Assistent standardmäßige oder benutzerdefinierte Feldergruppen bevorzugt. Standardfeldgruppen werden von Adobe definiert, benutzerdefinierte Feldgruppen dagegen von Ihrem Unternehmen. Siehe [Feldergruppe](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition#field-group) in der XDM-Dokumentation.

## Überprüfen der Zuordnung {#review}

Die Zuordnung listet jede Analytics-Variable zusammen mit dem XDM-Feld auf, dem sie zugeordnet ist, mit einer Vorschau des vollständigen Schemas daneben. Wählen Sie einen Teil des Schemas aus, um die Liste nach den Variablen zu filtern, die ihr zugeordnet sind. Sie können sowohl einzelne Zuordnungen als auch das Schema selbst anpassen.

Der Upgrade-Assistent verwendet KI, um Zuordnungen vorzuschlagen, und die Ergebnisse sind möglicherweise nicht genau oder vollständig. Überprüfen Sie jede Zuordnung, bevor Sie fortfahren. Der Upgrade-Assistent erstellt das Schema erst dann in Experience Platform, wenn Sie die [&#x200B; abgeschlossen &#x200B;](final-review.md#finalize).

Wenn Sie fertig sind, wählen Sie **[!UICONTROL Speichern und fortfahren]** um Ihre Zuordnung zu speichern und zur [Web SDK-Implementierung](web-sdk-implementation.md) zu wechseln. Um die Zuordnung nach dem Speichern zu ändern, wählen Sie **[!UICONTROL Bearbeiten]**, nehmen Sie Ihre Änderungen vor und klicken Sie dann erneut auf **[!UICONTROL Speichern und]** Weiter“. Änderungen, die auf diese Weise nicht gespeichert werden, werden beim Abschluss der Migration nicht einbezogen.
