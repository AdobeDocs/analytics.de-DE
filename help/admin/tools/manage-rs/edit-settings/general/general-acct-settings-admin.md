---
description: Beschreibung der Felder für allgemeine Kontoeinstellungen der Report Suite in Admin.
title: Allgemeine Kontoeinstellungen
feature: Admin Tools
uuid: c1ab5c34-2c41-4d12-a706-0e760dff8a95
exl-id: f49babb2-8e26-4cc6-b264-b4d7be93f130
TQID: https://experienceleague.adobe.com/1HGpY4lstZB6baXYggrD4xni1SWbYTDLa2fqYw11yd4
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 727
ht-degree: 56%

---

# Allgemeine Kontoeinstellungen

Feldbeschreibungen für die Report Suite „Allgemeine Kontoeinstellungen“ unter „Admin“.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Allgemeine Kontoeinstellungen]**

Diese Einstellungen umfassen Bearbeitungsoptionen für grundlegende Report-Suite-Funktionen wie Name und Zeitzone.


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Konfigurieren allgemeiner Kontoeinstellungen](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/administration/manage-report-suites/configuring-general-account-settings){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]

| Option | Beschreibung |
|--- |--- |
| Website-Titel | Identifiziert Ihre Site. Geben Sie jeder Report Suite einen eindeutigen Site-Titel. |
| Basis-URL | Gibt die Hauptwebsite der Report Suite an. Die Basis-URL hat keinen Einfluss auf die Referrer-Filterung. Verwenden Sie [interne URL-Filter](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md). |
| Zeitzone | Dies wirkt sich auf das Datum und die Uhrzeit aus, die mit Ihren Berichtdaten verbunden werden.  Durch das Ändern der Zeitzone bei einer Live-Report Suite ergibt sich entweder eine Spitze oder Lücke in den Berichtdaten. Um die Auswirkungen so gering wie möglich zu halten und keine Daten zu verfälschen, empfiehlt Adobe, die Zeitzonen außerhalb der besonders datenintensiven Zeiten zu ändern.  Wenn Sie beispielsweise die Zeitzone der Report Suite von Central in Pacific mit 3:00pm ändern, wird die aktuelle Zeit der Report Suite zu 1:00pm. Da beim Reporting bereits Daten für die :00 Stunde erfasst wurden, zeigen Berichte eine Traffic-Spitze zwischen 1 :00pm 3 :00pm.  Wenn Sie alternativ die Zeitzone der Report Suite von Central in Eastern um 3:00pm ändern, wird die aktuelle Zeit der Report Suite 4:00pm. Berichte zeigen am Tag :00pm Zeitumstellung keine Daten zwischen :00pm und 4 an. |
| Standardseite | Wenn der Bericht [!UICONTROL Bevorzugte Seiten] URL-Adressen statt Seitennamen enthält, verhindert diese Einstellung, dass für eine Webseite mehrere URL-Adressen angegeben werden. Beispielsweise sind die URLs `https://example.com` und `https://example.com/index.html` normalerweise dieselben Seiten. Sie können Standarddateinamen entfernen, damit beide URLs als `https://example.com` angezeigt werden.  Wenn Sie das Feld leer lassen, werden folgende Dateinamen aus den URLs entfernt: index.htm, index.html, index.cgi, index.asp, default.htm, default.html, default.cgi, default.asp, home.htm, home.html, home.cgi und home.asp.  Um das Entfernen von Dateinamen ganz zu deaktivieren, geben Sie einen Wert ein, der in Ihren URLs nicht vorkommt. |
| Letztes Oktett der IP-Adresse durch 0 ersetzen | Wenn diese Option aktiviert ist, wird das letzte Oktett von IP-Adressen durch eine Null ersetzt. Dies geschieht, bevor geobezogene Berichte ausgefüllt werden, und kann daher die Genauigkeit dieser Berichte beeinträchtigen. |
| IP-Verschleierung | Verwandelt IP-Adressen in nicht erkennbare Zeichenketten, was sie letztendlich aus den Adobe Datenspeichern löscht. Wenn die IP-Verschleierung aktiviert ist, gehen die ursprünglichen IP-Adressen dauerhaft verloren. <br> **Hinweis**: Die IP-Adressen werden überall in Analytics verschleiert, auch im Data Warehouse. Die IP-Einstellung in Target wird jedoch separat gesteuert, sodass diese Einstellung keine Auswirkungen auf Target hat.<br> Wenn die IP-Verschleierung aktiviert ist, erfolgt die gesamte erforderliche Verarbeitung, also auch die IP-Filterung bzw. der IP-Ausschluss, die Überprüfung von Bot-Regeln und Geosegmentierungssuchen, bevor die IP-Adresse verschleiert wird. Wenn Sie die IP-Verschleierung aktivieren, müssen Sie keine Änderungen vornehmen.<ul><li>Wenn **Deaktiviert** ausgewählt wird, bleibt die IP-Adresse in den Daten.</li><li>Wird **IP-Adresse verschleiern** markiert, wird die IP in zwei Doppelpunkte geändert, gefolgt von einem Hash-Wert (z. B. `::1932023538`).</li><li>Wenn Sie **IP-Adresse entfernen** aktivieren, wird die IP-Adresse nach der Geo-Suche durch `::X.X.X.X` in den Daten ersetzt<br/>Diese Option ist bei neuen Report Suites standardmäßig ausgewählt.</li></ul>**Hinweis**: Diese Einstellung erfordert möglicherweise Änderungen an benutzerdefinierten [Bot-Regeln](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md) oder [IP-Ausschlüssen](/help/admin/tools/exclude-ip.md).<br> **Hinweis**: Bei mit der Web-SDK erfassten Daten kann die IP-Verschleierung auf die Edge Network über die [Datenstromkonfiguration“ angewendet &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#@advanced-options). Wenn die IP-Verschleierung auf die Edge Network angewendet wird, wird sie bereits verschleiert, wenn sie Analytics erreicht. Diese Verschleierung wirkt sich sowohl auf Regeln als auch auf Geo-Suchen aus. |
| Transaktions-ID-Speicher | Ermöglicht die Verwendung von [Transaktions-ID](/help/import/data-sources/transactionid.md)-Datenquellen. |
| Data Warehouse aktivieren | Aktiviert die Data Warehouse-Benutzeroberfläche unter „Analytics“ > „Tools“ > „Data Warehouse“. |
| Postleitzahl-Option | Hier können Sie die Postleitzahl angeben, anstatt die von unserer Geo-IP-Suche erzeugten Elemente zu verwenden. |
| Unterstützung von Multi-Byte-Zeichen | Bei der Multi-Byte-Zeichenunterstützung werden Zeichen der Report Suite als UTF-8 gespeichert. Beim Empfang der Daten konvertiert das System die Daten aus dem Zeichensatz der Web-Seite in den UTF-8-Zeichensatz, damit Sie in Ihren Marketing-Berichten eine beliebige Sprache verwenden können. Wenden Sie sich an Ihr Adobe-Accountteam oder die Kundenunterstützung, wenn die Multi-Byte-Zeichenunterstützung für eine vorhandene Report Suite geändert werden soll. |
| Aktiviert | Gibt an, ob diese Report Suite aktiviert ist oder nicht. |
| Basiswährung | Hier können Sie die [Basiswährung](/help/implement/vars/config-vars/currencycode.md) für diese Report Suite angeben. |
| Organisations-ID | Die ID, die Ihrem bereitgestellten Experience Cloud-Unternehmen zugeordnet ist. Diese ID besteht aus einer 24-stelligen alphanumerischen Zeichenfolge gefolgt von @AdobeOrg (erforderlich). |
