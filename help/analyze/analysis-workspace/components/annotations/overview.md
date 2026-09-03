---
title: Anmerkungen – Überblick
description: Erfahren Sie, wie Sie Anmerkungen in Analysis Workspace verwenden.
role: User, Admin
solution: Analytics
feature: Annotations
exl-id: 722d7636-f619-479a-97f1-3da23e8f7f83
TQID: https://experienceleague.adobe.com/kVm6VfN3c-u3V2GHMz59QuB2uGi4DEozs1i-h4pJZOg
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2:
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 320
ht-degree: 82%

---

# Anmerkungen – Überblick

Mit Anmerkungen können Sie kontextbezogene Datennuancen und Erkenntnisse auf effektive Weise an andere Stakeholderinnen und Stakeholder in Ihrer Organisation übermitteln. Durch Anmerkungen können Sie Kalenderereignisse an bestimmte Dimensionen und Metriken binden. Sie können etwa zu einem Datum oder Datumsbereich Anmerkungen zu bekannten Datenproblemen, Feiertagen, Kampagnenstarts usw. machen, Anschließend können Sie Ereignisse grafisch anzeigen und sehen, ob sich Kampagnen oder andere Ereignisse auf den Traffic Ihrer Site, die Nutzung mobiler Apps, den Umsatz oder andere Metriken ausgewirkt haben.

Angenommen, Sie geben Projekte für Ihre Organisation frei. Wenn es einen merklichen Rückgang bei den Unique Visitors gegeben hat, können Sie die Anmerkung **Abnehmende Besucherzahlen** erstellen und diese auf Ihre gesamte Report Suite anwenden. Wenn Ihre Benutzenden eine Report Suite betrachten, die dieses Datum enthält, sehen sie die Anmerkung in ihren Projekten gemeinsam mit ihren Daten.

![Liniendiagramm mit hervorgehobener Anmerkung.](assets/annotation-example.png)

Anmerkungen können für Folgendes gelten:

* ein einzelnes Datum oder einen Datumsbereich.

* Ihren gesamten Datensatz oder bestimmte Metriken, Dimensionen oder Segmente.

* das Projekt, in dem Anmerkungen erstellt werden (Standard), oder alle Projekte.

* Die Report Suite, in der Anmerkungen erstellt werden (Standard), oder alle Report Suites.

Unter [Erstellen von Anmerkungen](create-annotations.md) finden Sie die verschiedenen Optionen zum Erstellen von Anmerkungen. Anschließend erstellen, ändern und speichern Sie Anmerkungen im Rahmen der [Anmerkungserstellung](create-annotations.md#annotation-builder).

Sie verwenden den [Anmerkungs-Manager](manage-annotations.md) zum Verwalten von Anmerkungen.

## Aktivieren oder Deaktivieren von Anmerkungen

Anmerkungen können auf verschiedenen Ebenen aktiviert oder deaktiviert werden:

| Ebene | Schritte |
|---|---|
| **Visualisierung** | Aktivieren oder deaktivieren Sie ![Einstellung](/help/assets/icons/Setting.svg) > **[!UICONTROL Einstellungen]** > **[!UICONTROL Anmerkungen anzeigen]**.<br/>![Aktivieren/Deaktivieren von Anmerkungen für eine Visualisierung](assets/annotations-visualization.png) |
| **Projekt** | Wählen Sie in einem Workspace-Projektmenü **[!UICONTROL Projekt]** > **[!UICONTROL Projektinformationen und -einstellungen]** aus und aktivieren oder deaktivieren Sie **[!UICONTROL Anmerkungen anzeigen]**.<br/>![Aktivieren/Deaktivieren von Anmerkungen für ein Projekt](assets/annotations-project.png) |
| **Benutzende** | Wählen Sie auf der Registerkarte **[!UICONTROL Komponenten]** die Option **[!UICONTROL Voreinstellungen]** oder im Workspace-Projektmenü die Option **[!UICONTROL Projekt]** > **[!UICONTROL Benutzervoreinstellungen]** aus. <br/>Wählen Sie unter **[!UICONTROL Voreinstellungen]** die Option **[!UICONTROL Projekte und Analysen]** aus. Wählen Sie in der linken Registerkartenleiste die Option **[!UICONTROL Daten]** aus. Aktivieren oder deaktivieren Sie unten unter der Überschrift **[!UICONTROL Freiformtabelle]** die Option **[!UICONTROL Anmerkungen anzeigen]** aus.<br/>![Aktivieren/Deaktivieren von Anmerkungen für eine Person](assets/annotations-user.png) |

<!--
# Annotations overview

Annotations in Workspace enable you to effectively communicate contextual data nuances and insights to your organization. They let you tie calendar events to specific dimensions/metrics. You can annotate a date or date range with known data issues, public holidays, campaign launches, etc. You can then graphically display events and see whether campaigns or other events have affected your site traffic, revenue, or any other metric.

For example, let's say you are sharing projects with your organization. If you had a major spike in traffic due to a marketing campaign, you could create a "Campaign launch date" annotation and scope it for your whole report suite. When your users view any data sets that included that date, they see the annotation within their projects, alongside their data.

![Annotation example](assets/annotation-example.png)

Keep this in mind:

* Annotations can be tied to a single date or to a date range.

* They can apply to your entire data set or to specified metrics, dimensions, or segments.

* They can apply to the project in which they were created (default) or to all projects.

* They can apply to the report suite in which they were created (default) or to all report suites.

## Permissions {#permissions}

By default, only Admins can create annotations. Users have rights to view annotations like they do with other other Analytics components (such as segments, calculated metrics, etc.).

However, Admins can give the [!UICONTROL Annotation Creation] permission (Analytics Tools) to users via the [Adobe Admin Console](/help/admin/admin-console/permissions/analytics-tools.md).

## Turn annotations on or off {#annotations-on-off}

Annotations can be turned on or off at several levels:

* At the Visualization level: [!UICONTROL Visualization] settings > [!UICONTROL Show annotations]

* At the Project level: [!UICONTROL Project info & settings] > [!UICONTROL Show annotations]

* At the User level: [!UICONTROL Components] > [!UICONTROL User preferences] > [!UICONTROL Data] > [!UICONTROL Show annotations]

![](assets/show-ann.png)

![](assets/show-ann2.png)
-->