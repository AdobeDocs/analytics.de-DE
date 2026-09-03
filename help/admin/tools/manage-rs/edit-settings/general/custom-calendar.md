---
description: Kalenderoptionen in anderen als dem gregorianischen Modell. Zu den Optionen gehören die Kalendermodelle 4-4-5, 4-5-4 und 5-4-4, die alle als Standards für den Einzelhandel verwendet werden. Das Reporting bietet außerdem einen vollständig anpassbaren Kalender, den Sie selbst einrichten können.
title: Anpassen von Kalendern
feature: Admin Tools
exl-id: 2196c7b7-7183-43a8-bb91-5a1e479819d4
role: Admin
TQID: https://experienceleague.adobe.com/14PcXGRnv3ab-D2NaRAs4-pgiDYk4OnMnKCfNB2uEbc
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: c153fd90-23e1-4614-81d3-3cc7571227f7id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
subfeature_v2: id: e44bec7e-8653-4d5b-b53e-60b1ae7c3475id: ef60b66e-5984-4336-ba72-6d978b1b6f87
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 563
ht-degree: 34%

---

# Anpassen von Kalendern

Kalenderoptionen in anderen als dem gregorianischen Modell. Zu den Optionen gehören die Kalendermodelle 4-4-5, 4-5-4 und 5-4-4, die alle als Standards für den Einzelhandel verwendet werden. Darüber hinaus bietet Reporting eine Option für einen vollständig anpassbaren Kalender, den Sie selbst einrichten können.

**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Report Suite auswählen **[!UICONTROL > Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Kalender benutzerspezifisch einstellen]**

>[!CAUTION]
>
>Wenn Sie Änderungen am Kalender vornehmen, ändern Sie die Art der Datenverarbeitung (d. h. die Definition der Unique Visitors pro Woche und pro Monat). Wenn die Definition von Wochen und Monaten eines Kalenders geändert wird, bleiben historische Daten unberührt. Diese Einstellung wirkt sich auch auf Segmente aus, die auf Datumsbereichen basieren.

Sie können den Kalender verwenden, um den ersten Wochentag und das erste Jahr zu definieren, oder einen anderen Einzelhandelskalenderstil verwenden. Die Kalenderformate werden für verschiedene Zwecke verwendet, einschließlich Verkaufsvergleich und Prognosestandardisierung, Lohnkostenanalyse oder Regulierung der Inventuranzahl. Beispielsweise verwendet die Einzelhandelsbranche den Buchungskalender 4-5-4, um die Besonderheiten der Verkaufssaison an die Einzelhandelsbranche zu unterstützen. Nachfolgend werden die einzelnen Kalenderformate beschrieben.

## Kalender benutzerspezifisch einstellen – Beschreibungen {#section_B0D224DACB914A378902A4E0E1234889}

| Kalender | Beschreibung |
|--- |--- |
| Gregorianischer Kalender | Verwendet das herkömmliche Kalenderformat (Januar bis Dezember, mit 30 oder 31 Tagen und einer variablen Anzahl von Wochen pro Monat). |
| Modifizierter gregorianischer Kalender | Verwendet den traditionellen gregorianischen Kalender, ermöglicht jedoch die Auswahl des ersten Monats des Jahres und des ersten Wochentags. |
| 4-5-4 Einzelhandelskalender | Schlüsselt jeden Monat nach der Anzahl der Wochen im Monat auf. Der Januar hat also vier Wochen und so weiter. Die National Retail Federation verwendet das Kalenderformat 4-5-4. |
| Benutzerdefinierter Kalender | Bietet drei Formate, die auf der Anzahl der Wochen in jedem Monat basieren. Die Anzahl der Wochen in jedem Monat hängt vom ausgewählten ersten Tag des Jahres ab.  Ein Jahr hat 52 Wochen. Teilen Sie das auf 4 Quartale auf und Sie bekommen 13 Wochen pro Quartal. Aber es gibt drei Monate in einem Quartal. Die Zahl 13 ist nicht durch 3 teilbar. Folglich muss die restliche Woche aus Konsistenzgründen zu einem der Monate hinzugefügt werden.<ul><li>5/4/4 bedeutet, dass der 1. Monat des Quartals die zusätzliche Woche hat. 4/5/4 bedeutet, dass der 2. Monat die zusätzliche Woche hat usw. Im Kalender 5-4-4 wird die 53. Woche zum letzten Quartal des Jahres hinzugefügt.</li><li>4-5-:January hat vier Wochen, Februar hat fünf Wochen, März hat vier Wochen usw.</li><li>4-4-5: Januar hat vier Wochen, Februar hat vier Wochen, März hat fünf Wochen usw.</li><li>5-4-4: Januar hat fünf Wochen, Februar hat vier Wochen, März hat vier Wochen usw.</li></ul> |

>[!NOTE]
>Diese Kalenderoptionen werden in allen Adobe Analytics-Tools (Analysis Workspace, Report Builder, Activity Map) mit Ausnahme von Data Warehouse unterstützt. Data Warehouse unterstützt nur den gregorianischen Kalender vollständig. Bei der Auswahl eines nicht-gregorianischen Kalenders verwendet Data Warehouse den erwarteten Datumsbereich des nicht-gregorianischen Kalenders. Die Aufschlüsselung nach Tag/Woche/Monat in den Berichtszeilen entspricht jedoch möglicherweise nicht den Erwartungen an einen nicht-gregorianischen Kalender.
