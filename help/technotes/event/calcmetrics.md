---
title: Ableiten von Daten, die von Ereignissen betroffen sind
description: Verwenden Sie berechnete Metriken, um die von einem Ereignis betroffenen Trenddaten zu korrigieren.
exl-id: 0fe70c8b-fa07-47e4-b6b3-b55eebad1fef
feature: Event, Calculated Metrics
source-git-commit: 811e321ce96aaefaeff691ed5969981a048d2c31
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 3%

---

# Ableiten von Daten, die von Ereignissen betroffen sind

Wenn von einem Ereignis ](overview.md) Daten [betroffen sind, können Sie berechnete Metriken verwenden, um geschätzte Werte für die Dauer des Ereignisses abzuleiten. Wenn Sie beispielsweise über ein Ereignis verfügten, das zu einem Datenabfall von 25 % führte, können Sie dies als Multiplikator in einer berechneten Metrik verwenden.

Diese Schritte funktionieren am besten, wenn Sie die Auswirkungen eines Ereignisses sowohl aus der Sicht der Segmentierung als auch des Datumsvergleichs verstehen. Vergewissern Sie sich, dass Sie [Datum vergleichen, die von einem Ereignis betroffen sind, mit vorherigen Bereichen](compare-dates.md) und [Bestimmte Daten in der Analyse ausschließen](segments.md) befolgen, bevor Sie dieser Seite folgen.

>[!NOTE]
>
>Bei diesem Ansatz handelt es sich um eine Schätzung, die auf einem bestimmten Satz von Eingaben und Datumsbereichen basiert. Es wird keine umfassende Lösung für alle Anwendungsfälle oder Datenscheiben sein. Darüber hinaus erfordert dieser Ansatz, dass der betroffene Datumsbereich mindestens 1 Treffer enthält, aus dem berechnet werden soll.

So erstellen Sie eine geschätzte berechnete Metrik für den betroffenen Zeitraum:

1. Erstellen Sie zwei Segmente für &quot;Betroffene Tage&quot;und &quot;Betroffene Tage ausschließen&quot;, wie unter [Ausschließen bestimmter Daten in der Analyse](segments.md) beschrieben.
2. Navigieren Sie zu **[!UICONTROL Komponenten]** > **[!UICONTROL Berechnete Metriken]**.
3. Klicken Sie auf **[!UICONTROL Hinzufügen]**.
4. Ziehen Sie beide der oben genannten Segmente auf die Arbeitsfläche für die Definition. Ändern Sie den Operator zwischen ihnen in &quot;`+`&quot;, um ihn zu summieren.
5. Fügen Sie die gewünschte Metrik in beiden Segmenten hinzu. Sie können beispielsweise die Metrik &quot;Besuche&quot;verwenden.

   ![Segment Builder](assets/event_segment_builder.png)

6. Klicken Sie oben rechts im Container &quot;Betroffene Tage&quot;auf **[!UICONTROL Hinzufügen]** und dann auf **[!UICONTROL Statische Zahl]**. Legen Sie die statische Zahl auf den Prozentsatz fest, mit dem Sie Ihre Daten versetzen möchten, wie unter [Datum vergleichen, die von einem Ereignis beeinflusst wurden, mit vorherigen Bereichen](compare-dates.md) beschrieben. In diesem Beispiel beträgt der Offset 25 % oder 1,25.

   ![Statische Zahl](assets/event_static_number.png)

7. Wenden Sie die &quot;korrigierte&quot;Metrik in einer Trend-Freiformtabelle nebeneinander an. Alle Tage außerhalb des Ereignisses spiegeln die normale Metrikanzahl wider, während alle betroffenen Tage den Multiplikatorversatz verwenden.

   ![Korrigierte Metrik](assets/event_corrected.png)

8. Zeigen Sie die Daten in einer Linienvisualisierung an, um die Auswirkungen Ihrer korrigierten Metrik anzuzeigen.

   ![Korrigierte Zeile](assets/event_line.png)
