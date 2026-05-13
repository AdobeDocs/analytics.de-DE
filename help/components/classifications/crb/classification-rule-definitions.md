---
description: Definitionen der Elemente auf den Seiten im Classification Rule Builder.
title: Klassifizierungsregeln – Definitionen
feature: Classifications
exl-id: 514501d1-7e1b-45da-b8fe-c68331e59dab
TQID: https://experienceleague.adobe.com/8SDdKOvF-Mk9jQCb7YWXt0NCl0dspfscnHL02y1cxKM
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 861
ht-degree: 56%

---

# Klassifizierungsregeldefinitionen (veraltet)

{{classification-rulebuilder-deprecation}}

Definitionen der Elemente auf den Seiten im Classification Rule Builder.

## Seite „Regeln“

Auf dieser Seite werden die Regeln in einem Regelsatz angezeigt.

![](assets/classification_rules_page.png)

**Definitionen**

<table id="table_2B3A8BB7BDE14836ACA6A1D444B011CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Report Suites und Variablen auswählen </p> </td> 
   <td colname="col2"> <p><b>Report Suite</b> </p> <p>Die Report Suites, für die der Regelsatz gilt. </p> <p><b>Variable</b> </p> <p>Sie können beim Erstellen eines Klassifizierungsregelsatzes nur eine Variable anwenden. Wenn Sie mehrere Regelsätze für eine Variable erstellen möchten, müssen Sie jeden Regelsatz auf mehrere Report Suites anwenden. </p> <p>Hinweis: Sie können nur die Variablen verwenden, auf die Sie in Ihren Report Suites Zugriff haben. Variablen werden erst im Bereich <span class="wintitle">Neuer Regelsatz</span> angezeigt, nachdem mindestens eine Classification für diese Variable definiert wurde. </p> <p> Sie können Classifications für eine Variable unter <span class="uicontrol">Admin</span> &gt; <span class="uicontrol">Report Suites</span> &gt; <span class="uicontrol">Traffic</span> &gt; <span class="uicontrol">Traffic-Classifications</span> (oder <span class="uicontrol">Konversion</span> &gt; <span class="uicontrol">Konversion-Classifications</span>) erstellen. Wählen Sie dann die Variable aus und klicken Sie auf <span class="uicontrol">Classification hinzufügen</span>. </p> <p>Weitere Informationen finden Sie in der Admin-Hilfe unter <a href="/help/admin/tools/manage-rs/edit-settings/c-traffic-variables/traffic-classifications.md"  >Traffic-Classifications</a> und <a href="/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/conversion-classifications.md"  >Konversion-Classifications</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="wintitle"> Aktivieren</span> </p> </td> 
   <td colname="col2"> <p>Validiert und aktiviert eine Regel. Aktive Regeln werden täglich verarbeitet und untersuchen Klassifizierungsdaten, die in der Regel einen Monat zurückgehen. Die Regeln überprüfen automatisch auf neue Werte und laden die Klassifizierungen hoch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="wintitle"> Deaktivieren</span> </p> </td> 
   <td colname="col2"> <p>Deaktiviert die Regeln, so dass Sie sie bearbeiten und testen können. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Konfigurieren von Report Suites und Variablen </p> </td> 
   <td colname="col2"> <p>Zeigt die Seite <span class="wintitle">Verfügbare Report Suites</span> an, auf der Sie verfügbare Report Suites auswählen können, die für alle Regelsätze verwendet werden sollen. (Diese Seite wird auch angezeigt, wenn Sie den <span class="wintitle">Classification Rule Builder</span> zum ersten Mal ausführen.) </p> <p>Mit dieser Funktion soll die Ladezeit für Report Suites reduziert werden, falls Hunderte Report Suites verfügbar sind. </p> <p>Die hier gewählten Report Suites werden auf Regelebene verfügbar gemacht, wenn Sie auf <span class="uicontrol">Suites hinzufügen</span> klicken, während Sie eine Regel erstellen. </p> <p>Hinweis: Eine Report Suite steht <span class="term"> nur</span> zur Verfügung, wenn in den Report Suites mindestens eine Classification für die Variable in den <span class="wintitle"> Admin Tools</span> definiert ist. <p>(Eine Erläuterung zu dieser Voraussetzung finden Sie unter <span class="term">Variable</span> unter <a href="/help/components/classifications/crb/classification-rule-set.md"  >Klassifizierungsregelsätze</a>.) </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Regeln überschreiben alle vorhandenen Werte. </p> </td> 
   <td colname="col2"> <p> (Standardeinstellung) Überschreiben Sie immer vorhandene Klassifizierungsschlüssel, einschließlich der über das Importtool (SAINT) hochgeladenen Klassifizierungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Regeln überschreiben nur nicht festgelegte Werte. </p> </td> 
   <td colname="col2"> <p>Nur leere (nicht aktivierte) Zellen ausfüllen. Bestehende Klassifizierungen werden nicht geändert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lookback-Fenster </p> </td> 
   <td colname="col2"> <p>Wenn Sie Regeln aktivieren und validieren, können Sie angeben, ob die Regeln vorhandene Classifications für die betroffenen Schlüssel überschreiben sollen. (Hiervon sind ausschließlich klassifizierte Schlüssel betroffen, die vorher im angegebenen Zeitraum an <span class="keyword">Adobe Analytics</span> übergeben wurden.) </p> <p>Wenn Sie kein <span class="term"> Lookback-Fenster angeben</span> sehen die Regeln ungefähr einen Monat zurück (je nach aktuellem Tag des Monats). Bestehende Klassifizierungen werden nur überschrieben, wenn Sie diese Option aktivieren. </p> <p><b>Entwicklungszentrum</b>: Partner können im <span class="wintitle">Entwicklungszentrum</span> Classification-Regeln erstellen. Diese Regeln werden bereitgestellt, wenn der Kunde eine Integration aktiviert. Mit der Option <span class="wintitle">„Seit“ überschreiben</span> im <span class="uicontrol">Entwicklungszentrum</span> kann der Partner angeben, ob der Kunde den Überschreibungswert festlegen kann, wenn er eine Integration aktiviert oder bearbeitet. </p> <p>Weitere Informationen zur Verarbeitung von Regeln finden Sie unter <a href="/help/components/classifications/crb/classification-quickstart-rules.md"  >Verarbeitung der Regeln</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="/help/components/classifications/crb/classification-quickstart-rules.md"  > Regel hinzufügen </a> </td> 
   <td colname="col2"> <p>Hier können Sie Regeln zum Regelsatz hinzufügen. </p> <p>Hinweis: Wenn für einen Wert zwei oder mehr Übereinstimmungen in einem Regelsatz vorliegen, wird dieser Wert anhand der jeweils letzten Regel klassifiziert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Entwurf</span> </td> 
   <td colname="col2"> Hier können Sie angeben, dass sich eine Regel im Entwurfsmodus befindet. Mit dem Entwurfsstatus können Sie die Regel testen, bevor Sie sie ausführen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Duplizieren</span> </td> 
   <td colname="col2"> Dupliziert (kopiert) einen Regelsatz, so dass Sie diesen Regelsatz auf eine andere Variable anwenden können (oder auch auf dieselbe Variable in einer anderen Report Suite). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="/help/components/classifications/crb/classification-quickstart-rules.md"  > Testregelsatz </a> </p> </td> 
   <td colname="col2"> <p>Hier testen Sie die Validität eines Regelsatzes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Übereinstimmende Bedingung</span> </td> 
   <td colname="col2"> Bestimmt die Bedingungen für die Regel. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Classification-Aktion</span> </td> 
   <td colname="col2"> <p>Gibt die Aktion an, die bei Auftreten der Übereinstimmungsbedingung ausgeführt werden soll. </p> <p>Sie legen beispielsweise einen Kampagnennamen auf $2 fest, wodurch Position 2 in einem Trackingcode als Kampagnenname identifiziert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> #</span> </td> 
   <td colname="col2"> <p>Die Nummer der Regel. </p> <p>Weitere Informationen finden Sie unter <a href="/help/components/classifications/crb/classification-quickstart-rules.md"  > Verarbeitung </a> Regeln . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Regeltyp auswählen</span> </td> 
   <td colname="col2"> <p>Jeder Regelsatz gilt für eine bestimmte Variable. Gültige Auswahlen sind: </p> 
    <ul id="ul_6A8E06BB4AF2402B99C215823CB3D59D"> 
     <li id="li_5C702D4F460841D38A59621A5161A3BC">Beginnt mit </li> 
     <li id="li_8052A741D9F34A2FBC136C181600193E">Endet mit </li> 
     <li id="li_D0FA6EA4F09644FFBC9E6BC568BE80AC">Enthält </li> 
     <li id="li_48675FE5253942ED887C6A72D1DCEF54"> <a href="/help/components/classifications/crb/classification-quickstart-rules.md"  > Regulärer Ausdruck </a> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Übereinstimmungskriterien eingeben</span> </td> 
   <td colname="col2"> Das gesuchte Textmuster in einer Taste. Bei diesen Kriterien kann es sich um Suchbegriffe, Zeichen oder reguläre Ausdrücke handeln. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Classification auswählen</span> </td> 
   <td colname="col2"> Die Classification-Spalte, die festgelegt werden soll, wenn die Übereinstimmungskriterien erfüllt sind. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Hierzu</span> </td> 
   <td colname="col2"> Der Wert, den Sie für die ausgewählte Classification-Spalte angeben möchten, wenn die Übereinstimmungskriterien erfüllt sind. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Filter </td> 
   <td colname="col2"> Ermöglicht die Suche nach Regeln. </td> 
  </tr> 
 </tbody> 
</table>

## Seite Regulärer Ausdruck {#section_C932A5469E774841B2229965A154163C}

Sie können reguläre Ausdrücke auf der Seite &quot;[!UICONTROL &quot; ].

![](assets/regex_tracking_code.png)

**Definitionen**

| Element | Beschreibung |
|---|---|
| Beispielschlüssel | Die zu verwendende Testzeichenfolge. Sie können beispielsweise eine Classification aus bestimmten Zeichen in einem Trackingcode erstellen. Sie können bestimmte Zeichen, Wörter oder Zeichenmuster zuordnen. |
| Übereinstimmungsgruppen | Zeigt, wie der reguläre Ausdruck den Kampagnen-ID-Zeichen entspricht, damit Sie eine Position in der Kampagnen-ID klassifizieren können. |
| Übereinstimmungsergebnis | Zeigt die Teile einer Zeichenfolge an, die dem regulären Ausdruck erfolgreich entsprechen. |

Siehe [Reguläre Ausdrücke in Klassifizierungsregeln](/help/components/classifications/crb/classification-quickstart-rules.md).

## Seite „Tests“ {#section_EC926F97901C4E65901413F9683AA70A}

Auf dieser Seite können Sie Regeln in einem Satz testen.

**Definitionen**

| Element | Beschreibung |
|---|---|
| Test ausführen | Verwenden Sie beim Testen des Regelsatzes die Schlüssel des Berichts, um zu sehen, wie sich der Regelsatz auf sie auswirkt. |
| Filter | Filtert die Werte im Bedienfeld [!UICONTROL Ergebnisse]. |
