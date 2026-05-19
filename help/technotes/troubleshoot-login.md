---
title: Fehlerbehebung bei der Anmeldung in Adobe Analytics
description: Schritte für den Fall, dass Sie sich nicht bei Adobe Analytics anmelden können.
feature: Analytics Basics
exl-id: e670a043-c55b-4717-9b60-613ea4d04382
TQID: https://experienceleague.adobe.com/akXZpx8BUywqvI2NGvk9dqIBL-pHEAza1-I05pC89io
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: a421fb65-2c82-457a-921c-28c46b697a39
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 9e2c89f4188c723b4623a6e7859b74ede15e155b
workflow-type: tm+mt
source-wordcount: 607
ht-degree: 88%

---

# Fehlerbehebung bei der Anmeldung in Adobe Analytics

Adobe Analytics verwendet mehrere Authentifizierungsmethoden bei der Anmeldung:

* Adobe ID durch CX Enterprise
* Alte Analytics ID
* Single Sign-on

**Wenn Sie regelmäßig auf Analytics zugreifen und gelegentlich Probleme bei der Anmeldung auftreten, können Sie die meisten Probleme beheben, indem Sie die Cookies und den Cache Ihres Browsers löschen.**

In einigen Fällen können Probleme mit der Verfügbarkeit die Möglichkeit zur Anmeldung beeinträchtigen. Überprüfen Sie [status.adobe.com](https://status.adobe.com) auf offene Fälle. Verwenden Sie andernfalls den entsprechenden Abschnitt je nach der Authentifizierungsmethode Ihres Unternehmens.

## Adobe ID

Beheben Sie Probleme bei der Anmeldung bei Adobe Analytics mithilfe von CX Enterprise.

1. Navigieren Sie zu [Adobe CX Enterprise](https://experience.adobe.com). Wenn Sie nicht auf diese Site zugreifen können, wird diese Domain von Ihrem Unternehmen möglicherweise nicht durch Ihre Firewall gelassen. Wenden Sie sich an das IT-Team Ihres Unternehmens, um dies zuzulassen. Unter [Von Adobe Analytics verwendete IP-Adressen](/help/technotes/ip-addresses.md) finden Sie hilfreiche Informationen für Ihr IT-Team.

2. Authentifizierung mit Adobe ID: Klicken Sie auf **[!UICONTROL Anmelden mit einer Adobe ID]**. Wenn Sie sich nicht anmelden können, überprüfen Sie erneut, ob Ihre E-Mail-Adresse korrekt eingegeben wurde. Klicken Sie andernfalls auf **[!UICONTROL Passwort zurücksetzen]** und befolgen Sie die Anweisungen zum Zurücksetzen des Adobe ID-Passworts.

3. Zugriff auf Analytics nach der Authentifizierung: Klicken Sie oben rechts auf das 9-Raster-Symbol und dann auf „Analytics“. Wenn Sie diese Option nicht haben oder sie ausgegraut ist, wenden Sie sich an einen Produktadministrator in Ihrem Unternehmen, um sicherzustellen, dass Sie über die richtigen Berechtigungen für den Zugriff auf Analytics verfügen.

## Alte Analytics ID

Ein Benutzer in Ihrer Organisation kann die folgende Fehlermeldung erhalten, wenn er versucht, sich anzumelden:

*Als Sicherheitsmaßnahme wurde dieses Konto aufgrund zu vieler fehlgeschlagener Anmeldeversuche gesperrt.*

Wenn das Problem nicht durch Löschen der Cookies/des Cache des Browsers behoben werden kann, setzen Sie das Passwort des Benutzers mithilfe eines Analytics-Administrators in Ihrem Unternehmen zurück.

>[!IMPORTANT]
>
>Die folgenden Schritte zum Zurücksetzen des Passworts eines Benutzers gelten nur für alte Analytics IDs, nicht für Adobe ID. Wenn Ihr Unternehmen Adobe ID verwendet, können Sie Benutzerkonten unter [adminconsole.adobe.com](https://adminconsole.adobe.com) verwalten.

1. Melden Sie sich bei Adobe Analytics mit einem Konto an, das über Administratorrechte verfügt.
2. Navigieren Sie zu **[!UICONTROL Admin]** > **[!UICONTROL Alle Administratoren]** > **[!UICONTROL Benutzerverwaltung]**.
3. Klicken Sie auf die Registerkarte **[!UICONTROL Benutzer]** und dann neben dem gewünschten Benutzer auf **[!UICONTROL Bearbeiten]**.
4. Ändern Sie das Passwort in eine beliebige Zeichenkette und aktivieren Sie das Kontrollkästchen **[!UICONTROL Benutzer auffordern, das Passwort bei der nächsten Anmeldung zu ändern]**.
5. Informieren Sie den Benutzer über das neue Passwort.

## Single Sign-on

Wenden Sie sich an einen Administrator in Ihrer Organisation, um Probleme beim Single Sign-on zu lösen.

## Abgelaufene Anmeldungen

Ein Benutzer in Ihrer Organisation kann die folgende Fehlermeldung erhalten, wenn er versucht, sich anzumelden:

*Fehler: Diese Anmeldung ist abgelaufen.*

Dieser Fehler ist beabsichtigt. Adobe Analytics bietet Administratoren die Möglichkeit, einen Datumsbereich festzulegen, in dem ein Benutzerkonto gültig ist. Wenn das aktuelle Datum außerhalb des gültigen Datumsbereichs für das Konto liegt, kann der Benutzer sich nicht anmelden. Wenden Sie sich an einen Analytics-Administrator in Ihrem Unternehmen, um den gültigen Datumsbereich der Anmeldung zu erweitern. Die Adobe-Kundenunterstützung ist nicht berechtigt, gültige Anmeldedatumsbereiche für Benutzerkonten zu ändern.

## Andere Anmeldeprobleme

Wenn keiner der oben genannten Schritte funktioniert, ermitteln Sie den Umfang des Anmeldeproblems:

* Tritt das Problem bei der Verwendung eines anderen Browsers nicht auf oder ist es bei allen Browsern anzutreffen?
* Tritt das Problem auf einem anderen Computer im Netzwerk auf oder ist es auf mehreren Computern vorhanden?
* Versuchen Sie, sich mit einem anderen Netzwerk anzumelden, wie etwa einer mobilen Datenverbindung, einem Bibliotheks- oder einem Heimnetzwerk. Ist das Problem netzwerkübergreifend vorhanden?

Wenn das Problem nur in Ihrem Netzwerk isoliert auftritt, wenden Sie sich an das IT-Team Ihres Unternehmens, um es zu beheben. Wenden Sie sich an die Adobe-Kundenunterstützung, wenn es nicht auf ein einzelnes Netzwerk beschränkt ist.
