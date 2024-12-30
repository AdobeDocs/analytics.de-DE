---
description: Alle mit Lesezeichen versehenen Berichte und Dashboard-Berichte werden jetzt im Anforderungs-Assistenten in Schritt 1 als Dimensionen aufgeführt und können als Report Builder-Anforderungen importiert werden.
title: Mit Lesezeichen markierte Berichte und Dashboard-Kurzberichte importieren
feature: Report Builder
role: User, Admin
exl-id: 19813950-2495-4a75-aacb-587b59bf2484
source-git-commit: ae6ffed05f5a33f032d0c7471ccdb1029154ddbd
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 65%

---

# Mit Lesezeichen markierte Berichte und Dashboard-Kurzberichte importieren

{{legacy-arb}}

Alle mit Lesezeichen versehenen Berichte und Dashboard-Berichte werden jetzt im Anforderungs-Assistenten in Schritt 1 als Dimensionen aufgeführt und können als Report Builder-Anforderungen importiert werden.

Wenn Sie einen mit Lesezeichen markierten Bericht auswählen, belegt der Anforderungs-Assistent alle Dimensionen und Metriken, die diesen mit Lesezeichen markierten Bericht definieren. Der Datumsbereich, die Granularität und das ausgewählte Segment werden ebenfalls auf der Grundlage des ausgewählten Lesezeichens aktualisiert.

So werden in Schritt 1 des Anforderungs-Assistenten ein Dashboard und die zugehörigen Kurzberichte angezeigt:

![Screenshot mit dem Anforderungs-Assistenten, Schritt 1 von 2, in dem die Optionen „Dashboards abrufen“ und „Lesezeichen abrufen“ hervorgehoben sind.](assets/import_dashboard_reportlet.png)

Wenn Sie auf **[!UICONTROL Ihre Dashboards abrufen]** oder auf **[!UICONTROL Ihre Lesezeichen abrufen]** klicken, werden Ihre vorhandenen Dashboard- und/oder Lesezeichendaten abgerufen und in das Arbeitsblatt eingefügt.

>[!NOTE]
>
>Es werden ausschließlich Daten importiert. Wenn das Lesezeichen ein Diagramm enthält oder der Dashboard-Kurzbericht nur aus einem Diagramm besteht, werden nur die Daten importiert, auf denen das Diagramm basiert.

Sobald Sie eine Anforderung durch Importieren eines Dashboard-Kurzberichts (bzw. eines Lesezeichens) erstellt haben, wird die Anforderung mit der primären Dimension des Kurzberichts (bzw. des Lesezeichens) verknüpft. Das führt dazu, dass in der Baumansicht nicht mehr der Knoten des Dashboard-Kurzberichts (bzw. des Lesezeichens) ausgewählt wird, wenn Sie eine Anforderung bearbeiten, sondern die primäre Dimension.

