---
title: Erstellen von Hyperlinks in einer Freiformtabelle in Analysis Workspace
description: Erfahren Sie, wie Sie Hyperlinks für Dimensionselemente in einer Freiformtabelle in Analysis Workspace erstellen
feature: Freeform Tables
role: User, Admin
exl-id: df846a73-e3e3-4376-844e-48153a20e5d6
source-git-commit: d7a6867796f97f8a14cd8a3cfad115923b329c7c
workflow-type: tm+mt
source-wordcount: '1739'
ht-degree: 1%

---

# Erstellen von Hyperlinks für Dimensionen in einer Freiformtabelle

Sie können Hyperlinks für Dimensionselemente erstellen, um sie in einer Freiformtabelle in Analysis Workspace anklickbar zu machen.

Diese Funktion ist besonders beim Erstellen von Hyperlinks für die folgenden Arten von Dimensionselementen nützlich:

* Seitenelemente mit URL-Werten, mit denen Sie eine Dimension verknüpfen möchten (z. B. eine Seiten-URL-Dimension)

* Dimension-Elemente, die Aufschlüsselungen mit URL-Werten enthalten, mit denen Sie eine Verknüpfung herstellen möchten (z. B. eine Dimension Seitenname mit einer Aufschlüsselung einer Dimension Seiten-URL )

* Elemente oder Aufschlüsselungen einer Dimension, deren Werte Teil einer URL sind, mit der Sie eine Verknüpfung herstellen möchten (z. B. eine Seitennamendimension, die Teil einer URL ist)


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Hyperlinks für Dimension](https://video.tv.adobe.com/v/3430411?quality=12&learn=on){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]





## Erstellen von Hyperlinks für ein oder mehrere Dimensionselemente

Beachten Sie beim Erstellen von Hyperlinks für Dimensionselemente Folgendes:

* Die von Ihnen erstellten Hyperlinks werden in der Freiformtabelle im Analysis Workspace-Projekt gespeichert. Hyperlinks bleiben nicht erhalten, wenn dieselbe Dimension oder Dimensionselemente in einer anderen Tabelle oder in einem anderen Projekt verwendet werden.

* Wenn Sie die Datenansicht der Freiformtabelle ändern, sind alle Hyperlinks, die für Dimensionen oder Dimensionselemente in der Tabelle erstellt wurden, weiterhin verfügbar, sofern die Dimension in der Datenansicht vorhanden ist.

* URLs werden beim Erstellen des Hyperlinks nicht auf ihre Gültigkeit überprüft.

  Wenn Sie einen Hyperlink mit einer ungültigen URL erstellen oder einen Hyperlink erstellen, der auf ein Dimensionselement ohne URL-Wert verweist (indem Sie entweder direkt auf das Dimensionselement verweisen oder die Variablen `$value` oder `$breakdown` verwenden), wird Benutzern, die auf den Hyperlink klicken, eine Fehlermeldung angezeigt, die besagt, dass die URL ungültig ist.

* Hyperlinks, die für ein einzelnes Dimensionselement erstellt werden, überschreiben Hyperlinks, die für die Dimension erstellt werden.

* Hyperlinks funktionieren nicht in [heruntergeladenen PDF-](/help/analyze/analysis-workspace/curate-share/download-send.md).

So erstellen Sie Hyperlinks für ein oder mehrere Dimensionselemente:

1. Führen Sie in einer Freiformtabelle in Analysis Workspace einen der folgenden Schritte aus:

   * **Erstellen eines Hyperlinks für ein einzelnes Dimensionselement:** Sie mit der rechten Maustaste auf das Dimensionselement in der Tabelle, für die Sie den Hyperlink erstellen möchten, und wählen Sie dann [!UICONTROL **Hyperlink erstellen**].

     ![Erstellen eines Hyperlinks für ein einzelnes Dimensionselement](assets/hyperlink-single-add.png)

     Das [!UICONTROL **Hyperlink erstellen**] wird angezeigt. Der Name des Dimensionselements, für das Sie einen Hyperlink erstellen, wird im Dialogfeld angezeigt.

     ![Erstellen eines Hyperlinks für ein Dialogfeld mit einem Element](assets/hyperlink-dialog-single.png)

   * **Erstellen von Hyperlinks für alle Dimensionselemente in einer Dimensionsspalte:** Klicken Sie mit der rechten Maustaste auf den Dimensionsnamen in der Spaltenüberschrift der Dimension und wählen Sie [!UICONTROL **Erstellen von Hyperlinks für alle Dimensionselemente**].

     ![Erstellen eines Hyperlinks für eine Dimension](assets/hyperlink-multiple-add.png)

     Das [!UICONTROL **Erstellen von Hyperlinks für alle Dimensionselemente**] wird angezeigt. Der Name der Dimension, für die Sie Hyperlinks erstellen, wird im Dialogfeld angezeigt.

     ![Dialogfeld „Hyperlinks erstellen“](assets/hyperlink-dialog-multiple.png)

1. Wählen Sie aus den folgenden Optionen:

   * [!UICONTROL **Wert des Dimensionselements als URL verwenden**]: Wählen Sie diese Option für Dimensionselemente mit URL-Werten, wie z. B. die Dimension Seiten-URL .

     Wenn Sie beispielsweise eine Seiten-URL -Dimension verwenden, bei der der Wert jedes Dimensionselements eine URL ist, wird durch die Auswahl dieser Option ein Hyperlink zur URL erstellt.

   * [!UICONTROL **Erstellen einer benutzerdefinierten URL**]: Geben Sie entweder eine statische oder eine dynamische benutzerdefinierte URL an. Wählen Sie diese Option aus, um Hyperlinks für Dimensionselemente zu erstellen, die keine URL-Werte haben.

     Wenn Sie beispielsweise eine Dimension Seitenname verwenden, bei der der Wert jedes Dimensionselements der Name einer Seite (und keine vollständige URL) ist, können Sie mit dieser Option einen Hyperlink angeben, der als Link für das Dimensionselement verwendet werden soll.

     Wenn Sie dynamische URLs für mehrere Dimensionselemente erstellen möchten, können Sie die Variablen `$value` und `$breakdown` in Ihrer benutzerdefinierten URL verwenden. Weitere Informationen finden Sie in der Tabelle unten.

     Um eine benutzerdefinierte URL zu erstellen, geben Sie die folgenden Informationen an:

     | Feld | Beschreibung |
     |---------|----------|
     | [!UICONTROL **Benutzerdefinierte URL**] | Geben Sie eine benutzerdefinierte URL an, die Sie für den Hyperlink verwenden möchten. URLs müssen als vollständig qualifizierte URLs eingegeben werden. Beispiel: https://www.example.com<p>Die von Ihnen erstellte benutzerdefinierte URL kann statisch oder dynamisch sein:</p> <ul><li>**Statische URLs:** Wenn Sie einen Hyperlink für ein einzelnes Dimensionselement erstellen, kann eine statische URL ausreichen. <p>Betrachten Sie das folgende Beispiel:Wenn Sie beispielsweise über ein Dimensionselement „Seitenname“ verfügen, können Sie eine statische URL erstellen, die Benutzer mit der spezifischen Web-Seite verknüpft, die Sie mit dem Seitennamen verknüpfen möchten.</p><p>Angenommen, Sie möchten Hyperlinks für eine Liste von Dimensionselementen erstellen, von denen jedes mit der entsprechenden Definition in der Dokumentation innerhalb einer internen Wiki-Seite verknüpft ist.</p><p>Sie können dies erreichen, indem Sie für jedes Dimensionselement eine statische URL erstellen. z. B.:</p><p>https://wiki.internal.company_name/page_name#item_definition</p></li><li>**Dynamische URLs:** Wenn Sie einen Hyperlink für mehrere Dimensionselemente oder für alle Dimensionselemente in einer Dimensionsspalte erstellen, ist eine dynamische URL wahrscheinlich praktischer. <p>Um benutzerdefinierte URLs dynamisch zu gestalten, schließen Sie Variablen in die URL ein, die es ermöglichen, die URL basierend auf dem Wert der Dimension selbst oder dem Wert der Aufschlüsselungsdimension dynamisch zu ändern.</p><p>Bei Verwendung von Variablen werden alle Dimensionselemente, die Zeichen enthalten, die in URLs ungültig sind (z. B. Leerzeichen), URL-kodiert.</p><p>Die folgenden Variablen sind verfügbar: (**Hinweis**: Obwohl Sie diese Variablen in derselben URL verwenden können, ist es wahrscheinlich üblicher, sie separat zu verwenden.)</p> <ul><li>**`$value`:** Ermöglicht Ihnen, den Wert des Dimensionselements in die von Ihnen angegebene URL einzufügen. <p>Betrachten Sie das folgende Szenario als Beispiel:</p><p>Angenommen, Sie möchten Hyperlinks für alle Dimensionselemente des Seitennamens in einer Freiformtabelle erstellen, wobei der Wert jedes Dimensionselements Teil der URL einer Web-Seite ist. In diesem Fall können Sie eine einzelne benutzerdefinierte URL erstellen, die sich für jedes Dimensionselement dynamisch anpasst. </p><p>Sie können dies erreichen, indem Sie die Variable `$value` am Ende der von Ihnen angegebenen benutzerdefinierten URL hinzufügen. z. B.:</p> <p>https://company-name.com/browse/product#$value</p><p>Wenn diese benutzerdefinierte URL auf Dimensionselemente mit Seitennamen angewendet wird, deren Werte „ProductY“ und „ProductZ“ sind, sehen die generierten Hyperlinks wie folgt aus: </p><p>https://company-name.com/browse/product#ProductY</p><p>und</p><p> https://company-name.com/browse/product#ProductZ </p><p>![Verwenden von Werten in Hyperlinks](assets/table-hyperlinks-vaule.png)</p><p>**Tipp**: Wenn Sie dem Feld „Benutzerdefinierte URL“ nur die Variable &quot;`$value`&quot; hinzufügen würden, wäre dies dasselbe, als würden Sie die Option [!UICONTROL **Wert des Dimensionselements verwenden**] beim Erstellen der URL auswählen.</p></li><li>**`$breakdown`:** Ermöglicht Ihnen, den Wert des Aufschlüsselungs-Dimensionselements in die von Ihnen angegebene URL einzufügen. Auf diese Weise können Sie eine Dimension mit einem benutzerfreundlichen Namen in Ihrem Bericht verwenden (z. B. eine Dimension „Produktname„), während Sie den Hyperlink auf der Grundlage einer Aufschlüsselungsdimension erstellen, die möglicherweise weniger benutzerfreundlich ist (z. B. eine Produkt-ID oder Seiten-URL-Dimension).<p>Beim Referenzieren einer Aufschlüsselungsdimension ist es am häufigsten, nur ein Aufschlüsselungselement für ein bestimmtes Dimensionselement zu haben. Wenn für ein bestimmtes Dimensionselement mehrere Aufschlüsselungselemente vorhanden sind, wird der Wert des ersten Aufschlüsselungselements in der URL verwendet. Wenn keine Aufschlüsselungselemente aufgelistet sind, ist die URL ungültig. Auf die Aufschlüsselungselemente wird die gleiche Sortierreihenfolge angewendet wie auf die Tabelle.</p><p>Die Aufschlüsselungsdimension geben Sie im Feld [!UICONTROL **Aufschlüsselungsdimension**] unten an.</p> <p>Betrachten Sie das unten beschriebene Beispielszenario für das Feld [!UICONTROL **Aufschlüsselungsdimension**].</p></li></ul> |
     | [!UICONTROL **Aufschlüsselungsdimension (optional)**] | Geben Sie den Namen der Aufschlüsselungsdimension ein, die Sie verwenden möchten, und wählen Sie sie dann aus der Dropdown-Liste aus. <p>Wenn Sie eine Aufschlüsselungsdimension in diesem Feld auswählen, müssen Sie sie mithilfe der `$breakdown` in der URL referenzieren, die Sie im Feld [!UICONTROL **Benutzerdefinierte URL**] angeben.</p><p>Betrachten Sie das folgende Szenario als Beispiel:</p><p>Angenommen, Sie möchten Hyperlinks für alle Dimensionselemente des Produktnamens in einer Freiformtabelle erstellen. Jedes Dimensionselement Produktname enthält eine Aufschlüsselung einer Produkt-ID-Dimension.</p></p>In diesem Fall können Sie Hyperlinks für jede Dimension „Produktname“ erstellen, die Benutzer mithilfe des Werts der Dimension „Produkt-ID-Aufschlüsselung“ zur Produktseite weiterleitet. </p><p>Sie können dies erreichen, indem Sie die Variable `$breakdown` am Ende der benutzerdefinierten URL hinzufügen, die Sie im Feld [!UICONTROL **Benutzerdefinierte URL**] angeben. z. B.:</p><p>https://company-name.com/browse/product/$breakdown</p><p>Wenn diese benutzerdefinierte URL auf die Dimensionselemente Ihres Produktnamens angewendet wird, die Aufschlüsselungs-Dimensionselemente haben, deren Werte „ProductY“ und „ProductZ“ sind, würden die generierten Hyperlinks in etwa wie folgt aussehen:</p><p>https://company-name.com/browse/product/ProductY</p><p>und</p><p>https://company-name.com/browse/product/ProductZ</p><p>Wählen Sie dann die Dimension Produkt-ID im Feld [!UICONTROL **Aufschlüsselungsdimension**] aus </p><p>![Aufschlüsselungen in Hyperlinks verwenden](assets/table-hyperlinks-breakdown.png)</p> |

1. Wählen Sie [!UICONTROL **Erstellen**] aus.

   Benutzer, die die Freiformtabelle anzeigen, sehen die mit Hyperlinks versehenen Dimensionselemente. Beim Klicken auf ein Dimensionselement werden die Benutzer in einer separaten Browser-Registerkarte zu den mit Hyperlinks versehenen Seiten weitergeleitet.

   <!-- add screenshot of a table with hyperlinks.-->

1. [Speichern Sie das Projekt](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md), um Ihre Änderungen zu speichern.

## Hyperlinks bearbeiten

Sie können Hyperlinks bearbeiten, die für Dimensionen oder Dimensionselemente in einer Freiformtabelle erstellt wurden.

1. Führen Sie in einer Freiformtabelle in Analysis Workspace einen der folgenden Schritte aus:

   * **Hyperlink für ein einzelnes Dimensionselement bearbeiten** Klicken Sie mit der rechten Maustaste auf das Dimensionselement in der Tabelle, in der Sie den Hyperlink bearbeiten möchten.

     ![Hyperlink für ein einzelnes Dimensionselement bearbeiten](assets/hyperlink-single-edit.png)

   * **Hyperlinks für alle Dimensionselemente in einer Dimensionsspalte bearbeiten** Klicken Sie mit der rechten Maustaste auf den Dimensionsnamen in der Spaltenüberschrift der Dimension.

     ![Hyperlink für eine Dimension bearbeiten](assets/hyperlink-dimension-edit.png)

1. Wählen [!UICONTROL **Hyperlink bearbeiten**] aus dem Kontextmenü aus.

   Das [!UICONTROL **„Hyperlinks für Dimensionselemente bearbeiten**] wird angezeigt.

1. Weitere Informationen zu den Konfigurationsoptionen für die Bearbeitung des Hyperlinks finden Sie in Schritt 3 im Abschnitt [Erstellen von Hyperlinks für ein oder mehrere Dimensionselemente](#create-hyperlinks-for-one-or-more-dimension-items) und wählen Sie dann [!UICONTROL **Anwenden**] aus, wenn Sie mit Ihren Aktualisierungen fertig sind.

1. [Speichern Sie das Projekt](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md), um Ihre Änderungen zu speichern.

## Entfernen von Hyperlinks

Sie können Hyperlinks entfernen, die für Dimensionselemente in einer Freiformtabelle erstellt wurden.

>[!NOTE]
>
>Wenn Sie in einer Freiformtabelle eine Dimension löschen, die Hyperlinks enthält, bleiben die Hyperlinks nicht erhalten, wenn Sie dieselbe Dimension wieder zur Freiformtabelle hinzufügen.

So entfernen Sie Hyperlinks aus Dimensionselementen:

1. Führen Sie in einer Freiformtabelle in Analysis Workspace einen der folgenden Schritte aus:

   * **Entfernen eines Hyperlinks aus einem einzelnen Dimensionselement:** Klicken Sie mit der rechten Maustaste auf das Dimensionselement in der Tabelle, in der Sie den Hyperlink entfernen möchten.

     ![Entfernen eines Hyperlinks aus einem einzelnen Dimensionselement](assets/hyperlink-single-remove.png)

   * **Entfernen Sie Hyperlinks aus allen Dimensionselementen in einer Dimensionsspalte:** Klicken Sie mit der rechten Maustaste auf den Dimensionsnamen in der Spaltenüberschrift der Dimension.

     ![Entfernen eines Hyperlinks aus einer Dimension](assets/hyperlink-dimension-remove.png)

1. Wählen [!UICONTROL **Hyperlink entfernen**] aus dem Kontextmenü aus.

   Der Hyperlink wird aus dem einzelnen Dimensionselement (wenn Sie ein einzelnes Dimensionselement ausgewählt haben) oder aus allen Dimensionselementen (wenn Sie den Dimensionsnamen in der Spaltenüberschrift der Dimension ausgewählt haben) entfernt.

1. [Speichern Sie das Projekt](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md), um Ihre Änderungen zu speichern.
