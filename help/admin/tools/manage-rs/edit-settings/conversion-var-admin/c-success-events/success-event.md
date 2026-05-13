---
description: Erfolgsereignisse sind Aktionen, die verfolgt werden können. Sie legen fest, was ein Erfolgsereignis ist. Wenn eine Besucherin oder ein Besucher beispielsweise einen Artikel kauft, kann das Kaufereignis als Erfolgsereignis betrachtet werden.
keywords: event
title: Übersicht über Erfolgsereignisse
feature: Metrics
role: Admin
exl-id: d52a691a-8124-4601-932f-d6d2d0a7842b
TQID: https://experienceleague.adobe.com/wOWG6t9fsrfkd4FE-BNkwIrPW6DEGxBKDc2XItyRaoc
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2:
  - id: a544b409-2610-410d-a842-474ac1d0d54e
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
  - id: b3a8b8a0-1cc2-48a8-ac82-ffd9c66ccab4
  - id: dcae653e-62c6-4cc8-84e6-ee110b848296
  - id: ef60b66e-5984-4336-ba72-6d978b1b6f87
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 962
ht-degree: 25%

---

# Erfolgsereignisse

Erfolgsereignisse (auch Konversionsereignisse oder benutzerdefinierte Ereignisse genannt) sind Aktionen, die verfolgt werden können. Sie legen fest, was ein Erfolgsereignis ist. Wenn eine Besucherin oder ein Besucher beispielsweise einen Artikel kauft, kann das Kaufereignis als Erfolgsereignis betrachtet werden.

Eine Videoübersicht über Erfolgsereignisse finden Sie unter [Einführung in Konversionsereignisse](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/analysis-workspace/metrics/introduction-to-conversion-events) im Handbuch Analytics-Tutorials .

## Beispiele für Erfolgsereignisse

Je nach Website-Typ gibt es viele Arten von Erfolgsereignissen. Einige Beispiele:

* **Einzelhandel**: Produktansicht, Checkout, Kauf
* **Media**: Abonnement, Wettbewerbsregistrierung, Seitenansicht, Videoansicht
* **Finanzen**: Anwendungsübermittlung, Anmeldung, Verwendung von Self-Service-Tools
* **Reisen**: Buchung (Kauf), interne Kampagne (Clickthrough), Suche (Preisfindungs-Reiseroute)
* **Telekommunikation**: Kauf, Leads, Verwendung von Self-Service-Tools
* **High Tech**: Whitepaper-Download, RFP, Formularausfüllung, Support-Anfragen
* **Automotive**: Lead-Übermittlung, Angebot anfordern, Broschüre herunterladen

Die [s.events](/help/implement/vars/page-vars/events/event-serialization.md)-Variable definiert ein Erfolgsereignis.

## Konfigurieren von Erfolgsereignissen

Sie können die auf Ihrer Site verwendeten Ereignisvariablen konfigurieren. Sie können bis zu 1.000 Erfolgsereignisse hinzufügen. Die Ereignisse 81-1.000 funktionieren nur, wenn Sie H22-Code oder höher verwenden.

So konfigurieren Sie Erfolgsereignisse:

1. Wählen Sie in Adobe Analytics **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** aus.
1. Wählen Sie die Report Suite aus, in der Sie Erfolgsereignisse konfigurieren möchten.
1. Wählen Sie **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Konversion]** > **[!UICONTROL Erfolgsereignisse]**.

   ![Ergebnis des Schritts](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/c-success-events/assets/success_event_page.png)

1. Geben [!UICONTROL **in der**] „Ereignis“ den Namen des Ereignisses an, das als Erfolgsereignis verwendet werden soll.

1. Aktivieren Sie in **[!UICONTROL Spalte &quot;]**&quot; das Kontrollkästchen neben dem Element, dessen Bearbeitung aktiviert werden soll, und geben Sie dann den gewünschten Namen an.

   Geben Sie Erfolgsereignissen, die auf Ihrer Site verwendet werden, aussagekräftige Namen. Wenn beispielsweise event1 zum Nachverfolgen von Registrierungen verwendet wird, ändern Sie den Namen hier, sodass event1 in allen Konversionsberichten als Metrik „Registrierungen“ dargestellt wird.

1. Aktivieren Sie in **[!UICONTROL Spalte]** Typ“ das Kontrollkästchen neben dem Element, um die Dropdown-Liste zu aktivieren, und wählen Sie dann den gewünschten Typ aus.

   >[!IMPORTANT]
   >
   >Beachten Sie beim Ändern des Ereignistyps Folgendes:<ul><li>Sie können den Ereignistyp zwischen Zähler und numerischen Werten ändern, ohne den Zugriff auf zuvor erfasste Daten zu verlieren.</li><li>Beim Ändern von Ereignistypen in oder von einem Währungsereignis wird eine Meldung angezeigt, die besagt, dass historische Daten im Reporting nicht verfügbar sind. Verschiedene Ereignistypen verwenden separate Datentabellen und können nicht gleichzeitig verwendet werden. Einige historische Daten können wiederhergestellt werden, wenn der Benutzer den Ereignistyp zurücksetzt. Daten, die nach der ersten Änderung erfasst wurden, sind jedoch nicht verfügbar.</li></ul>

   Der ausgewählte Typ bestimmt, ob das Ereignis ein Zähler- (Standard-), numerisches oder ein Währungsereignis ist. <p>Zählerereignisse werden verwendet, um ein Ereignis in der Zeit aufzuzeichnen.</p><p>Numerische Ereignisse werden für Berichte zu nicht währungsbezogenen Zahlen verwendet, z. B. die Anzahl der Coupons, die in einer Bestellung verwendet werden.</p> <p>Währungsereignisse zeichnen eine Dezimalzahl auf, z. B. Steuer oder Versand. Der an Währungsereignisse übergebene Wert wird bei Erhalt von der Seitenwährung in die Basiswährung der Report Suite umgerechnet. Währungsereignisse werden zur Verfolgung von Steuer- und Versandkosten verwendet. Weitere Informationen zur Verwendung von Währungsereignissen erhalten Sie von einem Adobe-Support-Mitarbeiter.<p>Mit numerischen und Währungsereignissen können Sie Metriken um mehr als ein Inkrement erhöhen.</p><p>Ereignisse, die im Standardtyp von Datenquellen verwendet werden, müssen numerische oder Währungsereignisse sein.</p>

1. Aktivieren Sie in **[!UICONTROL Spalte]** Polarität“ das Kontrollkästchen und wählen Sie dann aus dem Dropdown-Menü aus, ob für diese Metrik ein Aufwärts-Trend gut oder schlecht ist.

   Auf diese Weise können Sie angeben, ob Adobe Analytics es als gut oder schlecht erachten sollte, wenn ein bestimmtes benutzerspezifisches Ereignis (eine Metrik) aufsteigt. Sie aktiviert Richtungsindikatoren (Pfeile) für verschiedene Metriken, um Kontext hinzuzufügen (z. B. wochenweise Vergleiche).  Beispiele: Wenn „Bugs Submitted“ von Woche zu Woche ansteigt, sollte Adobe Analytics das als gut oder schlecht ansehen? Ein Anstieg der E-Mail-Registrierungen ist wahrscheinlich gut. Ein Anstieg bei den Übermittlungsfehlern für Formulare ist hingegen möglicherweise negativ.  In Analysis Workspace wird die Polarität auf Folgendes angewendet: bedingte Formatierung von Freiformtabellen, Visualisierungen von Zusammenfassungsänderungen und das Farbschema der Positiv-/Negativ-Kartenvisualisierung.

1. Aktivieren Sie in der Spalte **[!UICONTROL Sichtbarkeit]** das Kontrollkästchen und wählen Sie dann aus dem Dropdown-Menü aus, ob Standardmetriken (integriert), benutzerdefinierte Ereignisse und integrierte Ereignisse im Menü, Metrikselektoren, Generator für berechnete Metriken und Segment Builder ausgeblendet werden sollen.

   Diese Einstellung wirkt sich nicht auf die Datenerfassung für diese Metrik oder das Ereignis aus, sondern nur auf die Sichtbarkeit in der Benutzeroberfläche,:

   Folgende Einstellungen sind verfügbar:

   | Einstellung | Sichtbar in | Nicht sichtbar in |
   |---------|----------|---------|
   | [!UICONTROL **Überall eingeblendet**] | <ul><li>Analysis Workspace</li><li>Segment Builder</li><li>Aufbau berechneter Metriken</li></ul> | nicht angegeben |
   | [!UICONTROL **Builder**] | <ul><li>Segment Builder</li><li>Generator für berechnete Metriken</li><li>Analysis Workspace</li></ul> |  |
   | [!UICONTROL **Überall ausgeblendet**] | nicht angegeben | <ul><li>Analysis Workspace</li><li>Segment Builder</li><li>Aufbau berechneter Metriken</li></ul> |

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
   >Sie können den Beitrag für bis zu 100 benutzerspezifische Ereignisse aktivieren. Darüber hinaus können Sie im Generator für [berechnete Metriken](/help/components/calculated-metrics/workflow/c-build-metrics/participation-metric.md) Beitragsmetriken erstellen.

1. Wählen Sie **[!UICONTROL Speichern]** aus.
