---
description: Alle mit Lesezeichen versehenen Berichte und Dashboard-Berichte werden jetzt im Anforderungs-Assistenten in Schritt 1 als Dimensionen aufgeführt und können als Report Builder-Anforderungen importiert werden.
title: Mit Lesezeichen markierte Berichte und Dashboard-Kurzberichte importieren
feature: Report Builder
role: User, Admin
exl-id: 19813950-2495-4a75-aacb-587b59bf2484
TQID: https://experienceleague.adobe.com/dnOYs7eOvv15K73EPrfRegz1vH9-B5p8xI8d86vPYe4
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2: id: ac8a38fa-dec3-4581-8f64-178fde9f64e8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 241
ht-degree: 18%

---

# Mit Lesezeichen markierte Berichte und Dashboard-Kurzberichte importieren

{{legacy-arb}}

Alle mit Lesezeichen versehenen Berichte und Dashboard-Berichte werden jetzt im Anforderungs-Assistenten in Schritt 1 als Dimensionen aufgeführt und können als Report Builder-Anforderungen importiert werden.

Wenn Sie einen Bericht mit Lesezeichen auswählen, füllt der Anforderungs-Assistent alle Dimensionen und Metriken, die diesen Bericht mit Lesezeichen definieren. Der Datumsbereich, die Granularität und das ausgewählte Segment werden ebenfalls auf der Grundlage des ausgewählten Lesezeichens aktualisiert.

So zeigt der Anforderungs-Assistent in Schritt 1 ein Dashboard und die zugehörigen Reportlets an:

![Screenshot mit dem Anforderungs-Assistenten, Schritt 1 von 2, in dem die Optionen „Dashboards abrufen“ und „Lesezeichen abrufen“ hervorgehoben sind.](assets/import_dashboard_reportlet.png)

Wenn Sie auf **[!UICONTROL Dashboards abrufen]** oder **[!UICONTROL Lesezeichen abrufen]** klicken, werden Ihre vorhandenen Dashboard- und/oder Lesezeichen-Daten abgerufen und in das Arbeitsblatt eingefügt.

>[!NOTE]
>
>Es werden ausschließlich Daten importiert. Wenn das Lesezeichen ein Diagramm enthält oder der Dashboard-Kurzbericht nur aus einem Diagramm besteht, werden nur die Daten importiert, auf denen das Diagramm basiert.

Nachdem Sie eine Anfrage durch Importieren eines Dashboard-Reportlets (oder eines Lesezeichens) erstellt haben, wird die Anfrage dann mit der primären Dimension des Reportlets (oder des Lesezeichens) verknüpft. Wenn Sie die Anfrage bearbeiten, wählt die Baumstrukturansicht daher nicht mehr den Baumstrukturansichtsknoten (oder Lesezeichenknoten) des Reportlets aus: Stattdessen wird die primäre Dimension ausgewählt.

