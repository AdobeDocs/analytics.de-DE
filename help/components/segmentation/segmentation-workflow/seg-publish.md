---
description: Erfahren Sie, wie Sie Segmente für Marketing-Aktivitäten in Audience Library, Target und Audience Manager veröffentlichen.
title: Segmente veröffentlichen
feature: Segmentation
exl-id: 0215f896-d3f8-42cc-ac8d-8a94b009927b
TQID: https://experienceleague.adobe.com/JP5OI6SzaJ1xQpFY8iIgT-DNTVxofdSu93XmWI1vtsU
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 157cc2bde1047063014aff39319d5cfaa1de9b5c
workflow-type: tm+mt
source-wordcount: 1432
ht-degree: 29%

---

# Veröffentlichen von Segmenten {#publish-segments}

>[!CONTEXTUALHELP]
>id="components_segments_publishing"
>title="CX Enterprise-Publishing"
>abstract="Sie können die Zielgruppe in der Zielgruppenbibliothek veröffentlichen, wo sie für Marketing-Aktivitäten in Target und anderen CX Enterprise-Lösungen verwendet werden kann."

>[!CONTEXTUALHELP]
>id="components_segments_audiencelibrary"
>title="Zielgruppenbibliothek"
>abstract="In der Zielgruppenbibliothek erstellte Segmente sind sofort verfügbar und nicht von Analytics-Aktualisierungen abhängig."


Sie können ein Adobe Analytics-Segment in CX Enterprise veröffentlichen. Sie können das Segment also für Marketing-Aktivitäten in Audience Manager und in anderen Aktivierungskanälen verwenden, einschließlich Advertising, Target und Campaign.

Sie können Analytics-Segmente in weniger als acht Stunden in CX Enterprise veröffentlichen. Verwenden Sie diese Segmente, um Zielgruppen-Manager in Audience Manager für alle nachfolgenden Ziele zu aktivieren.


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Segmente veröffentlichen](https://experienceleague.adobe.com/de/docs/analytics-learn/tutorials/integrations/experience-cloud/improved-experience-cloud-audience-publishing){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]


>[!NOTE]
>
>Adobe Campaign (Classic und Standard) verhält sich anders, da es zusätzlich zur 8-Stunden-Latenz eine 24-Stunden-Latenz gibt.

## Voraussetzungen

* Stellen Sie sicher, dass die Report Suite, in der Sie dieses Segment speichern, [für CX Enterprise aktiviert) &#x200B;](/help/components/segmentation/segmentation-workflow/seg-publish.md). Andernfalls ist keine Veröffentlichung in CX Enterprise möglich.
* Stellen Sie sicher, dass Ihre Organisation Experience Cloud IDs verwendet.
* Bevor Sie Segmente veröffentlichen können, muss Ihr Administrator einem Produktprofil die Berechtigung für die [!UICONTROL Segmentveröffentlichung] in der [Admin Console](https://experienceleague.adobe.com/de/docs/core-services/interface/administration/admin-tool-experience-cloud) zuweisen und Sie zum Produktprofil hinzufügen.

## Zu beachten

* **Report Suite-Beschränkungen**: Sie können bis zu 75 Segmente pro Report Suite veröffentlichen. Diese Beschränkung wird erzwungen. Wenn Sie bereits 75 Segmente veröffentlicht haben, können Sie keine weiteren Segmente veröffentlichen, bis Sie die Veröffentlichung für genügend Segmente aufheben, um unter den Schwellenwert von 75 Segmenten zu gelangen.
* **Mitgliedschaftsbeschränkungen**: Zielgruppen, die von Adobe Analytics für CX Enterprise freigegeben wurden, dürfen nicht mehr als 20 Millionen eindeutige Mitglieder umfassen.
* **Datenschutz**: Zielgruppen werden nicht nach dem Authentifizierungsstatus der Besucher gefiltert. Ein Besucher kann möglicherweise Ihre Site in nicht authentifizierten und authentifizierten Status durchsuchen. Aktionen, die auftreten, wenn eine Besucherin oder ein Besucher nicht authentifiziert wird, können dennoch dazu führen, dass eine Besucherin oder ein Besucher in eine Zielgruppe aufgenommen wird. Lesen Sie [Adobe CX Enterprise-Datenschutz](https://www.adobe.com/de/privacy/experience-cloud.html) um die vollständigen Auswirkungen der Freigabe von Zielgruppen auf den Datenschutz zu verstehen.
* Eine Erläuterung der **Unterschiede zwischen Segmenten in [!DNL Adobe Analytics] und Audience Manager** finden Sie unter [Grundlegendes zu Segmenten in Analytics und Audience Manager](/help/integrate/c-audience-analytics/aam-analytics-segments.md).

## Timeline für die Segmentveröffentlichung

| Was ist verfügbar? | Wann ist es verfügbar? | Wo ist es verfügbar? |
|---|---|---|
| Metadaten (Segmenttitel und Definition) | Sofort nach der Veröffentlichung | Audience Manager, CX Enterprise-Zielgruppenbibliothek, Target |
| Verwendbares Segment mit Zugehörigkeit | ~ 8 Stunden nach der Veröffentlichung | Besucherprofil-Viewer in Audience Manager |
| Eigenschaften- und Mitgliedspopulation | Nach 24–48 Stunden | Audience Manager |

>[!NOTE]
>Einmal pro Woche werden alle Daten vollständig synchronisiert, um alle Deltas oder Diskrepanzen zu berücksichtigen, die in der vorherigen Woche nicht erfasst wurden.

## Veröffentlichen von Segmenten in [!UICONTROL Segment Builder]

1. Navigieren Sie in Adobe Analytics zu **[!UICONTROL Komponenten]** > **[!UICONTROL Segmente]**
1. Wählen Sie **[!UICONTROL Hinzufügen]** aus, um ein neues Segment zu erstellen.
   ![Veröffentlichung von CX Enterprise](assets/publish-ec.png)
1. Geben Sie einen Titel und eine Beschreibung für das Segment an. Diese Felder sind erforderlich, bevor Sie das Segment speichern können.
1. Wählen Sie im Abschnitt **[!UICONTROL CX Enterprise-]**) die Option **[!UICONTROL Dieses Segment in CX Enterprise veröffentlichen (für *Report Suite*)]**.

   >[!IMPORTANT]
   >
   >Stellen Sie sicher, dass Sie **[!UICONTROL Besucher mit Experience Cloud-ID]** in der **[!UICONTROL Datenvorschau]** anstelle der **[!UICONTROL Unique Visitors]** überwachen, wenn Sie Adobe Analytics-Zahlen mit Audience Manager-Zahlen vergleichen.
   >

| Element | Beschreibung |
|---|---|
| **[!UICONTROL Dieses Segment in Experience Cloud veröffentlichen (für *Report Suite*)]** | Wenn diese Option aktiviert ist, werden der Segmenttitel und die Definition sofort für CX Enterprise freigegeben, während die Segmentzugehörigkeit alle 4 Stunden ausgewertet und freigegeben wird. <br> Wenn diese Zielgruppe beispielsweise mit einer Aktivität in Target verknüpft ist, sendet [!DNL Analytics] IDs für Besucher, die sich für diese Zielgruppe von CX Enterprise und Target qualifizieren. Ab diesem Zeitpunkt werden der Zielgruppenname und die entsprechenden Daten auf der [!DNL Audience Library] in CX Enterprise angezeigt. </br> |
| **[!UICONTROL Fenster für die Zielgruppenerstellung]** | Der ausgewählte Zeitrahmen wird verwendet, um die Zielgruppe auf rollierender Kalenderbasis zu erstellen. Beispielsweise umfasst **[!UICONTROL Letzte 30 Tage]** (Standard) Besucher, die sich in den letzten 30 Tagen ab dem heutigen Datum für die Zielgruppe qualifiziert haben (NICHT ab dem ursprünglichen Datum, an dem das Segment erstellt wurde). |
| **[!UICONTROL In Zielgruppenbibliothek erstellen]** | Die Segmente, die Sie erstellen und veröffentlichen, können ohne Latenz auf der [!DNL Audience Library] in CX Enterprise verfügbar gemacht werden. Sie sind nicht von Analytics-Aktualisierungen abhängig. Diese Segmente werden nicht Ihrer Beschränkung auf 75 veröffentlichte Segmente angerechnet. |
| **[!UICONTROL x von 75 veröffentlicht]** | Die Anzahl der Segmente, die Sie in CX Enterprise veröffentlicht haben. Klicken Sie auf den Link, um eine Liste der veröffentlichten Segmente mit zugehöriger Report Suite und Eigentümer anzuzeigen. |
| **[!UICONTROL Speichern]** | Speichert dieses Segment. |

## Rückgängigmachen der Veröffentlichung oder Löschen von Segmenten

>[!CAUTION]
>
>Um ein Segment zu löschen, das in CX Enterprise veröffentlicht wurde, müssen Sie die Veröffentlichung des Segments zunächst aufheben. Um die Veröffentlichung eines Segments aufzuheben, heben Sie einfach die Auswahl von **[!UICONTROL Segment in Experience Cloud veröffentlichen (für *Report Suite*)]**.


>[!NOTE]
>
>Sie **die Veröffentlichung** Segments, das derzeit von einer der folgenden Adobe-Lösungen verwendet wird, nicht aufheben: Analytics (in Audience Analytics), Campaign, Advertising (für Kunden von Core Service und Audience Manager) und alle anderen externen Partner (für Kunden von Audience Manager). Sie **können** die Veröffentlichung eines Segments aufheben, das von Target verwendet wird.

## Anzeigen des Veröffentlichungsstatus von Segmenten

Die maximale Anzahl der veröffentlichbaren Adobe Analytics-Segmente beträgt 75.

Anzeigen veröffentlichter Segmente:

1. Navigieren Sie in Adobe Analytics zu **[!UICONTROL Komponenten]** > **[!UICONTROL Segmente]**.

1. Zeigen Sie die Spalte **[!UICONTROL Veröffentlicht]** an. **[!UICONTROL Ja]** in dieser Spalte bedeutet, dass das Segment in CX Enterprise veröffentlicht wurde. **[!UICONTROL Nein]** bedeutet, dass das Segment nicht veröffentlicht ist.

## Abrufen der Audience Manager-UUID

Es gibt zwei Möglichkeiten, die Adobe Audience Manager-UUID zu erfassen, die derzeit mit dem Browser verknüpft ist:

* Adobe CX Enterprise-Debugger
* Natives Entwickler-Tool in Browsern (z. B. Chrome Developer Tools)

Die folgenden Screenshots zeigen Ihnen, wie Sie die Adobe Audience Manager-UUID in Ihrem Browser abrufen und im Audience Manager-Besucherprofil-Viewer verwenden können, um die Trait- und Segmentzugehörigkeit zu überprüfen.

### Methode 1: Verwenden von Adobe CX Enterprise Debugger

1. Laden Sie [Adobe CX Enterprise Debugger](/help/implement/validate/debugger.md) herunter und installieren Sie ihn im Chrome Web Store.
1. Starten Sie den Debugger beim Laden einer Seite.
1. Scrollen Sie zum Abschnitt Audience Manager und suchen Sie die Adobe Audience Manager-UUID, die auf der aktuellen Browser-Seite festgelegt ist
(`35721780439475290181087231320657663953` im folgenden Beispiel)

   ![Debugger](assets/aepdebugger.png)

### Methode 2: Verwenden von Chrome Developer Tools (oder anderen Browser-Entwickler-Tools)

1. Starten Sie Chrome Developer Tools vor dem Laden einer Seite.
1. Laden Sie die Seite und aktivieren Sie „Anwendungen“ > „Cookies“. Die Adobe Audience Manager-UUID sollte im Drittanbieter festgelegt werden
Demdex-Cookie ([adobe.demdex.net](https://experienceleague.adobe.com/de/docs/audience-manager/user-guide/reference/demdex-calls) im folgenden Beispiel). Das Feld demdex ist der Adobe Audience Manager UUID-Satz
im Browser (`35721780439475290181087231320657663953` im folgenden Beispiel).

   ![Chrome Developer Tools](assets/devtools.png)

## Verwenden des Audience Manager-[!UICONTROL Besucherprofil-Betrachters]

Die Adobe Audience Manager-UUID im Browser wird standardmäßig angezeigt, wenn [!UICONTROL Besucherprofil-Viewer] geladen wird. Wenn Sie die Realisierung von Eigenschaften für andere Benutzer überprüfen möchten, geben Sie eine UUID in das UUID-Feld ein und klicken Sie auf [!UICONTROL Aktualisieren]. Weitere Informationen finden Sie unter [Besucherprofil-Betrachter](https://experienceleague.adobe.com/de/docs/audience-manager/user-guide/features/visitor-profile-viewer).

## Anzeigen der Segmenteigenschaften in Audience Manager

In Adobe Audience Manager wird die Besucherliste mit ECIDs für ein bestimmtes Segment ausgewertet, während Analytics Segmente für CX Enterprise freigibt.

1. Navigieren Sie in Audience Manager **[!UICONTROL Zielgruppendaten]** > **[!UICONTROL Eigenschaften]** > **[!UICONTROL Analytics-Eigenschaften]**. Für jede Analytics-Report Suite wird ein Ordner angezeigt, der Ihrer CX Enterprise-Organisation zugeordnet ist. Diese Ordner (für Eigenschaften, Segmente und Data Sources) werden erstellt, wenn der Hauptdienst Profile und Zielgruppen/Personen initiiert oder bereitstellt.
1. Wählen Sie den Ordner für die Report Suite aus, in der Sie zuvor das Segment erstellt haben, das Sie für Audience Manager freigeben möchten. Sie sehen das Segment/die Zielgruppe, das/die Sie erstellt haben. Wenn Sie ein Segment freigeben, passieren in Audience Manager zwei Dinge:
   * Eine Eigenschaft wird erstellt, zunächst ohne Daten. Ca. 8 Stunden nach der Veröffentlichung des Segments in [!DNL Analytics] wird die Liste der ECIDs integriert und für Audience Manager und andere CX Enterprise-Lösungen freigegeben.

     ![Audience Manager-Eigenschaften](assets/aam-traits.png)

   * Es wird ein Segment mit einer Eigenschaft erstellt. Es verwendet die Datenquelle, die mit der Report Suite verknüpft ist, in der Sie das Segment veröffentlicht haben.
   * Die Eigenschaft läuft nun nach 16 Tagen ab (zuvor waren es 2 Tage).

## Anzeigen des Segments in [!DNL Adobe Target]

Mit **[!UICONTROL Dieses Segment in Experience Cloud veröffentlichen]** kann das Segment in der benutzerdefinierten Zielgruppenbibliothek von Adobe Target verfügbar sein. Ein in Analytics oder Audience Manager erstelltes Segment kann für Aktivitäten in Target verwendet werden. Sie können zum Beispiel Kampagnenaktivitäten basierend auf Analytics-Konversionsmetriken und in Analytics erstellten Zielgruppensegmenten erstellen.

In Adobe Target:

1. Wählen Sie **[!UICONTROL Zielgruppen]** aus.
1. Suchen Sie auf **[!UICONTROL Seite]** Audiences“ die Audience, die Sie von CX Enterprise beziehen. Diese Zielgruppen stehen für die Verwendung in Target-Aktivitäten zur Verfügung.

   ![Audiences auswählen](assets/target-audiences.png)
