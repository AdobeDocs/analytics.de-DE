---
title: Sprachanalysedimensionen
description: Sprachanalysedimensionen
feature: Dimensions
exl-id: 6e1275c4-3b17-4c65-a308-d420ea1acdf6
source-git-commit: 6a229439c455389b88d5fe96a0366b8888809c02
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 4%

---

# Sprachanalysedimensionen

Wenn Sie [!UICONTROL Voice and Chatbots] in [[!UICONTROL Anwendungsberichten]](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/app-reporting.md) aktivieren, werden die folgenden Dimensionen (und [Metriken](../metrics/voice-metrics.md)) erstellt. Sie können [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md) verwenden, um sie auf den gewünschten Zeichenfolgenwert festzulegen. Wenn diese Option in den Report Suite-Einstellungen aktiviert ist, werden [Verarbeitungsregeln](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md) automatisch erstellt, um Sprachanalysedimensionen ihrer zugehörigen Kontextdatenvariablen zuzuordnen.

| Name der Dimension | Beschreibung | Kontextdatenvariable |
| --- | --- | --- |
| Sprachfehlertyp | Die Art des aufgetretenen Fehlers. | `a.voiceerrortype` |
| Sprachsprache | Die Sprache, in der der Benutzer mit Ihrer Sprachanwendung interagiert. | `a.voicelanguage` |
| Sprachabsicht | Der Befehl, den der Benutzer ausführen möchte. | `a.voiceintent` |
| Sprachanwendungs-Antwort | Die Antwort, die die Voice App an den Benutzer zurückgegeben hat. | `a.voiceappresponse` |
| Sprachauthentifizierung | Der authentifizierte Status des Benutzers bei der Interaktion mit der Voice App. | `a.voiceauthentication` |
| Zielpunkt-ID | Die Zielpunkt-ID. | `a.loc.poi.id` |

{style="table-layout:auto"}
