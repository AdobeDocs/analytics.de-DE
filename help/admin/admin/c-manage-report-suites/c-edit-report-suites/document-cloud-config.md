---
description: Sie können Document Cloud-Daten in Adobe Analytics anzeigen
title: Konfigurieren von Document Cloud-Berichten
feature: Admin Tools
exl-id: eb58d011-c4b0-4c0c-9241-83b2bccc2c77
source-git-commit: bdd9473b0ac3bd77ffeff53a095876e21ca2f4d4
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 7%

---

# Konfigurieren von Document Cloud-Berichten

Sie können PDF-spezifische Dimensionen und Metriken so konfigurieren, dass sie in Adobe Analytics verfügbar sind.

## Komponenten hinzugefügt, die beim Aktivieren der PDF-Berichterstellung hinzugefügt werden

Wenn die PDF-Berichterstellung ordnungsgemäß konfiguriert ist, sind die folgenden Dimensionen und Metriken in Adobe Analytics verfügbar:

**Dimensionen:**

* PDF-Suchbegriff

* PDF Zoom-Level

* PDF-Aktion

* PDF-Seitenzahl

* PDF Filename

**Metriken:**

* PDF-Ansichten

* PDF Seitenansichten

* PDF-Downloads

* PDF-Suche

* Verwendete PDF-Lesezeichen

* PDF Copy Text

* PDF Print

## PDF-Reporting in Adobe Analytics aktivieren

1. Gehen Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **`<select report suite>`** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Document Cloud-Verwaltung]** > [!UICONTROL **Document Cloud-Berichterstellung**].

1. Wählen Sie auf der Seite &quot;Adobe Document Cloud-Verwaltung&quot;die Option [!UICONTROL **PDF-Berichte aktivieren**].

1. Verwenden Sie das JavaScript-SDK [Adobe Document Cloud](https://www.adobe.io/apis/documentcloud/dcsdk.html), um Adobe Document Cloud für die Datenübertragung an Adobe Analytics zu konfigurieren.
