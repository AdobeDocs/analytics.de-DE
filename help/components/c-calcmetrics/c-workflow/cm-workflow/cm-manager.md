---
description: Die Seite „Berechnete Metriken“ bietet viele Möglichkeiten zum Kuratieren von Metriken, z. B. Freigeben, Filtern, Taggen, Genehmigen, Kopieren, Löschen und Kennzeichnen als Favoriten.
title: Manager für berechnete Metriken
feature: Calculated Metrics
exl-id: 32430e77-2450-4672-9c21-255e76802a4c
source-git-commit: 8e8f59f747ddacc5462cbc177d199a5e0e91908a
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 9%

---

# Manager für berechnete Metriken

Die Seite „Berechnete Metriken“ bietet viele Möglichkeiten zum Kuratieren von Metriken, z. B. Freigeben, Filtern, Taggen, Genehmigen, Kopieren, Löschen und Kennzeichnen als Favoriten.

Auf der Seite „Berechnete Metriken“ werden alle Segmente angezeigt, deren Inhaber Sie sind und die für Sie freigegeben wurden. Benutzer auf Admin-Ebene können alle benutzerdefinierten Metriken in der Organisation sehen.

<!-- add screenshot -->

## Zugriff auf den Manager für berechnete Metriken

1. Wählen Sie in Adobe Analytics [!UICONTROL **Komponenten**] > [!UICONTROL **Berechnete Metriken**].

## Verfügbare Aktionen im Manager für berechnete Metriken

Im Manager für berechnete Metriken haben Sie folgende Möglichkeiten:

* [Berechnete Metriken filtern](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-filter.md)

* [Berechnete Metriken als Favoriten markieren](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-favorite.md)

* [Berechnete Metriken genehmigen](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-approving.md)

* [Berechnete Metriken taggen](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-tagging.md)

* [Berechnete Metriken freigeben](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-sharing.md)

* Exportieren Sie eine berechnete Metrik in eine CSV-Datei.

* [Kopieren von berechneten Metriken](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-copy.md)

* Berechnete Metriken löschen

## Spalten konfigurieren

Sie können die für jede berechnete Metrik im Manager für berechnete Metriken angezeigten Informationen konfigurieren, indem Sie die angezeigten Spalten konfigurieren.

So konfigurieren Sie die sichtbaren Spalten im Manager für berechnete Metriken:

1. Wählen Sie in Adobe Analytics die Registerkarte **[!UICONTROL Komponenten]** und dann **[!UICONTROL Berechnete Metriken]** aus.

1. Klicken Sie im Manager für berechnete Metriken auf das Symbol **Spalten anpassen** (![Symbol Spalten anpassen](assets/customize-columns-icon.png) und wählen Sie dann die Spalten aus, die Sie im Manager für berechnete Metriken anzeigen möchten.

   Die folgenden Spalten sind verfügbar:

   | Spaltentitel | Beschreibung |
   |---|---|
   | Favoriten | Zeigt Sternsymbol neben jeder berechneten Metrik an, sodass Sie berechnete Metriken als Favoriten markieren können. Weitere Informationen finden Sie unter [Berechnete Metriken als Favoriten markieren](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-favorite.md). |
   | Titel und Beschreibung | Diese Werte werden im Generator für berechnete Metriken bereitgestellt. Um den Titel und die Beschreibung zu bearbeiten, klicken Sie auf den Titel-Link, um den Generator für berechnete Metriken zu öffnen. |
   | Report Suite | Gibt an, in welcher Report Suite die Metrik zuletzt gespeichert wurde. |
   | Inhaber | Gibt den Inhaber der benutzerdefinierten Metrik an. Wenn Sie kein Administrator sind, können Sie nur die Metriken sehen, deren Inhaber Sie sind, oder die für Sie freigegeben wurden. |
   | Tags | Zeigt Tags an, die auf die Metrik angewendet wurden, entweder von Ihnen oder von Personen, die die berechnete Metrik für Sie freigegeben haben. |
   | Freigegeben für | Listet Einzelpersonen oder Gruppen (nur Admin) oder Alle (nur Admin) auf, für die Sie die berechnete Metrik freigegeben haben. <p>Bei der Freigabe einer berechneten Metrik wird neben dem Namen der berechneten Metrik ein Freigabesymbol angezeigt.</p> |
   | Änderungsdatum | Gibt das Datum an, an dem die benutzerdefinierte Metrik zuletzt geändert wurde. |
   | Verwendet in | Zeigt an, wo berechnete Metriken derzeit verwendet werden und wie oft sie in den einzelnen Bereichen verwendet werden. <p>Wenn die berechnete Metrik beispielsweise in 40 Projekten und 2 Warnhinweisen verwendet wird, wird der Wert dieser Spalte als [!UICONTROL **42 Komponenten**] angezeigt. <p>Wählen Sie den Wert in dieser Spalte aus, um die Aufschlüsselung anzuzeigen, wo die berechneten Metriken verwendet werden (z. B. [!UICONTROL **Projekte (40)**], [!UICONTROL **Warnhinweise (2)**]). Darüber hinaus können Sie die Liste der Elemente anzeigen, in denen die berechneten Metriken verwendet werden. Um beispielsweise die Liste der Projekte anzuzeigen, in denen sie verwendet werden, klicken Sie auf den Link [!UICONTROL **Projekte (40)**].</p><p>Jeder der folgenden Bereiche zeigt die Anzahl der Instanzen berechneter Metriken an, die in diesem Bereich verwendet werden:</p> <ul><li>[!UICONTROL **Projekte**]<p>Enthält berechnete Metriken, [ im Generator für berechnete Metriken erstellt wurden ](/help/analyze/analysis-workspace/components/apply-create-metrics.md#create-calculated-metrics-for-all-projects) für alle Projekte verfügbar sind.</p></li><li>[!UICONTROL **Ad-hoc-Komponenten**]<p>Enthält berechnete Metriken, [ als schnelle berechnete Metriken erstellt wurden ](/help/analyze/analysis-workspace/components/apply-create-metrics.md#create-calculated-metrics-for-a-single-project) nur in einem einzigen Projekt verfügbar sind.</p></li><li>[!UICONTROL **Geplante Projekte**]</li><li>[!UICONTROL **Mobile Scorecards**]</li><li>[!UICONTROL **Anmerkungen**]</li><li>[!UICONTROL **Warnhinweise**]</li><li>[!UICONTROL **Report Builder**]<p>Wenn Sie diese Option wählen, wird eine CSV-Datei mit den folgenden Datenspalten heruntergeladen:</p><ul><li>Name des Report Builders</li><li>Zuletzt aufgerufen</li><li>Zuletzt aufgerufene IMS-Benutzer-ID</li><li>Zuletzt aufgerufener Benutzername</li></ul><p>Beim Anzeigen von Informationen zum Report Builder sind ab September 2024 Nutzungsinformationen verfügbar.</p></li></ul><p>Diese Informationen können Ihnen dabei helfen festzustellen, ob eine Komponente für Benutzende in Ihrer Organisation nützlich ist, wo sie verwendet wird und ob sie gelöscht oder geändert werden muss.</p><p>Beachten Sie Folgendes beim Anzeigen dieser Option:</p><ul><li>Diese Informationen stehen nur Systemadministratoren zur Verfügung.</li><li>Die Spalte [!UICONTROL **Verwendet in**] wird standardmäßig nicht angezeigt. [Spalten konfigurieren](#configure-columns) um sie anzuzeigen.</li><li>Wenn eine berechnete Metrik eine andere berechnete Metrik in ihrer Definition enthält, wird die Verwendung dieser berechneten Metrik nicht in der Spalte [!UICONTROL **Verwendet in**] angezeigt. Wenn eine berechnete Metrik in die Definition eines anderen Komponententyps (z. B. eines Segments) aufgenommen wird, wird die Verwendung in der Spalte [!UICONTROL **Verwendet in**] angezeigt.</li><li>Diese Informationen beinhalten keine Verwendung über die API oder die Data Warehouse.</li><li>Wenn in dieser Spalte keine Daten für eine bestimmte Komponente vorhanden sind, sie jedoch ein Datum [!UICONTROL **Zuletzt verwendet**] aufweist, wurde die Komponente möglicherweise in einer Analyse verwendet, ohne gespeichert zu werden.</li><li>Nutzungsinformationen sind ab September 2023 verfügbar.</li></ul><p>Sie können das [Datenwörterbuch](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) zusammen mit diesen Informationen verwenden, um zu verfolgen und besser zu verstehen, wie Komponenten in Ihrer Organisation verwendet werden.</p> |
   | Zuletzt verwendet | Zeigt das Datum, an dem die berechnete Metrik zuletzt in einem der folgenden Bereiche verwendet wurde: <ul><li>Warnhinweise</li><li>Berechnete Metriken </li><li>Projekte</li><li>Geplante Projekte</li></ul> <p>Diese Informationen können Ihnen dabei helfen festzustellen, ob eine Komponente für Benutzende in Ihrer Organisation nützlich ist, wo sie verwendet wird und ob sie gelöscht oder geändert werden muss.</p><p>Beachten Sie Folgendes beim Anzeigen dieser Option:</p><ul><li>Diese Informationen umfassen nicht die Verwendung der API, des Report Builders oder der Data Warehouse.</li><li>Bei einigen Komponenten enthält diese Spalte möglicherweise keine Daten, wenn die Komponente zuletzt vor September 2023 verwendet wurde.</li><li>Diese Informationen stehen nur Systemadministratoren zur Verfügung.</li></ul><p>Sie können das [Datenwörterbuch](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) zusammen mit diesen Informationen verwenden, um zu verfolgen und besser zu verstehen, wie Komponenten in Ihrer Organisation verwendet werden. |

   {style="table-layout:auto"}
