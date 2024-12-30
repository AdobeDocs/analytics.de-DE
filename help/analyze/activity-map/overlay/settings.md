---
description: Das Activity Map-Einstellungsbedienfeld ermöglicht es Ihnen, die Einstellungen und Eigenschaften für alle Arten von Überlagerungsvisualisierungen zu ändern.
title: Activity Map-Einstellungen konfigurieren
uuid: 42a0309e-3efc-4506-989b-09b6fe419423
feature: Activity Map
role: User, Admin
exl-id: 65c9c690-81e0-4f0f-989d-586d247ed380
source-git-commit: ba10ceb73d953ff495613d02dd1ff825b6e518df
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 48%

---

# Activity Map-Einstellungen konfigurieren

Das Activity Map-Einstellungsbedienfeld ermöglicht es Ihnen, die Einstellungen und Eigenschaften für alle Arten von Überlagerungsvisualisierungen zu ändern.

Rufen Sie das Activity Map-Einstellungsbedienfeld durch Klicken auf das Zahnradsymbol in der Activity Map-Symbolleiste auf.

## Allgemeine Einstellungen {#section_697A12F099494D699A4BF498598178C5}

| Einstellung | Beschreibung |
| --- | --- |
| **[!UICONTROL Unternehmen]** | Wählen Sie das entsprechende Anmeldeunternehmen aus. |
| **[!UICONTROL Report Suite]** | Die für Sie verfügbare Liste mit Report Suites ist nicht mehr beschränkt auf die im Web-Seiten-Tag definierten Report Suites. Sie können nun die ausgewählte Report Suite (die zu einem der Tags auf der Seite gehört) durch eine andere Report Suite ersetzen. Diese neue Report Suite muss nicht mit einem Tag auf der Seite verbunden sein. Wenn Sie die ausgewählte Report Suite in den Activity Map-Einstellungen ändern, werden alle betroffenen Analytics-Berichte durch den Speichervorgang aktualisiert.<br>**Wichtig**: [!UICONTROL Virtual Report Suites] sind nicht mit [!UICONTROL Live-Modus], sondern nur mit [!UICONTROL Standardmodus]. Wenn Sie sich im [!UICONTROL Live-Modus] für eine Standard-Report Suite befinden, aber eine [!UICONTROL Virtual Report Suite] in diesem Dialogfeld auswählen, wird nach Klicken **[!UICONTROL OK]** hier der Standardmodus angezeigt. Darüber hinaus wird das Calendar-Steuerelement entsprechend dem Kalendertyp der Report Suite (Gregorianisch, Einzelhandel, benutzerdefiniert usw.) neu initialisiert. |
| **[!UICONTROL Seitenname]** | Die Seite, für die diese Einstellungen gelten. |
| **[!UICONTROL Sprache]** | Die Auswahl entspricht den angebotenen Sprachen für Adobe Analytics. |
| **[!UICONTROL Overlays bezeichnen als]** | <ul><li>**[!UICONTROL Kein Label]**: nur für Verlaufsüberlagerungen In diesem Fall vermittelt die Farbe der Überlagerung ein Gefühl für die Rangfolge des Links</li><li>**[!UICONTROL Wert]**: Der unverarbeitete Gesamtwert der Metrik für den Link</li><li>**[!UICONTROL Prozent]**: Prozentsatz der Metrik für diesen Link im Vergleich zum Gesamtwert der Metrik für die Seite.</li><li>**[!UICONTROL Rang]**: Rang dieses Links im Vergleich zu allen Links auf der gerenderten Seite</li></ul> |
| **[!UICONTROL Schriftgröße Beschriftung]** | Ermöglicht Ihnen, die Schriftgröße der Überlagerungsbeschriftung zur besseren Lesbarkeit mithilfe eines Reglers zu erhöhen oder zu verringern. |
| **[!UICONTROL Verlauf/Bläschenfarbe]** | Um Überlagerungslink-Rankings für Visualisierungen von Verlauf oder Blasen-Überlagerung anzuzeigen, wählen Sie aus einem Farbbereich aus. |
| **[!UICONTROL Farbverlauf auf Grundlage von]** | <ul><li>**[!UICONTROL Top-30-Bewertungen]**: Die Farbintensität wird für die 30 höchsten Werte vereinheitlicht.</li><li>**[!UICONTROL Absoluter Metrikwert]**: Die Farbintensität ist eine Funktion des absoluten Metrikwerts.</li></ul> |
| **[!UICONTROL Verlaufstransparenz]** | Wählen Sie die Transparenzstufe für die Farbverlaufsüberlagerungen aus. Diese Einstellung hat keine Auswirkungen auf die [!UICONTROL Bubble]-Überlagerungen. |

## Standardeinstellungen {#section_24DB95376E1A448494ECF3F57743FC19}

Diese Einstellungen gelten für die Überlagerung im Standardmodus.

| Einstellung | Beschreibung |
| --- | --- |
| **[!UICONTROL Dynamische Datenfilterung]** | In dieser Dropdown-Liste können Sie Überlagerungen anzeigen für<ul><li>(Standard) Alle Links auf der Seite</li><li>Die obere (höchste) oder untere (niedrigste) Anzahl von Rangfolgen-Links auf der Seite, wobei # eine Auswahl von 1, 10, 50 oder 100 sein kann.</li></ul> |
| **[!UICONTROL Überlagerungen für Links ausblenden, die keine Treffer erhalten haben]**. | Ein Kontrollkästchen, das die Sichtbarkeit von Überlagerungen für Links umschaltet, die keine Daten enthalten.<ul><li>(Standard) Wenn das Kontrollkästchen aktiviert ist, wird keine Überlagerung angezeigt, wenn ein Link keine ActivityMap-Linkdaten hat.</li><li>Wenn das Kontrollkästchen deaktiviert ist und ein Link keine ActivityMap-Link-Daten hat, wird eine Überlagerung angezeigt und sie hat die Kennzeichnung &quot;-&quot;, was bedeutet: Nicht zutreffend. |

## Live-Einstellungen {#section_D30F6E62FB5D404090B588F396A460AF}

Diese Einstellungen gelten für die Live-Modus-Überlagerung.

| Einstellung | Beschreibung |
|---|---|
| **[!UICONTROL Anzeige oben]** | Um die **[!UICONTROL Gewinner]** oder **[!UICONTROL Verlierer]** (oder beide) als Überlagerungen anzuzeigen, wählen Sie die Anzahl der Links aus. |
| **[!UICONTROL Unterste ausschließen (%)]** | Wählen Sie diese Option, um Links für Gewinner oder Verlierer auszuschließen, für die wenig Daten vorhanden sind. Wenn Sie diesen Prozentsatz der Links ausschließen, werden nur noch die Links angezeigt, für die genug Daten vorhanden sind, um relevante Gewinne oder Verluste anzuzeigen. Der Prozentsatz wird anhand der Anzahl der Links auf der Seite berechnet. Wenn Sie beispielsweise die unteren 10 % einer Liste mit 200 Links herausfiltern, werden die unteren 20 Links herausgefiltert. |
| **[!UICONTROL Automatische Aktualisierung von Daten]** | Hiermit können Sie entscheiden, ob die in der Benutzeroberfläche angezeigten Analytics-Daten automatisch aktualisiert werden, wenn ein neuer Zeitraum berechnet wird. |
| **[!UICONTROL Zeitraum für automatische Aktualisierung]** | Wenn dieses Kontrollkästchen aktiviert wird, wird die Webseite jedes Mal aktualisiert, wenn neue Daten abgerufen werden. Dadurch können die Links auf der Seite genauer mit den erfassten Daten synchronisiert werden. |
