---
description: Besondere Hinweise bei der Verwendung von Virtual Report Suites in A4T und Adobe Analytics
title: Virtual Report Suites und Analytics for Target (A4T)
feature: VRS
exl-id: b81e5100-f512-4219-a8ab-5d7f6219d206
TQID: https://experienceleague.adobe.com/SIJbZiyHFtGFUrlno5-Kov3kDP4QOXREW00jyDsIGFI
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 137
ht-degree: 100%

---

# Virtual Report Suites und Analytics for Target (A4T)

Beachten Sie diese Einschränkungen bei der Verwendung von Virtual Report Suites im Kontext von Adobe Target:

* Sie können direkt aus Target keine Daten an eine Virtual Report Suite senden, sondern nur an eine echte Report Suite.
* Sie können in einer Virtual Report Suite Berichte zu A4T-Aktivitäten erstellen. Die A4T-Daten sind jedoch auf die Zeilen beschränkt, die mit dem Virtual Report Suite-Segment (und allen anderen angewendeten Segmenten) übereinstimmen. Wenn Sie beispielsweise eine Virtual Report Suite für Ihre EMEA-Kunden erstellt haben, spiegeln die A4T-Daten in dieser Virtual Report Suite nur die Target-Daten für Ihre EMEA-Kunden wider.
* Sie können keine Segmente aus einer Virtual Report Suite wieder in Target zur Aktivierung veröffentlichen.
