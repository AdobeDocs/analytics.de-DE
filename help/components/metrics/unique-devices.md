---
title: Eindeutige Geräte
description: Die Anzahl der eindeutigen Geräte.
feature: Metrics
exl-id: fa5c860f-bea7-4d03-9632-fa6e025647bf
source-git-commit: 16a9c9a2b6692b9b1944cfdb9b5b0411d48db666
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 73%

---

# Eindeutige Geräte

Die Metrik „Eindeutige Geräte[&#128279;](overview.md) ist eine Metrik [Geräteübergreifende Analyse](../cda/overview.md) die die Anzahl der eindeutigen nicht identifizierten Geräte und der eindeutigen virtuellen Geräte zählt. Nicht identifizierte Geräte sind Geräte, die anonyme Treffer erzeugen. Eindeutige virtuelle Geräte sind Einzelpersonen, die pro Gerät identifiziert werden.

## Berechnung dieser Metrik

Für jedes Gerät werden alle Einzelpersonen, die mit ihm verknüpft sind, zusammengefasst (einschließlich anonymer Personen, wenn das Gerät nicht zuordenbare Treffer enthält).

Beachten Sie, dass diese Metrik anders ist als [Unique Visitors](unique-visitors.md) in Report Suite mit nicht-geräteübergreifender Analyse. Nehmen wir an, ein Gerät wird von drei verschiedenen Konten gemeinsam genutzt. Wenn alle drei Konten Ihre Site in einem Berichtsfenster besuchen, zeigt der resultierende Bericht in der geräteübergreifenden Analyse drei eindeutige Geräte an. Dieselben Daten außerhalb der geräteübergreifenden Analyse würden 1 Unique Visitor ergeben.

## Beispiel

1. Sally kommt telefonisch über eine Anzeige auf Ihre Website, ist aber nicht angemeldet.
1. Sally möchte einen Kauf tätigen, würde ihn aber lieber auf dem Familien-Computer abschließen, weil sie dort bereits angemeldet ist. Auf dem Familien-Computer tätigt sie den Kauf.
1. Am nächsten Tag überprüft sie ihre Bestellung auf ihrem Handy und authentifiziert sich dort.
1. Bobs Frau Alice surft auf Ihrer Site, während sie in ihrem Konto auf dem Familien-Computer angemeldet ist.
1. Bobs Bruder Charles surft ebenfalls auf Ihrer Site, während er in seinem Konto auf dem Familien-Computer angemeldet ist.

![Anzahl eindeutiger Geräte](/help/components/metrics/assets/Unique_Devices_Count.png)

Wenn Sie diese Daten in einer Virtual Report Suite mit geräteübergreifender Analyse vor dem [Wiederholen](/help/components/cda/replay.md) ansehen, werden möglicherweise nicht authentifizierte Treffer angezeigt:

* **5 eindeutige Geräte**: 1 für den nicht authentifizierten Bob + 2 für Bob + 1 für Alice + 1 für Charles
* **4 [Personen](people.md)**: 1 [nicht identifizierte Person](unidentified-people.md) + 3 [identifizierte Personen](identified-people.md).
