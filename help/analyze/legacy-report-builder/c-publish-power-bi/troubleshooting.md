---
description: Häufige Probleme bei der Verwendung von Report Builder mit Power BI.
title: Fehlerbehebung für die Power BI-Integration
feature: Report Builder
role: User, Admin
exl-id: adb13a0e-99fb-48f5-add2-204d155e467f
TQID: https://experienceleague.adobe.com/Q4n08pGcqBwhUl5q3VnWhuVcW9E-tdvv3LoHSLoGleA
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 382
ht-degree: 40%

---

# Fehlerbehebung für die Power BI-Integration

{{legacy-arb}}

Ermitteln und Lösen von allgemeinen Problemen bei der Verwendung von Report Builder mit Power BI.

## Fehlschlagen der Veröffentlichung in Power BI

Geplante Arbeitsmappen, für die Power BI veröffentlicht werden muss, sind darauf angewiesen, dass Power BI-Services ausgeführt werden. Zwei Hauptgründe für eine Nichtveröffentlichung sind:

* Power BI-Services sind möglicherweise ausgefallen.
* Der Benutzer, der die Arbeitsmappe geplant hat, verfügt nicht mehr über gültige Microsoft-Kontoanmeldeinformationen.

Für jede geplante Report Builder-Aufgabe werden drei Versuche pro geplanter Ausführung durchgeführt:

* Nach dem ersten fehlgeschlagenen Versuch erhalten Sie folgende Nachricht: „Wir konnten diese geplante Arbeitsmappe nicht in Microsoft Power BI veröffentlichen. Wir werden es in Kürze erneut versuchen.“
* Nach dem zweiten fehlgeschlagenen Versuch erhalten Sie keine Meldung.
* Nach dem dritten fehlgeschlagenen Versuch erhalten Sie folgende Nachricht: „Wir konnten diese Arbeitsmappe nicht in Power BI veröffentlichen.“

## Beschädigte Visualisierungen in Power BI

Im Folgenden werden die wichtigsten Gründe für beschädigte Visualisierungen nach der Veröffentlichung von Report Builder-Anforderungen in Power BI aufgeführt:

* Sie haben eine Anforderung in Report Builder bearbeitet, z. B. durch Ändern der Metriken oder Dimensionen, und sie dann erneut in Power BI veröffentlicht. Das Bearbeiten von Anfragen kann die Visualisierungen beschädigen.
* Sie haben eine Anfrage gelöscht, die in einer Visualisierung verwendet wurde.

>[!IMPORTANT]
>
>Report Builder erfordert, dass ein Administrator den Zugriff auf die Ressourcen Ihrer Organisation autorisiert. Wenn Sie Zugriff benötigen, bitten Sie einen Administrator, Ihnen die Berechtigung zu erteilen.
> Ein Microsoft-Administrator kann die Einstellung *Benutzer können Anwendung registrieren* unter überprüfen: **[!UICONTROL Microsoft Azure]** > **[!UICONTROL Azure Active Directory]** > **[!UICONTROL Benutzereinstellungen lassen Optionen zu]**. Wenn diese Option auf **Nein** gesetzt ist, kann der Administrator diese Anwendungstypen registrieren.

Benutzer können Zugriff gewähren, indem sie sich bei ihrem [Microsoft Power BI-Konto anmelden](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&prompt=logint&client_id=8d84f6d8-29a4-4484-a670-589b32400278&redirect_uri=https%3a%2f%2fmy.omniture.com%2fsc15%2farb%2flogin.html&resource=https%3a%2f%2fanalysis.windows.net%2fpowerbi%2fapi&locale=en_US).

Administratoren können jedem Zugriff gewähren, indem sie sich bei ihrem [Microsoft Power BI-Konto des Administrators](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&prompt=admin_consent&client_id=8d84f6d8-29a4-4484-a670-589b32400278&redirect_uri=https%3a%2f%2fmy.omniture.com%2fsc15%2farb%2flogin.html&resource=https%3a%2f%2fanalysis.windows.net%2fpowerbi%2fapi&locale=en_US) anmelden.

## API-Limit erreicht

Das Reporting in Power BI funktioniert mit der Analytics-Reporting-API, sodass API-Schwellenwerte gelten.
