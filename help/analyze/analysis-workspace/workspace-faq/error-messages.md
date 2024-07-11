---
description: Liste der Fehlermeldungen in Adobe Analysis Workspace und der zugehörigen Komponenten
title: Allgemeine Fehlermeldungen in Analysis Workspace
feature: Workspace Basics
role: User, Admin
exl-id: e5c6f710-a205-48db-aeee-ee5b83c42795
source-git-commit: 6412fc0027c84df3b02ef2e7cbf35d24b4ee9319
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 100%

---

# Allgemeine Fehlermeldungen

Bei der Interaktion mit Analysis Workspace können Fehler auftreten, die auch die Leistung beeinflussen. Im Folgenden sind die häufigsten Fehlertypen, die Gründe dafür und Optimierungen aufgeführt, die vorgenommen werden können.

| Fehlermeldung | Grund | Optimierung |
| --- | --- | --- |
| [!UICONTROL Die Report Suite weist derzeit ein ungewöhnlich hohes Berichtvolumen auf. Bitte später erneut versuchen.] | Ihr Unternehmen versucht, zu viele Anfragen gleichzeitig für eine bestimmte Report Suite auszuführen. Zu diesem Fehler gehören API-Anfragen, geplante Projekte, terminierte Berichte, terminierte Warnhinweise und gleichzeitige Benutzer, die Reporting-Anfragen ausführen. | Verteilen Sie Ihre Anfragen und Zeitpläne für die Report Suite gleichmäßig über den Tag. |
| [!UICONTROL Die Report Suite überschreitet derzeit die Berichtskapazitäten. Bitte vereinfachen Sie die Anfrage oder versuchen Sie es später erneut.] | Ihr Unternehmen versucht, zu viele Anfragen gleichzeitig für eine bestimmte Report Suite auszuführen. Zu diesem Fehler gehören API-Anfragen, geplante Projekte, terminierte Berichte, terminierte Warnhinweise und gleichzeitige Benutzer, die Reporting-Anfragen ausführen. | Verteilen Sie Ihre Anfragen und Zeitpläne für die Report Suite gleichmäßig über den Tag. |
| [!UICONTROL Es ist ein Systemfehler aufgetreten. Melden Sie eine Anfrage an den Kundendienst unter Hilfe > senden Sie ein Support-Ticket und geben Sie Ihren Fehler-Code an.] | Adobe hat ein Problem, das behoben werden muss. | Senden Sie den Fehler-Code an die Kundenunterstützung. |
| [!UICONTROL Es ist ein unerwarteter Fehler aufgetreten. Versuchen Sie, Ihr Projekt erneut zu aktualisieren. Wenn das Problem weiterhin besteht, senden Sie bitte diese Fehler-ID zur weiteren Diagnose an die Adobe-Kundenunterstützung.] | Adobe hat ein Problem, das behoben werden muss. | Versuchen Sie, Ihr Projekt zu aktualisieren. Wenn das Problem weiterhin besteht, senden Sie den Fehler-Code an die Kundenunterstützung. |
| [!UICONTROL Fehler 500: Seite konnte nicht geladen werden] | Probleme mit Ihrem lokalen Netzwerk, wie z. B. die [Firewall-Einstellungen](https://experienceleague.adobe.com/docs/analytics/technotes/ip-addresses.html?lang=de) der Firma, tragen zu diesem Fehler bei. Darüber hinaus tritt bei Adobe möglicherweise ein Problem auf, das behoben werden muss. | Versuchen Sie nach einigen Minuten erneut sich anzumelden. Wenn das Problem weiterhin besteht, senden Sie den EIM-Instanz-ID-Code an die Kundenunterstützung. |
| [!UICONTROL Eines der Segmente oder die Suche in dieser Visualisierung enthält eine Textsuche, die zu viele Ergebnisse zurückgab.] | Ihre Segmentkriterien oder Berichtsfilter sind zu breit angelegt. | Schränken Sie die Suchtextkriterien ein und führen Sie die Anfrage erneut aus. |
| [!UICONTROL Diese Dimension unterstützt nicht-standardmäßige Zuordnungsmodelle derzeit nicht.] | Eine nicht-standardmäßige Zuordnung wird für die verwendete Dimension nicht unterstützt. | Ersetzen Sie die Dimension in Ihrer Tabelle durch eine Dimension, die mit [Attribution](/help/analyze/analysis-workspace/attribution/overview.md) kompatibel ist. |
| [!UICONTROL Ihre Anfrage schlug aufgrund zu vieler Spalten oder vorkonfigurierter Zeilen fehl.] | Ihre Tabelle enthält zu viele Freiformzellen (Zeile * Spalten). | Entfernen Sie Spalten oder Zeilen in der Tabelle oder erwägen Sie, die Tabelle in separate Anfragen zu unterteilen. |
