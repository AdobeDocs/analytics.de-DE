---
title: Echtzeitberichte in Adobe Analytics
description: Erfahren Sie, wie Sie Echtzeitberichte in Adobe Analytics abrufen, die auf Anwender ausgerichtet sind, die mit Google Analytics besser vertraut sind.
feature: Third-party Integration
exl-id: 0ca27992-fff8-4bb4-8582-31fd401b23f6
TQID: https://experienceleague.adobe.com/wmxzxGKSbeiMfdV09krfIQlmG1doEnPxOGp-Tusgjyg
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2:
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 1037
ht-degree: 93%

---

# Echtzeitberichte

Echtzeitberichte zeigen, was gerade auf Ihrer Site geschieht. Diese Berichtstypen sind besonders wertvoll, um die sofortigen Ergebnisse von Updates Ihrer Site zu sehen. Ein Unternehmen, das am Black Friday einen Verkauf durchführt, kann beispielsweise den Traffic auf bestimmten Seiten messen und festlegen, welche Verkäufe je nach Leistung in diesem Moment vorrangig behandelt werden sollen.

![Echtzeitbericht](/help/technotes/ga-to-aa/assets/realtime.png)

Echtzeitberichte sind eine der wenigen Funktionen, die noch nicht in Analysis Workspace eingeführt wurden. Diese Daten können mithilfe von Berichten abgerufen werden. Sie erfordern eine einfache Konfiguration, um mit der Datenerfassung zu beginnen.

So rufen Sie die Seite zur Konfiguration von Echtzeitberichten auf (Administratorberechtigungen erforderlich):

1. Klicken Sie in der **Navigationsleiste oben in Adobe Analytics auf** Workspace.
1. Wählen **[!UICONTROL Berichte]** über die linke Navigationsleiste aus.
1. Wählen Sie **[!UICONTROL Interaktion]** ![Chevron](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ChevronRight_18_N.svg) **[!UICONTROL Echtzeit]** aus. Sie können auch ![Suchen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Search_18_N.svg) nach Echtzeit suchen.
1. Wenn für die Report Suite die Echtzeit-Funktion noch nicht aktiviert ist, wird eine Meldung mit einem Link zur Konfiguration der Report Suite angezeigt.

Adobe ermöglicht bis zu drei Echtzeitberichte, die Daten gleichzeitig erfassen. Jede muss konfiguriert werden, bevor sie mit der Datenerfassung in Echtzeit beginnen.

![Konfiguration von Echtzeitberichten](/help/technotes/ga-to-aa/assets/realtime_config.png)

## Echtzeitstandorte

Die Echtzeitstandorte zeigen Ihnen, wo sich Besucher während des Besuchs Ihrer Site im aktuellen Moment befinden. So konfigurieren Sie einen Ihrer drei Echtzeitberichte, um Standortdaten anzuzeigen:

1. Klicken Sie neben dem Titel des Echtzeitberichts auf [!UICONTROL Konfigurieren].
2. Unter einem der Slots für Echtzeitberichte:
   * Benennen Sie Ihren Echtzeitbericht, z. B. mit „Standorte“.
   * Als Metrik wird in der Regel „Instanzen“ verwendet. „Benutzer“/„Unique Visitors“ stehen derzeit in Echtzeitberichten nicht zur Verfügung.
   * Als primäre Dimension wird in der Regel „GeoSegmentation Land“ verwendet. „GeoSegmentation Region“, „GeoSegmentation U.S. DMA“ und „GeoSegmentation Stadt“ sind ebenfalls verfügbar.
   * Verwenden Sie als die beiden sekundären Dimensionen die gewünschten zusätzlichen Daten, die Sie für diesen Traffic anzeigen möchten. Sekundäre Dimensionen müssen nicht standortspezifisch sein.
3. Klicken Sie auf [!UICONTROL Speichern und Bericht anzeigen].

## Echtzeit-Traffic-Quellen

Echtzeit-Traffic-Quellen geben an, woher Besucher während des Besuchs Ihrer Site im aktuellen Moment kamen. So konfigurieren Sie einen Ihrer drei Echtzeitberichte, um Traffic-Quellen anzuzeigen:

1. Klicken Sie neben dem Titel des Echtzeitberichts auf „Konfigurieren“.
2. Unter einem der Slots für Echtzeitberichte:
   * Benennen Sie Ihren Echtzeitbericht, z. B. mit „Traffic-Quellen“.
   * Als Metrik wird in der Regel „Instanzen“ verwendet. „Benutzer“/„Unique Visitors“ stehen derzeit in Echtzeitberichten nicht zur Verfügung.
   * Als primäre Dimension wird in der Regel „Referrer-Domäne“ verwendet. „Suchmaschine“ und „Suchbegriff“ sind ebenfalls verfügbar.
   * Verwenden Sie als die beiden sekundären Dimensionen die gewünschten zusätzlichen Daten, die Sie für diesen Traffic anzeigen möchten. Sekundäre Dimensionen müssen nicht Traffic-Quellen-spezifisch sein.
3. Klicken Sie auf [!UICONTROL Speichern und Bericht anzeigen].

## Echtzeitinhalt

Echtzeitinhalt zeigt Ihnen an, welche Seiten Ihre Besucher derzeit anzeigen. So konfigurieren Sie einen Ihrer drei Echtzeitberichte, um Inhaltsdaten anzuzeigen:

1. Klicken Sie neben dem Titel des Echtzeitberichts auf [!UICONTROL Konfigurieren].
2. Unter einem der Slots für Echtzeitberichte:
   * Benennen Sie Ihren Echtzeitbericht, z. B. mit „Inhalt“.
   * Als Metrik wird in der Regel „Instanzen“ verwendet. „Benutzer“/„Unique Visitors“ stehen derzeit in Echtzeitberichten nicht zur Verfügung.
   * Als primäre Dimension wird in der Regel „Seite“ verwendet. „Sitebereich“ und „Server“ sind ebenfalls verfügbar, wenn Ihre Implementierung diese Variablen definiert.
   * Verwenden Sie als die beiden sekundären Dimensionen die gewünschten zusätzlichen Daten, die Sie für diesen Traffic anzeigen möchten. Sekundäre Dimensionen müssen nicht inhaltsspezifisch sein.
3. Klicken Sie auf [!UICONTROL Speichern und Bericht anzeigen].

## Echtzeitereignisse

Echtzeitereignisse zeigen Ihnen, welche Ereignisse derzeit auf Ihrer Site am häufigsten auftreten. In Google Analytics erfasst ein Ereignis, wie oft eine bestimmte Aktion (im Allgemeinen eine Aktion, die nicht mit einer Seitenansicht in Zusammenhang steht) aufgetreten ist. GA-Ereignisse werden mit einer Kategorie, einer Bezeichnung und einer Aktion gesendet. In Adobe Analytics sind benutzerspezifische Ereignisse Metriken, denen in der Admin Console benutzerfreundliche Namen zugewiesen werden und die neben jeder Dimension analysiert werden können. Wenn Sie in Adobe Analytics nach einer Dimension suchen, die Google Analytics-Ereignissen ähnlich ist, sollten Sie die Dimension „Benutzerspezifischer Link“ anwenden. Diese Dimension wird häufig als Sammelbegriff für Daten verwendet, die nicht mit Seitenansichten in Zusammenhang stehen (zusätzlich zu Exit-Links für Ausstiehe- und Downloadlinks für Downloads).

>[!NOTE]
>
>Bei Verwendung benutzerdefinierter Ereignisse in Echtzeitberichten muss der Dimensionswert im selben Treffer wie das benutzerspezifische Ereignis definiert werden. Wenn Sie beispielsweise ein benutzerdefiniertes Ereignis „Registrierungen“ für die Dimension „Referrer-Domäne“ anzeigen, werden ohne zusätzliche Implementierung keine Daten zurückgegeben. Da die verweisende Domain nur beim ersten Treffer angezeigt wird und ein benutzerspezifisches Ereignis normalerweise später während des Besuchs auftritt, können die Daten nicht in Echtzeitberichten verknüpft werden. Diese Daten stehen in Analysis Workspace mit einer standardmäßigen Verarbeitungslatenz von 30 bis 90 Minuten zur Verfügung.

## Echtzeitkonversionen

Echtzeitkonversionen stellen Daten zwischen Plattformen unterschiedlich dar. Zielvorhaben in Google Analytics sind mit Metriken und Erfolgsereignissen in Adobe Analytics vergleichbar. Sie können die meisten Metriken in Adobe Analytics (sowohl benutzerspezifische Metriken wie Erfolgsereignisse als auch Standardmetriken wie den Umsatz) in Echtzeitberichten verwenden. Ähnlich wie Google Analytics können Sie auch Dimensionen wie Produktname, Trackingcode und Kampagnenleistung in Echtzeitberichten anwenden.

1. Klicken Sie neben dem Titel des Echtzeitberichts auf [!UICONTROL Konfigurieren].
2. Unter einem der Slots für Echtzeitberichte:
   * Benennen Sie Ihren Echtzeitbericht, z. B. mit „Konversionen“.
   * Als Metrik wird in der Regel „Instanzen“ verwendet. „Benutzer“/„Unique Visitors“ stehen derzeit in Echtzeitberichten nicht zur Verfügung.
   * Als primäre Dimension wird in der Regel „Trackingcode“ verwendet. Die Dimension „Produkte“ ist ebenfalls verfügbar, wenn Ihre Implementierung sie verwendet.
   * Verwenden Sie als die beiden sekundären Dimensionen die gewünschten zusätzlichen Daten, die Sie für diesen Traffic anzeigen möchten. Sekundäre Dimensionen müssen nicht konversionsspezifisch sein.
3. Klicken Sie auf [!UICONTROL Speichern und Bericht anzeigen].

>[!NOTE]
>
>Wenn Sie Ereignisse außerhalb von Instanzen verwenden, z. B. Bestellungen, stellen Sie sicher, dass Ihre Implementierung die Dimension und das Ereignis im selben Treffer definiert. Wenn Dimensionen und Ereignisse nicht im selben Treffer ausgelöst werden, stehen diese Daten in Analysis Workspace mit einer standardmäßigen Verarbeitungslatenz (in der Regel 30 bis 90 Minuten) zur Verfügung.
