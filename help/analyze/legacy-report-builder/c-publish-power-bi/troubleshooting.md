---
description: Häufige Probleme bei der Verwendung von Report Builder mit Power BI.
title: Fehlerbehebung für die Power BI-Integration
feature: Report Builder
role: User, Admin
exl-id: adb13a0e-99fb-48f5-add2-204d155e467f
source-git-commit: bb908f8dd21f7f11d93eb2e3cc843f107b99950d
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 64%

---

# Fehlerbehebung für die Power BI-Integration

Ermitteln und Lösen von allgemeinen Problemen bei der Verwendung von Report Builder mit Power BI.

## Fehlschlagen der Veröffentlichung in Power BI

Geplante Arbeitsmappen, die in Power BI veröffentlicht werden sollen, hängen davon ab, dass Power BI-Dienste ausgeführt werden. Zwei Hauptgründe für das Fehlschlagen einer Veröffentlichung sind:

* Power BI-Dienste werden nicht ausgeführt.
* Der Benutzer, der die Veröffentlichung der Arbeitsmappe geplant hat, besitzt keine gültigen Microsoft-Kontoanmeldedaten mehr.

Für jede geplante Report Builder-Aufgabe werden drei Versuche pro geplanter Ausführung durchgeführt:

* Nach dem ersten erfolglosen Versuch wird eine Fehlermeldung mit dem folgenden Wortlaut angezeigt: „Diese geplante Arbeitsmappe konnte nicht in Microsoft Power BI veröffentlicht werden. Ein neuer Versuch erfolgt in Kürze.“
* Nach dem zweiten erfolglosen Versuch wird keine Meldung angezeigt.
* Nach dem dritten erfolglosen Versuch wird eine Fehlermeldung mit dem folgenden Wortlaut angezeigt: „Diese geplante Arbeitsmappe konnte nicht in Power BI veröffentlicht werden.“

## Beschädigte Visualisierungen in Power BI

Im Folgenden werden die wichtigsten Gründe für beschädigte Visualisierungen nach der Veröffentlichung von Report Builder-Anforderungen in Power BI aufgeführt:

* Sie haben eine Anforderung in Report Builder bearbeitet, z. B. durch Ändern der Metriken oder Dimensionen, und sie dann erneut in Power BI veröffentlicht. Durch Bearbeiten von Anforderungen können Ihre Visualisierungen beschädigt werden.
* Sie haben eine Anforderung gelöscht, die in einer Visualisierung verwendet wurde.

>[!IMPORTANT]
>
>Für den Report Builder ist ein Administrator erforderlich, um den Zugriff auf die Ressourcen Ihrer Organisation zu genehmigen. Wenn Sie Zugriff benötigen, bitten Sie einen Administrator, Ihnen die Berechtigung zu erteilen.
> Ein Microsoft-Administrator kann die Einstellung &quot;*Benutzer können die Anwendung registrieren*&quot;überprüfen, die Sie unter: **[!UICONTROL Microsoft Azure]** > **[!UICONTROL Azure Active Directory]** > **[!UICONTROL Benutzereinstellungen ermöglichen Optionen]** finden. Wenn diese Option auf &quot;**Nein**&quot;festgelegt ist, kann der Administrator diese Anwendungstypen registrieren.

Benutzer können den Zugriff gewähren, indem sie sich bei ihrem [Microsoft Power BI-Konto](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&amp;prompt=logint&amp;client_id=8d84f6d8-29a4-4484-a670-589b32400278&amp;redirect_uri=https%3a%2f%2fmy.omniture.com%2fsc15%2farb%2flogin.html&amp;resource=https%3a%2f%2fanalysis.windows.net%2fpowerbi%2fapi&amp;locale=en_US) anmelden.

Administratoren können jedem Zugriff gewähren, indem sie sich beim Microsoft Power BI-Konto des [Administratoren sind](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&amp;prompt=admin_consent&amp;client_id=8d84f6d8-29a4-4484-a670-589b32400278&amp;redirect_uri=https%3a%2f%2fmy.omniture.com%2fsc15%2farb%2flogin.html&amp;resource=https%3a%2f%2fanalysis.windows.net%2fpowerbi%2fapi&amp;locale=en_US) anmelden.

## API-Limit erreichen

Die Berichterstellung in Power BI funktioniert mit der Analytics Reporting-API, sodass API-Schwellenwerte gelten. Weitere Informationen finden Sie unter [Fehlercodes für Webdienste](https://github.com/AdobeDocs/analytics-1.4-apis/blob/3dda746890743c2098256719d6595109b7748262/docs/getting-started/c_Web_Services_Error_Codes.md).
