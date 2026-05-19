---
description: Sie können Document Cloud-Daten in Adobe Analytics anzeigen
title: Konfigurieren von Document Cloud-Berichten
feature: Admin Tools
exl-id: eb58d011-c4b0-4c0c-9241-83b2bccc2c77
TQID: https://experienceleague.adobe.com/2X5YQxmTsMYdnwSWVL4EMr1K1aV9UM6FRMHa2P--Xuc
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 140
ht-degree: 28%

---

# Konfigurieren von Document Cloud-Berichten

Sie können PDF-spezifische Dimensionen und Metriken konfigurieren, die in Adobe Analytics verfügbar sein sollen.

## Komponenten, die beim Aktivieren der Berichterstellung für PDF hinzugefügt werden

Wenn PDF-Berichte ordnungsgemäß konfiguriert sind, sind in Adobe Analytics die folgenden Dimensionen und Metriken verfügbar:

**Dimensionen:**

* PDF-Suchbegriff

* PDF-Zoomfaktor

* PDF-Aktion

* PDF-Seitennummer

* PDF-Dateiname

**Metriken:**

* PDF-Ansichten

* PDF-Seitenansichten

* PDF-Downloads

* PDF-Suche

* Verwendete PDF-Lesezeichen

* Kopierter PDF-Text

* PDF-Druck

## Aktivieren von PDF-Berichten in Adobe Analytics

1. Navigieren Sie **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **`<select report suite>`** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Document Cloud-Verwaltung]** > [!UICONTROL **Document Cloud-Reporting**].

1. Wählen Sie auf der Seite &quot;Adobe Document Cloud-Verwaltung [!UICONTROL **die Option &quot;PDF-Berichte**].

1. Um Adobe Document Cloud für die Übertragung von Daten an Adobe Analytics zu konfigurieren, verwenden Sie die [Adobe Document Cloud JavaScript-SDK](https://www.adobe.io/apis/documentcloud/dcsdk.html).
