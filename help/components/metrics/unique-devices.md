---
title: Eindeutige Geräte
description: Die Anzahl der eindeutigen Geräte.
feature: Metrics
exl-id: fa5c860f-bea7-4d03-9632-fa6e025647bf
TQID: https://experienceleague.adobe.com/7KUpaGPuFGBHTXj8L4MKnjOsi1YQtA8KUCIXSa-NtXc
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 266
ht-degree: 73%

---

# Eindeutige Geräte

Die Metrik „Eindeutige Geräte[&#x200B; &#x200B;](overview.md) ist eine Metrik [Geräteübergreifende Analyse](../cda/overview.md) die die Anzahl der eindeutigen nicht identifizierten Geräte und der eindeutigen virtuellen Geräte zählt. Nicht identifizierte Geräte sind Geräte, die anonyme Treffer erzeugen. Eindeutige virtuelle Geräte sind Einzelpersonen, die pro Gerät identifiziert werden.

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
