---
description: Rangordnung und bedingte Filter, die Sie mit UND/ODER-Suchausdrücken entsprechend Boolscher Logik konfigurieren.
title: Bevorzugte Filter
uuid: 558fa592-41be-4e66-8705-81262afe1fc7
feature: Report Builder
role: User, Admin
exl-id: 31587740-6caa-40cb-bb24-d7a15181f642
TQID: https://experienceleague.adobe.com/TLo2RytIM7ZQlpFMqXsTdoz7vFAXnwqoTJGHDG7gWLg
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 633
ht-degree: 56%

---

# Bevorzugte Filter

{{legacy-arb}}

Rangordnung und bedingte Filter, die Sie mit UND/ODER-Suchausdrücken entsprechend Boolscher Logik konfigurieren.

Am meisten bevorzugte Filter sind Ausdrucksfilter, die Sie mit den UND/ODER-Bedingungen der Boolschen Logik konfigurieren, beispielsweise [!UICONTROL Seite enthält nicht ]*`<product name>`* mit Bedingungen oder Gruppen von Bedingungen wie [!UICONTROL Alle eingeschlossen], [!UICONTROL Beliebige eingeschlossen] oder [!UICONTROL Alle ausgeschlossen]. Sie können die Ausdrücke [speichern](/help/analyze/legacy-report-builder/layout/c-filter-dimensions/saved-filters.md), um sie in anderen Anforderungen in der aktuellen oder anderen Arbeitsmappen zu verwenden.

**So erstellen Sie am meisten bevorzugte Filter**

1. Erstellen oder bearbeiten Sie eine Anforderung und gehen Sie zum Dialogfeld [!UICONTROL Anforderungs-Assistent: Schritt 2].

1. Klicken Sie im Dialogfeld [!UICONTROL Anforderungs-Assistent: Schritt 2] im Raster auf den Link neben der Dimension und wählen Sie dann **[!UICONTROL Filter]**.

   ![Screenshot mit dem Dialogfeld „Filter definieren“ mit Optionen zum Filtern nach Anwendung, Benutzer und Projekt.](/help/admin/tools/assets/filter.png)

1. Aktivieren Sie im Dialogfeld [!UICONTROL Seiten auswählen] die Option **[!UICONTROL Am meisten bevorzugte]** und konfigurieren Sie dann die folgenden Optionen:

   **Startrang:** Der Startrang einer Dimension. Der Standardwert von 1 steht für das Element mit dem höchsten Wert in der Liste der berichteten Daten. Beispiel: Für die Dimension [!UICONTROL Seite] gibt ein Anfangszeichen von 1 die am häufigsten angeforderte Seite Ihrer Site an. Sie können beispielsweise 10 oder einen anderen Wert als Startrangzelle angeben, wodurch ein Bericht erstellt wird, der mit 10 als höchstem Wert beginnt. Metriken werden in absteigender Reihenfolge angeordnet, d. h. die Zeileneinträge mit der höchsten Aktivität werden als erste in der Liste aufgeführt. Wenn Sie mehr als 50.000 Seitennamen in einer Anfrage benötigen, aber Tausende von Seiten haben, auf denen Berichte erstellt werden sollen, können Sie die Anfrage kopieren und den Anfangsrang ändern, um die entsprechenden Daten in 50.000-Blocks abzurufen.

   **Anzahl der Einträge:** (nur [!UICONTROL Pivot-Layout]) Legt fest, wie viele Elemente für eine bestimmte Metrik über einen Datumsbereich berichtet werden. Einige Metriken können hunderte von Einträge aufweisen, andere nur einige wenige. Beispiel: Für die Dimension [!UICONTROL Site-Bereich] gibt eine Anzahl von Einträgen von 25 an, dass der Bericht die 25 am häufigsten besuchten Seiten anzeigt.

   Mit den Pfeilen können Sie den [!UICONTROL Anfangsrang] und [!UICONTROL Anzahl der Einträge] des ersten Datenpunkts im Blatt ändern. Standardmäßig ist der [!UICONTROL Startrang] auf 1 und die [!UICONTROL Anzahl der Einträge] auf 10 festgelegt. Diese Werte können für bestimmte Metriken von mindestens 1 bis maximal 50.000 angepasst werden. Jede Metrik hat einen eigenen Maximalwert für [!UICONTROL Anzahl der Einträge]. In diesen Feldern sind keine negativen oder Nullwerte erlaubt. Wenn Sie für [!UICONTROL Startrang] den Wert 15 und für [!UICONTROL Anzahl der Einträge] den Wert 10 wählen, geben Datenanforderungen für die Metrik die 10 am häufigsten besuchten Seiten zurück, wobei die erste der am häufigsten besuchten Seiten die Nummer 15 in der Liste für den jeweiligen Datumsbereich ist. Die am häufigsten angefragten Seiten, die von 15 bis 25 rangieren, werden in absteigender Reihenfolge aufgelistet.

   >[!NOTE]
   >
   >Wenn Sie Filter auf bestehende Anforderungen anwenden, ändern sich die angezeigten Daten. Angenommen, Sie haben die zehn wichtigsten [!UICONTROL Seiten] den Zellen $A$1 bis $A$10 zugeordnet, mit 1 für [!UICONTROL Starting Rank] und 10 für [!UICONTROL Number of Entries]. Wenn Sie diese Werte ändern, sodass 1 für &quot;[!UICONTROL  Rang] und nur 3 für &quot;[!UICONTROL  der Einträge] angezeigt werden, werden die Daten, die zuvor die Zellen $A$4 bis $A$10 gefüllt haben, nicht mehr angezeigt.

1. Um einen Suchausdruck zu erstellen, klicken Sie auf **[!UICONTROL Hinzufügen]**.

1. Konfigurieren Sie im Dialogfeld [!UICONTROL Filter definieren] die Ihren Anforderungen entsprechenden Bedingungen.


   ![Screenshot mit dem Dialogfeld „Filter definieren“.](assets/expressions_define_filter.png)

   Mit dem Symbol Zelle auswählen können Sie eine Bedingung finden, die im Wert einer Zelle definiert ist. ![Das Symbol „Zelle auswählen“.](assets/select_cell_icon.png)

   Über **Link** Bedingung hinzufügen“ können Sie eine Bedingung zum Ausdruck hinzufügen. Die Zahl der Bedingungen, die Sie hinzufügen können, ist nicht beschränkt.

1. Klicken Sie auf **[!UICONTROL OK]**.

   ![Screenshot des Dialogfelds „Filter definieren“ mit der Schaltfläche „OK“ unten rechts.](assets/choose_page_02.png)

1. Klicken Sie im Dialogfeld [!UICONTROL Seiten auswählen] auf **[!UICONTROL Speichern]**, um den Ausdruck zu speichern.
1. Klicken Sie auf **[!UICONTROL OK]**.
