---
title: Besuche
description: Erfahren Sie mehr über die Metrik Besuche in Analytics. Hier erfahren Sie, wie er berechnet wird, welche Verhaltensweisen ihn beeinflussen, wie er seine Definition ändert und vieles mehr.
feature: Metrics
exl-id: 4f78f2b5-f958-44fe-876a-83f07980beec
source-git-commit: 5f80d1f56fb8a95780ff2daf18644ac5ffb548d6
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 80%

---

# Besuche

Die [Metrik](overview.md) „Besuche“ gibt die Anzahl der Sitzungen für alle Besucherinnen und Besucher Ihrer Site an.

## Berechnung dieser Metrik

Ein Besuch ist immer mit einem Zeitraum verknüpft. So wissen Sie, ob es sich um einen neuen Besuch handelt, wenn dieselbe Person zu Ihrer Site zurückkehrt. Ein Besuch beginnt, wenn der Benutzer zum ersten Mal auf Ihrer Site ankommt. Ein Besuch endet, wenn eines der folgenden Kriterien erfüllt ist:

* **30 Minuten Inaktivität**: Fast alle Sitzungen enden auf diese Weise. Wenn mehr als 30 Minuten zwischen Treffern vergangen sind, beginnt ein neuer Besuch.
* **12 Stunden Aktivität**: Wenn ein Benutzer über einen Zeitraum von 12 Stunden Bildanforderungen ohne 30-minütige Pausen auslöst, beginnt automatisch ein neuer Besuch.
* **2500 Treffer**: Wenn ein Benutzer zahlreiche Treffer generiert, ohne eine neue Sitzung zu starten, wird nach 2500 Bildanforderungen ein neuer Besuch gezählt.
* **100 Treffer in 100 Sekunden**: Wenn ein Besuch mehr als 100 Treffer aufweist, die in den ersten 100 Sekunden des Besuchs auftreten, endet der Besuch automatisch. Dieses Verhalten deutet typischerweise auf Bot-Aktivität hin. Diese Einschränkung wird durchgesetzt, um die Berichtsleistung zu verbessern.

Ein Besuch fällt aufgrund der oben genannten Kriterien nicht unbedingt mit einer Browser-Sitzung zusammen. Einer der häufigsten Unterschiede besteht darin, dass ein Besucher zu Ihrer Site navigiert, den Tab mehr als 30 Minuten geöffnet lässt und dann das Surfen fortsetzt. Diese Aktion ist technisch gesehen Teil derselben Browser-Sitzung. Adobe betrachtet diese Aktion jedoch als zwei separate Besuche.

## Verhalten, das sich auf Besuche auswirkt

Wenn ein Besucher eine dieser Aktionen ausführt, beginnt ein neuer Besuch:

* Löscht die Cookies während der Sitzung und surft weiter auf Ihrer Site
* Lässt Ihre Site länger als 30 Minuten in einem Tab geöffnet und fährt dann mit dem Surfen fort.
* Öffnet einen anderen Browser und navigiert auf demselben Computer zu Ihrer Site.
* Derselbe Benutzer surft auf verschiedenen Geräten auf Ihrer Site.

Wenn ein Besucher eine dieser Aktionen ausführt, wird ein neuer Besuch **erst** gestartet, wenn zwischen aufeinanderfolgenden Treffern mehr als 30 Minuten liegen:

* Schließt seinen Browser und navigiert dann erneut zu Ihrer Site.
* Startet den Computer neu, öffnet denselben Browser und navigiert erneut zu Ihrer Site.
* Wechselt zu einem anderen Netzwerk, z. B. trennt die Verbindung der Docking-Station mit einem kabelgebundenen Netzwerk und wechselt zu einem drahtlosen Netzwerk.
* Besucht Ihre Site in mehreren Tabs. Wenn ein Besucher zwischen Tabs hin und her wechselt, zählt jeder Treffer als Teil desselben Besuchs.

## Ändern der Definition eines Besuchs

Sie können die Definition eines Besuchs auf eine andere Zeit als 30 Minuten ändern.

* Bei [Virtual Report Suites](../vrs/vrs-about.md) können Sie die maximale Wartezeit für Besuche (Zeit zwischen Treffern, die den Start eines neuen Besuchs verursacht) über die [!UICONTROL Besuchs-Zeitüberschreitung] ändern. Sie können das Besuchszeitlimit auf einen angemessenen Wert ändern.
* Wenden Sie sich bei Standard-Report Suites an die Kundenunterstützung, um anzufordern, dass die maximale Wartezeit für einen Besuch (Zeit zwischen Treffern, die den Start eines neuen Besuchs verursacht) für eine bestimmte Report Suite verkürzt wird. Die maximale Wartezeit für Besuche bei standardmäßigen Report Suites darf 30 Minuten nicht überschreiten. Daher können Sie sie nur verkürzen.

## Besuche, die eine Datumsgrenze überschreiten

Es wird für jeden betroffenen Zeitraum ein Besuch gezählt. Wenn beispielsweise ein Besucher Ihre Site am Montag um 23:00 :45 navigiert und dann am Dienstag um 12:00 Uhr seine letzte Bildanforderung sendet, wird :10 Besuch sowohl Montag als auch Dienstag zugeordnet. Die Gesamtbesuchsmetrik wird jedoch dedupliziert und zeigt einen einzelnen Besuch für den Datumsbereich des Projekts an.

## Besuche innerhalb einer Dimension im Vergleich zur Gesamtanzahl der Besuche

Besuche im Kontext einer Dimension (z. B. [Marketing-Kanal](../dimensions/marketing-channel.md)) zeigen die Anzahl der Besuche, die zu einem bestimmten Zeitpunkt ein bestimmtes Dimensionselement enthielten. Häufig gibt es mehrere Dimensionselemente bei verschiedenen Treffern im selben Besuch. Der Versuch, Besuche zu summieren, die über Dimensionselemente berichten, ist in der Regel nicht sinnvoll.

## Besuche aller Besucher in Data Warehouse

Die Metrik „Besuche – Alle Besucher“ steht zusätzlich zur Metrik „Besuche“ in Data Warehouse zur Verfügung. Die Metrik „Besuche – Alle Besucher“ ist mit der Metrik „Besuche“ in anderen Analytics-Tools vergleichbar. Die Metrik „Besuche“ in Data Warehouse schließt Besucher ohne beständige Cookies aus. Adobe empfiehlt die Verwendung von „Besuche – Alle Besucher“ in Data Warehouse-Anfragen, bei denen Besuche als Metrik gewünscht werden.
