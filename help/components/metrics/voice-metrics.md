---
title: Sprache – Analysemetriken
description: Sprache – Analysemetriken
feature: Metrics
exl-id: 3c1b4e4e-d8d2-446f-9582-a2ce5580a8d3
source-git-commit: 6a229439c455389b88d5fe96a0366b8888809c02
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 21%

---

# Sprache – Analysemetriken

Wenn Sie [!UICONTROL Voice and Chatbots] in [[!UICONTROL Anwendungsberichten]](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/app-reporting.md) aktivieren, werden die folgenden Metriken (und [Dimensionen](../dimensions/voice-dimensions.md)) erstellt. Sie können [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md) verwenden, um sie auf den Wert `1` (oder mehr, falls zutreffend) festzulegen. Wenn dies in den Report Suite-Einstellungen aktiviert ist, werden [Verarbeitungsregeln](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md) automatisch erstellt, um Sprachanalysemetriken ihrer zugehörigen Kontextdatenvariablen zuzuordnen.

| Metrikname | Beschreibung | Kontextdatenvariable |
| --- | --- | --- |
| Sprache – Äußerungen | Trigger, wenn einem Sprachassistenten ein Befehl erteilt wird. | `a.voiceutterances` |
| Sprache – Sitzung beenden | Trigger, wenn die Sprachanwendung geschlossen ist. | `a.voiceendsession` |
| Sprache – Fehler | Trigger, in denen die Voice App auf einen Fehler stößt. | `a.voiceerror` |

{style="table-layout:auto"}
