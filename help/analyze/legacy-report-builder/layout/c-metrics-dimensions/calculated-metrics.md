---
description: Report Builder 5.2 unterstützt vereinheitlichte berechnete Adobe Analytics-Metriken. Neben anderen Innovationen verfügen alle berechneten Metriken jetzt über eine globale ID – sie sind nicht mehr auf eine einzige Report Suite beschränkt.
title: Berechnete Metriken
feature: Report Builder
role: User, Admin
exl-id: 462086eb-675f-443c-b3a6-b4fa390254da
source-git-commit: fcecc8a493852f5682fd7fbd5b9bb484a850922c
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 78%

---

# Berechnete Metriken 

{{legacy-arb}}

Report Builder 5.2 und höher unterstützt berechnete Adobe Analytics-Metriken. Alle berechneten Metriken verfügen jetzt über eine globale ID und sind nicht mehr auf eine Report Suite beschränkt.

>[!NOTE]
>
>Vorhandene Arbeitsmappen können auf Anforderungen mit alten Metrik-IDs verweisen. Wenn Sie Report Builder 5.2 verwenden, werden diese alten Metrik-IDs in die neue globale ID konvertiert. Wenn Sie diese Arbeitsmappe für einen Benutzer von Report Builder v5.1 oder älter freigeben, kann dieser Benutzer die berechneten Metriken nicht anzeigen.

Weitere Informationen zum Erstellen und Verwalten von berechneten Metriken mit dem neuen Generator und Manager für berechnete Metriken finden Sie im Handbuch [Berechnete Metriken](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/cm-overview.html?lang=de).

In Schritt 2 des Anforderungs-Assistenten können Sie berechnete Metriken filtern und anwenden.

## Berechnete Metriken filtern {#section_376E986D3E684999A7CDB08E53854159}

**Filtern** Berechnete Metriken, indem Sie auf das Filtersymbol klicken: ![Screenshot der Filteroptionen mit den Feldern „Anwendung“, „Benutzer“, „Projekt“.](/help/admin/admin/assets/filter.png)

Im Dialogfeld „Erweiterte Filter“ werden die Standardmetriken und berechneten Metriken aufgeführt.

Folgende Filter stehen zur Verfügung:

![Screenshot mit den in der folgenden Tabelle beschriebenen erweiterten Filteroptionen.](assets/advanced_filters.png)

| Filtername | Beschreibung |
|---|---|
| Tags | Filtert berechnete Metriken mit bestimmten Tags. Beachten Sie, dass Tagfilter mit dem Operator AND arbeiten. Wenn Sie zwei Tags aktivieren, werden im rechten Fenster Metriken angezeigt, die mit **beiden** Tags versehen wurden. |
| Report Suites | Wenn Sie im Generator für berechnete Metriken in [!DNL Adobe Analytics] den Filter „Nur *Name der Report Suite*“ anwenden und dann in [!DNL Report Builder] den erweiterten Filter anzeigen, zeigt der erweiterte Filter nur die berechneten Metriken für die ausgewählte Report Suite an. |
| Inhaber | Filtert berechnete Metriken nach Inhaber. Beachten Sie, dass Inhaberfilter mit dem Operator OR arbeiten. Wenn Sie zwei Inhaber aktivieren, werden im rechten Fenster Metriken angezeigt, die **beiden** Inhabern gehören. |
| Weitere Filter > Genehmigt | Zeigt alle offiziell genehmigten Metriken an. |
| Weitere Filter > Favoriten | Zeigt alle Metriken an, die Sie als Favoriten markiert haben. |
| Weitere Filter > Meine | Zeigt alle Metriken an, deren Inhaber Sie sind. |
| Weitere Filter > Für mich freigegeben | Zeigt alle Metriken an, die für Sie freigegeben wurden. |

## Berechnete Metriken anwenden {#section_DF5CF349460A45FDA4B6E6BB8B52F18E}

Wenn Sie die Filter ausgewählt haben, klicken Sie auf **[!UICONTROL Übernehmen]**, um sie auf Ihre Anforderung anzuwenden. Die ausgewählten Metriken werden zum Berichtslayout hinzugefügt.

![Screenshot mit dem Anforderungs-Assistenten: Schritt 2: Site-Gesamtwerte, die auf das Fenster „Erweiterte Filter“ und die angewendeten Berichtsmetriken verweisen.](assets/filtering_for_metric.png)
