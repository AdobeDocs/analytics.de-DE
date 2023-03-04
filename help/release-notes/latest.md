---
title: Neueste Analytics-Versionshinweise
description: Hier finden Sie die aktuellen Versionshinweise zu Adobe Analytics.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: c53f886d5329e2a3b5023f9396c3aa2360a86901
workflow-type: tm+mt
source-wordcount: '1111'
ht-degree: 91%

---

# Aktuelle Adobe Analytics-Versionshinweise (Februar 2023)

**Letzte Aktualisierung**: 27. Februar 2023

Die Versionen von Adobe Analytics basieren auf einem [kontinuierlichen Bereitstellungsmodell](releases.md), das eine besser skalierbare, schrittweise Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue oder aktualisierte Funktionen in Adobe Analytics

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Aktualisierte Benutzeroberfläche für Datenschutzkennzeichnungen** | Die aktualisierte Benutzeroberfläche optimiert den Prozess der Erstellung, Verwaltung und Bearbeitung von Datenschutzkennzeichnungen für Report Suite-Komponenten. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/data-labels/gdpr-setup-reportsuite.html?lang=de) | Nicht angegeben | 8. Februar 2023 |
| **Ausblenden von Vergleichsdatumsbereichen in mobilen Scorecards** | Mit mobilen Scorecards können Sie zum Anzeigen oder Ausblenden von Vergleichsdaten die Einstellung **[!UICONTROL Vergleichsdaten einschließen]** umschalten. | Nicht angegeben | 8. Februar 2023 |
| **Kalenderaktualisierungen in Workspace** | <ul><li>Ankerbedienfielddaten: Sie können die Datumsbereichskomponenten im Verhältnis zum Bedienfeldkalender festlegen. [Weitere Informationen](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md#relative-panel-dates)</li><li>Aktualisierungen des Kalenderstils: Die Kalenderstile in der gesamten Benutzeroberfläche wurden aktualisiert, um einen konsistenteren und benutzerfreundlicheren Workflow zu bieten.</li><li>Aktualisierungen der Kalenderformel: Wenn Sie relative Daten verwenden, spiegeln alle Kalenderformeln den Beginn des Bedienfelddatumsbereichs wider. [Weitere Informationen](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md#formula-relative-dates)</li></ul> | Nicht angegeben | 8. Februar 2023 |
| **Aktualisierungen des Datumsbereichs des Bedienfelds** | In Workspace wurden die folgenden Verbesserungen hinzugefügt:<ul><li>Ab der Februarversion basieren die Komponenten- und Datenvorschauen auf dem Datumsbereich des Bedienfelds und nicht auf den letzten 90 Tagen. </li><li>Alle angezeigten Dimensionselemente sind basierend auf dem Datumsbereich des Bedienfelds verfügbar.</li><li>Alle Datumsvorschauen im Segment und Generatoren für berechnete Metriken basieren auf dem Datumsbereich des Bedienfelds (sofern nicht von den Komponenten-Managern darauf zugegriffen wird, die über kein verknüpftes Bedienfeld verfügen, basieren sie weiterhin auf den letzten 90 Tagen).</li><li>Bei jeder Datenvorschau werden Daten oder Komponenten basierend auf dem Datumsbereich des Bedienfelds angezeigt.</li></ul> | Nicht angegeben | 8. Februar 2023 |
| **Zeilen-/Spaltenfilter für Adobe Analytics-Source-Connector-Streaming** | Der Analytics-Source-Connector in Adobe Experience Platform ermöglicht jetzt das Filtern von Analytics-Daten, mit denen Profile in [Echtzeit-Kundenprofil](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=de) gefüllt werden. Die Filterung auf Zeilenebene hilft, die Anzahl der mit Profilen verknüpften Ereignisse zu reduzieren. Die Filterung auf Spaltenebene hilft, die Vielfalt der Ereignisse selbst zu reduzieren, und ermöglicht es Ihnen so, die Nutzung von Profilberechtigungen zu optimieren. Diese Filterung gilt nur für Daten, die an das Echtzeit-Kundenprofil und an [Identity Service](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=de) gesendet werden. **Die Filterung wirkt sich nicht auf die Daten aus, die zur Verwendung in Anwendungen wie Customer Journey Analytics an Data Lake gesendet werden**. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=de#filtering-for-profile) | Nicht angegeben | Geplant für den 29. März 2023 |

{style=&quot;table-layout:auto&quot;}

## Fehlerbehebungen in Adobe Analytics 

AN-302282; AN-303127; AN-303541; AN-303550; AN-305282; AN-306504; AN-307351; AN-307496; AN-307530; AN-307947; AN-308497; AN-308610; AN-308777; AN-308994; AN-309143; AN-309404; AN-309414; AN-309445; AN-309575; AN-309630; AN-309658; AN-309690; AN-309742; AN-309861; AN-309967; AN-309973; AN-310059; AN-310132; AN-310168; AN-310238; AN-310241; AN-310301; AN-310318; AN-310324; AN-310335; AN-310338; AN-310460; AN-310500; AN-310684; AN-310690; AN-311010; AN-311022; AN-311043; AN-311125; AN-311250; AN-311370; AN-311458;

## Wichtige Hinweise für Adobe Analytics-Administratoren

| Hinweis | Hinzugefügt  oder aktualisiert am | Beschreibung |
| ----------- | ---------- | ---------- |
| **Aktualisierung der Gerätesuche aufgrund von Google-Client-Hinweisen** | 27. Februar 2023 | Die Verwendung von Client-Hinweisen, die für den 16. Februar 2023 geplant sind, wurde verschoben, um die Qualität der Gerätesuche mithilfe von Hinweisen besser sicherzustellen. Wir haben die erste Phase der Veröffentlichung zur Unterstützung von Client Hints am 27. Februar 2023 und die zweite und letzte Phase am Donnerstag, 2. März 2023 abgeschlossen. [Weitere Informationen](/help/technotes/client-hints.md) |
| **Verfügbarkeit von Analytics Source Connector** | 15. Februar 2023 | Am 28. Februar 2023 wurde der Analytics Source Connector im neuen Adobe Experience Platform-Rechenzentrum in Kanada zur Verfügung gestellt. |
| **Automatische Migration zur Klassifizierungssatzarchitektur** | 8. Februar 2023 | In den nächsten Monaten plant Adobe, alle Klassifizierungen organisationsübergreifend auf die neueste Klassifizierungsarchitektur zu migrieren. Die letzten Kundinnen und Kunden werden schätzungsweise im Mai 2023 migriert. Es ist keine Kundenaktion erforderlich, und es wird keine Ausfallzeit erwartet. Diese neue Architektur bietet viele Vorteile, darunter:<ul><li>deutlich verkürzte Verarbeitungszeit (72 Stunden → 24 Stunden)</li><li>die Möglichkeit, die Benutzeroberfläche für [Klassifizierungssätze](/help/components/classifications/sets/overview.md) zu verwenden</li><li>die Option, Klassifizierungsdaten in Adobe Experience Platform künftig über den [Adobe Analytics-Source-Connector für Klassifizierungsdaten](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/classifications.html?lang=de) zu verwenden</li></ul>Beachten Sie die folgenden Änderungen, die sich möglicherweise auf den Workflow Ihrer Organisation auswirken können:<ul><li>Bei Verwendung des Browser- oder FTP-Imports ist „[!UICONTROL Bei Konflikt überschreiben]“ immer aktiviert.</li><li>Bei Verwendung des Browser- oder FTP-Imports wird die Option zum sofortigen Export nach dem Import nicht mehr unterstützt.</li><li>Der `GetDimensions`-Endpunkt der Analytics 2.0-API gibt jetzt Zeichenfolgenkennungen für Klassifizierungen anstelle numerischer Kennungen zurück. Numerische Kennungen können zwar weiterhin verwendet werden, Adobe empfiehlt jedoch, nach Möglichkeit die neuen Zeichenfolgenkennungen zu verwenden. Numerische Kennungen können mithilfe des Abfragezeichenfolgen-Parameters `?expansion=hidden` abgerufen werden.</li></ul>Wenden Sie sich an die Kundenunterstützung von Adobe, wenn Sie einen spezifischeren Migrationsplan für Ihre Organisation wünschen oder Fragen/Bedenken zu dieser Migration haben. [Weitere Informationen](/help/components/classifications/sets/overview.md) |

{style=&quot;table-layout:auto&quot;}

## Mitteilungen über das Ende der Nutzungsdauer (EOL)

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Ende der Nutzungsdauer einiger Planungsfunktionen für Reports &amp; Analytics und Report Builder** | 9. Februar 2023 | Die folgenden Planungsfunktionen wurden am 31. Januar 2023 eingestellt:<ul><li>die Option „Nach x Vorkommen beenden“ für stündliche Aufgaben in Report Builder </li><li>die Möglichkeit, in Reports and Analytics neue Berichte zu planen und Datenextraktionen herunterzuladen</li></ul><p>**Hinweis**: Ursprünglich hatten wir diese Funktionen im April 2022 beendet, aber wir haben die Änderung rückgängig gemacht. Wir haben außerdem eine Benachrichtigung gesendet, dass diese Funktionen vorübergehend wiederhergestellt wurden und am 31. Januar 2023 erneut beendet werden. |
| **EOL für die [!UICONTROL Veröffentlichungslisten]-Funktion** | 29. September 2022 | Im Rahmen des EOL von Reports &amp; Analytics ist geplant, dass die Veröffentlichungslisten im **Dezember 2023** das Ende ihrer Lebensdauer erreichen. Sie können keine neuen Veröffentlichungslisten erstellen oder auf vorhandene zugreifen, um Projekte in Analysis Workspace zu senden oder zu planen. |
| **EOL für Data Workbench** | 14. September 2022 | Adobe beabsichtigt, Data Workbench ab **31. Dezember 2023** einzustellen. Weitere Informationen finden Sie in der [Mitteilung zum Ende der Nutzungsdauer von Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html?lang=de). Wenden Sie sich bei Fragen an Ihr Adobe Account Team. |
| **EOL für [!DNL Reports & Analytics]** | 4. Januar 2022 | Adobe beabsichtigt, [!DNL Reports & Analytics] und die zugehörigen Berichte und Funktionen zum **31. Dezember 2023** einzustellen. Die Berichte, Visualisierungen und zugrunde liegenden Technologien, die [!DNL Reports & Analytics] unterstützen, entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Funktionen von [!DNL Reports & Analytics] sind in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen von [!DNL Reports & Analytics] nach Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In [dieser Mitteilung](https://spark.adobe.com/page/6WnF8JK6IRDhf/) wird der Ablauf der Produktlebensdauer erläutert. |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen (Version 2.23.0) finden Sie in den [Versionshinweisen zu AppMeasurement für JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=de).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2022](/help/release-notes/2022.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
