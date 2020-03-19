---
description: Überprüfen Sie, ob Ihre Dynamic Tag Management-Bibliothek ordnungsgemäß auf Ihrer Website geladen wird.
keywords: Analytics Implementation;implementation method;dynamic tag management;dtm;code;page code;header code;footer code;embed code;verify code;verify header code;verify footer code;embed tab;embed
title: Kopf- und Fußzeilencode überprüfen
topic: Developer and implementation
uuid: d395a417-0c61-41a6-a124-d2f400f4626f
translation-type: ht
source-git-commit: ebf149df7974f9f2889b6fe938088eda90c84051

---


# Kopf- und Fußzeilencode überprüfen

Überprüfen Sie, ob Ihre Dynamic Tag Management-Bibliothek ordnungsgemäß auf Ihrer Website geladen wird.

1. Öffnen Sie Ihre Website im Browser.
1. Öffnen Sie die [!UICONTROL Entwickler-Konsole] indem Sie mit der rechten Maustaste klicken und **[!UICONTROL Element prüfen]** > **[!UICONTROL Konsole]** auswählen. 
1. Drücken Sie die **[!UICONTROL Eingabetaste]**.

   Wenn der Code ordnungsgemäß installiert wurde, wird *`true`* in der Konsole angezeigt.

   Wenn der Code nicht korrekt installiert wurde, wird der Verweisfehler angezeigt:

   `_satellite is not defined`

   Wenn dieser Fehler angezeigt wird, müssen Sie sicherstellen, dass:

* Sie auf jeder einzelnen Seite der Website den vollständigen Kopfzeilencode im [!DNL HEAD]-Bereich so nah wie möglich am [!DNL <head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">]-Tag platziert haben.
* Keine unerwarteten Zeichen im Codeabschnitt angezeigt werden (die beispielsweise beim Kopieren und Einfügen aus einem formatierten Dokument entstanden sein können).

