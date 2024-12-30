---
description: Häufige Probleme bei der Verwendung von Report Builder mit Power BI.
title: Fehlerbehebung für die Power BI-Integration
feature: Report Builder
role: User, Admin
exl-id: adb13a0e-99fb-48f5-add2-204d155e467f
source-git-commit: ae6ffed05f5a33f032d0c7471ccdb1029154ddbd
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 64%

---

# Fehlerbehebung für die Power BI-Integration

{{legacy-arb}}

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
>Report Builder erfordert, dass ein Administrator den Zugriff auf die Ressourcen Ihres Unternehmens autorisiert. Wenn Sie Zugriff benötigen, bitten Sie einen Administrator, Ihnen die Berechtigung zu erteilen.
> Ein Microsoft-Administrator kann die Einstellung *Benutzer können Anwendung registrieren* unter **[!UICONTROL Microsoft Azure]** > **[!UICONTROL Azure Active Directory]** > **[!UICONTROL Benutzereinstellungen lassen Optionen zu]** überprüfen. Wenn diese Option auf **Nein** gesetzt ist, kann der Administrator diese Anwendungstypen registrieren.

Benutzende können Zugriff gewähren, indem sie sich bei ihrem [Microsoft Power BI-Konto anmelden](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&amp;prompt=logint&amp;client_id=8d84f6d8-29a4-4484-a670-589b32400278&amp;redirect_uri=https%3a%2f%2fmy.omniture.com%2fsc15%2farb%2flogin.html&amp;resource=https%3a%2f%2fanalysis.windows.net%2fpowerbi%2fapi&amp;locale=en_US).

Administratoren können jedem Zugriff gewähren, indem sie sich bei ihrem [Microsoft Power BI-Konto des Administrators](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&amp;prompt=admin_consent&amp;client_id=8d84f6d8-29a4-4484-a670-589b32400278&amp;redirect_uri=https%3a%2f%2fmy.omniture.com%2fsc15%2farb%2flogin.html&amp;resource=https%3a%2f%2fanalysis.windows.net%2fpowerbi%2fapi&amp;locale=en_US) anmelden.

## API-Limit erreicht

Das Reporting im Power BI funktioniert mit der Analytics-Reporting-API, sodass API-Schwellenwerte gelten. Weitere Informationen finden Sie [Web-Services-Fehlercodes](https://github.com/AdobeDocs/analytics-1.4-apis/blob/3dda746890743c2098256719d6595109b7748262/docs/getting-started/c_Web_Services_Error_Codes.md).
