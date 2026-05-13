---
title: Datenschicht erstellen
description: Erfahren Sie, was eine Datenschicht in Ihrer Analytics-Implementierung ist und wie sie zur Zuordnung von Variablen in Adobe Analytics verwendet werden kann.
feature: Implementation Basics
exl-id: 271dd8fa-3ba1-4a7f-b16a-c48a736a5bb5
role: Admin, Developer, Leader
TQID: https://experienceleague.adobe.com/JmxM3-AVA5--7Xt4kuES35KFtYbicdGO9JZXsygzuuE
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: df312454-73c4-43f6-a90e-18f5043f074cid: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 476
ht-degree: 100%

---

# Datenschicht erstellen

Eine Datenschicht ist ein Framework von JavaScript-Objekten auf Ihrer Site, die die in Ihrer Analytics-Implementierung verwendeten Variablenwerte enthalten. Dies ermöglicht eine bessere Kontrolle und einfachere Wartung beim Zuweisen von Werten zu Analytics-Variablen.

## Voraussetzungen

[Erstellen Sie ein Lösungsdesigndokument](solution-design.md): Für Ihr Unternehmen ist es wichtig, die Tracking-Anforderungen abzustimmen. Stellen Sie sicher, dass Sie ein Lösungs-Design-Dokument vorbereitet haben, bevor Sie sich an die Entwicklungs-Teams in Ihrer Organisation wenden.

## Workflow

Die Implementierung von Adobe Analytics mit einer Datenschicht folgt normalerweise diesen Schritten:

1. **Arbeiten Sie mit Ihrem Website-Entwicklungs-Team zusammen, um eine Datenschicht zu implementieren**: Ihr Website-Entwicklungs-Team ist in erster Linie dafür verantwortlich, dass das Datenschichtobjekt mit den richtigen Werten gefüllt wird. Gehen Sie diese Seite mit Ihrem Website-Entwicklungs-Team durch, um sicherzustellen, dass die Erwartungen zwischen den Teams abgestimmt sind.

   >[!NOTE]
   >
   >Das Befolgen der von Adobe empfohlenen Datenschichtspezifikationen ist optional. Wenn Sie bereits über eine Datenschicht verfügen oder sich anderweitig gegen die Adobe-Spezifikationen entscheiden, stellen Sie sicher, dass Ihre Organisation sich an den zu befolgenden Spezifikationen orientiert.

1. **Validieren Sie Ihre Datenschicht mithilfe einer Browser-Konsole**: Sobald eine Datenschicht erstellt ist, können Sie mit der Entwicklerkonsole eines beliebigen Browsers überprüfen, ob sie funktioniert. Sie können die Entwicklerkonsole in den meisten Browsern mit der Taste `F12` öffnen. Ein Beispiel für einen Variablenwert wäre `adobeDataLayer.page.title`.
1. **Verwenden der Adobe Experience Platform-Datenerfassung zum Zuordnen von Datenschichtobjekten zu Datenelementen**: Dieser Schritt variiert je nach Implementierungsmethode Ihrer Organisation:
   * **Bei Verwendung des Web SDK**: Ordnen Sie die gewünschten Datenschichtobjekte den gewünschten XDM-Feldern in Adobe Experience Platform Edge zu. Siehe [Zuordnen von Analytics-XDM-Variablen](../aep-edge/xdm-var-mapping.md), um die gewünschte Datenschichtzuordnung zu bestimmen.
   * **Bei Verwendung der Analytics-Erweiterung**: Erstellen Sie Datenelemente unter „Tags“ in der Adobe Experience Platform-Datenerfassung und weisen Sie sie den gewünschten Datenschichtobjekten zu. Weisen Sie dann innerhalb der Analytics-Erweiterung jedes Datenelement der entsprechenden Analytics-Variablen zu.

## Spezifikationen

Adobe empfiehlt die Verwendung der [Adobe Client-Datenschicht](https://github.com/adobe/adobe-client-data-layer/wiki) für neue oder umstrukturierte Implementierungen.

Ihre Organisation kann andere Datenschichtspezifikationen verwenden, z. B. die [Customer Experience Digital-Datenschicht](https://www.w3.org/2013/12/ceddl-201312.pdf), oder eine völlig andere benutzerdefinierte Spezifikation. Am wichtigsten ist die Zuweisung zu einer konsistenten Datenschicht, die den Anforderungen Ihrer Organisation entspricht.

Datenschichten sind erweiterbar. Wenn Sie unternehmensspezifische Anforderungen haben, können Sie Objekte in Ihre Datenschicht aufnehmen, um diese Anforderungen zu erfüllen.

## Festlegen von Datenschichtwerten

Datenschichten werden normalerweise Server-seitig generiert und verweisen auf dieselben Objekte, die zum Erstellen des Website-Inhalts verwendet wurden. Richten Sie die Datenschicht der Website anhand der im [Lösungsdesigndokument](solution-design.md) Ihres Unternehmens festgelegten Tracking-Anforderungen ein.

## Nächste Schritte

[Ordnen Sie Datenschichtobjekte Datenelementen zu](../launch/layer-to-elements.md): Verwenden Sie die Datenschicht Ihrer Site in Adobe Experience Platform.
