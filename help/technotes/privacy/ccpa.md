---
description: Dieses Dokument beschreibt, welche Schritte Sie in Adobe Analytics durchführen müssen, um CCPA-Zugriffs- und -Löschberechtigungen von Datensubjekten zu unterstützen.
title: Adobe Analytics und der CCPA
feature: Data Governance
role: Admin
exl-id: 1f37e72b-99e4-4833-a506-98c8ec415757
TQID: https://experienceleague.adobe.com/medgbA9EBG0fE2xttZ7HLKT42-RBr7rlMGGGGrAyoKw
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 476
ht-degree: 88%

---

# Adobe Analytics und der CCPA

Dieses Dokument beschreibt, welche Schritte Sie in Adobe Analytics durchführen müssen, um CCPA-Zugriffs- und -Löschberechtigungen von Datensubjekten zu unterstützen.

## Adobe-Übersicht

>[!IMPORTANT]
>
>Der Inhalt dieses Dokuments ist keine Rechtsberatung und soll keine Rechtsberatung ersetzen. Wenden Sie sich zur Unterstützung in CCPA-Fragen an die Rechtsabteilung Ihres Unternehmens.

Am 1. Januar 2020 tritt der California Consumer Privacy Act (CCPA) in Kraft. Weitere Informationen zu den Änderungen bei Adobe und den Auswirkungen auf Sie als Adobe-Kunde finden Sie im [Datenschutzzentrum von Adobe](https://www.adobe.com/de/privacy.html).

Wenn Adobe einem Unternehmen Software und Services bereitstellt, fungiert Adobe als Auftragsverarbeiter für alle personenbezogenen Daten, die wir im Rahmen dieser Services im Namen unserer Kunden empfangen und speichern. Als Datenverarbeiter verarbeitet Adobe personenbezogene Daten gemäß den gewährten Berechtigungen und Anweisungen Ihres Unternehmens (z. B. über Angaben in Ihrer Vereinbarung mit Adobe).

Als Datenverantwortlicher legen Sie fest, welche personenbezogenen Daten Adobe in Ihrem Namen verarbeitet und speichert. Wenn Sie Adobe Experience Cloud-Lösungen nutzen, hostet Adobe abhängig von den verwendeten Lösungen und den Informationen, die Sie an Ihr Adobe Experience Cloud-Konto senden, möglicherweise personenbezogene Daten für Sie. Eine Liste mit Beispielen finden Sie unter [Adobe Experience Cloud-Datenschutz.](https://www.adobe.com/de/privacy/experience-cloud.html#collect)

## So verarbeitet Adobe CCPA-Daten

Adobe Experience Cloud bietet eine integrierte Lösung, die die Data-Governance-Infrastruktur Ihrer Marke mit den Adobe-Tools zur Erstellung und Verwaltung von Kundenerlebnissen verbindet. Die Data-Governance-Funktionen von Adobe Experience Cloud ermöglichen direkte Verbindungen zwischen Data-Governance-Richtlinie und Datennutzung.

Machen Sie sich mit der [DSGVO-Verarbeitung in Adobe Analytics](https://www.adobe.com/de/data-analytics-cloud/analytics/general-data-protection-regulation.html) vertraut. Dort werden die Schritte zur Datenschutzbereitschaft und zur Integration in die Privacy Service API von Adobe Experience Cloud erläutert.

## CCPA-Bereitschaft und Ihre Adobe Analytics-Daten

Wir wissen, dass Sie die individuellen Daten Ihrer Report Suites am besten kennen. Deshalb bietet Adobe Ihnen die Möglichkeit, Ihre Data-Governance-Einstellungen und -Präferenzen selbst zu definieren.
Hierzu umfasst Adobe Analytics eine Data-Governance-Benutzeroberfläche, über die Sie als Datenverantwortlicher [Datenschutzbeschriftungen](/help/admin/tools/privacy-labeling/labels.md#data-governance-labels) zu Ihren Analytics Report Suites sowie allen Dimensionen und Metriken in diesen Report Suites festlegen können. Sie können die Spalten in Ihrem Datensatz identifizieren, die direkt identifizierbare Daten oder indirekt identifizierbare Daten enthalten, damit Sie Ihre Zugriffs- und Löschanfragen für diese Daten senden können. Für jede Anfrage werden die in der Data Governance-Benutzeroberfläche von Analytics definierten Kennzeichnungen für die spezifische Kennung berücksichtigt, die dieser Anfrage entspricht.

Weitere Informationen zum Festlegen von Beschriftungen finden Sie unter [Kennzeichnen von Report Suite-Daten](/help/admin/tools/privacy-labeling/labeling-overview.md).
