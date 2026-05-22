---
description: Die Registerkarte „Nutzung der Report Suite“ bietet Daten über die Server-Nutzung jeder Report Suite aller Anmeldeunternehmen innerhalb der aktuellen Nutzungsperiode, die mit Ihrem Abrechnungsunternehmen zusammenhängen.
title: Anzeigen der Nutzung der Report Suite
feature: Server Call Usage
exl-id: bedd4ed8-1c8b-45fd-a059-fed88e9fbe73
role: Admin
TQID: 'https://experienceleague.adobe.com/sA3dNQtSIT-j0SnIWh7nPtbRBwk-jQ1z01NoEuReTys'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
subfeature_v2:
  - id: c9d85838-8d05-4bc7-9f18-30ec779251bc
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 301a0341e725ca15f1700046528ea5f42969add4
workflow-type: tm+mt
source-wordcount: 436
ht-degree: 49%

---

# Anzeigen der Nutzung der Report Suite

Die Registerkarte „Nutzung der Report Suite“ bietet Daten über die Server-Nutzung jeder Report Suite aller Anmeldeunternehmen innerhalb der aktuellen Nutzungsperiode, die mit Ihrem Abrechnungsunternehmen zusammenhängen.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Nutzung der Server-Aufrufe]** > **[!UICONTROL Nutzung der Report Suite]**

>[!IMPORTANT]
>
>Wenn eine Report Suite nicht mit einer CX Enterprise-Organisation verknüpft ist, werden ihre Nutzungsdaten nicht in diesem Dashboard angezeigt. Außerdem kann eine Abrechnungs-ID mit mehreren CX Enterprise-Organisationen verknüpft sein. Es besteht nicht immer eine 1:1-Beziehung zwischen einer Organisation und einer Abrechnungs-ID.

Das Report Suite-Nutzungs-Dashboard

* Zeigt die Nutzung der Server-Aufrufe durch den aktuellen Nutzungszeitraum (alle Aufrufe, Primär, Sekundär, mobil, Primär, mobil Sekundär) für jede Report Suite in Ihrem CX Enterprise-Unternehmen.
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
| Enthaltene Aufruftypen | Legen Sie eine beliebige Kombination aus Folgendem fest: Alle Aufrufe (Standard), Primär, Sekundär, Primär mobil, Sekundär mobil. |
| Zeitraum | Sie können die aktuelle Nutzungsperiode auswählen oder selbst einen Zeitraum definieren.  Wenn Sie selbst einen Zeitraum definieren möchten, dann geben Sie bitte einen Beginn des Zeitraums und ein Ende des Zeitraums ein. <br>**Hinweis:** Sie können keine Nutzungsdaten herunterladen, die vor Januar 2015 aufgezeichnet wurden</br>. |

{style="table-layout:auto"}

1. Klicken Sie auf **[!UICONTROL Herunterladen]**.

Im Folgenden finden Sie einen Screenshot, wie die heruntergeladene .csv-Datei aussieht. Sie enthält eine Spalte für die Report Suite-ID. Die Report Suite-ID gibt eine eindeutige ID an, die nur alphanumerische Zeichen enthalten darf. Diese ID kann nach der Erstellung einer Report Suite nicht mehr geändert werden.

![](/help/admin/tools/server-call-usage/assets/download-usage.png)
