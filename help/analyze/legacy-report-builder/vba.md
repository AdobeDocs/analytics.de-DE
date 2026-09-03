---
title: Verwenden von Visual Basic-Makros in Report Builder
description: Erfahren Sie, wie Sie die Funktionalität von Excel-Arbeitsmappen und Report Builder mithilfe von VBA-Makros erweitern können.
feature: Report Builder
role: User, Admin
exl-id: 0d92bce2-22ae-4b0c-af1d-3d12f2041ddf
TQID: https://experienceleague.adobe.com/RxOpojtJn2vi5uMO8CGzCCm7FcPp4qVwbH-XTEBSRsY
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 195
ht-degree: 64%

---

# Visual Basic-Makros in Report Builder

{{legacy-arb}}

Visual Basic (VBA)-Makros bieten Features, mit denen Sie Excel-Arbeitsmappen aktualisieren können. Visual Basic hat Zugriff auf die Arbeitsmappe, Excel und Windows.

Sie müssen die neueste Version von Report Builder ausführen und sich anmelden, bevor Sie VBA-Makros ausführen.

>[!IMPORTANT]
>
>Aus Sicherheitsgründen ist es nicht möglich, eine Arbeitsmappe mit einem Makro zu planen.

Adobe unterstützt drei Report Builder-API-Methoden.

## `RefreshAllReportBuilderRequests()`

Das `RefreshAllReportBuilderRequests()`-Makro aktualisiert alle Report Builder-Anforderungen in der aktiven Arbeitsmappe. Zunächst wird das COM-Add-In von Report Builder über seine Produkt-ID und anschließend der `RefreshAllRequests()`-API-Befehl aufgerufen:

```vba
Sub RefreshAllReportBuilderRequests()
 
 Dim addIn As COMAddIn
 Dim automationObject As Object
 Dim success As String
 Set addIn = Application.COMAddIns("ReportBuilderAddIn.Connect")
 Set automationObject = addIn.Object
 success = automationObject.RefreshAllRequests(ActiveWorkbook)
 
End Sub
```

## `RefreshAllReportBuilderRequestsInActiveWorksheet()`

Das `RefreshAllReportBuilderRequestsInActiveWorksheet()`-Makro aktualisiert alle Report Builder-Anforderungen im aktiven Arbeitsblatt. Der `RefreshWorksheetRequests()`-API-Aufruf verwendet ein Arbeitsblattobjekt als Argument. Sie können diesen Aufruf für jedes Arbeitsblatt verwenden, das Report Builder-Anforderungen enthält:

```vba
Sub RefreshAllReportBuilderRequestsInActiveWorksheet()
 
 Dim addIn As COMAddIn
 Dim automationObject As Object
 Dim success As String
 Set addIn = Application.COMAddIns("ReportBuilderAddIn.Connect")
 Set automationObject = addIn.Object
 success = automationObject.RefreshWorksheetRequests(ActiveWorkbook.ActiveSheet)
 
End Sub
```

## `RefreshAllReportBuilderRequestsInCellsRange()`

Das `RefreshAllReportBuilderRequestsInCellsRange()`-Makro aktualisiert alle Report Builder-Anforderungen, deren Zellenausgabe den angegebenen Zellbereich überschneidet. Der in diesem Beispiel verwendete Zellbereich verweist auf den Bereich `B1:B54` des „Data“-Arbeitsblatts in der aktiven Arbeitsmappe. Der Bereichsausdruck unterstützt alle unterstützten Bereichsausdrücke in Excel:

```vba
Sub RefreshAllReportBuilderRequestsInCellsRange()
 
 Dim addIn As COMAddIn
 Dim automationObject As Object
 Dim success As String
 Set addIn = Application.COMAddIns("ReportBuilderAddIn.Connect")
 Set automationObject = addIn.Object
 success = automationObject.RefreshRequestsInCellsRange("'Data'!B1:B54")
  
End Sub
```
