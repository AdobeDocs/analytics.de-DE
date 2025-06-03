---
description: Anweisungen zum Auffinden Ihrer Konto-IDs für Google Ads und Microsoft Advertising.
title: Konto-IDs suchen
feature: Advertising Analytics
exl-id: 2faccfd1-df7b-4b0c-a2f3-23138c39a838
source-git-commit: 586459d99674f01a3b18f84f975a3365ddf2fcd9
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 3%

---

# Konto-IDs suchen {#locate-your-account-ids}

Erfahren Sie, wie Sie Ihre Konto-IDs für Google Ads und Microsoft Advertising finden.

## Google Ads (AdWords) {#google}

>[!IMPORTANT]
>
>Google Ads verwendet zwei Kontotypen:
>
>- MCC-Konto (My Client Center) und
>- Standardkonto.
>
>Für diese Integration mit Adobe Analytics **Sie müssen eine Standardkonto-Anmeldung verwenden** keine MCC-Konto-Anmeldung. Dies liegt daran, dass ein MCC-Konto als „Übersichtskonto“ dient, das mit einer einzigen Anmeldung auf mehrere Google Ads-Konten zugreifen kann, während die Standardkonto-Anmeldung pro Anmeldung nur auf ein Konto zugreifen kann. Google unterstützt zwar die Verknüpfung einer E-Mail mit fünf Konten, Advertising Analytics unterstützt diese Funktion jedoch noch nicht. Eine E-Mail kann nur mit einem Google Ads-Konto verknüpft werden.

Klicken Sie auf das Konto-Symbol oben rechts, um die Google Ads-Kontonummer (Kunden-ID) anzuzeigen.

![Google Ads Manager-Konto](assets/google-account.png)

## Microsoft Advertising (Bing) {#microsoft}

>[!NOTE]
>
>Wenn Ihr Microsoft Advertising-Konto (früher als Bing bezeichnet) die Google-Importfunktion verwendet, stellen Sie sicher, dass Sie die richtige Tracking-Zeichenfolge aktualisieren. Die Tracking-Zeichenfolge wird nicht automatisch von der Google-Version auf die richtige Tracking-Zeichenfolge für Microsoft Advertising aktualisiert, was zu nicht spezifizierten Daten führen kann. Weitere Informationen finden Sie [Was aus Google Ads importiert wird](https://help.ads.microsoft.com/apex/index/3/en/50851/) in der Hilfe zu Microsoft Advertising .

Die **[!UICONTROL Konto-ID]** und **[!UICONTROL Manager-Konto-ID]** sind beide erforderlich.

- Die **[!UICONTROL Konto-ID]** befindet sich unter **[!UICONTROL Einstellungen]** > **[!UICONTROL Kontoeinstellungen]** > **[!UICONTROL Konto-ID]**. Stellen Sie sicher, dass Sie [!UICONTROL Konto-ID] und NICHT [!UICONTROL Kontonummer] verwenden.
- Die **[!UICONTROL Manager-Konto]** ID) befindet sich unter **[!UICONTROL Einstellungen]** > **[!UICONTROL Manager-Kontoeinstellungen]** > **[!UICONTROL Manager-Konto-ID]**. Stellen Sie sicher, dass Sie [!UICONTROL Manager-Konto-ID] und NICHT [!UICONTROL Manager-Kontonummer] verwenden.

![Microsoft Advertising-Navigation](assets/bing-id.png)

>[!CONTEXTUALHELP]
>id="adanalytics_ma_account_id"
>title="Konto-ID"
>abstract="Die „Konto-ID“ ist ein numerischer Wert in der Benutzeroberfläche von Microsoft Advertising. Sie können sie finden, indem Sie zu Einstellungen > Kontoeinstellungen > Konto-ID navigieren."

>[!CONTEXTUALHELP]
>id="adanalytics_ma_manager_account_id"
>title="Manager-Konto-ID"
>abstract="Die „Manager-Konto-ID“ ist ein numerischer Wert in der Benutzeroberfläche von Microsoft Advertising. Sie können sie finden, indem Sie zu Einstellungen > Manager-Kontoeinstellungen > Manager-Konto-ID navigieren."
