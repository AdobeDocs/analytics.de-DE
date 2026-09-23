---
title: Trackingcode
description: Der Name des Trackingcodes oder der Kampagne.
feature: Dimensions
exl-id: e4f70552-6946-4974-a9e2-928faf563ecd
TQID: https://experienceleague.adobe.com/8e9126PxGCNXJqo4a3XYTgXwrcHdf34FVwygpHXm5JI
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 88%
---
# Trackingcode

In der [Dimension](overview.md) „Trackingcode“ werden die Namen der Trackingcodes auf Ihrer Site aufgelistet. Sie können Links mit verschiedenen Parameterwerten für Abfragezeichenfolgen an verschiedenen Stellen im Internet platzieren. Diese Dimension hilft Ihnen zu verstehen, welche Links am erfolgreichsten dazu beigetragen haben, den Traffic auf Ihre Site zu lenken.

Das Anhängen von Trackingcode-Abfragezeichenfolgen erfolgt häufig in E-Mails, Anzeigen, Social Media-Posts und anderen Marketing-Maßnahmen Ihrer Organisation.

## Füllen dieser Dimension mit Daten

AppMeasurement erfasst diese Daten mit der [`campaign`](/help/implement/vars/page-vars/campaign.md)-Variable. Diese Variable erhält ihren Wert normalerweise aus einer Abfragezeichenfolge unter Verwendung der [`getQueryParam`](/help/implement/vars/plugins/getqueryparam.md)-Hilfsmethode, obwohl Ihr Unternehmen genau bestimmt, wie sie festgelegt wird.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | [`campaign`](/help/implement/vars/page-vars/campaign.md) |
| **Feld Web SDK/XDM** | [`marketing.trackingCode`](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/campaign-marketing-details) |
| **Abfrageparameter** | [`v0`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<campaign>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Byte-Grenze** | 255 Byte |
| **Persistenz** | Konfigurierbar |

## Dimensionselemente

Zu den Dimensionselementen gehören die Namen der Trackingcodes auf Ihrer Site. Ihr Unternehmen legt fest, welche spezifischen Dimensionselemente Sie verwenden möchten. Weitere Informationen finden Sie unter [Kampagnen-Tracking](/help/implement/use-cases/campaign-tracking.md).

## Dimension „Trackingcode“ mit Dimension „Marketing-Kanäle“ vergleichen, die Trackingcodes erfasst

Einige Benutzer, die Verarbeitungsregeln für Marketing-Kanäle einrichten, konfigurieren eine Regel, die alle in der Dimension „Trackingcode“ verwendeten Werte berücksichtigt. Obwohl es sich um eine hervorragende Praxis handelt, unterscheiden sie sich aufgrund der inhärenten Verarbeitungs- und Architekturunterschiede. In der folgenden Liste wird erklärt, warum diese beiden Methoden, obwohl sie auf den ersten Blick ähnlich erscheinen, das Attributionsverhalten ändern können.

### Vorherige Kanäle in Verarbeitungsregeln

Verarbeitungsregeln für Marketing-Kanäle, die in der Liste weiter oben stehen, können verhindern, dass Treffer Ihrem Marketing-Kanal für Trackingcodes zugeordnet werden. Zum Beispiel:

1. Sie haben als erste Regel „Soziale Netzwerke“ und als zweite „Trackingcodes“ eingerichtet.
2. Ein Benutzer stellt einen Link zu Ihrer Site mit einem Trackingcode auf einer Social-Media-Website ein, und mehrere seiner Freunde klicken auf diesen Link zu Ihrer Site.

Da „Soziale Netzwerke“ die erste Verarbeitungsregel für Marketing-Kanäle ist, werden diese Benutzenden dem Marketing-Kanal „Soziale Netzwerke“ und nicht Ihrem Marketing-Kanal „Trackingcodes“ zugeordnet.

### Andere Marketing-Kanäle können die Attribution über den Letztkontakt übernehmen

Wenn es sich um eine standardmäßige Dimension „Trackingcodes“ handelt, müssen Sie sich keine Sorgen machen, dass andere Bereiche Ihrer Site die Attribution stehlen. Bei Marketing-Kanälen kann ein Benutzer jedoch eine andere Regel anwenden und eine andere Attribution vornehmen. Zum Beispiel:

1. Sie haben „Trackingcodes“ als ersten Kanal und „Direkt“ als zweiten.
2. Ein Benutzer gelangt zunächst über einen Trackingcode zu Ihrer Site, verlässt dann jedoch die Site.
3. Am nächsten Tag geben sie Ihre URL in ihre Adressleiste ein und tätigen dann einen Kauf.

In diesem Beispiel würde der Marketing-Kanal für „Trackingcodes“ für diesen Kauf keine Letztkontakt-Gewichtung erhalten. Stattdessen würde dies dem Marketing-Kanal „Direkt“ gutgeschrieben.


### Unterschiede beim Ablauf

Marketing-Kanäle haben ein rollierendes 30-tägiges Zeitfenster für Besucherinteraktionen, unabhängig davon, ob ein Kanal verwendet wurde oder nicht. Die Gültigkeit von Trackingcodes basiert auf dem Zeitpunkt, zu dem die Variable festgelegt wurde. Zum Beispiel:

1. Sie haben einen Ablauf der Besucherinteraktion von 30 Tagen und die Dimension „Trackingcode“ so konfiguriert, dass sie nach 30 Tagen abläuft.
2. Ein Benutzer gelangt über einen Trackingcode zu Ihrer Site. Er durchsucht die Site und verlässt sie anschließend.
3. Drei Wochen später kehrt er ohne Trackingcode oder Marketing-Kanal zurück und verlässt die Seite erneut.
4. Zwei weitere Wochen später (fünf Wochen nach dem ersten Besuch) kehrt er ohne Trackingcode oder Marketing-Kanal zurück und tätigt dann einen Kauf.

Der Nutzer tätigte letztendlich einen Kauf nach mehr als 30 Tagen, war aber nie länger als 30 Tage inaktiv. In diesem Fall würden Sie Umsatz sehen, der dem Marketing-Kanal für Trackingcodes zugeordnet ist, jedoch nicht der Dimension „Trackingcode“ selbst.



