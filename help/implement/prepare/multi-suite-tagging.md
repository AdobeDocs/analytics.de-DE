---
description: Erfahren Sie, wie Sie Multi-Suite-Tagging implementieren, um Bildanforderungen an mehrere Report Suites zu senden.
title: Implementieren von Multi-Suite-Tagging
feature: Implementation Basics
exl-id: c7fb0478-97e1-4367-8742-e7539f6f82e7
role: Admin, Developer, Leader
TQID: https://experienceleague.adobe.com/djrzQEjvc--wnh2wR1HNV-LVEn6RPcyiaLKLha5pfSY
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: c77ba355-6681-41fe-b719-563d3f507fdb
  - id: df312454-73c4-43f6-a90e-18f5043f074c
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 302
ht-degree: 93%

---

# Implementieren von Multi-Suite-Tagging

Mit [Multi-Suite-Tagging](/help/admin/tools/manage-rs/rollup-report-suite.md) können Sie Bildanforderungen nicht nur an eine globale Report Suite, sondern auch an einzelne untergeordnete Report Suites senden, damit Sie Teilmengen der globalen Report Suite-Daten Ihres Unternehmens verschiedenen Endbenutzern bereitstellen können.

Um Multi-Suite-Tagging zu implementieren, müssen Sie die Report Suite-ID (RSID) für die globale Report Suite sowie die RSIDs für die entsprechenden untergeordneten Report Suites in den Trackingcode für Ihre Webseiten und Apps aufnehmen.

* Geben Sie bei Tags-Implementierungen in Adobe Experience Platform für die [[!DNL Analytics] Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html?lang=de) jede der Report Suites an.

* Trennen Sie bei älteren JavaScript- und mobilen SDK-Implementierungen die RSIDs durch Kommas und keine Leerzeichen (`rsid1,rsid2,rsid3` usw.).

* Verwenden Sie für andere Implementierungstypen die erforderliche Syntax, um mehrere RSIDs aufzulisten.

>[!TIP]
>
> Es empfiehlt sich, zuerst die globale Report Suite oder die Report Suite-ID aufzulisten.

Multi-Suite-Tagging führt zu mehreren Server-Aufrufen für jede Bildanforderung: einen primären Aufruf an die globale Report Suite und einen sekundären Aufruf für jede untergeordnete Report Suite.

>[!NOTE]
>
> [Virtual Report Suites](/help/components/vrs/vrs-about.md), mit denen Sie auch Teilmengen der globalen Report Suite-Daten Ihres Unternehmens für verschiedene Endbenutzer bereitstellen können, führen nicht zu sekundären Server-Aufrufen.

## Sollte ich Multi-Suite-Tagging oder Virtual Report Suites implementieren?

Die Verwendung von Virtual Report Suites anstelle von Multi-Suite-Tagging ist häufig eine Best Practice, aber der beste Report Suite-Ansatz für Ihre Organisation hängt von Ihren Geschäftsanforderungen ab.

Informationen dazu, ob Virtual Report Suites Ihr bestmöglicher Ansatz sind, finden Sie unter [Virtual Report Suites und Überlegungen zum Multi-Suite-Tagging](/help/components/vrs/vrs-considerations.md). Siehe auch [Virtual Report Suites vs. , Multi-Suite-Tagging](/help/components/vrs/vrs-about.md#section_317E4D21CCD74BC38166D2F57D214F78) mit einem Vergleich von Multi-Suite-Tagging und Virtual Report Suite-Funktionalität.
