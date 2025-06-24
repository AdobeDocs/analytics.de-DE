---
description: Erfolgsereignisse sind Aktionen, die verfolgt werden können. Sie legen fest, was ein Erfolgsereignis ist. Wenn eine Besucherin oder ein Besucher beispielsweise einen Artikel kauft, kann das Kaufereignis als Erfolgsereignis betrachtet werden.
keywords: event
title: Übersicht über Erfolgsereignisse
feature: Metrics
role: Admin
exl-id: d52a691a-8124-4601-932f-d6d2d0a7842b
source-git-commit: 1281bdc569c9ebc5d8daa151b19dc21710633eab
workflow-type: tm+mt
source-wordcount: '938'
ht-degree: 54%

---

# Erfolgsereignisse

Erfolgsereignisse (auch Konversionsereignisse oder benutzerdefinierte Ereignisse genannt) sind Aktionen, die verfolgt werden können. Sie legen fest, was ein Erfolgsereignis ist. Wenn eine Besucherin oder ein Besucher beispielsweise einen Artikel kauft, kann das Kaufereignis als Erfolgsereignis betrachtet werden.

Eine Videoübersicht über Erfolgsereignisse finden Sie unter [Einführung in Konversionsereignisse](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/analysis-workspace/metrics/introduction-to-conversion-events) im Handbuch Analytics-Tutorials .

## Beispiele für Erfolgsereignisse

Es gibt, je nach Ihrem Websitetyp, viele Arten von Erfolgsereignissen. Zu diesen Arten zählen beispielsweise:

* **Einzelhandel**: Produktaufruf, Checkout, Kauf
* **Medien**: Abonnement, Wettbewerbsanmeldung, Seitenaufruf, Videoaufruf
* **Finanzen**: Applikationseinreichung, Anmeldung, Nutzung von Self-Service-Tools
* **Reisen**: Reservierung (Kauf), interne Kampagne (Clickthrough), Suche (Preisberechnung)
* **Telekommunikation**: Kauf, Leads, Nutzung von Self-Service-Tools
* **High Tech**: Download von White Papers, Gebotsanfragen, Formularausfüllung, Supportanfragen
* **Automotive**: Leadeinsendung, Preisanfrage, Download von Broschüren

Die Variable [s.events](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/events/event-serialization.html?lang=de) definiert ein Erfolgsereignis.

## Konfigurieren von Erfolgsereignissen

Sie können die auf Ihrer Site verwendeten Ereignisvariablen konfigurieren. Sie können bis zu 1.000 Erfolgsereignisse hinzufügen. Die Ereignisse 81-1.000 funktionieren nur, wenn Sie H22-Code oder höher verwenden.

So konfigurieren Sie Erfolgsereignisse:

1. Wählen Sie in Adobe Analytics **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** aus.
1. Wählen Sie die Report Suite aus, in der Sie Erfolgsereignisse konfigurieren möchten.
1. Wählen Sie **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Konversion]** > **[!UICONTROL Erfolgsereignisse]**.

   ![Ergebnis des Schritts](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/assets/success_event_page.png)

1. Geben [!UICONTROL **in der**] „Ereignis“ den Namen des Ereignisses an, das als Erfolgsereignis verwendet werden soll.

1. Aktivieren Sie in **[!UICONTROL Spalte &quot;]**&quot; das Kontrollkästchen neben dem Element, dessen Bearbeitung aktiviert werden soll, und geben Sie dann den gewünschten Namen an.

   Verwenden Sie aussagekräftige Namen für die auf Ihrer Website genutzten Erfolgsereignisse. Wenn beispielsweise Ereignis1 zur Nachverfolgung von Registrierungen verwendet wird, können Sie hier den Namen ändern, damit es in sämtlichen Konversionsberichten als „Registrierungen“ angezeigt wird.

1. Aktivieren Sie in **[!UICONTROL Spalte]** Typ“ das Kontrollkästchen neben dem Element, um die Dropdown-Liste zu aktivieren, und wählen Sie dann den gewünschten Typ aus.

   >[!IMPORTANT]
   >
   >Beachten Sie beim Ändern des Ereignistyps Folgendes:<ul><li>Sie können den Ereignistyp zwischen Zähler und numerischen Werten ändern, ohne den Zugriff auf zuvor erfasste Daten zu verlieren.</li><li>Beim Ändern von Ereignistypen in oder von einem Währungsereignis wird eine Meldung angezeigt, die besagt, dass historische Daten im Reporting nicht verfügbar sind. Die unterschiedlichen Ereignistypen verwenden separate Datentabellen, die nicht gleichzeitig genutzt werden können. Beim Wiederherstellen des bisherigen Ereignistyps kann ein Teil der historischen Daten unter Umständen wiederhergestellt werden. Daten, die nach der ersten Änderung erfasst wurden, sind jedoch nicht verfügbar.</li></ul>

   Der ausgewählte Typ bestimmt, ob das Ereignis ein Zähler- (Standard-), numerisches oder ein Währungsereignis ist. <p>Zählerereignisse werden verwendet, um ein Ereignis in der Zeit aufzuzeichnen.</p><p>Numerische Ereignisse werden für Berichte zu nicht währungsbezogenen Zahlen verwendet, z. B. die Anzahl der Coupons, die in einer Bestellung verwendet werden.</p> <p>Währungsereignisse zeichnen eine Dezimalzahl auf, z. B. Steuer oder Versand. Der in die Währungsereignisse einfließende Wert wird bei Eingang von der Seitenwährung in die Basiswährung der Report Suite konvertiert. Währungsereignisse werden zur Nachverfolgung von Steuern und Versandkosten verwendet. Weitere Informationen zur Verwendung von Währungsereignissen erhalten Sie bei Ihrem Adobe-Support-Mitarbeiter.<p>Bei numerischen Ereignissen und Währungsereignissen können die Metriken um einen anderen Wert als 1 erhöht werden.</p><p>Ereignisse im Standardtyp von „Data Sources“ müssen numerische oder Währungsereignisse sein.</p>

1. Aktivieren Sie in **[!UICONTROL Spalte]** Polarität“ das Kontrollkästchen und wählen Sie dann aus dem Dropdown-Menü aus, ob für diese Metrik ein Aufwärts-Trend gut oder schlecht ist.

   Auf diese Weise können Sie angeben, ob Adobe Analytics es als gut oder schlecht erachten sollte, wenn ein bestimmtes benutzerspezifisches Ereignis (eine Metrik) aufsteigt. Sie aktiviert Richtungsindikatoren (Pfeile) für verschiedene Metriken, um Kontext hinzuzufügen (z. B. wochenweise Vergleiche).  Beispiele: Wenn die Metrik „Übermittelte Bugs“ über mehrere Wochen ansteigt, soll Adobe Analytics dies als positiv oder negativ interpretieren? Ein Anstieg der E-Mail-Registrierungen ist wahrscheinlich positiv. Ein Anstieg bei den Übermittlungsfehlern für Formulare ist hingegen möglicherweise negativ.  In Analysis Workspace wird die Polarität angewendet auf: bedingte Formatierung der Freiformtabelle, Visualisierungen von Änderungen an der Zusammenfassung und das positive/negative Farbschema der Kartenvisualisierung.

1. Aktivieren Sie in der Spalte **[!UICONTROL Sichtbarkeit]** das Kontrollkästchen und wählen Sie dann aus dem Dropdown-Menü aus, ob Standardmetriken (integriert), benutzerdefinierte Ereignisse und integrierte Ereignisse im Menü, Metrikselektoren, Generator für berechnete Metriken und Segment Builder ausgeblendet werden sollen.

   Diese Einstellung wirkt sich nicht auf die Datenerfassung für diese Metrik oder das Ereignis aus, sondern nur auf die Sichtbarkeit in der Benutzeroberfläche,:

   Folgende Einstellungen sind verfügbar:

   | Einstellung | Sichtbar in | Nicht sichtbar in |
   |---------|----------|---------|
   | [!UICONTROL **Überall eingeblendet**] | <ul><li>Analysis Workspace</li><li>Segmentaufbau</li><li>Aufbau berechneter Metriken</li></ul> | nicht angegeben |
   | [!UICONTROL **Builder**] | <ul><li>Segmentaufbau</li><li>Aufbau berechneter Metriken</li><li>Analysis Workspace</li></ul> |
   | [!UICONTROL **Überall ausgeblendet**] | k. A. | <ul><li>Analysis Workspace</li><li>Segmentaufbau</li><li>Aufbau berechneter Metriken</li></ul> |

1. Aktivieren Sie in [!UICONTROL **Spalte**] Beschreibung“ das Kontrollkästchen und geben Sie dann eine Beschreibung ein.
1. Aktivieren Sie in [!UICONTROL **Spalte &quot;**] Ereignisaufzeichnung“ das Kontrollkästchen und wählen Sie dann aus dem Dropdown-Menü aus, ob das Ereignis immer aufgezeichnet werden soll.

   Die folgenden Optionen sind verfügbar:

   | Option | Funktion |
   |---------|----------|
   | [!UICONTROL **Einmal pro Besuch aufzeichnen**] | Verbindet das angegebene Ereignis mit der Sitzung des Besuchers. Nachfolgende Zählungen für ein bestimmtes Ereignis im selben Besuch werden ignoriert. Für diese Art der Ereignis-Serialisierung sind keine Implementierungsänderungen erforderlich. |
   | [!UICONTROL **Ereignis-ID verwenden**] | Verbindet das angegebene Ereignis mit einer benutzerdefinierten ID. Nachfolgende Zählungen für ein bestimmtes Ereignis mit derselben Ereignis-ID werden ignoriert. Für diese Art der Ereignis-Serialisierung ist eine benutzerdefinierte ID in Treffern erforderlich, um Werte zu deduplizieren. Siehe [Ereignis-ID-Serialisierung](/help/implement/vars/page-vars/events/event-serialization.md) im Benutzerhandbuch zu Implementierungen. |

1. Aktivieren Sie in [!UICONTROL **Spalte**] Teilnahme“ das Kontrollkästchen und legen Sie fest, ob die Teilnahme aktiviert oder deaktiviert werden soll. Wenn diese Option aktiviert ist, werden alle Dimensionselemente beim Besuch vollständig zugeordnet.

   >[!NOTE]
   >
   >Sie können den Beitrag für bis zu 100 benutzerspezifische Ereignisse aktivieren. Darüber hinaus können Sie im Generator für [berechnete Metriken](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/participation-metric.md) Beitragsmetriken erstellen.

1. Wählen Sie **[!UICONTROL Speichern]** aus.
