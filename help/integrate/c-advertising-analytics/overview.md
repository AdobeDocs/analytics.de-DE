---
description: Entdecken Sie alles, was Sie mit Advertising Analytics tun können, einschließlich erforderlicher Berechtigungen und verfügbarer Dimensionen und Metriken.
title: Advertising Analytics
feature: Advertising Analytics
exl-id: bc18b74a-0317-4871-b2e0-ec0977ef1731
source-git-commit: 6bedfb9b1333a442bf17cf71dad1e0883b97fd45
workflow-type: tm+mt
source-wordcount: '1112'
ht-degree: 70%

---

# Advertising Analytics

Mit Advertising Analytics können Sie alle Paid Search-Daten von Google Ads und Microsoft Advertising in Adobe Analytics nebeneinander anzeigen. Zuvor mussten alle Google Ads- oder Microsoft Advertising-Daten in Adobe Advertising Cloud (AMO) oder in jeder entsprechenden Anzeigenschnittstelle angezeigt werden. Sie können jetzt Impressions-, Klick- und Kostendaten direkt von Suchmaschinen sowie AMO ID-Instanzen (Klickinstanzen) erhalten.

Indem Sie die Daten aus diesen Suchmaschinen in Adobe Analytics zusammenführen, können Sie sie mit Analysis Workspace zentral analysieren. Eine neue Vorlage [Paid Search Performance](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-report-ad-data-an.md) in Workspace vereinfacht die Analyse.

![](assets/aa_aw.png)

Diese Integration zielt auf folgende Zielgruppen ab:

* **Analysten**, die Performance-Berichte für den Paid Search-Marketer erfassen müssen.
* **Paid Search-Marketer**, die folgende Fragen beantworten müssen: Wie viel Traffic sende ich an unsere Site bzw. konvertieren unsere Kunden? Welche meiner Werbekampagnen sind kosteneffektiv?


## Voraussetzungen {#prerequisites}

* Advertising Analytics steht nur für die Adobe Analytics-SKUs [Select](https://www.adobe.com/de/data-analytics-cloud/analytics/select.html), [Prime](https://www.adobe.com/de/data-analytics-cloud/analytics/prime.html) und [Ultimate](https://www.adobe.com/de/data-analytics-cloud/analytics/ultimate.html) zur Verfügung.
* Diese Funktion steht auch Kunden ohne Advertising Cloud und AMO zur Verfügung.
* Sie müssen ein Adobe Analytics-Administrator sein, um Zugriff auf Advertising Analytics zu erhalten, oder zu einem Produktprofil gehören, dem Zugriff [&#x200B; Advertising Analytics &#x200B;](/help/integrate/c-advertising-analytics/overview.md#permissions) wurde.
* Für jede Report Suite, in der Sie Google Ads- oder Microsoft Advertising-Suchdaten anzeigen möchten, müssen Sie [diese Report Suites für Advertising Analytics aktivieren](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-provision-rs.md) ( **[!UICONTROL Admin]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Advertising Analytics-Konfiguration]**).
* Sie benötigen die Anmeldedaten eines Benutzers mit Bearbeitungsberechtigungen für die Suchkonten, die Sie in Adobe Analytics integrieren möchten wie z. B. Google-Konto-ID und -Passwort.
* Im Fall von Microsoft Advertising benötigen Sie auch die [[!UICONTROL Konto-ID] und [!UICONTROL Manager-Konto-ID]](c-adanalytics-workflow/aa-locate-account-id.md).

## Advertising Analytics-Berechtigungen {#permissions}

Analytics verfügt über zwei Berechtigungen, die Analytics-Administrierenden automatisch erteilt werden. Administratoren können diese Berechtigungen dann an andere Benutzer weitergeben.

| Berechtigung | Definition | Berechtigung bei Anmeldung in Adobe Experience Cloud gewähren |
| --- | --- | --- |
| Advertising Analytics-Verwaltung | Ermöglicht Nutzern die Einrichtung, Bearbeitung und Anzeige von Werbesuchkonten. | Melden Sie sich bei [adminconsole.adobe.com](https://adminconsole.adobe.com) > [!UICONTROL Produkte] > [!UICONTROL Adobe Analytics] > [!UICONTROL Produktprofil] > [!UICONTROL Berechtigungen] Registerkarte > [!UICONTROL Analytics-Tools] > [!UICONTROL Advertising Analytics Management] |
| Advertising Analytics-Konfiguration | Ermöglicht Benutzern die Konfiguration von Report Suites, die für Advertising Analytics bereitgestellt werden sollen. | Melden Sie sich bei [adminconsole.adobe.com](https://adminconsole.adobe.com) > [!UICONTROL Produkte] > [!UICONTROL Adobe Analytics] > [!UICONTROL Produktprofil] > [!UICONTROL Berechtigungen] Registerkarte > [!UICONTROL Analytics-Tools] > [!UICONTROL Advertising Analytics Configuration] |

## Dimensionen und Metriken in Advertising Analytics {#dimensions-metrics}

Advertising Analytics fügt die folgenden Dimensionen und Metriken zu Analysis Workspace, Report Builder und der Analytics Reporting-API hinzu.

### Dimensionen

>[!IMPORTANT]
>
>Diese Integration erstellt eine neue Gruppe von Dimensionen mithilfe der Klassifizierungen der AMO-ID-Variablen. Diese neuen Dimensionen wirken sich nicht auf bestehende Marketingkanäle oder Dimensionen von Kampagnen-Tracking-Variablen aus. Die AMO-ID wird mit einem Besucherprofil verknüpft, wenn der Besucher über eine Paid Search-Werbeanzeige zur Site gelangt. Deshalb können Sie die AMO-Dimensionen nutzen, um sowohl die von dieser Integration bereitgestellten AMO-Metriken als auch vom Benutzer erfasste Daten (Besuche, Besucher, Seitenaufrufe, Absprungrate, Bestellungen, Umsatz, Kundenereignisse usw.) aufzuschlüsseln. Beim Reporting zu anderen lokalen Metriken können sie auch nach anderen Dimensionen aufgeschlüsselt werden.
>
>Die Klassifizierungen für diese Metriken werden täglich aktualisiert. Wenn Sie also Änderungen an Metadaten in einer Suchmaschine vornehmen, treten diese möglicherweise erst am folgenden Tag in Kraft, nachdem die Klassifizierungen aktualisiert wurden.

| Name der Klassifizierung (Dimension) | Definition |
| --- | --- |
| **[!UICONTROL Keyword MatchType (AMO-ID)]** | Der Keyword-Übereinstimmungstyp. Mögliche Werte lauten in der Regel „Weit gefasst“, „Wortgruppe“, „Exakt“ bzw. kein Wert, wenn die Anzeigenart nicht über einen Übereinstimmungstyp verfügt. |
| **[!UICONTROL Anzeigenplattform (AMO-ID)]** | Der Name der Suchmaschine. Werte können &quot;Google AdWords“ oder &quot;Microsoft Bing Ads“ sein. |
| **[!UICONTROL Konto (AMO-ID)]** | Der Name des Suchmaschinenkontos, das verfolgt wird. |
| **[!UICONTROL Campaign (AMO-ID)]** | Der Name der Kampagne in Ihrem Suchmaschinenkonto. |
| **[!UICONTROL Anzeigengruppe (AMO-ID)]** | Der Name der Anzeigengruppe in Ihren Suchmaschinen-Kampagnen. |
| **[!UICONTROL Anzeige (AMO-ID)]** | Der Anzeigentitel und die Anzeigenbeschreibung Ihrer Werbeanzeige. |
| **[!UICONTROL Keyword (AMO-ID)]** | Der Keyword-Wert aus Ihrem Suchmaschinenkonto. |
| **[!UICONTROL Übereinstimmungstyp (AMO-ID)]** | Der Ihrem Keyword zugewiesene Keyword-Übereinstimmungstyp. Mögliche Werte lauten in der Regel „Weit gefasst“, „Wortgruppe“, „Exakt“ bzw. kein Wert, wenn die Anzeigenart nicht über einen Übereinstimmungstyp verfügt. |
| **[!UICONTROL Ad Type (AMO ID)]** | Der Typ der verarbeiteten Anzeige, normalerweise „Textanzeige“. |
| **[!UICONTROL Anzeigentitel (AMO-ID)]** | Das in Ihrer Werbeanzeige verwendete Titelobjekt. |
| **[!UICONTROL Anzeigenbeschreibung (AMO-ID)]** | Die in Ihrer Werbeanzeige verwendete Anzeigenbeschreibung. |
| **[!UICONTROL Anzeige-URL (AMO-ID)]** | Die in Ihrer Werbeanzeige verwendete Werbeanzeigen-URL. |
| **[!UICONTROL Werbeziel-URL (AMO-ID)]** | Die Ihrer Werbeanzeige zugewiesene Landingpage-URL oder endgültige URL. |
| **[!UICONTROL Netzwerk (AMO-ID)]** | Das Netzwerk, auf dem die Werbeanzeige ausgeliefert wird. Bei Advertising Analytics lautet dieser Wert immer „Suche“. |
| **[!UICONTROL Platzierung (AMO-ID)]** | Die Website der verwalteten Platzierung (bei Content-Netzwerken). Diese Dimension wird nur bei verwalteten Platzierungen verwendet. |
| **[!UICONTROL Produktzielgruppe (AMO-ID)]** | Der bei PLA-Anzeigen verwendete Name des Produktziels (nicht das tatsächlich erworbene Produkt). |
| **[!UICONTROL Optimierung (AMO-ID)]** | Dies wird von Advertising Analytics nicht verwendet. Es wird nur von Advertising Cloud-Kunden verwendet. |
| **[!UICONTROL Gerät (AMO-ID)]** | Derzeit nicht verwendet. Platzhalter für potenzielle zukünftige Produktoptimierungen am jeweiligen Zielgerätetyp (z. B. Mobilgerät, Desktop) einer Werbeanzeige (nicht das tatsächliche Gerät des Besuchers). |

### Metriken

>[!IMPORTANT]
>
>Bei den von Advertising Analytics bereitgestellten Metriken (siehe unten) handelt es sich um Zusammenfassungsdaten aus den Suchmaschinen. Sie sind nicht mit den Analytics-Besucherprofilen verbunden. Sie sind nur mit der AMO-ID-Variablen und den zugehörigen Classification-Dimensionen verknüpft. Deshalb sollten sie nicht zu Berichten abseits der Dimensionen/Segmente hinzugefügt werden, die auf den AMO-ID-Dimensionen basieren. In einem solchen Fall zeigt Analytics nur Nullen für die Daten an. Sie können sie mit anderen Metriken zu berechneten Metriken hinzufügen, jedoch sollte die entsprechende berechnete Metrik nur nach den AMO-ID-Dimensionen aufgeschlüsselt werden.
>
>Bei diesen Metriken handelt es sich um täglich abgerufene Daten. Für den aktuellen Tag liegen also keine Daten vor. Sie sollten nicht mit einem Zeitabstand von unter einem Tag zu Berichten hinzugefügt werden.
>
>Es gibt eine Metrik zu AMO-ID-Instanzen, die festgelegt wird, wenn die AMO-ID auf einer Landingpage festgelegt wird (also bei einem Clickthrough). Diese Metrik wird in Echtzeit mit dem Landingpage-Aufruf erfasst und ist für Aufschlüsselungen mit anderen auf der Landingpage festgelegten Dimensionen verfügbar.

| Metrikname | Definition |
| --- | --- |
| **[!UICONTROL AMO-Impressionen]** | Die Anzahl der Werbeimpressionen gemäß den Daten der Suchmaschine. |
| **[!UICONTROL AMO-Klicks]** | Die Anzahl der Klicks gemäß den Daten der Suchmaschine. |
| **[!UICONTROL AMO-Kosten]** | Die Kosten pro Keyword/Werbeanzeige gemäß den Daten der Suchmaschine. |
