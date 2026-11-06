---
description: Die Registerkarte „Report Suite-Nutzung“ bietet Server-Nutzungsdaten für jede Report Suite für den aktuellen Nutzungszeitraum in allen Anmeldeunternehmen, die mit Ihrem Abrechnungsunternehmen verknüpft sind.
title: Anzeigen der Nutzung der Report Suite
feature: Server Call Usage
exl-id: bedd4ed8-1c8b-45fd-a059-fed88e9fbe73
role: Admin
TQID: 'https://experienceleague.adobe.com/sA3dNQtSIT-j0SnIWh7nPtbRBwk-jQ1z01NoEuReTys'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
    internal-label: Dashboards
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
    internal-label: Admin Tools
subfeature_v2:
  - id: c9d85838-8d05-4bc7-9f18-30ec779251bc
    internal-label: Server call usage
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 0ba418a49e6a226540e0791f0138027566022d6f
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 50%
---
# Anzeigen der Nutzung der Report Suite

Die Registerkarte „Nutzung der Report Suite“ bietet Daten über die Server-Nutzung jeder Report Suite aller Anmeldeunternehmen innerhalb der aktuellen Nutzungsperiode, die mit Ihrem Abrechnungsunternehmen zusammenhängen.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Nutzung der Server-Aufrufe]** > **[!UICONTROL Nutzung der Report Suite]**

>[!IMPORTANT]
>
>Wenn eine Report Suite nicht mit einer Adobe-Organisation verknüpft ist, werden ihre Nutzungsdaten nicht in diesem Dashboard angezeigt. Außerdem kann eine Abrechnungs-ID mit mehreren Organisationen verknüpft sein. Es besteht nicht immer eine 1:1-Beziehung zwischen einer Organisation und einer Abrechnungs-ID.

Das Report Suite-Nutzungs-Dashboard

* Zeigt die Nutzung der Server-Aufrufe durch den aktuellen Nutzungszeitraum (alle Aufrufe, Primär, Sekundär, mobil, Primär, mobil Sekundär) für jede Report Suite in Ihrem Unternehmen.
* Zeigt den Prozentsatz der Gesamtauslastung pro Server-Aufrufkategorie.
* Wird täglich aktualisiert.
* Ist herunterladbar.
* Lässt Sie auf die Benutzeroberfläche **[!UICONTROL Warnhinweise verwalten]** zugreifen.

![](/help/admin/tools/server-call-usage/assets/report-suite-usage.png)

## Dashboard-Einstellungen {#settings}

| Spalte | Definition |
|--- |--- |
| Report Suite-Name | Anzeigename der Report Suite |
| Alle Aufrufe (% der Gesamtheit) | Alle Server-Aufrufe, die im aktuellen Nutzungszeitraum anfallen. |
| Primäre Aufrufe (%) | Alle primären Server-Aufrufe (und ihr Prozentsatz der Gesamtheit), die im aktuellen Nutzungszeitraum getätigt wurden. |
| Sekundäre Aufrufe (%) | Alle sekundären Server-Aufrufe (und ihr Prozentsatz der Gesamtheit), die im aktuellen Nutzungszeitraum getätigt wurden. |
| Primär für Mobilgeräte (%) | Alle im aktuellen Nutzungszeitraum angefallenen mobilen primären Server-Aufrufe (und deren Prozentsatz an der Gesamtsumme). |
| Sekundär für Mobilgeräte (%) | Alle im aktuellen Nutzungszeitraum angefallenen sekundären Server-Aufrufe für Mobilgeräte (und ihr Prozentsatz an der Gesamtsumme). |

{style="table-layout:auto"}

## Nutzungsbericht herunterladen {#download}

Mit dieser Option können Sie Nutzungsdaten und Daten aus Zeiträumen vor der aktuellen Nutzungsperiode herunterladen (bis Januar 2015). Der Bericht wird als CSV-Datei heruntergeladen.

1. Wählen Sie mindestens eine Report Suite.
1. Klicken Sie auf **[!UICONTROL Bericht herunterladen]**.

   ![](/help/admin/tools/server-call-usage/assets/download_report.png)

| Berichtselement | Beschreibung |
|--- |--- |
| Dateiname | Hartkodierter Name: Gebrauchsbericht `day and time of report creation.csv` |
| Enthaltene Report Suites | Alle Report Suites, die Sie auf der Seite Nutzung des Berichtsservers ausgewählt haben, sind in dieser Liste enthalten. |
| Enthaltene Aufruftypen | Legen Sie eine beliebige Kombination aus Folgendem fest: Alle Aufrufe (Standard), Primär, Sekundär, Mobile primär, Mobile sekundär. |
| Zeitraum | Sie können die aktuelle Nutzungsperiode auswählen oder einen benutzerdefinierten Zeitraum festlegen.  Für einen benutzerdefinierten Zeitraum geben Sie den Zeitraumbeginn und das Zeitraumende an. <br>**Hinweis:** Sie können keine Nutzungsdaten herunterladen, die vor Januar 2015 aufgezeichnet wurden</br>. |

{style="table-layout:auto"}

1. Klicken Sie auf **[!UICONTROL Herunterladen]**.

Im Folgenden sehen Sie einen Screenshot, wie die heruntergeladene .csv-Datei aussieht. Sie enthält eine Spalte für die Report Suite-ID. Die Report Suite-ID gibt eine eindeutige ID an, die nur alphanumerische Zeichen enthalten darf. Diese ID kann nach der Erstellung einer Report Suite nicht mehr geändert werden.

![](/help/admin/tools/server-call-usage/assets/download-usage.png)
