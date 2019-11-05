---
description: Der Reiter „Nutzung der Report Suite“ bietet Daten über die Server-Nutzung jeder Report Suite aller Anmeldeunternehmen innerhalb der aktuellen Nutzungsperiode, die mit Ihrem Abrechnungsunternehmen zusammenhängen.
seo-description: Der Reiter „Nutzung der Report Suite“ bietet Daten über die Server-Nutzung jeder Report Suite aller Anmeldeunternehmen innerhalb der aktuellen Nutzungsperiode, die mit Ihrem Abrechnungsunternehmen zusammenhängen.
seo-title: Nutzung der Report Suite anzeigen
title: Nutzung der Report Suite anzeigen
uuid: c609ed99-9acc-4023-905a-81a40dd07a79
translation-type: tm+mt
source-git-commit: 8c4c368a84ba5499d85f0b7512c99de47ddb14c2

---


# Nutzung der Report Suite anzeigen

Der Reiter „Nutzung der Report Suite“ bietet Daten über die Server-Nutzung jeder Report Suite aller Anmeldeunternehmen innerhalb der aktuellen Nutzungsperiode, die mit Ihrem Abrechnungsunternehmen zusammenhängen.

**[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; Verwendung **[!UICONTROL des]** Server-Aufrufs &gt; **[!UICONTROL Report Suite-Nutzung]**

>[!IMPORTANT]
>
>If a report suite is not [linked to an Experience Cloud Organization](https://marketing.adobe.com/resources/help/en_US/mcloud/report-suite-mapping.html), its usage data will not be reflected in this dashboard. Außerdem kann eine Abrechnungs-ID mit mehreren Experience Cloud-Organisationen zusammenhängen. Das Verhältnis zwischen einer Organisation und einer Abrechnungs-ID ist nicht immer 1:1.

Das Dashboard zur Nutzung der Report Suite

* Zeigt die Nutzung der Server-Aufrufe für die aktuelle Nutzungsperiode (alle Aufrufe, primär, sekundär, primär mobil, sekundär mobil) für alle Report Suits innerhalb Ihrer Experience Cloud-Organisation an.
* Zeigt den Anteil der Gesamtnutzung pro Server-Aufruf-Kategorie an.
* Wird täglich aktualisiert.
* Kann heruntergeladen werden.
* Lässt Sie auf die Nutzeroberfläche **[!UICONTROL Warnhinweise verwalten]zugreifen.**

![](assets/report-suite-usage.png)

| Spalte | Definition |
|--- |--- |
| Name der Report Suite | Anzeigename der Report Suite |
| Alle Aufrufe (% der Gesamtzahl) | Alle Server-Aufrufe, die innerhalb der aktuellen Nutzungsperiode erfolgt sind. |
| Primäre Aufrufe (%) | Alle primären Server-Aufrufe (und ihr Anteil an der Gesamtzahl), die innerhalb der aktuellen Nutzungsperiode erfolgt sind. |
| Sekundäre Aufrufe (%) | Alle sekundären Server-Aufrufe (und ihr Anteil an der Gesamtzahl), die innerhalb der aktuellen Nutzungsperiode erfolgt sind. |
| Primäre mobile Aufrufe (%) | Alle primären mobilen Server-Aufrufe (und ihr Anteil an der Gesamtzahl), die innerhalb der aktuellen Nutzungsperiode erfolgt sind. |
| Sekundäre mobile Aufrufe (%) | Alle sekundären mobilen Server-Aufrufe (und ihr Anteil an der Gesamtzahl), die innerhalb der aktuellen Nutzungsperiode erfolgt sind. |


## Nutzungsbericht herunterladen {#section_D7345660B5E043CD8850954216509A3D}

Mit dieser Option können Sie Nutzungsdaten und Daten aus Zeiträumen vor der aktuellen Nutzungsperiode herunterladen (bis Januar 2015). Der Bericht wird als .csv-Datei heruntergeladen.

1. Wählen Sie mindestens eine Report Suite aus.
1. Klicken Sie auf **[!UICONTROL Bericht herunterladen]**.

   ![](assets/download_report.png)

| Berichtselement | Beschreibung |
|--- |--- |
| Dateiname | Hartkodierter Name: Nutzungsbericht `day and time of report creation.csv` |
| Enthaltene Report Suites | Diese Liste enthält jegliche Report Suites, die Sie auf der „Nutzung der Report Suite“-Seite ausgewählt haben. |
| Enthaltene Aufrufarten | Legen Sie eine beliebige Kombination aus Folgendem fest: Alle Aufrufe (Standard), Primär, Sekundär, Primär mobil, Sekundär mobil. |
| Zeitraum | Sie können die aktuelle Nutzungsperiode auswählen oder selbst einen Zeitraum definieren.  Wenn Sie selbst einen Zeitraum definieren möchten, dann geben Sie bitte einen Beginn des Zeitraums und ein Ende des Zeitraums ein. <br>**** Hinweis: Sie können keine Nutzungsdaten vor Januar 2015 herunterladen </br>. |

1. Klicken Sie auf **[!UICONTROL Herunterladen]**.

Im Folgenden finden Sie einen Screenshot, wie die heruntergeladene .csv-Datei aussieht. Es enthält eine Spalte für die Report Suite-ID. Die Report Suite-ID gibt eine eindeutige ID an, die nur alphanumerische Zeichen enthalten darf. Diese ID kann nach der Erstellung einer Report Suite nicht mehr geändert werden.

![](assets/download-usage.png)
