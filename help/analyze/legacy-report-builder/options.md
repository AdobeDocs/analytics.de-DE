---
description: Informationen zu den Report Builder-Optionen.
title: Über Report Builder-Optionen
uuid: f2920dee-4245-4617-a02e-03726dde2bb5
feature: Report Builder
role: User, Admin
exl-id: d3388990-7919-461d-a96e-4c996b8bdb8b
TQID: https://experienceleague.adobe.com/56Wyy-f9kDXxFSanTNILr4rNQ0OB3YtbIFPcRT082sc
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 474
ht-degree: 45%

---

# Report Builder-Optionen

{{legacy-arb}}

Im Bereich „Optionen“ können Sie Einstellungen für Datum und Latenzzeit (aktuelle Daten) sowie die Anmeldeinformationen festlegen und Updates konfigurieren.

1. Klicken Sie in der Symbolleiste „Add-Ins“ auf **[!UICONTROL Optionen]** ![](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Settings_18_N.svg):

| Element | Beschreibung |
|--- |--- |
| [!UICONTROL Ausführungsdatum] |  |
| Auf aktuelles Datum festlegen | Ermöglicht das Angeben oder Zurücksetzen des [!UICONTROL Ab-Datum], sodass Report Builder das aktuelle Datum verwendet oder Sie bei der Aktualisierung fragt, welches Datum verwendet werden soll. |
| Beim Aktualisieren zum Festlegen auffordern | Sie können das [!UICONTROL Ausführungsdatum] beim Aktualisieren einer Anforderung definieren. |
| [!UICONTROL Datenaktualität] |  |
| [!UICONTROL Aktuelle Daten einschließen] | Ermöglicht die Anzeige der Datenlatenz (auch [!UICONTROL Datenaktualität] genannt) bis zu einer Minute im Reporting, gelegentlich sogar noch bevor diese Daten von Adobe Analytics verarbeitet wurden.<br>Wenn Sie diese Option nicht verwenden, wird der finalisierte Modus (verarbeitet) verwendet, der in der Regel latenter ist.<br>Diese Einstellungen gelten für alle Anforderungen in dieser Arbeitsmappe, die kompatible aktuelle Daten enthalten. Ist eine Anforderung nicht kompatibel, wird der finalisierte Modus verwendet.<br>Beachten Sie die folgenden Situationen für die Verwendung von [!UICONTROL Aktuelle Daten einschließen] mode:<br>**Formatoptionen**: Sie können angeben, ob diese Informationen ([!UICONTROL Datenaktualität]) angezeigt werden sollen, wenn [Anzeigekopfzeilen formatieren](/help/analyze/legacy-report-builder/layout/t-format-display-headers.md).<br>**Aufschlüsselungen**: Nicht unterstützt. Wenn der Modus [!UICONTROL Datenaktualität] auf „aktuelle Daten“ eingestellt ist und eine der Anforderungen ein Aufgliederungselement enthält, wird der Modus für diese Anforderung wieder auf „nicht aktuell“ zurückgesetzt. Andere Anfragen verwenden jedoch weiterhin den Modus „Aktuelle Daten“.<br>**Anforderungs-Manager**: Sie können die Spalte „Aktuelle Daten“ im Anforderungs-Manager anzeigen lassen, um zu sehen, welche Einstellung für eine geplante Anforderung gilt.<br>**Geplante Arbeitsmappen**: Dieser Modus wird während des Planungsprozesses auf Arbeitsmappen-Ebene gespeichert. Wenn Sie eine Arbeitsmappe mit terminierten Daten öffnen und [!UICONTROL Aktuelle Daten einschließen] anwenden, wird danach der aktuelle Modus verwendet.<br>**Berechtigungen**: Für Benutzende, die keinen Zugriff auf aktuelle Daten haben, wird diese Option ausgeblendet.  Wenn diese Option aktiviert ist und eine oder mehrere Anfragen nicht angewendet werden können, wird eine Warnung ausgegeben. |
| Warnungen für mit aktuellen Daten inkompatible Anfragen deaktivieren | Mit dieser Option werden Warnungen angezeigt, wenn der Modus [!UICONTROL Aktuelle Daten einschließen] ausgewählt wird, der Datenmodus aber nicht auf die bearbeitete Anforderung übertragen werden kann.  Wenn Sie zum Beispiel [!UICONTROL Aktuelle Daten einschließen] auswählen und dann eine Anforderung bearbeiten, bei der ein Segment ausgewählt wird, so wird eine Warnung angezeigt. |
| Report Builder-Anfragen in lokaler Datei protokollieren (zur Fehlerbehebung) | Ermöglicht die Protokollierung von Anforderungen in einer lokalen Datei. Verwenden Sie diese Protokolldatei zur Fehlerbehebung. |
| Eingegebenen Wert interpretieren… | Interpretiert einen eingegebenen Wert in einem Filtersteuerelement als Zellenposition, bevor er als Filterausdruck betrachtet wird.<br>Wenn Sie z. B. eine Anforderung für die Top 10 Seiten mit Schuhen über einen Filter erstellen, wird eine Zelle angezeigt, die in etwa Folgendes enthält: Filter: Top 1–10 Seiten, Seite enthält Schuhe. |
| Aktualisieren, wenn eine neue Version verfügbar ist | Informiert das System, Sie zu benachrichtigen, wenn eine neue Version für die Installation verfügbar ist. |
