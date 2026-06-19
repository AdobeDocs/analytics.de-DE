---
description: Systemanforderungen und ein Vergleich von Analysis Workspace, Report Builder, Data Warehouse und Data Workbench
title: Analytics – Produktvergleich und Voraussetzungen
exl-id: 5adc6c10-cbbb-48d5-a7ab-367cbaff5e8a
feature: Analytics Basics
TQID: https://experienceleague.adobe.com/VQgK6DUSlz-UA3zk-Q18-QOAI5M6xfK7KqBYwW56j6w
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: a421fb65-2c82-457a-921c-28c46b697a39id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: ac8a38fa-dec3-4581-8f64-178fde9f64e8id: af53ada8-1b7d-4929-ac91-ac971dd20ec7id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: b3a8b8a0-1cc2-48a8-ac82-ffd9c66ccab4id: c4cb071e-4667-4fb1-b1f1-d8994549cfb2id: c80b99d6-98b9-4aeb-b5c4-933ef2ef705cid: dcae653e-62c6-4cc8-84e6-ee110b848296id: e9cb007b-c8b7-4975-bc81-11a788c535faid: ef60b66e-5984-4336-ba72-6d978b1b6f87id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: d4db20e3498d54162806b3fdef0b34f45c93a6ff
workflow-type: tm+mt
source-wordcount: 530
ht-degree: 67%

---

# Analytics – Produktvergleich und Voraussetzungen

Diese Seite enthält einen Vergleich verschiedener Adobe Analytics-Produkte: Analysis Workspace, Report Builder, Data Warehouse, Daten-Feeds und Analytics-API 2.0.

Informationen dazu, welches Adobe Analytics-Produkt verwendet werden sollte, finden Sie unter [Welches Adobe Analytics-Tool sollte ich verwenden?](/help/analyze/get-started/which-analytics-tool.md).

| Produktname und Link zur Hilfe | [Analysis Workspace](/help/analyze/analysis-workspace/home.md) | [Report Builder](/help/analyze/report-builder/rb-overview.md) | [Data Warehouse](/help/export/data-warehouse/data-warehouse.md) | [Data Feeds](/help/export/analytics-data-feed/data-feed-overview.md) | [Analytics-API 2.0](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
|---|---|---|---|---|---|
| **Zugriffsmethode** | [Browser](/help/analyze/get-started/sys-reqs.md) | [MS Excel für Windows](/help/analyze/legacy-report-builder/setup/system-requirements.md) | Einrichtung über den Browser. [Weitere Informationen](/help/analyze/get-started/sys-reqs.md) | Einrichtung über den Browser. [Weitere Informationen](/help/export/analytics-data-feed/data-feed-overview.md) | RESTful-API-Tools. Melden Sie sich mit Adobe Developer-Anmeldeinformationen an. [Weitere Informationen](https://developer.adobe.com/analytics-apis/docs/2.0/) |
| **Datengranularität** | Aggregiert | Aggregiert | Aggregiert | Treffer | Aggregiert |
| **Experience Cloud ID (ECID) verfügbar** | Nein | Nein | Ja | Ja | Nein |
| **Zeitstempel verfügbar** | Nein | Nein | Nein | Ja | Nein |
| **Verarbeitungsstufe** | Vollständig verarbeitet | Vollständig verarbeitet, mit separatem [Echtzeitbericht](/help/admin/tools/manage-rs/edit-settings/realtime/realtime.md) | Vollständig verarbeitet | Vollständig verarbeitet | Vollständig verarbeitet |
| **Admin-Bot-Filterdaten enthalten** <br> [Weitere Infos](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-removal.md) | Nein | Ja - separater Bot-Bericht | Nein | Nein | Nein |
| **Geringer Traffic (Individuelle Werte überschritten) wird angezeigt** <br> [Weitere Informationen](/help/technotes/low-traffic.md) | Ja | Ja | Nein | Nein | Ja |
| **Begrenzung der sichtbaren Zeilen (vor der Paginierung)** | 400 | 50000 | Unbegrenzt | Unbegrenzt | 50000 |
| **Mehrere Report Suites** | [Ja](/help/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.md) | Ja | Nein | Ja | Nein |
| **Anzahl der Aufschlüsselungen** | Unbegrenzt | Bis zu 2 | Unbegrenzt | Unbegrenzt | Unbegrenzt, über mehrere Abfragen ausführen |
| **Segmentierung** <br> [Weitere Informationen](/help/components/segmentation/segmentation-workflow/seg-workflow.md) | Ja | Ja | Ja, mit [Einschränkungen](/help/export/data-warehouse/segment-compatibility.md) | Nein | Ja |
| **Berechnete Metriken** <br> [Weitere Infos](/help/components/calculated-metrics/cm-overview.md) | Ja, mit [Attribution](/help/analyze/analysis-workspace/attribution/overview.md) | Ja, mit Attribution | Ja | Nein | Ja, mit [Attribution](/help/analyze/analysis-workspace/attribution/overview.md) |
| **Marketing-Kanäle** <br> [Weitere Infos](/help/components/c-marketing-channels/c-getting-started-mchannel.md) | Ja | Ja | Ja | Ja – [va_finder, va_closer](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md) | Ja |
| **Kohortenanalyse** | [Ja](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) | Ja | Nein | Nein | Nein |
| **Attribution** | Ja, mit [Attribution](/help/analyze/analysis-workspace/attribution/overview.md) | Begrenzt | Nein | Nein | Ja, mit [Attribution](/help/analyze/analysis-workspace/attribution/overview.md) |
| **Kuratierung** <br> [Weitere Infos](/help/analyze/analysis-workspace/curate-share/curate.md) | Ja – Projekt und Virtual Report Suite | Nein | Nein | Nein | Ja – nur Virtual Report Suite |
| **Projektfreigabe** <br> [Weitere Infos](/help/analyze/analysis-workspace/curate-share/share-projects.md) | Ja, mit Projektrollen | Ja | Nein | Nein | Nein |
| **Geplanter Versand** | Ja | Ja | Ja | Ja | Nein |
| **Versandziele** | E-Mail | E-Mail, FTP, SFTP, [Veröffentlichung auf Microsoft Power BI](/help/analyze/legacy-report-builder/c-publish-power-bi/power-bi.md) | Amazon S3, Google Cloud Platform, Azure SAS, Azure RBAC und E-Mail | Amazon S3, Azure RBAC, Azure SAS und Google Cloud Platform | – |
| **Berichtszeitverarbeitung von Virtual Report Suite** <br> [Weitere Informationen](/help/components/vrs/vrs-report-time-processing.md) | Ja | Nein | Nein | Nein | Ja |
| **Geo- und Technologieberichte** | Ja <p>Verwendet Mid-Werte statt Post-Felder. Die Logik für den Erstbesuch basiert auf `post_cust_hit_time_gmt` statt auf `visit_page_num=1`. Die Ergebnisse können von anderen Tools abweichen, wenn sich die IP-Adresse während des Besuchs ändert, Treffer nicht in der richtigen Reihenfolge eingehen oder Besuche monatlich erfolgen.</p> | Ja <p>Verwendet Mid-Werte statt Post-Felder. Die Logik für den Erstbesuch basiert auf `post_cust_hit_time_gmt` statt auf `visit_page_num=1`. Die Ergebnisse können von anderen Tools abweichen, wenn sich die IP-Adresse während des Besuchs ändert, Treffer nicht in der richtigen Reihenfolge eingehen oder Besuche monatlich erfolgen.</p> | Ja <p>Verwendet POST-Werte und -`visit_page_num=1`, um den ersten Treffer des Besuchs zu bestimmen. Wendet für diese Dimensionen den Wert aus dem ersten Treffer auf alle Treffer im Besuch an.</p> | Ja <p>Verwendet POST-Werte und -`visit_page_num=1`, um den ersten Treffer des Besuchs zu bestimmen. Wendet für diese Dimensionen den Wert aus dem ersten Treffer auf alle Treffer im Besuch an.</p> | Ja <p>Verwendet Mid-Werte statt Post-Felder. Die Logik für den Erstbesuch basiert auf `post_cust_hit_time_gmt` statt auf `visit_page_num=1`. Die Ergebnisse können von anderen Tools abweichen, wenn sich die IP-Adresse während des Besuchs ändert, Treffer nicht in der richtigen Reihenfolge eingehen oder Besuche monatlich erfolgen.</p> |
