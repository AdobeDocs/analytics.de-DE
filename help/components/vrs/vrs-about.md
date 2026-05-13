---
description: Virtual Report Suites segmentieren die Adobe Analytics-Daten, sodass der Zugriff auf die einzelnen Segmente gesteuert werden kann.
title: Virtual Report Suites – Überblick
feature: VRS
exl-id: 45d18d14-d95a-42fe-b00a-cfce5f936e37
TQID: https://experienceleague.adobe.com/gEs8c9pIUGbbPx7DBAwFhSvT-C6W2vfosgMkrO-32ic
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2:
  - id: ac8a38fa-dec3-4581-8f64-178fde9f64e8
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
  - id: c069c44e-5426-4c1a-accc-8028662f2fde
  - id: e93b8c4c-c5f7-45f8-9abe-9b710f53f502
  - id: ef60b66e-5984-4336-ba72-6d978b1b6f87
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 812
ht-degree: 33%

---

# Virtual Report Suites – Überblick

Virtual Report Suites segmentieren die Adobe Analytics-Daten, sodass der Zugriff auf die einzelnen Segmente gesteuert werden kann.

Bei vielen Kunden fließen Daten in eine globale Report Suite, aber auch Daten in kleinere Report Suites. Sie legen eine Variable auf mehrere Report Suites fest und senden ihre Daten an mehr als eine Report Suite. Die Bezeichnung dafür lautet *Multi-Suite-Tagging* oder *zugrunde liegende/übergeordnete Report Suites*.

Beispielsweise können alle Daten in einer Report Suite erfasst werden. Anschließend können Sie jedoch sekundäre Report Suites einrichten, sodass andere Personen in Ihrem Unternehmen Zugriff auf einen Teil der Daten haben, jedoch nicht auf alle. Die Daten können nach Region unterteilt sein. Es kann verschiedene Websites für verschiedene Länder geben. Andere Beispiele sind bestimmte Marken, die zu einem größeren Unternehmen gehören, aber jeweils über eigene Marketing-Teams verfügen.

Mithilfe einer *Virtual Report Suite* können Sie dieses Verzweigungskonzept reproduzieren, indem Sie anstelle von mehreren Report Suites Segmente verwenden. Die Daten werden an eine Report Suite gesendet und dann nach Segmenten unterteilt. Wenn Sie das Beispiel „Mehrere Marken“ verwenden, können Sie eine Eigenschaft für die Marke festlegen, zu der ein Element gehört. Mithilfe von Segmenten können Sie Berichte zu den Elementen erstellen, die jeder Eigenschaft zugewiesen sind. Jedes dieser Segmente wird zu einer eigenen Ansicht und erstellt effektiv eine neue Report Suite. Sie senden keine spezifischen Daten an dieses Segment, sondern nur an die globale Report Suite. In Ihren Berichten funktioniert dies jedoch so, als wäre es eine andere Report Suite.

Eine Virtual Report Suite übernimmt die meisten Service-Level der zugrunde liegenden Report Suite, z. B. eVar-Einstellungen, Verarbeitungsregeln, Klassifizierungen usw. Die folgenden Einstellungen werden NICHT vererbt:

* Report Suite-ID (RSID)
* Name der Report Suite
* Berechtigungsgruppen (Virtual Report Suites können ihren eigenen Berechtigungsgruppen zugewiesen werden)

## Vorteile von Virtual Report Suites {#section_3420422FE6DF46EAB151FD9442AAFDC4}

Kunden zahlen für sekundäre Server-Aufrufe, sodass die Eliminierung dieser Aufrufe zu erheblichen Einsparungen führen kann. Eine Virtual Report Suite ist ebenfalls vollständig rückwirkend. Wenn die globale Report Suite bereits Daten enthält, werden die entsprechenden Daten automatisch in eine neue Virtual Report Suite aufgenommen. Eine neue sekundäre Report Suite beginnt erst mit der Datenerfassung, nachdem sie erstellt wurde, sodass sie keine historischen Daten enthält. Wenn Sie Analytics implementieren, müssen Sie nur Daten an eine Report Suite senden, anstatt Implementierungen für die globale Report Suite und jede sekundäre Report Suite erstellen zu müssen.

Virtual Report Suites bieten Hilfe:

* Vereinfachen Sie die Implementierung, indem Sie eine einzelne Report Suite-ID (RSID) für alle Sites/Domains verwenden. Die Tatsache, dass alle Daten in einer einzigen Report Suite erfasst sind, ermöglicht Kundenanalysen auf dem Weg zur nächsten Generation von Adobe Analytics.
* Business-Anwender in Ihrer Organisation sehen immer nur die Datensegmente, die für sie relevant sind.
* Erhöhen Sie die Sicherheit, indem Sie es Admin-Benutzern ermöglichen, den Datenzugriff nach der Implementierung einfacher und detaillierter zu steuern.
* Metrik für Personen
* Eine zentrale Datenansicht (in der Zukunft)
* Die Möglichkeit, unbegrenzte Virtual Report Suites zu erstellen, um Daten zu segmentieren

## Einschränkungen von Virtual Report Suites {#section_F22A6DEBDC9848429E446F4CC2C4EEDE}

Virtual Report Suites haben die folgenden Einschränkungen:

* Die Einschränkungen von Segmenten gelten auch für Virtual Report Suites

  Eine Virtual Report Suite ist lediglich ein Segment, das auf eine Report Suite angewendet wird. Da alle Report Suites über ein eigenes Data Warehouse und einen eigenen Daten-Feed verfügen, bietet die Verwendung mehrerer Report Suites einige Vorteile gegenüber Segmenten.
* Echtzeitbericht
* Einstellungen und Variablennamen können nicht wie bei einer vollständigen Report Suite angepasst werden

## Virtual Report Suites und Multi-Suite-Tagging im Vergleich {#section_317E4D21CCD74BC38166D2F57D214F78}

| Funktion | Virtual Report Suite | Multi-Suite-Tagging |
|--- |--- |--- |
| Berichte zu Echtzeit- oder aktuellen Daten | Nein | Ja |
| Funktioniert in allen Analytics-Tools (Analysis Workspace, Report Builder usw.) | Ja. **Hinweis:** Sie können sie nur unter [!UICONTROL Analytics] > [!UICONTROL Komponenten] > [!UICONTROL Virtual Report Suites] bearbeiten und identifizieren. Sie können in den anderen Tools jedoch in den Dropdown-Listen für Report Suites ausgewählt werden.<p>**Wichtig**: Virtual Report Suites mit Berichtszeitverarbeitung und Variablenanpassung werden derzeit in Adobe Report Builder nicht unterstützt. | Ja |
| Können Daten in ihn hochladen (über Klassifizierungen, Daten-Feeds usw.), | Nein | Ja |
| Unterstützt die Erstellung von DL-Berichten, Lesezeichen, Dashboards, Zielen, Warnhinweisen, Segmenten, berechneten Metriken… | Ja | Ja |
| Kann einzeln zu Berechtigungsgruppen hinzugefügt werden | Ja | Ja |
| Kann mithilfe von Admin-Funktionen einzelne Einstellungen dieser Report Suite ändern (Admin > Report Suites) | Nein (Einstellungen werden von der übergeordneten übernommen) | Ja |

{style="table-layout:auto"}

## Kombinieren von Virtual Report Suites und Multi-Suite-Tagging {#section_026FA3FCD7314DD18220E73EC5702AFF}

In einigen Fällen hat die Verwendung von Virtual Report Suites und Multi-Suite-Tagging Vorteile.

Beispielsweise kann ein retailer für jede Marke eine Report Suite und für jede Marke Virtual Report Suites verwenden, um Daten nach Region aufzuschlüsseln. Gleichermaßen kann eine sportliche Organisation für jedes Team eine Report Suite und dann Virtual Report Suites verwenden, um die Fans in der Region des Teams von denen außerhalb der Region zu unterscheiden.
