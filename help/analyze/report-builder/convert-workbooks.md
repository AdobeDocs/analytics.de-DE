---
title: So konvertieren Sie ältere Report Builder-Arbeitsmappen in Datenblöcke
description: Beschreibt, wie ältere Anfragen in Datenblöcke konvertiert werden
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: ff9011b2-fc18-456f-81dc-151b9e4fccd2
source-git-commit: 08e29da4847e8ef70bd4435949e26265d770f557
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 22%

---

# Alte Report Builder-Arbeitsmappen in Datenblöcke konvertieren

Im Zuge der Umstellung auf eine neue Report Builder-Technologie können Sie Ihre aktuellen alten Arbeitsmappen schnell in JavaScript-basierte Arbeitsmappen konvertieren.

>[!IMPORTANT]
>
>Duplizieren Sie jede Arbeitsmappe und benennen Sie eine Version um, bevor Sie sie konvertieren. Auf diese Weise haben Sie immer noch eine Kopie der ursprünglichen Arbeitsmappe, falls Sie sie benötigen sollten.


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Arbeitsmappen konvertieren](https://video.tv.adobe.com/v/3434957?quality=12&learn=on){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]



1. Richten Sie die neue Report Builder ein[&#x200B; indem Sie die folgenden Anweisungen &#x200B;](/help/analyze/report-builder/report-builder-setup.md).

1. Öffnen Sie Excel und klicken Sie oben rechts auf das Adobe Report Builder-Symbol .

1. Klicken Sie **[!UICONTROL &quot;]**&quot; und melden Sie sich bei Report Builder an.

1. Das Report Builder-Add-in erkennt, ob diese Arbeitsmappe [veraltete Report Builder](/help/analyze/legacy-report-builder/home.md)-Anfragen enthält.

   ![Arbeitsmappen-Eingabeaufforderung aktualisieren](assets/upgrade_workbook.png)

1. Wenn eine oder mehrere ältere Anforderungen gefunden werden, klicken Sie auf **[!UICONTROL Aktualisieren]**, um eine Arbeitsmappe zu aktualisieren.

   >[!NOTE]
   >
   >Sie müssen jede Anfrage einzeln aktualisieren. Massenaktualisierung wird nicht unterstützt.


1. Es wird eine Warnung angezeigt, die Sie auf Änderungen an der Arbeitsmappe hinweist, wenn Sie eine Aktualisierung durchführen. Außerdem werden Sie aufgefordert, eine Sicherungskopie Ihrer alten Arbeitsmappe zu erstellen, bevor Sie fortfahren.

   ![Upgrade-Warnung](assets/upgrade_warning.png)

1. Klicken Sie **[!UICONTROL Fortfahren]**, um mit dem Upgrade fortzufahren.

   Wenn das Upgrade erfolgreich durchgeführt wurde, wird die folgende Benachrichtigung angezeigt:

   ![Upgrade abgeschlossen](assets/upgrade_complete.png)

1. (Optional) Klicken Sie auf **[!UICONTROL Upgrade-Bericht herunterladen]**. Dieser Bericht enthält den Status für jeden Datenblock, der aktualisiert wurde.

Sie können [den Datenblock verwalten](/help/analyze/report-builder/manage-reportbuilder.md).


## Keine Unterstützung von Funktionen der Vorgängerversion von Report Builder in der neuen Report Builder-Version {#unsupported}

Einige Funktionen der Vorgängerversion von Report Builder stehen im neuen Report Builder-Add-in nicht mehr zur Verfügung:

- Echtzeit-Anfragen

- Pfad-/Fallout-Berichte

- FTP-Option für geplante Berichte

- Besuchermetriken. Die folgenden Metriken werden alle in „Unique Visitors“ konvertiert, obwohl das Berichtsergebnis möglicherweise keine exakte Übereinstimmung aufweist: `visitorshourly`, `visitorsdaily`, `visitorsweekly`, `visitorsmonthly`, `visitorsquarterly` und `visitorsyearly`. Dies gilt auch für `mobilevisitorshourly`, `mobilevisitorsdaily`, `mobilevisitorsweekly`, `mobilevisitorsmonthly`, `mobilevisitorsquarterly` und `mobilevisitorsyearly`.

## Planen einer konvertierten Arbeitsmappe {#schedule}

Siehe [Planen einer konvertierten Arbeitsmappe](/help/analyze/report-builder/schedule-reportbuilder.md) im Artikel Planung .