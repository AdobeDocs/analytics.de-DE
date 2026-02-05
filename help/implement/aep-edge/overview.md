---
title: Implementieren von Adobe Analytics mit Adobe Experience Platform Edge
description: Übersicht über die Verwendung von XDM-Daten aus Experience Platform in Adobe Analytics
exl-id: 7d8de761-86e3-499a-932c-eb27edd5f1a3
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: 9845f1bc73b6cf5fd932c6896a50379ddd008c20
workflow-type: ht
source-wordcount: '550'
ht-degree: 100%

---

# Implementieren von Adobe Analytics mit dem Adobe Experience Platform Edge Network

Mit Adobe Experience Platform Edge Network können Sie Daten, die für mehrere Produkte bestimmt sind, an einen zentralen Ort senden. Edge Network leitet die entsprechenden Informationen an die gewünschten Produkte weiter. Mit diesem Konzept können Sie Implementierungsaufgaben zusammenfassen, insbesondere, wenn mehrere Datenlösungen vorhanden sind. Adobe Analytics ist eines der Produkte, an die Sie mithilfe von Edge Network Daten senden können.

## Verarbeiten von Edge Network-Daten durch Adobe Analytics

Da über Edge Network gesendete Daten und AppMeasurement-Daten unterschiedlich funktionieren, bestimmt die Edge Network-Payload, wie Adobe Analytics den Treffer verarbeitet. Weitere Informationen finden Sie unter [Edge Network-Ereignistypen in Adobe Analytics](hit-types.md).

Daten, die an Adobe Experience Platform Edge Network gesendet werden, können drei Formate aufweisen: **XDM-Objekt**, **Datenobjekt** und **Kontextdaten**. Wenn ein Datenstrom Daten an Adobe Analytics weiterleitet, werden sie in ein Format übersetzt, das Adobe Analytics verarbeiten kann.

## Objekt `xdm`

Entsprechen Schemata, die Sie basierend auf [XDM](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/home) (Experience-Datenmodell) erstellen. Mit XDM können Sie flexibel bestimmen, welche Felder als Teil von Ereignissen definiert werden. Wenn Sie ein vordefiniertes, Adobe Analytics-spezifisches Schema verwenden möchten, können Sie die [Schemafeldergruppe „Adobe Analytics ExperienceEvent“](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/field-groups/event/analytics-full-extension) zu Ihrem Schema hinzufügen. Nach dem Hinzufügen können Sie dieses Schema mithilfe des Objekts `xdm` in Web SDK ausfüllen, um Daten an eine Report Suite zu senden. Wenn Daten beim Edge Network eingehen, wird das XDM-Objekt in ein Format übersetzt, das Adobe Analytics versteht.

Die vollständige Referenz zu XDM-Feldern und ihrer Zuordnung zu Analytics-Variablen finden Sie in [Zuordnen von XDM-Objektvariablen zu Adobe Analytics](xdm-var-mapping.md).

>[!TIP]
>
>Wenn Sie in Zukunft zu [Customer Journey Analytics](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-landing) wechseln möchten, rät Adobe von der Verwendung der Schemafeldergruppe in Adobe Analytics ab. Stattdessen empfiehlt Adobe das [Erstellen eines eigenen Schemas](https://experienceleague.adobe.com/de/docs/analytics-platform/using/compare-aa-cja/upgrade-to-cja/schema/cja-upgrade-schema-architect) und die Verwendung der Datenstromzuordnung, um die gewünschten Analytics-Variablen auszufüllen. Diese Strategie legt Sie nicht auf ein Schema aus Props und eVars fest, wenn Sie für den Wechsel zu Customer Journey Analytics bereit sind.

## Objekt `data`

Als Alternative zur Verwendung des Objekts `xdm` können Sie stattdessen das Objekt `data` verwenden. Das Datenobjekt ist auf Implementierungen ausgerichtet, die derzeit AppMeasurement verwenden, was die Aktualisierung auf Web SDK erheblich erleichtert. Das Edge Network erkennt das Vorhandensein von Adobe Analytics-spezifischen Feldern, ohne dass eine Entsprechung mit einem Schema erforderlich ist.

Die vollständige Referenz zu Datenobjektfeldern und ihrer Zuordnung zu Analytics-Variablen finden Sie in [Zuordnen von Datenobjektvariablen zu Adobe Analytics](data-var-mapping.md).

## Kontextdatenvariablen

Senden Sie Daten in einem beliebigen Format an das Edge Network. Alle Felder, die den Objektfeldern `xdm` oder `data` nicht automatisch zugeordnet werden, werden bei der Weiterleitung an Adobe Analytics als [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md) einbezogen. Anschließend müssen Sie [Verarbeitungsregeln](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md) verwenden, um die gewünschten Felder den entsprechenden Analytics-Variablen zuzuordnen.

Angenommen, Sie haben ein benutzerdefiniertes XDM-Schema, das wie folgt aussieht:

```json
{
  "xdm": {
    "key": "value",
    "animal": {
      "species": "Raven",
      "size": "13 inches"
    },
    "array": [
      "v0",
      "v1",
      "v2"
    ],
    "objectArray":[{
      "ad1": "300x200",
      "ad2": "60x240",
      "ad3": "600x50"
    }]
  }
}
```

Dann wären diese Felder die Kontextdatenschlüssel, die Ihnen in der Benutzeroberfläche für Verarbeitungsregeln zur Verfügung stehen:

```javascript
a.x.key // value
a.x.animal.species // Raven
a.x.animal.size // 13 inches
a.x.array.0 // v0
a.x.array.1 // v1
a.x.array.2 // v2
a.x.objectarray.0.ad1 // 300x200
a.x.objectarray.1.ad2 // 60x240
a.x.objectarray.2.ad3 // 600x50
```

Die maximale Größe für die Payload einer bestimmten Kontextdatenvariable (einschließlich Schlüssel und Werte) beträgt 32 KB. Sie können die Größe dieser Payload reduzieren, indem Sie die entsprechenden Felder so anpassen, dass sie von Adobe Analytics in den Objekten [`xdm`](xdm-var-mapping.md) oder [`data`](data-var-mapping.md) erkannt werden.
