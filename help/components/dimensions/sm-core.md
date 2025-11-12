---
title: Kerndimensionen der Streaming-Mediendienste
description: Verfügbare Dimensionen, wenn Sie [!UICONTROL Media Core] für eine Report Suite aktivieren.
feature: Dimensions
exl-id: 1316a646-a31a-49a4-a670-d56d90dd462b
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 7%

---

# Kerndimensionen der Streaming-Mediendienste

*Auf dieser Seite werden die verfügbaren Dimensionen beschrieben, wenn Sie [!UICONTROL Media Core] für eine Report Suite aktivieren. Verfügbare Metriken finden Sie [Kernmetriken ](../metrics/sm-core.md) Streaming-Mediendienste“.*

Die Kerndimensionen der Streaming-Mediendienste bieten grundlegende Reporting-Funktionen für Daten, die über Bibliotheken der Streaming-Mediendienste erfasst werden. Für die Verwendung dieser Dimensionen ist das Add **[!UICONTROL on Adobe Analytics for Streaming Media erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

Wenn Sie **[!UICONTROL Media Core]** unter [Medienberichte](/help/admin/tools/manage-rs/edit-settings/media-management.md) aktivieren, sind die folgenden Dimensionen verfügbar:

| Name der Dimension | Beschreibung | Gesendet mit | Kontextdatenvariable | XDM-Feld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Inhalt]** | Inhalts-ID des Inhalts. | Medienstart, Medienschluss | `a.media.`<br>`name` | `xdm.mediaCollection.`<br>`sessionDetails.name`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.name` |
| **[!UICONTROL Inhaltskanal]** | Die Verteilungs-Workstation oder der Kanal, auf der bzw. dem der Inhalt wiedergegeben wird. Jeder Zeichenfolgenwert ist gültig. | Medienstart, Medienschluss | `a.media.`<br>`channel` | `xdm.mediaCollection.`<br>`sessionDetails.channel`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.channel` |
| **[!UICONTROL Inhaltslänge (variabel)]** | Die maximale Länge (oder Dauer) des verbrauchten Inhalts in Sekunden. Diese Dimension ist für mehrere Metriken erforderlich, einschließlich &quot;[!UICONTROL Zielgruppendurchschnitt pro Minute]. Wenn diese Dimension nicht festgelegt ist, sind abhängige Metriken nicht verfügbar.<br><br>Eine Classification-Dimension mit dem Namen [!UICONTROL Videolänge] ist ebenfalls verfügbar und hat einen ähnlichen Zweck. Diese Dimension und die Klassifizierung werden als zwei verschiedene Dimensionen behandelt. | Medienstart, Medienschluss | `a.media.`<br>`length` | `xdm.mediaCollection.`<br>`sessionDetails.length`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.length` |
| **[!UICONTROL Inhaltsname (Variable)]** | Der Anzeigename des Inhalts. Eine Klassifizierung mit dem Namen [!UICONTROL Videoname] ist ebenfalls verfügbar und hat einen ähnlichen Zweck. Diese Dimension und die Klassifizierung werden als zwei verschiedene Dimensionen behandelt. | Medienstart, Medienschluss | `a.media.`<br>`friendlyName` | `xdm.mediaCollection.`<br>`sessionDetails.friendlyName`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.friendlyName` |
| **[!UICONTROL Name des Inhalts-Players]** | Der Name des Content-Players. | Medienstart, Medienschluss | `a.media.`<br>`playerName` | `xdm.mediaCollection.`<br>`sessionDetails.playerName`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.playerName` |
| **[!UICONTROL Inhaltssegment]** | Das Intervall in Minuten, das den angezeigten Teil des Inhalts beschreibt. Das Segment wird als Mindest- und Höchstwert der Werte der Abspielleiste bei einer Wiedergabesitzung berechnet. | Schließen von Medien | `a.media.`<br>`segment` | `xdm.mediaReporting.`<br>`sessionDetails.segment` |
| **[!UICONTROL Content-Typ]** | Der Inhaltstyp. Gültige Werte sind `song`, `podcast`, `audiobook`, `radio`, `VoD`, `Live`, `Linear`, `UGC`, `DVoD` oder ein benutzerdefinierter Wert. | Medienstart, Medienschluss | `a.contentType` | `xdm.mediaCollection.`<br>`sessionDetails.contentType`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.contentType` |
| **[!UICONTROL Medienpfad]** | Der Pfad, über den der Besucher zum Inhalt gelangte. | Medienstart | `a.media.path` | |
| **[!UICONTROL Stream-Typ]** | Der Stream-Typ. Gültige Werte sind `audio` und `video`. | Medienstart, Medienschluss | `a.media.`<br>`streamType` | `xdm.mediaCollection.`<br>`sessionDetails.streamType`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.streamType` |

Zusätzlich zu den oben genannten Dimensionen erstellt Adobe automatisch die folgenden Klassifizierungsdimensionen. Sie müssen Klassifizierungsdaten hochladen, um Berichte anzuzeigen, die diese Dimensionen verwenden.

| Klassifizierungsname | Übergeordnete Dimension | Beschreibung |
| --- | --- | --- |
| **[!UICONTROL Videolänge]** | [!UICONTROL Inhalt] | Die maximale Länge (oder Dauer) des verbrauchten Inhalts in Sekunden. Metriken, die von der Inhaltslänge abhängen, können diese Klassifizierung nicht verwenden. Sie müssen eine berechnete Metrik erstellen, um Metriken wie &quot;[!UICONTROL Zielgruppendurchschnitt pro Minute] mit dieser Klassifizierung zu erhalten. |
| **[!UICONTROL Videoname]** | [!UICONTROL Inhalt] | Der Anzeigename des Inhalts. Dies entspricht der Klassifizierung von &quot;[!UICONTROL Inhaltsname (Variable)]&quot;. |
