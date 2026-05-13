---
title: Fehlerbehebung bei Sitzungen in Adobe Analytics
description: Erfahren Sie, wie Sie Probleme bei der Abmeldung von Adobe Analytics beheben können.
feature: Analytics Basics
exl-id: 191250ef-8313-47be-9717-046cce870998
TQID: https://experienceleague.adobe.com/b8dTBhP3a6FZSmABKtQKTp9XkmYIjfS5--Vbzl6xRGE
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: a421fb65-2c82-457a-921c-28c46b697a39
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 367
ht-degree: 88%

---

# Fehlerbehebung bei Sitzungen in Adobe Analytics

Auf dieser Seite finden Sie Informationen zur Fehlerbehebung bei Sitzungen. Bei entsprechenden Problemen können Sie sich zwar erfolgreich anmelden, haben jedoch Schwierigkeiten, angemeldet zu bleiben. Wenn Sie Probleme mit der Anmeldung bei Adobe Analytics haben, lesen Sie [Fehlerbehebung bei Anmeldeproblemen mit Adobe Analytics](troubleshoot-login.md).

Fast alle sitzungsbasierten Probleme haben ihre Ursache im angepassten Unternehmensnetzwerk. Wenn Sie sich bei Adobe Analytics anmelden können, aber Probleme dabei haben, angemeldet zu bleiben, verwenden Sie diesen Artikel, um die Ursache zu ermitteln.

## Bestimmen Sie, ob das Problem auf das Netzwerk Ihres Unternehmens zurückzuführen ist. {#network}

Viele Unternehmen stellen zusätzliche Netzwerkfunktionen bereit, um die Sicherheit zu erhöhen, wie z. B. Proxyserver oder Firewalls. Diese Anpassungen können manchmal die Möglichkeit beeinträchtigen, eine aktive Sitzung in Adobe Analytics beizubehalten.

Um festzustellen, ob das Unternehmensnetzwerk, mit dem Sie verbunden sind, Probleme mit der Verwendung von Adobe Analytics verursacht, verwenden Sie Ihre Experience Cloud-Anmeldedaten auf einem Gerät außerhalb Ihres Unternehmensnetzwerks. Nutzen Sie hierfür beispielsweise Ihr Heimnetzwerk oder den Datenplan eines Mobilgeräts. Wenn Sie erfolgreich von Seite zu Seite wechseln können, ohne abgemeldet zu werden, ist das Netzwerk Ihres Unternehmens der Grund für Ihre Abmeldung bei Adobe Analytics.

## Probleme aufgrund von Proxy {#proxy}

Adobe verwendet bei Anforderungen an Adobe einen Autorisierungs-Header. Einige Proxys wie Edge Secure Web Gateway (früher Bluecoat) entfernen wichtige Informationen vom Autorisierungs-Header, die von Adobe Analytics verwendet werden. Wenn Adobe den Autorisierungs-Header nicht empfängt, läuft die Sitzung ab.

Um dieses Problem zu beheben, empfiehlt Adobe, mit dem IT-Team Ihres Unternehmens zusammenzuarbeiten, um den Autorisierungs-Header über den Proxy Ihres Unternehmens zuzulassen.

>[!NOTE]
>
>Mitglieder der Analytics-Community fanden die folgenden Links hilfreich, die allerdings nicht zu Adobe gehören. Berücksichtigen Sie diese Anmerkung bei der Anzeige der Inhalte.

Informationen zu Symantec-Proxys und Authentifizierungs-Headern finden Sie hier:

* [Konfigurieren der Upstream-Proxy-Authentifizierung in einer Proxy-Kettenbereitstellung auf einer ProxySG- oder ASG-Appliance](https://techdocs.broadcom.com/us/en/symantec-security-software/web-and-network-security/edge-swg/7-3/authentication_co.html)
* [Weiterleiten von Anmeldeinformationen von Benutzern an einen Server hinter der ProxySG-Einheit](https://knowledge.broadcom.com/external/article/165859/how-to-forward-user-credentials-to-a-ser.html)
