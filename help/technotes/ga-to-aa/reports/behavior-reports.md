---
title: Verhaltensberichte in Adobe Analytics
description: Erfahren Sie, wie Sie Verhaltensberichte in Adobe Analytics erstellen.
feature: Third-party Integration
exl-id: ea441afa-e595-4ffa-b446-d67e87f8a7c9
source-git-commit: cbfe932eecf2e89d72b1aa373d723de4cf0af073
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 95%

---

# Verhaltensberichte

Verhaltensberichte zeigen Informationen zur Interaktion der Anwender mit Ihrer Site an.

Auf dieser Seite wird davon ausgegangen, dass der Anwender über grundlegende Kenntnisse in der Verwendung von Analysis Workspace verfügt. Siehe [Basisbericht in Analysis Workspace für GA-Anwender erstellen](create-report.md), wenn Sie mit dem Tool in Adobe Analytics noch nicht vertraut sind.

## Verhaltensfluss

Der Verhaltensflussbericht kann mithilfe der Flussvisualisierung nachgebildet werden.

1. Klicken Sie auf das Symbol „Visualisierungen“ auf der linken Seite und ziehen Sie die Flussvisualisierung auf den Arbeitsbereich über der Freiformtabelle.
2. Suchen Sie die Dimension **Seite** und klicken Sie dann auf das Pfeilsymbol, um die Seitenwerte anzuzeigen. Dimensionselemente sind gelb markiert.
3. Suchen Sie den gewünschten Seitenwert, mit dem Sie beginnen möchten, und ziehen Sie ihn in den mittigen Bereich namens „Dimension oder Element“.
4. Dieser Flussbericht ist interaktiv. Klicken Sie auf einen der Werte, um den Fluss auf nachfolgende oder vorherige Seiten zu erweitern. Verwenden Sie das Kontextmenü, um Spalten zu erweitern oder zu reduzieren. Im selben Flussbericht können auch verschiedene Dimensionen verwendet werden.

![Flussbericht](/help/technotes/ga-to-aa/assets/flow.png)

## Site-Content – Alle Seiten

Der Seitenbericht zeigt die Leistung einzelner Seiten auf Ihrer Site an.

1. Suchen Sie im Menü „Komponenten“ die Dimension **Seiten** und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

Als Alternative bietet Adobe mehrere vordefinierte Arbeitsbereiche, die als Vorlagen bezeichnet werden. Die Vorlage für Content-Verbrauch (Web) bietet einen ähnlichen Wert wie der Bericht „Alle Seiten“.

1. Klicken Sie auf *[!UICONTROL Projekt] > [!UICONTROL Neu]*, um ein modales Fenster mit Projektoptionen zu öffnen.
2. Klicken Sie auf die Vorlage für Content-Verbrauch (Web) und dann auf „Erstellen“.

## Site-Content – Content-Drilldown

Mit dem Content-Drilldown-Bericht können Sie sich den Seiten-Traffic nach URL-Struktur ansehen. Für die Verwendung in Analysis Workspace ist eine zusätzliche Implementierung erforderlich. Adobe empfiehlt, mit einem Implementierungsberater zusammenzuarbeiten, um sicherzustellen, dass diese Daten korrekt erfasst werden.

## Site-Content – Landingpages

Der Bericht zu Zielseiten zeigt die führenden Landingpages Ihrer Site an. Landingpages sind in Analysis Workspace als Dimension **Entrypage** verfügbar.

1. Suchen Sie im Menü „Komponenten“ die Dimension **Entrypage** und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

Adobe empfiehlt die Verwendung der Metrik **Besuche** für diese Dimension.

## Site-Content – Exit-Pages

Der Bericht zu Exit-Pages zeigt die Seiten an, von denen aus Besucher die Site am häufigsten verlassen haben. Er ist in Analysis Workspace als „Exitpage“ verfügbar.

1. Suchen Sie im Menü „Komponenten“ die Dimension **Exitpage** und ziehen Sie sie in den großen Freiformtabellenbereich mit der Bezeichnung „Dimension hier ablegen“.
2. Ziehen Sie die gewünschten Metriken in den Arbeitsbereich neben die automatisch erstellte Metrik **Vorfälle**. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im [Handbuch zur Metrikübersetzung](common-metrics.md).

Adobe empfiehlt die Verwendung der Metrik **Besuche** für diese Dimension.

## Berichte zur Site-Geschwindigkeit

Berichte zur Site-Geschwindigkeit zeigen, wie schnell Seiten geladen werden, und enthalten Möglichkeiten, die Seitenladezeit zu reduzieren.

Diese Funktion erfordert auf beiden Plattformen eine zusätzliche Implementierung. Adobe empfiehlt, mit einem Implementierungsberater zusammenzuarbeiten, um sicherzustellen, dass diese Daten korrekt für Analysis Workspace konfiguriert sind. Das Plugin [getPageLoadTime](/help/implement/vars/plugins/getpageloadtime.md) wird normalerweise einer eVar zugewiesen, um Leistungsdaten in Adobe Analytics abzurufen.

## Berichte zur Site-Suche

Berichte zur Site-Suche bieten einen Einblick, wie Besucher die internen Suchfunktionen Ihrer Site nutzen.

Diese Funktion erfordert auf beiden Plattformen eine zusätzliche Implementierung. Adobe empfiehlt, mit einem Implementierungsberater zusammenzuarbeiten, um sicherzustellen, dass diese Daten korrekt für Analysis Workspace konfiguriert sind. In der Regel wird ein interner Suchbegriff aus einem Abfragezeichenfolgen-Parameter abgerufen und für Berichte in eine eVar eingefügt.

## Ereignisberichte

Ereignisse weisen einige große strukturelle Unterschiede zwischen Google und Adobe Analytics auf. Beide erfordern zusätzliche Implementierungsänderungen, damit sie auf der jeweiligen Plattform ordnungsgemäß funktionieren.

* In Google Analytics werden Ereignisse in Ihrer Implementierung als Text definiert. Ereignisse verfügen über Kategorien, Aktionen und Bezeichnungen.
* In Adobe Analytics werden Ereignisse zuerst in der Admin Console eingerichtet, wo ihnen eine ID zugewiesen wird. Diese ID wird im Implementierungs-Code verwendet. Beispiel:
   1. Sie können „event1“ in der Admin Console als „Registrierungen“ festlegen.
   2. In Ihrer Implementierung würden Sie „event1“ in die Ereignisvariable auf der Seite zur Registrierungsbestätigung aufnehmen. Jedes Mal, wenn die Seite zur Registrierungsbestätigung angezeigt wird, steigt „event1“ um 1.
   3. In Analysis Workspace erscheint „Registrierungen“ als Metrik zur Verwendung in einem beliebigen Bericht.

Da für diese Funktion Implementierungsänderungen erforderlich sind, empfiehlt Adobe, mit einem Implementierungsberater zusammenzuarbeiten, um sicherzustellen, dass die Daten für Analysis Workspace korrekt konfiguriert sind.

## Publisher-Berichte

Ähnlich wie Google eine Verbindung mit Google Ad Manager erfordert, bietet Adobe ein dediziertes Produkt zur Bereitstellung von insight namens Adobe Advertising an. Wenn Ihr Unternehmen an der Verwendung dieses Produkts interessiert ist, wenden Sie sich an Ihr Adobe Account Team.
