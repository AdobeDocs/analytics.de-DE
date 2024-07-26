---
title: Kapiteldimensionen von Streaming-Medien
description: Verfügbare Dimensionen, wenn Sie [!UICONTROL Medienkapitel] für eine Report Suite aktivieren.
feature: Dimensions
source-git-commit: 26c131a37fa1f30c83fd99b290523a97d3c954db
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 14%

---

# Kapiteldimensionen von Streaming-Medien

*Auf dieser Seite werden die verfügbaren Dimensionen beschrieben, wenn Sie [!UICONTROL Medienkapitel] für eine Report Suite aktivieren. Verfügbare Metriken finden Sie unter [Kapitelmetriken für Streaming-Medien](../metrics/sm-chapters.md) .*

Die Kapiteldimensionen von Streaming-Medien bieten zusätzliche Berichtsfunktionen für die Datenerfassung über Streaming-Mediensammlungsbibliotheken. Für die Verwendung dieser Dimensionen ist das **[!UICONTROL Adobe Streaming Media Collection Add-on]** erforderlich. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

Wenn Sie **[!UICONTROL Medienkapitel]** unter [Medienberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, ist die folgende Dimension verfügbar:

| Name der Dimension | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Kapitel | Die automatisch generierte Kapitel-ID. | Chapter Close | `a.media.chapter.name` |

{style="table-layout:auto"}

Zusätzlich zu den oben genannten Dimensionen erstellt Adobe automatisch die folgenden Classification-Dimensionen. Sie müssen Classification-Daten hochladen, um Berichte anzuzeigen, die diese Dimensionen verwenden.

| Klassifizierungsname | Übergeordnete Dimension | Beschreibung |
| --- | --- | --- |
| Urheber | [Inhalt](sm-core.md) | Der Ersteller des Inhalts. |
| Kapitellänge | Kapitel | Die Länge des Kapitels in Sekunden. |
| Kapitelname | Kapitel | Der Anzeigename des Kapitels. |
| Kapiteloffset | Kapitel | Der Versatz des Kapitels innerhalb des Inhalts ab Beginn in Sekunden. |
| Kapitelposition | Kapitel | Die Indexposition des Kapitels im Inhalt. |

{style="table-layout:auto"}
