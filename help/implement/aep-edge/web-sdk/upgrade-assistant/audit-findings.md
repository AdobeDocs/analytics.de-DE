---
title: Audit-Ergebnisse im Web SDK Upgrade Assistant
description: Überprüfen und beheben Sie die optionalen Bereinigungsempfehlungen für Ihre Tags-Komponenten, bevor Sie zur Web-SDK migrieren.
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
source-wordcount: '336'
ht-degree: 2%
---
# Prüfungsergebnisse

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_auditfindings"
>title="Prüfungsergebnisse"
>abstract="Die Ergebnisse zeigen Regeln und Datenelemente, die Sie vor der Migration bereinigen sollten, z. B. Datenelemente, die durch nichts referenziert werden. Akzeptieren Sie ein Ergebnis, um seine empfohlene Änderung in die Migration aufzunehmen, oder lehnen Sie es ab, um die Komponente so zu lassen, wie sie ist. Dieser Schritt ist optional."

<!-- markdownlint-enable MD034 -->

Der Upgrade-Assistent überprüft die unter „Komponentenauswahl“ ausgewählten Regeln [ Datenelemente ](component-selection.md) kennzeichnet diejenigen, die Sie vor der Migration bereinigen möchten:

* Duplizieren Sie Regeln oder Regeln, die Ereignisse und Bedingungen gemeinsam nutzen, die Sie konsolidieren könnten
* Regelaktionssequenzen, die sich auf die Datengenauigkeit auswirken können
* Duplizieren Sie Datenelemente, die Sie konsolidieren könnten
* Möglicherweise nicht verwendete Datenelemente, die Sie deaktivieren können

Dieser Schritt ist optional. Sie können beliebig viele Ergebnisse beheben oder direkt mit der [Report Suite-Überprüfung) ](rs-verification.md).

## Überprüfen eines Ergebnisses {#review}

Einen Fund auswählen, um seine Details anzuzeigen, einschließlich:

* Eine Beschreibung des Ergebnisses
* Die aktuelle Konfiguration der Komponente
* Wo die Komponente verwendet wird, sowohl in Ihrer Tags-Eigenschaft als auch in Adobe Analytics

Jedes Ergebnis enthält eine empfohlene Aktion, die vom Typ des Ergebnisses abhängt. Die empfohlene Aktion für ein Datenelement, auf das nichts verweist, besteht beispielsweise darin, es zu deaktivieren.

>[!IMPORTANT]
>
>Ein Datenelement, das als nicht verwendet gekennzeichnet ist, kann weiterhin dynamisch oder von außerhalb von Tags referenziert werden. Bevor Sie einen Fund akzeptieren, überprüfen Sie die vorgeschlagenen Änderungen, den benutzerdefinierten Code, die Aktionsreihenfolge und die Verweise, um zu bestätigen, dass sie das beabsichtigte Verhalten beibehalten.

## Ergebnisse beheben {#resolve}

Wenn Sie die empfohlene Aktion eines Ergebnisses verwenden, wird das Ergebnis akzeptiert. Der Upgrade-Assistent fügt die Änderung zur Migration hinzu und wendet sie an, wenn Sie [die Migration abschließen](final-review.md#finalize). Wenn Sie die Änderung nicht vornehmen möchten, lehnen Sie die Suche stattdessen ab.

Sie können eine akzeptierte oder abgelehnte Suche erneut öffnen, wenn Sie es sich anders überlegen. Um mehrere Ergebnisse gleichzeitig zu aktualisieren, wählen Sie sie in der Liste aus.
