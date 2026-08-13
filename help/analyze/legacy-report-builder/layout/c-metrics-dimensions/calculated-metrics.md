---
description: Report Builder 5.2 unterstützt vereinheitlichte berechnete Adobe Analytics-Metriken. Neben anderen Innovationen verfügen alle berechneten Metriken jetzt über eine globale ID – sie sind nicht mehr auf eine einzige Report Suite beschränkt.
title: Berechnete Metriken
feature: Report Builder
role: User, Admin
exl-id: 462086eb-675f-443c-b3a6-b4fa390254da
TQID: https://experienceleague.adobe.com/Ae-k-aIMg3n3kXYWFngOzYihtlexLCoD5CmnEN3afhI
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 396
ht-degree: 40%

---

# Berechnete Metriken

{{legacy-arb}}

Report Builder 5.2 und höher unterstützt berechnete Adobe Analytics-Metriken. Alle berechneten Metriken verfügen jetzt über eine globale ID und sind nicht mehr auf eine Report Suite beschränkt.

>[!NOTE]
>
>Vorhandene Arbeitsmappen können auf Anforderungen mit alten Metrik-IDs verweisen. Wenn Sie Report Builder 5.2 verwenden, werden diese alten Metrik-IDs in die neue globale ID konvertiert. Wenn Sie diese Arbeitsmappe für einen Benutzer von Report Builder v5.1 oder älter freigeben, kann dieser Benutzer die berechneten Metriken nicht anzeigen.

Weitere Informationen zum Erstellen und Verwalten berechneter Metriken mit dem neuen Generator und Manager für berechnete Metriken finden Sie im Handbuch [Berechnete Metriken](/help/components/calculated-metrics/cm-overview.md) .

In Schritt 2 des Anforderungs-Assistenten können Sie berechnete Metriken filtern und anwenden.

## Berechnete Metriken filtern {#section_376E986D3E684999A7CDB08E53854159}

**Filtern** Berechnete Metriken, indem Sie auf das Filtersymbol klicken: ![Screenshot der Filteroptionen mit den Feldern „Anwendung“, „Benutzer“, „Projekt“.](/help/admin/tools/assets/filter.png)

Das Dialogfeld Erweiterte Filter enthält sowohl standardmäßige als auch berechnete Metriken.

Zu den verfügbaren Filtern gehören:

![Screenshot mit den in der folgenden Tabelle beschriebenen erweiterten Filteroptionen.](assets/advanced_filters.png)

| Filtername | Beschreibung |
|---|---|
| Tags | Ermöglicht das Filtern berechneter Metriken mit bestimmten Tags. Beachten Sie, dass Tagfilter mit dem Operator AND arbeiten. Wenn Sie zwei Tags überprüfen, zeigt der rechte Bereich Metriken an, die mit (**)** Tags versehen wurden. |
| Report Suites | Wenn Sie im Generator für berechnete Metriken in [!DNL Adobe Analytics] den Filter „Nur *Name der Report Suite*“ anwenden und dann in [!DNL Report Builder] den erweiterten Filter anzeigen, zeigt der erweiterte Filter nur die berechneten Metriken für die ausgewählte Report Suite an. |
| Inhaberinnen oder Inhaber | Ermöglicht das Filtern von Metriken nach Inhaber. Beachten Sie, dass Inhaberfilter mit dem Operator OR arbeiten. Wenn Sie zwei Eigentümer überprüfen, zeigt der rechte Bereich Metriken an, die dem/**Eigentümer/** gehören. |
| Weitere Filter > Genehmigt | Zeigt alle offiziell genehmigten Metriken an. |
| Weitere Filter > Favoriten | Zeigt alle Metriken an, die als Favoriten markiert wurden. |
| Weitere Filter > Meine | Zeigt alle Metriken an, deren Inhaber Sie sind. |
| Weitere Filter > Für mich freigegeben | Zeigt alle Metriken an, die andere für Sie freigegeben haben. |

## Berechnete Metriken anwenden {#section_DF5CF349460A45FDA4B6E6BB8B52F18E}

Klicken Sie nach Auswahl der Filter auf **[!UICONTROL Anwenden]** um sie auf Ihre Anfrage anzuwenden. Die ausgewählte(n) Metrik(en) werden jetzt zum Berichtslayout hinzugefügt.

![Screenshot mit dem Anforderungs-Assistenten: Schritt 2: Site-Gesamtwerte, die auf das Fenster „Erweiterte Filter“ und die angewendeten Berichtsmetriken verweisen.](assets/filtering_for_metric.png)
