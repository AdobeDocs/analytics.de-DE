---
description: Dieses Dokument beschreibt, welche Schritte Sie in Adobe Analytics durchführen müssen, um CCPA-Zugriffs- und -Löschberechtigungen von Datensubjekten zu unterstützen.
title: Adobe Analytics und der CCPA
feature: Data Governance
role: Admin
exl-id: 1f37e72b-99e4-4833-a506-98c8ec415757
TQID: 'https://experienceleague.adobe.com/medgbA9EBG0fE2xttZ7HLKT42-RBr7rlMGGGGrAyoKw'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
subfeature_v2:
  - id: b99602d0-836e-4dbb-979f-c0dec53f883c
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 301a0341e725ca15f1700046528ea5f42969add4
workflow-type: tm+mt
source-wordcount: 474
ht-degree: 63%

---

# Adobe Analytics und der CCPA

Dieses Dokument beschreibt, welche Schritte Sie in Adobe Analytics durchführen müssen, um CCPA-Zugriffs- und -Löschberechtigungen von Datensubjekten zu unterstützen.

## Adobe-Übersicht

>[!IMPORTANT]
>
>Der Inhalt dieses Dokuments ist keine Rechtsberatung und soll keine Rechtsberatung ersetzen. Wenden Sie sich zur Unterstützung in CCPA-Fragen an die Rechtsabteilung Ihres Unternehmens.

Am 1. Januar 2020 tritt der California Consumer Privacy Act (CCPA) in Kraft. Weitere Informationen zu den Änderungen bei Adobe und den Auswirkungen auf Sie als Adobe-Kunde finden Sie im [Datenschutzzentrum von Adobe](https://www.adobe.com/de/privacy.html).

Wenn Adobe einem Unternehmen Software und Services bereitstellt, fungiert Adobe als Auftragsverarbeiter für alle personenbezogenen Daten, die wir im Rahmen dieser Services im Namen unserer Kunden empfangen und speichern. Als Datenverarbeiter verarbeitet Adobe personenbezogene Daten gemäß den gewährten Berechtigungen und Anweisungen Ihres Unternehmens (z. B. über Angaben in Ihrer Vereinbarung mit Adobe).

Als Datenverantwortlicher legen Sie fest, welche personenbezogenen Daten Adobe in Ihrem Namen verarbeitet und speichert. Wenn Sie Adobe CX Enterprise-Lösungen verwenden, kann Adobe personenbezogene Daten für Sie hosten, je nachdem, welche Lösungen Sie verwenden und welche Informationen Sie an Ihr Adobe CX Enterprise-Konto senden möchten. Eine Liste mit Beispielen finden Sie unter [Adobe CX Enterprise-Datenschutz.](https://www.adobe.com/de/privacy/experience-cloud.html#collect)

## So verarbeitet Adobe CCPA-Daten

Adobe CX Enterprise bietet eine integrierte Lösung, die die Data Governance-Infrastruktur Ihrer Marke mit den Adobe-Tools verbindet, die zum Erstellen und Verwalten von Kundenerlebnissen verwendet werden. Die Data Governance-Funktionen von Adobe CX Enterprise ermöglichen eine direkte Verknüpfung der Data Governance-Richtlinien mit der Datennutzung.

Machen Sie sich mit dem Thema [Handhabung der DSGVO durch Adobe Analytics](https://www.adobe.com/de/data-analytics-cloud/analytics/general-data-protection-regulation.html) vertraut, in dem die Schritte zur Einhaltung der Datenschutzbestimmungen und zur Integration in die Adobe CX Enterprise Privacy Service-API erläutert werden.

## CCPA-Bereitschaft und Ihre Adobe Analytics-Daten

Wir wissen, dass Sie die individuellen Daten Ihrer Report Suites am besten kennen. Deshalb bietet Adobe Ihnen die Möglichkeit, Ihre Data-Governance-Einstellungen und -Präferenzen selbst zu definieren.
Hierzu umfasst Adobe Analytics eine Data-Governance-Benutzeroberfläche, über die Sie als Datenverantwortlicher [Datenschutzbeschriftungen](/help/admin/tools/privacy-labeling/labels.md#data-governance-labels) zu Ihren Analytics Report Suites sowie allen Dimensionen und Metriken in diesen Report Suites festlegen können. Sie können die Spalten in Ihrem Datensatz identifizieren, die direkt identifizierbare Daten oder indirekt identifizierbare Daten enthalten, damit Sie Ihre Zugriffs- und Löschanfragen für diese Daten senden können. Für jede Anfrage werden die in der Data Governance-Benutzeroberfläche von Analytics definierten Kennzeichnungen für die spezifische Kennung berücksichtigt, die dieser Anfrage entspricht.

Weitere Informationen zum Festlegen von Beschriftungen finden Sie unter [Kennzeichnen von Report Suite-Daten](/help/admin/tools/privacy-labeling/labeling-overview.md).
