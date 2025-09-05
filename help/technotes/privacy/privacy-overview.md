---
description: Übersicht der Daten, die Adobe Analytics erfasst, und sonstige Hinweise zum Datenschutz.
keywords: Datenschutz
title: Datenschutzübersicht
feature: Data Governance
exl-id: 71c83106-a047-47d7-9a70-4a24595e3d0a
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '977'
ht-degree: 98%

---

# Datenschutzübersicht

Adobe möchte Ihr Unternehmen in die Lage versetzen, die geltenden Gesetze und Vorschriften einzuhalten. Weitere Informationen finden Sie unter {[}Adobe Experience Cloud-Datenschutz. ](https://www.adobe.com/de/privacy/experience-cloud.html){target=_blank} Zwischen Adobe Analytics und Ihrer Organisation agiert Adobe als „Auftragsverarbeiter“ und Sie sind der oder die „Datenverantwortliche“ (oder ein Äquivalent gemäß den geltenden Gesetzen zum Schutz der Privatsphäre und des Datenschutzes). Es ist Sache Ihrer Organisation, ob sie offenlegen möchte, wie Sie die Adobe-Produkte und -Dienste verwenden. Denn nur Ihre Organisation hat die Kontrolle darüber, wie die Adobe-Lösungen implementiert werden. Bei der Verwendung von Adobe Analytics ist Ihre Organisation für die Einhaltung Ihrer eigenen Datenschutzrichtlinie, Ihrer Service-Vereinbarung mit Adobe und aller geltenden Gesetze verantwortlich.

Adobe empfiehlt dringend die Einhaltung der folgenden übergreifenden Konzepte:

* **Wenn Sie personenbezogene Daten erfassen, stellen Sie sicher, dass Sie die Datenschutzgesetze und -vorschriften einhalten.** Mit benutzerspezifischen Variablen können Sie praktisch alles erfassen, auf das Sie zugreifen können. Beachten Sie jedoch die Datenschutzrichtlinien Ihrer Organisation und die geltenden Gesetze.
* **Stellen Sie Ihrer Kundschaft leicht auffindbare und leicht verständliche Datenschutzinformationen für Ihre Organisation bereit.** Hilfreiche Informationen umfassen Opt-out-Links, die Verwendung der Browser-Daten und die Verwendung bzw. die Planung der Verwendung von Adobe-Diensten.
* **Bleiben Sie sowohl über die lokalen als auch die internationalen Gesetze informiert, die für Sie gelten.** Wenn Ihre Organisation auf globaler Ebene tätig ist, können einige internationale Gesetze gelten.

## Aufschlüsselung der Datenerfassung

Adobe bietet mehrere Datenerfassungsbibliotheken, die das Senden von Daten an Adobe unterstützen. Zu diesen gehören als wichtige Beispiele:

* **AppMeasurement**: Eine Bibliothek, die dafür konzipiert ist, Daten direkt an Adobe Analytics zu senden.
* **Web SDK**: Eine Bibliothek, die zum Senden von Daten an das Adobe Experience Platform Edge Network konzipiert ist und diese Daten dann an Adobe Analytics weiterleitet.
* **Tags**: Eine Web-basierte Benutzeroberfläche, mit der Sie Ihre Implementierung konfigurieren können, ohne Zugriff auf den Quell-Code einer Website oder App über die ursprüngliche Tag-Implementierung hinaus zu benötigen. Erweiterungen sind sowohl für AppMeasurement als auch für das Web SDK verfügbar.

Adobe Analytics kann die folgenden Datentypen erfassen:

| Datentyp: | Details | Beispielvariablen mit diesen Daten |
| --- | --- | --- |
| Seitennamen oder URLs von Webseiten auf Ihrer Site | Diese Daten sind erforderlich, damit Adobe Analytics funktioniert. Für jeden Treffer ist eine URL oder ein Seitenname erforderlich. | [Seite](/help/components/dimensions/page.md), [Seiten-URL](/help/components/dimensions/page-url.md) |
| Zeitbezogene Daten | Diese Daten sind erforderlich, damit Adobe Analytics funktioniert. Für die Datenerfassung ist ein Zeitstempel erforderlich und zeitbezogene Daten werden vom Zeitstempel abgeleitet. | [Auf der Seite verbrachte Zeit](/help/components/dimensions/time-spent-on-page.md), [Tageszeit](/help/components/dimensions/hour-of-day.md), [Vormittag/Nachmittag](/help/components/dimensions/am-pm.md), [Werktag/Wochenende](/help/components/dimensions/weekday-weekend.md), [Wochentag](/help/components/dimensions/day-of-week.md), [Monat](/help/components/dimensions/month-of-year.md) |
| Referrer-Daten | Datenerfassungsbibliotheken erfassen standardmäßig die Referrer-URL, wenn eine Besucherin oder ein Besucher auf Ihre Website gelangt. Sie können Ihre Implementierung anpassen, um Daten in der Abfragezeichenfolge eines Referrers zu erfassen. Diese Vorgehensweise wird häufig bei Kampagnen und beim Tracking der Wirksamkeit von Anzeigen angewandt. | [Referrer](/help/components/dimensions/referrer.md), [Referrer Domain](/help/components/dimensions/referring-domain.md) |
| Anonymisierte Besucher-IDs | Datenerfassungsbibliotheken generieren und referenzieren eine Besucher-ID für jeden Browser, der Ihre Site besucht. Diese ID wird in einem Cookie gespeichert. Wenn eine Datenerfassungsbibliothek keinen Cookie-Identifikator festlegen kann, verwendet die Bibliothek eine Ausweichmethode zur anonymen Identifizierung von Besucherinnen und Besuchern. Bei dieser Methode werden zugehörige Treffer mit demselben Besuch verknüpft, indem die IP-Adresse der Person und die Benutzeragenten-Zeichenfolge verwendet werden. Wenn für Ihre Organisation die IP-Verschleierung aktiviert ist, wird diese Einstellung berücksichtigt. Weitere Informationen finden Sie unter [Adobe Analytics und Browser-Cookies](../cookies/cookies.md). | [Unique Visitors](/help/components/metrics/unique-visitors.md) |
| Identifizierbare Besucher-IDs | Adobe erfasst nicht automatisch benutzerdefinierte Besucher-IDs. Sie können Ihre Implementierung jedoch anpassen, um diese Daten zu erfassen. | [`visitorID`](/help/implement/vars/config-vars/visitorid.md) |
| Externe Suchbegriffe | Externe Suchdaten enthalten Keywords, die von Suchmaschinen stammen. Datenerfassungsbibliotheken suchen nach diesen Daten basierend auf der Referrer-URL. Viele moderne Suchmaschinen enthalten diese Informationen jedoch nicht mehr. | [Suchbegriff](/help/components/dimensions/search-keyword.md) |
| Interne Suchbegriffe | Interne Suchdaten enthalten Keywords, die aus den Suchfunktionen Ihrer Website oder App stammen. Adobe erfasst interne Suchdaten nicht automatisch. Sie können Ihre Implementierung jedoch anpassen, um diese Daten zu erfassen. Diese Vorgehensweise wird häufig bei Organisationen angewandt, die Adobe Analytics verwenden. | [eVar](/help/components/dimensions/evar.md) |
| Computer- und Browser-Spezifikationen | Datenerfassungsbibliotheken erfassen automatisch Browser-Hinweise mit geringer Entropie, z. B. den Browser-Typ und den Betriebssystemtyp, und ob es sich bei dem Gerät um ein Desktop- oder ein Mobilgerät handelt. Eine benutzerdefinierte Konfiguration ist erforderlich, um Hinweise mit hoher Entropie zu sammeln, z. B. die spezifische Version/den Build des Browsers, das Gerätemodell oder die Betriebssystemversion. Weitere Informationen dazu finden Sie in der [Übersicht zu Client-Hinweisen](../client-hints.md). | [Browser](/help/components/dimensions/browser.md), [Betriebssystem](/help/components/dimensions/operating-systems.md), [Mobilgeräte-Dimensionen](/help/components/dimensions/mobile-dimensions.md), [Bildschirmauflösung](/help/components/dimensions/monitor-resolution.md) |
| Informationen zur Geolokalisierung | Adobe bietet die Möglichkeit, eine detaillierte Geolokalisierung zu verhindern, indem das letzte Oktett einer IP-Adresse auf 0 gesetzt wird. Dadurch werden Geo-Informationen weniger präzise und können in den [Report Suite-Einstellungen](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md) festgelegt werden. | [Städte](/help/components/dimensions/cities.md), [Regionen](/help/components/dimensions/regions.md), [Länder](/help/components/dimensions/countries.md) |
| IP-Adresse | Adobe bietet die Möglichkeit, die IP-Adresse der Besucherinnen und Besucher beim Speichern dieser Daten zu verschleiern (Hash) oder vollständig zu entfernen. Bei Kundinnen und Kunden im EMEA-Raum ist die IP-Adresse in der Regel standardmäßig verschleiert. Unabhängig von der Verschleierungseinstellung ist die IP-Adresse nicht als Dimension in Analysis Workspace verfügbar. Sie ist nur in [Daten-Feeds](/help/export/analytics-data-feed/data-feed-overview.md) enthalten. Details zu den verfügbaren Verschleierungseinstellungen finden Sie unter [Allgemeine Kontoeinstellungen](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md) im Administratorhandbuch. | Keine |
| Formularinformationen, die auf Ihrer Site bereitgestellt werden | Alle Implementierungstypen erfordern eine Konfiguration zur Erfassung dieser Daten. Sie können diese Daten in benutzerdefinierte Variablen aufnehmen. | [eVar](/help/components/dimensions/evar.md) |
| Angeklickte Anzeigen oder Links auf Ihrer Site | Diese Daten werden erfasst, wenn [`trackExternalLinks`](/help/implement/vars/config-vars/trackexternallinks.md) oder [`trackDownloadLinks`](/help/implement/vars/config-vars/trackdownloadlinks.md) aktiviert ist. Zusätzliche Informationen, wie der Ort der Klicks, sind verfügbar, wenn Sie Activity Map aktivieren. | [Activity Map](/help/analyze/activity-map/overview.md), [Exitlink](/help/components/dimensions/exit-link.md), [Download-Link](/help/components/dimensions/download-link.md) |
| Auf Ihrer Site gekaufte Produkte | Alle Implementierungstypen erfordern eine Konfiguration zur Erfassung dieser Daten. Adobe bietet mehrere Standardvariablen, um diese Informationen zu sammeln. | [Produkt](/help/components/dimensions/product.md), [Bestellungen](/help/components/metrics/orders.md), [Umsatz](/help/components/metrics/revenue.md) |

{style="table-layout:auto"}

Weitere Variablen, unter denen Adobe potenziell Daten sammeln kann, finden Sie im Navigationsmenü unter [Übersicht der Dimensionen](/help/components/dimensions/overview.md) und [Übersicht der Metriken](/help/components/metrics/overview.md).

## Standorte für die Datenverarbeitung

Adobe besitzt drei Standorte für die Datenverarbeitung für Adobe Analytics. Diese Sites empfangen Rohdaten und verarbeiten sie in einer Report Suite, die für Datenspeicherung und Berichtsabruf optimiert ist. Diese Standorte für die Datenverarbeitung befinden sich derzeit in den USA (Oregon), Großbritannien (London) und Singapur. Weitere Informationen finden Sie unter {0[ Adobe Analytics-Sicherheitsübersicht.](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adb-analytics-security-wp.pdf){target=_blank}
