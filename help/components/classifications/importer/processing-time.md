---
title: Verarbeitungszeit des Klassifizierungs-Import-Tools
description: Verstehen Sie den Zeitrahmen, in dem Adobe Classification-Dateien verarbeitet, und wie Sie die Verarbeitungszeit minimieren.
feature: Classifications
exl-id: 6b8b87f1-5dbc-46b8-9912-0e3086ff4b2a
TQID: 'https://experienceleague.adobe.com/D53-pBQ6RKbTCjEIyAgXmh1ZGx9FEtj5sLF8nHUp7P0'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: 00071d55-23eb-5795-a8d9-9d9b784f2791
    internal-label: Classifications
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: 9a50beeb0aa51cf9f4baf212566947c14029ce8e
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 100%
---
# Verarbeitungszeit des Klassifizierungs-Import-Tools

{{classification-importer-deprecation}}

Die Verarbeitungszeit für eine Klassifizierungsdatei hängt von der Größe der Datei und der Gesamtzahl der von Adobe verarbeiteten Dateien ab. Klassifizierungen dauern in der Regel nicht länger als 24 Stunden. In Unternehmen, die Adobe Analytics einsetzen, kann es jedoch vorkommen, dass Dateien in Zeiten starker Nutzung von Klassifizierungen länger als 24 Stunden benötigen. Adobe verzeichnet in den Monaten vor der Feiertagssaison eine starke Nutzung von Klassifizierungen.

Wenn Sie sehen möchten, ob eine Klassifizierungsdatei abgeschlossen ist, gehen Sie wie folgt vor:

1. Melden Sie sich bei Adobe Analytics an und navigieren Sie dann zu **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
2. Wählen Sie die betreffende Report Suite und den betreffenden Datensatz aus.
3. Wenn die Verarbeitung noch nicht abgeschlossen ist, wird eine der folgenden Meldungen angezeigt:

   * ![Hinweis](assets/icon_notice_notice.gif) Der ausgewählte Bericht enthält einen Classification-Import, der verarbeitet wird.
   * ![Hinweis](assets/icon_notice_notice.gif) Der ausgewählte Bericht enthält Classification-Daten, die noch nicht alle Server erreicht haben.

Wenn Sie die Importzeit für Klassifizierungen minimieren möchten, empfiehlt Adobe dringend die Einhaltung der folgenden Richtlinien:

* **Verwenden Sie nach Möglichkeit den Classification Rule Builder**: Der Classification Rule Builder verarbeitet Daten anders als der herkömmliche Klassifizierungs-Importer. Wenn die Klassifizierungsdaten bestimmten Mustern folgen, wird die Verwendung dieser Funktion dringend empfohlen.
* **Nur geänderte Zeilen hochladen**: Durch diese Vorgehensweise wird die Zeit für die Verarbeitung von Classification-Dateien erheblich reduziert, da unveränderte Zeilen nicht sortiert werden. Adobe empfiehlt dringend, nur geänderte Zeilen hochzuladen.
* **Vorausplanen**: Beginnen Sie so bald wie möglich mit dem Hochladen von Classification-Daten, insbesondere wenn diese Daten während der Weihnachtssaison verwendet werden.
* **Classification-Dateien nach Möglichkeit kombinieren**: Wenn eine Variable mehrere Classifications hat, laden Sie eine einzige Datei mit allen zutreffenden Classification hoch. Vermeiden Sie das Hochladen mehrerer Klassifizierungen für dieselbe Variable.
* **Hochladen von Dateien über 500 MB vermeiden**: Bei großen Mengen an Classification-Daten empfiehlt Adobe, Dateien in Dateien mit 100 MB bis 500 MB aufzuteilen.
* **Hochladen großer Dateimengen auf FTP vermeiden**: Wenn Sie vorhaben, dieselben Dateien über FTP in viele Report Suites hochzuladen, begrenzen Sie die Anzahl der gleichzeitig hochgeladenen Dateien. Adobe empfiehlt, dass die Anzahl der Dateien multipliziert mit der Anzahl der Report Suites weniger als 1000 beträgt. Wenn das Hochladen von 100 Dateien in 100 Report Suites erforderlich ist, beträgt die Gesamtanzahl der Dateien 10.000. Anstatt alle 100 Dateien gleichzeitig hochzuladen, teilen Sie sie in 10 Gruppen zu je 10 Dateien auf.
* **Kleine Dateien über den Browser-Importer hochladen**: Wenn Sie eine Datei mit einer Größe von weniger als 1 MB (weniger als 50.000 Zeilen) haben, empfiehlt Adobe die Verwendung des Browser-Importers. Browser-Importe sind fast immer schneller als FTP-Importe.
