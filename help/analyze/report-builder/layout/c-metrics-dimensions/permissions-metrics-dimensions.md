---
description: Adobe ReportBuilder bietet jetzt Berechtigungseinstellungen, die denjenigen der Admin Tools von Analytics entsprechen.
title: Benutzerzugriffsberechtigungen für Dimensionen und Metriken
topic: Report builder
uuid: b561407d-c4fa-4f1e-8b16-5ca46fcbf36f
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Benutzerzugriffsberechtigungen für Dimensionen und Metriken

Adobe ReportBuilder bietet jetzt Berechtigungseinstellungen, die denjenigen der Admin Tools von Analytics entsprechen.

Als Benutzer ohne Administratorrechte haben Sie möglicherweise bereits Arbeitsmappen mit Anforderungen erstellt, die auf Dimensionen und Metriken verweisen, auf die Sie keinen Zugriff haben. Diese Berechtigungen kommen nun zur Geltung.

Wenn Sie zum Beispiel eine Anforderung aktualisieren, die Dimensionen oder Metriken enthält, auf die Sie keinen Zugriff haben, erhalten Sie eine Fehlermeldung wegen eingeschränkter Berechtigung:

![](assets/arb_restrc_perm.png)

Befolgen Sie diese Anweisungen für **jede** ReportBuilder-Arbeitsmappe, die Sie pflegen:

1. Öffnen Sie die Arbeitsmappe.
1. Aktualisieren Sie alle Anforderungen.
1. Wenn ein Fehler wegen Benutzerzugriffsberechtigungen angezeigt wird, klicken Sie auf **[!UICONTROL CSV-Datei öffnen], um Zugriff auf die Liste der Fehler wegen eingeschränkter Berechtigungen zu erhalten.**
1. Erstellen Sie die Datei "AllRestrictedPermissionErrors.xlsx"und kopieren Sie die Liste der Fehler mit eingeschränkter Berechtigung aus der CSV-Datei in diese Datei.
1. Schließen Sie die ReportBuilder-Arbeitsmappe.

Nachdem Sie alle Arbeitsmappen verarbeitet haben, sollten Sie eine umfassende Liste mit Fehlern wegen eingeschränkter Berechtigung in "AllRestrictedPermissionErrors.xlsx"haben. Senden Sie diese Liste an Ihren für den Benutzerzugriff zuständigen Adobe Analytics-Administrator und bitten Sie darum, Ihnen Zugriff auf die Metriken und Dimensionen zu gewähren.
