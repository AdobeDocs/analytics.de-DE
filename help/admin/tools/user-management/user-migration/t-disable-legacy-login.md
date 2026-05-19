---
description: Erfahren Sie, wie Sie veraltete Anmeldedaten für Analytics-Benutzer deaktivieren.
title: Deaktivieren von veralteten Anmeldedaten
feature: Admin Tools
exl-id: 3e619700-722d-429b-94dc-7aa162e114c0
role: Admin
TQID: https://experienceleague.adobe.com/xwLXKuaeoKB5-TSVC7FLQXdUsBEeOg-zuITMa8Z3OIo
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 7d733a6375f6c6009563bc53f5a3ff090dbc48ed
workflow-type: tm+mt
source-wordcount: 185
ht-degree: 52%

---

# Deaktivieren von veralteten Anmeldedaten

Erfahren Sie, wie Sie veraltete Anmeldedaten für Analytics-Benutzer deaktivieren.

Nachdem Ihre Benutzerinnen und Benutzer vom bisherigen Analytics-Benutzerverwaltungssystem zum Adobe Admin Console migriert haben, können Sie ihre bisherigen Anmeldedaten deaktivieren. Durch Deaktivieren von Legacy-Anmeldungen werden Benutzer zur CX Enterprise-Anmeldung weitergeleitet, wenn sie versuchen, die Legacy-Anmeldung zu verwenden.

1. Öffnen Sie das Migrationstool in **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Benutzer-ID-Migration]**.
1. Suchen Sie im Abschnitt „[!DNL User Information]“ nach der Domain mit den Benutzern, mit denen Sie arbeiten möchten, und klicken Sie dann auf **[!UICONTROL Benutzer auswählen]**.
1. Wählen Sie die Benutzer mit bisherigen Anmeldedaten aus, die Sie deaktivieren möchten.

   ![](/help/admin/tools/user-management/user-migration/assets/user-info.png)

   Die Benutzer, die berechtigt sind, haben in der Spalte „Migrationsstatus“ den Status *`Migrated`*. Sie können die bisherigen Anmeldedaten von Benutzern erst deaktivieren, wenn sie migriert wurden.
1. Klicken Sie auf **[!UICONTROL Bisherige Anmeldedaten deaktivieren]** und dann auf **[!UICONTROL Fertig]**.

   „Bisherige Anmeldedaten deaktivieren“ gibt an, welcher Ihrer Benutzer seinen alten [!DNL my.omniture.com]-Benutzernamen und sein Passwort weiterhin verwenden kann.

   Sie können keine veralteten Anmeldedaten für Benutzende deaktivieren, die noch migriert werden müssen. Nach der Deaktivierung müssen sich Benutzende mit ihrer Experience Cloud-ID anmelden und auf Analytics zugreifen.
