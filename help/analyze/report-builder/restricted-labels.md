---
title: Was sind eingeschränkte Beschriftungen in Report Builder
description: Beschreibt eingeschränkte Beschriftungen in Report Builder
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: aa2182f9-a140-4239-b2fb-f723e2767260
source-git-commit: c333a82848ed74a002a07f8c5e2857426a78425c
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 49%

---

# Eingeschränkte Beschriftungen in Report Builder

Im Allgemeinen werden die Einstellungen für die Data Governance in Adobe Analytics von Adobe Experience Platform übernommen. Die Integration zwischen Adobe Analytics und Adobe Experience Platform Data Governance ermöglicht die Kennzeichnung sensibler Adobe Analytics-Daten und die Durchsetzung von Datenschutzrichtlinien.

Datenschutzbeschriftungen und -richtlinien, die für vom Experience Platform genutzte Datensätze erstellt wurden, können im Workflow von Adobe Analytics Report Suites angezeigt werden. Diese Beschriftungen stoppen oder warnen Benutzer, die Metriken und/oder Dimensionen aus sensiblen Feldern erstellen. Weiterführende Informationen über Datensätze finden Sie in der [Datensatzübersicht](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=de)

Darüber hinaus werden beim Exportieren von Daten aus Adobe Analytics (über Reporting, Export, API usw.) Warnhinweise oder Beschriftungen hinzugefügt, die Benutzer darauf hinweisen, dass ein Bericht sensible Informationen enthält, die auf bestimmte Weise behandelt werden müssen.

Durch diese Integration können Sie die Compliance einfacher verwalten. Datenverantwortliche in Ihrem Unternehmen können Richtlinien festlegen, um die Nutzung zu beschränken. Dadurch können Ihre Adobe Analytics-Benutzer Daten sicherer nutzen, da sie wissen, dass sie den von den Datenverwaltern festgelegten Richtlinien entsprechen.

Weitere Informationen finden Sie unter [Adobe Analytics und Data Governance](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-privacy/privacy-overview.html?lang=de)

## Anzeigen eingeschränkter Daten in Report Builder

In Adobe Analytics werden zwei Adobe-definierte Richtlinien angezeigt, die sich auf die Berichterstellung, den Download und die Freigabe auswirken:

* Analytics erzwingen-Richtlinie
* Download erzwingen-Richtlinie

Komponenten, die von diesen Richtlinien betroffen sind, sind grau ausgeblendet. Wenn Sie den Mauszeiger über eine Komponente bewegen, auf die eine Richtlinie angewendet wurde, wird ein Hinweis angezeigt, der Folgendes angibt: **Auf dieses Feld wurden Richtlinien angewendet, die die Verwendung dieser Daten untersagen.** Weitere Informationen finden Sie unter [Beschriftungen und Richtlinien](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/data-governance.html?lang=de).

![Der Hinweis zu verbotenen Datennutzungen.](assets/rb-restricted-label.png)

## Aktualisieren von Berichten mit eingeschränkten Daten

Wenn ein Anwender einen Report Builder-Bericht mit Datenelementen erstellt hat, die später eingeschränkt werden, wird bei der Aktualisierung des Berichts eine Fehlermeldung angezeigt.

![Die Fehlermeldung, die angezeigt wird, nachdem Datenelemente später eingeschränkt wurden.](assets/error-restricted-data.png)
