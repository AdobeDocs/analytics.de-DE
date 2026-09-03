---
title: Optionen zum Abmildern der Auswirkungen von Beschränkungen für Browser-Cookies
description: Erfahren Sie, wie Sie die Auswirkungen von Beschränkungen für Browser-Cookies reduzieren können, um die Datenerfassung für Adobe Analytics zu verbessern.
feature: Data Configuration and Collection
exl-id: 81cf3f0c-4871-435d-bcc9-bcff5c682f05
role: Admin
TQID: https://experienceleague.adobe.com/f6gcSRLmsupsIVKYH-bF1T7vuVhoj9Ef8zVh3t6vU2Q
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2:
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 590
ht-degree: 98%

---

# Optionen zum Abmildern der Auswirkungen von Beschränkungen für Browser-Cookies

In diesem Dokument werden Optionen zur Beibehaltung einer beständigen Besucheridentifizierung über Eigenschaften und Lösungen hinweg besprochen, da in den wichtigsten Browsern Tracking-Präventionsmaßnahmen für Cookies implementiert sind.

Adobe Analytics verwendet First-Party-Cookies, um die Aktivitäten eines Besuchers auf einer Site aufzuzeichnen. Analytics nutzt außerdem Third-Party-Cookies, um die Offsite-Aktivitäten eines Besuchers zu verstehen, z. B. Aktivitäten in anderen Domänen in Ihrem Besitz. Third-Party-Cookies werden in vielen Browsern blockiert und werden nach dem bevorstehenden Ende der Unterstützung durch Chrome (derzeit für Ende 2024 geplant) weitgehend nicht mehr verfügbar sein. First-Party-Cookies sind in allen Browsern erlaubt, laufen jedoch unter Safari und anderen Browsern unter den [ITP-Tracking-Präventionsmaßnahmen](https://webkit.org/tracking-prevention) von Apple begrenzt ab. Weitere Informationen zu aktuellen Einschränkungen bei Browser-Cookies finden Sie unter [Adobe Analytics und Browser-Cookies](cookies.md).

Diese Browser-Beschränkungen spiegeln einen allgemeinen Übergang vom anonymen Third-Party-Tracking zum expliziten Austausch von Informationen zwischen Benutzern und Marken wider, denen sie vertrauen. Um diesen Schritt zu unterstützen, bietet Adobe Möglichkeiten für Kunden, herkömmliche Cookies zu ergänzen, indem dauerhafte Kennungen einbezogen werden, die über ihre First-Party-Beziehungen erfasst werden.

## Customer Journey Analytics und geräteübergreifende Analyse

[Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=de) und [geräteübergreifende Analytics](/help/components/cda/overview.md) ermöglichen es, neben Cookies auch dauerhafte Kennungen wie Hash-Anmeldungen einzuschließen. Auf diese Weise können Sie die Customer Journey geräteübergreifend und im Fall von Customer Journey Analytics auch über Online- und Offline-Kanäle hinweg nachvollziehen:

* **Customer Journey Analytics** basiert auf Adobe Experience Platform und bietet die Flexibilität, Online- und Offline-Daten in Analysis Workspace basierend auf einer beliebigen Kunden-ID zu kombinieren. Sie können für jede beliebige Analyse angeben, welche ID Sie verwenden möchten, und die Daten in Analysis Workspace untersuchen. Kunden, die Analytics Select, Prime und Ultimate verwenden, sind zum Erwerb dieses Zusatzprodukts qualifiziert.

* Die **geräteübergreifende Analyse** ist eine Erweiterung für das herkömmliche Adobe Analytics, mit der Kunden alternative Kennungen für Besucher verwenden können. Mit dieser Funktion können Sie von einer geräteorientierten Ansicht zu einer personenorientierten Ansicht wechseln. Die geräteübergreifende Analyse steht Analytics Ultimate-Kunden zur Verfügung.

## Server-seitige Datenerfassung

Die Server-seitige Erfassung bietet die Flexibilität, Ihre eigene Kennung bereitzustellen, anstatt sich bei der Festlegung von Cookies auf Browser-Mechanismen zu verlassen.

Sie können Daten Server-seitig mit der [Data Insertion-API](https://developer.adobe.com/analytics-apis/docs/1.4/guides/data-insertion/) oder der [Bulk Data Insertion-API](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/) an Analytics senden. Die Bulk Data Insertion-API wird für neue Server-seitige Implementierungen empfohlen. Einen Vergleich der beiden APIs finden Sie unter „[Welches Adobe Analytics-Tool sollte ich verwenden?](/help/analyze/get-started/which-analytics-tool.md)“.

## First-Party-Geräte-ID (FPID) mit dem Web SDK

Mit dem Adobe Experience Platform Web SDK können Sie anstelle der von Adobe generierten Experience Cloud-IDs (ECIDs) Ihre eigenen Geräte-IDs festlegen und verwalten. Diese werden als First-Party-Geräte-IDs (FPIDs) bezeichnet. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/edge/identity/first-party-device-ids.html?lang=de).

## Weitere Informationen

Praktische Schritte, mit denen Ihr Unternehmen die Abkehr von Third-Party-Cookies einleiten kann, finden Sie unter [Kundenakquise und -bindung in einer Welt ohne Cookies mit Adobe](https://business.adobe.com/de/solutions/cookieless.html) und in dem ausführlichen Artikel [Jenseits des Third-Party-Cookies: Ihr kompletter Leitfaden zu einer Welt ohne Third-Party-Cookies](https://business.adobe.com/content/dam/www/us/en/pdfs/Adobe_Thinking_Beyond_the_Third_Party_Cookie.pdf).

>[!MORELIKETHIS]
>
>[Adobe Analytics und Browser-Cookies](cookies.md)
