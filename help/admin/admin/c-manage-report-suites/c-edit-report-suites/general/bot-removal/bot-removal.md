---
title: Entfernen von Bots in Adobe Analytics
description: Entfernen von Bots in Adobe Analytics
feature: Bot Removal
role: Admin
exl-id: 6d4b1925-4496-4017-85f8-82bda9e92ff3
source-git-commit: 50c2881aa61097c14057dd4fd4654c832f20b26f
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 78%

---

# Entfernen von Bots in Adobe Analytics

Adobe Analytics bietet mehrere Optionen zum Entfernen von Bot-Traffic aus Berichten:

## Verwenden von Bot-Regeln

Sowohl Standard- als auch benutzerdefinierte Bot-Filtermethoden werden in **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Bot-Regeln]** unterstützt:

| Regeltyp | Beschreibung |
|--- |--- |
| Standard-IAB-Bot-Regeln | Wenn Sie **[!UICONTROL IAB Bot-Filterungsregeln aktivieren]** auswählen, wird die Liste „International Spiders &amp; Bots List“ von [IAB](https://www.iab.com/) (International Advertising Bureau) verwendet, um Bot-Traffic zu entfernen. Die meisten Kunden wählen mindestens diese Option aus. |
| Benutzerdefinierte Bot-Regeln | Sie können benutzerdefinierte Bot-Regeln festlegen und hinzufügen, die auf Benutzeragenten, IP-Adressen oder IP-Bereichen basieren. |

Weitere Informationen finden Sie unter [Grundlegendes zu und Konfigurieren von Bot-Regeln](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md).

## Identifizieren von Bots mit dem Plug-in [!UICONTROL websiteBot]

Mit dem Plug-in [!UICONTROL websiteBot] können Sie dynamisch feststellen, ob es sich bei Desktop-Besuchern um Bots handelt. Mithilfe dieser Daten können Sie eine höhere Genauigkeit bei allen Arten von Berichten erzielen. Dadurch verfügen Sie über eine bessere Möglichkeit, legitimen Sitetraffic zu messen.

Dieses Plug-in führt zwei Prüfungen durch:

* Zunächst wird anhand der navigator.UserAgent-Variablen ermittelt, ob es sich bei dem Gerät um ein Desktop-Gerät oder ein Mobilgerät handelt. Smartphones und Tablets werden ignoriert.
* Wenn es sich um ein Desktop-Gerät handelt, wird ein Ereignis-Listener für Mausbewegungen hinzugefügt.

Weitere Informationen finden Sie im [Adobe Analytics-Implementierungshandbuch](https://experienceleague.adobe.com/docs/analytics/implementation/vars/plugins/websitebot.html?lang=de).

## Verwenden einer Kombination aus Adobe-Tools

Da Bots sich schnell wandeln, bietet Adobe außerdem mehrere leistungsstarke Funktionen, die, wenn sie richtig und regelmäßig kombiniert werden, dazu beitragen können, diese Feinde der Datenqualität zu beseitigen. Zu diesen Funktionen gehören: Experience Cloud ID-Service, Segmentierung, Data Warehouse, Kundenattribute und Virtual Report Suites. Im Folgenden finden Sie eine Übersicht darüber, wie Sie diese Tools nutzen können.

### Schritt 1: Experience Cloud ID Ihrer Besucher in eine neue deklarierte ID übertragen

Erstellen Sie zunächst eine neue deklarierte ID im [People Core Service](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=de). Übertragen Sie die Experience Cloud ID Ihres Besuchers in diese neue deklarierte ID. Mit [Tags in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/id-service/overview.html?lang=de) ist dies schnell und einfach möglich. Verwenden wir den Namen „ECID“ für die deklarierte ID.

![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/assets/bot-cust-attr-setup.png)

Hier erfahren Sie, wie Sie diese ID über das Datenelement erfassen können. Achten Sie darauf, Ihre Experience Cloud-Organisations-ID korrekt in das Datenelement einzutragen.

```return Visitor.getInstance("REPLACE_WITH_YOUR_ECORG_ID@AdobeOrg").getExperienceCloudVisitorID();```

Nachdem dieses Datenelement eingerichtet wurde, befolgen Sie [diese Anweisungen](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/id-service/overview.html?lang=de), um mithilfe von Tags in Adobe Experience Platform deklarierte IDs in das ECID-Tool zu übertragen.

### Schritt 2: Segmentierung verwenden, um Bots zu identifizieren

Nachdem die ECID Ihres Besuchers in eine deklarierte ID übertragen wurde, können Sie die [Segmentierung in Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/segments/t-freeform-project-segment.html?lang=de) verwenden, um Besucher zu identifizieren, die sich wie Bots verhalten. Bots werden oft durch ihr Verhalten definiert: Besuche mit Einzelzugriff, ungewöhnliche Benutzeragenten, unbekannte Geräte-/Browser-Informationen, keine verweisenden Stellen, neue Besucher, ungewöhnliche Landingpages usw. Verwenden Sie die Möglichkeiten von Drilldowns und Segmentierung in Workspace, um die Bots zu identifizieren, die der IAB-Filterung und den Bot-Regeln Ihrer Report Suite entgangen sind. Hier ist zum Beispiel ein Screenshot eines Segments, das Sie verwenden könnten:

![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/assets/bot-filter-seg1.png)

### Schritt 3: Alle [!DNL Experience Cloud IDs] aus dem Segment über Data Warehouse exportieren

Nachdem Sie die Bots anhand von Segmenten identifiziert haben, ist der nächste Schritt die Nutzung von Data Warehouse, um alle mit diesem Segment verbundenen Experience Cloud IDs zu extrahieren. Richten Sie Ihre [Data Warehouse](/help/export/data-warehouse/data-warehouse.md)-Anfrage wie in dem Screenshot gezeigt ein:

![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/assets/bot-dwh-3.png)

Denken Sie daran, die Experience Cloud-Besucher-ID als Dimension zu verwenden und das Bots-Segment anzuwenden.

### Schritt 4: Diese Liste als Kundenattribut an Adobe zurückgeben

Sobald der Data Warehouse-Bericht eintrifft, verfügen Sie über eine Liste der ECIDs, die aus historischen Daten gefiltert werden müssen. Kopieren Sie diese ECIDs und fügen Sie sie in eine leere .CSV-Datei mit nur zwei Spalten, „ECID“ und „Bot Flag“, ein.

* **ECID**: Stellen Sie sicher, dass diese Spaltenüberschrift mit dem Namen übereinstimmt, den Sie für die neue deklarierte ID oben angegeben haben.
* **Bot Flag**: Fügen Sie „Bot Flag“ als Schema-Dimension für Kundenattribute hinzu.

Verwenden Sie diese CSV-Datei als Kundenattribut-Importdatei und abonnieren Sie dann Ihre Report Suite(s) für das Kundenattribut, wie in diesem [ beschrieben](https://blog.adobe.com/en/publish/2016/10/20/link-digital-behavior-customers).

![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/assets/bot-csv-4.png)

### Schritt 5: Erstellen Sie ein Segment, das das neue Kundenattribut nutzt.

Nachdem Ihr Datensatz verarbeitet und in Analysis Workspace integriert wurde, erstellen Sie ein weiteres Segment, das Ihre neue Kundenattributdimension „Bot Flag“ und einen [!UICONTROL Ausschließen]-Container nutzt:

![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/assets/bot-filter-seg2.png)

### Schritt 6: Dieses Segment als Virtual Report Suite-Filter verwenden

Erstellen Sie abschließend eine [Virtual Report Suite](/help/components/vrs/vrs-about.md) die dieses Segment verwendet, um die identifizierten Bots herauszufiltern:

![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/assets/bot-vrs.png)

Diese neu segmentierte Virtual Report Suite führt nun zu einem saubereren Datensatz, aus dem die identifizierten Bots entfernt wurden.

### Schritt 7: Schritte 2, 3 und 4 regelmäßig wiederholen

Legen Sie mindestens eine monatliche Erinnerung fest, um neue Bots zu identifizieren und auszufiltern, vielleicht vor der regelmäßig geplanten Analyse.

>[!MORELIKETHIS]
>
>* [Bessere Bot-Blockierung (Teil 1): Die Grundlagen](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/better-bot-blocking-part-1-the-basics/ba-p/715839)
>* [Better Bot Blocking (Teil 2): Identifizieren von Bots und Nutzung von CIDR](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/better-bot-blocking-part-2-identifying-bots-and-leveraging-cidr/ba-p/722132)
>* [Bessere Bot-Blockierung (Teil 3): Der Trefferregler](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/better-bot-blocking-part-3-the-hit-governor/ba-p/727051)

