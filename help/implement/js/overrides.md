---
title: Variablenüberschreibungen
description: Durch das Überschreiben von Variablen können Sie den Wert einer Variablen für einen einzelnen Verfolgungs- oder Verfolgungslinkaufruf ändern.
feature: Implementation Basics
exl-id: e297ef94-c5f7-42b1-a9d0-57e073f0d1a9
role: Developer
TQID: 'https://experienceleague.adobe.com/IVA-JMaZPrKpF1NhhL6o3uiCQOOCtZerk78aQTqJAyc'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 106
ht-degree: 100%

---

# Variablenüberschreibungen

Mit Variablenüberschreibungen können Sie Analytics-Werte für einen einzelnen Treffer ändern, ohne dass sich dies auf vorhandene Variablen auf der Seite auswirkt.

## Workflow

1. Erstellen Sie ein neues JavaScript-Objekt. Der Objektname kann beliebig sein.

   ```js
   var y = new Object();
   ```

2. Weisen Sie diesem Objekt gültige Analytics-Eigenschaften zu:

   ```js
   y.eVar1 = "New value";
   y.events = "event2";
   ```

3. Verwenden Sie das Objekt als Argument innerhalb des entsprechenden Tracking-Aufrufs:

   ```js
   // Use the override object in a standard page view call
   s.t(y);
   
   // Use the override object in a link tracking call
   s.tl(this,'o','Example override link',y);
   ```

Wenn ein Tracking-Aufruf ein Objekt im Überschreibungsparameter empfängt, überschreiben alle gültigen Werte im Überschreibungsobjekt die Werte im standardmäßigen Analytics-Objekt. Bereits in Ihrem vorhandenen Analytics-Objekt definierte Variablen sind davon nicht betroffen.
