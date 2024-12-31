---
description: Erfahren Sie, wie Sie den Offline-Modus verwenden, um Platzhalterdaten zurückzugeben.
title: Aktivieren des Offline-Modus
uuid: 4eb1f754-b6da-4896-a64f-b737563925b8
feature: Report Builder
role: User, Admin
exl-id: f18859e3-19e4-48af-963f-0bb4d1b46380
source-git-commit: fcecc8a493852f5682fd7fbd5b9bb484a850922c
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 33%

---

# Offline-Modus zum Erstellen und Bearbeiten von Anforderungen

{{legacy-arb}}

Im Offline-Modus werden Platzhalterdaten zurückgegeben, um das Erstellen und Bearbeiten von Anfragen zu beschleunigen.

Wenn Sie eine neue Anfrage erstellen oder bearbeiten, werden Report API-Aufrufe durchgeführt, um die Antwort abzurufen. Manchmal verlangsamen diese Aufrufe den Prozess der Anfrageerstellung, da Sie warten müssen, bis die Daten zurückgegeben werden, bevor Sie mit dem nächsten Schritt fortfahren. Der Offline-Modus gibt nur Platzhalterdaten zurück und die API wird nicht erstellt.

So aktivieren Sie den Offline-Modus

1. Klicken Sie im Report Builder-Menü auf **[!UICONTROL Optionen]**.

   ![Screenshot des Bildschirms „Optionen“ mit ausgewähltem Offline-Modus.](assets/offline_mode.png)

1. Aktivieren Sie neben **[!UICONTROL Aktivieren Sie den Offline-Modus, um Anforderungen zu erstellen und zu bearbeiten]** das Kontrollkästchen.
1. Geben Sie im Feld **[!UICONTROL Metrikdaten anzeigen als]** die Platzhalterdaten ein, die bei Ihrer Anforderung zurückgegeben werden sollen. Geben Sie zum Beispiel „1“ ein.
1. Klicken Sie auf **[!UICONTROL OK]**.
1. Erstellen Sie Ihre Anfrage und führen Sie sie im Offline-Modus mit dem Anforderungs-Assistenten aus. Der folgende Screenshot zeigt ein Beispiel für eine Anfrage mit „1“ als Platzhalterdaten.

   ![Screenshot mit dem Beispiel für den Offline-Modus, in dem 1 als Platzhalter verwendet wird.](assets/offline_mode_example.png)

   >[!IMPORTANT]
   >
   >Stellen Sie sicher, dass Sie den Offline-Modus deaktivieren, bevor Sie Ihre Anfragen mit echten Daten ausführen.
