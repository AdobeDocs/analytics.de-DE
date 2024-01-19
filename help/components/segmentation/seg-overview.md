---
description: Mit Segmenten können Besucheruntergruppen anhand von Merkmalen oder Website-Interaktionen identifiziert werden. Segmente sind als kodifizierte Zielgruppeneinblicke ausgelegt, die Sie für bestimmte Anforderungen erstellen und dann prüfen, bearbeiten und für andere Team-Mitglieder freigeben oder in anderen Produkten von Adobe und in Analytics verwenden können.
title: Informationen zu Segmenten
feature: Segmentation
exl-id: 11d930ca-5d59-4ea5-b6e5-fe3d57be94fd
source-git-commit: 93099d36a65ca2bf16fbd6342f01bfecdc8c798e
workflow-type: tm+mt
source-wordcount: '1148'
ht-degree: 67%

---

# Informationen zu Segmenten

Mit Segmenten können Besucheruntergruppen anhand von Merkmalen oder Website-Interaktionen identifiziert werden. Segmente sind als Einblicke in Zielgruppen konzipiert, die Sie für Ihre spezifischen Anforderungen erstellen und dann überprüfen, bearbeiten und mit anderen Teammitgliedern teilen oder in anderen Adobe- und Analytics-Funktionen verwenden können.

Segmente basieren auf einer [!UICONTROL Besucher], [!UICONTROL Besuch], und [!UICONTROL Treffer] Hierarchie der Ebene mit einem verschachtelten Behältermodell. Mit verschachtelten Containern können Sie Besucherattribute definieren sowie Aktionen, die auf Regeln zwischen den Containern und innerhalb der Container basieren. Analytics-Segmente können erstellt, genehmigt, freigegeben, gespeichert und über viele Produkte und Funktionen in der [!DNL Adobe Experience Cloud] hinweg ausgeführt werden. Segmente können aus einem Bericht generiert, in einem Dashboard-Bericht erstellt oder für den schnellen Zugriff mit einem Lesezeichen versehen werden.

Sie können Segmente im Segment Builder erstellen und speichern oder aus einem Fallout-Bericht (in  Analysis Workspace) generieren. Sie können auch vorgefertigte Segmente verwenden und erweitern, die auf bestimmten Regeln zwischen verschachtelten Containern basieren. Diese ermöglichen das Filtern von Ergebnissen und können auf Berichte angewendet werden. Darüber hinaus können Segmente zusammen als [gestapelte Segmente](/help/components/segmentation/segmentation-workflow/seg-workflow.md).

Identifizierung von Segmenten

- wer Ihre Besucher sind (Land, Geschlecht, Café),
- welche Geräte und Dienste sie verwenden (Browser, Suchmaschine, Mobilgerät),
- von dem aus sie navigiert sind (Suchmaschine, vorherige Ausstiegsseite, natürliche Suche),
- und vieles mehr.

<!--![](assets/seg.png)-->

Segmente können auf folgenden Werten basieren:

- Auf Attributen basierende Besucher: Browsertyp, Gerät, Anzahl Besuche, Land, Geschlecht.
- Auf Interaktionen basierende Besucher: Kampagnen, Keyword, Suchmaschine.
- Auf Exits und Entries basierende Besucher: Besucher von Facebook, einer bestimmten Landingpage, Referrerdomäne.
- Auf benutzerdefinierten Variablen basierende Benutzer: Formularfeld, definierte Kategorien, Kunden-ID.

Beim Erstellen von Zielgruppensegmenten in Segment Builder definieren Sie Bedingungen, für die Sie zwischen den Containern die Operatoren [!UICONTROL AND] und [!UICONTROL OR] verwenden.

<table style="table-layout:fixed; border: none;">

<tr>

<td style="background-color: #E5E4E2;" colspan="3" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_User_18_N.svg"/> Besucher</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Besuche</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;"></td><td colspan="2">AND</td></td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Besuche</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>
</table>

<table style="table-layout:fixed; border: none;">

<tr>

<td style="background-color: #E5E4E2;" colspan="3" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_User_18_N.svg"/> Besucher</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Besuche</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;"></td><td colspan="2">OR</td></td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Besuche</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>
</table>

<!--![](assets/standard_segment_containers.png)-->

Dieser Segmenttyp filtert Datensätze auf der Grundlage von Merkmalen, die mit den Operatoren [!UICONTROL AND] und [!UICONTROL OR] verbunden werden.

- Sie können [mehrere Segmente auf einen Bericht oder ein Projekt anwenden](/help/components/segmentation/segmentation-workflow/seg-workflow.md).
- Alle Segmente gelten nun für alle Report Suites.
- Der [Segment Builder](/help/components/segmentation/segmentation-workflow/seg-workflow.md) vereinfacht das Erstellen von Segmenten.
- Der neue [Segment-Manager](/help/components/segmentation/segmentation-workflow/seg-workflow.md) ermöglicht die Einrichtung von [Workflows](/help/components/segmentation/segmentation-workflow/seg-workflow.md) und bietet Funktionen zum Teilen, Taggen, Prüfen und Genehmigen.
- Sie können Segmente zum Organisieren und Suchen [taggen](/help/components/segmentation/segmentation-workflow/seg-workflow.md), anstatt Ordner zu verwenden.
- Sie können [sequenzielle Segmente](/help/components/segmentation/segmentation-workflow/seg-sequential-build.md) erstellen.
- Die [!UICONTROL Seitenansicht] Der Container ist jetzt [!UICONTROL Treffer] -Container, um anzugeben, dass dieser Container alle Datentypen segmentiert und nicht nur Seitenansichten. So werden z. B. Linktracking-Aufrufe und trackAction-Aufrufe aus den Mobile SDKs durch den Treffercontainer vollständig ein- oder ausgeschlossen.

## Segmentierung in Analysis Workspace

Analysis Workspace umfasst die folgenden zusätzlichen Funktionen:

- Sie können [Segmente vergleichen](../../analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md).
- Verwenden Sie [Segmente als Dimensionen](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=de) bei Vergleichen.
- Verwenden Sie Segmente in der [Fallout-Analyse](../../analyze/analysis-workspace/visualizations/fallout/compare-segments-fallout.md).

## Adobe-bereitgestellte Segmente

Die Leiste &quot;Komponente&quot;auf der linken Bildschirmseite zeigt Segmente an, die von Ihnen und Ihrem Unternehmen erstellt wurden, sowie Adobe-Segmente, die standardmäßig bereitgestellt werden. Wenn Sie auf **[!UICONTROL Alle anzeigen]**, werden diese Segmente in der Regel unten in der Liste angezeigt und durch das Adobe-Logo rechts gekennzeichnet.

## Sequenzielle Segmente {#sequential}

Mit sequenziellen Segmenten können Sie Besucher anhand der Navigation und den Seitenansichten innerhalb Ihrer Site identifizieren, indem Sie ein Segment mit definierten Aktionen und Interaktionen bereitstellen. Mit sequenziellen Segmenten können Sie erkennen, was ein Besucher mag und was er meidet. Beim Erstellen sequenzieller Segmente wird der Operator [!UICONTROL THEN] eingesetzt, um die Navigation des Besuchers zu definieren und zu ordnen.

<!--![](assets/sequential_seg.png)-->

| Erster Besuch | Zweiter Besuch | Dritter Besuch |
|---|---|---|
| Beim ersten Besuch besuchte der Besucher die Haupt-Landingpage A, schloss die Kampagnenseite B aus und sah sich dann die Produktseite C an. | Beim zweiten Besuch besuchte der Besucher erneut die Haupt-Landingpage A, schloss die Kampagnenseite B aus, besuchte erneut die Produktseite C und dann eine neue Seite D. | Beim dritten Besuch hat der Besucher denselben Pfad wie beim ersten und zweiten Besuch eingegeben und gefolgt und dann Seite F ausgeschlossen, um direkt zu einer Targeting-Produktseite G zu wechseln. |

Sequenzielle Segmente können auf folgenden Trefferwerten basieren:

- Auf der Sequenz von Seitentreffern basierende Besucher: Seitenansichten innerhalb eines einzelnen Besuchs, Seitenansichten über verschiedene Besuche hinweg, Besuche, bei denen Seitenansichten ausgeschlossen wurden.
- Auf der Zeit zwischen und nach Seitenansichten basierende Besucher: nach einem Zeitlimit, zwischen Treffern, nach einem Ereignis.

<table style="table-layout:fixed; border: none;">

<tr>

<td style="background-color: #E5E4E2;" colspan="3" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_User_18_N.svg"/> Besucher</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Besuche</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;"></td><td colspan="2">DANN</td></td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Besuche</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>
</table>

<table style="table-layout:fixed; border: none;">

<tr>

<td style="background-color: #E5E4E2;" colspan="3" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_User_18_N.svg"/> Besucher</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Besuche</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;"></td><td style="background-color: #D3D3D3;"></td><td>AND</td></td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;"></td><td colspan="2">DANN</td></td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Besuche</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>

<tr>
<td style="background-color: #E5E4E2;"></td><td style="background-color: #D3D3D3;"></td><td>OR</td></td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>
</tr>
</table>

<!--![](assets/sequential_segmentation_containers_view.png)-->

Ein sequenzielles Segment filtert Datensätze basierend auf Benutzeraktionen. Dazu wird der [!UICONTROL THEN]-Operator verwendet.

## Video zur Segmentierung {#segment-video}

In diesem Video erhalten Sie einen kurzen Überblick darüber, was Segmentcontainer sind und wie sie verwendet werden:

>[!VIDEO](https://video.tv.adobe.com/v/25401/?quality=12&learn=on)


## Zugriff auf die Segmentierungswerkzeuge {#access}

+++ **Wie komme ich zum Segment Builder?**

Sie können wie folgt auf den Segment Builder zugreifen:

- Öffnen Sie einen vorhandenen Bericht und klicken Sie auf das ![Segmentsymbol](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Segmentation_18_N.svg) im linken Navigationsmenü. Klicken Sie in der angezeigten Segmentleiste auf **[!UICONTROL Hinzufügen]** oder

- Klicken Sie oben im Segment-Manager auf **[!UICONTROL + Hinzufügen]**.  ![Schaltfläche hinzufügen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_AddCircle_18_N.svg)

  oder

- klicken Sie im Segment-Manager auf einen Segmenttitel, um das Segment im Segment Builder zu bearbeiten.

+++

+++ **Wie komme ich zum Segment-Manager?**

Sie können wie folgt auf den Segment-Manager zugreifen:

- Wechseln Sie in der oberen Navigation zu **[!UICONTROL Analysen]** > **[!UICONTROL Komponenten]**. Klicken Sie anschließend auf **[!UICONTROL Segmente]** oder

- Öffnen Sie einen vorhandenen Bericht und klicken Sie auf das ![Segmentsymbol](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Segmentation_18_N.svg) im linken Navigationsmenü. Klicken Sie anschließend auf **[!UICONTROL Verwalten]** oder

- drücken Sie an einer beliebigen Stelle die Schrägstrich-Taste (/) und suchen Sie nach Segment Manager.

+++

## Zugriffsberechtigung {#section_648DFA3A882146C485A84ED014EEC707}

+++ **Welche Rechte und Privilegien benötige ich, um Segmente zu verwenden, zu erstellen und zu verwalten?**

Standardmäßig können alle Benutzer persönliche Segmente erstellen und bearbeiten. Administratoren können jedoch entscheiden, wer [Berechtigungen zur Erstellung von Segmenten](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/home.html?lang=de) erhält, und sie bestimmten Gruppen zuweisen. Diese Segmente können direkt für andere Analytics-Benutzer freigegeben werden.

Administratoren können alle Segmente bearbeiten und Segmente für Gruppen und alle Personen der Organisation freigeben. [Mehr …](/help/components/segmentation/seg-reference/seg-rights.md)

+++

+++ **Kann ich alle in meinem Unternehmen vorhandenen Segmente sehen?**

Ja, Administratoren können alle Segmente innerhalb der [!DNL Analysis Workspace] -Benutzeroberfläche.

Report Builder zeigt Segmente an, deren Inhaber Sie sind, sowie Segmente, die für Sie freigegeben wurden.

+++

+++ **Kann ich alle Analytics-Segmente im Segment-Manager verwalten?**

Ja, alle Segmente können in Segment Manager verwaltet werden. Der Segment-Manager zeigt Segmente an, die für den Inhaber (den Benutzer, der das Segment erstellt hat), Benutzer, für die diese freigegeben sind, und Administratorbenutzer sichtbar sind. Die Segmentauswahl zeigt Segmente an, deren Inhaber der Benutzer ist, und solche, die für ihn freigegeben wurden.

Administratoren können alle Segmente in der Benutzeroberfläche von Analysis Workspace anzeigen.

Report Builder zeigt nur von Ihnen erstellte Segmente oder Segmente, die für Sie freigegeben wurden, an.

+++

+++ **Warum kann ich dieses Segment nicht löschen?**

In der [Experience Cloud](/help/components/segmentation/segmentation-workflow/seg-workflow.md) veröffentlichte Segmente können nicht gelöscht oder bearbeitet werden. Sie können das Segment jedoch kopieren und die Kopie bearbeiten.

+++
