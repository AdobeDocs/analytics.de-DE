---
description: Häufige Einsatzmöglichkeiten für Verarbeitungsregeln.
subtopic: Processing rules
title: Anwendungsfälle für Verarbeitungsregeln
feature: Processing Rules
role: Admin
exl-id: 914a0d31-d256-456e-a44a-008490e86a23
source-git-commit: 0bed2622f54bf2f46aa57dbfad7bd55a61d6c7d0
workflow-type: tm+mt
source-wordcount: '831'
ht-degree: 16%

---

# Anwendungsfälle für Verarbeitungsregeln

Die Anwendungsmöglichkeiten für die Verwendung von Verarbeitungsregeln in Ihrem Unternehmen sind vielfältig. In den folgenden Abschnitten werden einige gängige Methoden erläutert, mit denen Sie diese zu Ihrem Vorteil nutzen können.

+++Kontextdatenvariable in eine eVar kopieren

Verarbeitungsregeln werden verwendet, um Werte von [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md) in [Props](/help/components/dimensions/prop.md) und [eVars](/help/components/dimensions/evar.md) zu verschieben. Ohne Verarbeitungsregeln sind Kontextdatenvariablen bedeutungslos und füllen keine Berichte in Analytics aus.

Die [!UICONTROL Kontextvariablen] enthält alle Variablen, die in den letzten 30 Tagen an die Report Suite gesendet wurden. Wenn Sie den Namen der Kontextdatenvariablen kennen, ihn jedoch nicht an die aktuelle Report Suite gesendet haben, können Sie ihn manuell hinzufügen:

![Manuelles Hinzufügen einer Kontextdatenvariablen zu einer Verarbeitungsregel](assets/add-context-variable.png)

Im folgenden Beispiel wird die `search_term` Kontextdatenvariable genommen und ihr Wert in eVar3 platziert:

| Regelsatz | Wert |
| Bedingung | `search_term` (Kontextdaten) ist festgelegt |
| Aktion | [!UICONTROL Wert von überschreiben] eVar3 mit `search_term` (Kontextdaten) |

![Screenshot der Schnittstelle für Verarbeitungsregeln, auf der die Verwendung einer Kontextdatenvariablen dargestellt ist](assets/set-context-data.png)

Das obige Beispiel funktioniert hervorragend, wenn nur wenige eVars gefüllt werden müssen. Wenn Ihre Organisation über Hunderte von Kontextdatenvariablen verfügt, die jeweils eine eigene eVar benötigen, können Sie bedingte Anweisungen verwenden. Dutzende bedingte Anweisungen können in eine einzige Verarbeitungsregel passen, sodass Ihre Organisation alle eVars in einer Report Suite füllen kann, ohne das Verarbeitungsregellimit von 150 Regeln zu verletzen.

Im folgenden Beispiel werden mehrere Variablen mit unterschiedlichen Kontextdatenvariablen gefüllt. Eine Aktion enthält auch eine bedingte Anweisung:

| Regelsatz | Wert |
| Aktion | [!UICONTROL Wert von überschreiben] eVar55 mit `spa.billing_customer_name` (Kontextdaten) |
| Aktion | [!UICONTROL Wert von überschreiben] Prop7 mit `testhierarchy` (Kontextdaten), wenn `testhierarchy` (Kontextdaten) festgelegt ist |
| Aktion | [!UICONTROL Wert von überschreiben] eVar8 mit `spa.ims_org` (Kontextdaten) |

![Screenshot der Schnittstelle für Verarbeitungsregeln, auf der gezeigt wird, wie ein Wert bedingt festgelegt werden kann](assets/add-conditional.png)

+++

+++Festlegen eines Ereignisses mithilfe einer Kontextdatenvariablen

Verarbeitungsregeln können Trigger-Ereignisse basierend auf [Kontextdatenvariablen) ](/help/implement/vars/page-vars/contextdata.md).

Die [!UICONTROL Kontextvariablen] enthält alle Variablen, die in den letzten 30 Tagen an die Report Suite gesendet wurden. Wenn Sie den Namen der Kontextdatenvariablen kennen, ihn jedoch nicht an die aktuelle Report Suite gesendet haben, können Sie ihn manuell hinzufügen:

![Manuelles Hinzufügen einer Kontextdatenvariablen zu einer Verarbeitungsregel](assets/add-context-variable.png)

Die folgende Regeldefinition legt für jeden Treffer, der eine bestimmte Kontextdatenvariable enthält, ein Ereignis fest:

| Regelsatz | Wert |
| --- | --- |
| Bedingung | `search_term` (Kontextdaten) ist festgelegt |
| Aktion | [!UICONTROL Ereignis festlegen] event1 auf [!UICONTROL Benutzerdefinierter Wert] `1` |

![Screenshot der Benutzeroberfläche für Verarbeitungsregeln, auf der gezeigt wird, wie ein Ereignis festgelegt wird](assets/processing_rule_set_event.png)

+++

+++Füllen Sie eine Variable mithilfe eines Abfragezeichenfolgenparameters

Sie können eine Variable mithilfe eines Abfragezeichenfolgenparameters auffüllen. In den meisten Fällen würden Sie Ihre Implementierung normalerweise anpassen, um die gewünschten Werte für die Abfragezeichenfolge zu erhalten. Wenn Sie Ihre Implementierung jedoch nicht einfach anpassen können, um diese Daten zu erfassen, sind Verarbeitungsregeln eine geeignete Alternative. Wenn das Auffüllen aufgrund eines Schreibfehlers oder einer vergleichbaren Ursache fehlschlägt, können Sie die Variable mit Hilfe von Verarbeitungsregeln auffüllen.

Überprüfen Sie immer, ob ein Wert leer ist oder den erwarteten Wert enthält, bevor Sie ihn überschreiben.

| Regelsatz | Wert |
| --- | --- |
| Bedingung | Kampagne ist nicht festgelegt |
| Aktion | [!UICONTROL Wert von überschreiben] Campaign mit [!UICONTROL Abfragezeichenfolgenparameter] `cpid` |

![Screenshot der Benutzeroberfläche für Verarbeitungsregeln mit bedingter Kampagnenlogik](assets/set-campaign-conditionally.png)

| Regelsatz | Wert |
| --- | --- |
| Bedingung | [!UICONTROL Abfragezeichenfolgenparameter] `q` [!UICONTROL festgelegt] |
| Aktion | [!UICONTROL Wert von überschreiben] Interne Suchbegriffe mit [!UICONTROL Abfragezeichenfolgenparameter] `q` |

![Screenshot der Benutzeroberfläche für Verarbeitungsregeln mit interner Suchbegrifflogik](assets/populate-internal-search-terms.png)

+++

+++Beliebiges Ereignis bedingt festlegen

Ereignisse können basierend auf jeder in den Verarbeitungsregeln verfügbaren Bedingung festgelegt werden. Beispielsweise können Sie einen Trigger für ein Ereignis erstellen, wenn der Seitenname „Produktübersicht“ lautet.

| Regelsatz | Wert |
| --- | --- |
| Bedingung | Wenn [!UICONTROL Seitenname] gleich „Produktübersicht“ ist |
| Aktion | [!UICONTROL Ereignis] ([!UICONTROL ) &#x200B;] auf [!UICONTROL benutzerdefinierter Wert] `1` |

![Screenshot der Schnittstelle für Verarbeitungsregeln, auf der ein bedingt festgelegtes Ereignis angezeigt wird](assets/set-product-view-event.png)

+++

+++Hinzufügen einer Unterkategorie durch Verketten von Kategorie und Seitenname

Mit der Option „Verketten“ können Sie Werte durch die Kombination anderer Werte ausfüllen.

| Regelsatz | Wert |
| --- | --- |
| Bedingung | Keine (immer ausführen) |
| Aktion | [!UICONTROL Wert von überschreiben] eVar1 mit [!UICONTROL Verketteter Wert] Kategorie + Seitenname |

![Screenshot der Schnittstelle für Verarbeitungsregeln mit einem verketteten Wert](assets/add-subcategory-using-concat.png)

+++

+++Bereinigen von Werten in einem Bericht

Sie können Werte mit gesammelten Rechtschreibfehlern abgleichen und sie aktualisieren, damit sie in Berichten korrekt angezeigt werden.

Adobe empfiehlt, die restriktivste Abgleichoption zu verwenden, um unerwünschte Überschreibungen zu vermeiden. Sie können einen Bericht zu der Variablen ausführen und nach potenziellen Regelbedingungen suchen, die Sie verwenden möchten. Beim Zeichenfolgenvergleich wird nicht zwischen Groß- und Kleinschreibung unterschieden.

| Regelsatz | Wert |
| --- | --- |
| Bedingung | Wenn prop1 [!UICONTROL beginnt mit] &quot;[!DNL Shoping]&quot; |
| Aktion | [!UICONTROL Wert von überschreiben] prop1 mit [!UICONTROL Benutzerdefinierter Wert] &quot;[!DNL Shopping]&quot; |

![Screenshot der Benutzeroberfläche für Verarbeitungsregeln, auf der gezeigt wird, wie ein Tippfehler behoben werden kann](assets/clean-up-values-in-report.png)

+++

+++Ereignis aus einem Treffer entfernen

Sie können ein bestimmtes Ereignis aus einem Treffer mithilfe von Verarbeitungsregeln entfernen oder verwerfen, ohne Ihre Implementierung zu ändern. Wenn Sie für das Ereignis den benutzerdefinierten `0` festlegen, wird das Ereignis nicht gezählt.

| Regelsatz | Wert |
| Bedingung | Keine (immer ausführen) |
| Aktion | [!UICONTROL Ereignis festlegen] Event1 auf [!UICONTROL Benutzerdefinierter Wert] `0` |

![Screenshot der Oberfläche für Verarbeitungsregeln, auf der zu sehen ist, wie ein Ereignis entfernt wird](assets/remove_event.png)

+++
