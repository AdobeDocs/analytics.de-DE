---
title: Kerndimensionen der Streaming-Mediendienste
description: Verfügbare Dimensionen, wenn Sie [!UICONTROL Media Core] für eine Report Suite aktivieren.
feature: Dimensions
exl-id: 1316a646-a31a-49a4-a670-d56d90dd462b
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 9%

---

# Kerndimensionen der Streaming-Mediendienste

*Auf dieser Seite werden die verfügbaren Dimensionen beschrieben, wenn Sie [!UICONTROL Media Core] für eine Report Suite aktivieren. Verfügbare Metriken finden Sie [Kernmetriken &#x200B;](../metrics/sm-core.md) Streaming-Mediendienste“.*

Die Kerndimensionen der Streaming-Mediendienste bieten grundlegende Reporting-Funktionen für Daten, die über Bibliotheken der Streaming-Mediendienste erfasst werden. Für die Verwendung dieser Dimensionen ist das Add **[!UICONTROL on Adobe Analytics for Streaming Media erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

Wenn Sie **[!UICONTROL Media Core]** unter [Medienberichte](/help/admin/tools/manage-rs/edit-settings/media-management.md) aktivieren, sind die folgenden Dimensionen verfügbar:

| Name der Dimension | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Inhalt | Inhalts-ID des Inhalts. | Medienstart, Medienschluss | `a.media.name` |
| Inhaltskanal | Die Verteilungs-Workstation oder der Kanal, auf der bzw. dem der Inhalt wiedergegeben wird. Jeder Zeichenfolgenwert ist gültig. | Medienstart, Medienschluss | `a.media.channel` |
| Inhaltslänge (variabel) | Die maximale Länge (oder Dauer) des verbrauchten Inhalts in Sekunden. Diese Dimension ist für mehrere Metriken erforderlich, einschließlich „Zielgruppendurchschnitt pro Minute“. Wenn diese Dimension nicht festgelegt ist, sind abhängige Metriken nicht verfügbar.<br><br>Eine Klassifizierungsdimension mit dem Namen „Videolänge“ ist ebenfalls verfügbar und hat einen ähnlichen Zweck. Diese Dimension und die Klassifizierung werden als zwei verschiedene Dimensionen behandelt. | Medienstart, Medienschluss | `a.media.length` |
| Inhaltsname (Variable) | Der Anzeigename des Inhalts. Eine Klassifizierung mit dem Namen „Videoname“ ist ebenfalls verfügbar und hat einen ähnlichen Zweck. Diese Dimension und die Klassifizierung werden als zwei verschiedene Dimensionen behandelt. | Medienstart, Medienschluss | `a.media.friendlyName` |
| Name des Inhalts-Players | Der Name des Content-Players. | Medienstart, Medienschluss | `a.media.playerName` |
| Inhaltssegment | Das Intervall in Minuten, das den angezeigten Teil des Inhalts beschreibt. Das Segment wird als Mindest- und Höchstwert der Werte der Abspielleiste bei einer Wiedergabesitzung berechnet. | Schließen von Medien | `a.media.segment` |
| Inhaltstyp | Der Inhaltstyp. Gültige Werte sind `song`, `podcast`, `audiobook`, `radio`, `VoD`, `Live`, `Linear`, `UGC`, `DVoD` oder ein benutzerdefinierter Wert. | Medienstart, Medienschluss | `a.contentType` |
| Medienpfad | Der Pfad, über den der Besucher zum Inhalt gelangte. | Medienstart | `a.media.path` |
| Stream-Typ | Stream-Typ. Gültige Werte sind `audio` und `video`. | Medienstart, Medienschluss | `a.media.streamType` |

{style="table-layout:auto"}

Zusätzlich zu den oben genannten Dimensionen erstellt Adobe automatisch die folgenden Klassifizierungsdimensionen. Sie müssen Klassifizierungsdaten hochladen, um Berichte anzuzeigen, die diese Dimensionen verwenden.

| Klassifizierungsname | Übergeordnete Dimension | Beschreibung |
| --- | --- | --- |
| Videolänge | Inhalt | Die maximale Länge (oder Dauer) des verbrauchten Inhalts in Sekunden. Metriken, die von der Inhaltslänge abhängen, können diese Klassifizierung nicht verwenden. Sie müssen eine berechnete Metrik erstellen, um Metriken wie „Zielgruppendurchschnitt pro Minute“ mit dieser Klassifizierung zu erhalten. |
| Videoname | Inhalt | Der Anzeigename des Inhalts. Es ist das Klassifizierungsäquivalent des Inhaltsnamens (Variable). |

{style="table-layout:auto"}
