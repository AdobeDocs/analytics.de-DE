---
description: Der Segment-Manager bietet verschiedene Möglichkeiten zum Kuratieren von Segmenten wie das Freigeben, Filtern, Taggen, Genehmigen, Kopieren, Löschen und Kennzeichnen als Favoriten.
title: Segmente verwalten (Segment-Manager)
feature: Segmentation
exl-id: be182a55-23cb-415f-a7d0-3c1efeead1a1
source-git-commit: 8e8f59f747ddacc5462cbc177d199a5e0e91908a
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 27%

---

# Segment-Manager

Der Segment-Manager bietet verschiedene Möglichkeiten zum Kuratieren von Segmenten wie das Freigeben, Filtern, Taggen, Genehmigen, Kopieren, Löschen und Kennzeichnen als Favoriten.

Der Segment-Manager in Analytics zeigt Ihnen alle Segmente, die sich in Ihrem Besitz befinden und für Sie freigegeben wurden. Benutzer auf Administratorebene sehen alle Segmente der Organisation. In dieser Übersicht werden die Benutzeroberfläche und die Funktionen des Segment-Managers vorgestellt.

![Segment-Manager](assets/segments-manager.png)

## Zugriff auf den Segment-Manager

1. Wählen Sie in Adobe Analytics die Registerkarte **[!UICONTROL Komponenten]** und dann **[!UICONTROL Segmente]** aus.

   Oder

   Wählen Sie in einem vorhandenen Bericht im linken Navigationsbereich das Symbol Segmente ![](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Segmentation_18_N.svg) und dann **[!UICONTROL Verwalten]** aus.

## Verfügbare Aktionen im Segment-Manager

Im Segment-Manager haben Sie folgende Möglichkeiten:

* [Filtern von Segmenten](/help/components/segmentation/segmentation-workflow/t-seg-filter.md)

* [Segmente als Favoriten markieren](/help/components/segmentation/segmentation-workflow/t-seg-favorite.md)

* [Segmente genehmigen](/help/components/segmentation/segmentation-workflow/seg-approve.md)

* [Segmente taggen](/help/components/segmentation/segmentation-workflow/seg-tag.md)

* [Segmente freigeben](/help/components/segmentation/segmentation-workflow/t-seg-share.md)

* Exportieren Sie ein Segment in eine CSV-Datei.

* [Segmente kopieren](/help/components/segmentation/segmentation-workflow/seg-copy.md)

* [Segmente löschen](/help/components/segmentation/segmentation-workflow/seg-delete.md)

## Spalten konfigurieren

Sie können die in Segment Manager für jedes Segment angezeigten Informationen konfigurieren, indem Sie die angezeigten Spalten konfigurieren.

So konfigurieren Sie die sichtbaren Spalten im Segment-Manager:

1. Wählen Sie in Adobe Analytics die Registerkarte **[!UICONTROL Komponenten]** und dann **[!UICONTROL Segmente]** aus.

1. Klicken Sie im Segment-Manager auf das Symbol **Spalten anpassen** (Symbol ![ Spalten anpassen](assets/customize-columns-icon.png) und wählen Sie dann die Spalten aus, die Sie im Segment-Manager anzeigen möchten.

   Die folgenden Spalten sind verfügbar:

   | Spaltentitel | Beschreibung |
   |---|---|
   | Titel und Beschreibung | Diese Werte werden im Segment Builder bereitgestellt. Um den Titel und die Beschreibung zu bearbeiten, klicken Sie auf den Titel-Link, um Segment Builder zu öffnen. |
   | Favoriten | Zeigt Sternsymbole neben jedem Segment an, sodass Sie Segmente als Favoriten markieren können. Weitere Informationen finden Sie unter [Segmente als Favoriten markieren](/help/components/segmentation/segmentation-workflow/t-seg-favorite.md). |
   | Report Suites | Diese Spalte zeigt an, in welcher Report Suite das Segment zuletzt gespeichert wurde. |
   | Inhaber | Zeigt an, wer Inhaber des Segments ist. Wenn Sie kein Administrator sind, können Sie nur Segmente sehen, deren Inhaber Sie sind, sowie Segmente, die für Sie freigegeben wurden. |
   | Tags (in der Spaltenauswahl nicht aktiviert, weshalb die Spalte nicht angezeigt wird) | Tags, die entweder durch Sie oder durch Personen, die ein Segment für Sie freigegeben haben, auf das Segment angewendet wurden. |
   | Freigegeben für | Zeigt Personen oder Gruppen (nur Administrator) oder „Alle“ (nur Administrator) an, für die Sie das Segment freigegeben haben. <p>Wenn ein Segment von Ihnen oder für Sie freigegeben wird, wird neben dem Segmentnamen ein Freigabesymbol angezeigt.</p> |
   | Änderungsdatum | Zeigt das Datum der letzten Änderung des Segments an. |
   | Verwendet in | Zeigt an, wo Segmente derzeit verwendet werden und wie oft sie in den einzelnen Bereichen verwendet werden. <p>Wenn das Segment beispielsweise in 40 Projekten und 2 Warnhinweisen verwendet wird, wird der Wert dieser Spalte als [!UICONTROL **42 Komponenten**] angezeigt.</p> <p>Wählen Sie den Wert in dieser Spalte aus, um die Aufschlüsselung anzuzeigen, wo die Segmente verwendet werden (z. B. [!UICONTROL **Projekte (40)**], [!UICONTROL **Warnhinweise (2)**]). Darüber hinaus können Sie die Liste der Elemente anzeigen, in denen die Segmente verwendet werden. Um beispielsweise die Liste der Projekte anzuzeigen, in denen sie verwendet werden, klicken Sie auf den Link [!UICONTROL **Projekte (40)**].</p><p>Jeder der folgenden Bereiche zeigt die Anzahl der Instanzen der Segmente an, die in diesem Bereich verwendet werden:</p>  <ul><li>[!UICONTROL **Projekte**]<p>Enthält Segmente, [ im Segment Builder erstellt wurden ](/help/components/segmentation/segmentation-workflow/seg-build.md) für alle Projekte verfügbar sind.</p></li><li>[!UICONTROL **Ad-hoc-Komponenten**]<p>Enthält Segmente, [ als Schnellsegmente erstellt wurden ](/help/analyze/analysis-workspace/components/segments/quick-segments.md) nur in einem einzigen Projekt verfügbar sind.</p></li><li>[!UICONTROL **Geplante Projekte**]</li><li>[!UICONTROL **Mobile Scorecards**]</li><li>[!UICONTROL **Anmerkungen**]</li><li>[!UICONTROL **Warnhinweise**]</li><li>[!UICONTROL **Berechnete Metriken**]</li><li>[!UICONTROL **Report Builder**]<p>Wenn Sie diese Option wählen, wird eine CSV-Datei mit den folgenden Datenspalten heruntergeladen:</p><ul><li>Name des Report Builders</li><li>Zuletzt aufgerufen</li><li>Zuletzt aufgerufene IMS-Benutzer-ID</li><li>Zuletzt aufgerufener Benutzername</li></ul><p>Beim Anzeigen von Informationen zum Report Builder sind ab September 2024 Nutzungsinformationen verfügbar.</p></li></ul><p>Diese Informationen können Ihnen dabei helfen festzustellen, ob eine Komponente für Benutzende in Ihrer Organisation nützlich ist, wo sie verwendet wird und ob sie gelöscht oder geändert werden muss.</p><p>Beachten Sie Folgendes beim Anzeigen dieser Option:</p><ul><li>Diese Informationen stehen nur Systemadministratoren zur Verfügung.</li><li>Die Spalte [!UICONTROL **Verwendet in**] wird standardmäßig nicht angezeigt. [Spalten konfigurieren](#configure-columns) um sie anzuzeigen.</li><li>Wenn ein Segment ein anderes Segment in seiner Definition enthält, wird eine Verwendung dieses Segments nicht in der Spalte [!UICONTROL **Verwendet in**] angezeigt. Wenn ein Segment in der Definition eines anderen Komponententyps enthalten ist (z. B. eine berechnete Metrik), wird die Verwendung in der Spalte [!UICONTROL **Verwendet in**] angezeigt.</li><li>Diese Informationen beinhalten keine Verwendung über die API oder die Data Warehouse.</li><li>Wenn in dieser Spalte keine Daten für eine bestimmte Komponente vorhanden sind, sie jedoch ein Datum [!UICONTROL **Zuletzt verwendet**] aufweist, wurde die Komponente möglicherweise in einer Analyse verwendet, ohne gespeichert zu werden.</li><li>Nutzungsinformationen sind ab September 2023 verfügbar.</li></ul><p>Sie können das [Datenwörterbuch](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) zusammen mit diesen Informationen verwenden, um zu verfolgen und besser zu verstehen, wie Komponenten in Ihrer Organisation verwendet werden.</p> |
   | Zuletzt verwendet | Zeigt das Datum an, an dem das Segment zuletzt in einem der folgenden Komponententypen verwendet wurde: <ul><li>Warnhinweise</li><li>Berechnete Metriken </li><li>Projekte</li><li>Geplante Projekte</li><li>Segmente </li></ul> <p>Diese Informationen können Ihnen dabei helfen festzustellen, ob eine Komponente für Benutzende in Ihrer Organisation nützlich ist, wo sie verwendet wird und ob sie gelöscht oder geändert werden muss.</p><p>Beachten Sie Folgendes beim Anzeigen dieser Option:</p><ul><li>Diese Informationen umfassen nicht die Verwendung der API, des Report Builders oder der Data Warehouse.</li><li>Bei einigen Komponenten enthält diese Spalte möglicherweise keine Daten, wenn die Komponente zuletzt vor September 2023 verwendet wurde.</li><li>Diese Informationen stehen nur Systemadministratoren zur Verfügung.</li></ul><p>Sie können das [Datenwörterbuch](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) zusammen mit diesen Informationen verwenden, um zu verfolgen und besser zu verstehen, wie Komponenten in Ihrer Organisation verwendet werden. |

   {style="table-layout:auto"}

## Anleitungsvideo {#section_B3C5DA22DC5248DBA17C56E03DA2D4F2}

In diesem [Adobe Analytics-Video](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/components/segmentation/segment-management-and-sharing.html?lang=de) erhalten Sie einen kurzen Überblick darüber, wie Sie Segment Manager einsetzen können.


