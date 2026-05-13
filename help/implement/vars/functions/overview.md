---
title: Funktionen und Methoden
description: Erfahren Sie, wie Sie die Funktionen und Methoden verwenden können, die Adobe in Ihrer Implementierung anbietet.
feature: Appmeasurement Implementation
exl-id: 9ef5bd92-fae1-4fe4-90ea-c735e8ff4b9c
role: Admin, Developer
TQID: https://experienceleague.adobe.com/dKPvTPeRa7-SIFyIDU-7Mlob-3jsrfvhWmKeAveHGEc
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: c069c44e-5426-4c1a-accc-8028662f2fde
  - id: c8add8f2-4250-4fd9-9cde-9707036c567d
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 142
ht-degree: 100%

---

# Funktionen und Methoden

Adobe bietet verschiedene Funktionen und Methoden an, die Sie bei Ihrer Implementierung verwenden können. Wenn Sie auf diese Funktionen oder Methoden verweisen, führen diese gewöhnliche Aufgaben mit einer einzelnen Codezeile aus.

Einige dieser Codezeilen gehören zu folgenden Kategorien:

* **Tracking-Aufrufe**: Die gängigsten Methoden und in vielen Implementierungen besonders wichtig. Dazu gehören die Methoden [`t()`](t-method.md) und [`tl()`](tl-method.md).
* **AppMeasurement-Dienstprogramme**: In früheren Versionen von AppMeasurement mussten Implementierungen ihren eigenen Code schreiben, um diese Aufgaben durchzuführen. Adobe stellt diese Dienstprogrammmethoden bereit, um diese gängigen Aufgaben zu optimieren. AppMeasurement-Dienstprogramme umfassen [`Util.cookieRead()`](util-cookieread.md), [`Util.cookieWrite()`](util-cookiewrite.md) und [`Util.getQueryParam()`](util-getqueryparam.md).
* **Registrierfunktionen**: Sie können eigene Funktionen schreiben und von AppMeasurement automatisch ausführen lassen, bevor oder nachdem Sie einen Tracking-Aufruf an Adobe senden. Variablen, die unter diese Kategorie fallen, sind [`doPlugins()`](doplugins.md), [`registerPreTrackCallback()`](registerpretrackcallback.md) und [`registerPostTrackCallback()`](registerposttrackcallback.md).
