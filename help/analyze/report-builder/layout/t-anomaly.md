---
description: Erfahren Sie, wie Sie in Report Builder eine Anomalieerkennungsanforderung erstellen.
title: Konfigurieren einer Anomalieerkennungsanforderung
uuid: 1e504ff9-df88-4fa7-95ea-1ca05a6f9c0d
feature: Report Builder
role: User, Admin
exl-id: 0a8b1971-8d32-424a-9d41-d7ab2af54d1e
source-git-commit: 2eff7656741bdba3d5d7d1f33e9261b59f8e6083
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 72%

---

# Konfigurieren einer Anomalieerkennungsanforderung

So erstellen Sie eine Anomalieerkennungsanforderung in Report Builder:

1. Wählen Sie einen Trendbericht aus, z. B. einen Bericht für **[!UICONTROL Site-Metriken]** > **[!UICONTROL Traffic]**.
1. Wählen Sie im Menü [!UICONTROL Granularität anwenden] den Eintrag **[!UICONTROL Tag]**.

   >[!NOTE]
   >
   >Das Menü [!UICONTROL Anomalieerkennung] ist nur verfügbar, wenn Sie als Granularität „Tag“ auswählen. Die Daten der letzten 30 Tage werden unabhängig vom gewählten Datumsbereich als Schulungszeitraum für statistische Daten verwendet.

1. Nach dem Konfigurieren der Datumsbereiche klicken Sie auf **[!UICONTROL Weiter]**.

   Im Anforderungs-Assistenten, Schritt 2 von 2, fügen Sie eine Metrik hinzu, z. B. **[!UICONTROL Besuche]**.

   Klicken Sie für die hinzugefügte Metrik auf den Link **[!UICONTROL Keine]**.

   ![Screenshot mit der Anomalieerkennung, gefolgt von &quot;Einfügen&quot;und anschließenden Optionen für &quot;Untere&quot;und &quot;Obere Grenze&quot;und &quot;Erwartet&quot;.](assets/anomaly_select.png)

1. Wählen Sie **[!UICONTROL Anomalieerkennung]** > **[!UICONTROL `<selection>`]** aus.

   ![Screenshot mit dem Anforderungs-Assistenten, Schritt 2: Traffic-Bericht.](assets/anomaly_visit.png)

   Wenn Sie eine dieser Optionen wählen, erstellt das System für die Anomalieerkennung Kopien der ursprünglichen Metrik. Beispielsweise wird für die Besuchsmetrik der Gruppe [!UICONTROL Metrik] eine Metrik für die Untergrenze von Besuchen hinzugefügt.
1. Klicken Sie auf **[!UICONTROL Fertigstellen]** und wählen Sie eine Zelle für die Ausgabe in Excel.

   Siehe [Anomalieerkennung](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) für Definitionen.
