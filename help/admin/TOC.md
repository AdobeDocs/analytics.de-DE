---
product: analytics
audience: admin
user-guide-title: Administratorhandbuch für Analytics
breadcrumb-title: Administratorhandbuch
user-guide-description: Erfahren Sie mehr über Analytics-Verwaltungsaufgaben, wie z. B. das Verwalten von Benutzern und Produkten in der Experience Cloud Admin Console, das Konfigurieren von Report Suites und mehr.
source-git-commit: 35675c2e65456a175d1516dd421b80d2af809286
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 99%

---


# Administratorhandbuch für Adobe Analytics {#admin}

+ [Administratorhandbuch für Analytics](home.md)
+ [Versionshinweise zu Analytics](https://experienceleague.adobe.com/de/docs/analytics/release-notes/latest)
+ Adobe Admin Console {#admin-console}
   + [Überblick](admin-console/home.md)
   + [Adobe Analytics-Handbuch für erste Administratoren](admin-console/first-admin-guide.md)
   + [Administratorrollen in Adobe Analytics](admin-console/admin-roles-in-analytics.md)
   + Zusammenfassung der Berechtigungen für Analytics-Tools {#permissions}
      + [Produktprofile für Adobe Analytics](admin-console/permissions/product-profile.md)
      + [Produktprofil-Berechtigungen für Report Suite-Werkzeuge](admin-console/permissions/report-suite-tools.md)
      + [Produktprofilberechtigungen für Analytics-Werkzeuge](admin-console/permissions/analytics-tools.md)
+ Admin-Tools für Analytics {#admin-tools}
   + [Übersicht über Admin-Tools](tools/c-admin-tools.md)
   + [Code-Manager](tools/code-manager-admin.md)
   + [Analytics-Inventar](tools/analytics-inventory.md)
   + [Datenquellen](tools/data-sources.md)
   + [Nach IP-Adresse ausschließen](tools/exclude-ip.md)
   + [Protokolle](tools/logs.md)
   + Reporting Activity Manager {#reporting-activity-manager}
      + [Überblick](tools/reporting-activity-manager/reporting-activity-overview.md)
      + [Anzeigen der Berichtsaktivität](tools//reporting-activity-manager/reporting-activity.md)
      + [Abbrechen von Berichtsanfragen](tools/reporting-activity-manager/reporting-activity-cancel-requests.md)
   + Komponenten-Migration {#component-migration}
      + [Vorbereitung der Migration](tools/component-migration/prepare-component-migration.md)
      + [Migrations-Workflow](tools/component-migration/component-migration.md)
   + Report Suite Manager {#manage-report-suites}
      + Bearbeiten der Einstellungen einer Report Suite {#edit-report-suite}
         + Allgemein {#report-suite-general}
            + [Allgemeine Kontoeinstellungen](tools/manage-rs/edit-settings/general/general-acct-settings-admin.md)
            + [Interne URL-Filter](tools/manage-rs/edit-settings/general/internal-url-filter-admin.md)
            + [Anpassen von Kalendern](tools/manage-rs/edit-settings/general/custom-calendar.md)
            + Paid-Search-Erkennung {#paid-search-detection}
               + [Übersicht über die Paid-Search-Erkennung](tools/manage-rs/edit-settings/general/paid-search-detection/paid-search-detection.md)
               + [Konfigurieren der Erkennung von Paid Search](tools/manage-rs/edit-settings/general/paid-search-detection/t-paid-search-detection.md)
            + Verarbeitungsregeln {#processing-rules}
               + [Überblick](tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md)
               + [Benutzeroberfläche](tools/manage-rs/edit-settings/general/processing-rules/pr-interface.md)
               + [Verlauf ansehen](tools/manage-rs/edit-settings/general/processing-rules/pr-view-history.md)
               + [Kopierregeln](tools/manage-rs/edit-settings/general/processing-rules/pr-copy.md)
               + [Verfügbare Dimensionen und Metriken](tools/manage-rs/edit-settings/general/processing-rules/pr-variables.md)
               + [Anwendungsfälle](tools/manage-rs/edit-settings/general/processing-rules/pr-use-cases.md)
            + Bot-Regeln {#bot-removal}
               + [Entfernung von Bots](tools/manage-rs/edit-settings/general/bot-removal/bot-removal.md)
               + [Verstehen und Konfigurieren von Bot-Regeln](tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md)
               + [Allgemeine Bot-Signaturen](tools/manage-rs/edit-settings/general/bot-removal/bot-signatures.md)
               + [Bot-Ausschlussmethoden](tools/manage-rs/edit-settings/general/bot-removal/bot-exclusion-methods.md)
            + [Datenschutzeinstellungen](tools/manage-rs/edit-settings/general/privacy-settings.md)
            + [Konfiguration von Zeitstempeln](tools/manage-rs/edit-settings/general/timestamp-configuration.md)
            + Serverseitige Weiterleitung {#server-side-forwarding}
               + [Übersicht über die Server-seitige Weiterleitung](tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf.md)
               + [DSGVO/ePrivacy – Einhaltung und Server-seitige Weiterleitung](tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf-gdpr.md)
               + [Anforderungen an die Server-seitige Weiterleitung](tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf-requirements.md)
               + [Daten- und Codereferenz für die Server-seitige Weiterleitung](tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf-reference.md)
               + [Überprüfen der Server-seitigen Weiterleitungsimplementierung](tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf-verify.md)
               + [Häufig gestellte Fragen zur Server-seitigen Weiterleitung](tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf-faq.md)
         + Traffic {#traffic-variables}
            + [Traffic-Variablen](tools/manage-rs/edit-settings/c-traffic-variables/traffic-var.md)
            + [Traffic-Klassifizierung](tools/manage-rs/edit-settings/c-traffic-variables/traffic-classifications.md)
            + [Beschreibung benutzerspezifischer Berichte](tools/manage-rs/edit-settings/c-traffic-variables/custom-desc-admin.md)
         + Konversion {#conversion-variables}
            + [Konversionsvariablen](tools/manage-rs/edit-settings/conversion-var-admin/conversion-var-admin.md)
            + [Suchmethoden](tools/manage-rs/edit-settings/conversion-var-admin/finding-methods.md)
            + [Konversionsklassifizierungen](tools/manage-rs/edit-settings/conversion-var-admin/conversion-classifications.md)
            + Unique-Visitor-Variable {#unique-visitor-variable}
               + [Festlegen der Unique-Visitor-Variable](tools/manage-rs/edit-settings/conversion-var-admin/unique-visitor-variable-admin/t-unique-visitor-variable.md)
               + [Anwendungsfall – Extrahieren von Besucher-IDs](tools/manage-rs/edit-settings/conversion-var-admin/unique-visitor-variable-admin/extract-visitorids-usecase.md)
            + [Erfolgsereignisse](tools/manage-rs/edit-settings/conversion-var-admin/c-success-events/success-event.md)
            + [Klassifizierungshierarchien](tools/manage-rs/edit-settings/conversion-var-admin/classification-hierarchies.md)
            + [Listenvariablen](tools/manage-rs/edit-settings/conversion-var-admin/list-var-admin.md)
            + [Merchandising-eVars](tools/manage-rs/edit-settings/conversion-var-admin/merchandising-evars.md)
         + Marketing-Kanäle {#marketing-channels}
            + [Marketing-Kanal-Manager](tools/manage-rs/edit-settings/marketing-channels/c-channels.md)
            + [Marketing-Kanal-Verarbeitungsregeln](tools/manage-rs/edit-settings/marketing-channels/c-rules.md)
            + [Klassifizierungen von Marketing-Kanälen](tools/manage-rs/edit-settings/marketing-channels/classifications-mchannel.md)
            + [Ablauf von Marketing-Kanälen](tools/manage-rs/edit-settings/marketing-channels/visitor-engagement.md)
         + Traffic-Management {#traffic-management}
            + [Überblick](tools/manage-rs/edit-settings/c-traffic-management/traffic-management.md)
            + [Planen einer Spitze](tools/manage-rs/edit-settings/c-traffic-management/t-traffic-schedule-spike.md)
            + [Dauerhafter Traffic](tools/manage-rs/edit-settings/c-traffic-management/t-traffic-permanent.md)
         + [Standardmetriken](tools/manage-rs/edit-settings/default-metrics.md)
         + App-Management {#app-management}
            + [App-Berichterstellung](tools/manage-rs/edit-settings/app-reporting.md)
            + [App-Klassifizierungen](tools/manage-rs/edit-settings/app-classifications.md)
         + [Medienverwaltung](tools/manage-rs/edit-settings/media-management.md)
         + [Activity Map](tools/manage-rs/edit-settings/activity-map.md)
         + [AEM](tools/manage-rs/edit-settings/adobe-experience-manager.md)
         + [Adobe Campaign](tools/manage-rs/edit-settings/adobe-campaign.md)
         + [Datenschutzberichte](tools/manage-rs/edit-settings/privacy-reporting.md)
         + Document Cloud-Verwaltung {#doc-cloud-mgt}
            + [Konfigurieren von Document Cloud mit Adobe Analytics](tools/manage-rs/edit-settings/document-cloud-mgt.md)
            + [Konfigurieren von Document Cloud-Berichten](tools/manage-rs/edit-settings/document-cloud-config.md)
         + [Konfiguration von Advertising Analytics](tools/manage-rs/edit-settings/advertising-analytics-config.md)
         + Echtzeit {#real-time-reports}
            + [Übersicht über Echtzeitberichte](tools/manage-rs/edit-settings/realtime/realtime.md)
            + [Konfiguration von Echtzeitberichten](tools/manage-rs/edit-settings/realtime/t-realtime-admin.md)
            + [Unterstützte Echtzeit-Metriken und -Dimensionen](tools/manage-rs/edit-settings/realtime/realtime-metrics.md)
      + [Verwalten von Report Suites](tools/manage-rs/report-suites-admin.md)
      + [Globale Report Suites](tools/manage-rs/rollup-report-suite.md)
      + [Speichern einer Report Suite-Suche](tools/manage-rs/t-report-suite-saved-search.md)
      + [Herunterladen von Report Suite-Einstellungen](tools/manage-rs/t-download-rs-settings.md)
      + Neue Report Suite {#c-new-report-suite}
         + [Erstellen einer Report Suite](tools/manage-rs/new-rs/t-create-a-report-suite.md)
         + [Erstellen einer Report Suite-Gruppe](tools/manage-rs/new-rs/t-create-rs-group.md)
         + [Neue Report Suite – Einstellungen](tools/manage-rs/new-rs/new-report-suite.md)
         + [Aus einer Quell-Report Suite nicht kopierte Einstellungen](tools/manage-rs/new-rs/settings-not-copied-from-rs.md)
      + Report Suite-Vorlagen {#report-suite-templates}
         + [Übersicht über Report Suite-Vorlagen](tools/manage-rs/rs-templates/report-suite-templates.md)
         + [Aggregatorportal](tools/manage-rs/rs-templates/aggregator-portal.md)
         + [Handel](tools/manage-rs/rs-templates/commerce-admin.md)
         + [Inhalte und Medien](tools/manage-rs/rs-templates/content-media.md)
         + [Standardvorlage](tools/manage-rs/rs-templates/default-rs-template.md)
         + [Finanzdienste](tools/manage-rs/rs-templates/financial-services.md)
         + [Job-Portal](tools/manage-rs/rs-templates/job-portal.md)
         + [Lead-Generierung](tools/manage-rs/rs-templates/lead-generation.md)
         + [Unterstützungsmedien](tools/manage-rs/rs-templates/support-media.md)
   + Unternehmenseinstellungen {#company-settings}
      + [Übersicht über Unternehmenseinstellungen](tools/company/c-company-settings.md)
      + [Sicherheits-Manager](tools/company/security-manager.md)
      + [Web-Services](tools/company/web-services-admin.md)
      + [Report Builder-Berichte](tools/company/report-builder-reports-admin.md)
      + [Single Sign-on](tools/company/single-signon-admin.md)
      + [Ausblenden von Report Suites](tools/company/c-hide-report-suites.md)
      + [Voreinstellungs-Manager](tools/company/preferences-manager.md)
      + [Ausstehende Aktionen](tools/company/pending-actions-admin.md)
      + [Funktionszugriffsebenen](tools/company/feature-access-levels.md)
   + Datenschutzkennzeichnung {#privacy-labeling}
      + [Überblick](tools/privacy-labeling/labeling-overview.md)
      + [Datenschutzkennzeichnungen für Analytics-Komponenten](tools/privacy-labeling/labels.md)
      + [Anzeigen/Verwalten von Datenschutzkennzeichnungen von Report Suites](tools/privacy-labeling/view-settings.md)
      + [Best Practices für Beschriftungen](tools/privacy-labeling/best-practices.md)
      + [Beschriftungsbeispiel](tools/privacy-labeling/examples.md)
      + [Namespaces](tools/privacy-labeling/namespaces.md)
   + Nutzung der Server-Aufrufe {#server-call-usage}
      + [Übersicht zur Nutzung von Server-Aufrufen](tools/server-call-usage/overage-overview.md)
      + [Anzeigen der aktuellen Nutzung der Server-Aufrufe](tools/server-call-usage/server-call-usage-dashboard.md)
      + [Anzeigen der Nutzung der Report Suite](tools/server-call-usage/report-suite-usage.md)
      + [Warnhinweise zur Nutzung von Server-Aufrufen](tools/server-call-usage/scu-alerts.md)
      + [Häufig gestellte Fragen zur Nutzung von Server-Aufrufen](tools/server-call-usage/overage-faq.md)
   + Verwalten von Benutzenden und Produkten (veraltet) {#user-product-management}
      + [Verwalten von Benutzenden und Produkten (veraltet)](tools/user-management/user-management.md)
      + [Verwalten von älteren Benutzerkonten, Assets und Ablaufdaten](tools/user-management/users-assets.md)
      + Migrieren von Benutzenden zur Adobe Admin Console {#migrate-users}
         + [Analytics-Benutzermigration zur Admin Console](tools/user-management/user-migration/c-migration-tool.md)
         + [Migrieren von Analytics-Benutzerkonten für Adobe IDs](tools/user-management/user-migration/t-migrate-users.md)
         + [Migrieren von Analytics-Benutzerkonten für Enterprise und Federated IDs](tools/user-management/user-migration/migrate-enterprise.md)
         + [Deaktivieren von veralteten Anmeldedaten](tools/user-management/user-migration/t-disable-legacy-login.md)
         + [Von der Migration betroffene APIs](tools/user-management/user-migration/developer.md)
+ [Admin-API](c-admin-api/c-admin-api.md)
+ [Häufig gestellte Fragen zur Einstellung der Adobe Analytics 1.4-API](c-admin-api/c-admin-14-api-eol.md)

