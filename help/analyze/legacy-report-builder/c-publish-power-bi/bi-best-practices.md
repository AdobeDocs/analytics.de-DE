---
description: Best Practices für Power BI.
title: Best Practices
feature: Report Builder
role: User, Admin
exl-id: 2d9447f4-77ac-465b-af93-206dc3ea80f7
source-git-commit: ae6ffed05f5a33f032d0c7471ccdb1029154ddbd
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 100%

---

# Best Practices

{{legacy-arb}}

## Beibehalten von Referenzen in Power BI-Visualisierungen

Wenn Sie eine Anforderung erstellen, besitzt diese Anforderung immer die gleiche Referenz in Power BI. Wenn Sie jedoch eine Anforderung löschen, wird die Referenz von einer neuen Anforderung verwendet, die Sie für die gleiche Dimension erstellen.

Wenn Sie eine Anfrage in Ihrer Arbeitsmappe löschen, stellen Sie sicher, dass in Power BI keine Visualisierung auf diese Anfrage verweist, da die Visualisierung dadurch beschädigt wird.

* Sofern möglich, löschen Sie keine Anforderungen, die Sie in Report Builder erstellt haben.
* Wenn Sie Anforderungen in Report Builder löschen müssen, löschen Sie auch die entsprechenden Visualisierungen in Power BI.
* Wenn Sie nicht sicher sind, löschen Sie die Anforderungen, die Sie nicht mehr benötigen, führen Sie eine erneute Veröffentlichung durch und wechseln Sie zu Power BI, um festzustellen, welche Visualisierungen beschädigt wurden.
