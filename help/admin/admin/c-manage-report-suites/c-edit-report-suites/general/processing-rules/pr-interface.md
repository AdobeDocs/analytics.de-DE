---
title: Schnittstelle für Verarbeitungsregeln
description: Navigieren Sie in der -Benutzeroberfläche, um Verarbeitungsregeln zu erstellen, zu bearbeiten oder zu löschen.
feature: Processing Rules
role: Admin
source-git-commit: c2adf6d2e328378332cc290ba2dfd75ee6587ef6
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# Schnittstelle für Verarbeitungsregeln

Die Benutzeroberfläche für Verarbeitungsregeln ermöglicht das Erstellen, Bearbeiten oder Löschen von Verarbeitungsregeln.

**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Report Suite auswählen > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Verarbeitungsregeln]**

>[!WARNING]
>
>Verarbeitungsregeln wirken sich direkt auf die Datenerfassung aus und können bei falscher Verwendung zu Datenverlust führen. Testen Sie Verarbeitungsregeln immer in einer Entwicklungs-Report Suite, bevor Sie sie in einer Produktions-Report Suite aktivieren, um Datenqualitätsprobleme zu beheben.

## übergreifende Struktur

Diese Schnittstelle umfasst zwei Hauptkomponenten:

* **[!UICONTROL Verarbeitungsreihenfolge]**: Regeln werden genau in der angegebenen Reihenfolge ausgeführt, beginnend mit Regel 1. Jeder Treffer durchläuft jede Regel; es gibt keine Early-Out-Bedingungen. Stellen Sie sicher, dass die Bedingungen jeder Verarbeitungsregel jeden Treffer berücksichtigen, der an die Report Suite gesendet wird.
* **[!UICONTROL Regelsätze]**: Die Definitionen der einzelnen Verarbeitungsregeln.

Pro Verarbeitungsregel können bis zu 150 Verarbeitungsregeln und bis zu 30 Bedingungen verwendet werden. Für die Anzahl der Aktionen pro Verarbeitungsregel gibt es keine vernünftige Begrenzung.

## Regelsatzstruktur

Jede Verarbeitungsregel enthält die folgenden Abschnitte:

* **Regeltitel**: Der Titel der Regel. Dies wirkt sich nicht auf die Verarbeitungsregellogik aus, ist aber nützlich, um zu verfolgen, was die Regel tut.
* **Bedingung** wird als Text &quot;[!UICONTROL Wenn eines/alle der folgenden zutrifft]&quot; angezeigt. Wenn Sie keine Bedingung einschließen, wird die Regel immer bei jedem Treffer ausgeführt.
* **Aktion**: Wenn keine Bedingung vorhanden ist, wird der Text als &quot;[!UICONTROL Immer ausführen] angezeigt. Wenn eine Bedingung vorhanden ist, wird der Text als &quot;[!UICONTROL Dann gehen Sie folgendermaßen vor]&quot; angezeigt. Wenn die obige Bedingung als `true` ausgewertet wird, wird möglicherweise jede in diesem Abschnitt aufgeführte Aktion ausgeführt. Zusätzlich zur Bedingung einer Regel können Sie _auch) Bedingungen_ einzelnen Aktionen anhängen. Die folgenden Aktionen sind verfügbar:
   * **[!UICONTROL Wert überschreiben von]**: Überschreibt die gewünschte Variable mit einer anderen Variablen, einem statischen Wert oder einem verketteten Wert.
   * **[!UICONTROL Wert löschen von]**: Löscht den gewünschten Variablenwert für diesen Treffer.
   * **[!UICONTROL Ereignis festlegen]**: Trigger des gewünschten Ereignisses. Normalerweise würden Sie Ereignisse auf den benutzerdefinierten Wert `1` festlegen. Das Festlegen von Ereignissen auf andere Werte als `1` oder sogar das Festlegen auf Werte, die in Kontextdatenvariablen festgelegt sind, ist ebenfalls zulässig.
* **Andernfalls Aktion**: Wenn eine Bedingung vorhanden ist, wird dieser Abschnitt als &quot;[!UICONTROL Andernfalls führen Sie die folgenden Schritte aus] angezeigt. Wenn die obige Bedingung als `false` ausgewertet wird, wird möglicherweise jede in diesem Abschnitt aufgeführte Aktion ausgeführt. In diesem Abschnitt werden dieselben Regelaktionen wie oben beschrieben ausgeführt, einschließlich der Möglichkeit zum Überschreiben von Werten, Löschen von Werten und Festlegen von Ereignissen.
* **Grund**: Notieren Sie, wer die Regel angefordert hat und wovon sie abhängt. Dies wirkt sich nicht auf die Verarbeitungsregellogik aus, ist aber nützlich, um zu verfolgen, warum die Regel vorhanden ist.

Unter [Für Verarbeitungsregeln verfügbare Dimensionen und Metriken](pr-variables.md) finden Sie eine umfassende Liste der Variablen, die Sie in dieser Benutzeroberfläche verwenden können.

* Jede Variable, die „Lesen“ ermöglicht, kann in einer Bedingung verwendet werden.
* Jede Variable, die „write“ ermöglicht, kann in einer Aktion verwendet werden.
