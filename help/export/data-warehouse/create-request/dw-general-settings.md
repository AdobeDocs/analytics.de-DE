---
description: In diesen Schritten wird beschrieben, wie Sie eine Data Warehouse-Anfrage erstellen.
title: Allgemeine Einstellungen für Data Warehouse-Anfragen
feature: Data Warehouse
exl-id: f564d5a9-78a2-431e-987a-78c4b0b9d31e
source-git-commit: 1e1a26b8595ca026fb049322125a6f91d9d5513c
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 33%

---

# Allgemeine Einstellungen für Data Warehouse-Anfragen

Beim Erstellen einer Data Warehouse-Anfrage stehen verschiedene Konfigurationsoptionen zur Verfügung. Die folgenden Informationen beschreiben, wie Sie allgemeine Einstellungen für die Anfrage konfigurieren.

Informationen zum Erstellen einer Anfrage sowie Links zu anderen wichtigen Konfigurationsoptionen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

So konfigurieren Sie allgemeine Einstellungen für eine Data Warehouse-Anfrage:

1. Beginnen Sie mit der Erstellung einer Data Warehouse-Anfrage in Adobe Analytics, indem Sie **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **Hinzufügen**] auswählen.

   Weitere Informationen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. Wählen Sie auf der Seite Neue Data Warehouse-Anfrage die Registerkarte [!UICONTROL **Allgemeine Einstellungen**] aus.

   ![Registerkarte „Berichtsziel“](assets/dw-general-settings.png)

1. Füllen Sie die folgenden Felder aus:

   | Option | Funktion |
   |---------|----------|
   | Anfragename | Dieser Name erscheint auf der Hauptseite von Data Warehouse beim Verwalten von Anfragen. |
   | Datumsbereiche | Wählen Sie den Datumsbereich aus, der in den Bericht aufgenommen werden soll. <p>Sie können benutzerdefinierte Datumswerte oder einen voreingestellten Datumsbereich auswählen. Vordefinierte Bereiche sind relativ zum Datum, an dem der Bericht gesendet wird.</p><p>Die folgenden Voreinstellungsoptionen sind verfügbar:</p><ul><li>Am aktuellen Tag</li><li>Am Vortag</li><li>Letzte 7 Tage</li><li>Letzte 30 Tage</li><li>Diese Woche</li><li>Letzte Woche</li><li>Letzte 2 Wochen</li><li>Letzte 3 Wochen</li><li>Letzte 4 Wochen</li><li>Diesen Monat</li><li>Letzter Monat</li><li>Letzte Stunde</li></ul> |
   | Granularität | Die Zeitgranularität. Gültige Werte sind „Keine“, „Stunde“, „Tag“, „Woche“, „Monat“, „Quartal“ und „Jahr“.<p>Die Berichtgranularität verlängert die Verarbeitungszeit. Wenn Sie die monatliche Granularität über ein ganzes Jahr in einem Bericht darstellen, so wird der Bericht erheblich schneller verarbeitet, wenn Sie je eine Berichtanforderung für jeden Monat senden.</p><p>**Hinweis:** Bei der Anwendung der Granularität in einer Data Warehouse-Anfrage wird dem Bericht die Spalte „Datum“ hinzugefügt. Je nach ausgewählter Granularität ändert sich das Datumsformat wie folgt:</p><ul><li>**Stundengranularität**:<ul> <li>**format**: `mmmm d, yyyy` Stunde `H`</li><li>**Beispiel**: 1. Januar 20XX, Stunde 0 </li></ul><li>**Tägliche Granularität**:<ul> <li>**Format**: `mmmm d, yyyy`</li><li>**Beispiel**: 1. Januar 20XX</li></ul><li>**Wöchentliche**:<ul> <li>**format**: Woche `w, yyyy`</li><li>**Beispiel**: Woche 1, 20XX </li></ul><li>**Monatliche Granularität**:<ul> <li>**Format**: `mmmm yyyy`</li><li>**Beispiel**: 20XX. Januar </li></ul><li>**Vierteljährliche Granularität**:<ul> <li>**format**: `q` Quartal `yyyy`</li><li>**Beispiel**: 1. Quartal 20XX </li></ul><li>**Jährliche**:<ul> <li>**Format**: `yyyy`</li><li>**Beispiel**: 20XX</li></ul> |
   | Für Benutzende in Ihrer Organisation verfügbar machen | Alle Data Warehouse-Anfragen sind nur für Sie und etwaige Systemadministratoren sichtbar. Aktivieren Sie diese Option, wenn die Anfrage für alle Personen in Ihrer Organisation sichtbar sein soll. <p>Die Aktivierung dieser Option ist nützlich, wenn Sie möchten, dass andere Benutzer in Ihrem Unternehmen bei der Erstellung oder Aktualisierung der Anfrage helfen.</p> |

   {style="table-layout:auto"}

1. Fahren Sie mit der Konfiguration Ihrer Data Warehouse-Anfrage auf der Registerkarte [!UICONTROL **Bericht erstellen**] fort. Weitere Informationen finden Sie unter [Erstellen eines Berichts für eine Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/dw-request-build-report.md).
