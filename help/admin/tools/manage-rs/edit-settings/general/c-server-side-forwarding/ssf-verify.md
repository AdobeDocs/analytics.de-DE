---
description: Um sicherzustellen, dass die Server-seitige Weiterleitung ordnungsgemäß aktiviert ist, müssen Sie die HTTP-Antwort aus der Analytics-Tracking-Anfrage überprüfen. Diese Anweisungen veranschaulichen, welche Indikatoren vorhanden sein müssen, um sicherzustellen, dass die Server-seitige Weiterleitung ordnungsgemäß aktiviert ist.
solution: Analytics
title: So überprüfen Sie die Implementierung der Server-seitigen Weiterleitung
feature: Report Suite Settings
exl-id: 21db4572-da3c-43aa-a774-86a089656695
role: Admin
TQID: 'https://experienceleague.adobe.com/FpB4dk9D87gc24t5KG6WRJ-r8GFOvOEUlRTTjc6XFYI'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
    internal-label: Admin Tools
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
    internal-label: Data configuration and collection
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
subfeature_v2:
  - id: c354699e-6555-4397-8706-1a9a89984069
    internal-label: Server side forwarding
  - id: fab61dd8-112a-4e5e-ad5f-fb0240b7a60b
    internal-label: Report Suite settings
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9a50beeb0aa51cf9f4baf212566947c14029ce8e
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 33%
---
# So überprüfen Sie die Implementierung der Server-seitigen Weiterleitung

Um sicherzustellen, dass die Server-seitige Weiterleitung ordnungsgemäß aktiviert ist, müssen Sie die HTTP-Antwort aus der Analytics-Tracking-Anfrage überprüfen. Dies kann mit den Entwickler-Tools eines Browsers oder mit einem Proxy-Tool wie Charles Web Debugger erfolgen. Die folgenden Anweisungen veranschaulichen, welche Indikatoren vorhanden sein müssen, um sicherzustellen, dass die Server-seitige Weiterleitung ordnungsgemäß aktiviert ist.

So überprüfen Sie den Status der Server-seitigen Weiterleitung:

1. Laden Sie eine Testseite, die aktualisierten AppMeasurement-Code enthält.
1. Überprüfen Sie in den Debugging-Tools Ihres Browsers oder mithilfe Ihrer Proxy-Software die HTTP-Antwort aus der Tracking-Anfrage von Analytics (Sie können diese einfach filtern, indem Sie einen beliebigen Pfad auswählen, der „b/ss“ enthält).
1. Überprüfen Sie die HTTP-Antwort. Wenn die Antwort Audience Manager-Daten enthält (wie unten dargestellt), funktioniert die Server-seitige Weiterleitung.

![](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/assets/ssf-succeed.png)

>[!CAUTION]
>
>Wenn die Antwort das Schlüssel/Wert-Paar „`"status":"SUCCESS"`“ oder ein 2-x-2-Bild enthält, ist die serverseitige Weiterleitung nicht korrekt konfiguriert. Stellen Sie sicher, dass der Identity Service ordnungsgemäß bereitgestellt ist, dass Sie das AppMeasurement-Modul bereitgestellt haben, dass die jeweilige Report Suite der korrekten Organisations-ID zugewiesen wurde und dass die Server-seitige Weiterleitung in den Analytics Admin Tools aktiviert wurde.

>[!MORELIKETHIS]
>
>* [Charles Web Debugger](https://www.charlesproxy.com/)
