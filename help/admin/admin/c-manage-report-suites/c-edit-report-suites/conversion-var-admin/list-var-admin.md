---
title: Listenvariablen
description: Erstellen und konfigurieren Sie Listenvariablen für die Verwendung in Berichten.
feature: Admin Tools
role: Admin
exl-id: 6d9a52d4-e7f3-4bbc-bad4-55c79f30b9f7
source-git-commit: 7c8ffe8f4ccf0577136e4d7ee96340224897d2a4
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 25%

---

# Listenvariablen

Erstellen und konfigurieren Sie Listenvariablen für die Verwendung in Berichten. Legen Sie die Werte für Trennzeichen, Ablauf, Zuordnung und Höchstwert fest. Erfassen von Daten für Listenvariablen mithilfe von [`list1` - `list3`](/help/implement/vars/page-vars/list.md).

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Konversion]** > **[!UICONTROL Listenvariablen]**

* **[!UICONTROL Name]**: Der Name der Listenvariablen. Dieser Name ist die Dimensionsbezeichnung in Analysis Workspace.

* **[!UICONTROL Status]**: Aktivieren oder deaktivieren Sie die Datenerfassung für diese Variable. Wenn eine Variable deaktiviert ist, werden keine Daten erfasst, selbst wenn Ihre Implementierung Daten an diese Variable sendet.

* **[!UICONTROL Werttrennzeichen]**: Das Zeichen, das zum Trennen von Werten in der Listenvariablen verwendet wird. Meistens handelt es sich dabei um Zeichen wie Kommas, Doppelpunkte, senkrechte Striche oder Ähnliches. Multi-Byte-Zeichen werden als Trennzeichen in Listenvariablen nicht unterstützt.

* **[!UICONTROL Läuft ab nach]**: Ähnlich wie beim Ablauf eines eVar bestimmt dieses Feld die Zeitspanne, die zwischen der Listenvariablen und dem Konversionsereignis für die Zuordnung auftreten kann.
   * **Auf Seitenansichts- oder Besuchsebene**: Erfolgsereignisse außerhalb der Seitenansicht oder des Besuchs werden nicht mit Werten in der Listenvariablen verknüpft.
   * **Auf Grundlage eines Zeitraums, z. B. Tag, Woche, Monat usw.**: Erfolgsereignisse, die über den angegebenen Zeitraum hinausgehen, werden nicht mit Werten in der Listenvariablen verknüpft. Hier kann auch eine benutzerspezifische Anzahl von Tagen festgelegt werden.
   * **Spezifische Konversionsereignisse**: Alle anderen Erfolgsereignisse, die nach dem angegebenen Ereignis ausgelöst werden, werden nicht mit Werten in der Listenvariablen verknüpft.
   * **Nie**: Zwischen der Listenvariablen und dem Erfolgsereignis kann ein beliebiger Zeitraum verstreichen.

* **[!UICONTROL Zuordnung]**: Diese Einstellung gibt vor, wie Erfolgsereignisse Gutschriften auf Werte aufteilen:
   * **Vollständig**: Erfolgsereignisse werden in allen Variablenwerten, die vor dem Ablauf der Variablen definiert sind, vollständig gutgeschrieben.
   * **Linear**: Konversionsereignisse werden in allen Variablenwerten, die vor dem Ablauf der Variablen definiert sind, aufgeteilt gutgeschrieben.
   * Variablenwerte werden niemals überschrieben, sondern die Gutschriften werden zu den Werten, in denen Erfolgsereignisse gutgeschrieben werden, hinzugefügt.

* **[!UICONTROL Beschreibung]**: Eine Beschreibung, wie Ihr Unternehmen die Listenvariable verwendet.

* **[!UICONTROL Höchstwerte]**: Gibt die Anzahl der für diese Listenvariable zulässigen aktiven Werte an. Wenn dieser Wert z. B. auf „3“ gesetzt ist, werden nur die letzten drei erfassten Werte gespeichert, und alle vorhergehenden Werte werden verworfen. Beachten Sie, dass jeder Wert denselben Zeitstempel hat und nicht garantiert wird, welcher Wert gespeichert wird, wenn für denselben Treffer mehrere Werte für dieselbe Listenvariable gesendet werden und Sie sich auf max -Werte beschränkt haben. Wenn ein Besucher mehr Werte als das erlaubte Maximum beibehält, werden die neuesten Werte verwendet. Es sind bis zu 250 Werte zulässig.

  Diese Einstellung ist nützlich, um die Attribution auf eine bestimmte Anzahl von Werten zu beschränken. Wenn beispielsweise eine list -Variable auf `"A,B,C"` auf der ersten Seite eines Besuchs und setzen Sie dann auf `"X,Y,Z"` auf der nächsten Seite wird die Attribution basierend auf ihrer Zuordnung auf diese sechs Werte verteilt. Wenn Sie die Attribution nur auf `"X,Y,Z"`können Sie den Maximalwert auf drei setzen.
