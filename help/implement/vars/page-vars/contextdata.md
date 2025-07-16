---
title: contextData
description: Mithilfe von Kontextdatenvariablen können Sie auf jeder Seite benutzerdefinierte Variablen definieren, die Verarbeitungsregeln lesen können.
feature: Appmeasurement Implementation
exl-id: f2c747a9-1a03-4f9f-8025-9f4745403a81
role: Admin, Developer
source-git-commit: c2adf6d2e328378332cc290ba2dfd75ee6587ef6
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 68%

---

# contextData

Mithilfe von Kontextdatenvariablen können Sie auf jeder Seite benutzerdefinierte Variablen definieren, die Verarbeitungsregeln lesen können. Anstatt Analytics-Variablen explizit Werte in Ihrem Code zuzuweisen, können Sie Daten in Kontextdatenvariablen senden. Verarbeitungsregeln nehmen dann Kontextdatenvariablenwerte auf und übergeben sie an die entsprechenden Analytics-Variablen. Weitere Informationen finden Sie im Admin-Benutzerhandbuch unter [Verarbeitungsregeln](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-overview.md).

Kontextdatenvariablen sind für Entwicklungsteams hilfreich, um Daten in benannten Elementen, statt in nummerierten Variablen zu erfassen. Anstatt beispielsweise anzufordern, dass Entwicklungsteams den Autor der Seite `eVar10` zuweisen, können Sie sie stattdessen auffordern, ihn `s.contextData["author"]` zuzuweisen. Ein Analytics-Administrator in Ihrem Unternehmen kann dann Verarbeitungsregeln erstellen, um Kontextdatenvariablen Analysevariablen für die Berichterstellung zuzuordnen. Entwicklungs-Teams würden sich letztendlich nur um Kontextdatenvariablen kümmern, anstatt um die vielen Seitenvariablen, die Adobe anbietet.

## Kontextdatenvariablen, die das Web SDK verwenden

Bei Verwendung des [**XDM-**](/help/implement/aep-edge/xdm-var-mapping.md)) werden alle Felder, die keiner Adobe Analytics-Variablen zugeordnet sind, automatisch als Kontextdatenvariable eingefügt. Sie können Kontextdaten auch explizit mithilfe des XDM-Objekts festlegen. Anschließend können Sie [Verarbeitungsregeln](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-overview.md) verwenden, um die Kontextdatenvariable der gewünschten Analytics-Variablen zuzuweisen.  Weitere Informationen finden [ unter „Zuordnen anderer XDM-Felder ](../../aep-edge/xdm-var-mapping.md#mapping-other-xdm-fields-to-analytics-variables) Analytics-Variablen“.

Bei Verwendung des [**Datenobjekts**](/help/implement/aep-edge/data-var-mapping.md) befinden sich alle Kontextdatenvariablen in `data.__adobe.analytics.contextData` als Schlüssel-Wert-Paare:

```js
alloy("sendEvent", {
  "data": {
    "__adobe": {
      "analytics": {
        "contextData": {
          "example_variable": "Example value",
          "second_example": "Another value"
        }
      }
    }
  }
});
```

Die [Verarbeitungsregeln](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-overview.md) Benutzeroberfläche zeigt `example_variable` und `second_example` in den entsprechenden Dropdown-Menüs an.

## Kontextdatenvariablen, die die Adobe Analytics-Erweiterung verwenden

Die Adobe Experience Platform-Datenerfassung verfügt über keinen speziellen Ort zum Festlegen von Kontextdatenvariablen. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.contextData in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.contextData`-Variable nimmt keinen Wert direkt an. Legen Sie stattdessen die Eigenschaften dieser Variablen auf eine Zeichenfolge fest.

```js
// Assign the example_variable property a value
s.contextData["example_variable"] = "Example value";
```

* Gültige Kontextdatenvariablen enthalten nur alphanumerische Zeichen, Unterstriche und Punkte. Adobe garantiert die Datenerfassung in den Verarbeitungsregeln nicht, wenn Sie andere Zeichen, wie z. B. Bindestriche, einfügen.
* Starten Sie Kontextdatenvariablen nicht mit `"a."`. Dieses Präfix ist reserviert und wird von Adobe verwendet. Verwenden Sie zum Beispiel nicht `s.contextData["a.InstallEvent"]`.
* Bei Kontextdatenvariablen wird nicht zwischen Groß- und Kleinschreibung unterschieden. Die Variablen `s.contextData["example"]` und `s.contextData["EXAMPLE"]` sind identisch.
* Ein einzelner Schlüssel kann nicht mehr als einen Wert enthalten. Wenn Sie Kontextdatenvariablen für Variablen mit mehreren Werten verwenden möchten, verketten Sie alle Werte mithilfe eines Trennzeichens (normalerweise ein Komma) und übergeben Sie sie entweder in eine [Listen-Prop](prop.md#list-props) oder eine [Listenvariable](list.md) mithilfe von Verarbeitungsregeln.

## Verwenden von Verarbeitungsregeln zum Ausfüllen von Analytics-Variablen

>[!WARNING]
>
>Kontextdatenvariablen werden nach Ausführung der Verarbeitungsregeln verworfen. Wenn keine Verarbeitungsregeln aktiv sind, die Werte in Variablen platzieren, gehen diese Daten dauerhaft verloren!

1. Aktualisieren Sie Ihre Implementierung, um Kontextdatenvariablennamen und -werte festzulegen.
2. Melden Sie sich bei Adobe Analytics an und gehen Sie zu **[!UICONTROL Admin]** > **[!UICONTROL Report]** Suites.
3. Wählen Sie die gewünschte Report Suite aus und navigieren Sie zu **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Verarbeitungsregeln]**.
4. Erstellen Sie eine Verarbeitungsregel, die eine Analytics-Variable auf den Wert der Kontextdatenvariablen setzt.
5. Speichern Sie die Änderungen.

Verarbeitungsregeln werden sofort nach dem Speichern wirksam. Sie gelten nicht für historische Daten.

## Senden von Kontextdaten in einem Linktracking-Aufruf

Schließen Sie die Kontextdatenvariable als Eigenschaft von `contextData` in [`s.linkTrackVars`](../config-vars/linktrackvars.md) ein:

```js
s.contextData["example_variable"] = "Example value";
s.linkTrackVars = "contextData.example_variable";
s.tl(true,"o","Example context data link");
```

## Ereignisse mithilfe von Kontextdatenvariablen erhöhen

Beim Erstellen von Verarbeitungsregeln können Sie Ereignissen Kontextdatenvariablen zuweisen.

* Enthält eine Kontextdatenvariable einen Textt, wird das Ereignis um 1 inkrementiert.
* Wenn eine Kontextdatenvariable eine Ganzzahl enthält, wird das Ereignis um diesen ganzzahligen Betrag inkrementiert.

```js
// Assigning this context data variable to an event increments it by one
s.contextData["example_text"] = "Text value";

// Assigning this context data variable to an event increments it by four
s.contextData["example_number"] = "4";
```
