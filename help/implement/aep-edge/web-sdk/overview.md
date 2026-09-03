---
title: Implementieren von Adobe Analytics mit dem Adobe Experience Platform Web SDK
description: Verwenden Sie die Web-SDK, um Daten an Adobe Analytics zu senden.
exl-id: 97f8d650-247f-4386-b4d2-699f3dab0467
feature: Implementation Basics
role: Admin, Developer, Leader
TQID: 'https://experienceleague.adobe.com/8p05Bfxo37frjI9pPQOPHPtzt8yxPmFXj-nYW00IYfE'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
subfeature_v2:
  - id: b3e5f43e-2e2f-43c0-810a-044a5f91e31a
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 242
ht-degree: 42%

---

# Implementieren von Adobe Analytics mit dem Adobe Experience Platform Web SDK

Sie können das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/web-sdk/home.html) verwenden, um Daten an Adobe Analytics zu senden. Es gibt zwei Hauptmethoden zur Implementierung der Web-SDK, und jede Methode verfügt über zwei Implementierungstypen:

| | **Migration aus AppMeasurement** | **Clean Web SDK-Implementierung** |
| --- | --- | --- |
| **Verwenden von Tags** | [Migrieren von der Analytics-Erweiterung zur Web SDK-Erweiterung](analytics-extension-to-web-sdk.md) | [Senden von Daten an Adobe Analytics mithilfe der Web SDK-Erweiterung](web-sdk-tag-extension.md) |
| **Verwenden von JavaScript** | [Migrieren von AppMeasurement zur Web SDK JavaScript-Bibliothek](appmeasurement-to-web-sdk.md) | [Senden von Daten an Adobe Analytics mithilfe der Web SDK JavaScript-Bibliothek](web-sdk-javascript-library.md) |

Wenn Ihr Unternehmen eine neue Web SDK-Implementierung benötigt und in Zukunft Customer Journey Analytics verwenden möchte, empfiehlt Adobe eine saubere Web SDK-Implementierung unter Verwendung Ihres eigenen Schemas. Siehe [Aufnehmen von Daten über die Adobe Experience Platform Web &#x200B;](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk) im Customer Journey Analytics-Benutzerhandbuch.

## Zusätzliche Ressourcen

Tags können in hohem Maße angepasst werden. Erfahren Sie, wie Sie Adobe Analytics optimal nutzen können, indem Sie die richtigen Daten in Ihre Implementierung aufnehmen.

- [Tags-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=de#): Hier erfahren Sie, wie die Benutzeroberfläche funktioniert und welche Erweiterungen verfügbar sind.

- [Dokumentation zu Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/web-sdk.html?lang=de)
