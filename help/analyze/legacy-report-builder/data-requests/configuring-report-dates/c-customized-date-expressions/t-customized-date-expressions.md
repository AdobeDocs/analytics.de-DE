---
description: Sie können einen komplexen Datumsbereich festlegen, indem Sie einen benutzerdefinierten Ausdruck verwenden.
title: Benutzerdefinierte Datumsausdrücke – Übersicht
uuid: 7d6d7c03-a3f4-4dec-8343-de2e6478bf06
feature: Report Builder
role: User, Admin
exl-id: b3bdc07e-5c2d-4be3-86c9-b4b7380be0f6
source-git-commit: ae6ffed05f5a33f032d0c7471ccdb1029154ddbd
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 24%

---

# Benutzerdefinierte Datumsausdrücke

{{legacy-arb}}

Sie können einen komplexen Datumsbereich festlegen, indem Sie einen benutzerdefinierten Ausdruck verwenden.

Verweisen Sie beim Erstellen von Ausdrücken auf einen Kalender, um die Anzahl der Wochen und Tage korrekt anzugeben. Excel bietet verschiedene integrierte Funktionen für die Berechnung von Tagen, Werktagen, Monaten und Jahren, die zwischen zwei Datumswerten liegen. Sie können diese Funktionen in Formeln verwenden, um andere Intervalle zu berechnen, etwa Wochen oder Quartale.

**So aktivieren Sie benutzerdefinierte Ausdrücke**

Das folgende Beispiel zeigt, wie ein benutzerdefinierter Ausdruck für „Rollierende **[!UICONTROL &quot; aktiviert]**.

1. Wählen Sie im [!UICONTROL Anforderungs-Assistenten: Schritt 1] anstelle von **[!UICONTROL Vordefinierte Datumswerte]** die Option **[!UICONTROL Rollierende Datumswerte]**.

   ![Screenshot mit ausgewählten rollierenden Datumsangaben.](assets/rolldates1.png)

1. Wechseln Sie zu „Rollierend“ (wöchentlich, monatlich, vierteljährlich oder jährlich). Beachten Sie, wie sich die unten stehenden Optionen ändern.
1. Um weitere Anpassungsoptionen anzuzeigen, klicken Sie auf **[!UICONTROL Erweiterte Optionen anzeigen]**.

   ![Screenshot mit hervorgehobenen Optionen für „Erweiterte Optionen anzeigen“.](assets/rolldates2.png)

1. Wenn Sie beispielsweise die obigen Datumsangaben vom ersten Tag vor drei Monaten auf den ersten Tag dieses Monats in „Rollierend monatlich“ ändern, werden die Datumsangaben im Abschnitt „Erweiterte Optionen“ selbst aktualisiert, um Folgendes widerzuspiegeln:

   ![Screenshot mit den rollierenden Datumsangaben vom ersten Tag vor drei Monaten bis zum ersten Tag dieses Monats.](assets/rolldatesfor3.png)

1. Aktivieren Sie **[!UICONTROL Ausdruck anpassen]**. Durch Auswahl von Optionen unter **[!UICONTROL Rollierende Datumswerte]** können Sie die Syntax für benutzerdefinierte Datumsausdrücke leicht erkennen.

   ![Screenshot mit ausgewähltem Ausdruck anpassen.](assets/rolldatesfor5.png)

   Sie können erweiterte Optionen verwenden, um benutzerdefinierte Datumsausdrücke zu mischen und zuzuordnen. Wenn Sie beispielsweise Daten vom ersten Tag des Jahres bis zum Ende des letzten vollen Monats anzeigen möchten, können Sie Folgendes eingeben: `From: cy` `To: cm-1d`. Im Assistenten werden diese Daten als 31.1.2020-1.2020 angezeigt.
