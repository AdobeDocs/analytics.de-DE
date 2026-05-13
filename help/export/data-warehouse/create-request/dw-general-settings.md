---
description: In diesen Schritten wird beschrieben, wie Sie eine Data Warehouse-Anfrage erstellen.
title: Allgemeine Einstellungen für Data Warehouse-Anfragen
feature: Data Warehouse
exl-id: f564d5a9-78a2-431e-987a-78c4b0b9d31e
TQID: https://experienceleague.adobe.com/-FIw9vHeGpDbpd09GgRQqgK-5-srLyNCjDCLLhPBEYI
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 399
ht-degree: 29%

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
   | Anfragename | Dieser Name wird beim Verwalten von Anfragen auf der Data Warehouse-Hauptseite angezeigt. |
   | Datumsbereiche | Wählen Sie den Datumsbereich aus, der in den Bericht aufgenommen werden soll. <p>Sie können benutzerdefinierte Datumswerte oder einen voreingestellten Datumsbereich auswählen. Vordefinierte Bereiche sind relativ zum Datum, an dem der Bericht gesendet wird.</p><p>Die folgenden Voreinstellungsoptionen sind verfügbar:</p><ul><li>Heute</li><li>Gestern</li><li>Letzte 7 Tage</li><li>Letzte 30 Tage</li><li>Diese Woche</li><li>Letzte Woche</li><li>Letzte 2 Wochen</li><li>Letzte 3 Wochen</li><li>Letzte 4 Wochen</li><li>Diesen Monat</li><li>Letzter Monat</li><li>Letzte Stunde</li></ul> |
   | Granularität | Die Zeitgranularität. Gültige Werte sind „Keine“, „Stunde“, „Tag“, „Woche“, „Monat“, „Quartal“ und „Jahr“.<p>Die Berichtsgranularität erfordert eine zusätzliche Verarbeitungszeit. Wenn Sie monatliche Granularität über ein ganzes Jahr hinweg melden, werden Ihre Berichte viel schneller verarbeitet, wenn Sie für jeden Monat eine Berichtsanfrage senden.</p><p>**Hinweis:** Bei der Anwendung der Granularität in einer Data Warehouse-Anfrage wird dem Bericht die Spalte „Datum“ hinzugefügt. Je nach ausgewählter Granularität ändert sich das Datumsformat wie folgt:</p><ul><li>**Stundengranularität**:<ul> <li>**format**: `mmmm d, yyyy` Stunde `H`</li><li>**Beispiel**: 1. Januar 20XX, Stunde 0 </li></ul><li>**Tägliche Granularität**:<ul> <li>**Format**: `mmmm d, yyyy`</li><li>**Beispiel**: 1. Januar 20XX</li></ul><li>**Wöchentliche**:<ul> <li>**format**: Woche `w, yyyy`</li><li>**Beispiel**: Woche 1, 20XX </li></ul><li>**Monatliche Granularität**:<ul> <li>**Format**: `mmmm yyyy`</li><li>**Beispiel**: 20XX. Januar </li></ul><li>**Vierteljährliche Granularität**:<ul> <li>**format**: `q` Quartal `yyyy`</li><li>**Beispiel**: 1. Quartal 20XX </li></ul><li>**Jährliche**:<ul> <li>**Format**: `yyyy`</li><li>**Beispiel**: 20XX</li></ul> |
   | Für Benutzende in Ihrer Organisation verfügbar machen | Alle Data Warehouse-Anfragen sind nur für Sie und etwaige Systemadministratoren sichtbar. Aktivieren Sie diese Option, wenn die Anfrage für alle Personen in Ihrer Organisation sichtbar sein soll. <p>Die Aktivierung dieser Option ist nützlich, wenn Sie möchten, dass andere Benutzer in Ihrem Unternehmen bei der Erstellung oder Aktualisierung der Anfrage helfen.</p> |

   {style="table-layout:auto"}

1. Fahren Sie mit der Konfiguration Ihrer Data Warehouse-Anfrage auf der Registerkarte [!UICONTROL **Bericht erstellen**] fort. Weitere Informationen finden Sie unter [Erstellen eines Berichts für eine Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/dw-request-build-report.md).
