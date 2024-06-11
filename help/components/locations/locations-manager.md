---
description: Konfigurieren Sie das Cloud-Importkonto und den Speicherort, an den Classification-Daten hochgeladen werden können.
keywords: Analysis Workspace
title: Standorte-Manager
feature: Classifications
exl-id: ace70568-220a-44e8-8e5f-f73002b9e2a2
source-git-commit: 82c6d1e6d748a9b52b5988af5abb78d2c27ca077
workflow-type: tm+mt
source-wordcount: '1473'
ht-degree: 1%

---

# Standorte-Manager

Mit dem Locations Manager können Sie Konten und Standorte anzeigen, erstellen, bearbeiten oder löschen. Diese können für einen der folgenden Zwecke verwendet werden:

* Exportieren von Dateien mithilfe von [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md)
* Exportieren von Berichten mithilfe von [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)
* Importieren von Schemata mit [Klassifizierungssätze](/help/components/classifications/sets/overview.md)

## Anzeigen, Filtern und Suchen von Standorten

Mit dem Standort-Manager können Sie alle von Ihnen erstellten Orte oder freigegebene Orte anzeigen. Systemadministratoren können von allen Benutzern erstellte Standorte anzeigen, unabhängig davon, ob sie freigegeben sind.

1. Um auf den Locations Manager in Adobe Analytics zuzugreifen, wählen Sie **[!UICONTROL Komponenten]** > **[!UICONTROL Standorte]**.

1. (Bedingt) Wenn Sie Systemadministrator sind, können Sie die [!UICONTROL **Anzeigen von Standorten für alle Benutzer**] -Option zum Anzeigen von Orten, die von allen Benutzern in Ihrer Organisation erstellt wurden. <!-- Maybe add a screenshot? This is new functionality -->

1. Filtern oder durchsuchen Sie die Liste der Standorte:

   * **Filter:** Wählen Sie das Symbol Filter aus, um die Liste der Standorte zu filtern.

     Sie können Standorte nach **[!UICONTROL Location Type]**, **[!UICONTROL Konto]** oder **[!UICONTROL Erstellt von]**.

     ![Standortfilter](assets/locations-filters.png)

   * **Suchen:** Geben Sie im Suchfeld den Namen des Standorts ein, den Sie anzeigen möchten. Die Ergebnisse werden bei der Eingabe gefiltert. Die folgenden Spalten werden durchsucht: **Ortsname**, **Location Type**, **Konto**, und **Erstellt von**.

1. (Optional) Wenn Sie mehr als 1.000 Standorte haben, werden nur die ersten 1.000 angezeigt. Auswählen [!UICONTROL **Mehr laden**] , um 1.000 weitere Standorte zu laden.

## Spalten im Locations Manager konfigurieren

Die folgenden Spalten sind im Locations Manager verfügbar. Um die in der Tabelle angezeigten Spalten anzupassen, wählen Sie die **Tabelle anpassen** icon ![Symbol &quot;Tabelle anpassen&quot;](assets/customize-table-icon.png).

* **[!UICONTROL Ortsname]**: Der Standortname. Wählen Sie das 3-Punkt-Menü neben einem Ortsnamen aus, um [Speicherort bearbeiten](/help/components/locations/configure-import-locations.md) oder löschen Sie sie.
* **[!UICONTROL Standorttyp]**: Der Kontotyp, der mit dem Standort verknüpft ist.
* **[!UICONTROL Konto]**: Das spezifische Konto, das mit dem Standort verknüpft ist.
* **Anwendung**: Der Anwendungstyp, mit dem der Speicherort verwendet werden kann (z. B. Daten-Feeds, Data Warehouse oder Classification-Sets).
* **[!UICONTROL Zuletzt verwendet]**: Das Datum, an dem der Standort zuletzt verwendet wurde.
* **[!UICONTROL Erstellt von]**: Der Benutzer, der den Standort erstellt hat.
* **[!UICONTROL Erstellungsdatum]**: Das Datum, an dem der Speicherort erstellt wurde.

## Erstellen und Verwalten von Standorten

Sie können Speicherorte erstellen, bearbeiten und löschen.

### Erstellen eines Standorts

Informationen zum Erstellen eines Standorts finden Sie unter [Konfigurieren von Cloud-Import- und -Exportspeicherorten](/help/components/locations/configure-import-locations.md).

<!-- Do I need to add some steps here about how to create a location and then assign that location to be used with DF, DW, or Classifications sets? Need to hear back from Ron and team whether we are including this functionality -->

### Speicherort bearbeiten

Ein Speicherort kann nur von dem Benutzer, der ihn erstellt hat, oder von einem Systemadministrator bearbeitet werden.

Informationen zum Bearbeiten eines Standorts finden Sie unter [Konfigurieren von Cloud-Import- und -Exportspeicherorten](/help/components/locations/configure-import-locations.md).

### Löschen eines Speicherorts

>[!IMPORTANT]
>
>Wenn ein Speicherort gelöscht wird, schlagen alle Daten-Feed-Dateien, Data Warehouse-Berichte oder Classification-Set-Schemata, die mit dem gelöschten Speicherort verknüpft sind, bei der nächsten Verwendung fehl.
>
>Wenn Sie einen Ort löschen, sollten Sie [Bearbeiten Ihrer Daten-Feeds](/help/export/analytics-data-feed/create-feed.md), [Data Warehouse-Berichte](/help/export/data-warehouse/create-request/dw-request-report-destinations.md), und [Classification-Sets-Schemata](/help/components/classifications/sets/manage/schema.md) , um einen funktionierenden Standort zu verwenden.

Ein Speicherort kann nur von dem Benutzer, der ihn erstellt hat, oder von einem Systemadministrator gelöscht werden.

So löschen Sie einen Speicherort im Locations Manager in Adobe Analytics:

1. Auswählen **[!UICONTROL Komponenten]** > **[!UICONTROL Standorte]** und wählen Sie dann die [!UICONTROL **Standorte**] Registerkarte.

1. Wählen Sie das Menü mit 3 Punkten im [!UICONTROL **Ortsname**] -Spalte für den Ort, den Sie löschen möchten.

1. Wählen Sie [!UICONTROL **Löschen**] aus.

## Erstellen und Verwalten von Konten

Sie können Konten erstellen, bearbeiten und löschen.

### Konto erstellen

Informationen zum Erstellen eines Kontos finden Sie unter [Konfigurieren von Cloud-Import- und -Exportkonten](/help/components/locations/configure-import-accounts.md).

### Konto bearbeiten

Ein Konto kann nur von dem Benutzer, der es erstellt hat, oder von einem Systemadministrator bearbeitet werden.

Informationen zum Bearbeiten eines Kontos finden Sie unter [Konfigurieren von Cloud-Import- und -Exportkonten](/help/components/locations/configure-import-accounts.md).

### Kontoschlüssel anzeigen

Nachdem Sie ein Konto erstellt haben, können Sie alle zugehörigen Kontoschlüssel für dieses Konto anzeigen. Möglicherweise müssen Sie diese Informationen einsehen, wenn Sie die Konfiguration des Kontos mit Ihrem Cloud-Anbieter bei der [ursprünglich das Konto konfiguriert hat](/help/components/locations/configure-import-accounts.md).

So zeigen Sie Schlüssel an, die mit einem Exportkonto verknüpft sind:

1. Wählen Sie in Adobe Analytics **[!UICONTROL Komponenten]** > **[!UICONTROL Standorte]** und wählen Sie dann die [!UICONTROL **Standortkonten**] Registerkarte.

1. (Bedingt) Wenn Sie Systemadministrator sind, können Sie die [!UICONTROL **Anzeigen von Standorten für alle Benutzer**] -Option zum Anzeigen von Orten, die von allen Benutzern in Ihrer Organisation erstellt wurden. <!-- Maybe add a screenshot? This is new functionality -->

1. Wählen Sie das 3-Punkt-Symbol für das Konto aus, das Sie bearbeiten möchten, und wählen Sie dann [!UICONTROL **Kontoschlüssel**].

### Konto löschen

>[!IMPORTANT]
>
>Konten können nur gelöscht werden, wenn sie nicht von Orten verwendet werden. Bevor Sie ein Konto löschen, müssen Sie zunächst alle Speicherorte im Konto löschen, wie hier beschrieben: [Löschen eines Speicherorts](#delete-a-location).

Ein Konto kann nur von dem Benutzer, der es erstellt hat, oder von einem Systemadministrator gelöscht werden.

So löschen Sie ein Konto:

1. Wählen Sie in Adobe Analytics **[!UICONTROL Komponenten]** > **[!UICONTROL Standorte]** und wählen Sie dann die [!UICONTROL **Standortkonten**] Registerkarte.

1. (Bedingt) Wenn Sie Systemadministrator sind, können Sie die [!UICONTROL **Anzeigen von Konten für alle Benutzer**] -Option zum Anzeigen von Orten, die von allen Benutzern in Ihrer Organisation erstellt wurden.

1. Wählen Sie das 3-Punkt-Symbol für das Konto aus, das Sie bearbeiten möchten, und wählen Sie dann [!UICONTROL **Konto löschen**]

## unternehmensweite Einstellungen konfigurieren (nur Administratoren)

{{release-limited-testing-section}}

Systemadministratoren können Benutzer daran hindern, Konten und Standorte zu erstellen, oder sie können die Arten von Konten einschränken, die Benutzer erstellen und verwenden können.

### Konfigurieren, ob Benutzer Konten erstellen und bearbeiten können

Standardmäßig können alle Benutzer der Organisation Konten erstellen und Konten bearbeiten, die sie in Ihrer Adobe Analytics-Umgebung erstellen, wie hier beschrieben: [Konfigurieren von Cloud-Import- und -Exportkonten](/help/components/locations/configure-import-accounts.md).

Sie können Benutzer daran hindern, Konten zu erstellen. Wenn Sie dies tun, können Benutzer weiterhin alle Konten verwenden, die sie bereits erstellt haben, sie können sie jedoch nicht mehr bearbeiten. Sie können von Benutzern erstellte Konten löschen, wie unter [Konto löschen](#delete-an-account).

So beschränken Sie das Erstellen und Bearbeiten von Konten für alle Benutzer:

1. Wählen Sie in Adobe Analytics **[!UICONTROL Komponenten]** > **[!UICONTROL Standorte]** und wählen Sie dann die [!UICONTROL **Admin-Einstellungen**] Registerkarte.

1. Im [!UICONTROL **Standortkonten**] -Abschnitt die Auswahl der Option aufheben, [!UICONTROL **Benutzern erlauben, Standortkonten zu erstellen und zu verwalten**].

1. Wählen Sie [!UICONTROL **Speichern**] aus.

1. (Optional) Löschen Sie alle von Benutzern erstellten Konten, die Sie nicht mehr verwenden möchten, wie unter [Konto löschen](#delete-an-account).

### Konfigurieren, ob Benutzer Standorte erstellen und bearbeiten können

Standardmäßig können alle Benutzer der Organisation Standorte erstellen und Positionen bearbeiten, die sie in Ihrer Adobe Analytics-Umgebung erstellen, wie hier beschrieben: [Cloud-Import- und -Exportspeicherorte konfigurieren](/help/components/locations/configure-import-locations.md).

Sie können Benutzer daran hindern, Orte zu erstellen. Wenn Sie dies tun, können Benutzer weiterhin alle Orte verwenden, die sie bereits erstellt haben, sie können sie jedoch nicht mehr bearbeiten. Sie können von Benutzern erstellte Speicherorte löschen, wie unter [Speicherorte löschen](#delete-a-location).

So beschränken Sie die Erstellung und Bearbeitung von Standorten für alle Benutzer:

1. Wählen Sie in Adobe Analytics **[!UICONTROL Komponenten]** > **[!UICONTROL Standorte]** und wählen Sie dann die [!UICONTROL **Admin-Einstellungen**] Registerkarte.

1. Im [!UICONTROL **Standorte**] -Abschnitt die Auswahl der Option aufheben, [!UICONTROL **Benutzern erlauben, Standorte zu erstellen und zu verwalten**].

1. Wählen Sie [!UICONTROL **Speichern**] aus.

1. (Optional) Löschen Sie alle Orte, die Benutzer erstellt haben und die Sie nicht mehr verwenden möchten, wie unter [Löschen eines Speicherorts](#delete-a-location).

### Beschränken, welche Kontotypen Benutzer erstellen und verwenden können

Sie können die Kontotypen einschränken, die Benutzern in den folgenden Fällen angezeigt werden:

* Wann [Erstellen neuer Konten](/help/components/locations/configure-import-accounts.md).

* Bei der Auswahl der Konten, die beim Exportieren von Dateien mit [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md), um Berichte mithilfe von [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)oder Schemata importieren mithilfe von [Klassifizierungssätze](/help/components/classifications/sets/overview.md).

Wenn Sie die in diesem Abschnitt beschriebenen Kontotypen einschränken, sind Konten des Typs, den Sie einschränken, für Benutzer nicht mehr sichtbar. Dies bedeutet, dass keine neuen Konten dieses Typs erstellt werden können und vorhandene Konten dieses Typs nicht bei der Erstellung von Daten-Feeds, Data Warehouse oder Classification-Sets verwendet werden können.

Vorhandene Konten, die für geplante Exporte konfiguriert sind, müssen jedoch gelöscht werden, wenn Sie sie von der Verwendung beschränken möchten.

#### Stellen Sie sicher, dass Konten nicht für geplante Exporte verwendet werden

Wenn Sie die Kontotypen einschränken, werden vorhandene Konten ausgeblendet und nicht gelöscht.

Wenn Zeitpläne bereits so konfiguriert sind, dass Daten an ein Konto gesendet werden, das dem von Ihnen begrenzten Typ entspricht, werden die Zeitpläne auch nach der Begrenzung des Kontotyps weiter ausgeführt und die Daten werden weiterhin an das Konto gesendet.  Wenn beispielsweise ein Daten-Feed geplant ist, Daten an einen von Ihnen beschränkten Kontotyp zu senden, wird der Zeitplan weiterhin ausgeführt.

Wenn Sie sicherstellen müssen, dass Konten eines bestimmten Typs nicht in geplanten Exporten verwendet werden, können Sie die Konten vor dem [die Kontotypen begrenzen](#limit-the-account-types-that-are-available-to-users).

So löschen Sie Konten:

1. Suchen Sie die Konten des Kontotyps, den Sie begrenzen möchten, die für geplante Exporte verwendet werden.

1. Löschen Sie die Konten, wie unter [Konto löschen](#delete-an-account).

1. Fahren Sie mit dem folgenden Abschnitt fort: [Beschränken der für Benutzer verfügbaren Kontotypen](#limit-the-account-types-that-are-available-to-users).

#### Beschränken der für Benutzer verfügbaren Kontotypen

So beschränken Sie die Kontotypen, die Benutzern beim Erstellen und Verwenden von Konten zur Verfügung stehen:

1. Wählen Sie in Adobe Analytics **[!UICONTROL Komponenten]** > **[!UICONTROL Standorte]** und wählen Sie dann die [!UICONTROL **Admin-Einstellungen**] Registerkarte.

1. Suchen Sie die [!UICONTROL **Zulässige Kontotypen**] Abschnitt.

   Die folgenden Kontotypen sind standardmäßig für Benutzer verfügbar. Heben Sie die Auswahl dieser Kontotypen auf, die Sie die Verwendung von Benutzern beschränken möchten.

   * [!UICONTROL **Amazon S3 Role ARN**]

   * [!UICONTROL **Google Cloud Platform**]

   * [!UICONTROL **Azure SAS**]

   * [!UICONTROL **Azure RBAC**]

   * [!UICONTROL **E-Mail**]

   * Veraltete Kontotypen, einschließlich [!UICONTROL **Amazon S3**], [!UICONTROL **Azure**], [!UICONTROL **FTP**], und [!UICONTROL **SFTP**]

1. Wählen Sie [!UICONTROL **Speichern**] aus.


