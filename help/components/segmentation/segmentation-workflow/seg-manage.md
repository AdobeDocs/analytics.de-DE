---
description: Der Segment-Manager bietet verschiedene Möglichkeiten zum Kuratieren von Segmenten wie das Freigeben, Filtern, Taggen, Genehmigen, Kopieren, Löschen und Kennzeichnen als Favoriten.
title: Segmente verwalten (Segment-Manager)
feature: Segmentation
exl-id: be182a55-23cb-415f-a7d0-3c1efeead1a1
source-git-commit: 704f5a30e6399fe59429856246aff364ae3f842d
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 28%

---

# Segment-Manager

Der Segment-Manager bietet verschiedene Möglichkeiten zum Kuratieren von Segmenten wie das Freigeben, Filtern, Taggen, Genehmigen, Kopieren, Löschen und Kennzeichnen als Favoriten.

Der Segment-Manager in Analytics zeigt Ihnen alle Segmente, die sich in Ihrem Besitz befinden und für Sie freigegeben wurden. Benutzer auf Administratorebene sehen alle Segmente der Organisation. Diese Übersicht zeigt die Benutzeroberfläche und die Funktionen des Segment-Managers.

![Segment-Manager](assets/segments-manager.png)

## Zugriff auf den Segment-Manager

1. Wählen Sie in Adobe Analytics die Registerkarte **[!UICONTROL Komponenten]** und dann **[!UICONTROL Segmente]** aus.

   Oder

   Wählen Sie in einem vorhandenen Bericht das Segmentsymbol ![](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Segmentation_18_N.svg) im linken Navigationsbereich und dann **[!UICONTROL Verwalten]** aus.

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

Sie können die für jedes Segment im Segment-Manager angezeigten Informationen konfigurieren, indem Sie die angezeigten Spalten konfigurieren.

So konfigurieren Sie die sichtbaren Spalten im Segment-Manager:

1. Wählen Sie in Adobe Analytics die Registerkarte **[!UICONTROL Komponenten]** und dann **[!UICONTROL Segmente]** aus.

1. Wählen Sie im Segment-Manager das Symbol **Spalten anpassen** ![Spaltensymbol anpassen](assets/customize-columns-icon.png) und wählen Sie dann die Spalten aus, die im Segment-Manager angezeigt werden sollen.

   Die folgenden Spalten sind verfügbar:

   | Spaltentitel | Beschreibung |
   |---|---|
   | Titel und Beschreibung | Diese Werte werden im Segment Builder bereitgestellt. Um den Titel und die Beschreibung zu bearbeiten, wählen Sie den Titel-Link aus, um den Segment Builder zu öffnen. |
   | Favoriten | Zeigt neben jedem Segment Sternensymbole an, mit denen Sie Segmente als Favoriten markieren können. Weitere Informationen finden Sie unter [Segmente als Favoriten markieren](/help/components/segmentation/segmentation-workflow/t-seg-favorite.md). |
   | Report Suites | Diese Spalte zeigt an, in welcher Report Suite das Segment zuletzt gespeichert wurde. |
   | Inhaber | Zeigt an, wer Inhaber des Segments ist. Wenn Sie kein Administrator sind, können Sie nur Segmente sehen, deren Inhaber Sie sind, sowie Segmente, die für Sie freigegeben wurden. |
   | Tags (in der Spaltenauswahl nicht aktiviert, weshalb die Spalte nicht angezeigt wird) | Tags, die entweder durch Sie oder durch Personen, die ein Segment für Sie freigegeben haben, auf das Segment angewendet wurden. |
   | Freigegeben für | Zeigt Personen oder Gruppen (nur Administrator) oder „Alle“ (nur Administrator) an, für die Sie das Segment freigegeben haben. <p>Wenn ein Segment von Ihnen oder für Sie freigegeben wird, wird neben dem Segmentnamen ein Freigabesymbol angezeigt.</p> |
   | Änderungsdatum | Zeigt das Datum der letzten Änderung des Segments an. |
   | Verwendet in | Zeigt an, wo Segmente derzeit verwendet werden und wie oft sie in den einzelnen Bereichen verwendet werden. <p>Wenn das Segment beispielsweise in 40 Projekten und 2 Warnhinweisen verwendet wird, wird der Wert dieser Spalte als [!UICONTROL **42 Komponenten**] angezeigt.</p> <p>Wählen Sie den Wert in dieser Spalte aus, um die Aufschlüsselung der verwendeten Segmente anzuzeigen (z. B. [!UICONTROL **Projekte (40)**], [!UICONTROL **Warnhinweise (2)**]). Darüber hinaus können Sie die Liste der Elemente anzeigen, in denen die Segmente verwendet werden. Sehen Sie sich beispielsweise die Liste der Projekte an, in denen sie verwendet werden, und klicken Sie auf den Link [!UICONTROL **Projekte (40)**] .</p><p>Jeder der folgenden Bereiche zeigt die Anzahl der Instanzen von Segmenten, die in diesem Bereich verwendet werden:</p>  <ul><li>[!UICONTROL **Projekte**]<p>Enthält Segmente, die im Segment Builder ](/help/components/segmentation/segmentation-workflow/seg-build.md) erstellt wurden und für alle Projekte verfügbar sind.[</p></li><li>[!UICONTROL **Ad-hoc-Komponenten**]<p>Enthält Segmente, die [als Schnellsegmente erstellt wurden](/help/analyze/analysis-workspace/components/segments/quick-segments.md) und nur in einem einzelnen Projekt verfügbar sind.</p></li><li>[!UICONTROL **Geplante Projekte**]</li><li>[!UICONTROL **Mobile Scorecards**]</li><li>[!UICONTROL **Anmerkungen**]</li><li>[!UICONTROL **Warnhinweise**]</li><li>[!UICONTROL **Berechnete Metriken**]</li><li>[!UICONTROL **Report Builder**]<p>Bei Auswahl dieser Option wird eine CSV-Datei mit den folgenden Datenspalten heruntergeladen:</p><ul><li>Name des Report Builders</li><li>Zuletzt aufgerufen</li><li>Letzter Zugriff auf IMS-Benutzer-ID</li><li>Letzter Benutzername</li></ul></li></ul><p>Diese Informationen können Ihnen dabei helfen festzustellen, ob eine Komponente für Benutzer in Ihrer Organisation nützlich ist, wo sie verwendet wird und ob sie gelöscht oder geändert werden muss.</p><p>Beachten Sie Folgendes beim Anzeigen dieser Option:</p><ul><li>Diese Informationen sind nur für Systemadministratoren verfügbar.</li><li>Die Spalte [!UICONTROL **Verwendet in**] wird nicht standardmäßig angezeigt. [Konfigurieren Sie Spalten](#configure-columns), um sie anzuzeigen.</li><li>Diese Informationen enthalten keine Verwendung über die API oder Data Warehouse.</li><li>Wenn in dieser Spalte keine Daten für eine bestimmte Komponente vorhanden sind, sie jedoch das Datum [!UICONTROL **Zuletzt verwendet**] hat, wurde die Komponente möglicherweise in einer Analyse verwendet, ohne gespeichert zu werden.</li><li>Nutzungsinformationen sind ab September 2023 verfügbar.</li></ul><p>Sie können das [Datenwörterbuch](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) zusammen mit diesen Informationen verwenden, um die Verwendung von Komponenten in Ihrer Organisation zu verfolgen und besser zu verstehen.</p> |
   | Zuletzt verwendet | Zeigt das Datum der letzten Verwendung des Segments in einem der folgenden Komponententypen an: <ul><li>Warnhinweise</li><li>Berechnete Metriken </li><li>Projekte</li><li>Geplante Projekte</li><li>Segmente </li></ul> <p>Diese Informationen können Ihnen dabei helfen festzustellen, ob eine Komponente für Benutzer in Ihrer Organisation nützlich ist, wo sie verwendet wird und ob sie gelöscht oder geändert werden muss.</p><p>Beachten Sie Folgendes beim Anzeigen dieser Option:</p><ul><li>Diese Informationen enthalten keine Verwendung von API, Report Builder oder Data Warehouse.</li><li>Bei einigen Komponenten enthält diese Spalte möglicherweise keine Daten, wenn die Komponente zuletzt vor September 2023 verwendet wurde.</li><li>Diese Informationen sind nur für Systemadministratoren verfügbar.</li></ul><p>Sie können das [Datenwörterbuch](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) zusammen mit diesen Informationen verwenden, um die Verwendung von Komponenten in Ihrer Organisation zu verfolgen und besser zu verstehen. |

   {style="table-layout:auto"}

## Anleitungsvideo {#section_B3C5DA22DC5248DBA17C56E03DA2D4F2}

In diesem [Adobe Analytics-Video](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/components/segmentation/segment-management-and-sharing.html?lang=de) erhalten Sie einen kurzen Überblick darüber, wie Sie Segment Manager einsetzen können.


