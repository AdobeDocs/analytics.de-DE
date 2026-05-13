---
description: Sie können Klassifizierungsdaten mit dem Browser importieren (hochladen). Diese Methode beschränkt den Upload Ihrer Klassifizierungsdaten auf eine einzige Report Suite
title: Browser-Import
feature: Classifications
exl-id: 5bef1f6d-9b27-464d-8343-472f300a7437
TQID: https://experienceleague.adobe.com/iFVW-d9C12dj6TXnUlA3-zVF0oBAWpJwg1JK8LqzF-s
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 354
ht-degree: 29%

---

# Browser-Import (veraltet)

{{classification-importer-deprecation}}

Sie können Klassifizierungsdaten mit dem Browser importieren (hochladen). Diese Methode beschränkt den Upload Ihrer Klassifizierungsdaten auf eine einzige Report Suite

## Browser-Import {#concept_314FB3D5FD5A439B9CFEDE37A3337BA7}

Sie können Klassifizierungsdaten mit dem Browser importieren (hochladen). Diese Methode beschränkt den Upload Ihrer Klassifizierungsdaten auf eine einzige Report Suite

**[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**

## Browser-Import von Classifications – Feldbeschreibungen {#section_F628C47081DA4026A4D30E3D3454B1DA}

| Element | Beschreibung |
| --- | --- |
| Report Suite auswählen | Die Report Suite, in die Sie die Klassifizierungsdaten importieren möchten. Die Importdatendatei muss dem Format des Datensatzes in der Report Suite entsprechen. |
| Datensatz, der klassifiziert werden soll | Der Datensatz, der die Klassifizierungen erhalten soll. Die Dropdown-Liste enthält alle Berichte in Ihren Report Suites, die für Klassifizierungen konfiguriert sind. |
| Zu importierende Datei auswählen | Navigieren Sie hier zur Importdatendatei, die hochgeladen werden soll.  Hinweis: Für das Hochladen von Dateien gilt eine maximale Dateigröße von 1 MB. |
| Daten in Konflikten überschreiben | Vorhandene Daten, die mit den importierten Daten kollidieren, werden automatisch überschrieben.<br>**Wichtig**: Diese Option ist nicht für Report Suites verfügbar, die für die neue Klassifizierungsarchitektur aktiviert sind. |
| Klassifizierungsdatei nach Abschluss des Imports automatisch herunterladen | Lädt automatisch eine durch Tabulatoren getrennte Datei herunter, die den Datensatz mit den neu hochgeladenen Klassifizierungsdaten darstellt. Adobe generiert diese Datei automatisch für Sie, wenn beim Import eindeutige IDs erstellt werden oder Fehler auftreten.<br>**Wichtig**: Diese Option ist nicht für Report Suites verfügbar, die für die neue Klassifizierungsarchitektur aktiviert sind. |


## Importieren von Classifications über Browser {#task_D7D51CB6FB35437AB68599B1B23FEAC1}

1. Klicken Sie auf **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Klicken Sie auf **[!UICONTROL Datei importieren]**.
1. Konfigurieren Sie die Felder **[!UICONTROL Browser-Import]**.
1. Klicken Sie auf **[!UICONTROL Datei importieren]**.
1. Behalten Sie das Statusfenster für Benachrichtigungen zum Stand der Verarbeitung im Auge.
1. (Bedingt) Wenn Sie die Option **[!UICONTROL Klassifizierungsdatei nach dem Hochladen automatisch herunterladen]** ausgewählt haben, geben Sie an, wo die entsprechende Datei nach Abschluss der Bearbeitung gespeichert werden soll. Beachten Sie, dass diese Option nicht für Report Suites verfügbar ist, die für die neue Klassifizierungsarchitektur aktiviert sind.

>Bei einem erfolgreichen Import werden die entsprechenden Änderungen sofort in einem Export angezeigt. Datenänderungen in Berichten können jedoch bei Verwendung eines Browser-Imports bis zu vier Stunden und bei Verwendung eines FTP-Imports bis zu 24 Stunden dauern.
