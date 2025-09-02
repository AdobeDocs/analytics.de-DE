---
title: Implementieren von Adobe Analytics mit Adobe Experience Platform Edge
description: Übersicht über die Verwendung von XDM-Daten aus Experience Platform in Adobe Analytics
exl-id: 7d8de761-86e3-499a-932c-eb27edd5f1a3
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: 0ea86e7628e3cebe6f5fe1c4f584da1186b8cb83
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 16%

---

# Implementieren von Adobe Analytics mit dem Adobe Experience Platform Edge Network

Mit Adobe Experience Platform Edge Network können Sie Daten, die für mehrere Produkte bestimmt sind, an einen zentralen Ort senden. Edge Network leitet die entsprechenden Informationen an die gewünschten Produkte weiter. Mit diesem Konzept können Sie Implementierungsaufgaben zusammenfassen, insbesondere, wenn mehrere Datenlösungen vorhanden sind. Adobe Analytics ist eines der Produkte, an das Sie Daten mithilfe von Edge Network senden können.

## Verarbeiten von Edge Network-Daten durch Adobe Analytics

Da die an die Edge Network gesendeten Daten und die Daten von AppMeasurement unterschiedlich funktionieren, bestimmt die Edge Network-Payload, wie Adobe Analytics den Treffer verarbeitet. Weitere Informationen finden Sie unter [Ereignistypen für Edge Network ](hit-types.md) Adobe Analytics.

Daten, die an Adobe Experience Platform Edge Network gesendet werden, können drei Formaten entsprechen **(XDM**, **Datenobjekt** und **Kontextdaten**. Wenn ein Datenstrom Daten an Adobe Analytics weiterleitet, werden sie in ein Format übersetzt, das Adobe Analytics verarbeiten kann.

## `xdm`

Entsprechen Sie den Schemata, die Sie basierend auf [XDM](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/home) (Experience-Datenmodell) erstellen. Mit XDM können Sie flexibel bestimmen, welche Felder als Teil von Ereignissen definiert werden. Wenn Sie ein vordefiniertes Schema verwenden möchten, das speziell für Adobe Analytics gilt, können Sie die Schemafeldgruppe [Adobe Analytics ExperienceEvent](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/field-groups/event/analytics-full-extension) zu Ihrem Schema hinzufügen. Nach dem Hinzufügen können Sie dieses Schema mithilfe des `xdm`-Objekts in der Web-SDK ausfüllen, um Daten an eine Report Suite zu senden. Wenn Daten an der Edge Network eingehen, wird das XDM-Objekt in ein Format übersetzt, das Adobe Analytics versteht.

Siehe [XDM-Objektvariablenzuordnung zu Adobe Analytics](xdm-var-mapping.md) für eine vollständige Referenz zu XDM-Feldern und deren Zuordnung zu Analytics-Variablen.

>[!TIP]
>
>Wenn Sie beabsichtigen, in Zukunft zu [Customer Journey Analytics](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-landing) zu wechseln, rät Adobe davon ab, die Schemafeldgruppe von Adobe Analytics zu verwenden. Stattdessen empfiehlt Adobe [Erstellen eines eigenen Schemas](https://experienceleague.adobe.com/de/docs/analytics-platform/using/compare-aa-cja/upgrade-to-cja/schema/cja-upgrade-schema-architect) und die Verwendung der Datenstromzuordnung, um die gewünschten Analytics-Variablen zu befüllen. Durch diese Strategie werden Sie nicht an ein Schema von Props und eVars gebunden, wenn Sie für den Wechsel zu Customer Journey Analytics bereit sind.

## `data`

Als Alternative zur Verwendung des `xdm` -Objekts können Sie stattdessen das `data` -Objekt verwenden. Das Datenobjekt ist auf Implementierungen ausgerichtet, die derzeit AppMeasurement verwenden, was das Upgrade auf die Web-SDK viel einfacher macht. Edge Network erkennt das Vorhandensein von Adobe Analytics-spezifischen Feldern, ohne dass ein Schema eingehalten werden muss.

Unter [Zuordnung von Datenobjektvariablen zu Adobe Analytics](data-var-mapping.md) finden Sie eine vollständige Referenz zu Datenobjektfeldern und deren Zuordnung zu Analytics-Variablen.

## Kontextdatenvariablen

Senden Sie Daten in einem beliebigen Format an die Edge Network. Alle Felder, die nicht automatisch `xdm`- oder `data` Objektfeldern zugeordnet werden, werden bei [ Weiterleitung an Adobe Analytics als Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md) einbezogen. Anschließend müssen Sie [Verarbeitungsregeln](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-overview.md) verwenden, um die gewünschten Felder ihren jeweiligen Analytics-Variablen zuzuordnen.

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
