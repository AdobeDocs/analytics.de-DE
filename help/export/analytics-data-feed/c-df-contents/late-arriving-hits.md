---
title: Verspätete Treffer
description: Erfahren Sie, wie Daten-Feeds verspätete Treffer behandeln.
feature: Data Feeds
exl-id: c99a702b-2aaa-47a6-958a-1e5ab66961ba
source-git-commit: 4d0007d1a23a81f0d5ba60541b4f7b9ac7b00ace
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 21%

---

# Verspätete Treffer {#late-arriving-hits}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_datafeed_late_hits"
>title="Verspätete Treffer zulassen"
>abstract="Wählen Sie diese Option aus, um Daten einzubeziehen, die nach Abschluss der Datenverarbeitung im festgelegten Berichtszeitraum (normalerweise täglich oder stündlich) eingingen. Wenn diese Option aktiviert ist, untersucht ein Daten-Feed bei der Verarbeitung von Daten alle spät eingetroffenen Treffer und stapelt sie mit der nächsten gesendeten Daten-Feed-Datei."

<!-- markdownlint-enable MD034 -->

## Verstehen von spät eintreffenden Treffern

Historische Daten können nach Abschluss der Verarbeitung eines Daten-Feed-Auftrags für eine bestimmte Stunde oder einen bestimmten Tag eingehen, z. B. über Treffer mit Zeitstempel oder Datenquellen.

Normalerweise werden bei der Datenverarbeitung eines Daten-Feeds nur Daten innerhalb des Berichtsfensters (in der Regel die letzte Stunde oder der letzte Tag) beachtet. Wenn Daten nach der Verarbeitung innerhalb dieses Berichtsfensters durch einen Feed eingehen, werden diese Daten in keinen Daten-Feed mehr aufgenommen.

Wenn verspätet eintreffende Treffer aktiviert sind, ändert sich die Verarbeitungsmethode, um diese Daten einzuschließen. Jedes Mal, wenn ein Daten-Feed Daten verarbeitet, werden alle verspäteten Treffer, die eingetroffen sind, untersucht und in der nächsten gesendeten Daten-Feed-Datei in Batches aufgenommen.

## Verspätete Treffer aktivieren

Bevor Sie die Option zum Zulassen verspäteter Treffer für einen Daten-Feed aktivieren, beachten Sie Folgendes:

* Daten für verschiedene Tage werden häufig in Daten-Feeds angezeigt, wenn verspätete Treffer aktiviert sind. Stellen Sie sicher, dass die Plattform, die Sie zum Erfassen von Daten-Feeds verwenden, Daten aus verschiedenen Tagen in derselben Datei aufnehmen kann.
* Wenn eine Daten-Feed-Datei erneut verarbeitet wird, werden die in der Originaldatei enthaltenen verspäteten Treffer in die erneut verarbeitete Datei aufgenommen, wenn die Neuverarbeitung innerhalb der ersten 5 Tage erfolgt. Nach 5 Tagen werden verspätete Treffer nicht in die erneut verarbeitete Datei aufgenommen.

Sie können beim Erstellen oder Bearbeiten eines Daten-Feeds verspätete Treffer aktivieren, indem Sie die Option **[!UICONTROL Verspätete Treffer zulassen]** aktivieren, wie in [Erstellen eines Daten-Feeds](/help/export/analytics-data-feed/create-feed.md) beschrieben.
