---
description: Verarbeitungsregeln können Ereignisse auf der Grundlage von Kontextdatenvariablen auslösen.
subtopic: Processing rules
title: Festlegen eines Ereignisses mit einer Kontextdatenvariablen
feature: Admin Tools
role: Admin
exl-id: f0af0e23-c08a-4f82-85b4-25064eeaa3c6
source-git-commit: 429aaa43fdae669350bdb5a5a54a7d4b9b1c65f2
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 100%

---

# Festlegen eines Ereignisses mit einer Kontextdatenvariablen

Verarbeitungsregeln können Ereignisse auf der Grundlage von Kontextdatenvariablen auslösen.

Kontextdatenvariablen werden in AppMeasurement im folgenden Format spezifiziert:

```
 s.contextData['search_term']
```

Die [!UICONTROL Kontextvariablenliste] enthält alle Variablen, die in den letzten 30 Tagen an die Report Suite gesendet wurden. Wenn Sie den Namen der Kontextdatenvariablen kennen, diese aber nicht an die aktuelle Report Suite gesendet haben, können Sie einen Wert hinzufügen, indem Sie den Variablennamen eingeben und auf **[!UICONTROL Kontextdaten für Variablennamen hinzufügen]** klicken:

![](assets/add-context-variable.png)

Die folgende Regeldefinition erweitert die Regel [Kontextdatenvariable in eine eVar kopieren](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md), um bei jedem Hit, der eine bestimmte Kontextdatenvariable enthält, auch ein Ereignis zu setzen:

| Regelsatz | Wert |
|---|---|
| Bedingung | Wenn „Suchbegriff“-Kontextdaten eingestellt sind |
| Aktion | Ereignis „Suchvorgänge“ setzen |

Beispiel:

![](assets/processing_rule_set_event.png)

Weitere Informationen finden Sie unter [Kontextdatenvariablen](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/contextdata.html?lang=de) in der Implementierungshilfe.
