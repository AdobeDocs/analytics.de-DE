---
description: Filter, die dimensionsspezifische Terme anwenden.
title: Spezifische Filter
uuid: b3a8187a-3d59-4da0-abca-e933664332e3
feature: Report Builder
role: User, Admin
exl-id: e5f2d67c-3add-4d51-8a76-ee3b2a6eef94
TQID: https://experienceleague.adobe.com/yNIeTJwwWtjXkbi47lX1Ve-Rbz6lF1PazD4YxxXa0Ac
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 336
ht-degree: 60%

---

# Spezifische Filter

{{legacy-arb}}

Filter, die dimensionsspezifische Terme anwenden.

Sie können dimensionsspezifische Filter setzen, indem Sie einen Filter erstellen, für den exakte Kriterien erfüllt werden müssen. Beispielsweise können Sie den folgenden Filtertyp erstellen: Seite unter [!DNL homepage.htm], [!DNL contact_us.html], [!DNL corporate_info.html].

**So erstellen Sie einen spezifischen Filter**

1. Erstellen oder bearbeiten Sie eine Anforderung und gehen Sie zum Dialogfeld [!UICONTROL Anforderungs-Assistent: Schritt 2].

   ![Screenshot mit den Optionen zum Filtern nach: Anwendung, Benutzer und Projekt.](/help/admin/tools/assets/filter.png)

1. Klicken Sie im Dialogfeld [!UICONTROL Anforderungs-Assistent: Schritt 2] im Raster auf den Link neben der Dimension und wählen Sie dann **[!UICONTROL Filter]**.

1. Aktivieren Sie **[!UICONTROL spezifisch]**.

   ![Screenshot des Dialogfelds „Seite wählen“ mit ausgewählter Option „Spezifisch“.](assets/choose_page_specific01.png)

1. Aktivieren Sie eine der folgenden spezifischen Optionen:

   * **Aus Zellenbereich:** Hier können Sie Daten aus Zellen auswählen. Folgende Optionen stehen zur Auswahl:
      * **Alle Zellen im Bereich:** Hier können Sie jede Zelle für den Bereich zuordnen. Eine Textbeschreibung erläutert, wie viele Gruppen von Zellen Sie auswählen müssen. Um mehr als eine Zellengruppe zuzuordnen, drücken Sie die Strg-Taste, während Sie aufeinander folgende Auswahlen vornehmen. Wenn der zuzuordnende Bereich nur eine Zelle enthält, ist dies die einzige verfügbare Option
      * **Erste Zelle des Bereichs** Sie müssen nur die obere linke Zelle des Bereichs auswählen und dann eine Richtung für die Daten auswählen. Wenn die Anforderung mehrere Perioden umfasst, wählen Sie außerdem die Richtung der Perioden aus und legen fest, ob eine bestimmte Anzahl von Zellen zwischen den Perioden übersprungen werden soll.
   * **Aus Liste** Ermöglicht die Auswahl von Daten aus einer Liste, der Sie Daten hinzufügen können.
1. Wenn Sie die Option **[!UICONTROL Aus Liste]** aktivieren, können Sie aus den verfügbaren aufgelisteten Elementen auswählen oder auf **[!UICONTROL Hinzufügen]** klicken.

   Wenn Sie auf **[!UICONTROL Hinzufügen]** klicken, wird im Dialogfeld [!UICONTROL Aus Liste auswählen] eine Liste der für den Datumsbereich der aktuellen Anforderung verfügbaren Dimensionselemente, beschränkt auf die ersten 10.000 Elemente, angezeigt. Sie können diese Elemente durchsuchen oder auf **[!UICONTROL Mehr ...]** klicken, um das [!UICONTROL Suchdialogfeld] anzuzeigen, in dem Sie detaillierter nach Dimensionen suchen können.
1. Klicken Sie im Dialogfeld [!UICONTROL Aus Liste auswählen] auf **[!UICONTROL OK]**.
1. Speichern Sie im Formular [!UICONTROL Seiten auswählen], falls gewünscht, Ihren spezifischen Filter und klicken Sie dann auf **[!UICONTROL OK]**.
