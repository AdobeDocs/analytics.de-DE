---
description: Ein Regelsatz ist eine Gruppe von Classification-Regeln für eine bestimmte Variable. Auf den Regelsatz wird eine Variable angewendet. Sollen mehrere Regelsätze für eine einzelne Variable erstellt werden, so müssen Sie jeden Regelsatz auf mehrere Report Suites anwenden.
subtopic: Classifications
title: Klassifizierungsregelsätze
topic: Admin tools
uuid: c4d7b77c-fa98-44be-955f-9aee7f73480b
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Klassifizierungsregelsätze

Ein Regelsatz ist eine Gruppe von Classification-Regeln für eine bestimmte Variable. Auf den Regelsatz wird eine Variable angewendet. Sollen mehrere Regelsätze für eine einzelne Variable erstellt werden, so müssen Sie jeden Regelsatz auf mehrere Report Suites anwenden.

## Klassifizierungsregelsätze

Ein Regelsatz ist eine Gruppe von Classification-Regeln für eine bestimmte Variable. Auf den Regelsatz wird eine Variable angewendet. Sollen mehrere Regelsätze für eine einzelne Variable erstellt werden, so müssen Sie jeden Regelsatz auf mehrere Report Suites anwenden.

## Classification Rule Builder-Seite {#section_C60B0888C76D49C596EF19F11808B718}

**[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Classification Rule Builder]**

Die Seite [!UICONTROL Classifications Rule Builder] bietet die nachfolgenden Felder und Optionen.

<table id="table_A5D92409969747E39E041216A5AA32CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><a href="/help/components/c-classifications2/crb/classification-rule-set.md"  > Regelsatz hinzufügen</a> </p> </td> 
   <td colname="col2"> <p>Erstellt einen Regelsatz. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Regeln </p> </td> 
   <td colname="col2"> Zeigt die Anzahl der Regeln im Regelsatz an. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Status </p> </td> 
   <td colname="col2"> Zeigt den Aktivitätsstatus des Regelsatzes an, beispielsweise „Entwurf“ oder „Aktiv“. Aktive Regeln werden täglich verarbeitet, wobei die zu untersuchenden Classification-Daten in der Regel einen Monat zurückgehen. Die Regeln suchen automatisch nach neuen Werten und laden die Classifications hoch. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zuletzt geändert </p> </td> 
   <td colname="col2"> Gibt den Zeitpunkt an, zu dem der Regelsatz bearbeitet wurde. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Duplizieren </p> </td> 
   <td colname="col2"> Dupliziert (kopiert) einen Regelsatz, so dass Sie diesen Regelsatz auf eine andere Variable anwenden können (oder auch auf dieselbe Variable in einer anderen Report Suite). </td> 
  </tr> 
 </tbody> 
</table>

## Erstellen eines Klassifizierungsregelsatzes {#create-classification-rule-set}

<!-- 

t_classification_rule_set.xml

 -->

Benennen Sie den Classification-Regelsatz, wenden Sie die Variable an und legen Sie die Einstellungen für Überschreiben fest.

1. (Voraussetzung) Definieren Sie die Klassifizierungsstruktur unter **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]**.

   (Informationen zum Hinzufügen von Classifications finden Sie unter [Classifications](https://marketing.adobe.com/resources/help/en_US/reference/classifications.html) in der Admin Tools-Hilfe.)

   Variablen werden erst im Bereich [!UICONTROL Neuer Regelsatz] angezeigt, nachdem mindestens eine Classification für diese Variable definiert wurde.

   Sie können Klassifizierungen für eine Variable unter **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]** &gt; **[!UICONTROL Traffic]** &gt; **[!UICONTROL Traffic-Klassifizierungen]** (oder **[!UICONTROL Konversion]** &gt; **[!UICONTROL Konversionsklassifizierungen]**) erstellen. Wählen Sie dann die Variable aus und klicken Sie auf **[!UICONTROL Classification hinzufügen]**.

1. Um den Regelsatz zu erstellen, klicken Sie auf **[!UICONTROL Admin]** &gt; **[!UICONTROL Classification Rule Builder]** &gt; **[!UICONTROL Regelsatz hinzufügen]**.

   ![](assets/new_rule_set.png)

1. Geben Sie dem Regelsatz einen Namen und klicken Sie auf **[!UICONTROL Regelsatz erstellen]**.
1. Wählen Sie den zu bearbeitenden Regelsatz aus.

   ![](assets/classification_rules_page.png)

1. Klicken Sie auf **[!UICONTROL Report Suites und Variablen auswählen]**.

   Die Report Suite und die Variablenliste werden mit allen klassifizierten Variablen ausgefüllt, die in allen Report Suites Ihres angemeldeten Unternehmens verfügbar sind. Eine Variable in einer Report Suite kann nur zu jeweils einem einzigen Regelsatz gehören.

   Siehe *`Variable`* in den Definitionen für die Seite [Classification Rule Builder](/help/components/c-classifications2/crb/classification-rule-definitions.md) für weitere Informationen.
1. Geben Sie die zu verwendenden Report Suites und Variablen an und klicken Sie auf **[!UICONTROL Speichern]**.
1. Fahren Sie fort, indem Sie [Klassifizierungsregeln zum Regelsatz hinzufügen](/help/components/c-classifications2/crb/classification-rule-set.md).
