---
title: Regeln für Klassifizierungssätze
description: Erfahren Sie, wie Sie Klassifizierungssätze-Regeln verwenden, um Regeln für Klassifizierungsdaten zu definieren.
feature: Classifications
source-git-commit: 3cbbcdb89009b9c53892c939ddc5c06a732b2267
workflow-type: tm+mt
source-wordcount: '1682'
ht-degree: 13%

---


# Regeln für Klassifizierungssätze

Sie verwenden Regeln, um automatische Klassifizierungen in Szenarien zu unterstützen, in denen sich Ihre Schlüsseldimension ständig ändert. Die Aktualisierung von Klassifizierungen durch Upload oder Automatisierung wird zu einem umständlichen Prozess oder verzögert die korrekte Klassifizierung für neue Dimensionswerte. Beispielsweise interne Kampagnen, Trackingcodes oder Produkt-SKUs. Die Dimension muss Werte enthalten, mit denen Sie eine oder mehrere Regeln anwenden können, damit Sie Klassifizierungsdaten aus den Werten ableiten können.

Sie definieren Regeln im Kontext eines Klassifizierungssatzes. Dieser Kontext bedeutet, dass Regeln (wenn aktiviert) auf alle Report Suite- und Schlüssel-Dimensionskombinationen angewendet werden, die für den Klassifizierungssatz abonniert wurden. Diese Implementierung unterscheidet sich etwas von der Funktionsweise des alten Classification Rule Builders. Definieren Sie im Classification Rule Builder eine oder mehrere Regeln als Teil eines Regelsatzes separat und verknüpfen Sie dann den Regelsatz mit einer oder mehreren Report Suites. In der neuen Benutzeroberfläche werden die Regeln innerhalb des Klassifizierungssatzes auch als Regelsatz bezeichnet. Die Regelsätze werden jedoch in derselben Benutzeroberfläche definiert, in der Sie andere Klassifizierungssatzattribute konfigurieren.


So definieren Sie einen Regelsatz für einen Klassifizierungssatz:

1. Wählen Sie **[!UICONTROL Komponenten]** in der oberen Menüleiste von Adobe Analytics aus und wählen Sie dann **[!UICONTROL Klassifizierungssätze]**.
1. Wählen **[!UICONTROL unter]** die Registerkarte **[!UICONTROL Klassifizierungssätze]** aus.
1. Wählen **[!UICONTROL Manager Klassifizierungssätze]** Klassifizierungssatz aus, für den Sie die Regeln definieren möchten.
1. Wählen Sie **[!UICONTROL Dialogfeld „Klassifizierungssatz _(Klassifizierungssatzname_]**&#x200B;die Registerkarte **[!UICONTROL Regeln]**&#x200B;aus.

   * Wenn Sie zum ersten Mal auf die **[!UICONTROL Rules]**-Schnittstelle für einen Klassifizierungssatz zugreifen oder sich bisher entschieden haben, weiterhin die alte Rule Builder-Schnittstelle zu verwenden, wird ein Dialogfeld angezeigt, in dem Sie auswählen können, wie Sie beginnen möchten. Die Optionen sind:

      * **Migrieren vorhandener Regeln**. Importieren Sie Ihre aktuellen Klassifizierungsregeln und arbeiten Sie weiterhin mit diesen Regeln in der neuen Benutzeroberfläche. Ihre vorhandenen Regeln werden beibehalten und in das neue Format konvertiert.
         * Wählen Sie **[!UICONTROL Regeln migrieren]** aus, um fortzufahren.
         * Lesen Sie **[!UICONTROL Dialogfeld &quot;]** bestätigen“ die Auswirkungen der Migration.
            * Wählen Sie **[!UICONTROL Regeln migrieren]** aus, um die Migration zu bestätigen. Verwenden Sie nach Abschluss der Migration die [Regelsatzschnittstelle), &#x200B;](#rule-set-interface) neue Regeln zu erstellen und Ihre vorhandenen migrierten Regeln zu bearbeiten.
            * Wählen Sie **[!UICONTROL Abbrechen]**, um die Migration abzubrechen

      * **Neu starten**. Erstellen Sie neue Klassifizierungsregeln von Grund auf mit dem neuen Regel-Builder. Wählen Sie diese Option aus, wenn Sie Ihre Klassifizierungslogik umgestalten oder mit neuen Klassifizierungsregeln neu starten möchten.
         * Wählen Sie **[!UICONTROL Neue Regeln erstellen]** aus, um fortzufahren.
         * Lesen Sie **[!UICONTROL Dialogfeld „Neuen]** bestätigen“ die Auswirkungen eines Neustarts.
            * Wählen Sie **[!UICONTROL Neu starten]**, um einen Neustart zu bestätigen und vorhandene Regeln zu verwerfen. Verwenden Sie die [Regelsatzschnittstelle](#rule-set-interface) um neue Regeln zu erstellen.
            * Wählen Sie zum Abbrechen **[!UICONTROL Abbrechen]** aus.


      * **Alte Benutzeroberfläche**. Verwenden Sie weiterhin die bisherige Oberfläche des Regel-Builders. Sie können jederzeit auf die neue Oberfläche umsteigen, wenn Sie bereit sind.
         * Wählen Sie **[!UICONTROL Zur alten Benutzeroberfläche wechseln]** aus, um fortzufahren. Sie werden zur veralteten Benutzeroberfläche **[!UICONTROL Classification Rule Builder]**.

   * Wenn Sie bereits Regeln migriert oder neue Regeln für einen Klassifizierungssatz erstellt haben, landen Sie direkt in der Benutzeroberfläche des Regelsatzes.



## Benutzeroberfläche für Regelsätze {#rule-set-interface}

>[!CONTEXTUALHELP]
>id="classificationsets_rules_samplekeys"
>title="Beispielschlüssel"
>abstract="Geben Sie Testschlüssel ein, oder fügen Sie sie ein, um den Regelsatz zu testen. Jede Zeile ist ein separater Schlüsselwert. Wählen Sie **[!UICONTROL Regelsatz testen]**, um ein Dialogfeld mit den Ergebnissen anzuzeigen."


Verwenden Sie zum Erstellen oder Bearbeiten von Regeln die Benutzeroberfläche „Regelsatz“.

![Regelsatz-Schnittstelle](assets/rulesets-ui.png)

| | Name | Beschreibung |
|---|---|---|
| 1 | **[!UICONTROL Funktionen]** | Im Bereich **[!UICONTROL Funktionen]** können Sie Ihre Funktionen auswählen und per Drag-and-Drop in den Regelsatz-Builder ziehen. |
| 2 | **Rule Set Builder** | Sie erstellen Ihren Regelsatz mit einer oder mehreren Regeln. Eine Regel ist die Implementierung einer Funktion, die immer nur einer Funktion zugeordnet ist. Eine Funktion kann über mehrere Operatoren verfügen. Sie erstellen eine Regel, indem Sie eine Funktion per Drag-and-Drop in den Regelsatz-Builder ziehen. Der Funktionstyp definiert die Schnittstelle der Regel. <br/>Weitere Informationen finden Sie in [&#128279;](#rule-interface)Regelschnittstelle).<br/>Funktionen können an jeder beliebigen Stelle eingefügt werden. Die Funktionen werden nacheinander ausgeführt, um die endgültigen Werte für die Klassifizierungen zu bestimmen.<br/>Mit **[!UICONTROL Alle reduzieren]** reduzieren Sie alle Regeln und verwenden Sie **[!UICONTROL Alle erweitern]**, um alle Regeln zu erweitern. |
| 3 | **[!UICONTROL Status]** | Zeigt Status und Datum der letzten Änderung des Regelsatzes an. <br/>Wählen Sie **[!UICONTROL Aktivieren]** aus, um den Regelsatz zu aktivieren. <br/>Wählen Sie **[!UICONTROL Deaktivieren]** aus, um den Regelsatz zu deaktivieren. |
| 4 | **[!UICONTROL Lookback]** | Geben Sie das Lookback-Fenster für den Regelsatz an.<br/>Wählen Sie eine Option (von 1 Monat bis 6 Monate) aus dem Dropdown-Menü aus.<br/>Wählen Sie **[!UICONTROL Lookback durchführen]** aus, um einen Lookback unter Verwendung des ausgewählten Lookback-Zeitraums durchzuführen. |
| 5 | **[!UICONTROL Testoptionen]** | Verwenden Sie Beispiel-Schlüsseldimensionswerte, um die Klassifizierungen zu testen: <ul><li>Fügen Sie Werte im Textbereich **[!UICONTROL Beispielschlüssel“ hinzu]** fügen Sie sie ein.<br/>Überprüfen Sie **[!UICONTROL Beispielschlüssel speichern]** um sicherzustellen, dass Beispielschlüssel in verschiedenen Verwendungsbereichen der Regelsatzschnittstelle bestehen bleiben.</li><li>Wählen **[!UICONTROL Regelsatz testen]**, um den Regelsatz zu testen.</li></ul> |


## Oberfläche für Regeln

Sie definieren jede einzelne Regel innerhalb des Regelsatzes in der Benutzeroberfläche „Regel“. Die Benutzeroberfläche besteht aus den folgenden Elementen:

![Regelschnittstelle](assets/rule-ui.png)

| | Beschreibung |
|---|---|
| 1 | Der Name der ausgewählten Funktion und die für die Funktion eingegebene Eingabe. |
| 2 | Die Eingabe für die ausgewählte Funktion. Die Eingabe hängt von der gewählten Funktion ab. Für die Funktion **[!UICONTROL Regulärer Ausdruck]** ist die Eingabe beispielsweise ein regulärer Ausdruck. Und für die **[!UICONTROL Split]**-Funktion ist die Eingabe ein Token. Geben Sie die entsprechende Eingabe für die spezifische Funktion ein. Beispiel: `^(.+)\:(.+)\:(.+)$` für einen regulären Ausdruck, der drei Klassifizierungen in einem internen Kampagnen-Code identifiziert. |
| 3 | Jeder Vorgang legt eine bestimmte Klassifizierung auf einen Wert fest. <br/>Wählen Sie im Dropdown-Menü **[!UICONTROL Klassifizierung festlegen]** eine Klassifizierung aus und geben Sie einen Wert für &quot;**[!UICONTROL &quot;]**. <br/>Verwenden Sie ![CrossSize400](/help/assets/icons/CrossSize400.svg), um einen Vorgang aus der Liste zu löschen. |
| 4 | Wählen Sie ![Hinzufügen](/help/assets/icons/Add.svg) **[!UICONTROL Vorgang hinzufügen]** aus, um der Funktion einen zusätzlichen Vorgang hinzuzufügen. |
| 5 | Wählen Sie ![ChevronDown](/help/assets/icons2/ChevronDown.svg) aus, um die Regel auszublenden. Wählen Sie ![ChevronLeft](/help/assets/icons/ChevronLeft.svg) aus, um die Regel zu erweitern.<br/>Wählen Sie ![CrossSize400](/help/assets/icons/CrossSize400.svg) aus, um die Regel zu löschen. |

## Funktionsreferenz

Im Folgenden finden Sie Details zu den erforderlichen Eingabe- und Beispielanwendungsfällen für jede unterstützte Funktion.


### Beginnt mit…

Legt eine Klassifizierung basierend auf einem bestimmten Wert fest, mit dem die Schlüsseldimension beginnt.

+++ Details 

#### Erforderliche Eingabe

Geben Sie einen Wert für **[!UICONTROL Beginnt mit“]**. Beispiel: `em`.

#### Anwendungsfall

Sie möchten eine Regel definieren, die `Email` als Wert für die Klassifizierung **[!UICONTROL Kanal]** zuweist, wenn der Wert für die Schlüsseldimension Interne Kampagne mit `em` beginnt (z. B.: `em:FY2025:Summer Sale`).

>[!BEGINTABS]

>[!TAB Regel]

![Regel - Beginnt mit](assets/rule-startswith.png)

>[!TAB Testergebnisse]

![Regel - Beginnt mit Testergebnissen](assets/rule-startswith-test.png)

>[!ENDTABS]

+++



### Endet mit…

Legt eine Klassifizierung basierend auf einem bestimmten Wert fest, mit dem die Schlüsseldimension endet.

+++ Details 

#### Erforderliche Eingabe

Geben Sie einen Wert für **[!UICONTROL Endet mit]** ein. Beispiel: `2025`.

#### Anwendungsfall

Sie möchten eine Regel definieren, die `2025` als Wert der Klassifizierung **[!UICONTROL Jahr]** zuweist, wenn der Wert für die Schlüsseldimension Interne Kampagne `2025` enthält (z. B.: `em:Summer Sale:FY2025`).

>[!BEGINTABS]

>[!TAB Regel]

![rule - endet mit](assets/rule-endswith.png)

>[!TAB Testergebnisse]

![Regel - Endet mit Testergebnissen](assets/rule-endswith-test.png)

>[!ENDTABS]

+++


### Enthält…

Legt eine Klassifizierung auf Grundlage eines bestimmten Werts fest, den die Schlüsseldimension enthält.

+++ Details 

#### Erforderliche Eingabe

Geben Sie einen Wert für **[!UICONTROL Enthält]** ein. Beispiel: `Winter`.

#### Anwendungsfall

Sie möchten eine Regel definieren, um der Klassifizierung `Winter Sale`Typ“ **[!UICONTROL als Wert zuzuweisen]** wenn der Wert für die Schlüsseldimension Interne Kampagne mit `Winter` enthält (z. B.: `fb:Winter:FY2024`).


>[!BEGINTABS]

>[!TAB Regel]

![Regel - Enthält](assets/rule-contains.png)

>[!TAB Testergebnisse]

![Regel - Enthält Ergebnisse](assets/rule-contains-test.png)

>[!ENDTABS]

+++


### Stimmt überein mit 

Legt eine Klassifizierung basierend auf einem bestimmten Wert fest, der mit dem Wert der Schlüsseldimension übereinstimmt.

+++ Details 

#### Erforderliche Eingabe

Geben Sie einen Wert für &quot;**[!UICONTROL &quot;]**. Beispiel: `em:Summer:2025`.

#### Anwendungsfall

Sie möchten eine Regel definieren, um `Email` als Wert für die Klassifizierung **[!UICONTROL Kanal]**, `Summer Sale` als Wert für die Klassifizierung **[!UICONTROL Typ]** und `2025` für die Klassifizierung **[!UICONTROL Jahr]** zuzuweisen. Aber nur, wenn der Wert für die Schlüsseldimension Interne Kampagne `em:Summer:2025` entspricht.


>[!BEGINTABS]

>[!TAB Regel]

![Regel - stimmt überein](assets/rule-matches.png)

>[!TAB Testergebnisse]

![Regel - stimmt überein](assets/rule-matches-test.png)

>[!ENDTABS]

+++


### Regulärer Ausdruck

Legt eine oder mehrere Klassifizierungen basierend auf einem regulären Ausdruck fest, der auf den Wert der Schlüsseldimension angewendet wird.

+++ Details 

#### Erforderliche Eingabe

Geben Sie einen Wert für **[!UICONTROL Regulärer Ausdruck]** ein. Beispiel: `^(.+)\:(.+)\:FY(.+)$`.

#### Anwendungsfall

Sie möchten eine Regel definieren, um den Klassifizierungen **[!UICONTROL Channel]**, **[!UICONTROL Type]** und **[!UICONTROL Year]** Werte zuzuweisen, indem Sie die `^(.+)\:(.+)\:FY(.+)$` des regulären Ausdrucks anwenden und Übereinstimmungsgruppen (`$1`, `$2` und `$3`) auf die Werte für die Schlüsseldimension Interne Kampagne verwenden.

>[!BEGINTABS]

>[!TAB Regel]

![Regel - Regulärer Ausdruck](assets/rule-regex.png)

>[!TAB Testergebnisse]

![Regel - Testergebnisse für reguläre Ausdrücke](assets/rule-regex-test.png)

>[!ENDTABS]



#### Referenztabelle

Unten finden Sie eine Referenztabelle mit regulären Ausdrücken.

| Regulärer Ausdruck | Beschreibung |
|---|---|
| `(?ms)` | Ordnen Sie den gesamten regulären Ausdruck einer mehrzeiligen Eingabe zu, sodass der `.` Platzhalter allen Zeilenumbruchzeichen entspricht. |
| `(?i)` | Ordnen Sie den gesamten regulären Ausdruck so zu, dass die Groß-/Kleinschreibung nicht beachtet wird. |
| `[abc]` | Beliebiges einzelnes Zeichen aus: a, b oder c |
| `[^abc]` | Beliebiges einzelnes Zeichen, außer: a, b oder c |
| `[a-z]` | Beliebiges einzelnes Zeichen im Bereich a-z |
| `[a-zA-Z]` | Beliebiges einzelnes Zeichen im Bereich a-z oder A-Z |
| `^` | Zeilenanfang (Übereinstimmung mit dem Zeilenanfang) |
| `$` | Am Ende der Zeile (oder vor dem Zeilenumbruch am Ende) anpassen |
| `\A` | Beginn der Zeichenfolge |
| `\z` | Ende der Zeichenfolge |
| `.` | Übereinstimmung mit einem beliebigen Zeichen (außer Umbruch) |
| `\s` | Beliebiges Whitespace-Zeichen |
| `\S` | Beliebiges Zeichen, außer Whitespace-Zeichen |
| `\d` | Beliebige Ziffer |
| `\D` | Beliebiges Zeichen, außer Ziffern |
| `\w` | Beliebiges Zeichen, das in Wörtern zulässig ist (Buchstabe, Ziffer, Unterstrich) |
| `\W` | Beliebiges Zeichen, das nicht in Wörtern zulässig ist |
| `\b` | Beliebige Wortgrenze |
| `(...)` | Alles erfassen zwischen |
| `(a\b)` | a oder b |
| `a?` | Null oder eins von a |
| `a*` | Null oder mehr von a |
| `a+` | Ein oder mehr von a |
| `a{3}` | Genau 3 von a |
| `a{3,}` | 3 oder mehr von a |
| `a{3,6}` | Zwischen 3 und 6 von a |

+++


### Aufspalten

Teilt den Wert der Schlüsseldimension basierend auf einem Token auf eine oder mehrere Klassifizierungen auf.

+++ Details

#### Erforderliche Eingabe

Geben Sie einen Wert für &quot;**[!UICONTROL &quot;]**. Beispiel: `:`.

#### Anwendungsfall

Sie möchten eine Regel definieren, die die Werte für die Schlüsseldimension Interne Kampagne auf die Klassifizierungen **[!UICONTROL Kanal]**, **[!UICONTROL Typ]** und **[!UICONTROL Jahr]** basierend auf dem `:`**[!UICONTROL Token]** aufteilt.

>[!BEGINTABS]

>[!TAB Regel]

![Regel - Aufspaltung](assets/rule-split.png)

>[!TAB Testergebnisse]

![Regel - Aufspaltung der Testergebnisse](assets/rule-split-test.png)

>[!ENDTABS]

+++

## Regelpriorität

Die letzte Regel bestimmt den Wert für die Klassifizierung, wenn:

* Ein Schlüssel-Dimensionswert wird mehreren Regeln zugeordnet.
* Der Regelsatz enthält Regeln mit demselben Vorgang **[!UICONTROL Klassifizierung festlegen]**.

Daher sollten Sie den wichtigsten Vorgang **[!UICONTROL Klassifizierung von]**) als Teil der letzten Regel in Ihrem Regelsatz bewerten.

Wenn Sie mehrere Regeln erstellen, die nicht denselben Vorgang **[!UICONTROL Klassifizierung festlegen]** verwenden, spielt die Verarbeitungsreihenfolge keine Rolle.


### Beispiel

Sie möchten mit der Klassifizierung (**[!UICONTROL ) klassifizieren]** wie Benutzer mithilfe der Suchzeichenfolge als Schlüsseldimension nach einem Sportler suchen. Verwenden Sie beispielsweise diesen Regelsatz:

![Regelpriorität](assets/rule-priority.png)

* Wenn ein(e) Benutzende(r) nach `Cowboys Fantasy Tony Romo` sucht, wird `Romo` als &quot;**[!UICONTROL &quot;]**.
* Wenn ein(e) Benutzende(r) nach `Cowboys Fantasy Tony Romeo` sucht`Fantasy` wird als **[!UICONTROL Typ]** klassifiziert.
* Wenn ein(e) Benutzende(r) nach `Cowboys vs. Broncos` sucht`Team` wird als **[!UICONTROL Typ]** klassifiziert.

