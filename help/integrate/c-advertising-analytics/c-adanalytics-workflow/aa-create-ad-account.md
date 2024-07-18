---
title: Einrichten eines Werbekontos in Advertising Analytics
description: In diesem Artikel wird erläutert, wie Sie neue Werbekonten erstellen und mehrere Konten mehreren Report Suites zuordnen.
feature: Advertising Analytics
exl-id: f593c714-e85f-4000-85b2-6294cad81e25
source-git-commit: a34dfc63c47b6fe4b91b2b67ea21cdddafb0bfd0
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 31%

---

# Werbekonto einrichten

Adobe Analytics-Administratoren können neue Werbekonten erstellen und mehrere Konten mehreren Report Suites zuordnen (1 : 1, 1 : Viele, Viele : Viele).

Administratoren können auch [Nicht-Administratoren Zugriff gewähren](/help/integrate/c-advertising-analytics/overview.md#section_FCC58EB635954A32990D4E67B52B4369), damit sie Werbekonten einrichten können.

<!--
![](assets/aa_accounts.png)
-->

1. Navigieren Sie in Adobe Analytics zu **[!UICONTROL Admin]** > **[!UICONTROL Werbekonten]**.
1. (Nur bei erster Verwendung) Akzeptieren Sie die Bedingungen der Endnutzer-Lizenzvereinbarung.
1. Wählen Sie **[!UICONTROL + Hinzufügen]** aus.
1. Das Dialogfeld [!UICONTROL Neue Suchmaschineneinstellung] wird angezeigt.

   ![](assets/aa-new-se-account.png)

1. Füllen Sie die **[!UICONTROL Suchmaschineneinstellungen]** gemäß den folgenden Richtlinien aus:

   | Einstellung | Beschreibung |
   | --- | --- |
   | **[!UICONTROL Typ]** | Sie haben zwei Optionen: **[!UICONTROL Google Adwords]** und **[!UICONTROL Bing Ads]**.  Hinweis: Yahoo Gemini wurde am 31. März 2019 von Microsoft Bing übernommen. Daher ist die Anzeigen-Kontenoption „Yahoo Gemini“ nicht mehr verfügbar. |
   | Kontoname | Sie können diesen Kontonamen auf einen beliebigen Namen setzen, der Ihnen passt.  Der Kontoname ist der Anzeigename des Kontos, der in der Benutzeroberfläche angezeigt wird. |
   | OAuth-Token | **Hinweis**: OAuth ist ein offener Standard für die Zugriffsdelegierung, der häufig verwendet wird, um Websites oder Anwendungen Zugriff auf Informationen auf Websites zu gewähren, ohne Kennwörter anzugeben. Sie sehen, dass Sie an eine Drittanbieter-URL (efrontier.com) weitergeleitet werden. Adobe verwendet Adobe Media Optimizer, um den OAuth-Authentifizierungsprozess für alle drei Suchmaschinen zu unterstützen. Wenn Sie Internet Explorer 11 (oder früher) verwenden, können Sie das OAuth-Token für keine der drei Suchmaschinen abrufen. Verwenden Sie stattdessen einen anderen Webbrowser.<p>Wählen Sie **[!UICONTROL Token abrufen]** aus, um den OAuth2-Authentifizierungsprozess zu starten. Sie werden aufgefordert, sich mit Ihren Anmeldedaten bei Ihrem Google-/Bing-Suchkonto anzumelden. Je nachdem, welchen Prozess Sie ausgewählt haben, unterscheidet sich der Prozess geringfügig: <ul><li>Google AdWords: Geben Sie die Google-Konto-ID an</li><li>Microsoft Bing: Geben Sie die Bing-Konto-ID und die Bing-Kunden-ID an.</li></ul>Weitere Informationen zu diesen IDs finden Sie unter [Konto-ID ermitteln](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-locate-account-id.md) . Nachdem Sie sich erfolgreich angemeldet haben, wird im Feld **[!UICONTROL OAuth-Token]** **[!UICONTROL Abgerufen]** angezeigt. |

1. Im Abschnitt **[!UICONTROL Tracking]** geben Sie Informationen zum Tracking der Daten mithilfe Ihrer Adobe Analytics-Implementierung an. Das Tracking ist ein erforderlicher Schritt, um die Adobe Analytics-Daten ordnungsgemäß mit den Suchmaschinendaten zu ergänzen.
Legen Sie die **[!UICONTROL Tracking-Einstellungen]** gemäß folgenden Richtlinien fest:

   | Einstellung | Beschreibung |
   | --- | --- |
   | Typ | <ul><li>**Auto**: Hier entscheidet die Advertising Cloud-Engine, wie die Tracking-Parameter an die Tracking-Vorlagen/Ziel-URLs der Tracking-Parameter angehängt werden. [!UICONTROL Tracking automatischer Typen] ist der einfachste Ansatz, der jedoch möglicherweise nicht zum besten integrierten Datensatz führt.<br>**Wichtig:** Um ein Suchmaschinenkonto mit dem Befehl [!UICONTROL Tracking des automatischen Typs] zu konfigurieren, sind Sie für die folgenden Aktionen verantwortlich:<ul><li>Der Parameter `s_kwcid` und der Wert werden den Konto-Tracking-Vorlagen oder Landingpage-URLs im hinzugefügten Konto hinzugefügt. Der Parameter und der Wert werden am Ende der URL eingefügt. Es kann eine zusätzliche Aktion erforderlich sein, wenn Ihr Webserver ein bestimmtes `key=value` -Paar am Ende der URL benötigt. Oder es ist ein Update erforderlich, um ein neues `key=value`-Paar in der URL zu unterstützen. **Hinweis**: Erfahren Sie mehr darüber, ob Sie diesen Parameter zu Ihrer [Inhaltssicherheitsrichtlinie](https://experienceleague.adobe.com/en/docs/id-service/using/reference/csp) hinzufügen sollten.</li><li>Darüber hinaus können Keywords als Teil des Wertes `s_kwcid` in die Landingpage-URL eingefügt werden. Wenn die Suchbegriffe Sonderzeichen oder Symbole enthalten, vergewissern Sie sich bitte, dass Ihr Webserver diese Zeichen unterstützen kann. Ein Beispiel für ein gängiges Sonderzeichen ist `+`, das in Suchbegriffen mit der Bezeichnung &quot;Weit reichende Übereinstimmung geändert&quot;verwendet wird.</li></ul></li><li>**Manuell**: Hiermit können Sie verwalten, wie Tracking-Parameter zu den Tracking-Vorlagen/Ziel-URLs der Suchmaschine hinzugefügt werden. [Weitere Informationen finden Sie in den Beispielen für manuelles Tracking für die einzelnen Suchmaschinen](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-manual-vs-automatic-tracking.md).</li></ul> |

1. Wählen Sie im Abschnitt **[!UICONTROL Zuordnung]** eine oder mehrere Report Suites aus, die mit diesem Suchmaschinenkonto verknüpft werden sollen. Sie müssen mindestens eine Report Suite angeben, bevor Sie das Werbekonto speichern können. Sie können mehrere Konten mehreren Report Suites zuordnen (1 : 1, 1 : Viele, Viele : viele). Beachten Sie, dass die Daten, die Adobe Media Optimizer von der Suchmaschine abruft, einfach in eine zugeordnete Report Suite kopiert werden, sodass keine Datenaufteilung erfolgt.

   >[!IMPORTANT]
   >
   >Nur Report Suites, die einer Experience Cloud-Organisation zugeordnet sind, können ausgewählt werden. Wenn Ihre Report Suite nicht aufgeführt ist, suchen Sie im Abschnitt [Problembehebung in Advertising Analytics](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-troubleshooting.md) nach weiteren Informationen.

   Legen Sie die **[!UICONTROL Zuordnungseinstellungen]** gemäß folgenden Richtlinien fest:

   | Einstellung | Beschreibung |
   | --- | --- |
   | Report-Suite-Zuordnung | Die Report-Suite-Zuordnung bestimmt die Report Suite, die mit diesem Suchmaschinenkonto verknüpft werden soll. Anders ausgedrückt: Sie bestimmt, an welche Report Suite(s) die Daten der Suchmaschine gesendet werden. |


1. Wählen Sie **[!UICONTROL Speichern]** aus.
1. Ein Haftungsausschluss zeigt eine Liste mit Einschränkungen an. Bestätigen Sie, dass Sie diese Vereinbarung gelesen haben und verstehen Sie sie. Aktivieren Sie das Kontrollkästchen und wählen Sie dann **[!UICONTROL OK]** aus.

   Nun wird die [Verwaltungsoberfläche](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-manage-ad-accounts.md) für Werbekonten angezeigt, in der das neu erstellte Konto aufgeführt sein sollte.

>[!NOTE]
>
>Es dauert in der Regel mindestens 24 Stunden, bis Suchmaschinendaten in Ihren Analytics-Berichten angezeigt werden.
