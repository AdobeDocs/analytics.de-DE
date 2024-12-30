---
title: Listenvariablen
description: Erstellen und konfigurieren Sie Listenvariablen für die Verwendung in Berichten.
feature: Admin Tools
role: Admin
exl-id: 6d9a52d4-e7f3-4bbc-bad4-55c79f30b9f7
source-git-commit: cf924b337772764b33d750787a0d09b3f11203be
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 25%

---

# Listenvariablen

Erstellen und konfigurieren Sie Listenvariablen für die Verwendung in Berichten. Legen Sie die Werte für Trennzeichen, Gültigkeit, Zuordnung und Maximum fest. Erfassen von Daten für Listenvariablen mithilfe von [`list1` - `list3`](/help/implement/vars/page-vars/list.md).

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Konversion]** > **[!UICONTROL Listenvariablen]**

* **[!UICONTROL Name]**: Der Name der Listenvariablen. Dieser Name ist die Dimensionsbeschriftung in Analysis Workspace.

* **[!UICONTROL Status]**: Aktivieren oder deaktivieren Sie das Erfassen von Daten für diese Variable. Wenn eine Variable deaktiviert ist, werden keine Daten erfasst, selbst wenn Ihre Implementierung Daten an diese Variable sendet.

* **[!UICONTROL Wertetrennzeichen]**: Das Zeichen, das zum Trennen von Werten innerhalb der Listenvariablen verwendet wird. Meistens handelt es sich dabei um Zeichen wie Kommas, Doppelpunkte, senkrechte Striche oder Ähnliches. Multi-Byte-Zeichen werden in Listenvariablen nicht als Trennzeichen unterstützt.

* **[!UICONTROL Läuft ab nach]**: Dieses Feld bestimmt ähnlich wie die eVar-Gültigkeit die Zeit, die zwischen der Listenvariablen und dem Konversionsereignis vergehen kann, damit sie miteinander in Beziehung gesetzt werden.
   * **Auf Seitenansichts- oder Besuchsebene**: Erfolgsereignisse, die über die Seitenansicht oder den Besuch hinausgehen, werden nicht mit Werten innerhalb der Listenvariablen verknüpft.
   * **Basierend auf einem Zeitraum, z. B. Tag, Woche, Monat usw**: Erfolgsereignisse, die über den angegebenen Zeitraum hinausgehen, werden nicht auf Werte innerhalb der Listenvariablen zurückgeführt. Hier kann auch eine benutzerspezifische Anzahl von Tagen festgelegt werden.
   * **Spezifische Konversionsereignisse**: Alle anderen Erfolgsereignisse, die nach dem angegebenen spezifischen Ereignis ausgelöst werden, werden nicht auf Werte innerhalb der Listenvariablen zurückgeführt.
   * **Nie**: Zwischen der Listenvariablen und dem Erfolgsereignis kann ein beliebiger Zeitraum verstreichen.

* **[!UICONTROL Zuordnung]**: Diese Einstellung gibt vor, wie Erfolgsereignisse Gutschriften auf Werte aufteilen:
   * **Vollständig**: Erfolgsereignisse werden in allen Variablenwerten, die vor dem Ablauf der Variablen definiert sind, vollständig gutgeschrieben.
   * **Linear**: Konversionsereignisse werden in allen Variablenwerten, die vor dem Ablauf der Variablen definiert sind, aufgeteilt gutgeschrieben.
   * Variablenwerte werden niemals überschrieben, sondern die Gutschriften werden zu den Werten, in denen Erfolgsereignisse gutgeschrieben werden, hinzugefügt.

* **[!UICONTROL Beschreibung]**: Eine Beschreibung, wie Ihr Unternehmen die Listenvariable verwendet.

* **[!UICONTROL Höchstwerte]**: Gibt die Anzahl der für diese Listenvariable zulässigen aktiven Werte an. Wenn dieser Wert z. B. auf „3“ gesetzt ist, werden nur die letzten drei erfassten Werte gespeichert, und alle vorhergehenden Werte werden verworfen. Beachten Sie, dass, wenn mehrere Werte für dieselbe Listenvariable für denselben Treffer gesendet werden und Sie die Verwendung von Maximalwerten eingeschränkt haben, jeder Wert denselben Zeitstempel hat und es nicht garantiert ist, welcher Wert gespeichert wird. Wenn ein Besucher mehr Werte beibehält als die maximal zulässige, werden die neuesten Werte verwendet. Es sind maximal 250 Werte zulässig.

  Diese Einstellung ist nützlich, um die Attribution auf eine bestimmte Anzahl von Werten zu beschränken. Wenn beispielsweise eine Listenvariable auf der ersten Seite eines Besuchs auf `"A,B,C"` und auf der nächsten Seite auf `"X,Y,Z"` festgelegt ist, wird die Attribution auf der Grundlage ihrer Zuordnung auf diese sechs Werte verteilt. Wenn Sie die Attribution auf `"X,Y,Z"` beschränken möchten, können Sie die Höchstwerte auf drei festlegen.
