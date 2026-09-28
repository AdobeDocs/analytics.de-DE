---
description: Überblick über die von Adobe Analytics erfassten Daten und weitere Datenschutzaspekte.
keywords: Privatsphäre
title: Datenschutzübersicht
feature: Data Governance
exl-id: 71c83106-a047-47d7-9a70-4a24595e3d0a
TQID: 'https://experienceleague.adobe.com/pIwRuvYPl6dcv-FEgSdeUZQlfqI1J8GJhbHeef1JdOI'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
    internal-label: Analysis Workspace
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
    internal-label: Data configuration and collection
subfeature_v2:
  - id: b99602d0-836e-4dbb-979f-c0dec53f883c
    internal-label: Privacy
  - id: f7fb4c71-5c39-4655-ba2d-b3b189287ab7
    internal-label: Data governance
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 9a50beeb0aa51cf9f4baf212566947c14029ce8e
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 88%
---
# Datenschutzübersicht

Adobe möchte Ihr Unternehmen in die Lage versetzen, die geltenden Gesetze und Vorschriften einzuhalten. Weitere Informationen finden Sie unter {](https://www.adobe.com/de/privacy/experience-cloud.html){target=_blank}}Adobe CX Enterprise-Datenschutz. [Zwischen Adobe Analytics und Ihrer Organisation agiert Adobe als „Auftragsverarbeiter“ und Sie sind der „Datenverantwortliche“ (oder ein entsprechendes Äquivalent gemäß den geltenden Datenschutzgesetzen). Es ist Sache Ihrer Organisation offenzulegen, wie Sie die Adobe-Produkte und -Dienste verwenden, da ausschließlich Ihre Organisation kontrolliert, wie die Adobe-Lösungen implementiert werden. Bei der Verwendung von Adobe Analytics ist Ihre Organisation für die Einhaltung Ihrer eigenen Datenschutzrichtlinie, Ihres Service-Vertrags mit Adobe und aller geltenden Gesetze verantwortlich.

Adobe empfiehlt dringend die Einhaltung der folgenden übergreifenden Konzepte:

* **Wenn Sie personenbezogene Daten erfassen, stellen Sie sicher, dass Sie die Datenschutzgesetze und -vorschriften einhalten.** Benutzerdefinierte Variablen ermöglichen es Ihnen, praktisch alles zu erfassen, auf das Sie zugreifen können. Sie müssen jedoch auch die Datenschutzrichtlinien Ihres Unternehmens und die geltenden Gesetze berücksichtigen.
* **Stellen Sie Ihren Kunden leicht auffindbare und leicht verständliche Datenschutzinformationen für Ihr Unternehmen zur Verfügung.** Zu den hilfreichen Informationen gehören Opt-out-Links, Informationen zur Verwendung ihrer Browser-Daten und dazu, wie Sie die Services von Adobe verwenden bzw. deren Nutzung planen.
* **Achten Sie sowohl auf lokale als auch auf internationale Gesetze, die für Sie gelten.** Wenn Ihr Unternehmen auf globaler Ebene tätig ist, können einige internationale Gesetze angewendet werden.

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
| Referrer-Daten | Datenerfassungsbibliotheken erfassen standardmäßig die Referrer-URL, wenn eine Besucherin oder ein Besucher auf Ihre Website gelangt. Sie können Ihre Implementierung anpassen, um Daten in der Abfragezeichenfolge eines Referrers zu erfassen. Diese Vorgehensweise wird häufig bei Kampagnen und beim Tracking der Werbewirksamkeit angewandt. | [Referrer](/help/components/dimensions/referrer.md), [Referrer Domain](/help/components/dimensions/referring-domain.md) |
| Anonymisierte Besucher-IDs | Datenerfassungsbibliotheken generieren und referenzieren eine Besucher-ID für jeden Browser, der Ihre Site besucht. Diese ID wird in einem Cookie gespeichert. Wenn eine Datenerfassungsbibliothek keinen Cookie-Identifikator festlegen kann, verwendet die Bibliothek eine Ausweichmethode zur anonymen Identifizierung von Besucherinnen und Besuchern. Bei dieser Methode werden zugehörige Treffer mit demselben Besuch verknüpft, indem die IP-Adresse der Besucherin bzw. des Besuchers und die Benutzeragenten-Zeichenfolge verwendet werden. Wenn für Ihre Organisation die IP-Verschleierung aktiviert ist, wird diese Einstellung berücksichtigt. Weitere Informationen finden Sie unter [Adobe Analytics und Browser-Cookies](../cookies/cookies.md). | [Unique Visitors](/help/components/metrics/unique-visitors.md) |
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

Adobe unterhält drei Standorte für die Datenverarbeitung für Adobe Analytics. Diese Sites empfangen Rohdaten und verarbeiten sie in einer Report Suite, die für Datenspeicherung und Berichtsabruf optimiert ist. Diese Standorte für die Datenverarbeitung befinden sich derzeit in den USA (Oregon), Großbritannien (London) und Singapur. Weitere Informationen finden Sie unter {0](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adb-analytics-security-wp.pdf){target=_blank} Adobe Analytics-Sicherheitsübersicht.[
