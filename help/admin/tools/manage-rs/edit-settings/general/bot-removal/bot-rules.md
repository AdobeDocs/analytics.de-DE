---
description: Mit „Bot-Regeln“ können Sie Traffic aus Ihrer Report Suite entfernen, der von bekannten Spiders und Bots verursacht wird. Durch das Ausblenden des Bot-Traffics kann die Benutzeraktivität auf Ihrer Website genauer gemessen werden.
title: Verstehen und Konfigurieren von Bot-Regeln
feature: Bot Removal
role: Admin
exl-id: 1c0009f6-2746-4ef1-8dcb-e2693617e91e
source-git-commit: 8b1e25b9633b6db3e49da079f7014e6b7b595474
workflow-type: tm+mt
source-wordcount: '1669'
ht-degree: 40%

---

# Verstehen und Konfigurieren von Bot-Regeln

Mit Bot-Regeln können Sie Traffic aus Ihrer Report Suite entfernen, der von bekannten Spiders und Bots generiert wird. Durch das Ausblenden des Bot-Traffics kann die Benutzeraktivität auf Ihrer Website genauer gemessen werden.

Nach der Definition von Bot-Regeln wird aller eingehender Traffic mit den definierten Regeln abgeglichen. Traffic, der mit einer dieser Regeln übereinstimmt, wird nicht in der Report Suite erfasst und ist nicht in Traffic-Metriken enthalten.

Durch das Entfernen von Bot-Traffic wird in der Regel das Traffic-Volumen und die Konversionsmetriken reduziert. Viele Kunden stellen fest, dass die Entfernung von Bot-Traffic zu höheren Konversionsraten und Steigerungen bei anderen Nutzungsmetriken führt.

Traffic-Daten von Bots werden in einem separaten Repository gespeichert, um sie in den Berichten „Bots“ und „Bot-Seiten“ anzuzeigen.

>[!NOTE]
>
>Adobe Experience Platform Edge Network bietet einen [Bot-Erkennungs-Service](https://experienceleague.adobe.com/docs/experience-platform/datastreams/bot-detection.html?lang=de) der Treffer kennzeichnet, die als von Bots stammend identifiziert wurden. Der in Adobe Analytics verwendete Bot-Erkennungsprozess ist separat und verweist nicht auf den Bot-Score, der in Daten enthalten ist, die über die Edge Network eingehen. Die beiden Systeme verwenden jedoch dieselbe IAB-Bot-Liste.

## Bot-Regeln aktualisieren oder hochladen

>[!IMPORTANT]
>
>Bevor Sie Bot-Traffic entfernen, kommunizieren Sie mit den Stakeholdern, um sicherzustellen, dass sie infolge dieser Änderung die erforderlichen Anpassungen an wichtigen Leistungsindikatoren vornehmen können. Wenn möglich, empfehlen wir, zunächst den Bot-Traffic aus einer kleinen Report Suite zu entfernen, um die potenziellen Auswirkungen abschätzen zu können.


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Konfigurieren von Bot-Regeln](https://experienceleague.adobe.com/de/docs/analytics-learn/tutorials/administration/manage-report-suites/configure-bot-rules-in-analytics){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]


So aktualisieren oder laden Sie Bot-Regeln hoch:

1. Navigieren Sie **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.

1. Wählen Sie die Report Suite aus, in der Sie Bot-Regeln aktualisieren möchten, und wählen Sie dann **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Bot-Regeln]**.

1. Verwenden Sie eine der folgenden Optionen, um Bot-Regeln für die Report Suite zu aktualisieren oder hochzuladen:

   * Wählen Sie [!UICONTROL **IAB-Bot-Filterregeln aktivieren**] aus, um Bots aus der IAB-Liste (International Advertising Bureau) „International Spiders &amp; Bots List“ zu entfernen, um Bot-Traffic zu entfernen.

     Es wird empfohlen, mindestens diese Option auszuwählen.

     Weitere Informationen finden Sie im folgenden Abschnitt &quot;[&#x200B; IAB-Bot-Regeln](#standard-iab-bot-rules).

   * Wählen Sie [!UICONTROL **Regel hinzufügen**] aus, um benutzerdefinierte Bot-Regeln basierend auf Benutzeragenten, IP-Adressen oder IP-Bereichen zu definieren und hinzuzufügen.

     Weitere Informationen finden Sie im folgenden Abschnitt [Benutzerdefinierte Bot-Regeln](#custom-bot-rules).

   * Klicken Sie neben dem Bereich [!UICONTROL **CSV-Bot-Datei zum Importieren auswählen**] auf [!UICONTROL **Datei auswählen**] und wählen Sie dann die CSV-Datei aus, die die Bot-Regeln definiert.

     Weitere Informationen finden Sie im folgenden Abschnitt &quot;[&#x200B; von Bot-Regeln](#upload-bot-rules).

1. Wählen Sie [!UICONTROL **Speichern**] aus.

## Standard-IAB-Bot-Regeln

Standard-IAB-Bot-Regeln können aktiviert werden, indem Sie das Kontrollkästchen [!UICONTROL IAB Bot-Filterungsregeln aktivieren] aktivieren. Diese Auswahl entfernt Bots in der Liste „International Spiders &amp; Bots List“ von IAB (International Advertising Bureau), um Bot-Traffic zu entfernen. Adobe aktualisiert diese Liste von IAB monatlich.

![](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/assets/bot-iab-checkbox.png)

Adobe kann die detaillierte IAB-Bot-Liste nicht an Kunden weitergeben, aber Sie können den Bericht „Bots“ verwenden, um eine Liste der Bots anzuzeigen, die auf Ihre Website zugegriffen haben. Um einen Bot an die IAB-Liste zu senden, gehen Sie zu [IAB](https://www.iab.com).

Informationen zum Aktivieren von standardmäßigen IAB-Bot-Regeln in einer Report Suite finden Sie unter [Aktualisieren oder Hochladen von Bot-Regeln](#update-or-upload-bot-rules).

## Benutzerdefinierte Bot-Regeln

>[!NOTE]
>
>: In der Benutzeroberfläche können 500 Regeln manuell definiert werden. Wenn diese Grenze erreicht wurde, müssen Regeln über die Optionen „Datei importieren“ und „Bot-Regeln exportieren“ stapelweise verwaltet werden.

Mit benutzerdefinierten Bot-Regeln können Sie Traffic-Bedingungen filtern, die Sie definieren. Informationen dazu, wie Sie benutzerdefinierte Bot-Regeln in einer Report Suite aktivieren, finden Sie unter [Aktualisieren oder Hochladen von Bot-Regeln](#update-or-upload-bot-rules).

Benutzerdefinierte Bot-Regeln werden mithilfe der folgenden Bedingungstypen definiert:

* Benutzeragent
* IP-Adresse
* IP-Bereich

Für eine einzelne Regel können mehrere Bedingungen definiert werden. Mehrere Bedingungen werden mit „oder“ abgeglichen. Wenn Sie beispielsweise einen Wert für Benutzeragent und IP-Adresse angeben, wird der Traffic als Traffic betrachtet, wenn eine der Bedingungen erfüllt ist.

### Benutzeragent

Eine Benutzeragent-Bedingung prüft den Benutzeragentenwert, um zu sehen, ob dieser mit der angegebenen Zeichenfolge **[!UICONTROL beginnt]** oder diese **[!UICONTROL enthält]**. Wenn **[!UICONTROL enthält]** ausgewählt wurde, wird die Unter-Zeichenfolge zugewiesen, wenn sie an einer beliebigen Stelle im Benutzeragenten auftaucht.

Optionale Werte können in die Liste **[!UICONTROL enthält nicht]** aufgenommen werden, um Werte zu definieren, die der Benutzeragent für eine erfolgreiche Übereinstimmung nicht enthalten darf. Mehrere Werte können angegeben werden, indem ein Wert pro Zeile eingeschlossen wird. Erfüllt der Benutzeragent die in der Übereinstimmungszeichenfolge angegebenen Kriterien, enthält aber auch eine Zeichenfolge in der Liste Enthält nicht , wird er nicht als Übereinstimmung betrachtet.

Das Feld **[!UICONTROL enthält]** ist auf 100 Zeichen begrenzt. Die Liste Enthält nicht ist auf 255 Zeichen minus einem Trennzeichen für jede neue Zeile beschränkt. (Dies entspricht der Anzahl der Zeichenfolgen - 1. Wenn Sie 4 angeben *enthält nicht* Zeichenfolgen, sind 3 Trennzeichen erforderlich.) Bei allen Zeichenfolgen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

### IP-Adresse (inklusive Wildcard-Übereinstimmungen)

Weist eine oder mehrere IP-Adressen im selben Block mithilfe von Wildcards (&#42;) zu. Geben Sie die numerischen Werte der IP-Adresse an, für die Sie eine Übereinstimmung suchen. Ersetzen Sie die Werte, für die Sie eine Wildcard-Übereinstimmung suchen, durch eine Wildcard (&#42;). Die folgende Liste enthält Beispiele der IP-Adressen-Übereinstimmungszeichenfolge:

```
10.10.10.1
10.10.10.*
```

### IP-Adressbereich

Geben Sie die Start- und Endbereiche der zuzuweisenden IP-Adressen an. Ersetzen Sie die Werte, für die Sie eine Wildcard-Übereinstimmung suchen, durch eine Wildcard (&#42;).

### Definieren einer benutzerdefinierten Bot-Regel

1. Wechseln Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin]**, wählen Sie eine oder mehrere Report Suites aus und klicken Sie auf **[!UICONTROL Allgemein]** > **[!UICONTROL Bot-Regeln]**.
1. Klicken Sie auf **[!UICONTROL Regel hinzufügen]** und definieren Sie eine oder mehrere Übereinstimmungsbedingungen.
1. Klicken Sie auf **[!UICONTROL Speichern]**. Die Änderung sollte binnen 30 Minuten in Kraft treten.

## Hochladen von Bot-Regeln

Um Bot-Regeln stapelweise zu importieren, können Sie eine CSV-Datei hochladen, die die Regeln definiert.

1. Informationen zum Starten des Uploads von Bot-Regeln in eine Report Suite finden Sie unter [Aktualisieren oder Hochladen von Bot-Regeln](#update-or-upload-bot-rules).

1. Erstellen Sie eine CSV-Datei mit den folgenden Spalten in Zeile 1 des Arbeitsblatts und in der angegebenen Reihenfolge:

   | Spalte 1, Zeile 1 | Spalte 2, Zeile 1 | Spalte 3, Zeile 1 | Spalte 4, Zeile 1 | Spalte 5, Zeile 1 | Spalte 6, Zeile 1 |
   |--- |--- |---|---|---|---|
   | Bot-Name | IP-Beginn | IP-Ende | Regel<br>(enthält oder beginnt mit)</br> | Benutzeragenten-Include | Benutzeragent ausschließen<br>(Limit von 255 Zeichen)</br> |

   Sie können drei Arten von Bot-Regeln definieren:

   * Benutzeragent enthält oder beginnt mit
   * Einzelne IP-Adresse oder Wildcard-Übereinstimmung
   * IP-Bereichsübereinstimmung

   Jede Zeile in der Importdatei kann nur eine der folgenden Bot-Definitionen enthalten:

   >[!NOTE]
   >
   >   Um eine Übereinstimmung für einen Bot mithilfe einer OR-Kombination aus Regeln zu finden (z. B. Benutzeragent ODER IP-Adresse), geben Sie einen identischen Namen für alle Regeln an, die Sie in dem Bot-Namensfeld kombinieren möchten. AND-Übereinstimmungen werden nicht unterstützt.


   * **Benutzeragent enthält oder beginnt mit**: Geben Sie eine einzelne Benutzeragenten-Zeichenfolge an, die in der Spalte „Agent einschließen“ abgeglichen werden soll. Geben Sie den Typ der Übereinstimmung an, die ausgeführt werden soll, indem Sie *enthält* oder *beginnt mit* im Feld Agentenübereinstimmungsregel platzieren. Ein optionaler Wert kann in die Spalte „Agent ausschließlich“ aufgenommen werden, der eine oder mehrere längsstrichgetrennte (`|`) Zeichenketten definiert, die der Agent nicht enthalten darf. Bei Zeichenfolgenübereinstimmungen wird nicht zwischen Groß- und Kleinschreibung unterschieden. Die Spalten IP-Start und IP-Ende müssen leer sein.

   * **Einzelne IP-Adresse oder Wildcard-Übereinstimmung**: Um eine Übereinstimmung mit einer einzelnen IP-Adresse (`10.10.10.1`) oder einer Platzhalter-IP-Adresse (`10.10.*.*`) herzustellen, platzieren Sie denselben Wert in den Spalten „IP-Start“ und „IP-Ende“. „Übereinstimmungsregel“, „Agent einschließlich“ und „Agent ausschließlich“ müssen leer sein.

   * **IP-Bereichsübereinstimmung**: Definieren Sie einen Bereich von IP-Adressen mithilfe der Spalten IP-Start und IP-Ende . Sie können Platzhalter nutzen, um Übereinstimmungen für IP-Bereiche zu finden, z. B. `10.10.10.*` bis `10.10.20.*`. „Übereinstimmungsregel“, „Agent einschließlich“ und „Agent ausschließlich“ müssen leer sein.

1. Klicken Sie auf der Seite „Bot-Regeln“ in Report Suite Manager neben dem Bereich [!UICONTROL **CSV-Bot-Datei zum Importieren auswählen**] auf [!UICONTROL **Datei auswählen**] und wählen Sie dann die CSV-Datei aus, die die zu importierenden Bot-Regeln definiert.

1. (Optional) Aktivieren Sie das Kontrollkästchen **[!UICONTROL Vorhandene Regeln überschreiben]**, um alle vorhandenen Regeln zu löschen und sie durch die in der Upload-Datei definierten Regeln zu ersetzen.

1. Wählen Sie [!UICONTROL **Datei importieren**].

1. Überprüfen Sie [!UICONTROL **Bereich &quot;**]&quot; die importierten Regeln.

1. Wählen Sie [!UICONTROL **Speichern**] aus.

## Bot-Regeln exportieren

So exportieren Sie alle in der Benutzeroberfläche definierten Regeln im CSV-Format:

1. Navigieren Sie **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.

1. Wählen Sie die Report Suite aus, die die zu exportierenden Bot-Regeln enthält, und wählen Sie dann **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Bot-Regeln]**.

1. Wählen **[!UICONTROL Exportieren von Bot]** Regeln und speichern Sie dann die CSV-Datei in Ihrem Dateisystem.

## Auswirkung von Bot-Regeln auf die Datenerfassung {#section_F01A3130E7A04A9993371CF26F6586F2}

Bot-Regeln gelten für alle Analysedaten. Mithilfe von Bot-Regeln entfernte Daten sind nur in den Berichten „Bots“ und „Bot-Seiten“ sichtbar.

VISTA-Regeln werden nach Bot-Regeln angewendet. Weitere Informationen finden Sie im Technote-Benutzerhandbuch unter [Verarbeitungsreihenfolge](/help/technotes/processing-order.md).

**Verarbeitung von Besuchen mit hoher Trefferrate:** Wenn bei einem Besuch mehr als 100 Treffer auftreten, bestimmt das Reporting, ob die Besuchszeit in Sekunden kleiner oder gleich der Anzahl der Treffer im Besuch ist. In diesem Fall beginnt das Reporting aufgrund der Kosten für die Verarbeitung langer, intensiver Besuche mit einem neuen Besuch. Besuche mit hohen Treffern werden in der Regel durch Bot-Angriffe verursacht und gelten nicht als normales Browsen durch Besucher.

>[!NOTE]
>
>Treffer, die als *`bots`* markiert sind, werden als [Server-Aufrufe](/help/admin/tools/server-call-usage/overage-overview.md) in Rechnung gestellt.

## Auswirkung der IP-Verschleierung auf die Bot-Filterung {#section_92E60B95BE8940D983F28C79E0CD6B12}

Die IAB-Bot-Liste basiert ausschließlich auf dem Benutzeragenten. Daher ist das Filtern auf der Grundlage dieser Liste von den Einstellungen für die IP-Verschleierung nicht betroffen. Bei der Nicht-IAB-Bot-Filterung (benutzerdefinierte Regeln) kann IP Teil der Filterkriterien sein. Wenn Bots über IP gefiltert werden, erfolgt die Bot-Filterung, nachdem das letzte Oktett entfernt wurde, sofern diese Einstellung aktiviert ist, aber vor den anderen IP-Verschleierungsoptionen, z. B. vor dem Löschen der gesamten IP oder dem Ersetzen durch eine eindeutige ID.

Wenn die IP-Verschleierung aktiviert ist, erfolgt der IP-Ausschluss, bevor die IP-Adresse verschleiert wird, sodass Kunden nichts ändern müssen, wenn sie die IP-Verschleierung aktivieren.

Wenn das letzte Oktett entfernt wird, geschieht dies vor der IP-Filterung. Dabei wird das letzte Oktett mit „0“ ersetzt und die Regeln für den IP-Ausschluss sollten aktualisiert werden, sodass sie IP-Adressen mit einer Null am Ende berücksichtigen. Übereinstimmende &#42; sollten 0 entsprechen.
