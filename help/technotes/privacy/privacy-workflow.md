---
description: Erläutert die Schritte, mit denen Sie Ihre Adobe Analytics-Implementierung so aktivieren, dass sie die Zugriffs- und Löschrechte betroffener Personen in Bezug auf den Datenschutz unterstützt.
title: Workflow zum Datenschutz
feature: Data Governance
role: Admin
exl-id: c364b364-6d77-4b2c-88ab-65daf812f242
TQID: 'https://experienceleague.adobe.com/n0zqbcuPD2lvtgYNtdQx5VsBl-FrmzfqU-z2iIn83hg'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
    internal-label: Integrations
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
    internal-label: Data configuration and collection
subfeature_v2:
  - id: b99602d0-836e-4dbb-979f-c0dec53f883c
    internal-label: Privacy
  - id: f7fb4c71-5c39-4655-ba2d-b3b189287ab7
    internal-label: Data governance
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 9a50beeb0aa51cf9f4baf212566947c14029ce8e
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 59%
---
# Workflow zum Datenschutz

Dieser Workflow erläutert die Schritte, die Sie durchführen müssen, damit Ihre Adobe Analytics-Implementierung bereit ist, die Datenschutz-Zugriffs- und Löschrechte betroffener Personen zu unterstützen.

1. Beginnen Sie mit dem [Überblick über Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=de) in Adobe Experience Platform, um sich einen Überblick darüber zu verschaffen, welche Fragen gestellt werden müssen, bevor Sie Ihre Analytics-Daten kennzeichnen.
1. **Legen Sie Ihre Richtlinie zur Datenaufbewahrung fest.** Eine Richtlinie zur Datenaufbewahrung ist erforderlich, damit Adobe Zugriffs-/Löschanfragen für Datenschutzdaten bearbeiten kann.  Weitere Informationen finden Sie unter [Häufig gestellte Fragen zur Datenspeicherung](/help/technotes/data-retention.md). Um die Privacy-Services-API verwenden zu können, müssen Sie sicherstellen, dass die Datenspeicherung in Adobe Analytics festgelegt ist.
1. **Machen Sie sich mit den Datenschutz-Kennzeichnungen, Adobe Analytics-IDs und Namespaces vertraut.** Siehe [Datenschutzbeschriftungen für Analytics-Variablen](/help/admin/tools/privacy-labeling/labels.md) und [Best Practices für Beschriftungen](/help/admin/tools/privacy-labeling/best-practices.md).
1. **Weisen Sie jeder Variablen in einer Report Suite Beschriftungen zu Identität, Vertraulichkeit und Data Governance zu.** Die Beschriftung muss jedes Mal überprüft werden, wenn eine neue Report Suite erstellt wird oder in einer vorhandenen Report Suite eine neue Variable aktiviert wird. Sie sollten die Beschriftung auch dann prüfen, wenn neue Lösungsintegrationen aktiviert werden, da sie neue Variablen aufzeigen können, für die möglicherweise eine Beschriftung erforderlich ist. Durch eine erneute Implementierung Ihrer Mobile Apps oder Websites kann sich die Art und Weise der Verwendung vorhandener Variablen ändern. Dadurch kann ebenfalls eine Aktualisierung der Beschriftungen erforderlich sein. Siehe [Beschriften von Report Suite-Daten](/help/admin/tools/privacy-labeling/namespaces.md).
1. **Stellen Sie eine Verbindung zur Datenschutz-API von Adobe her und reichen Sie Zugriffs- und Löschanfragen ein.** Als Adobe Analytics-Kunde können Sie einzelne Datenschutzanfragen für den Zugriff auf oder die Löschung von Kundendaten durch einen Aufruf der [ Adobe Experience Privacy Service-API ](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html?lang=de). Sie können in den Anfragen neben den entsprechenden Namespace-IDs (Datenquellen-IDs) beliebige Analytics-IDs hinzufügen (siehe [Best Practices für Beschriftungen](/help/admin/tools/privacy-labeling/best-practices.md)).
1. **Anzeigen und Verwalten der Datenschutzeinstellungen Ihrer Report Suite.** Siehe [Anzeigen der Data Governance-Einstellungen einer Report Suite](/help/admin/tools/privacy-labeling/view-settings.md).
