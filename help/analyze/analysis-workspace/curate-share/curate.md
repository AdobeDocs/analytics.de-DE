---
description: Durch Kuratierung können Sie die Komponenten einschränken, bevor Sie ein Projekt freigeben.
keywords: Analysis Workspace-Kuratierung
title: Kuratieren von Projekten
feature: Curate and Share
role: User, Admin
exl-id: 5e23be83-586a-4543-9be9-65c631b8b0b7
source-git-commit: d7a6867796f97f8a14cd8a3cfad115923b329c7c
workflow-type: tm+mt
source-wordcount: '567'
ht-degree: 98%

---

# Kuratieren von Projekten

Mit der Kuratierung können Sie die Komponenten (Dimensionen, Metriken, Segmente, Datumsbereiche) vor der Freigabe eines Projekts einschränken. Wenn ein Empfänger das Projekt öffnet, wird ihm eine begrenzte Anzahl von Komponenten angezeigt, die Sie für ihn kuratiert haben. Die Kuratierung ist ein optionaler, aber empfehlenswerter Schritt, bevor Sie ein Projekt freigeben.

>[!NOTE]
> Produktprofile bestimmen als Hauptmechanismen, welche Komponenten ein Anwender sehen kann. Sie werden über die Adobe Experience Cloud Admin Console verwaltet. Kuratierung ist ein Sekundärfilter.


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Kuratieren von Projekten](https://video.tv.adobe.com/v/24711?quality=12&learn=on){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]


## Anwenden der Projektkuratierung

1. Klicken Sie auf **[!UICONTROL Freigeben]** > **[!UICONTROL Projektdaten kuratieren]**.
Die im Projekt verwendeten Komponenten werden automatisch hinzugefügt.
   **Hinweis**: Wenn ein Projekt mehrere Report Suites hat, wird für jede Report Suite im Projekt ein Feld zum Kuratieren angezeigt.
1. (Optional) Um weitere Komponenten hinzuzufügen, ziehen Sie die freizugebenden Komponenten aus der linken Leiste in das Feld [!UICONTROL Komponenten kuratieren].
1. Klicken Sie auf **[!UICONTROL Fertig]**.

Eine Kuratierung kann auch über das Menü [!UICONTROL Freigeben] angewendet werden, indem Sie auf **[!UICONTROL Kuratieren und freigeben]** klicken. Diese Option kuratiert das Projekt automatisch auf die im Projekt verwendeten Komponenten. Sie können weitere Komponenten hinzufügen, wie oben beschrieben.

![](assets/curation-field.png)

## Ansicht des kuratierten Projekts

Wenn ein Empfänger ein kuratiertes Projekt öffnet, wird ihm nur der ausgewählte Satz der von Ihnen definierten Komponenten angezeigt:

![](assets/curate-project.png)

## Entfernen der Projektkuratierung

So entfernen Sie die Projektkuratierung und stellen Sie den vollständigen Satz der Komponenten in der linken Leiste wieder her:

1. Klicken Sie auf **[!UICONTROL Freigeben]** > **[!UICONTROL Projektdaten kuratieren]**.
1. Klicken Sie auf **[!UICONTROL Kuratierung entfernen]**.
1. Klicken Sie auf **[!UICONTROL Fertig]**.

## Kuratierung einer Virtual Report Suite

Um die Kuratierung auf Report Suite-Ebene anzuwenden, sodass sie für viele Projekte gleichzeitig gilt, können Sie Komponenten in einer [Virtual Report Suite kuratieren](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-components.html?lang=de).

>[!NOTE]
> Die Kuratierung einer Virtual Report Suite wird immer vor der Projektkuratierung ausgeführt. Das bedeutet, dass selbst dann, wenn Ihr kuratiertes Projekt bestimmte Komponenten enthält, diese herausgefiltert werden, wenn die kuratierte Virtual Report Suite diese nicht enthält.

## Option „Alle anzeigen“ für Komponenten

In einem kuratierten Projekt oder einer Virtual Report Suite wird der Empfängerin bzw. dem Empfänger die Option **[!UICONTROL Alle anzeigen]** für Komponenten in der linken Leiste angezeigt. [!UICONTROL Alle anzeigen] zeigt verschiedene Komponentensätze an, je nach:

* Berechtigungsebene der Person (Admin oder Nicht-Admin)
* Projektrolle (Inhaber/Bearbeiter oder nicht)
* Art der angewendeten Kuratierung (Virtual Report Suite oder Projekt)
* Komponenten, die dem Benutzer gehören oder für ihn freigegeben wurden. Zu den eigenen/freigegebenen Komponenten gehören Segmente, berechnete Kennzahlen und Datumsbereiche. Sie enthalten keine implementierten Komponenten wie eVars, Props und benutzerdefinierte Ereignisse.

Hinweis: Rollen ohne Administratoransicht haben keinen Zugriff auf die linke Leiste in einem Projekt, daher wurden sie in der unten stehenden Tabelle weggelassen.

| Kuratierungstyp | Admins | Inhaber- oder Bearbeiterrolle, kein Admin | Duplizierte Rolle „Nicht-Administrator“ |
|---|---|---|---|
| Kuratierte Virtual Report Suite | Alle nicht kuratierten Komponenten der Virtual Report Suite | Nicht kuratierte Virtual Report Suite- und Projektkomponenten, die dieser Rolle gehören oder die für diese Rolle freigegeben wurden | Nicht kuratierte Virtual Report Suite- und Projektkomponenten, die dieser Rolle gehören oder die für diese Rolle freigegeben wurden |
| Kuratierte Projekte | Alle nicht kuratierten Projektkomponenten | Alle nicht kuratierten Projektkomponenten | Nicht kuratierte Projektkomponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden |
| Kuratierte Projekte in einer kuratierte Virtual Report Suite | Alle nicht kuratierten Komponenten, aufgeführt unter **[!UICONTROL Nicht kuratierte Projektkomponenten]** und **[!UICONTROL Nicht kuratierte Virtual Report Suite-Komponenten]** | Alle nicht kuratierten Projektkomponenten UND nicht kuratierten Komponenten der Virtual Report Suite, die dieser Rolle gehören oder die für diese Rolle freigegeben wurden | Nicht kuratierte Virtual Report Suite- und Projektkomponenten, die dieser Rolle gehören oder die für diese Rolle freigegeben wurden |
