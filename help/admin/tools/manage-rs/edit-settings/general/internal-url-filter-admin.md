---
description: Mit internen URL-Filtern werden die Referrer, die Sie als seitenintern betrachten, gekennzeichnet. Dies hilft, Berichte zu Traffic-Quellen mit Daten zu füllen und internen Traffic zu filtern.
title: Interne URL-Filter
feature: Admin Tools
uuid: 70868edb-208d-4dad-9401-70967468d40c
exl-id: fa387da2-e9be-47c0-9c4e-edd75af1f05a
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 31%

---


# Interne URL-Filter

Interne URL-Filter ermöglichen es Ihnen, die Referrer zu identifizieren, die Sie als intern für Ihre Site erachten. Dies hilft, Berichte zu Traffic-Quellen mit Daten zu füllen und internen Traffic zu filtern.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Interne URL-Filter]**

Ein Referrer oder eine verweisende Seite ist normalerweise die Seite, von der aus Besucher Ihre Website aufgerufen haben. Um Datenverzerrungen zu vermeiden, können Sie interne Seiten als Referrer herausfiltern. Zu den Dimensionen, die auf internen URL[Filtern basieren, gehören &#x200B;](/help/components/dimensions/referrer.md)Referrer[&#x200B; „Referrer Domain](/help/components/dimensions/referring-domain.md), [Marketing-Kanäle](/help/components/dimensions/marketing-channel.md) und andere Dimensionen der Traffic-Quelle.

[Marketing-Kanal-Verarbeitungsregeln](../marketing-channels/c-rules.md) geben als mögliche Regelkriterien &quot;[!UICONTROL stimmt mit internen URL-Filtern überein] an.

>[!IMPORTANT]
>
>Einige Report Suites verfügen über einen standardmäßig konfigurierten internen URL-Filter eines Zeitraums (`.`). Wenn dieser Filter vorhanden ist, wird der gesamte Traffic als intern klassifiziert. Berichte zu Referrern funktionieren erst, nachdem dieser Filter entfernt und durch eine oder mehrere gewünschte interne Domains ersetzt wurde.

* Alle vorhandenen Filter im Abschnitt **[!UICONTROL Aktuelle Filter]** anzeigen.
* Fügen Sie mithilfe des Textfelds unter dem Abschnitt „Filter **[!UICONTROL &quot; einen Filter]** und klicken Sie dann auf **[!UICONTROL Hinzufügen]**.

Filter arbeiten mit **contains**-Logik für die vollständige URL. Adobe empfiehlt, beim Erstellen von Filtern Protokoll (`https://`) und Subdomains wegzulassen, es sei denn, Traffic von separaten Subdomains wird als externer Traffic gewünscht.
