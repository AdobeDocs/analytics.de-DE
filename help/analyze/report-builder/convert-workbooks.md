---
title: Alte Report Builder-Arbeitsmappen konvertieren
description: Erfahren Sie, wie Sie ältere Report Builder-Arbeitsmappen in die neue Report Builder migrieren und konvertieren. Folgen Sie den schrittweisen Anweisungen in diesem Migrationshandbuch, um Ihre Adobe Analytics-basierten Arbeitsmappen nahtlos zu konvertieren.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: ff9011b2-fc18-456f-81dc-151b9e4fccd2
source-git-commit: 9743d7ac2a6c7e63d7a6701e60d05683c5680d36
workflow-type: tm+mt
source-wordcount: '1179'
ht-degree: 0%

---

# Alte Report Builder-Arbeitsmappen konvertieren

Die alte Report Builder-Version wurde im Juni 2026 eingestellt. Sie sollten Ihre Arbeitsmappen von der alten Report Builder zur neuen Report Builder migrieren. Die neue Report Builder bietet eine praktische Möglichkeit, mit der veralteten Report Builder erstellte Arbeitsmappen schnell zu migrieren.

>[!IMPORTANT]
>
>Duplizieren Sie jede Arbeitsmappe und benennen Sie eine Version um, bevor Sie die alte Arbeitsmappe konvertieren. Dadurch wird sichergestellt, dass Sie immer eine Kopie der ursprünglichen alten Arbeitsmappe haben, falls Sie sie benötigen.


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Arbeitsmappen konvertieren](https://experienceleague.adobe.com/de/docs/analytics-learn/tutorials/exporting/report-builder/upgrade-and-reschedule-workbooks){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]


>[!NOTE]
>
>Um veraltete Arbeitsmappen zu konvertieren, müssen Sie zunächst [die neue Report Builder einrichten](/help/analyze/report-builder/report-builder-setup.md).


## Alte Arbeitsmappe öffnen

Um eine ältere Arbeitsmappe zu öffnen, haben Sie folgende Möglichkeiten:

* Öffnen Sie eine geplante ältere Arbeitsmappe auf der **[!UICONTROL Zeitplan]** im [Report Builder-Hub](report-builder-hub.md). Diese Aktion ist die bevorzugte Methode für geplante ältere Arbeitsmappen. Sie haben die Möglichkeit, den mit der alten Arbeitsmappe verknüpften Zeitplan zu verwenden, sobald Sie [die konvertierte alte Arbeitsmappe planen](#schedule-a-converted-legacy-workbook).

   1. Öffnen Sie [!DNL Excel] und wählen Sie ![AdobeLogoRedonWhite](/help/assets/icons/AdobeLogoRedOnWhite.svg) **[!UICONTROL Report Builder]** in der [!DNL Excel] aus.

   1. Wählen Sie **[!UICONTROL Anmelden]** aus und melden Sie sich bei Report Builder an.

   1. Wählen Sie **[!UICONTROL Zeitplan]** im [Report Builder-Hub](report-builder-hub.md).
   1. Wählen Sie die Registerkarte **[!UICONTROL Legacy]** aus. Auf der Registerkarte werden die von Ihnen erstellten Legacy-Report Builder-basierten geplanten Arbeitsmappen aufgelistet.

      ![Alte Arbeitsmappen](assets/upgrade-legacy-schedule.png)

   1. Wählen Sie ![SelectBox](/help/assets/icons/SelectBox.svg) die geplante Arbeitsmappe aus, die Sie konvertieren möchten, und klicken Sie auf ![Herunterladen](/help/assets/icons/Download.svg). Die Arbeitsmappe wird heruntergeladen und in einem neuen Fenster in [!DNL Excel] geöffnet. Sie können jetzt [die alte Report Builder-Arbeitsmappe konvertieren](#convert-a--workbook).


* Öffnen Sie eine ältere Arbeitsmappe direkt auf Ihrem lokalen Computer oder Netzwerk. Wenn Sie diese Methode verwenden, wird nicht angeboten, den Zeitplan zu verwenden, der möglicherweise mit der alten Arbeitsmappe verknüpft ist. <br/>Wenn die alte Arbeitsmappe in [!DNL Excel] geöffnet ist:

   1. Wählen Sie ![AdobeLogoRedOnWhite](/help/assets/icons/AdobeLogoRedOnWhite.svg) **[!UICONTROL Report Builder]** in der [!DNL Excel] Multifunktionsleiste aus.
   1. Wählen Sie **[!UICONTROL Anmelden]** aus und melden Sie sich bei Report Builder an.
   1. Konvertieren [&#x200B; dann die alte Arbeitsmappe](#convert-a-workbook).


## Alte Arbeitsmappe konvertieren

So konvertieren Sie eine veraltete Arbeitsmappe:

1. Nachdem Sie eine veraltete Arbeitsmappe geöffnet haben, erkennt die neue Report Builder, ob diese Arbeitsmappe [veraltete Report Builder](/help/analyze/legacy-report-builder/home.md)-Anfragen enthält.

   ![Screenshot des [!DNL Excel] Report Builder-Upgrade-Berichts mit Migrationsaktualisierung](assets/upgrade-workbook.png){zoomable="yes"}

1. Wenn eine oder mehrere ältere Anforderungen gefunden werden, klicken Sie im Dialogfeld **[!UICONTROL Arbeitsmappe aktualisieren]** auf **[!UICONTROL Aktualisieren]**, um die Arbeitsmappe zu aktualisieren.

   >[!NOTE]
   >
   >Sie müssen jede Anfrage einzeln aktualisieren. Massenaktualisierung wird nicht unterstützt.


1. Ein **[!UICONTROL Warnung]** wird angezeigt, das Sie bei einer Aktualisierung auf Änderungen an der Arbeitsmappe hinweist. Außerdem werden Sie aufgefordert, eine Sicherungskopie Ihrer alten Arbeitsmappe zu erstellen, bevor Sie fortfahren.

   ![Screenshot des [!DNL Excel] Report Builder-Upgrade-Berichts mit Migrationswarnung](assets/upgrade-warning.png){zoomable="yes"}

1. Klicken Sie **[!UICONTROL Fortfahren]**, um mit dem Upgrade fortzufahren.

   Wenn die Aktualisierung erfolgreich war, wird eine **[!UICONTROL Die Arbeitsmappen-Aktualisierung ist jetzt abgeschlossen]**-Benachrichtigung angezeigt.

   ![Screenshot des [!DNL Excel] Report Builder-Upgrade-Berichts mit abgeschlossener Migration](assets/upgrade-complete.png)

   * Wählen Sie **[!UICONTROL Schließen]** aus, um die Benachrichtigung zu schließen und weiterhin in der Arbeitsmappe mit aktualisierten Anfragen für die neue Report Builder zu arbeiten.

   * Wählen Sie **[!UICONTROL Aktualisierungsbericht herunterladen]** aus, um eine neue [!DNL Excel] Arbeitsmappe mit dem Ergebnis der Aktualisierung herunterzuladen und zu öffnen. Ein Beispiel finden Sie unten.

     ![Screenshot des [!DNL Excel] Report Builder-Upgrade-Berichts mit dem Migrationsbericht](assets/upgrade-report.png)

Sie können [&#x200B; Datenblöcke in &#x200B;](/help/analyze/report-builder/manage-reportbuilder.md) Arbeitsmappe verwalten. Diese Datenblöcke sind das Ergebnis des Upgrades und ersetzen Ihre veralteten Report Builder-Anfragen.


## Planen einer konvertierten Legacy-Arbeitsmappe

Sie haben die Möglichkeit, die Zeitplandetails aus der alten Arbeitsmappe zu verwenden, die Sie heruntergeladen und auf der Registerkarte **[!UICONTROL Zeitplan]** im Report Builder-Hub geöffnet haben. Diese Option ist nicht für ältere Arbeitsmappen mit Zeitplandetails verfügbar, die Sie über Ihren lokalen Computer oder Ihr Netzwerk öffnen.

1. So planen Sie eine konvertierte veraltete Arbeitsmappe mit einem veralteten Zeitplan:

   * Wählen Sie **[!UICONTROL Arbeitsmappe senden]** über den Report Builder-Hub aus oder
   * Wählen Sie **[!UICONTROL Arbeitsmappe planen]** auf der Registerkarte **[!UICONTROL Arbeitsmappen]** aus, die auf der Registerkarte **[!UICONTROL Zeitpläne]** in Report Builder verfügbar ist.

1. Sie erhalten die Möglichkeit, die Zeitplandetails aus der alten Arbeitsmappe als Standardzeitplaneinstellungen zu verwenden.

   ![Screenshot der [!DNL Excel] Optionen für ältere Report Builder-Zeitplaneinstellungen](assets/upgrade-legacy-schedule-convert.png)

   * Wählen Sie **[!UICONTROL Verwenden]** aus, um die Details des alten Zeitplans zu verwenden. Die Zeitplandetails werden vorab in der Benutzeroberfläche [Arbeitsmappe senden](schedule-reportbuilder.md#schedule-a-workbook) ausgefüllt.
   * Wählen Sie **[!UICONTROL Nicht verwenden]** aus, um nicht die Details des alten Zeitplans zu verwenden.
   * Wählen Sie zum Abbrechen **[!UICONTROL Abbrechen]** aus.

   Wählen Sie **[!UICONTROL Alte Metadaten aus der zukünftigen Verwendung entfernen]** aus, um die Details des alten Zeitplans für diese Arbeitsmappe in Zukunft nicht zu verwenden.


## Migration von Legacy Report Builder

Einige Funktionen der alten Report Builder werden in Report Builder nicht unterstützt, teilweise unterstützt oder anders implementiert:

* **Echtzeit-Anfragen**. Echtzeit-Anfragen werden nicht unterstützt und aus der konvertierten alten Arbeitsmappe entfernt.

* **Pfad-/Fallout-**. Fallout-Anfragen werden nicht unterstützt und aus der konvertierten veralteten Arbeitsmappe entfernt.

* **[!DNL FTP]Option für terminierte Berichte**. Die Option zum Planen von Berichten für den Versand an einen [!DNL FTP] ist nicht mehr verfügbar.

* **Option Arbeitsmappe in [!DNL Power BI] veröffentlichen für terminierte Berichte**. Die Option zum Planen von Berichten für [!DNL Power BI] ist nicht mehr verfügbar.

* **Besuchermetriken**. Die folgenden Metriken werden in *konvertierten veralteten Arbeitsmappe in* Unique Visitors“ konvertiert, auch wenn das Berichtsergebnis möglicherweise keine exakte Übereinstimmung aufweist: `visitorshourly`, `visitorsdaily`, `visitorsweekly`, `visitorsmonthly`, `visitorsquarterly` und `visitorsyearly`. Diese Konversion gilt auch für `mobilevisitorshourly`, `mobilevisitorsdaily`, `mobilevisitorsweekly`, `mobilevisitorsmonthly`, `mobilevisitorsquarterly` und `mobilevisitorsyearly`.

* **Automatische erneute**. Wenn Sie eine neue [!DNL Excel] öffnen, müssen Sie sich explizit erneut authentifizieren. Diese erneute Authentifizierung ist eine Sicherheitsfunktion [!DNL Office Add-ins] Funktionalität.

* **Kopieren Sie ein Arbeitsblatt mit einer Gruppe von Datenblöcken**. So unterstützen Sie die Kopie eines Arbeitsblatts, das mehr als einen Datenblock enthält:

   1. Wählen Sie die Registerkarte Arbeitsblatt in der [!DNL Excel] Arbeitsmappe aus, die Sie kopieren möchten.
   1. Wählen Sie im Kontextmenü der Registerkarte die Option **[!UICONTROL Verschieben oder Kopieren…]**
   1. Im Dialogfeld **[!UICONTROL Verschieben oder Kopieren]**:
      1. Wählen Sie aus, wohin das kopierte Arbeitsblatt kopiert werden soll.
      1. Stellen Sie sicher, **[!UICONTROL Sie „Kopie erstellen]** aktivieren.
      1. Klicken Sie **[!UICONTROL OK]**.
   1. Aus dem Quellarbeitsblatt:
      1. Wählen Sie den Zellenbereich aus, der alle Datenblöcke umfasst.
      1. Wählen Sie ![Kopieren](/help/assets/icons/Copy.svg) **[!UICONTROL Datenblock kopieren]** aus dem [Report Builder-Hub](/help/analyze/report-builder/report-builder-hub.md).
   1. Im Zielarbeitsblatt:
      1. Wählen Sie die Zelle aus, in die der kopierte Zellbereich eingefügt werden soll.
      1. Wählen Sie ![Einfügen](/help/assets/icons/Paste.svg) **[!UICONTROL Datenblock einfügen]** aus dem [Report Builder-Hub](/help/analyze/report-builder/report-builder-hub.md).

* **Datumsbereich**. Report Builder migriert die Formatierungsoptionen für Datumsbereiche (Anfangs- und Endperiode anzeigen **[!UICONTROL ) nicht]** einer Zeilenbeschriftung für einen Datumsbereich in der veralteten Report Builder.

* **Durchschnitt**. Report Builder migriert die ausgewählte Formatierungsoption **[!UICONTROL Durchschnittsoptionen]** (**[!UICONTROL Tagesdurchschnitt]** bis **[!UICONTROL Jahresdurchschnitt]**), die auf eine Metrik in der veralteten Report Builder angewendet wird, nicht. Ersetzen Sie die ausgewählte Option durch eine berechnete Metrik.

* **Text voranstellen/**. Report Builder migriert den **[!UICONTROL Text voranstellen/verschieben]** der auf eine Metrik in der alten Report Builder angewendet wird, nicht.

* **Zwischensummen**. Report Builder migriert die Formatierungsoption **[!UICONTROL SubTotal(diese Anfrage)]** nicht, die auf eine Metrik in der veralteten Report Builder angewendet wurde. Wenn Sie **[!UICONTROL SubTotal(diese Anfrage)]** in einer veralteten Arbeitsmappen-Anfrage verwendet haben, wird die Funktion in &quot;**[!UICONTROL &quot;]**. Beispiel: in einem Legacy-Datenblock mit den fünf häufigsten Seitennamen, in dem Sie **[!UICONTROL Zwischensumme(Seitenansichten)]** verwendet haben, um die Summe der Seitenansichten für die fünf häufigsten Seitennamen zurückzugeben. Nach der Migration gibt derselbe Datenblock mit den fünf häufigsten Seitennamen die Summe der Seitenansichten für *alle“* zurück. Verwenden Sie die Funktion „Berechnete Metriken“, um die alte Funktion **[!UICONTROL Zwischensumme]** zu ersetzen.
