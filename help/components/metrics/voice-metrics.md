---
title: Sprache – Analysemetriken
description: Sprache – Analysemetriken
feature: Metrics
exl-id: 3c1b4e4e-d8d2-446f-9582-a2ce5580a8d3
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 21%

---

# Sprache – Analysemetriken

Wenn Sie [!UICONTROL Sprach- und &#x200B;]) für [[!UICONTROL Anwendungsberichte]](/help/admin/tools/manage-rs/edit-settings/app-reporting.md) aktivieren, werden die folgenden Metriken (und [Dimensionen](../dimensions/voice-dimensions.md)) erstellt. Sie können [Kontextdatenvariablen“ verwenden](/help/implement/vars/page-vars/contextdata.md) um sie auf einen Wert von `1` (oder ggf. auf mehr) festzulegen. Wenn diese Option in den Report Suite-Einstellungen aktiviert [, &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md) automatisch Verarbeitungsregeln erstellt, die Sprachanalysemetriken der zugehörigen Kontextdatenvariablen zuordnen.

| Metrikname | Beschreibung | Kontextdatenvariable |
| --- | --- | --- |
| Sprache – Äußerungen | Trigger, wenn ein Befehl an einen Sprachassistenten ausgegeben wird. | `a.voiceutterances` |
| Sprache – Sitzung beenden | Trigger beim Schließen der Sprach-App. | `a.voiceendsession` |
| Sprache – Fehler | Trigger, wenn in der Sprach-App ein Fehler auftritt. | `a.voiceerror` |

{style="table-layout:auto"}
