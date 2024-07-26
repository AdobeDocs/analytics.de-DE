---
title: Hauptdimensionen der Streaming-Medien
description: Verfügbare Dimensionen, wenn Sie [!UICONTROL Media Core] für eine Report Suite aktivieren.
feature: Dimensions
source-git-commit: 26c131a37fa1f30c83fd99b290523a97d3c954db
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 9%

---

# Hauptdimensionen der Streaming-Medien

*Auf dieser Seite werden die verfügbaren Dimensionen beschrieben, wenn Sie [!UICONTROL Media Core] für eine Report Suite aktivieren. Verfügbare Metriken finden Sie unter [Kernmetriken der Streaming-Medien](../metrics/sm-core.md) .*

Die Kerndimensionen von Streaming-Medien bieten grundlegende Berichtsfunktionen für Daten, die über Streaming-Mediensammlungsbibliotheken erfasst werden. Für die Verwendung dieser Dimensionen ist das **[!UICONTROL Adobe Streaming Media Collection Add-on]** erforderlich. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

Wenn Sie **[!UICONTROL Medien-Core]** unter [Medienberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, sind die folgenden Dimensionen verfügbar:

| Name der Dimension | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Inhalt | Kennung des Inhalts. | Media Start, Media Close | `a.media.name` |
| Inhaltskanal | Die Verteilungsstation oder der Kanal, auf der der Inhalt wiedergegeben wird. Jeder Zeichenfolgenwert ist gültig. | Media Start, Media Close | `a.media.channel` |
| Inhaltslänge (Variable) | Die maximale Länge (oder Dauer) des wiedergegebenen Inhalts in Sekunden. Diese Dimension ist für verschiedene Metriken erforderlich, darunter &quot;Zielgruppe &quot;Durchschnittliche Minute&quot;. Wenn diese Dimension nicht festgelegt ist, sind keine abhängigen Metriken verfügbar.<br><br>Es ist auch eine Classification-Dimension mit dem Namen &quot;Videolänge&quot;verfügbar, die einen ähnlichen Zweck bietet. Diese Dimension und die Classification werden als zwei unterschiedliche Dimensionen behandelt. | Media Start, Media Close | `a.media.length` |
| Inhaltsname (Variable) | Der Anzeigename des Inhalts. Es ist auch eine Classification mit dem Namen &quot;Videoname&quot;verfügbar, die einen ähnlichen Zweck bietet. Diese Dimension und die Classification werden als zwei unterschiedliche Dimensionen behandelt. | Media Start, Media Close | `a.media.friendlyName` |
| Name des Inhaltsplayers | Der Name des Inhaltsplayers. | Media Start, Media Close | `a.media.playerName` |
| Inhaltssegment | Das Intervall, das den Teil des Inhalts beschreibt, der in Minuten angezeigt wurde. Das Segment wird als Mindest- und Höchstwert der Werte der Abspielleiste bei einer Wiedergabesitzung berechnet. | Media Close | `a.media.segment` |
| Inhaltstyp | Der Inhaltstyp. Gültige Werte sind `song`, `podcast`, `audiobook`, `radio`, `VoD`, `Live`, `Linear`, `UGC`, `DVoD` oder ein benutzerdefinierter Wert. | Media Start, Media Close | `a.contentType` |
| Medienpfad | Der Pfad, den der Besucher zum Erreichen des Inhalts verwendet hat. | Medienstart | `a.media.path` |
| Stream-Typ | Stream-Typ. Gültige Werte sind `audio` und `video`. | Media Start, Media Close | `a.media.streamType` |

{style="table-layout:auto"}

Zusätzlich zu den oben genannten Dimensionen erstellt Adobe automatisch die folgenden Classification-Dimensionen. Sie müssen Classification-Daten hochladen, um Berichte anzuzeigen, die diese Dimensionen verwenden.

| Klassifizierungsname | Übergeordnete Dimension | Beschreibung |
| --- | --- | --- |
| Videolänge | Inhalt | Die maximale Länge (oder Dauer) des wiedergegebenen Inhalts in Sekunden. Metriken, die von der Inhaltsdauer abhängen, können diese Classification nicht verwenden. Sie müssen eine berechnete Metrik erstellen, um Metriken wie z. B. die Zielgruppe &quot;Durchschnittliche Minute&quot;mithilfe dieser Classification zu erhalten. |
| Videoname | Inhalt | Der Anzeigename des Inhalts. Dies ist das Classification-Äquivalent zum Inhaltsnamen (Variable). |

{style="table-layout:auto"}
