---
title: Streaming-Medien-Kapiteldimensionen
description: Verfügbare Dimensionen, wenn Sie [!UICONTROL Medienkapitel] für eine Report Suite aktivieren.
feature: Dimensions
exl-id: cac66a0b-3f83-46a9-b35c-ba08e0eafb92
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 8%

---

# Kapiteldimensionen für Streaming-Mediendienste

*Auf dieser Seite werden die verfügbaren Dimensionen beschrieben, wenn Sie [!UICONTROL Medienkapitel] für eine Report Suite aktivieren. Verfügbare Metriken finden [&#x200B; unter &#x200B;](../metrics/sm-chapters.md)Metriken zu Streaming-Mediendiensten“.*

Die Kapiteldimensionen für Streaming-Mediendienste bieten zusätzliche Berichtsfunktionen für die Datenerfassung über Streaming-Mediendienstbibliotheken. Für die Verwendung dieser Dimensionen ist das Add **[!UICONTROL on Adobe Analytics for Streaming Media erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

Wenn Sie **[!UICONTROL Medienkapitel]** unter [Medienberichte](/help/admin/tools/manage-rs/edit-settings/media-management.md) aktivieren, ist die folgende Dimension verfügbar:

| Name der Dimension | Beschreibung | Gesendet mit | Kontextdatenvariable | XDM-Feld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Kapitel]** | Die automatisch generierte Kapitel-ID. | Kapitelschluss | `a.media.chapter.name` | `xdm.mediaReporting.`<br>`chapterDetails.ID` |

Zusätzlich zu den oben genannten Dimensionen erstellt Adobe automatisch die folgenden Klassifizierungsdimensionen. Sie müssen Klassifizierungsdaten hochladen, um Berichte anzuzeigen, die diese Dimensionen verwenden.

| Klassifizierungsname | Übergeordnete Dimension | Beschreibung |
| --- | --- | --- |
| **[!UICONTROL Urheber]** | [[!UICONTROL Inhalt]](sm-core.md) | Der Ersteller des Inhalts. |
| **[!UICONTROL Kapitellänge]** | [!UICONTROL Kapitel] | Die Länge des Kapitels in Sekunden. |
| **[!UICONTROL Kapitelname]** | [!UICONTROL Kapitel] | Der Anzeigename des Kapitels. |
| **[!UICONTROL Kapitelversatz]** | [!UICONTROL Kapitel] | Der Versatz des Kapitels innerhalb des Inhalts vom Anfang in Sekunden. |
| **[!UICONTROL Kapitelposition]** | [!UICONTROL Kapitel] | Die Indexposition des Kapitels im Inhalt. |
