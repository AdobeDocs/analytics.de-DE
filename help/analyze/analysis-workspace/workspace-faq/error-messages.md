---
description: Erfahren Sie mehr über Fehler und Fehlerbehebung in Analysis Workspace.
title: Fehler bei der Fehlerbehebung in Analysis Workspace
feature: Workspace Basics
role: User, Admin
exl-id: e5c6f710-a205-48db-aeee-ee5b83c42795
source-git-commit: 0146d0798571d8589a74fb6d3fbbd574af224631
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 97%

---

# Fehler und Fehlerbehebung

Bei der Interaktion mit Analysis Workspace können Fehler auftreten, die ggf. die Funktionalität und Leistung beeinflussen. Im Folgenden sind die häufigsten Fehlertypen, die Gründe dafür und Optimierungen aufgeführt, die vorgenommen werden können.

## Fehlermeldungen

Häufige Fehlermeldungen, die bei der Verwendung von Analysis Workspace möglicherweise angezeigt werden:

| Fehlermeldung | Fehlerursache | Optimierung |
| --- | --- | --- |
| [!UICONTROL Die Datenansicht verzeichnet derzeit ein ungewöhnlich hohes Reporting-Aufkommen. Bitte später erneut versuchen.] | Ihr Unternehmen versucht, zu viele Anfragen gleichzeitig für eine bestimmte Datenansicht auszuführen. Dieser Fehler kann etwa ausgelöst werden durch API-Anfragen, geplante Projekte, terminierte Berichte, terminierte Warnhinweise und die gleichzeitige Ausführung von Reporting-Anfragen durch mehrere Benutzende. | Verteilen Sie die Anfragen und Zeitpläne für die Datenansicht gleichmäßiger über den Tag.<p>Admins können den [Berichterstellungsaktivitäts-Manager verwenden, um Anfragen zu identifizieren und abzubrechen](/help/admin/admin/reporting-activity-manager/reporting-activity-overview.md), die Berichtskapazität verbrauchen.</p> |
| [!UICONTROL Dieser Bericht ist zu komplex. Beachten Sie die Best Practices für die Erstellung von Analysis Workspace-Berichten.] | Ihre Reporting-Anfrage ist zu groß und kann nicht ausgeführt werden. Gründe für diesen Fehler sind Zeitüberschreitungen aufgrund der Komplexität der Anfrage. | Vereinfachen Sie die Anfrage. Verkürzen Sie beispielsweise den Datumsbereich, vereinfachen Sie die Segmentkriterien oder entfernen Sie einige Spalten oder Zeilen aus der Tabelle. Sie können die Tabelle ggf. auch in separate Anfragen aufteilen. |
| [!UICONTROL Die Datenansicht überschreitet derzeit die Berichtskapazitäten. Bitte vereinfachen Sie die Anfrage oder versuchen Sie es später erneut.] | Ihr Unternehmen versucht, zu viele Anfragen gleichzeitig für eine bestimmte Datenansicht auszuführen. Dieser Fehler kann etwa ausgelöst werden durch API-Anfragen, geplante Projekte und die gleichzeitige Ausführung von Reporting-Anfragen durch mehrere Benutzende. | Verteilen Sie die Anfragen und Zeitpläne für die Datenansicht gleichmäßiger über den Tag. |
| [!UICONTROL Es ist ein Systemfehler aufgetreten. Melden Sie eine Anfrage an die Kundenunterstützung unter **[!UICONTROL Hilfe > senden Sie ein Support-Ticket]** und geben Sie Ihren Fehler-Code an.] | Adobe hat ein Problem, das behoben werden muss. | Senden Sie den Fehler-Code an die Kundenunterstützung. |
| [!UICONTROL Fehler 500: Seite konnte nicht geladen werden] | Probleme mit Ihrem lokalen Netzwerk, wie z. B. die [Firewall-Einstellungen](/help/technotes/ip-addresses.md) der Firma, tragen zu diesem Fehler bei. Darüber hinaus tritt bei Adobe möglicherweise ein Problem auf, das behoben werden muss. | Versuchen Sie nach einigen Minuten erneut sich anzumelden. Wenn das Problem weiterhin besteht, senden Sie den EIM-Instanz-ID-Code an die Kundenunterstützung. |
| [!UICONTROL Ihre Anfrage schlug aufgrund zu vieler Spalten oder vorkonfigurierter Zeilen fehl.] | Ihre Tabelle enthält zu viele Freiformzellen (Zeile * Spalten). | Entfernen Sie Spalten oder Zeilen in der Tabelle oder erwägen Sie, die Tabelle in separate Anfragen zu unterteilen. |


## Fehlerbehebung

Bei Verwendung von Analysis Workspace können Sie die folgenden Informationen verwenden, um einige häufige Probleme zu beheben.

| Problem | Fehlerbehebung |
|---|---|
| Wenn ich eine Metrik per Drag-and-Drop ziehe, wird die Meldung *Ungültige Daten* angezeigt. | „Ungültige Daten“ bedeuten, dass Adobe keine Daten mit der Kombination von Dimensionen und Metriken zurückgeben kann, die im Bericht verwendet werden. Beispielsweise können zwei Metriken, die übereinander gestapelt sind, nicht als Daten zurückgegeben werden, da es nicht möglich ist, zwei Metriken in dieser Weise anzuzeigen. Platzieren Sie die Metriken stattdessen nebeneinander. |
| Wenn ich eine Metrik per Drag-and-Drop ziehe, sehe ich keine tatsächlichen Daten, sondern nur Nullen. | Wenn Sie einen Workspace-Bericht erfolgreich erstellt haben, aber keine Daten vorhanden sind, können Sie einige der folgenden Dinge überprüfen:<ul><li>Wenn Sie ein Segment in Ihrem Bericht angewendet haben, stimmen die Segmentkriterien möglicherweise nicht mit den Daten überein. Versuchen Sie, das Segment zu entfernen oder die Segmentdefinition anzupassen.</li><li>Überprüfen Sie den Datumsbereich oben rechts und stellen Sie sicher, dass er auf einen erwarteten Wert eingestellt ist.</li><li>Navigieren Sie zu Ihrer Website und überprüfen Sie mit dem [Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=de), ob Daten erfasst werden.</li></ul> |



<!--
# Common error messages

You may encounter errors when interacting with Analysis Workspace that will also influence performance. Listed below are the most common error types, why they occur, and optimizations that can be made.

| Error message | Why does this occur? | Optimization |
| --- | --- | --- |
| [!UICONTROL The report suite is experiencing unusually heavy reporting. Please try again later.] | Your organization is trying to run too many concurrent requests against a specific report suite. Contributors to this error are API requests, scheduled projects, and concurrent users making reporting requests. | Spread your requests and schedules for the report suite more evenly throughout the day. <p>Administrators can use the [Reporting Activity Manager to identify and cancel requests](/help/admin/admin/reporting-activity-manager/reporting-activity-overview.md) that are consuming reporting capacity. |
| [!UICONTROL The report suite is currently exceeding its reporting capacity. Please simplify the request or try again later.] |  Your organization is trying to run too many concurrent requests against a specific report suite. Contributors to this error are API requests, scheduled projects, scheduled reports, scheduled alerts, and concurrent users making reporting requests. | Spread your requests and schedules for the report suite more evenly throughout the day. |
| [!UICONTROL A system error has occurred. Please log a Customer Care request under Help > Submit Support Ticket and include your error code.] | Adobe is experiencing an issue that needs to be resolved. | Submit the error code to Customer Care. |
| [!UICONTROL An unexpected error has occurred; try refreshing your project again. If the problem persists, please submit this error ID to Adobe Customer Care for further diagnosis.] | Adobe is experiencing an issue that needs to be resolved. | Try refreshing your project and if the problem persists, submit the error code to Customer Care. |
| [!UICONTROL Error 500: Failed to load page] | Issues with your local network, such as company [firewall settings](https://experienceleague.adobe.com/docs/analytics/technotes/ip-addresses.html?lang=de), are a contributing factor to this error. Additionally, Adobe may be experiencing an issue that needs to be resolved. | Try logging in again after several minutes. If the issue persists, submit the EIM instance ID code to Customer Care. |
| [!UICONTROL One of the segments or the search in this visualization contains a text search that returned too many results.] | Your segment criteria or report filter is too broad. | Narrow your search text criteria and try the request again. |
| [!UICONTROL This dimension does not currently support non-default attribution models.] | Non-default attribution is not supported for the dimension that you are using. | Replace the dimension in your table with one that is compatible with [Attribution](/help/analyze/analysis-workspace/attribution/overview.md). |
| [!UICONTROL Your request failed as a result of too many columns or pre-configured rows.] | Your table has too many freeform cells (row * columns). | Remove columns or rows in your table, or consider splitting the table into separate requests. |
-->