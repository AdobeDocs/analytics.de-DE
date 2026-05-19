---
title: Legacy-Debugger
description: Installieren Sie den Legacy-Debugger. Dieser Debugger überprüft Tags für Analytics, Target, Advertising, Identity Service und Datenerfassung.
feature: Implementation Basics
exl-id: 8fd07285-f702-4770-81bd-5f856561f4a9
role: Admin, Developer, Leader, User
TQID: https://experienceleague.adobe.com/igbKBwN0NmXCPRi9Rc1UtG7Ty1ffpd0rwyWEOTWPWdk
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 157cc2bde1047063014aff39319d5cfaa1de9b5c
workflow-type: tm+mt
source-wordcount: 681
ht-degree: 75%

---

# Legacy-Debugger

>[!IMPORTANT]
>
>Dieses Debugging-Tool wird nicht mehr unterstützt. Adobe empfiehlt stattdessen die Verwendung der [Adobe CX Enterprise Debugger-Chrome-Erweiterung](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=de).

Der [!UICONTROL Legacy-Debugger] überprüft Tags für die meisten Adobe CX Enterprise-Services. Mithilfe des Debuggers können Sie sehen, welche Daten auf einer bestimmten Seite Ihrer Site an Adobe gesendet werden. Anhand dieser Informationen können Sie die Implementierung Ihrer Organisation reparieren oder validieren.

## Installieren des Legacy-Debuggers

Erstellen Sie ein JavaScript-Lesezeichen, um den Debugger zu installieren.

### Schritt 1: Lesezeichen-Code kopieren

Kopieren Sie den folgenden Code in die Zwischenablage:

```JavaScript
javascript:void(window.open("","stats_debugger","width=800,height=800,location=0,menubar=0,status=1,toolbar=0,resizable=1,scrollbars=1").document.write("<script language=\"JavaScript\" id=dbg src=\"https://www.adobetag.com/d1/digitalpulsedebugger/live/DPD.js\"></"+"script>"+"<script language=\"JavaScript\">window.focus();</script>"));
```

### Schritt 2: Lesezeichen-Code in ein Lesezeichen einfügen

Jeder Browser hat verschiedene Möglichkeiten, Lesezeichen zu bearbeiten, aber das Konzept ist dasselbe. Ein Lesezeichen wird mit dem gewünschten Namen und dem Lesezeichen-Code als URL erstellt.

#### Chrome

Wenn Sie darauf bestehen, die [Chrome-Erweiterung](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=de) nicht zu verwenden, kann stattdessen das Legacy-Debugger-Lesezeichen verwendet werden.

1. Klicken Sie auf die drei Punkte oben rechts und gehen Sie dann zu „Lesezeichen“ > „Lesezeichen-Manager“. Sie können auch die Tastenkombination `Ctrl` + `Shift` + `O` (Windows) oder `Cmd` + `Shift` + `O` (Mac) drücken.
2. Klicken Sie oben rechts im Lesezeichen-Manager auf die drei Punkte und dann auf „Neues Lesezeichen hinzufügen“.
3. Beschriften Sie ihn im Feld Name mit „Legacy Debugger“ und fügen Sie den Code-Ausschnitt in das URL-Feld ein.
4. Verwenden Sie den Lesezeichen-Manager, um Ihr neues Lesezeichen an der gewünschten Stelle zu platzieren.

#### Firefox

1. Klicken Sie auf die drei Zeilen oben rechts und gehen Sie dann zu „Bibliothek“ > „Lesezeichen“ > „Alle Lesezeichen anzeigen“. Sie können auch die Tastenkombination `Ctrl` + `Shift` + `B` (Windows) oder `Cmd` + `Shift` + `B` (Mac) drücken.
2. Klicken Sie auf „Organisieren“ > „Neues Lesezeichen“.
3. Beschriften Sie ihn mit „Legacy-Debugger“ im Feld Name und fügen Sie den Code-Ausschnitt in das Feld Speicherort ein. Die Felder „Tags“ und „Keyword“ sind nicht erforderlich.
4. Verwenden Sie das Bibliotheksfenster, um Ihr neues Lesezeichen an der gewünschten Stelle zu platzieren.

#### Edge

In Edge können Sie Lesezeichen nicht manuell erstellen, jedoch können Sie eine Lesezeichen-URL in ein Lesezeichen umwandeln.

1. Klicken Sie auf das Sternsymbol rechts neben dem Feld „URL“, um die aktuelle Seite mit einem Lesezeichen zu versehen.
2. Benennen Sie das Lesezeichen „Legacy Debugger“ und speichern Sie es am gewünschten Speicherort.
3. Klicken Sie auf das Sternsymbol mit Linien, um die Favoritenleiste zu öffnen.
4. Klicken Sie mit der rechten Maustaste auf das neu erstellte Lesezeichen und wählen Sie „URL bearbeiten“.
5. Fügen Sie den Codeausschnitt in das Textfeld ein und drücken Sie die Eingabetaste.

#### Safari

In Safari können Sie Lesezeichen nicht manuell erstellen, jedoch können Sie eine Lesezeichen-URL in ein Lesezeichen umwandeln.

1. Klicken Sie oben rechts auf das Symbol „Freigeben“, um ein modales Lesezeichen-Fenster zu öffnen.
2. Benennen Sie das Lesezeichen „Legacy Debugger“ und speichern Sie es am gewünschten Speicherort.
3. Klicken Sie auf „Lesezeichen“ > „Lesezeichen bearbeiten“ und suchen Sie das neu erstellte Lesezeichen.
4. Klicken Sie mit der rechten Maustaste, wählen Sie „Adresse bearbeiten“ und fügen Sie dann den Codeausschnitt in das Textfeld ein.

## Verwenden des Legacy-Debuggers

Navigieren Sie zur gewünschten Seite auf Ihrer Website und klicken Sie dann auf das Lesezeichen. Es wird ein Popupfenster mit an Adobe gesendeten Daten angezeigt.

>[!NOTE]
>
>Bestimmte werbeblockierende Plug-ins und Popupblocker können das Laden des Debugger-Fensters beeinträchtigen. Überprüfen Sie, ob Popups im Browser blockiert sind, und lassen Sie sie zu, damit der Debugger ordnungsgemäß funktioniert.

Für den Debugger stehen verschiedene Optionen zur Verfügung, mit denen die Anzeige der Daten angepasst wird. Keine dieser Optionen wirkt sich auf die Datenerfassung aus.

* **[!UICONTROL Angezeigte Experience Cloud-Produkte]**: Blendet Bildanforderungen für die jeweiligen CX Enterprise-Produkte ein oder aus.
* **[!UICONTROL URL-Decodierung]**: URL decodiert die Bildanforderung, sodass sie mit dem übereinstimmt, was im Bericht angezeigt wird. Adobe empfiehlt, dieses Kontrollkästchen zu aktivieren.
* **[!UICONTROL Auto Refresh]**: aktualisiert das Popup-Fenster automatisch alle paar Sekunden, um auf weitere Bildanforderungen auf der Seite zu prüfen. Wenn Sie Inhalte im Debugger kopieren/einfügen müssen, deaktivieren Sie die automatische Aktualisierung, damit die Auswahl erhalten bleibt.
* **[!UICONTROL Benutzerfreundliches Format]**: Schaltet das Anzeigeformat zwischen hilfreichen Beschriftungen und rohen Abfragezeichenfolgen in einer Bildanforderung um. Weitere Informationen finden Sie unter [Datenerfassungs-Abfrageparameter](query-parameters.md).

Um standardmäßige Anzeigeoptionen für den Debugger zu speichern, klicken Sie mit der rechten Maustaste auf den Link „Adobe Debugger“ in der oberen rechten Ecke und kopieren Sie dann die Linkadresse. Bearbeiten Sie das aktuelle Debugger-Lesezeichen und fügen Sie den aktualisierten Codeausschnitt in das Feld „URL“ ein.
