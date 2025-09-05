---
description: Ermöglicht das Steuern des Zugriffs auf Berichterstellungsdaten. Zu den Optionen gehören sichere Passwörter, Passwortablauf, IP-Anmeldebeschränkungen und E-Mail-Domänenbeschränkungen.
title: Sicherheits-Manager
feature: Company Settings
exl-id: 6dcf0354-4b4a-4bd5-ba6c-ae42c7b9e4df
role: Admin
source-git-commit: e09234ca27fbf923e026aa1f2ed0ebfed636bf7c
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 94%

---

# Sicherheits-Manager

Mit dem Sicherheits-Manager können Sie den Zugriff auf Berichtsdaten kontrollieren. Zu den Optionen gehören sichere Passwörter, Passwortablauf, IP-Anmeldebeschränkungen und E-Mail-Domänenbeschränkungen.

## Einstellungen

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Alle Administratoren]** > **[!UICONTROL Firmeneinstellungen]** > **[!UICONTROL Sicherheit]**

| Einstellung | Beschreibung |
| --- | --- |
| Sichere Passwörter erforderlich | Erzwingt die Erstellung sicherer Passwörter, die folgende Regeln beachten: <ul><li>Muss mindestens acht Zeichen lang sein.</li><li>Muss mindestens ein Symbol oder eine Zahl zwischen dem ersten und dem letzten Zeichen enthalten.</li><li>Muss mindestens ein Alpha-Zeichen enthalten.</li><li>Darf nicht im Wörterbuch stehen oder Begriffe aus dem (englischen) Wörterbuch enthalten.</li><li>Darf nicht drei (3) aufeinanderfolgende Zeichen aus dem Anmeldenamen des Benutzers enthalten.</li><li>Muss sich von den vorhergehenden 10 Passwörtern unterscheiden.</li></ul>**Hinweis**: Diese Funktion wird bei zukünftigen neuen Passwörtern erzwungen. Vorhandene Passwörter werden nicht überprüft, und die Benutzer werden auch nicht aufgefordert, ihre bisherigen Passwörter zu ändern. Erwägen Sie daher, den Kennwortablauf zu aktivieren, um Benutzer zu zwingen, ihre Kennwörter zu ändern und die strengen Kennwortregeln einzuhalten. |
| Passwortablauf | Erzwingt die regelmäßige Änderung des Kontopassworts durch den Benutzer. Sie können das Intervall festlegen, in dem die Kennwörter ablaufen, und den sofortigen Ablauf von Kennwörtern erzwingen. |
| E-Mail-Domänenbeschränkungen erzwingen | Filtert die E-Mail-Adressen und Domänen, an die Analytics Lesezeichen, herunterladbare Berichte und Warnhinweise sendet. Die E-Mail-Filterliste kann bis zu 100 Einträge lang sein. Jeder einzelne Eintrag steht für eine E-Mail-Adresse oder eine gesamte E-Mail-Domäne. Wenn ein terminierter Bericht als Zieladresse eine nicht genehmigte E-Mail-Adresse aufweist, versendet Analytics eine E-Mail-Benachrichtigung zu diesem Problem sowie einen Link zur Aufhebung der Berichtsplanung. Die Funktion **[!UICONTROL E-Mail-Domänenbeschränkungen erzwingen]** wird nur durchgesetzt, wenn sich in der Liste akzeptierter E-Mail-Domänenfilter mindestens ein Eintrag befindet. **[!UICONTROL Akzeptierte E-Mail-Adresse und Domains]**: Wenn Sie einen IP-Adressbereich angeben möchten, schließen Sie den Bereich in eckigen Klammern ein (z. B. `192.168.10.[20-240]`). Sie können auch Platzhalter verwenden, um eine beliebige Zahl zwischen 0 und 255 anzugeben (z. B. `192.168.[10-14].*`). |
| Benachrichtigung über Passwortwiederherstellung | Benachrichtigt die jeweiligen Administratoren, wenn ein Benutzer versucht, das Passwort seines Benutzerkontos zurückzusetzen. **[!UICONTROL Verfügbare Admins]**: Es wird eine Liste sämtlicher Administratoren angezeigt. Halten Sie bei Bedarf beim Klicken die STRG- bzw. Umschalttaste gedrückt, um mehrere Administratoren gleichzeitig auszuwählen. **[!UICONTROL E-Mail-Mitglieder]**: Hiermit wird die aktuell definierte E-Mail-Gruppe angezeigt. |
