---
title: Trackingcode
description: Der Name des Trackingcodes oder der Kampagne.
feature: Dimensions
exl-id: e4f70552-6946-4974-a9e2-928faf563ecd
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 66%

---

# Trackingcode

Die Dimension „Trackingcode[&#x200B; listet &#x200B;](overview.md) Namen von Trackingcodes auf Ihrer Site auf. Sie können Links mit verschiedenen Abfragezeichenfolgenparameterwerten an verschiedenen Stellen im Internet platzieren. Diese Dimension hilft Ihnen zu verstehen, welche Links am erfolgreichsten den Traffic zu Ihrer Site geleitet haben.

Das Anhängen von Trackingcode-Abfragezeichenfolgen ist in E-Mails, Anzeigen, Social-Media-Posts und anderen Marketing-Maßnahmen Ihres Unternehmens häufig.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [`v0` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mit der [`campaign`](/help/implement/vars/page-vars/campaign.md)-Variable.

## Dimensionselemente

Zu den Dimensionselementen gehören die Namen der Trackingcodes auf Ihrer Site. Ihr Unternehmen legt fest, welche spezifischen Dimensionselemente Sie verwenden möchten. Siehe [Kampagnen-Tracking](/help/implement/use-cases/campaign-tracking.md) für weitere Informationen.

## Dimension „Trackingcode“ mit Dimension „Marketing-Kanäle“ vergleichen, die Trackingcodes erfasst

Einige Benutzer, die Verarbeitungsregeln für Marketing-Kanäle einrichten, konfigurieren eine Regel, die alle in der Dimension „Trackingcode“ verwendeten Werte berücksichtigt. Obwohl es sich um eine hervorragende Praxis handelt, unterscheiden sie sich aufgrund der inhärenten Verarbeitungs- und Architekturunterschiede. In der folgenden Liste wird erläutert, warum diese beiden Methoden, obwohl sie auf einen Blick ähnlich sind, das Attributionsverhalten ändern können.

### Vorherige Kanäle in Verarbeitungsregeln

Verarbeitungsregeln für Marketing-Kanäle weiter oben in der Liste können verhindern, dass Treffer Ihrem Marketing-Kanal für Trackingcodes zugeordnet werden. Beispiel:

1. Sie haben als erste Regel „Soziale Netzwerke“ und als zweite „Trackingcodes“ eingerichtet.
2. Ein Benutzer stellt einen Link zu Ihrer Site mit einem Trackingcode auf einer Social-Media-Website ein, und mehrere seiner Freunde klicken auf diesen Link zu Ihrer Site.

Da „Soziale Netzwerke“ die erste Verarbeitungsregel für Marketing-Kanäle ist, werden diese Benutzer dem Marketing-Kanal „Soziale Netzwerke“ und nicht Ihrem Marketing-Kanal für Trackingcodes zugeordnet.

### Andere Marketing-Kanäle können die Attribution durch Letztkontakt übernehmen

Wenn Sie mit einer Standard-Trackingcode-Dimension arbeiten, müssen Sie sich keine Sorgen darüber machen, dass andere Teile Ihrer Site die Attribution stehlen. Bei Marketing-Kanälen kann ein Benutzer jedoch eine andere Regel anwenden und eine andere Attribution vornehmen. Beispiel:

1. Sie haben „Trackingcodes“ als ersten Kanal und „Direkt“ als zweiten.
2. Ein Benutzer gelangt zunächst über einen Trackingcode zu Ihrer Site, verlässt dann jedoch die Site.
3. Am nächsten Tag geben sie Ihre URL in ihre Adressleiste ein und tätigen dann einen Kauf.

In diesem Beispiel erhält der Marketing-Kanal für Trackingcodes für diesen Kauf keine Letztkontakt-Gutschrift. Stattdessen würde er dem Marketing-Kanal „Direkt“ gutgeschrieben.


### Gültigkeitsunterschiede

Marketing-Kanäle haben einen rollierenden Ablauf der Besucherinteraktion um 30 Tage, unabhängig davon, ob ein Kanal berührt wurde oder nicht. Die Gültigkeit von Trackingcodes basiert auf dem Zeitpunkt, zu dem die Variable festgelegt wurde. Beispiel:

1. Sie haben einen Besucherinteraktionsablauf von 30 Tagen und die Dimension „Trackingcode“ so konfiguriert, dass sie nach 30 Tagen abläuft.
2. Ein Benutzer gelangt über einen Trackingcode zu Ihrer Site. Er durchsucht die Site und verlässt sie anschließend.
3. Drei Wochen später kehrt er ohne Trackingcode oder Marketing-Kanal zurück und verlässt die Seite erneut.
4. Zwei weitere Wochen später (fünf Wochen nach dem ersten Besuch) kehrt er ohne Trackingcode oder Marketing-Kanal zurück und tätigt dann einen Kauf.

Der Benutzer tätigte letztendlich einen Kauf nach mehr 30 Tagen, war aber nie länger als 30 Tage inaktiv. In diesem Fall wird der Umsatz angezeigt, der dem Marketing-Kanal Trackingcodes zugeordnet ist, nicht jedoch der Trackingcode-Dimension selbst.



