---
description: Adobe Report Builder bietet jetzt Berechtigungseinstellungen, die denjenigen der Admin Tools von Analytics entsprechen.
title: Benutzerzugriffsberechtigungen für Dimensionen und Metriken
uuid: b561407d-c4fa-4f1e-8b16-5ca46fcbf36f
feature: Report Builder
role: User, Admin
exl-id: 53cfdcf4-31c3-40ab-aca4-8f0f9be6fe13
TQID: https://experienceleague.adobe.com/p-nsvA1hqNBbwXesj5cumraamq2nEk1zVHgbby-XwEA
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 45%

---

# Benutzerzugriffsberechtigungen für Dimensionen und Metriken

{{legacy-arb}}

Adobe Report Builder verfügt über Berechtigungseinstellungen, die denen der Analytics Admin Tools ähneln.

Als Benutzer ohne Administratorrechte haben Sie möglicherweise zuvor Arbeitsmappen mit Anfragen erstellt, die auf Dimensionen und Metriken verweisen, auf die Sie keinen Zugriff haben. Diese Berechtigungen werden jetzt erzwungen.

Wenn Sie beispielsweise eine Anfrage aktualisieren, die Dimensionen oder Metriken enthält, auf die Sie keinen Zugriff haben, wird der Berechtigungsfehler eingeschränkt angezeigt. Die Fehlermeldung besagt, dass eine Anfrage aufgrund von Administratorberechtigungen für Ihr Benutzerkonto nicht verfügbar ist.

![Screenshot mit der Fehlermeldung „Eingeschränkte Berechtigung“.](assets/arb_restrc_perm.png)

Befolgen Sie diese Anweisungen für **jede** Report Builder-Arbeitsmappe, die Sie pflegen:

1. Öffnen Sie die Arbeitsmappe.
1. Alle Anfragen aktualisieren.
1. Wenn Sie aufgrund einer Benutzerzugriffsberechtigung aufgefordert werden, klicken Sie auf **[!UICONTROL CSV-Datei öffnen]** um Zugriff auf die Liste der Fehler mit eingeschränkten Berechtigungen zu erhalten.
1. Erstellen Sie eine Datei mit dem Namen „AllRestrictedPermissionErrors.xlsx“ und kopieren Sie die Liste mit den Fehlern wegen eingeschränkter Berechtigungen aus der CSV-Datei und fügen Sie sie in diese Datei ein.
1. Schließen Sie die Report Builder-Arbeitsmappe.

Wenn Sie alle Arbeitsmappen verarbeitet haben, sollten Sie über eine umfassende Liste mit Fehlern wegen eingeschränkter Berechtigungen in „AllRestrictedPermissionErrors.xlsx“ verfügen. Senden Sie diese Liste an Ihren für den Benutzerzugriff zuständigen Adobe Analytics-Administrator und ersuchen Sie um Zugriff auf die Metriken und Dimensionen.
