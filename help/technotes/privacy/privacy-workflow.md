---
description: Erläutert die Schritte, mit denen Sie in Ihrer Adobe Analytics-Implementierung die Zugriffs- und Löschrechte der betroffenen Personen für den Datenschutz unterstützen.
title: Workflow zum Datenschutz
feature: Data Governance
role: Admin
exl-id: c364b364-6d77-4b2c-88ab-65daf812f242
TQID: https://experienceleague.adobe.com/n0zqbcuPD2lvtgYNtdQx5VsBl-FrmzfqU-z2iIn83hg
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 333
ht-degree: 59%

---

# Workflow zum Datenschutz

Dieser Workflow beinhaltet die erforderlichen Schritte, die Sie durchführen müssen, damit Ihre Adobe Analytics-Implementierung die Datenschutz-Zugriffs- und -Löschberechtigungen von Datensubjekten unterstützt.

1. Beginnen Sie mit dem [Überblick über Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=de) in Adobe Experience Platform, um sich einen Überblick darüber zu verschaffen, welche Fragen gestellt werden müssen, bevor Sie Ihre Analytics-Daten kennzeichnen.
1. **Legen Sie Ihre Richtlinie zur Datenaufbewahrung fest.** Eine Richtlinie zur Datenaufbewahrung ist erforderlich, damit Adobe Zugriffs-/Löschanfragen für Datenschutzdaten bearbeiten kann.  Weitere Informationen finden Sie unter [Häufig gestellte Fragen zur Datenspeicherung](/help/technotes/data-retention.md). Um die Privacy Services-API verwenden zu können, müssen Sie sicherstellen, dass die Datenspeicherungsdauer in Adobe Analytics festgelegt ist.
1. **Machen Sie sich mit den Datenschutz-Kennzeichnungen, Adobe Analytics-IDs und Namespaces vertraut.** Siehe [Datenschutzbeschriftungen für Analytics-Variablen](/help/admin/tools/privacy-labeling/labels.md) und [Best Practices für Beschriftungen](/help/admin/tools/privacy-labeling/best-practices.md).
1. **Weisen Sie jeder Variablen in einer Report Suite Beschriftungen zu Identität, Vertraulichkeit und Data Governance zu.** Die Beschriftung muss jedes Mal überprüft werden, wenn eine neue Report Suite erstellt wird oder in einer vorhandenen Report Suite eine neue Variable aktiviert wird. Sie sollten die Beschriftung auch dann überprüfen, wenn neue Lösungsintegrationen aktiviert werden, da sie neue Variablen aufzeigen können, für die möglicherweise eine Beschriftung erforderlich ist. Durch eine erneute Implementierung Ihrer Mobile Apps oder Websites kann sich die Art und Weise der Verwendung vorhandener Variablen ändern. Dadurch kann ebenfalls eine Aktualisierung der Beschriftungen erforderlich sein. Siehe [Beschriften von Report Suite-Daten](/help/admin/tools/privacy-labeling/namespaces.md).
1. **Stellen Sie eine Verbindung zur Datenschutz-API von Adobe her und reichen Sie Zugriffs- und Löschanfragen ein.** Als Adobe Analytics-Kunde können Sie einzelne Datenschutzanfragen für den Zugriff auf oder die Löschung von Kundendaten durch einen Aufruf der [ Adobe Experience Privacy Service-API ](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html?lang=de). Sie können in den Anfragen neben den entsprechenden Namespace-IDs (Datenquellen-IDs) beliebige Analytics-IDs hinzufügen (siehe [Best Practices für Beschriftungen](/help/admin/tools/privacy-labeling/best-practices.md)).
1. **Anzeigen und Verwalten der Datenschutzeinstellungen Ihrer Report Suite.** Siehe [Anzeigen der Data Governance-Einstellungen einer Report Suite](/help/admin/tools/privacy-labeling/view-settings.md).
