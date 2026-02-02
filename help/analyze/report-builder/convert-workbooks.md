---
title: Alte Report Builder-Arbeitsmappen konvertieren
description: Erfahren Sie, wie Sie Ihre veralteten Report Builder-basierten Arbeitsmappen für die Verwendung der neuen Report Builder konvertieren.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: ff9011b2-fc18-456f-81dc-151b9e4fccd2
source-git-commit: d7832dc56eb680f57a6875cf32e29fd5a8858098
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 1%

---

# Alte Report Builder-Arbeitsmappen konvertieren

Im Rahmen der Umstellung auf eine neue Report Builder-Funktion können Sie Ihre aktuellen veralteten Report Builder-basierten Arbeitsmappen (veraltete Arbeitsmappen) schnell konvertieren, um die neue Report Builder-Funktion [Datenblöcke](create-a-data-block.md) zu verwenden.

>[!IMPORTANT]
>
>Duplizieren Sie jede Arbeitsmappe und benennen Sie eine Version um, bevor Sie die alte Arbeitsmappe konvertieren. Dadurch wird sichergestellt, dass Sie immer eine Kopie der ursprünglichen alten Arbeitsmappe haben, falls Sie sie benötigen.


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Arbeitsmappen konvertieren](https://video.tv.adobe.com/v/3446191?captions=ger&quality=12&learn=on){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]


>[!NOTE]
>
>Um veraltete Arbeitsmappen zu konvertieren, müssen Sie zunächst [die neue Report Builder einrichten](/help/analyze/report-builder/report-builder-setup.md).


## Alte Arbeitsmappe öffnen

Um eine ältere Arbeitsmappe zu öffnen, haben Sie folgende Möglichkeiten:

* Öffnen Sie eine ältere Arbeitsmappe direkt auf Ihrem lokalen Computer oder Netzwerk. Wenn die alte Arbeitsmappe in Excel geöffnet ist:

   1. Wählen Sie ![AdobeLogoRedonWhite](/help/assets/icons/AdobeLogoRedOnWhite.svg) **[!UICONTROL Report Builder]** in der Excel-Multifunktionsleiste aus.
   1. Wählen Sie **[!UICONTROL Anmelden]** aus und melden Sie sich bei Report Builder an.
   1. Konvertieren [&#x200B; dann die alte Arbeitsmappe](#convert-a-workbook).

* Öffnen Sie eine geplante ältere Arbeitsmappe auf der **[!UICONTROL Zeitplan]** im [Report Builder-Hub](report-builder-hub.md). Gehen Sie dazu wie folgt vor:

   1. Öffnen Sie Excel und wählen Sie ![AdobeLogoRedonWhite](/help/assets/icons/AdobeLogoRedOnWhite.svg) **[!UICONTROL Report Builder]** in der Excel-Multifunktionsleiste aus.

   1. Wählen Sie **[!UICONTROL Anmelden]** aus und melden Sie sich bei Report Builder an.

   1. Wählen Sie **[!UICONTROL Zeitplan]** im [Report Builder-Hub](report-builder-hub.md).
   1. Wählen Sie die Registerkarte **[!UICONTROL Legacy]** aus. Auf der Registerkarte werden die veralteten, auf Report Builder basierenden geplanten Arbeitsmappen aufgeführt.

      ![Alte Arbeitsmappen](assets/upgrade-legacy-schedule.png)

   1. Wählen Sie ![SelectBox](/help/assets/icons/SelectBox.svg) die geplante Arbeitsmappe aus, die Sie konvertieren möchten, und klicken Sie auf ![Herunterladen](/help/assets/icons/Download.svg). Die Arbeitsmappe wird heruntergeladen und in einem neuen Fenster in Excel geöffnet. Sie können jetzt [die alte Report Builder-Arbeitsmappe konvertieren](#convert-a--workbook).


## Alte Arbeitsmappe konvertieren

So konvertieren Sie eine veraltete Arbeitsmappe:

1. Nachdem Sie eine veraltete Arbeitsmappe geöffnet haben, erkennt die neue Report Builder, ob diese Arbeitsmappe [veraltete Report Builder](/help/analyze/legacy-report-builder/home.md)-Anfragen enthält.

   ![Arbeitsmappen-Eingabeaufforderung aktualisieren](assets/upgrade-workbook.png){zoomable="yes"}

1. Wenn eine oder mehrere ältere Anforderungen gefunden werden, klicken Sie im Dialogfeld **[!UICONTROL Arbeitsmappe aktualisieren]** auf **[!UICONTROL Aktualisieren]**, um die Arbeitsmappe zu aktualisieren.

   >[!NOTE]
   >
   >Sie müssen jede Anfrage einzeln aktualisieren. Massenaktualisierung wird nicht unterstützt.


1. Ein **[!UICONTROL Warnung]** wird angezeigt, das Sie bei einer Aktualisierung auf Änderungen an der Arbeitsmappe hinweist. Außerdem werden Sie aufgefordert, eine Sicherungskopie Ihrer alten Arbeitsmappe zu erstellen, bevor Sie fortfahren.

   ![Upgrade-Warnung](assets/upgrade-warning.png){zoomable="yes"}

1. Klicken Sie **[!UICONTROL Fortfahren]**, um mit dem Upgrade fortzufahren.

   Wenn die Aktualisierung erfolgreich war, wird eine **[!UICONTROL Die Arbeitsmappen-Aktualisierung ist jetzt abgeschlossen]**-Benachrichtigung angezeigt.

   ![Upgrade abgeschlossen](assets/upgrade-complete.png)

   * Wählen Sie **[!UICONTROL Schließen]** aus, um die Benachrichtigung zu schließen und weiterhin in der Arbeitsmappe mit aktualisierten Anfragen für die neue Report Builder zu arbeiten.

   * Wählen Sie **[!UICONTROL Aktualisierungsbericht herunterladen]**, um eine neue Excel-Arbeitsmappe mit dem Ergebnis der Aktualisierung herunterzuladen und zu öffnen. Ein Beispiel finden Sie unten.

     ![Excel Report Builder Upgrade Report-Arbeitsmappe](assets/upgrade-report.png)

Sie können [den Datenblock verwalten](/help/analyze/report-builder/manage-reportbuilder.md).


## Planen einer konvertierten Legacy-Arbeitsmappe

Sie haben die Möglichkeit, die Zeitplandetails aus der alten Arbeitsmappe zu verwenden, die Sie heruntergeladen und auf der Registerkarte **[!UICONTROL Zeitplan]** im Report Builder-Hub geöffnet haben. Diese Option ist nicht für ältere Arbeitsmappen mit Zeitplandetails verfügbar, die Sie über Ihren lokalen Computer oder Ihr Netzwerk öffnen.

1. Arbeitsmappe planen. So planen Sie eine konvertierte veraltete Arbeitsmappe mit einem veralteten Zeitplan:

   * Wählen Sie **[!UICONTROL Arbeitsmappe senden]** über den Report Builder-Hub aus oder
   * Wählen Sie **[!UICONTROL Arbeitsmappe planen]** auf der Registerkarte **[!UICONTROL Arbeitsmappen]** aus, die auf der Registerkarte **[!UICONTROL Zeitpläne]** in Report Builder verfügbar ist.

1. Sie erhalten die Möglichkeit, die Zeitplandetails aus der alten Arbeitsmappe als Standardzeitplaneinstellungen zu verwenden.

   ![Migrieren eines alten Arbeitsmappen-Zeitplans](assets/upgrade-legacy-schedule-convert.png)

   * Wählen Sie **[!UICONTROL Verwenden]** aus, um die Details des alten Zeitplans zu verwenden. Die Zeitplandetails werden vorab in der Benutzeroberfläche [Arbeitsmappe senden](schedule-reportbuilder.md#schedule-a-workbook) ausgefüllt.
   * Wählen Sie **[!UICONTROL Nicht verwenden]** aus, um nicht die Details des alten Zeitplans zu verwenden.
   * Wählen Sie zum Abbrechen **[!UICONTROL Abbrechen]** aus.

   Wählen Sie **[!UICONTROL Alte Metadaten aus der zukünftigen Verwendung entfernen]** aus, um die Details des alten Zeitplans für diese Arbeitsmappe in Zukunft nicht zu verwenden.


## Alte Report Builder-Funktionen werden nicht unterstützt {#unsupported}

Einige alte Report Builder-Funktionen sind in der neuen Report Builder nicht mehr verfügbar

* Echtzeit-Anfragen.

* Pfad-/Fallout-Berichte

* FTP-Option für terminierte Berichte.

* Besuchermetriken. Die folgenden Metriken werden in *Unique Visitors* konvertiert, auch wenn das Berichtsergebnis möglicherweise nicht genau übereinstimmt: `visitorshourly`, `visitorsdaily`, `visitorsweekly`, `visitorsmonthly`, `visitorsquarterly` und `visitorsyearly`. Diese Konversion gilt auch für `mobilevisitorshourly`, `mobilevisitorsdaily`, `mobilevisitorsweekly`, `mobilevisitorsmonthly`, `mobilevisitorsquarterly` und `mobilevisitorsyearly`.
