---
title: Mapper-Vorbereitung im Web SDK Upgrade-Assistenten
description: Überprüfen Sie die Analytics-Variablen in Ihren Report Suites und wählen Sie aus, welche in die XDM-Zuordnung übernommen werden sollen.
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
source-git-commit: 212d38950264a33b925b7281c241992cadca2bfb
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%
---
# Mapper-Vorbereitung

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_mapperprep"
>title="Mapper-Vorbereitung"
>abstract="Überprüfen Sie die Analytics-Variablen, die Ihre Tags-Eigenschaft an jede Report Suite sendet. Variablen, die Sie hier auswählen, werden in die XDM-Zuordnung übertragen. Verwenden Sie die Registerkarten, um nach aktuellen Daten zu suchen, doppelte Variablen zu finden und Einstellungen in allen Report Suites zu vergleichen."

<!-- markdownlint-enable MD034 -->

Der Upgrade-Assistent identifiziert die Report Suites, an die Ihre Tags-Eigenschaft Daten sendet, und vergleicht dann die Analytics-Variablen in Ihrer Implementierung mit der Konfiguration jeder Report Suite und den jüngsten Daten. Verwenden Sie diesen Schritt, um zu entscheiden, welche Variablen in die XDM[Zuordnung &#x200B;](xdm-mapping.md) werden.

Der Upgrade-Assistent verwendet Ihre Report Suites, um zu verstehen, welche Variablen Ihre Implementierung setzt und wie sie konfiguriert sind. Aktivitätsdaten beziehen sich auf die letzten 90 Tage.

## Aktivität „Variable“ {#variable-activity}

Auf der Registerkarte **[!UICONTROL Variablenaktivität]** werden die Analytics-Variablen für die Report Suite aufgelistet, die Sie in der [Variablenanalyse](#variable-analysis) zugeordnet haben, und es wird angezeigt, ob jede Variable in den letzten 90 Tagen Daten erfasst hat.

Variablen, die Sie auswählen, werden in die XDM-Zuordnung übertragen. Löschen Sie Variablen, die keine Daten mehr erfassen oder die Sie nicht in Ihrer Web SDK-Implementierung benötigen. Eine Variable ohne aktuelle Aktivität kann weiterhin verwendet werden, z. B. wenn sie saisonal abhängig ist oder nur geringen Traffic hat. Bestätigen Sie also, dass Sie sie nicht benötigen, bevor Sie sie löschen.

Geben Sie für jede Listenvariable und Listen-Prop, die Sie weiterleiten, das Trennzeichen ein, das die Werte trennt. Der Upgrade-Assistent kann keine Trennzeichen aus Adobe Analytics erhalten und Sie können nicht fortfahren, bis jeder ein Trennzeichen hat.

## Variablenanalyse {#variable-analysis}

Wenn Ihre Tags-Eigenschaft Daten an mehr als eine Report Suite sendet, wählen Sie zunächst die zuzuordnende Report Suite aus. Auf der Registerkarte **[!UICONTROL Variablenanalyse]** werden dann Variablen gekennzeichnet, die möglicherweise einer Entscheidung bedürfen, bevor Sie sie zuordnen:

* Variablen, die anscheinend dieselben Daten erfassen. Vergewissern Sie sich, dass sie dieselben Informationen erfassen, und entscheiden Sie dann, ob sie in einer einzelnen Variablen zusammengeführt oder getrennt bleiben sollen.
* Variablen, die in letzter Zeit keine Daten erfasst haben.
* Variablen mit Werten „Unspecified“.

## Report Suites vergleichen {#compare}

Wenn Ihre Tags-Eigenschaft Daten an mehr als eine Report Suite sendet, werden auf der Registerkarte **[!UICONTROL Report Suites vergleichen]** die Einstellungen jeder Variablen in bis zu drei dieser Report Suites verglichen. Verwenden Sie sie, um Variablen zu finden, die zwischen den Report Suites unterschiedlich konfiguriert sind, bevor Sie sie einem Schema zuordnen.

## Aktualisieren von Report Suite-Daten {#refresh}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_mapperprep_refresh"
>title="Report Suite-Daten aktualisieren"
>abstract="Überprüft die mit dieser Tags-Eigenschaft verknüpften Report Suites erneut, einschließlich ihrer Variableneinstellungen und der letzten Daten, und führt dann die Variablenanalyse erneut aus. Wenn der Upgrade-Assistent noch keine Report Suites gefunden hat, sucht er zuerst in der Tag-Eigenschaft nach ihnen. Ihre Auswahl und Entscheidungen werden beibehalten."

<!-- markdownlint-enable MD034 -->

Sie können in diesem Schritt ändern, welche Report Suites der Upgrade-Assistent analysiert. Wenn sich Ihre Report Suite-Konfiguration während einer Migration ändert, wählen Sie **[!UICONTROL Report Suite-Daten aktualisieren]** aus, um die Analyse erneut auszuführen. Der Upgrade-Assistent behält Ihre vorhandenen Auswahlen und Entscheidungen bei.

Wenn Sie fertig sind, wählen Sie **[!UICONTROL Speichern und fortfahren]** aus, um zur [XDM-Zuordnung“ &#x200B;](xdm-mapping.md).
