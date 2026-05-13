---
title: Listenvariablen
description: Erstellen und konfigurieren Sie Listenvariablen für die Verwendung in Berichten.
feature: Admin Tools
role: Admin
exl-id: 6d9a52d4-e7f3-4bbc-bad4-55c79f30b9f7
TQID: https://experienceleague.adobe.com/22yU-AEfp08-BPNwwC6LrJO7iX7n44mZzP9799l6fmQ
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
subfeature_v2:
  - id: b3a8b8a0-1cc2-48a8-ac82-ffd9c66ccab4
  - id: ef60b66e-5984-4336-ba72-6d978b1b6f87
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 490
ht-degree: 4%

---

# Listenvariablen

Erstellen und konfigurieren Sie Listenvariablen für die Verwendung in Berichten. Legen Sie die Werte für Trennzeichen, Gültigkeit, Zuordnung und Maximum fest. Erfassen von Daten für Listenvariablen mithilfe von [`list1` - `list3`](/help/implement/vars/page-vars/list.md).

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Konversion]** > **[!UICONTROL Listenvariablen]**

* **[!UICONTROL Name]**: Der Name der Listenvariablen. Dieser Name ist die Dimensionsbeschriftung in Analysis Workspace.

* **[!UICONTROL Status]**: Aktivieren oder deaktivieren Sie das Erfassen von Daten für diese Variable. Wenn eine Variable deaktiviert ist, werden keine Daten erfasst, selbst wenn Ihre Implementierung Daten an diese Variable sendet.

* **[!UICONTROL Wertetrennzeichen]**: Das Zeichen, das zum Trennen von Werten innerhalb der Listenvariablen verwendet wird. Meistens handelt es sich dabei um Zeichen wie Kommas, Doppelpunkte, senkrechte Striche oder Ähnliches. Multi-Byte-Zeichen werden in Listenvariablen nicht als Trennzeichen unterstützt.

* **[!UICONTROL Läuft ab nach]**: Dieses Feld bestimmt ähnlich wie die eVar-Gültigkeit die Zeit, die zwischen der Listenvariablen und dem Konversionsereignis vergehen kann, damit sie miteinander in Beziehung gesetzt werden.
   * **Auf Seitenansichts- oder Besuchsebene**: Erfolgsereignisse, die über die Seitenansicht oder den Besuch hinausgehen, werden nicht mit Werten innerhalb der Listenvariablen verknüpft.
   * **Basierend auf einem Zeitraum, z. B. Tag, Woche, Monat usw**: Erfolgsereignisse, die über den angegebenen Zeitraum hinausgehen, werden nicht auf Werte innerhalb der Listenvariablen zurückgeführt. Es kann auch eine benutzerdefinierte Anzahl von Tagen definiert werden.
   * **Spezifische Konversionsereignisse**: Alle anderen Erfolgsereignisse, die nach dem angegebenen spezifischen Ereignis ausgelöst werden, werden nicht auf Werte innerhalb der Listenvariablen zurückgeführt.
   * **Nie**: Zwischen der Listenvariablen und dem Erfolgsereignis kann ein beliebiger Zeitraum verstreichen.

* **[!UICONTROL Zuordnung]**: Diese Einstellung bestimmt, wie Erfolgsereignisse die Gutschrift auf verschiedene Werte aufteilen:
   * **Full**: Alle Variablenwerte, die vor dem Ablauf der Variablen definiert wurden, werden für Erfolgsereignisse vollständig angerechnet.
   * **Linear**: Alle Variablenwerte, die vor dem Ablauf der Variablen definiert wurden, erhalten eine geteilte Gutschrift für Konversionsereignisse.
   * Variablenwerte werden nie überschrieben, sondern stattdessen zu den Werten hinzugefügt, die bei Erfolgsereignissen angerechnet werden.

* **[!UICONTROL Beschreibung]**: Eine Beschreibung, wie Ihr Unternehmen die Listenvariable verwendet.

* **[!UICONTROL Max Values]**: Gibt die Anzahl der aktiven Werte an, die für diese Listenvariable zulässig sind. Wenn beispielsweise auf 3 festgelegt, werden nur die letzten drei erfassten Werte gespeichert und alle vorherigen erfassten Werte werden verworfen. Beachten Sie, dass, wenn mehrere Werte für dieselbe Listenvariable für denselben Treffer gesendet werden und Sie die Verwendung von Maximalwerten eingeschränkt haben, jeder Wert denselben Zeitstempel hat und es nicht garantiert ist, welcher Wert gespeichert wird. Wenn ein Besucher mehr Werte beibehält als die maximal zulässige, werden die neuesten Werte verwendet. Es sind maximal 250 Werte zulässig.

  Diese Einstellung ist nützlich, um die Attribution auf eine bestimmte Anzahl von Werten zu beschränken. Wenn beispielsweise eine Listenvariable auf der ersten Seite eines Besuchs auf `"A,B,C"` und auf der nächsten Seite auf `"X,Y,Z"` festgelegt ist, wird die Attribution auf der Grundlage ihrer Zuordnung auf diese sechs Werte verteilt. Wenn Sie die Attribution auf `"X,Y,Z"` beschränken möchten, können Sie die Höchstwerte auf drei festlegen.
