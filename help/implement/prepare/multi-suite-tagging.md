---
description: Erfahren Sie, wie Sie Multi-Suite-Tagging implementieren, um Bildanforderungen an mehrere Report Suites zu senden.
title: Implementieren von Multi-Suite-Tagging
feature: Implementation Basics
exl-id: c7fb0478-97e1-4367-8742-e7539f6f82e7
role: Admin, Developer, Leader
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 93%

---

# Implementieren von Multi-Suite-Tagging

Mit [Multi-Suite-Tagging](/help/admin/admin/c-manage-report-suites/rollup-report-suite.md) können Sie Bildanforderungen nicht nur an eine globale Report Suite, sondern auch an einzelne untergeordnete Report Suites senden, damit Sie Untergruppen der globalen Report Suite-Daten Ihres Unternehmens verschiedenen Endbenutzern bereitstellen können.

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
> [Virtual Report Suites](/help/components/vrs/vrs-about.md), mit denen Sie auch Untergruppen der globalen Report Suite-Daten Ihres Unternehmens für verschiedene Endbenutzer bereitstellen können, führen nicht zu sekundären Server-Aufrufen.

## Sollte ich Multi-Suite-Tagging oder Virtual Report Suites implementieren?

Die Verwendung von Virtual Report Suites anstelle von Multi-Suite-Tagging ist häufig eine Best Practice, aber der beste Report Suite-Ansatz für Ihre Organisation hängt von Ihren Geschäftsanforderungen ab.

Informationen dazu, ob Virtual Report Suites Ihr bestmöglicher Ansatz sind, finden Sie unter [Virtual Report Suites und Überlegungen zum Multi-Suite-Tagging](/help/components/vrs/vrs-considerations.md). Siehe auch [Virtual Report Suites vs. , Multi-Suite-Tagging](/help/components/vrs/vrs-about.md#section_317E4D21CCD74BC38166D2F57D214F78) mit einem Vergleich von Multi-Suite-Tagging und Virtual Report Suite-Funktionalität.
