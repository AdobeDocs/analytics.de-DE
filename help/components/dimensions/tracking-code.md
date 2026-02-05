---
title: Trackingcode
description: Der Name des Trackingcodes oder der Kampagne.
feature: Dimensions
exl-id: e4f70552-6946-4974-a9e2-928faf563ecd
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: ht
source-wordcount: '559'
ht-degree: 100%

---

# Trackingcode

In der [Dimension](overview.md) „Trackingcode“ werden die Namen der Trackingcodes auf Ihrer Site aufgelistet. Sie können Links mit verschiedenen Abfragezeichenfolgenparameterwerten an verschiedenen Stellen im Internet platzieren. Diese Dimension hilft Ihnen zu verstehen, welche Links am erfolgreichsten dazu beigetragen haben, den Traffic auf Ihre Site zu lenken.

Das Anhängen von Trackingcode-Abfragezeichenfolgen erfolgt häufig in E-Mails, Anzeigen, Social Media-Posts und anderen Marketing-Maßnahmen Ihrer Organisation.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [`v0` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mit der [`campaign`](/help/implement/vars/page-vars/campaign.md)-Variable.

## Dimensionselemente

Zu den Dimensionselementen gehören die Namen der Trackingcodes auf Ihrer Site. Ihr Unternehmen legt fest, welche spezifischen Dimensionselemente Sie verwenden möchten. Weitere Informationen finden Sie unter [Kampagnen-Tracking](/help/implement/use-cases/campaign-tracking.md).

## Dimension „Trackingcode“ mit Dimension „Marketing-Kanäle“ vergleichen, die Trackingcodes erfasst

Einige Benutzer, die Verarbeitungsregeln für Marketing-Kanäle einrichten, konfigurieren eine Regel, die alle in der Dimension „Trackingcode“ verwendeten Werte berücksichtigt. Obwohl es sich um eine hervorragende Praxis handelt, unterscheiden sie sich aufgrund der inhärenten Verarbeitungs- und Architekturunterschiede. In der folgenden Liste wird erklärt, warum diese beiden Methoden, obwohl sie auf den ersten Blick ähnlich erscheinen, das Attributionsverhalten ändern können.

### Vorherige Kanäle in Verarbeitungsregeln

Verarbeitungsregeln für Marketing-Kanäle, die in der Liste weiter oben stehen, können verhindern, dass Treffer Ihrem Marketing-Kanal für Trackingcodes zugeordnet werden. Zum Beispiel:

1. Sie haben als erste Regel „Soziale Netzwerke“ und als zweite „Trackingcodes“ eingerichtet.
2. Ein Benutzer stellt einen Link zu Ihrer Site mit einem Trackingcode auf einer Social-Media-Website ein, und mehrere seiner Freunde klicken auf diesen Link zu Ihrer Site.

Da „Soziale Netzwerke“ die erste Verarbeitungsregel für Marketing-Kanäle ist, werden diese Benutzer dem Marketing-Kanal „Soziale Netzwerke“ und nicht Ihrem Marketing-Kanal für Trackingcodes zugeordnet.

### Andere Marketing-Kanäle können die Attribution über den Letztkontakt übernehmen

Wenn es sich um eine standardmäßige Dimension „Trackingcodes“ handelt, müssen Sie sich keine Sorgen zu machen, dass andere Bereiche Ihrer Site die Attribution stehlen. Bei Marketing-Kanälen kann ein Benutzer jedoch eine andere Regel anwenden und eine andere Attribution vornehmen. Zum Beispiel:

1. Sie haben „Trackingcodes“ als ersten Kanal und „Direkt“ als zweiten.
2. Ein Benutzer gelangt zunächst über einen Trackingcode zu Ihrer Site, verlässt dann jedoch die Site.
3. Am nächsten Tag geben sie Ihre URL in ihre Adressleiste ein und tätigen dann einen Kauf.

In diesem Beispiel würde der Marketing-Kanal für „Trackingcodes“ für diesen Kauf keine Letztkontakt-Gewichtung erhalten. Stattdessen würde er dem Marketing-Kanal „Direkt“ gutgeschrieben.


### Unterschiede beim Ablauf

Marketing-Kanäle haben ein rollierendes 30-tägiges Zeitfenster für Besucherinteraktionen, unabhängig davon, ob ein Kanal verwendet wurde oder nicht. Die Gültigkeit von Trackingcodes basiert auf dem Zeitpunkt, zu dem die Variable festgelegt wurde. Zum Beispiel:

1. Sie haben einen Besucherinteraktionsablauf von 30 Tagen und die Dimension „Trackingcode“ so konfiguriert, dass sie nach 30 Tagen abläuft.
2. Ein Benutzer gelangt über einen Trackingcode zu Ihrer Site. Er durchsucht die Site und verlässt sie anschließend.
3. Drei Wochen später kehrt er ohne Trackingcode oder Marketing-Kanal zurück und verlässt die Seite erneut.
4. Zwei weitere Wochen später (fünf Wochen nach dem ersten Besuch) kehrt er ohne Trackingcode oder Marketing-Kanal zurück und tätigt dann einen Kauf.

Der Benutzer tätigte letztendlich einen Kauf nach mehr 30 Tagen, war aber nie länger als 30 Tage inaktiv. In diesem Fall würden Sie Umsatz sehen, der dem Marketing-Kanal für Trackingcodes zugeordnet ist, jedoch nicht der Dimension „Trackingcode“ selbst.



