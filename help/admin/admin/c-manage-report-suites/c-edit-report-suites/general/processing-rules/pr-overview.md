---
description: Verarbeitungsregeln erleichtern die Datenerfassung und ermöglichen die Verwaltung der Inhalte, die an die Berichterstellung gesendet wurden.
subtopic: Processing rules
title: Übersicht über Verarbeitungsregeln
feature: Processing Rules
role: Admin
exl-id: 0244aba2-4345-463a-8528-d4dcd2f872ff
source-git-commit: 0bed2622f54bf2f46aa57dbfad7bd55a61d6c7d0
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 3%

---

# Übersicht über Verarbeitungsregeln

Mit Verarbeitungsregeln können Sie ändern, wie Ihre Daten erfasst werden, bevor sie in eine Report Suite geschrieben werden.

**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Report Suite auswählen > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Verarbeitungsregeln]**

>[!WARNING]
>
>Verarbeitungsregeln wirken sich direkt auf die Datenerfassung aus und können bei falscher Verwendung zu Datenverlust führen. Testen Sie Verarbeitungsregeln immer in einer Entwicklungs-Report Suite, bevor Sie sie in einer Produktions-Report Suite aktivieren, um Datenqualitätsprobleme zu beheben.

Zu den beiden primären Anwendungsfällen für Verarbeitungsregeln gehören:

* **Verwenden des Implementierungs-Workflows für Kontextdatenvariablen**: Anstatt Variablen in Ihrer Implementierung direkt festzulegen, können Sie [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md) verwenden, um Schlüssel/Wert-Paare festzulegen. Beispielsweise anstatt Folgendes festzulegen:

  ```js
  s.eVar1 = "Robert Munch";
  s.eVar2 = "Books";
  s.eVar3 = "Youth";
  ```

  Stattdessen können Sie Folgendes festlegen:

  ```js
  s.contextData['author'] = "Robert Munch";
  s.contextData['section'] = "Books";
  s.contextData['genre'] = "Youth";
  ```

  Anschließend können Sie die Kontextdatenvariablen den gewünschten Dimensionen und Metriken in der Analytics-Benutzeroberfläche zuordnen.

  Die Verwendung von Kontextdatenvariablen erleichtert die Kommunikation mit Entwicklern in Ihrer Organisation, um Analytics für eine Eigenschaft zu implementieren. Entwickler können einfach jedes Schlüssel-Wert-Paar einmal implementieren. Dann können Sie als Analytics-Admin sicherstellen, dass die Daten in die richtige Implementierungsvariable gelangen.

* **Daten bei der Erfassung ändern**: Dieser Anwendungsfall kann für eine breite Palette von Anwendungen eingesetzt werden, z. B. zur temporären Behebung der Datenqualität oder zur Schließung von Implementierungslücken. Weitere [ und spezifische Beispiele finden Sie ](pr-use-cases.md) „Anwendungsfälle für Verarbeitungsregeln“.

## Berechtigungen

Produktadministratoren haben standardmäßig Zugriff auf Verarbeitungsregeln. Sie können Benutzern ohne Administratorrechte Zugriff auf Verarbeitungsregeln gewähren, indem Sie sie in ein Produktprofil aufnehmen, das das Berechtigungselement **[!UICONTROL Verarbeitungsregeln]** enthält. Weitere [ finden Sie unter „Produktprofilberechtigungen für Report Suite](/help/admin/admin-console/permissions/report-suite-tools.md)Tools“.

## Überlegungen beim Erstellen oder Bearbeiten von Verarbeitungsregeln

Berücksichtigen Sie beim Erstellen oder Bearbeiten von Verarbeitungsregeln Folgendes:

* **Mögliche leere Werte**: Wenn Sie eine Regel erstellen, sollten Sie Fälle berücksichtigen, in denen der Wert zum Überschreiben leer ist. Wenn Sie beispielsweise eine Regel haben, die eVar1 mit eVar2 überschreibt und eVar2 leer ist, werden beide Variablen leer gelassen. Adobe empfiehlt, eine Bedingung hinzuzufügen, die nach einem Variablenwert sucht, bevor sie zum Überschreiben eines anderen Werts verwendet wird.
* **Sofort beim Speichern anwenden**: Die Verarbeitungsregeln gelten für die erfassten Daten in dem Moment, in dem Sie sie speichern. Sie gelten nicht rückwirkend für Daten, die bereits erhoben werden.
* **Verarbeitungsreihenfolge innerhalb von Regeln**: Wenn Sie mehrere Verarbeitungsregeln haben, ist die Reihenfolge ihrer Ausführung von Bedeutung. Stellen Sie sicher, dass eine Variable, die in mehreren Regeln verwendet wird, in der richtigen Reihenfolge ausgeführt wird. Wenn Sie eVar3 in Regel 1 überschreiben, ist dieser eVar3-Originalwert in keiner nachfolgenden Regel verfügbar.
* **Verarbeitungsreihenfolge innerhalb der Datenerfassungs-Pipeline**: Unter [Verarbeitungsreihenfolge für Daten in Adobe Analytics](/help/technotes/processing-order.md) erfahren Sie, wo in der gesamten Datenerfassungs-Pipeline Verarbeitungsregeln gelten.
* **Codierung**: Halten Sie sich in fast allen Fällen an die UTF-8-Codierung.
* **Groß-/**: Bei Zeichenfolgenvergleichen in Verarbeitungsregeln wird nicht zwischen Groß- und Kleinschreibung unterschieden. Die Zeichenfolgenwerte, mit denen Sie Werte überschreiben, verwenden dieselben Regeln wie beim direkten Ausfüllen der Variablen.
* **Einzelne Report Suite**: Beim Bearbeiten von Verarbeitungsregeln gelten diese nur für eine Report Suite. Wenn Sie im Report Suite Manager mehrere Report Suites auswählen, müssen Sie eine einzelne Report Suite auswählen. Nachdem Sie die gewünschten Verarbeitungsregeln erstellt oder bearbeitet haben, können [ diese Regeln in andere Report Suites kopieren](pr-copy.md).
* **Kein Datenausschluss**: Der Ausschluss von Daten ist kein beabsichtigtes Merkmal von Verarbeitungsregeln. Erwägen Sie die Verwendung von [`abort`](/help/implement/vars/config-vars/abort.md) auf Datenerfassungsebene oder verwenden Sie [VISTA-Regeln](/help/technotes/vista.md) nachdem Daten erfasst wurden.
* **Verfügbare Variablen**: In Verarbeitungsregeln sind nicht alle Dimensionen und Metriken verfügbar. Unter [Für Verarbeitungsregeln verfügbare Dimensionen und Metriken](pr-variables.md) finden Sie eine vollständige Liste der unterstützten Funktionen.
* **Anzahl der zulässigen Regeln**: Jede Report Suite kann bis zu 150 Regeln enthalten. Jede Regel kann bis zu 30 Bedingungen enthalten.

>[!MORELIKETHIS]
>
>![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Ordnen Sie Kontextdatenvariablen Props und eVars mit Verarbeitungsregeln zu](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/implementation/implementation-basics/map-contextdata-variables-into-props-and-evars-with-processing-rules){target="_blank"}
