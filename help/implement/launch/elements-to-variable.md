---
title: Zuordnen von Tag-Datenelementen zu Analytics-Variablen
description: Weisen Sie den Analytics-Variablen Datenelemente zu, damit Sie sie als Dimensionen in Analysis Workspace verwenden können.
feature: Tags
exl-id: 996c1204-3f8a-453e-8104-5e8e1279517c
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/-eif71BEIQnPRQWSaXK5Wb5WL0rTROwRDDxzbUNL98I'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: df312454-73c4-43f6-a90e-18f5043f074c
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 448
ht-degree: 96%

---

# Zuordnen von Tag-Datenelementen zu Analytics-Variablen

Sobald Sie über ein Repository mit Tag-Datenelementen verfügen, können Sie sie Analytics-Dimensionen zuweisen.

## Voraussetzungen

[Zuordnen von Datenschichtobjekten zu Datenelementen](layer-to-elements.md): Vergewissern Sie sich, dass Sie Tag-Datenelemente verstehen und mehrere davon zur Verfügung haben.

[Erstellen Sie ein Lösungs-Design-Dokument](../prepare/solution-design.md): Ein Lösungs-Design-Dokument ist für eine übersichtliche Organisation unverzichtbar. Wenn Sie Ihrem Lösungs-Design-Projekts folgen, wird die Zuweisung von Datenelementen zu Analytics-Variablen einfacher.

## Zuweisen von Datenelementen zu Analytics-Variablen

Wenn Sie eine Tag-Bibliothek veröffentlichen, nachdem Sie diese Schritte ausgeführt haben, können Sie benutzerdefinierte Dimensionen in Analysis Workspace verwenden. Sie können Analytics-Variablen global oder in einzelnen Regeln festlegen.

### Globale Variablen festlegen

Globale Variablen eignen sich ideal, wenn Sie Variablenwerte auf allen Seiten festlegen möchten, auf denen Ihr Datenelement vorhanden ist.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Klicken Sie auf die Registerkarte [!UICONTROL Erweiterungen] und dann unter „Adobe Analytics“ auf [!UICONTROL Konfigurieren].
1. Klicken Sie auf das Akkordeon [!UICONTROL Globale Variablen]. Daraufhin wird die Benutzeroberfläche zum Zuweisen globaler Variablen angezeigt.

### Variablen in Regeln festlegen

Die in Regeln festgelegten Variablen sind optimal, wenn Sie nicht möchten, dass Variablen auf jeder Seite festgelegt werden. Sie definieren die Kriterien in der Regel. Siehe [Regeln](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html?lang=de) in der Dokumentation zu Adobe Experience Platform-Tags.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Klicken Sie auf die Registerkarte [!UICONTROL Regeln] und dann auf die gewünschte Regel (oder erstellen Sie eine).
1. Klicken Sie auf die Schaltfläche [!UICONTROL Hinzufügen] unter [!UICONTROL Aktionen].
1. Legen Sie [!UICONTROL &#x200B; Dropdown]Liste „Erweiterung“ auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf Variablen fest.
1. Klicken Sie auf das Symbol ![Datenelement](assets/data-element.png) rechts neben der gewünschten Analytics-Variable. Das [Lösungs-Design-Dokument](../prepare/solution-design.md) Ihres Unternehmens bestimmt, welche Analytics-Variable verwendet werden soll.
1. Wählen Sie im modalen Fenster das gewünschte Datenelement aus. Klicken Sie auf [!UICONTROL Auswählen].
1. Der Name des Datenelements wird dem Textfeld, das von `%`-Zeichen eingeschlossen ist, hinzugefügt. Wenn Sie Ihr Datenelement beispielsweise „Seitenname“ nennen, wird die Zeichenfolge `%Page name%` angezeigt, wenn Sie einer Variablen ein Datenelement zuweisen.

>[!TIP]
>
>Sie können Datenelemente in derselben Variablen verketten. Wenn Sie beispielsweise das Datenelement „Hostname“ und das Datenelement „Pathname“ haben, können Sie beide durch `%Hostname%%Pathname%` in einer einzigen Variablen kombinieren.

## Nächste Schritte

[Seitenvariablen](../vars/page-vars/page-variables.md): Erfahren Sie, welche Seitenebenenvariablen Sie in Ihrer Implementierung verwenden können, um die Dimensionen in Analysis Workspace optimal zu nutzen.

[Konfigurationsvariablen](../vars/config-vars/configuration-variables.md): Erfahren Sie, welche Konfigurationsvariablen Sie in Ihrer Implementierung verwenden können, um weitere Funktionen in Adobe Analytics zu verwenden.
