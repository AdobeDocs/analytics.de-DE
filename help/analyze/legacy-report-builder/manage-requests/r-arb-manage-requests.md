---
description: Erfahren Sie mehr über die Feldbeschreibungen für „Anfragen verwalten“ in Report Builder.
title: Verwalten von Anfragen in Report Builder
uuid: 01b21d0e-c870-4df8-95b9-f4aef1f4d16b
feature: Report Builder
role: User, Admin
exl-id: fd8c0145-4c7e-4f07-aa63-656a8a20724c
TQID: https://experienceleague.adobe.com/ZAVAW4NN9WCHCdj-ZPXDOflV4oC0-WPbClzkdlrf3JM
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2:
  - id: ac8a38fa-dec3-4581-8f64-178fde9f64e8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 563
ht-degree: 38%

---

# Anforderungen verwalten – Definitionen

{{legacy-arb}}

Zeigen Sie Details eines Anfragestatus an und verwenden Sie die Feldbeschreibungen, um Anfragen in Report Builder zu verwalten.

## Überblick {#section_75C288C945FA4781A4EDF806711A5660}

Der [!UICONTROL Anforderungs-Manager] bietet eine detaillierte Ansicht des Status aller Anforderungen, die Sie für alle Arbeitsblätter oder nur für ein Blatt der aktiven Arbeitsmappe erstellt haben. Sie können auch eine Anfrage hinzufügen, bearbeiten, aktualisieren und löschen. Diese Funktionen sind in der Regel mit dem [!UICONTROL Anforderungs-]) und [!UICONTROL Anforderungs-Manager] verknüpft, wenn Sie mit der rechten Maustaste auf eine verfügbare Zelle in der Excel-Tabelle klicken, die frühere Anforderungen enthält.

Der [!UICONTROL Anforderungs-Manager] wird angezeigt, wenn Sie in **[!UICONTROL Report Builder-Symbolleiste]** Verwalten![](assets/edit_request.gif) klicken.

>[!NOTE]
>
>Adobe Report Builder erzwingt Anfrageabhängigkeiten nur innerhalb desselben Arbeitsblatts, nicht über Arbeitsblätter hinweg. Durch die Beschränkung auf Abhängigkeiten in einem einzigen Arbeitsblatt wird die fristgerechte Ausführung gewährleistet.

## Definitionen {#section_FD29D8614DE74F32A0027FA130F40304}

<table id="table_0880204181074BDBBA37E3DF2972A672"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feld </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Alle Blätter </p> </td> 
   <td colname="col2"> <p>Die Anforderungen aus allen Arbeitsblättern der aktiven Arbeitsmappe werden angezeigt. Wenn Sie Anforderungen aus bestimmten Arbeitsblättern anzeigen möchten, müssen Sie diese Option deaktivieren. Wenn Sie diese Option deaktivieren, müssen Sie auf die Registerkarte für ein Arbeitsblatt am unteren Rand des Excel-Berichts klicken, um die zugehörigen Anforderungen im <span class="wintitle">Anforderungs-Manager</span> anzuzeigen. Die Beschriftung neben dem Kontrollkästchen gibt an, auf welches Blatt der Arbeitsmappe sich derzeit der Fokus befindet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Blatt </p> </td> 
   <td colname="col2"> <p>Zeigt den Namen der Blätter in der Arbeitsmappe an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Report Suite </p> </td> 
   <td colname="col2"> <p>Zeigt den Namen der Report Suite an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Datumsbereich </p> </td> 
   <td colname="col2"> <p>Zeigt den angegebenen Datumsbereich des Berichts an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Granularität </p> </td> 
   <td colname="col2"> <p>Gibt die Granularität der Anfrage an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Letzte Ausführung </p> </td> 
   <td colname="col2"> <p>Es wird das Datum angezeigt, an dem die Anforderung zuletzt von Report Builder verarbeitet wurde. In dieser Tabelle werden in der Spalte <span class="wintitle">Letzte Ausführung</span> auch gegebenenfalls erforderliche diagnostische Meldungen angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hinzufügen </p> </td> 
   <td colname="col2"> <p>Zeigt das Dialogfeld Anforderungs-Assistent an. Siehe <a href="/help/analyze/legacy-report-builder/data-requests/t-create-a-data-request.md"   > Erstellen einer Datenanfrage</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bearbeiten </p> </td> 
   <td colname="col2"> <p> (Oder mehrere bearbeiten) Bearbeitet eine ausgewählte Anfrage. Das System zeigt den <span class="wintitle">Anforderungs-Assistenten</span> an. Siehe <a href="/help/analyze/legacy-report-builder/manage-requests/t-edit-multiple-requests.md"   > Mehrere Anforderungen bearbeiten</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Löschen </p> </td> 
   <td colname="col2"> <p>Löscht Anfragen. Sie können mehrere Anforderungen gleichzeitig löschen. Sie können eine Anforderung in der Liste auch löschen, indem Sie die Anforderung auswählen und Löschen auf der Tastatur drücken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Alle auswählen </p> </td> 
   <td colname="col2"> <p>Wählen Sie alle Anforderungen aus. Die Anzahl der von Ihnen ausgewählten Anforderungen wird im <span class="wintitle">Anforderungs-Manager</span> am unteren Ende der Anforderungsliste angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Von Zelle </p> </td> 
   <td colname="col2"> <p>Ruft Daten für eine Anfrage aus dem Arbeitsblatt ab. Wenn eine Anfrage mit der aktuell ausgewählten Zelle im aktiven Arbeitsblatt verknüpft ist, wird die zugehörige Anfrage in der Liste ausgewählt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Aktualisieren </p> </td> 
   <td colname="col2"> <p>Aktualisiert eine einzelne Anfrage oder eine Auswahl von Anfragen (Siehe <a href="/help/analyze/legacy-report-builder/manage-requests/t-refresh-a-request.md"   > Aktualisieren einer Anfrage</a>.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Liste aktualisieren </p> </td> 
   <td colname="col2"> <p>Aktualisiert alle angezeigten Anforderungen. Die Aktualisierung aller Anforderungen in Ihren Bericht mit den Daten vom Server nimmt um so mehr Zeit in Anspruch, je komplexer die Anforderungen in dem Bericht sind. Bei sehr großen Berichten kann die Aktualisierung aller Anforderungen mehrere Minuten in Anspruch nehmen. Aus diesem Grund könnte es von Vorteil sein, dringende Anforderungen möglichst einzeln zu aktualisieren und <span class="wintitle">Alle aktualisieren</span> erst zu einem späteren Zeitpunkt zu wählen, wenn keine Dringlichkeit geboten ist. </p> <p> <p>Hinweis: Es wird empfohlen, dass Sie bei der Aktualisierung einer Arbeitsmappe mit mehreren Anforderungen die Ergebnisse öfter im <span class="wintitle">Anforderungs-Manager</span> überprüfen. Wenn eine Anfrage fehlschlägt, hilft Ihnen die Fehlermeldung in der Spalte Diagnose , die Ursache des Fehlers zu identifizieren. Während in den meisten Fällen eine Fehlermeldung angezeigt wird, wenn eine Anfrage fehlschlägt, beachten Sie, dass gelegentlich keine Fehlermeldung generiert wird. Sie werden möglicherweise feststellen, dass bei einer Aktualisierung die Daten in einer Zelle, die einen Verweis enthält, nicht aktualisiert werden oder dass bei einer Aktualisierung die Daten aus der Zelle entfernt werden. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>
