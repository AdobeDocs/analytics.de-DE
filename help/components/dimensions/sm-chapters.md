---
title: Streaming-Medien-Kapiteldimensionen
description: Verfügbare Dimensionen, wenn Sie [!UICONTROL Medienkapitel] für eine Report Suite aktivieren.
feature: Dimensions
exl-id: cac66a0b-3f83-46a9-b35c-ba08e0eafb92
source-git-commit: fdd66c9558f070cd760f37a39e5911f0dac22612
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 14%

---

# Streaming-Medien-Kapiteldimensionen

*Auf dieser Seite werden die verfügbaren Dimensionen beschrieben, wenn Sie [!UICONTROL Medienkapitel] für eine Report Suite aktivieren. Unter [Metriken für Streaming-Medien](../metrics/sm-chapters.md) finden Sie verfügbare Metriken.*

Streaming-Medien-Kapiteldimensionen bieten zusätzliche Reporting-Funktionen für die Datenerfassung über Streaming-Mediensammlungsbibliotheken. Für die Verwendung dieser Dimensionen ist die Sammlung **[!UICONTROL Adobe-Streaming-Medien erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

Wenn Sie **[!UICONTROL Medienkapitel]** unter [Medienberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, ist die folgende Dimension verfügbar:

| Name der Dimension | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Kapitel | Die automatisch generierte Kapitel-ID. | Kapitelschluss | `a.media.chapter.name` |

{style="table-layout:auto"}

Zusätzlich zu den oben genannten Dimensionen erstellt Adobe automatisch die folgenden Klassifizierungsdimensionen. Sie müssen Klassifizierungsdaten hochladen, um Berichte anzuzeigen, die diese Dimensionen verwenden.

| Klassifizierungsname | Übergeordnete Dimension | Beschreibung |
| --- | --- | --- |
| Urheber | [Inhalt](sm-core.md) | Der Ersteller des Inhalts. |
| Kapitellänge | Kapitel | Die Länge des Kapitels in Sekunden. |
| Kapitelname | Kapitel | Der Anzeigename des Kapitels. |
| Versatz des Kapitels | Kapitel | Der Versatz des Kapitels innerhalb des Inhalts vom Anfang in Sekunden. |
| Kapitelposition | Kapitel | Die Indexposition des Kapitels im Inhalt. |

{style="table-layout:auto"}
