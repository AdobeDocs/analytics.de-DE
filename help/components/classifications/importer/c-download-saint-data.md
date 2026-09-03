---
description: (Optional) Vor dem Import von Klassifizierungen in Marketing-Berichte können Sie eine Vorlage herunterladen, mit der Sie eine Klassifizierungsdatendatei erstellen können. Die Datendatei verwendet Ihre gewünschten Klassifizierungen als Spaltenüberschriften und organisiert dann den Berichtsdatensatz unter den entsprechenden Klassifizierungs-Überschriften.
title: Klassifizierungsvorlage
feature: Classifications
exl-id: e299509a-0c4f-4ba8-9e91-96356c386054
TQID: https://experienceleague.adobe.com/OR9THCLd93iUl58npPiinO4yAsK8KG3FU8qmBILHioY
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: c80b99d6-98b9-4aeb-b5c4-933ef2ef705c
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 355
ht-degree: 61%

---

# Klassifizierungsvorlage (veraltet)

{{classification-importer-deprecation}}

(Optional) Vor dem Importieren von Klassifizierungen in Marketing-Berichte können Sie eine Vorlage herunterladen, um eine Klassifizierungsdatendatei zu erstellen. Die Datendatei verwendet Ihre gewünschten Klassifizierungen als Spaltenüberschriften und organisiert dann den Berichtsdatensatz unter den entsprechenden Klassifizierungs-Überschriften.

## Klassifizierungsvorlage {#concept_0F06847AD8D042F5BA818AE3C37E2417}

(Optional) Vor dem Import von Klassifizierungen in Marketing-Berichte können Sie eine Vorlage herunterladen, mit der Sie eine Klassifizierungsdatendatei erstellen können. Die Datendatei verwendet Ihre gewünschten Klassifizierungen als Spaltenüberschriften und organisiert dann den Berichtsdatensatz unter den entsprechenden Klassifizierungs-Überschriften.

**[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.

| Element | Beschreibung |
| --- | ---|
| Report Suite auswählen | Die in der Vorlage zu verwendende Report Suite auswählen. Report Suite und Datensatz müssen übereinstimmen. |
| Datensatz, der klassifiziert werden soll | Wählen Sie den Datentyp für die Datendatei aus. Das Menü enthält alle Berichte in Ihren Report Suites, die für Klassifizierungen konfiguriert sind. |
| Export von Numerisch 2 | **Wichtig**: Diese Option ist nicht für Report Suites verfügbar, die für die neue Klassifizierungsarchitektur aktiviert sind. |
| Codierung | Wählen Sie die Zeichencodierung für die Datendatei aus. Das Standardcodierungsformat ist UTF-8.<br>**Wichtig**: Diese Option ist nicht für Report Suites verfügbar, die für die neue Klassifizierungsarchitektur aktiviert sind. |
| Download | Lädt die Vorlagendatei herunter. |

Die Vorlage enthält die derzeit definierten Klassifizierungen (Spaltenüberschriften) eines bestimmten Datensatzes, ohne die mit den einzelnen Klassifizierungen verknüpften Daten einzubeziehen.

>[!NOTE]
>
>Die Vorlagenmethode beschränkt Ihre heruntergeladenen Classification-Daten auf eine einzige Report Suite.

Weitere Informationen zur Datendateistruktur finden Sie unter [Informationen zu Klassifizierungsdatendateien](/help/components/classifications/importer/c-saint-data-files.md).

## Herunterladen einer Classification-Datenvorlage (optional) {#task_8DFCF309B6FD43ABB1D6FEE9AFAEC596}

Die Vorlage liefert das Dateiformat, das für Classifications genutzt werden muss.

>[!NOTE]
>
>Die Vorlagenmethode beschränkt Ihre heruntergeladenen Daten auf eine einzige Report Suite.

1. Klicken Sie auf **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Legen Sie unter der Registerkarte **[!UICONTROL Vorlage herunterladen]** die Konfiguration für die [-Datenvorlage fest](/help/components/classifications/importer/c-download-saint-data.md).
1. Klicken Sie auf **[!UICONTROL Herunterladen]**.
1. Speichern Sie die Vorlagendatei auf Ihrem lokalen System.

   Die Vorlagendatei ist eine tabulatorgetrennte Datendatei (Dateierweiterung [!DNL .tab]), die von den meisten Tabellenkalkulationsprogrammen unterstützt wird.
