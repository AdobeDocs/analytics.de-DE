---
title: Sprache – Analysemetriken
description: Sprache – Analysemetriken
feature: Metrics
exl-id: 3c1b4e4e-d8d2-446f-9582-a2ce5580a8d3
source-git-commit: c2adf6d2e328378332cc290ba2dfd75ee6587ef6
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 21%

---

# Sprache – Analysemetriken

Wenn Sie [!UICONTROL Sprach- und ]) für [[!UICONTROL Anwendungsberichte]](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/app-reporting.md) aktivieren, werden die folgenden Metriken (und [Dimensionen](../dimensions/voice-dimensions.md)) erstellt. Sie können [Kontextdatenvariablen“ verwenden](/help/implement/vars/page-vars/contextdata.md) um sie auf einen Wert von `1` (oder ggf. auf mehr) festzulegen. Wenn diese Option in den Report Suite-Einstellungen aktiviert [, ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-overview.md) automatisch Verarbeitungsregeln erstellt, die Sprachanalysemetriken der zugehörigen Kontextdatenvariablen zuordnen.

| Metrikname | Beschreibung | Kontextdatenvariable |
| --- | --- | --- |
| Sprache – Äußerungen | Trigger, wenn ein Befehl an einen Sprachassistenten ausgegeben wird. | `a.voiceutterances` |
| Sprache – Sitzung beenden | Trigger beim Schließen der Sprach-App. | `a.voiceendsession` |
| Sprache – Fehler | Trigger, wenn in der Sprach-App ein Fehler auftritt. | `a.voiceerror` |

{style="table-layout:auto"}
