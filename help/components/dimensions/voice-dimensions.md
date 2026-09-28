---
title: Voice Analytics-Dimensionen
description: Voice Analytics-Dimensionen
feature: Dimensions
exl-id: 6e1275c4-3b17-4c65-a308-d420ea1acdf6
TQID: 'https://experienceleague.adobe.com/OZ-lQkbS8hsv8ywUUa2BQoH40nfklRkJNd9SlEVkmEI'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
    internal-label: Data configuration and collection
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
  - id: b22bc0f7-b089-4966-95a1-31e7b3b69b79
    internal-label: Dimensions
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
source-git-commit: 9a50beeb0aa51cf9f4baf212566947c14029ce8e
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 16%
---
# Voice Analytics-Dimensionen

Wenn Sie [!UICONTROL Sprach- und &#x200B;]) für [[!UICONTROL Anwendungsberichte]](/help/admin/tools/manage-rs/edit-settings/app-reporting.md) aktivieren, werden die folgenden Dimensionen (und [Metriken](../metrics/voice-metrics.md)) erstellt. Sie können [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md) verwenden, um sie auf den gewünschten Zeichenfolgenwert festzulegen. Wenn diese Option in den Report Suite[Einstellungen aktiviert ist, &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md) automatisch Verarbeitungsregeln erstellt, die Sprachanalysedimensionen der zugehörigen Kontextdatenvariablen zuordnen.

| Name der Dimension | Beschreibung | Kontextdatenvariable |
| --- | --- | --- |
| Voice-Fehlertyp | Der Typ des aufgetretenen Fehlers. | `a.voiceerrortype` |
| Voice-Sprache | Die Sprache, in der der Benutzer mit Ihrer Sprach-App interagiert. | `a.voicelanguage` |
| Voice-Absicht | Der Befehl, den der Benutzer ausführen möchte. | `a.voiceintent` |
| Voice-App-Antwort | Die Antwort, die die Sprach-App an den Benutzer zurückgegeben hat. | `a.voiceappresponse` |
| Sprach-Authentifizierung | Der authentifizierte Status des Benutzers bei der Interaktion mit der Sprach-App. | `a.voiceauthentication` |
| Zielpunkt-ID | Die Point of Interest-ID. | `a.loc.poi.id` |

{style="table-layout:auto"}
