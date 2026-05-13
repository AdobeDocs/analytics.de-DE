---
description: Interne URL-Filter identifizieren die Referrer, die Sie als interne Referrer Ihrer Site betrachten. Sie unterstützen Traffic-Quellen beim Ausfüllen von Daten und beim Filtern des internen Traffics.
title: Interne URL-Filter
feature: Admin Tools
uuid: 70868edb-208d-4dad-9401-70967468d40c
exl-id: fa387da2-e9be-47c0-9c4e-edd75af1f05a
TQID: https://experienceleague.adobe.com/J78ImTXRPFm6aMHqrxJXZOUVyG-ETnutipYYo2wrofc
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
subfeature_v2:
  - id: c80b99d6-98b9-4aeb-b5c4-933ef2ef705c
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 221
ht-degree: 2%

---

# Interne URL-Filter

Interne URL-Filter ermöglichen es Ihnen, die Referrer zu identifizieren, die Sie als intern für Ihre Site erachten. Sie unterstützen Traffic-Quellen beim Ausfüllen von Daten und beim Filtern des internen Traffics.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Interne URL-Filter]**

Eine verweisende Stelle oder verweisende Seite ist normalerweise die Seite, von der aus ein Besucher auf Ihre Website gelangt ist. Um Datenverfälschungen zu vermeiden, können Sie interne Referrer herausfiltern. Zu den Dimensionen, die auf internen URL[Filtern basieren, gehören &#x200B;](/help/components/dimensions/referrer.md)Referrer[&#x200B; „Referrer Domain](/help/components/dimensions/referring-domain.md), [Marketing-Kanäle](/help/components/dimensions/marketing-channel.md) und andere Dimensionen der Traffic-Quelle.

[Marketing-Kanal-Verarbeitungsregeln](../marketing-channels/mc-proc-rules.md) geben als mögliche Regelkriterien &quot;[!UICONTROL stimmt mit internen URL-Filtern überein] an.

>[!IMPORTANT]
>
>Einige Report Suites verfügen über einen standardmäßig konfigurierten internen URL-Filter eines Zeitraums (`.`). Wenn dieser Filter vorhanden ist, wird der gesamte Traffic als intern klassifiziert. Berichte zu Referrern funktionieren erst, nachdem dieser Filter entfernt und durch eine oder mehrere gewünschte interne Domains ersetzt wurde.

* Alle vorhandenen Filter im Abschnitt **[!UICONTROL Aktuelle Filter]** anzeigen.
* Fügen Sie mithilfe des Textfelds unter dem Abschnitt „Filter **[!UICONTROL &quot; einen Filter]** und klicken Sie dann auf **[!UICONTROL Hinzufügen]**.

Filter arbeiten mit **contains**-Logik für die vollständige URL. Adobe empfiehlt, beim Erstellen von Filtern Protokoll (`https://`) und Subdomains wegzulassen, es sei denn, Traffic von separaten Subdomains wird als externer Traffic gewünscht.
