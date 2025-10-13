---
description: Erfahren Sie, wie Sie Data Warehouse-Anfragen anzeigen, duplizieren und neu priorisieren können.
title: Verwalten von Data Warehouse-Anforderungen
feature: Data Warehouse
uuid: cdeb764f-56f9-43ec-9228-8ed5a2b58909
exl-id: a399d366-8402-4f4f-9b9f-14b218cd074a
source-git-commit: d929e97a9d9623a8255f16729177d812d59cec05
workflow-type: tm+mt
source-wordcount: '1148'
ht-degree: 4%

---

# Verwalten von Data Warehouse-Anforderungen

Sie können von Ihnen gestellte Data Warehouse-Anfragen anzeigen und verwalten. Nur Admins können Anfragen anderer Benutzender in ihrer Organisation anzeigen und verwalten.

In den folgenden Abschnitten werden die Aktivitäten beschrieben, die Sie beim Verwalten von Anfragen ausführen können.

## Anfragen anzeigen

Standardmäßig können Sie nur die von Ihnen erstellten Anfragen anzeigen, es sei denn, die Benutzer haben ausgewählt, ihre Anfragen für andere Personen in der Organisation sichtbar zu machen (wie in den allgemeinen Einstellungen für Data Warehouse-Anfragen in [](/help/export/data-warehouse/create-request/dw-general-settings.md) beschrieben). Systemadministratoren können alle Anforderungen anzeigen.

So zeigen Sie Data Warehouse-Anfragen an:

1. Wählen Sie in Adobe Analytics [!UICONTROL **Tools**] > [!UICONTROL **Data Warehouse**].

   Auf der Seite Data Warehouse werden alle von Ihnen gestellten Anfragen angezeigt. Daten werden in jeder Spalte angezeigt. Sie können [konfigurieren, welche Spalten](#configure-columns) sichtbar sind.

   <!-- add screenshot of main page -->

<!-- describe columns? -->

1. (Optional) Klicken Sie auf den Anfragenamen, um ein Dialogfeld mit den folgenden Informationen anzuzeigen: <!-- Check this -->

   * Wann die Verarbeitung einer Anfrage begonnen hat

   * Rate eingeschränkt: In Ihrem Unternehmen werden zu viele Data Warehouse-Anfragen ausgeführt. Die Anfrage wird angehalten, bis andere Datenanfragen abgeschlossen sind.

## Anforderungen bearbeiten

Beachten Sie beim Bearbeiten von Anfragen Folgendes:

* Nur Anfragen, die für die Ausführung nach einem Zeitplan konfiguriert sind, können bearbeitet werden.

* Nicht alle mit der Anfrage verknüpften Felder können bearbeitet werden. Felder, die nicht bearbeitet werden können, sind abgeblendet.

* Administratoren, die die Anfrage eines anderen Benutzers bearbeiten, müssen ein neues Konto und einen neuen Speicherort auswählen, auf die sie zugreifen können.

So bearbeiten Sie eine geplante Anfrage:

1. Wählen Sie in Adobe Analytics [!UICONTROL **Tools**] > [!UICONTROL **Data Warehouse**].

1. Wählen Sie auf der Data Warehouse-Seite die Anfrage aus, die Sie bearbeiten möchten.

   ![Verwalten einer Anfrage](assets/dw-manage-request.png)

1. Wählen Sie [!UICONTROL **Bearbeiten**] aus.

1. Bearbeiten Sie die Anfrage nach Bedarf. Abgeblendete Konfigurationsoptionen können nicht bearbeitet werden.

   Informationen zu den einzelnen Konfigurationsoptionen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. Wählen [!UICONTROL **Änderungen speichern**].

## Anzeigen des Verlaufs einer Anfrage

Sie können den Verlauf aller von Ihnen durchgeführten Data Warehouse-Anfragen anzeigen.

1. Wählen Sie in Adobe Analytics [!UICONTROL **Tools**] > [!UICONTROL **Data Warehouse**].

1. Wählen Sie auf der Seite Data Warehouse die Anfrage aus, deren Verlauf Sie anzeigen möchten.

   ![Verwalten einer Anfrage](assets/dw-manage-request.png)

1. Wählen Sie [!UICONTROL **Verlauf anzeigen**] aus.

   Die [!UICONTROL **Data Warehouse-Anfrage anzeigen**] zeigt eine Liste einzelner Berichtssendungen an, die mit der Anfrage verknüpft sind.

   Wählen Sie das Symbol **Spalte konfigurieren** ![Symbol „Spalte konfigurieren“ aus](assets/configure-column-icon.png) um Spalten auszublenden oder anzuzeigen, die nicht standardmäßig angezeigt werden.

   ![Seite mit Anfrageverlauf](assets/dw-request-history.png)

   Die folgenden Spalten sind verfügbar:

   | Spalte | Beschreibung |
   |---------|----------|
   | [!UICONTROL **Erstellt am**] | Datum und Uhrzeit der Erstellung des Berichts.<p>Dies wird in der Zeitzone des Benutzers angezeigt, der die Anfrage initiiert hat.</p> |
   | [!UICONTROL **Startdatum**] | Das Datum und die Uhrzeit des Berichtsstarts.<p>Dies wird in der Zeitzone des Benutzers angezeigt, der die Anfrage initiiert hat.</p> |
   | [!UICONTROL **Abschlussdatum**] | Datum und Uhrzeit der Fertigstellung des Berichts.<p>Dies wird in der Zeitzone des Benutzers angezeigt, der die Anfrage initiiert hat.</p> |
   | [!UICONTROL **Aktualisierungsdatum**] | Datum und Uhrzeit der letzten Aktualisierung des Berichts.<p>Dies wird in der Zeitzone des Benutzers angezeigt, der die Anfrage initiiert hat.</p> |
   | [!UICONTROL **Status**] | Der Status des Berichtversands. Mögliche Status sind:<ul><li>[!UICONTROL **Erstellt**]: Der Bericht wurde erstellt, aber noch nicht verarbeitet.</li><li>[!UICONTROL **Ausstehend**]: Der Bericht wartet auf die Verarbeitung.</li><li>[!UICONTROL **Verarbeitung**]: Der Bericht wird derzeit verarbeitet.</li><li>[!UICONTROL **Abgeschlossen**] Der Bericht wurde abgeschlossen und ist jetzt verfügbar.</li><li>[!UICONTROL **Geplant**]: Der Bericht ist geplant, hat jedoch noch nicht begonnen.</li><li>[!UICONTROL **Abgebrochen**]: Der Bericht wurde vom Benutzer abgebrochen.</li><li>[!UICONTROL **Fehler - Verarbeitung**:] Beim Bericht ist ein Fehler aufgetreten und er konnte nicht verarbeitet werden.</li><li>[!UICONTROL **Fehler - Fehler beim Senden**]: Der Bericht wurde erfolgreich generiert, konnte jedoch nicht bereitgestellt werden. Überprüfen Sie die [Konfiguration Ihres Ziels](/help/export/data-warehouse/create-request/dw-request-report-destinations.md) und senden Sie dann den Bericht erneut.</li></ul>. |
   | [!UICONTROL **Von**] | Das Startdatum des im Bericht enthaltenen Gesamtzeitrahmens.<p>Dies wird in der Zeitzone der Report Suite angezeigt.</p> |
   | [!UICONTROL **Bis**] | Das Enddatum des im Bericht enthaltenen Gesamtzeitrahmens. <p>Dies wird in der Zeitzone der Report Suite angezeigt.</p> |
   | [!UICONTROL **Legacy-Anfrage-ID**] | Die ID, die zur Identifizierung eines Berichts in der veralteten Benutzeroberfläche von Data Warehouse verwendet wird. Diese ID kann erforderlich sein, wenn Sie sich an die Kundenunterstützung von Adobe wenden. |
   | [!UICONTROL **Berichts-ID**] | Die ID, die zur Identifizierung eines Berichts in der aktuellen Data Warehouse-Benutzeroberfläche verwendet wird. Diese ID kann erforderlich sein, wenn Sie sich an die Kundenunterstützung von Adobe wenden. |


1. Wählen Sie einen Berichtsversand aus und wählen Sie dann eine der folgenden Optionen:

   | Option | Funktion |
   |---------|----------|
   | [!UICONTROL **Zieldetails**] | Zeigt die mit der Anfrage verbundenen Konto- und Standortdetails an. Dies ist das Konto und der Speicherort, die zuvor konfiguriert wurden, wie unter [Konfigurieren eines Berichtsziels für eine Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/dw-request-report-destinations.md) beschrieben. |
   | [!UICONTROL **Bericht abbrechen**] | Bricht den Bericht ab. Sie können keine Berichte abbrechen, die den Status [!UICONTROL **Abgeschlossen**] oder [!UICONTROL **Abgebrochen**] haben. |
   | [!UICONTROL **Bericht erneut ausführen**] | Führt den Bericht mit den Daten erneut so aus, wie er ursprünglich gesendet wurde. Sie können einen Bericht mit einem der folgenden Status erneut ausführen: [!UICONTROL **Abgebrochen**], [!UICONTROL **Abgeschlossen**], [!UICONTROL **Fehler - Verarbeitung**] oder [!UICONTROL **Fehler - Fehler - Fehler beim Senden**]. |
   | [!UICONTROL **Bericht erneut senden**] | Sendet die zuvor erstellte Berichtsdatei erneut. Sie können einen Bericht mit einem der folgenden Status erneut senden: [!UICONTROL **Abgeschlossen**] oder [!UICONTROL **Fehler - Fehler - Fehler beim Senden**]. |

## Kopieren von Anforderungen

Wenn Sie eine Anfrage kopieren, werden alle Konfigurationsoptionen aus der ursprünglichen Anfrage kopiert.

1. Wählen Sie in Adobe Analytics [!UICONTROL **Tools**] > [!UICONTROL **Data Warehouse**].

1. Wählen Sie auf der Seite Data Warehouse die Anfrage aus, die Sie kopieren möchten.

   ![Verwalten einer Anfrage](assets/dw-manage-request.png)

1. Wählen Sie [!UICONTROL **Kopieren**] aus.

   Die Seite Data Warehouse-Anfrage kopieren wird angezeigt. Alle Konfigurationsoptionen werden aus der ursprünglichen Anfrage kopiert.

1. Aktualisieren Sie alle Konfigurationsoptionen, die mit der Anfrage verknüpft sind.

   Informationen zu den einzelnen Konfigurationsoptionen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. Wählen [!UICONTROL **Änderungen speichern**].

## Anfragen abbrechen

Nur Anfragen, die für die Ausführung nach einem Zeitplan konfiguriert sind, können abgebrochen werden.

So brechen Sie eine geplante Anfrage ab:

1. Wählen Sie in Adobe Analytics [!UICONTROL **Tools**] > [!UICONTROL **Data Warehouse**].

1. Wählen Sie auf der Data Warehouse-Seite die Anfrage aus, die Sie bearbeiten möchten.

   ![Verwalten einer Anfrage](assets/dw-manage-request.png)

1. Wählen Sie [!UICONTROL **Abbrechen**] aus.

   Die Anfrage wird nicht mehr zur geplanten Zeit ausgeführt.

## Konfigurieren von Spalten

Sie können konfigurieren, welche Informationen für jede Anfrage angezeigt werden, indem Sie Spalten hinzufügen oder entfernen.

1. Wählen Sie **oben rechts auf** Seite Data Warehouse das Symbol „Spalten konfigurieren“ aus.

   ![Spalten konfigurieren](assets/dw-configure-columns.png)

   Die folgenden Spalten sind verfügbar:

   | Verfügbare Spalte | Beschreibung |
   |---------|----------|
   | Anfragename | Der Name der Person, die die Anfrage erstellt hat. |
   | Report Suite | Die mit der Anfrage verknüpfte Report Suite. |
   | Angefragt von | Der Benutzer, der die Anfrage erstellt hat. |
   | Datum der Anfrage | Das Datum, an dem die Anfrage erfolgte. |
   | Status | Die folgenden Status sind verfügbar:<ul><li><p>**Abgeschlossen**: Die Anfrage wurde erfolgreich ausgeführt.</p></li><li><p>**Abgebrochen**: Die Anfrage wurde vom Benutzer abgebrochen.</p></li><li><p>**Geplant**: Die Anfrage wurde für die Ausführung nach einem Zeitplan konfiguriert.</p></li><li><p>**Fehlgeschlagen**: Die Anfrage konnte nicht abgeschlossen werden. Wenn die Anfrage weiterhin fehlschlägt, wenden Sie sich an den Support.</p></li></ul> |

   {style="table-layout:auto"}

1. Stellen Sie sicher, dass alle Spalten, die angezeigt werden sollen, ausgewählt sind. Die ausgewählten Spalten werden auf der Data Warehouse-Seite angezeigt und enthalten die entsprechenden Informationen.

## Anfragen filtern und sortieren

1. Wählen Sie **Symbol** Filtern“ in der linken Leiste der Seite &quot;Data Warehouse&quot; aus.

   ![Anfragen filtern](assets/dw-filter.png)

1. Erweitern Sie die [!UICONTROL **Report Suites**], [!UICONTROL **Inhaber**] oder [!UICONTROL **Status**] und wählen Sie dann aus, wie Sie die Anfragen filtern möchten.

## Nach Anfragen suchen

1. Geben Sie im Suchfeld oben auf der Data Warehouse-Seite den Namen der Anfrage an, die Sie anzeigen möchten.

   Anfragen werden bei der Eingabe gefiltert.