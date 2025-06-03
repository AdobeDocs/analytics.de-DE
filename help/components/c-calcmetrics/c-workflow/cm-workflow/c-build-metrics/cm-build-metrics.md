---
description: Der Generator für berechnete Metriken bietet eine Arbeitsfläche, mit der Sie Dimensionen, Segmente und Funktionen per Drag-and-Drop verschieben können, um benutzerdefinierte Metriken basierend auf Containerhierarchielogik, Regeln und Operatoren zu erstellen. Mit diesem integrierten Entwicklungs-Tool können Sie einfache berechnete Metriken oder komplexe, erweiterte berechnete Metriken erstellen und speichern.
title: Erstellen von Metriken
feature: Calculated Metrics
exl-id: 12bb3734-e25d-4c67-8c62-e1226d9aef94
source-git-commit: d9f95b12a43305cecff1190e6544334f3b48835d
workflow-type: ht
source-wordcount: '1112'
ht-degree: 100%

---

# Erstellen von Metriken {#build-metrics}

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_externalid"
>title="Externe ID"
>abstract="Eine Änderung der externen ID kann sich auf die Darstellung der berechneten Metrik in externen Quellen auswirken, z. B. auf Business Intelligence-Tools"


Adobe Analytics bietet eine Arbeitsfläche, auf der Sie Dimensionen, Metriken, Segmente und Funktionen per Drag-and-Drop verschieben können, um benutzerdefinierte Metriken basierend auf Container-Hierarchielogik, Regeln und Operatoren zu erstellen. Mit diesem integrierten Entwicklungs-Tool können Sie einfache oder komplexe berechnete Metriken erstellen und speichern.

## Mit dem Erstellen einer berechneten Metrik beginnen

Sie können den Generator für berechnete Metriken verwenden, um berechnete Metriken zu erstellen oder zu bearbeiten. Wenn berechnete Metriken auf diese Weise erstellt werden, sind sie in der Komponentenliste verfügbar und können dann in Projekten in Ihrer gesamten Organisation verwendet werden. Alternativ können Sie schnell eine berechnete Metrik erstellen, die nur für das Projekt verfügbar ist, in dem sie erstellt wurde, wie in [Erstellen berechneter Metriken für ein einzelnes Projekt](/help/analyze/analysis-workspace/components/apply-create-metrics.md#create-calculated-metrics-for-a-single-project) in [Metriken](/help/analyze/analysis-workspace/components/apply-create-metrics.md) beschrieben.

Greifen Sie auf den Generator für berechnete Metriken zu, um mit der Erstellung einer berechneten Metrik zu beginnen, die in der Komponentenliste verfügbar ist.

1. Greifen Sie auf eine der folgenden Arten auf den Generator für berechnete Metriken zu:

   * Öffnen Sie ein Projekt in Analysis Workspace und wählen Sie dann **[!UICONTROL Komponenten]** > **[!UICONTROL Metrik erstellen]** aus.
   * Öffnen Sie ein Projekt in Analysis Workspace und wählen Sie dann in der linken Leiste das **Plus**-Symbol neben dem Abschnitt [!UICONTROL **Metriken**] aus.
   * Navigieren Sie in [!DNL Adobe Analytics] zu **[!UICONTROL Komponenten]** > **[!UICONTROL Berechnete Metriken]** und wählen Sie dann **[!UICONTROL + Hinzufügen]** oben auf der Seite „Berechnete Metriken“ aus.

1. Fahren Sie mit [Bereiche des Generators für berechnete Metriken](#areas-of-the-calculated-metrics-builder) fort.

## Bereiche des Generators für berechnete Metriken

Das folgende Bild und die dazugehörige Tabelle erläutern einige der Hauptbereiche und -funktionen des Generators für berechnete Metriken.

![](assets/cm_builder_ui.png)

| Position im Bild | Name und Funktion |
|---|---|
| 1 | **Titel**: Ein Name für die Metrik ist obligatorisch. Sie können nur benannte Metriken speichern. |
| 2 | **Beschreibung**: Geben Sie der Metrik eine benutzerfreundliche Beschreibung, um ihren Zweck anzugeben und sie von ähnlichen Metriken zu unterscheiden. <p>Die Beschreibung wird auch in Berichten angezeigt. Sie sollten die Formel NICHT in die Beschreibung aufnehmen. Erläutern Sie stattdessen, wofür diese Metrik verwendet werden sollte und wofür nicht. (Die Formel wird unter der Überschrift „Zusammenfassung“ generiert, während Sie die Metrik erstellen. Daher müssen Sie die Formel nicht noch der Beschreibung hinzufügen.) </p> |
| 3 | **Format**: Hier können Sie zwischen „Dezimal“, „Zeit“, „Prozent“ und „Währung“ wählen. |
| 4 | **Dezimalstellen**: Zeigt an, wie viele Dezimalstellen im Bericht angezeigt werden. Sie können maximal 10 Dezimalstellen angeben. |
| 5 | **Aufwärts-Trend anzeigen als**: Diese Einstellung für die Metrikpolarität legt fest, ob Analytics einen Aufwärts-Trend in der Metrik als positiv (grün) oder negativ (rot) betrachten soll. Dementsprechend wird ein steigendes Diagramm des Berichts grün oder rot angezeigt. |
| 6 | **Tags**: Anhand von Tagging können Metriken praktisch organisiert werden. Alle Benutzer können Tags erstellen und eines oder mehrere Tags auf eine Metrik anwenden. Sie sehen Tags jedoch nur für die Segmente, deren Inhaber Sie sind oder die für Sie freigegeben wurden. Welche Arten von Tags sollten Sie erstellen? Hier finden Sie einige Vorschläge für nützliche Tags:<ul><li>**Team-Namen** wie Social-Media-Marketing, Mobil-Marketing.</li><li>**Projekte** (Analyse-Tags) wie Einstiegsseitenanalyse.</li><li>**Kategorien** wie Frauen oder Geografie.</li><li>**Workflows** wie: Genehmigung ausstehend, kuratiert für (einen bestimmten Geschäftsbereich)</li></ul> |
| 7 | **Zusammenfassung**: <p>Die Formel unter „Zusammenfassung“ wird jedes Mal aktualisiert, wenn Sie die Metrikdefinition ändern. Diese Formel wird außerdem in der Metrikleiste links angezeigt, wenn Sie mit der Maus auf eine Metrik zeigen und auf das Symbol <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Info_18_N.svg" id="image_BDA0EAF89C19440CB02AE248BA3F968E" /> klicken. </p> |
| 8 | **Definition**: Hierhin ziehen Sie die Metriken/berechneten Metriken, Segmente und/oder Funktionen, um die berechnete Metrik zu erstellen. <ul><li>Wenn Sie eine berechnete Metrik hierhin ziehen, wird die zugehörige Metrikdefinition automatisch eingeblendet. </li> <li>Sie können Definitionen mit Containern verschachteln. Im Gegensatz zu Segmentcontainern funktionieren diese Container allerdings wie ein mathematischer Ausdruck und bestimmen die Reihenfolge der Vorgänge. </li> </ul> |
| 9 | **Operator:** „Geteilt durch“ ( <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Divide_18_N.svg" width="15" id="image_320D7363DE024BDEB21E44606C8B367F" width="25px" />) ist der Standardoperator. Darüber hinaus gibt es die Operatoren „+“, „-“ und „x“. |
| 10 | **Vorschau**: Ermöglicht einen schnellen Einblick in potenzielle Fehler. Die Vorschau deckt die letzten 90 Tage ab. So können Sie schnell einschätzen, ob Sie die richtigen Komponenten für die Metrik ausgewählt haben. Bei einem unerwarteten Ergebnis müssten Sie die Metrikdefinition noch einmal genauer prüfen. |
| 11 | **Produktkompatibilität**: Dank der Produktkompatibilität können Sie sehen, ob die Metrik mit <a href="https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/current-data.html?lang=de"  > aktuellen Daten </a>, mit vollständig verarbeiteten Daten oder nur mit Marketing-Kanalberichten (Erstkontaktzuordnung) kompatibel ist. <p>Hinweis: Bei aktuellen Daten werden nicht alle Metriken unterstützt. Metriken mit Segmenten oder Funktionen sind nicht mit aktuellen Daten kompatibel. <a href="/help/components/c-calcmetrics/cm-compatibility.md"  > Mehr... </a> </p> </p> |
| 12 | **Hinzufügen**: Sie können Container und statische Nummern zu den Definitionen aller Arten berechneter Metriken hinzufügen. Für erweiterte berechnete Metriken können Sie auch Segmente und Funktionen hinzufügen. <ul><li>Container funktionieren wie mathematische Ausdrücke und bestimmen die Reihenfolge der Vorgänge. Jedes Element in einem Container wird also vor dem nächsten Vorgang verarbeitet.</li><li>Wenn Sie ein Segment in einen Container ziehen, werden alle Elemente in diesem Container segmentiert. (Nur erweiterte berechnete Metriken)</li><li>Sie können mehrere Segmente in einem Container stapeln.</li></ul> |
| 13 | **Zahnradsymbol (Metriktyp, Attribution)**: Wenn Sie das Zahnradsymbol neben einer Metrik auswählen, können Sie den <a href="/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md"  > Metriktyp und die Attributionsmodelle </a> angeben. |
| 14 | **Neu**: Ermöglicht Ihnen die Erstellung einer neuen Komponente, z. B. eines neuen Segments (Sie werden zum <a href="/help/components/segmentation/segmentation-workflow/seg-build.md"  > Segment Builder </a> geleitet). |
| 15 | **Komponenten suchen**: Mit dieser Suchleiste können Sie nach Dimensionen, Metriken, Segmenten (nur erweiterte berechnete Metriken) und Funktionen (nur erweiterte berechnete Metriken) suchen. |
| 16 | **Liste der Dimensionen:**: Zum Erstellen eines einfachen Segments (im Segment Builder) brauchen Sie den Generator für berechnete Metriken nicht zu verlassen (z. B. „Seite = Homepage“). Sie können nämlich das Element „Seite“ hereinziehen und „Homepage“ direkt im Generator für berechnete Metriken auswählen.<p>So profitieren Sie von einem deutlich optimierten Arbeitsablauf bei der Erstellung segmentierter berechneter Metriken.</p> |
| 17 | **Liste der Metriken:** Metriken sind in drei Kategorien unterteilt: <ul> <li>Standardmetriken (<img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Event_18_N.svg" id="image_65A80F54D73443E78542FE0B31CC3F20" />) </li><li>Berechnete Metriken ( <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calculator_18_N.svg" id="image_C5674AB9B9EB4DA9A56782D15822C319" />) </li><li id="li_8735E76637ED4C3F983731A66E04C93E">Metrikvorlagen ( <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Folder_18_N.svg" id="image_D236601511CC4DD3828F223431E27E88" />) – unten in der Liste. </li> </ul> <p>Wenn Sie den Mauszeiger über eine Metrik bewegen, wird das Infosymbol rechts neben der Metrik angezeigt. <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Info_18_N.svg" width="15px" id="image_5A65E772A68A4B94ACAD6552CCF21F5F" />. Durch Klicken auf dieses Symbol erhalten Sie die folgenden Informationen: </p><ul> <li>Die Formel für die Berechnung der Metrik. </li><li>Ein Vorschautrend der Metrik. </li><li>Ein Bearbeitungssymbol (Bleistift) <img placement="break" align="center"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg" width="15px" id="image_7D5B2F026A034118BE4DA81B9215A883" /> oben rechts, über das Sie zum Generator für berechnete Metriken gelangen, wo Sie diese berechnete Metrik bearbeiten können. </li></ul> |
| 18 | **Liste der Segmente:**: (Nur erweiterte berechnete Metriken) Wenn Sie Admin sind, enthält diese Liste alle in Ihrer Unternehmensanmeldung erstellten Segmente. Wenn Sie kein Administrator sind, enthält diese Liste Segmente, deren Eigentümer Sie sind, sowie Segmente, die für Sie freigegeben wurden. <a href="https://experienceleague.adobe.com/docs/analytics/components/segmentation/segment-reference/seg-rights.html?lang=de"  > Mehr... </a> |
| 19 | **Liste der Funktionen:** (Nur erweiterte berechnete Metriken) Funktionen sind in zwei Listen unterteilt: <a href="/help/components/c-calcmetrics/cm-reference/cm-functions.md"  > Einfach </a> (am häufigsten verwendet) und <a href="/help/components/c-calcmetrics/cm-reference/cm-adv-functions.md"  > Erweitert </a>. |
| 20 | **Report Suite-Auswahlhilfe:** Damit können Sie zu einer anderen Report Suite wechseln. |

{style="table-layout:auto"}
