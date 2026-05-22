---
title: Unterschiede bei Verarbeitung und Architektur von Analyseplattformen
description: Erfahren Sie, wie einige Daten auf unterschiedlichen Plattformen wie Adobe Analytics und Google Analytics auf verschiedene Weise erfasst und angezeigt werden.
feature: Third-party Integration
exl-id: 3e457915-3c2d-49f7-9b77-df18c04d49cd
TQID: 'https://experienceleague.adobe.com/pL36oKany2sKuJrEn4-oIja3O91PZ47YQGoNvhdt6y8'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
subfeature_v2:
  - id: a60fda7a-bb0b-4eb6-b9fe-77558cbee1fa
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 503
ht-degree: 96%

---

# Unterschiede bei Verarbeitung und Architektur von Analyseplattformen

Obwohl Adobe Analytics und Google Analytics beide Analysetools sind, unterscheidet sich die Art und Weise, wie Daten erfasst und verarbeitet werden, zwischen den beiden Plattformen stark. Verwenden Sie diese Seite, um einige der wichtigsten Unterschiede bei der Erfassung bestimmter Dimensionen und Metriken zu verstehen und herauszufinden, warum sie in ähnlichen Berichten möglicherweise unterschiedliche Zahlen anzeigen.

## [!UICONTROL Absprungrate]

Die [!UICONTROL Absprungrate] ist ein häufig verwendeter KPI, mit dem in den meisten Analyse-Tools die Effektivität und Relevanz der Landingpages gemessen werden kann. Dies wird normalerweise definiert als Besuche, die auf die Website gelangen, aber keinen Klick auf eine andere Seite beinhalten.

* In Adobe Analytics wird die [!UICONTROL Absprungrate] anhand der Formel **Absprünge dividiert durch Einstiege** berechnet.
* In Google Analytics wird die [!UICONTROL Absprungrate] anhand der Formel **Einseitige Sitzungen dividiert durch Sitzungen** berechnet.

Wenn auf beiden Plattformen bei demselben Besuch oder derselben Sitzung mehrere Treffer gesendet werden, wird dies nicht als Absprung gewertet. In Adobe Analytics sind benutzerspezifische Links verfügbar und relativ häufig, wodurch verhindert werden kann, dass ein Besuch als Absprung gezählt wird. Google Analytics sendet normalerweise nicht mehr als eine Datenanfrage auf derselben Seite.

Um eine bessere Parität zwischen den Berichts-Tools zu erreichen, verwenden Sie in Adobe Analytics anstelle von [!UICONTROL Absprüngen] die Metrik [!UICONTROL Einzelseitenbesuche] als Teil einer berechneten Metrik. Die Metrik [!UICONTROL Einzelseitenbesuche] enthält die Gesamtanzahl der Besuche, bei denen nur ein Seitenaufruf stattfand oder die keinen Klick auf eine andere Seite beinhalteten.

Weitere Informationen finden Sie im Abschnitt zur Metrik [Absprungrate](/help/components/metrics/bounce-rate.md) im Benutzerhandbuch zu Komponenten.

## [!UICONTROL Besuche und Sitzungen]

[!UICONTROL Besuche] (in Google Analytics als Sitzungen bezeichnet) sind jeweils eine Gruppe von Seitenaufrufen, die ein und derselbe Anwender in kurzer Zeit tätigt. [!UICONTROL Besuche] auf beiden Plattformen laufen in der Regel nach 30 Minuten Inaktivität ab. Beide Plattformen ermöglichen die Anpassung der Bedingungen für das Ablaufen eines [!UICONTROL Besuchs]. Es gibt mehrere Szenarien, die Unterschiede auf den verschiedenen Plattformen verursachen können.

* **Tagesende:** Alle Sitzungen in Google Analytics laufen an einem bestimmten Tag nach :59 23 Uhr ab. Wenn der Anwender nach 00:00 Uhr noch auf Ihrer Site aktiv ist, wird eine neue Sitzung erstellt. Adobe Analytics führt Besuche am Folgetag im Rahmen desselben Besuchs fort.
* **Verschiedene Kampagnen:** In Google Analytics wird eine neue Sitzung gestartet, wenn sich die Kampagnenquelle eines Anwenders ändert. Wenn in Adobe Analytics ein neuer Wert für den [!UICONTROL Trackingcode] auftaucht, wird er als Teil desselben Besuchs betrachtet.
* **Manuelle Sitzungsüberschreibungen:** In Google Analytics wird eine neue Sitzung gestartet, wenn Sie `sessionControl` verwenden, um eine Sitzung manuell zu starten oder zu beenden. [!UICONTROL In Adobe Analytics können Besuche nicht manuell beendet werden.]
* **Ausreißerbesuchserkennung in Adobe Analytics:** In Adobe Analytics beginnt automatisch ein neuer [!UICONTROL Besuch], wenn ein Anwender 12 Stunden kontinuierlicher Aktivität, 2.500 Treffer oder 100 Treffer innerhalb von 100 Sekunden erreicht. Jedes dieser Erkennungskriterien wird normalerweise durch Bot-Aktivitäten ausgelöst.

Weitere Informationen finden Sie im Abschnitt zur Metrik [Besuche](/help/components/metrics/visits.md) im Benutzerhandbuch zu Komponenten.
