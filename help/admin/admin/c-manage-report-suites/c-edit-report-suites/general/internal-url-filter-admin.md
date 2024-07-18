---
description: Mit internen URL-Filtern werden die Referrer, die Sie als seitenintern betrachten, gekennzeichnet. Dies hilft, Berichte zu Traffic-Quellen mit Daten zu füllen und internen Traffic zu filtern.
title: Interne URL-Filter
feature: Admin Tools
uuid: 70868edb-208d-4dad-9401-70967468d40c
exl-id: fa387da2-e9be-47c0-9c4e-edd75af1f05a
source-git-commit: 5c2643a143e5c8e17fcf11cfa2da81183bc5c39a
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 31%

---


# Interne URL-Filter

Mit internen URL-Filtern können Sie die Referrer identifizieren, die Sie als intern für Ihre Site betrachten. Dies hilft, Berichte zu Traffic-Quellen mit Daten zu füllen und internen Traffic zu filtern.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Interne URL-Filter]**

Ein Referrer oder eine verweisende Seite ist normalerweise die Seite, von der aus Besucher Ihre Website aufgerufen haben. Um Datenverzerrungen zu vermeiden, können Sie interne Seiten als Referrer herausfiltern. Zu den Dimensionen, die auf interne URL-Filter angewiesen sind, zählen [Referrer](/help/components/dimensions/referrer.md), [Referrer-Domäne](/help/components/dimensions/referring-domain.md), [Marketing-Kanäle](/help/components/dimensions/marketing-channel.md) und andere Traffic-Quelldimensionen.

[Verarbeitungsregeln für Marketing-Kanäle](../marketing-channels/c-rules.md) stellen als Regelkriterium &quot;[!UICONTROL Entspricht internen URL-Filtern]&quot;bereit.

>[!IMPORTANT]
>
>Einige Report Suites verfügen über einen internen URL-Filter für einen Zeitraum (`.`), der standardmäßig konfiguriert ist. Wenn dieser Filter vorhanden ist, wird der gesamte Traffic als intern klassifiziert. Berichte der verweisenden Stelle funktionieren erst, wenn dieser Filter entfernt und durch eine oder mehrere gewünschte interne Domänen ersetzt wurde.

* Zeigen Sie alle vorhandenen Filter im Abschnitt **[!UICONTROL Aktuelle Filter]** an.
* Fügen Sie mithilfe des Textfelds unter dem Abschnitt **[!UICONTROL Filter hinzufügen]** einen Filter hinzu und klicken Sie dann auf **[!UICONTROL Hinzufügen]** .

Filter werden mit der Logik **contains** gegen die vollständige URL ausgeführt. Adobe empfiehlt, beim Erstellen von Filtern das Nichtberücksichtigungsprotokoll (`https://`) und die Subdomänen wegzulassen, es sei denn, der Traffic von separaten Subdomänen ist als externer Traffic erwünscht.
