---
title: Analyse der von Ereignissen betroffenen Daten
description: Verstehen Sie, wie die von einem Ereignis betroffenen Daten zur Datenqualität insgesamt beitragen.
exl-id: 8d81a432-42d6-4f5d-b66a-bb3af7fc4857
feature: Curate and Share
TQID: 'https://experienceleague.adobe.com/DJoJwtp9CkgrCfA1DwW8rKX2x3ssfzLCo7vCfhdLusg'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
    internal-label: Analysis Workspace
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
    internal-label: Admin Tools
subfeature_v2:
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
    internal-label: Components
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
    internal-label: Events
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
  - id: c510df06-c813-424c-abc1-c7ae8b03e9b3
    internal-label: Curate and Share
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b4dd41a7-ccf8-4e9d-918e-acaab534a307
    internal-label: Data quality
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
source-git-commit: 9a50beeb0aa51cf9f4baf212566947c14029ce8e
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 90%
---
# Analyse der von Ereignissen betroffenen Daten

Manchmal kann ein Ereignis die Datenqualität in Ihrem Unternehmen beeinträchtigen. Beispiele hierfür sind:

* Ein Bot, der Ausreißerdaten sendet, beispielsweise Umsätze in Millionenhöhe,
* Ihr Unternehmen hat eine Aktualisierung Ihrer Website veröffentlicht, die sich negativ auf Ihre Analytics-Implementierung auswirkt.
* Andere Aspekte, die die Datenqualität oder -vollständigkeit beeinträchtigen.

Wenn auf Ihrer Site Probleme mit der Datenqualität aufgetreten sind, möchten Sie diese möglicherweise vom Reporting ausschließen, um zu verhindern, dass Sie geschäftliche Entscheidungen auf dieser Grundlage treffen. Verwenden Sie diese Abschnitte, um die Auswirkungen des Ereignisses auf Ihre Daten zu beurteilen und festzulegen, wie Sie vorgehen möchten.

## Ursache eines Ereignisses bestimmen

Wenn Sie sich nicht sicher sind, warum Sie Datenspitzen oder Datenrückgänge sehen, lesen Sie [Fehlerbehebung bei Datenspitzen/Datenrückgängen](spikes-drops.md).

## Daten mithilfe der Segmentierung analysieren und ausschließen

Adobe Analytics bietet eine einfache und robuste Möglichkeit, mithilfe von Segmentierung den Fokus auf bestimmte Daten zu legen oder Daten auszuschließen. Sie können Datumsbereichsdimensionen innerhalb von Segmenten verwenden, um diese bestimmten Daten herauszufiltern oder sich darauf zu konzentrieren. Weitere Informationen finden Sie unter [Ausschließen spezifischer Daten in der Analyse](segments.md).

## Vergleichen eines Ereignisses mit vorherigen Datumsbereichen

Wenn Sie mehr darüber erfahren möchten, wie stark sich ein Ereignis im Laufe der Zeit auf Ihre Daten auswirkt, können Sie den Datumsvergleich in Analysis Workspace verwenden. Mit dieser Funktion können Sie Daten Tag für Tag, Woche für Woche oder Monat für Monat vergleichen, um zu sehen, wie sie sich im Vergleich zu früheren Zeiträumen verhalten. Sie können diesen Vergleich dann verwenden, um festzustellen, wie stark ein Ereignis Trends beeinflusst. Weitere Informationen finden Sie unter [Daten, die von einem Ereignis beeinflusst wurden, mit vorherigen Datumsbereichen vergleichen](compare-dates.md).

## Daten mithilfe berechneter Metriken ableiten

Sobald Sie Segmente erstellt und den Datumsvergleich verwendet haben, können Sie beide Konzepte kombinieren, um Trend-Daten mithilfe berechneter Metriken zu korrigieren. Schließen Sie die Segmente in eine berechnete Metrik ein und multiplizieren Sie dann die betroffenen Tage mit dem beim Datumsvergleich gefundenen Versatz. Weitere Informationen finden Sie unter [Ableiten von Daten, die von Ereignissen betroffen sind](calcmetrics.md).

## Kommunizieren von Auswirkungen für Benutzende in Ihrer Organisation

Sobald Sie mit der geplanten Handhabung eines Ereignisses vertraut sind, können Sie mit den Benutzern in Ihrem Unternehmen [kommunizieren](communicate.md). Adobe bietet in Analytics mehrere Stellen an, an denen Sie Text platzieren können, um den Benutzern mitzuteilen, was passiert ist und welche Komponenten sie verwenden können.

## Video

>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Analysieren und Kommunizieren von Varianten in Ihren Daten](https://video.tv.adobe.com/v/33316?quality=12&learn=on){target="_blank"} finden Sie ein Demovideo.

* **0:**: Ausschließen von Daten mithilfe der Segmentierung
* **2:**: Vergleichen eines Ereignisses mit vorherigen Bereichen
* **8:**: Ableiten von Daten mithilfe berechneter Metriken
* **11:**: Kommunizieren der Auswirkungen für Benutzer

>[!ENDSHADEBOX]


