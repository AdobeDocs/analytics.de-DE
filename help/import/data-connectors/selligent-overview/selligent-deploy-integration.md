---
description: Die Bereitstellung dieser Integration erfolgt in drei Schritten.
seo-description: Die Bereitstellung dieser Integration erfolgt in drei Schritten.
seo-title: Bereitstellen der Integration
solution: Analytics
title: Bereitstellen der Integration
uuid: c578bf26-34c2-44ea-8e60-2990273f8659
translation-type: tm+mt
source-git-commit: a31f25e8a4681cf34525a7994b00580aa3aac15d

---


# Bereitstellen der Integration{#deploying-the-integration}

Die Bereitstellung dieser Integration erfolgt in drei Schritten.

## Ausführen des Integrationsassistenten{#completing-the-integration-wizard}

Um die Integration zu aktivieren, müssen Sie den Assistenten für die intelligente Integration in der Data Connectors-Oberfläche ausführen.

1. Navigieren Sie zum Bereich Data Connectors in der Adobe Experience Cloud.

   ![](assets/selligent-data_connectors.png)

1. Ziehen Sie unter "Integrationen **[!UICONTROL hinzufügen]**"das Plugin "Selligent"in Adobe Experience Cloud.

   ![](assets/selligent-add_integration.png)

   Dadurch wird die Selligent Data Connector-Integration geöffnet.

1. **Integrationseinstellungen**: Wählen Sie die gewünschte Report Suite und geben Sie unter **[!UICONTROL Integrationseinstellungen]** einen Namen für die Integration ein.

1. Geben Sie unter " **[!UICONTROL Benutzerdefinierte Werte]**"alle Informationen zum Selligent-Konto ein.

   ![](assets/selligent-general_settings.png)

1. **Variablenzuordnung**: Wählen Sie die entsprechenden reservierten eVars und Ereignisse aus den Dropdownmenüs aus:

   ![](assets/selligent-variables.png)

1. **Dateneinstellungen**: Sie können Ihre eigenen Segmente unter **[!UICONTROL Ihre Segmente]** mit Ausnahme der 3 automatisierten **[!UICONTROL Partnersegmente]** auswählen.

1. Diese Integration erfordert möglicherweise das Herunterladen einiger Datenpunkte in Ihr Selligent-Konto. Sie können unter **[!UICONTROL Zugriffsanfrage]** Zugriff auf das Gleiche gewähren.
1. Wählen Sie unter **[!UICONTROL Datenerfassung]** eine automatisierte oder manuelle Lösung (JavaScript-Plugin), um Abfragezeichenfolgenparameter aus der URL der Einstiegsseite zu erfassen. Wenn Sie eine automatisierte Lösung wählen, geben Sie den Abfragezeichenfolgenparameter für die Nachrichten-ID und die Empfänger-ID ein, die jeweils MID bzw. RID lautet. Wenden Sie sich für das JavaScript-Plug-in an Ihren Adobe-Berater.
1. **Berichtseinstellungen**: Aktivieren Sie unter **[!UICONTROL Dashboard-Erstellung]** das Kontrollkästchen, damit das Selligent-Dashboard automatisch für Sie generiert wird.

   ![](assets/selligent-report_settings.png)

1. Überprüfen Sie die Integrationszusammenfassung und klicken Sie auf **[!UICONTROL Aktivieren]**.

## Konfiguration innerhalb von Selligent{#configuration-within-selligent}

Sobald die Integration in Adobe Analytics aktiviert ist, wird eine automatische Konfiguration auf der Selligent-Seite aktiviert.

Es wurde ein Tracker erstellt, der jede E-Mail verfolgt. Falls Sie sie auf eine bestimmte Domäne begrenzen möchten, aktualisieren Sie bitte die Trackerkonfiguration.

Wir empfehlen dringend, den Verfolgungsparameter für Adobe Analytics in der URL nach vorne zu verschieben. Dadurch wird sichergestellt, dass die Adobe-Verarbeitungsregeln die Parameter aus der URL der Einstiegsseite abrufen. Aktivieren Sie die Verfolgung, indem Sie das Kontrollkästchen wie unten gezeigt aktivieren.

![](assets/selligent-tracker.png)

## Verifying the Integration{#verifying-the-integration}

Once all deployment steps have been completed you can validate that the integration is successfully transferring data.

It will take a few days for the data exchange to begin. Please make sure you contact Selligent after you activate the integration.

### Protokoll zu den Integrationsaktivitäten {#section-927e270495db479fba9578915d9ae9c9}

Navigate to your Selligent Integration within Data Connectors. Under the Support tab, you should see events like Metric Data imported and/or Classification Data imported successfully :****

![](assets/selligent-verifying.png)

### Reporting Data {#section-ebd481a162324e66bd6dc8cb4b8d2424}

View your Selligent Message reports with appropriate metrics.

1. Go to Report &amp; Analytics under Adobe Experience Cloud.
1. Wählen Sie die gewünschte Report Suite aus.
1. Under Custom Conversion, select the Message ID Reports and choose Message ID/Message Name.************
