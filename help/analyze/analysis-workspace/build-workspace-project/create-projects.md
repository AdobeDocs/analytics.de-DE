---
description: Erfahren Sie mehr über die Grundlagen zum Erstellen eines Projekts in Analysis Workspace
title: Erstellen von Projekten
feature: Workspace Basics
role: User, Admin
exl-id: 24193013-1361-43fc-b129-c44f207d9101
source-git-commit: 273fea86cde8880d9c9e03ac9c6a99b75f70f6cd
workflow-type: ht
source-wordcount: '770'
ht-degree: 100%

---

# Erstellen von Projekten in Analysis Workspace

[Projekte](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md) in Analysis Workspace ermöglichen Ihnen die Anzeige von geschäftskritischen Analysen, die Sie mit Stakeholdern innerhalb oder außerhalb Ihrer Organisation teilen können.

Weitere Informationen zu den ersten Schritten mit Analysis Workspace finden Sie unter [Analysis Workspace – Übersicht](/help/analyze/analysis-workspace/home.md).

In den folgenden Abschnitten wird beschrieben, wie Sie ein Projekt erstellen und die wichtigsten Bausteine für ein Analysis Workspace-Projekt hinzufügen: Bedienfelder, Visualisierungen und Komponenten.

## Erstellen eines Projekts aus einem leeren Projekt oder Bericht

1. Wählen Sie in Adobe Analytics [!UICONTROL **Arbeitsbereich**] aus.

1. Legen Sie fest, ob ein leeres Projekt oder ein Projekt aus einem Bericht erstellt werden soll:

   +++Erstellen eines leeren Projekts

   1. Wählen Sie auf der Registerkarte [!UICONTROL **Arbeitsbereich**] die Registerkarte [!UICONTROL **Projekte**] am linken Rand der Seite und wählen Sie dann [!UICONTROL **Projekt erstellen**].

   1. Legen Sie fest, ob ein leeres Projekt oder eine leere mobile Scorecard erstellt werden soll.

      * **Leeres Projekt**, wenn Sie Ihre Analyse über den Browser freigeben möchten.
      * [**Leere mobile Scorecard**](/help/analyze/mobile-app/curator.md), wenn Sie Ihre Analyse über die Mobile App Adobe Analytics-Dashboards freigeben möchten.

   1. Wählen Sie [!UICONTROL **Erstellen**] aus.

+++

   +++Erstellen eines Projekts aus einem Bericht

   1. Wählen Sie auf der Registerkarte [!UICONTROL **Arbeitsbereich**] die Registerkarte [!UICONTROL **Projekte**] am linken Rand der Seite aus.

   1. Suchen Sie nach oder navigieren Sie zu dem Bericht, den Sie verwenden möchten, und wählen Sie ihn aus, wenn er angezeigt wird.

      Eine Reihe von Standardberichten ist standardmäßig verfügbar. Darüber hinaus hat Ihr Unternehmen möglicherweise benutzerdefinierte Berichte erstellt, aus denen Sie auswählen können.

   1. Wählen Sie [!UICONTROL **Projekt**] > [!UICONTROL **Speichern**], um den Bericht als neues Projekt zu speichern.

      Weitere Informationen zu Berichten finden Sie unter „Navigieren durch die Registerkarte ,Berichte‘“ auf der [Adobe Analytics-Landingpage](/help/analyze/landing.md).

+++

1. Als Nächstes müssen Sie Ihrem Projekt Bedienfelder, Visualisierungen und Komponenten hinzufügen. Fügen Sie zunächst Bedienfelder zu Ihrem Projekt in Analysis Workspace hinzu, wie unter [Hinzufügen von Bedienfeldern zum Projekt](#add-panels-to-the-project) beschrieben. Sie können dann allen Bedienfeldern Visualisierungen hinzufügen. Schließlich können Sie allen Bedienfeldern oder Visualisierungen Komponenten hinzufügen.

## Hinzufügen von Bedienfeldern zum Projekt {#panels}

[Bedienfelder](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=de) sind die Grundlage für jedes Projekt in Analysis Workspace. Bedienfelder dienen zum Organisieren der Inhalte (Visualisierungen und Komponenten) eines Projekts.

Viele der in Analysis Workspace bereitgestellten Bedienfelder generieren einen vollständigen Satz von Analysen auf der Grundlage einiger Benutzereingaben.

So fügen Sie ein Bedienfeld hinzu:

1. Wählen Sie das Symbol [!UICONTROL **Bedienfelder**] in der linken Leiste.

   ![](assets/build-panels.png)

1. Suchen Sie nach dem Bedienfeld, das Sie hinzufügen möchten. Wenn es in der linken Leiste angezeigt wird, ziehen Sie es in Ihr Projekt.

1. Fügen Sie Ihrem Bedienfeld Visualisierungen hinzu, wie unter [Hinzufügen von Visualisierungen zum Projekt](#add-visualizations-to-the-project) beschrieben.

   Alternativ können Sie Komponenten direkt zu einem Bedienfeld hinzufügen, wie unter [Hinzufügen von Komponenten zum Projekt](#add-components-to-the-project) beschrieben.

## Hinzufügen von Visualisierungen zum Projekt

[Visualisierungen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html?lang=de) (wie z. B. eine Freiformtabelle, ein Balken- oder ein Liniendiagramm) können verwendet werden, um Daten visuell zum Leben zu erwecken.

>[!TIP]
>
>Freiformtabellen sind der am häufigsten verwendete Visualisierungstyp und bilden die Grundlage für die interaktive Datenanalyse. Weitere Informationen zum Arbeiten mit Freiformtabellen in Analysis Workspace finden Sie unter [Freiformtabelle](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md).

So fügen Sie eine Visualisierung hinzu.

1. Wählen Sie das Symbol **[!UICONTROL Visualisierungen]** in der linken Leiste.

   ![](assets/build-visualizations.png)

1. Suchen Sie nach der Visualisierung, die Sie hinzufügen möchten. Wenn sie in der linken Leiste angezeigt wird, ziehen Sie sie in ein Bedienfeld innerhalb Ihres Projekts.

1. Fügen Sie der Visualisierung Komponenten hinzu, wie unter [Hinzufügen von Komponenten zum Projekt](#add-components-to-the-project) beschrieben.

## Hinzufügen von Komponenten zum Projekt

[Komponenten](/help/analyze/analysis-workspace/components/analysis-workspace-components.md) bilden die eigentlichen Daten eines jeden Projekts. Sie können Komponenten zu Visualisierungen oder Bedienfeldern hinzufügen.

>[!TIP]
>
>Informationen zu den einzelnen Komponenten erhalten Sie, wenn Sie in der linken Leiste das Infosymbol neben dem Namen einer Komponente auswählen, oder in der [Komponentenübersicht](/help/components/home.md).

Im Folgenden finden Sie grundlegende Informationen zum Hinzufügen einer Komponente zu einem Projekt in Analysis Workspace. Detaillierte Informationen zum Hinzufügen der verschiedenen Komponententypen (Dimensionen, Metriken, Segmente und Datumsbereiche) finden Sie unter [Verwenden von Komponenten in Analysis Workspace](/help/analyze/analysis-workspace/components/use-components-in-workspace.md).

So fügen Sie einem Projekt in Analysis Workspace eine Komponente hinzu:

1. Wählen Sie in der linken Leiste das Symbol **[!UICONTROL Komponenten]** aus.

   ![](assets/build-components.png)

1. Scrollen Sie zu der Komponente, die Sie hinzufügen möchten, oder suchen Sie sie und ziehen Sie sie anschließend in ein Bedienfeld oder eine Visualisierung innerhalb Ihres Projekts.

   Sie können beispielsweise ein Segment in den Segment-Ablegebereich in der Kopfzeile eines Bedienfelds ziehen.

   ![Segment im Ablegebereich ablegen](assets/segment-dropzone.png)

   Weitere Informationen zum Hinzufügen von Komponenten zu Projekten finden Sie unter [Verwenden von Komponenten in Analysis Workspace](/help/analyze/analysis-workspace/components/use-components-in-workspace.md).

1. (Optional) Geben Sie das Projekt wie unter [Speichern und Freigeben des Projekts](#save-and-share-the-project) beschrieben frei.

## Speichern und Freigeben des Projekts

Bei der Erstellung einer Analyse in Analysis Workspace wird Ihre Arbeit [automatisch gespeichert](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md).

Wenn Sie das Projekt fertiggestellt haben und es praktische Einblicke liefert, kann das Projekt auch von anderen genutzt werden. Sie können das Projekt für Benutzende sowie Gruppen in Ihrer Organisation oder auch für Personen außerhalb Ihrer Organisation freigeben. Informationen zum Freigeben eines Projekts finden Sie unter [Freigeben von Projekten](/help/analyze/analysis-workspace/curate-share/share-projects.md).
