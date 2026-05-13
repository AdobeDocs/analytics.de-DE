---
title: list
description: Benutzerdefinierte Variablen, die mehrere Werte im selben Treffer enthalten.
feature: Appmeasurement Implementation
exl-id: 612f6f10-6b68-402d-abb8-beb6f44ca6ff
role: Admin, Developer
TQID: https://experienceleague.adobe.com/LpUX55ZGYgm7Z2-P4uAwH-rV88JMbi2661i4f9RYd-Q
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: c4cb071e-4667-4fb1-b1f1-d8994549cfb2id: fab61dd8-112a-4e5e-ad5f-fb0240b7a60b
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 503
ht-degree: 74%

---

# list

Listenvariablen sind benutzerspezifische Variablen, die Sie beliebig verwenden können. Sie funktionieren ähnlich wie eVars, allerdings können sie mehrere Werte im selben Treffer enthalten. Listenvariablen haben keine Zeichenbeschränkung.

Vergewissern Sie sich, dass Sie die Verwendung der einzelnen Listenvariablen und deren Logik in Ihrem [Lösungs-Design-Dokument](../../prepare/solution-design.md) aufzeichnen.

>[!NOTE]
>
>Listenvariablen speichern die neuesten Werte pro Besucher basierend auf ihrer Einstellung [!UICONTROL Max] in [Report Suite-Einstellungen](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/list-var-admin.md). Es werden bis zu 250 Werte unterstützt. Wenn es mehr eindeutige Werte gibt, als die Einstellung [!UICONTROL Max] zulässt, werden die ältesten Werte nicht den Metriken zugeordnet.

## Einrichten von Listenvariablen in den Report Suite-Einstellungen

Stellen Sie sicher, dass Sie jede Listenvariable in den Report Suite-Einstellungen konfigurieren, bevor Sie sie in Ihrer Implementierung verwenden. Weitere Informationen finden Sie im Admin-Handbuch unter [Konversionsvariablen](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/list-var-admin.md). Dieser Schritt gilt für alle Implementierungsmethoden.

## Listenvariablen, die das Web SDK verwenden

Bei Verwendung des [**XDM-**](/help/implement/aep-edge/xdm-var-mapping.md)) verwenden Listenvariablen die zu `xdm._experience.analytics.customDimensions.lists.list3.list[]` XDM-Felder `xdm._experience.analytics.customDimensions.lists.list1.list[]` . Jedes Array-Element enthält ein `"value"`-Objekt, das jede Zeichenfolge enthält. Es ist nicht erforderlich, ein Trennzeichen anzugeben. Datenerfassungs-Server von Adobe erkennen automatisch das richtige Trennzeichen, das in den [Report Suite-Einstellungen“ festgelegt ](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/list-var-admin.md).

```json
"xdm": {
  "_experience": {
    "analytics": {
      "customDimensions": {
        "lists": {
          "list1": {
            "list": [
              {
                "value": "Example value 1"
              },
              {
                "value": "Example value 2"
              },
              {
                "value": "Example value 3"
              }
            ]
          }
        }
      }
    }
  }
}
```

>[!NOTE]
>
>Das Adobe-XDM-Schema enthält `key`-Objekte zusätzlich zu `value`-Objekten in jedem `list[]`-Array. Adobe verwendet diese `key`-Objekte nicht beim Senden von Daten an Adobe Analytics.

Bei Verwendung des [**Datenobjekts**](/help/implement/aep-edge/data-var-mapping.md) verwenden Listenvariablen `data.__adobe.analytics.list1` - `data.adobe.analytics.list3` der folgenden AppMeasurement-Syntax. Stellen Sie sicher, dass Sie das richtige Trennzeichen verwenden, das in [Report Suite-Einstellungen“ festgelegt ](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/list-var-admin.md).

```json
"data": {
  "__adobe": {
    "analytics": {
      "list1": "Example value 1,Example value 2,Example value 3"
    }
  }
}
```

## Listenvariablen, die die Adobe Analytics-Erweiterung verwenden

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.list1 – s.list3 in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Jede Listenvariable ist eine Zeichenfolge, die für Ihr Unternehmen spezifische benutzerdefinierte Werte enthält. Diese Variable hat keine maximale Byteanzahl; jedoch hat jeder einzelne Wert eine maximale Anzahl von 255 Byte. Das Trennzeichen, das Sie verwenden, wird beim Einrichten der Variablen in den [Report Suite-Einstellungen](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/list-var-admin.md) festgelegt. Verwenden Sie keine Leerzeichen, wenn Sie mehrere Elemente trennen.

```js
// A list variable configured with a comma as a delimiter
s.list1 = "Example value 1,Example value 2,Example value 3";
```

>[!TIP]
>
>Wenn Sie im selben Treffer doppelte Werte festlegen, dedupliziert Adobe alle Instanzen dieser Werte. Wenn Sie z. B. `s.list1 = "Brick,Brick";` festlegen, wird eine Instanz in Berichten gezählt.

## Vergleich von Listen-Props mit Listenvariablen

Listen-Props und Listenvariablen können beide im selben Treffer mehrere Werte enthalten. Zwischen diesen beiden Variablentypen gibt es jedoch einige wichtige Unterschiede.

* Jede Prop kann eine Listen-Prop werden. Sie können bis zu 75 Listen-Props haben, wenn jede Prop eine Listen-Prop ist. Es sind nur drei Listenvariablen verfügbar.
* Listen-Props haben eine 100-Byte-Grenze für die gesamte Variable. Listenvariablen haben eine 255-Byte-Grenze pro Wert und keine Gesamt-Byte-Grenze.
* Listen-Props bleiben nicht über den festgelegten Treffer hinaus erhalten. Für Listenvariablen gelten die gewünschten Gültigkeitseinstellungen. Bei der [Berichtszeitverarbeitung](/help/components/vrs/vrs-report-time-processing.md) können Sie jedoch sowohl auf Listen-Props als auch auf Listenvariablen eine benutzerdefinierte Attribution anwenden.
