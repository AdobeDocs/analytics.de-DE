---
description: Erfahren Sie, wie Sie Ihren Bericht benennen und konfigurieren, wie Sie Zeilen- und Spaltenüberschriften anzeigen.
title: Formatieren von Anzeigekopfzeilen
uuid: cd0e167b-9463-43fd-87b2-724d1c79de68
feature: Report Builder
role: User, Admin
exl-id: 168daa6b-965c-4f8b-97b7-651a7ad55d6c
source-git-commit: fcecc8a493852f5682fd7fbd5b9bb484a850922c
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 71%

---

# Anzeigeüberschriften formatieren

{{legacy-arb}}

Sie können Ihrem Bericht einen Namen geben und konfigurieren, wie die Zeilen- und Spaltenüberschriften angezeigt werden. Der Link „Formatoptionen“ ist für die Layouttypen „Pivot“ und „Benutzerdefiniert“ verfügbar.

1. Erstellen Sie im Dialogfeld [!UICONTROL Anforderungs-Assistent: Schritt 1] eine Anforderung.
1. Klicken Sie auf **[!UICONTROL Weiter]**.
1. Fügen Sie der Anforderung im Dialogfeld [!UICONTROL Anforderungs-Assistent: Schritt 2] Dimensionen und Metriken entsprechend Ihren Bedürfnissen hinzu.
1. Klicken Sie auf **[!UICONTROL Formatoptionen]**.
1. Konfigurieren Sie [!UICONTROL die Anzeigeoptionen]:

   | Element | Beschreibung |
   |--- |--- |
   | Berichtsname | Zeigt entweder den Namen des Berichtstyps an, der über den Baum in Schritt 1 des Berichtsassistenten ausgewählt wurde (z. B. [!DNL Traffic Report]), oder den im Feld [!DNL Name this Request] eingegebenen Namen. |
   | Filtert Parameter | Zeigt die Dimensionsfilter wie beispielsweise Suchfilter an |
   | Segment | Zeigt die Segmentparameter an |
   | Datenaktualität | Zeigt die Parameter für Datenaktualität an Beispiel:    Datenaktualität: Seitenansichten (vor 1,5 Stunden), Ausstiege (vor 30 Minuten) Weitere Informationen zur aktuellen Datenverarbeitung finden [ unter ](/help/analyze/legacy-report-builder/options.md). |

   Anzeigereihefolge: Wenn im [!UICONTROL Zeilentitel] (Schritt 2) ein Element enthalten ist, wird dies in der Anforderung zuerst angezeigt. Falls nicht, verwendet das System das erste vorhandene Element im Raster [!UICONTROL Spaltenbezeichnung]. Falls weder Zeilen- oder Spaltenelemente vorhanden sind, wird das erste Element im Raster [!UICONTROL Metriken] angezeigt.

   **Zeilen- und Spaltenüberschriften anzeigen:** Fügt eine Zeile und Spalte zur Anzeige dieser Elemente hinzu.

   In Version 3.11 konnte man eine Überschrift für jedes einzelne Element anzeigen. In Version 4 werden diese Elemente entweder alle oder gar nicht angezeigt. Wenn Sie eine Anfrage in Version 3.11 erstellt und in Version 4.x geöffnet haben, fordert Sie der Report Builder in Schritt 2 auf, den Bereich für Elemente, denen eine Kopfzeile fehlt, um eine Zelle zu aktualisieren.

   **Überschriften in automatische Filterung von Excel ändern:** Nur verfügbar, wenn Zeilen- und Spaltenüberschriften angezeigt werden. Diese Einstellung erstellt einen automatischen Excel-Filter und hängt ihn an den Daten-Report Builder an, der für diese Anfrage zurückgibt.

   >[!NOTE]
   >
   >Excel unterstützt nur einen einzigen automatischen Filter pro Arbeitsblatt. Wenn Sie einen neuen automatischen Filter in einem Arbeitsblatt erstellen, das bereits einen automatischen Filter enthält, gibt Excel keine Warnung aus, dass der vorhandene automatische Filter ersetzt wird.

   **Automatische Kontur durchführen:** Wandelt das vom Report Builder zurückgegebene Datum von einer Listenansicht in eine Baumstrukturansicht um.

   **Diese Anforderung benennen:** Hier können Sie einen benutzerdefinierten Namen für die Anforderung eingeben oder den in Schritt 1 ausgewählten Standardnamen verwenden. Dieser Name wird als [!UICONTROL Berichtname] im [!UICONTROL Anforderungs-Manager] angezeigt. Siehe [Benennen einer Anfrage](/help/analyze/legacy-report-builder/layout/name-a-request.md).

1. Klicken Sie auf **[!UICONTROL OK]**.
