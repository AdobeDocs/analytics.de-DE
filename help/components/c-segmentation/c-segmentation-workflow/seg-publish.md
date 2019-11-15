---
description: Ermöglicht die Verwendung des Segments für Marketingaktivitäten in der Zielgruppenbibliothek, in Target und im Audience Manager.
solution: Analytics
title: Segmente in der Experience Cloud veröffentlichen
topic: Segments
uuid: e5ce20c0-ce43-423b-a29f-ba66e9e24d27
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Segmente in der Experience Cloud veröffentlichen

>[!IMPORTANT]
>
>Die auf dieser Seite beschriebenen Verbesserungen der Latenz bei der Segmentveröffentlichung und der Benutzeroberfläche sind noch nicht für alle Kunden verfügbar. Die aktuelle Produktionsumgebung wird [hier](https://docs.adobe.com/content/help/en/core-services/interface/audiences/t-publish-audience-segment.html)beschrieben.

Publishing a segment to the Experience Cloud lets you use the segment for marketing activity in the [!UICONTROL Audience Library], [!DNL Target], [!DNL Audience Manager], [!DNL Advertising Cloud], and [!DNL Campaign]. Die neuesten Updates haben den Veröffentlichungsarbeitsablauf erheblich optimiert. Bisher dauerte die Veröffentlichung eines brauchbaren Segments etwa 48 Stunden.

Die Verarbeitung kann jetzt bis zu 8 Stunden dauern, aber je nach anderem Traffic und der Segmentgröße kann die Verarbeitung sogar noch schneller erfolgen. (Derzeit haben wir jedoch keine Möglichkeit, Sie darüber zu informieren, wann das Segment verfügbar ist. Daher müssen Sie es manuell überprüfen.) Außerdem haben wir die maximale Anzahl an publizierbaren Segmenten von 20 auf 75 erhöht. Sie können veröffentlichte Segmente unter Komponenten &gt; Segmente anzeigen.

> [!NOTE] Adobe Campaign (Classic und Standard) verhält sich anders, da es eine zusätzliche Latenz von 24 Stunden über der 8-Stunden-Latenz erzielt.


## Voraussetzungen

* Ensure that the report suite that you are saving this segment to is [enabled for the Experience Cloud](https://docs.adobe.com/content/help/en/core-services/interface/audiences/t-publish-audience-segment.html). Andernfalls können Sie sie nicht in der Experience Cloud veröffentlichen.
* Vergewissern Sie sich, dass Sie an einer Report Suite arbeiten, die Ihrer Experience Cloud-Organisation [zugeordnet](https://docs.adobe.com/content/help/en/core-services/interface/about-core-services/report-suite-mapping.html)ist.
* Stellen Sie sicher, dass Ihr Unternehmen Experience Cloud IDs verwendet.
* Bevor Sie Segmente veröffentlichen können, muss Ihr Administrator einem Produktprofil in der [!UICONTROL Admin-Konsole]die Berechtigung für die [Segmentveröffentlichung](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/admin-getting-started.html) zuweisen und Sie zum Produktprofil hinzufügen.


## Zu beachten

* **Report Suite-Beschränkungen**: Sie können bis zu 75 Segmente pro Report Suite veröffentlichen. Diese Beschränkung wird erzwungen. Wenn Sie bereits 75 Segmente veröffentlicht haben, können Sie keine weiteren Segmente veröffentlichen, bis Sie genügend Segmente aufheben, um unter den Schwellenwert von 75 Segmenten zu gelangen.
* **Mitgliedsbeschränkungen**: Zielgruppen, die über Analytics für die [!DNL Experience Cloud] Zielgruppe freigegeben werden, dürfen 20 Millionen individuelle Mitglieder nicht überschreiten.
* **Datenschutz**: Zielgruppen werden nicht basierend auf dem Authentifizierungsstatus eines Besuchers gefiltert. Wenn Besucher Ihre Site sowohl authentifiziert als auch nicht authentifiziert anzeigen können, kann eine Aktion, die ein nicht authentifizierter Benutzer durchführt, dennoch dazu führen, dass der Besucher in die Zielgruppe aufgenommen wird. Lesen Sie sich die [Adobe Experience Cloud-Datenschutzbestimmungen](https://www.adobe.com/privacy/experience-cloud.html) durch, um die Auswirkungen der Zielgruppenfreigabe auf den Datenschutz zu verstehen.
* Eine Diskussion über die **Unterschiede zwischen Segmenten in[!DNL Adobe Analytics]und[!DNL Audience Manager]** finden Sie [hier](https://docs.adobe.com/content/help/en/analytics/integration/audience-analytics/audience-analytics-workflow/aam-analytics-segments.html).

## Zeitschiene Segmentveröffentlichung

| Verfügbare Elemente | Sobald es verfügbar ist | Wo es verfügbar ist |
|---|---|---|
| Metadaten (Segmenttitel und Definition) | Sofort nach der Veröffentlichung | [!DNL Audience Manager], [!UICONTROL Experience Cloud-Zielgruppenbibliothek], [!DNL Target] |
| Benutzerbares Segment mit Mitgliedschaft | ~ 8 Stunden nach der Veröffentlichung | Besucherprofil-Viewer in [!DNL Audience Manager] |
| Eigenschaften- und Mitgliedspopulation | Innerhalb von 24-48 Stunden | [!DNL Audience Manager] |

## Veröffentlichen von Segmenten im [!UICONTROL Segmentaufbau]

1. Navigieren Sie zu **[!UICONTROL Analytics &gt; Arbeitsbereich &gt; Komponenten &gt; Segmente]&gt; +**
1. Erstellen Sie ein Segment im [!UICONTROL Segmentaufbau].
1. Geben Sie einen Titel und eine Beschreibung für das Segment ein. Andernfalls können Sie es nicht speichern.
1. Check **[!UICONTROL Publish this segment to the Experience Cloud (for *report suite*)]**.

![](assets/publish-ec.png)

>[!IMPORTANT]
>
>Stellen Sie sicher, dass Sie "Besucher mit Experience Cloud ID"verwenden, wenn Sie Segmentvorschauen in Analytics anstelle der Segmentvorschau "Unique Visitors"insgesamt betrachten, wenn Sie Adobe Analytics-Zahlen mit Audience Manager-Zahlen vergleichen:
>
>![](assets/seg-vis-ecid.png)

| Element | Beschreibung |
|---|---|
| **[!UICONTROL Dieses Segment in Experience Cloud veröffentlichen (für *<report suite>*)]** | Wenn diese Option aktiviert ist, werden der Segmenttitel und die Definition (d. h. die Shell-Zielgruppe, wie sie häufig in Anzeigenplattformen verwendet wird) sofort für die Experience Cloud freigegeben, während die Segmentmitgliedschaft ausgewertet und alle 4 Stunden freigegeben wird. <br> Wenn diese Zielgruppe mit einer Aktivität verknüpft ist, beginnt [!DNL Target]beispielsweise [!DNL Analytics] mit dem Senden von IDs für Besucher, die sich für diese Experience Cloud und [!DNL Target] Zielgruppe qualifizieren. Ab diesem Zeitpunkt werden der Zielgruppenname und die zugehörigen Daten auf der Experience Cloud Audiences-Seite angezeigt. </br> |
| **[!UICONTROL Fenster für die Zielgruppenerstellung]** | Der von Ihnen ausgewählte Zeitraum wird verwendet, um die Zielgruppe in einem rollierenden Kalender zu erstellen. "Letzte 30 Tage"(Standard) umfasst zum Beispiel Besucher, die sich in den letzten 30 Tagen ab dem heutigen Datum für die Zielgruppe qualifiziert haben (NICHT ab dem ursprünglichen Datum, an dem das Segment erstellt wurde). |
| **[!UICONTROL In Zielgruppenbibliothek erstellen]** | Die Segmente, die Sie erstellen und veröffentlichen, können in der Experience Cloud-Zielgruppenbibliothek ohne Latenz zur Verfügung gestellt werden. Sie sind nicht von Analytics-Aktualisierungen abhängig. Diese Segmente werden nicht mit Ihrer Beschränkung auf 75 veröffentlichte Segmente angerechnet. |
| **[!UICONTROL x von 75 Veröffentlicht]** | Zeigt die Anzahl der Segmente an, die Sie in Experience Cloud veröffentlicht haben. Klicken Sie auf den Link, um eine Liste der veröffentlichten Segmente und der zugehörigen Report Suite und des Eigentümers anzuzeigen. |
| **[!UICONTROL Speichern]** | Speichert dieses Segment. |

## Rückgängigmachen der Veröffentlichung oder Löschen von Segmenten

Um ein in Experience Cloud veröffentlichtes Segment zu löschen, müssen Sie zuerst die Veröffentlichung rückgängig machen. Um die Veröffentlichung eines Segments rückgängig zu machen, **deaktivieren Sie einfach das Kontrollkästchen**, das Sie zum Veröffentlichen aktiviert haben.

> [!NOTE]Sie können die Veröffentlichung eines Segments **nicht** rückgängig machen, das aktuell von einer der folgenden Adobe-Lösungen verwendet wird: [!DNL Analytics] (in [!DNL Audience Analytics]), [!DNL Campaign], [!DNL Advertising Cloud] (für Kunden von [!DNL Core Service] und [!DNL Audience Manager]) und alle anderen externen Partner (für Kunden von [!DNL Audience Manager]). Die Veröffentlichung eines Segments, das von [!DNL Target] verwendet wird, **kann** rückgängig gemacht werden.

## Anzeigen des Segmentveröffentlichungsstatus im [!UICONTROL Segment-Manager]

1. Navigieren Sie zu [!UICONTROL Analytics &gt; Komponenten &gt; Segmente].
1. Beachten Sie die neue Spalte [!UICONTROL Veröffentlicht] . Ja/Nein bezieht sich darauf, ob das Segment in der Experience Cloud veröffentlicht wurde oder nicht.

![](assets/publish-status.png)

## Abrufen der [!DNL Audience Manager] UUID

Es gibt zwei Möglichkeiten, die AAM UUID zu erfassen, die derzeit mit dem Browser verknüpft ist:

* Adobe Experience Cloud-Debugger
* Natives Developer Tool in Browsern (z. B. Chrome Developer Tools)

Die folgenden Screenshots zeigen Ihnen, wie Sie die AAM-UUID in Ihrem Browser abrufen und sie in Audience Manager-Besucherprofil-Viewer verwenden, um Eigenschaften- und Segmentmitgliedschaften zu validieren.

**Methode 1: Adobe Experience CLoud Debugger verwenden**

1. Laden Sie den [Adobe Experience Cloud-Debugger](https://docs.adobe.com/content/help/en/analytics/implementation/testing-and-validation/debugger.html) im Chrome Web Store herunter und installieren Sie ihn.
1. Starten Sie den Debugger, wenn Sie eine Seite laden.
1. Blättern Sie zum Audience Manager-Abschnitt und suchen Sie die AAM UUID, die auf der aktuellen Browserseite eingestellt ist (`50814298273775797762943354787774730612` im Beispiel unten).

![](assets/debugger.jpg)

**Methode 2: Verwenden Sie die Chrome Developer Tools (oder andere Browser-Entwicklerwerkzeuge)**

1. Starten Sie Chrome Developer Tools, bevor Sie eine Seite laden
1. Laden Sie die Seite und aktivieren Sie Anwendungen &gt; Cookies. Die AAM-UUID sollte im Drittanbieter-Demdex-Cookie ([adobe.demdex.net](https://marketing.adobe.com/resources/help/en_US/aam/demdex-calls.html) im Beispiel unten) festgelegt werden. Das Feld demdex ist die AAM UUID-Einstellung im Browser (`50814298273775797762943354787774730612` im Beispiel unten).

![Chrome Developer Tools](assets/ggogle-uuid.png)

## Verwenden des Audience Manager- [!UICONTROL Besucherprofil-Viewers]

Die AAM-UUID im Browser wird standardmäßig verwendet, wenn der [!UICONTROL Besucherprofil-Viewer] geladen wird. Wenn Sie die Eigenschaften für andere Benutzer überprüfen, geben Sie eine UUID in das Feld UUID ein und klicken Sie auf [!UICONTROL Aktualisieren]. Weitere Informationen finden Sie im [Besucherprofil-Viewer](https://marketing.adobe.com/resources/help/en_US/aam/t_visitor_profile_viewer.html) .

![](assets/aam-vpv.png)

## Segmentmerkmale anzeigen unter [!DNL Audience Manager]

In AAM wird die Liste der Besucher mit ECIDs für ein bestimmtes Segment als Streaming ausgewertet, da Analytics Segmente mit Experience Cloud teilt.

1. Gehen Sie [!DNL Audience Manager]zu [!UICONTROL Zielgruppendaten &gt; Eigenschaften &gt; Analytics-Eigenschaften]. Es wird ein Ordner für jede Analytics Report Suite angezeigt, der Ihrer Experience Cloud-Organisation zugeordnet ist. Diese Ordner (für Eigenschaften, Segmente und Datenquellen) werden erstellt, wenn der Hauptdienst Profile und Zielgruppen/Personen initiiert oder bereitgestellt wird.
1. Wählen Sie den Ordner für die Report Suite aus, in der Sie zuvor das Segment erstellt haben, für das Sie freigeben möchten [!DNL Audience Manager]. Sie sehen das Segment/die Zielgruppe, das/die Sie erstellt haben. Wenn Sie ein Segment freigeben, geschieht dies in zwei Bereichen: [!DNL Audience Manager]
* Eine Eigenschaft wird erstellt, zunächst ohne Daten. Ungefähr. 8 Stunden nach der Veröffentlichung des Segments in [!DNL Analytics]wird die Liste der ECIDs für [!DNL Audience Manager] und andere Experience Cloud-Lösungen integriert und freigegeben.

![](assets/aam-traits.png)

* Es wird ein Einwegsegment erstellt. Es verwendet die Datenquelle, die mit der Report Suite verknüpft ist, in der Sie das Segment veröffentlicht haben.

## Anzeigen des Segments in [!DNL Adobe Target]

The [!UICONTROL Publish this segment to the Experience Cloud] checkbox during the segment creation process in Adobe Analytics allows the segment to be available within the Adobe Target's custom audience library. Ein in Analytics oder Audience Manager erstelltes Segment kann für Aktivitäten in Target verwendet werden. Sie können zum Beispiel Kampagnenaktivitäten basierend auf Analytics-Konversionsmetriken und in Analytics erstellten Zielgruppensegmenten erstellen.
] klicken Sie auf [!UICONTROL Zielgruppen].
1. On the [!UICONTROL Audiences] page, locate the audience sourced from the [!DNL Experience Cloud]. These audiences are available for use in [!DNL Target] activities.

