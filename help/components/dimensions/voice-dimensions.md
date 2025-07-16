---
title: Voice Analytics-Dimensionen
description: Voice Analytics-Dimensionen
feature: Dimensions
exl-id: 6e1275c4-3b17-4c65-a308-d420ea1acdf6
source-git-commit: c2adf6d2e328378332cc290ba2dfd75ee6587ef6
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 6%

---

# Voice Analytics-Dimensionen

Wenn Sie [!UICONTROL Sprach- und &#x200B;]) für [[!UICONTROL Anwendungsberichte]](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/app-reporting.md) aktivieren, werden die folgenden Dimensionen (und [Metriken](../metrics/voice-metrics.md)) erstellt. Sie können [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md) verwenden, um sie auf den gewünschten Zeichenfolgenwert festzulegen. Wenn diese Option in den Report Suite[Einstellungen aktiviert ist, ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-overview.md) automatisch Verarbeitungsregeln erstellt, die Sprachanalysedimensionen der zugehörigen Kontextdatenvariablen zuordnen.

| Name der Dimension | Beschreibung | Kontextdatenvariable |
| --- | --- | --- |
| Sprachfehlertyp | Der Typ des aufgetretenen Fehlers. | `a.voiceerrortype` |
| Sprache | Die Sprache, in der der Benutzer mit Ihrer Sprach-App interagiert. | `a.voicelanguage` |
| Sprachabsicht | Der Befehl, den der Benutzer ausführen möchte. | `a.voiceintent` |
| Sprach-App-Antwort | Die Antwort, die die Sprach-App an den Benutzer zurückgegeben hat. | `a.voiceappresponse` |
| Sprach-Authentifizierung | Der authentifizierte Status des Benutzers bei der Interaktion mit der Sprach-App. | `a.voiceauthentication` |
| Point of Interest-ID | Die Point of Interest-ID. | `a.loc.poi.id` |

{style="table-layout:auto"}
