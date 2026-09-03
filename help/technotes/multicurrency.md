---
description: Beschreibt, wie Sie Zielwährungs-Codes definieren, damit die Unterstützung mehrerer Währungen funktioniert.
title: Unterstützung mehrerer Währungen
feature: Analytics Basics
exl-id: b67f459c-0636-4eac-af52-51846bb583b5
TQID: https://experienceleague.adobe.com/-t0JAIvbmUmzTCTznOWcjVmvtJbmQNV5MIrbQBvhv6M
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: a421fb65-2c82-457a-921c-28c46b697a39id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 127
ht-degree: 18%

---

# Unterstützung mehrerer Währungen

Adobe bietet mehrere Ebenen der Währungsumrechnung, damit Ihr Unternehmen die gewünschte Währung in vielen Berichten erreichen kann. Die Konversion erfolgt auf drei Ebenen:

## Seitenebene

Sie können die Variable [`currencyCode`](/help/implement/vars/config-vars/currencycode.md) verwenden, um die gewünschte Währung auf jeder Seite festzulegen. Wenn die Währung auf der Seite nicht mit der Ziel-Report Suite-Währung übereinstimmt, führt Adobe eine Währungsumrechnung zur Report Suite-Währung durch, die auf dem Wechselkurs des aktuellen Tages basiert. Die umgerechnete Währung wird erfasst.

## Report Suite-Ebene

Jede Report Suite verfügt über eine **Basiswährung**. Diese Währung bestimmt den Kontext aller Währungsmetriken (z. B[ „Umsatz](/help/components/metrics/revenue.md)). Alle Währungsdaten werden in der Basiswährung der Report Suite gespeichert.

