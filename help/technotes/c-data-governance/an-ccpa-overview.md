---
description: Dieses Dokument beschreibt, welche Schritte Sie in Adobe Analytics durchführen müssen, um CCPA-Zugriffs- und -Löschberechtigungen von Datensubjekten zu unterstützen.
title: Adobe Analytics und der CCPA
feature: Data Governance
exl-id: 1f37e72b-99e4-4833-a506-98c8ec415757
source-git-commit: 1ca7040156f7f2105a9625f921de3d90b4175056
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 100%

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

Die Adobe Cloud Platform (ACP) bietet eine integrierte Lösung, die die Data-Governance-Infrastruktur Ihrer Marke mit den Adobe-Tools zur Erstellung und Verwaltung von Kundenerlebnissen verbindet. Die Data-Governance-Funktionen der Adobe Cloud Platform ermöglichen direkte Verbindungen zwischen Data-Governance-Richtlinie und Datennutzung.

Machen Sie sich mit der [DSGVO-Verarbeitung in Adobe Analytics](https://www.adobe.com/de/data-analytics-cloud/analytics/general-data-protection-regulation.html) vertraut. Dort werden die Schritte zur Datenschutzbereitschaft und zur Integration in die Privacy Service API von Adobe Experience Cloud erläutert.

## CCPA-Bereitschaft und Ihre Adobe Analytics-Daten

Wir wissen, dass Sie die individuellen Daten Ihrer Report Suites am besten kennen. Deshalb bietet Adobe Ihnen die Möglichkeit, Ihre Data-Governance-Einstellungen und -Präferenzen selbst zu definieren.
Hierzu umfasst Adobe Analytics eine Data-Governance-Benutzeroberfläche, über die Sie als Datenverantwortlicher [Datenschutzbeschriftungen](/help/technotes/c-data-governance/data-labeling/gdpr-labels.md#data-governance-labels) zu Ihren Analytics Report Suites sowie allen Dimensionen und Metriken in diesen Report Suites festlegen können. Sie können die Spalten in Ihrem Datensatz festlegen, die direkt oder indirekt identifizierbare Daten enthalten, damit Sie Zugriffs- und Löschanfragen zu diesen Daten einreichen können. Bei jeder Anfrage werden die in der Analytics Data Governance-Benutzeroberfläche definierten Beschriftungen für die spezifische ID, die mit der Anfrage übereinstimmt, berücksichtigt.

Weitere Informationen finden Sie unter [Report Suite-Daten beschriften](/help/technotes/c-data-governance/data-labeling/gdpr-setup-reportsuite.md).

## Voraussetzungen

* Machen Sie sich mit der [DSGVO-Terminologie](/help/admin/c-data-governance/gdpr-terminology.md) vertraut.
* Verbinden Sie Ihr Anmeldeunternehmen ggf. mit einer Experience Cloud-Organisation. Wenden Sie sich an die Adobe-Kundenunterstützung und lesen Sie die Informationen unter [Organisationen und Kontoverknüpfung.](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/organizations.html?lang=de)
* Legen Sie für jede Report Suite eine Richtlinie zur Datenaufbewahrung fest, damit CCPA-Zugriffs- und -Löschanfragen bearbeitet werden können.

   Adobe Analytics kann Sie bei der Verarbeitung von Anfragen an die Privacy Services API – also bei der Verarbeitung von Zugriffs- oder Löschanfragen, die Sie von Ihren Endbenutzern erhalten – nicht unterstützen, wenn in Adobe Analytics kein Zeitraum zur Datenaufbewahrung festgelegt wurde. Bitte wenden Sie sich an Ihren Customer Success Manager, um die Speicherdauer Ihrer Daten festzulegen.

* Überprüfen Sie Ihre Berechtigungen: Um die Analytics-Benutzeroberfläche zur Data-Governance-Verwaltung zu verwenden, müssen Sie Adobe Analytics-Administrator sein.
* Erwägen Sie die Implementierung der [Managementvariablen zur Einwilligung](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/privacy-reporting.md), um den Genehmigungsstatus auf Trefferebene zu verfolgen.
