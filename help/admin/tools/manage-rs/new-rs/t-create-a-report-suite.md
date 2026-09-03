---
description: Erstellen eines einfachen Containers für die Datenerfassung in Adobe Analytics
title: Erstellen einer Report Suite
feature: Report Suite Settings
exl-id: 255ae051-d993-41a5-8cf3-819a54c17e34
TQID: https://experienceleague.adobe.com/ZmPcYHvXOhaXXnqsSVUh1bpvignxomS3d4S76iMCAa4
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
subfeature_v2: id: c4cb071e-4667-4fb1-b1f1-d8994549cfb2
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11id: d3cdead0-685a-4489-9250-4bb709942f66id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: c2ae876122715b4fa6367326dc23479dd9648021
workflow-type: tm+mt
source-wordcount: 312
ht-degree: 87%

---

# Erstellen einer Report Suite

Bei einer Report Suite handelt es sich um einen Datenspeicher, mit dem Adobe Analytics Berichte abruft. Eine Organisation kann über viele Report Suites verfügen, die jeweils unterschiedliche Datensätze enthalten. Auch wenn in der Vergangenheit separate Report Suites wichtig waren, hat sich eine einzelne Report Suite als vorteilhafter erwiesen. Die Einführung von [Virtual Report Suites](/help/components/vrs/vrs-about.md#virtual-report-suites) und die Verarbeitung von Berichtszeiten ermöglicht es Administratoren, eigene Teilmengen von Daten zu erstellen, was die Flexibilität bietet, sowohl globale als auch Site-spezifische Daten zu erhalten.

Dieser Artikel wurde für Administratoren oder Adobe Analytics-Administratoren auf Systemebene zur Vorbereitung auf die Datenerfassung erstellt.

## Voraussetzungen

[Adobe Analytics First Admin Guide](/help/admin/admin-console/first-admin-guide.md): Vergewissern Sie sich, dass Ihnen ein Systemadministrator über die CX Enterprise Admin Console Zugriff auf Adobe Analytics gewährt hat.

## Erstellen einer Report Suite {#create-report-suite}

1. Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Klicken Sie **[!UICONTROL Report Suite hinzufügen]**.
1. Wählen Sie entweder eine vordefinierte Vorlage oder eine vorhandene Report Suite als [Vorlage](/help/admin/tools/manage-rs/rs-templates/report-suite-templates.md) aus.

   >[!NOTE]
   >
   >Es können nur Einstellungen und keine Daten kopiert werden. Wenn die Kundenunterstützung die Einstellungen kopiert, müssen Sie den Haftungsausschluss der Kundenunterstützung bezüglich der involvierten Risiken schriftlich bestätigen. Weitere Informationen finden Sie unter [Aus einer Quell-Report Suite nicht kopierte Einstellungen](/help/admin/tools/manage-rs/new-rs/settings-not-copied-from-rs.md).

1. Füllen Sie die unter [Neue Report Suite](/help/admin/tools/manage-rs/new-rs/new-report-suite.md) beschriebenen Felder aus.
1. Klicken Sie auf **[!UICONTROL Report Suite erstellen]**.

Eine Report Suite-ID hat eine maximale Länge von 40 Byte. Ein benutzerfreundlicher Name einer Report Suite hat eine maximale Länge von 255 Byte.

## Fehlerbehebung

**Nach der Anmeldung bei CX Enterprise ist das Analytics-Symbol ausgegraut.**

Das bedeutet, dass Ihrem Konto nicht die richtigen Berechtigungen für Analytics erteilt wurden. Arbeiten Sie mit einem Administrator auf Systemebene in Ihrer Organisation zusammen, um sicherzustellen, dass Sie zu einem Profil gehören, das über ausreichende Zugriffsberechtigungen für Adobe Analytics verfügt.

## Nächste Schritte

[Erstellen einer Adobe Analytics-Tag-Eigenschaft](/help/implement/launch/create-analytics-property.md): Erstellen eines Bereichs zur Verwaltung Ihrer Analytics-Implementierung.
