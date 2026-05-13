---
description: Fügen Sie Warnhinweise zur Nutzung von Server-Aufrufen hinzu oder verwalten Sie diese. Wenn Sie einen Warnhinweis einrichten, dann gilt dieser für alle Report Suites und Anmeldeunternehmen eines Abrechnungsunternehmens.
title: Warnhinweise zur Nutzung von Server-Aufrufen
feature: Server Call Usage
exl-id: 35926566-c570-4ed2-9bbc-0906518bcf64
role: Admin
TQID: https://experienceleague.adobe.com/aF3SxS36Y1xQN-saS6NTRJoN6H5XwgCx2iRmWPvUPm0
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: e93b8c4c-c5f7-45f8-9abe-9b710f53f502
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 517
ht-degree: 49%

---

# Warnhinweise zur Nutzung von Server-Aufrufen

Wenn Sie einen Warnhinweis einrichten, dann gilt dieser für alle Report Suites und Anmeldeunternehmen eines Abrechnungsunternehmens.

Warnhinweise zur Nutzung von Server-Aufrufen sind Teil der Benutzeroberfläche [Warnhinweise](/help/components/alerts/alert-manager.md).

Diese Kategorie enthält **standardmäßig einen Warnhinweis**, der innerhalb jedes Anmeldeunternehmens auftaucht, das Zugriff auf die Funktion „Nutzung der Server-Aufrufe“ hat. Dieser Warnhinweis löst eine Benachrichtigung an alle Administratoren des Anmeldeunternehmen aus, wenn eines der folgenden Kriterien erfüllt ist:

* „Beliebige“ Nutzung der Server-Aufrufe, die 100 % über oder gleich für jeden Server-Aufruftyp ist, zu dem Sie berechtigt sind, ODER
* „Beliebige“ Nutzung der Server-Aufrufe, die für jeden Server-Aufruftyp, zu dem Sie berechtigt sind, „größer oder gleich“ 90 % ist, ODER
* „Jede“ Nutzung von Server-Aufrufen, die „über oder gleich“ 75 % für jeden Server-Aufruftyp beträgt, zu dem Sie berechtigt sind, UND „Verwendeter Zeitraum“ „ist unter oder gleich“ 75 % des Verwendungszeitraums.

![](/help/admin/tools/server-call-usage/assets/alerts.png)

Sie können auf zwei Arten auf Warnhinweise zur Nutzung von Server-Aufrufen zugreifen:

* Klicken Sie auf **[!UICONTROL Warnhinweise verwalten]** in der oberen rechten Ecke der Registerkarte „Aktuelle Nutzung“ oder der Registerkarte „Nutzung der Report Suite“; oder
* Navigieren Sie in Adobe Analytics zu **[!UICONTROL Komponenten]** > **[!UICONTROL Warnhinweise]**.

## Erstellen von Warnhinweisen zur Nutzung von Server-Aufrufen {#create}

Um zusätzliche Warnhinweise zu erstellen:

1. Klicken Sie auf **[!UICONTROL + Hinzufügen]** und wählen Sie **[!UICONTROL Warnhinweise zur Nutzung von Server-Aufrufen]** aus.

   ![](/help/admin/tools/server-call-usage/assets/server_call_alert.png)

1. Definieren Sie den Warnhinweis.

   ![](/help/admin/tools/server-call-usage/assets/sc_alert.png)

   * **Titel** Geben Sie einen beschreibenden Namen ein. Sie können einen Warnhinweis nicht ohne Namen speichern.
   * **Zeitgranularität**: Bestimmt, wie oft der Warnhinweis überprüft wird. *Derzeit wird nur die wöchentliche Granularität unterstützt.* Das bedeutet, dass der Warnhinweis wöchentlich überprüft wird und auf die Daten aus dem aktuellen Nutzungszeitraum zurückblickt.
   * **Empfänger**: Bestimmen Sie beliebige Personen aus der Organisation, die eine E-Mail erhalten sollen, wenn der Warnhinweis den festgelegten Schwellenwert überschreitet.
   * **Ablaufdatum**: Standardmäßig liegt das Ablaufdatum ein Jahr nach dem Erstellungsdatum des Warnhinweises.
   * **Warnhinweis senden, wenn**:

      * Trigger einer dieser Metriken
Fügen Sie den Typ der Server-Aufrufe als Metrik hinzu und geben Sie den Warnschwellenwert an, indem Sie den Modifikator und den Schwellenwert auswählen:
         * ist größer oder gleich
         * ist kleiner oder gleich
      * Mit
Geben Sie den Schwellenwert und die Bedingung (ist über oder gleich oder ist unter oder gleich) für den Verwendungszeitraum an.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Verwalten von Warnhinweisen zur Nutzung von Server-Aufrufen {#manage}

![](/help/admin/tools/server-call-usage/assets/alert_mgmt.png)

So verwalten Sie Warnhinweise:

1. Wählen Sie das Kästchen neben einem oder mehreren Warnhinweisen aus. Die Warnungsverwaltungsaktionen werden oben angezeigt.
1. Führen Sie eine oder mehrere der folgenden Aktionen aus:

   | Aktion | Definition |
   |--- |--- |
   | + Hinzufügen | Die [Warnhinweiserstellung](/help/admin/tools/server-call-usage/scu-alerts.md) per Klick auf [!UICONTROL + Hinzufügen] öffnen. |
   | Tag | Markieren Sie Warnhinweise, um sie benutzerfreundlicher zu organisieren. |
   | Löschen | Sie können alle Warnhinweise mit Ausnahme der Standardwarnhinweise löschen. |
   | Umbenennen | Sie können alle Warnhinweise außer den Standardwarnhinweisen umbenennen. |
   | Genehmigen | Genehmigen von Warnhinweisen, um sie „offiziell“ zu machen. |
   | Aktivieren/Deaktivieren | Sie können alle Warnhinweise aktivieren oder deaktivieren, auch die Standardwarnhinweise. |
   | Verlängern | Wenn ein oder mehrere Warnhinweise ausgewählt sind, können sie verlängert werden. Dadurch wird das Ablaufdatum unabhängig vom ursprünglichen Ablaufdatum auf 1 Jahr ab dem Tag [!UICONTROL Verlängern] verlängert. |
   | In CSV exportieren | Siehe [Nutzungsbericht herunterladen](/help/admin/tools/server-call-usage/report-suite-usage.md) |

   {style="table-layout:auto"}
