---
description: Sie können einen komplexen Datumsbereich festlegen, indem Sie einen benutzerdefinierten Ausdruck verwenden.
title: Benutzerdefinierte Datumsausdrücke – Übersicht
uuid: 7d6d7c03-a3f4-4dec-8343-de2e6478bf06
feature: Report Builder
role: User, Admin
exl-id: b3bdc07e-5c2d-4be3-86c9-b4b7380be0f6
TQID: https://experienceleague.adobe.com/s6Q9D3KoMLw0-95kydXM0IyO-NjaSNF6hKcHK25KMH0
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 281
ht-degree: 12%

---

# Benutzerdefinierte Datumsausdrücke

{{legacy-arb}}

Sie können einen komplexen Datumsbereich festlegen, indem Sie einen benutzerdefinierten Ausdruck verwenden.

Verweisen Sie beim Erstellen von Ausdrücken auf einen Kalender, um die Anzahl der Wochen und Tage korrekt anzugeben. Excel verfügt über mehrere integrierte Funktionen, mit denen Sie die Anzahl der Tage, Arbeitstage, Monate und Jahre zwischen den Datumsangaben berechnen können. Sie können diese Funktionen in Formeln verwenden, um andere Intervalle wie Wochen und Quartale zu berechnen.

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
