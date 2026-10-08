---
description: Erfahren Sie mehr über Fehler und die Fehlerbehebung für Analysis Workspace.
title: Fehler und Fehlerbehebung
feature: Workspace Basics
role: User, Admin
exl-id: e5c6f710-a205-48db-aeee-ee5b83c42795
TQID: 'https://experienceleague.adobe.com/Kr34CyT7YxRqKRdwpaLN-DZwHhLbaT663Gj-pc5Wd8s'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
    internal-label: Analysis Workspace
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
    internal-label: Dashboards
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
  - id: a421fb65-2c82-457a-921c-28c46b697a39
    internal-label: Analytics basics
subfeature_v2:
  - id: e93b8c4c-c5f7-45f8-9abe-9b710f53f502
    internal-label: Alerts
  - id: c457b289-f974-4a67-a5b6-dec3ffa77675
    internal-label: Workspace basics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 319f78bb5f8c2449a7263e3f1c378c49656889a7
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 94%
---
# Fehler und Fehlerbehebung

Bei der Interaktion mit Analysis Workspace können Fehler auftreten, die ggf. die Funktionalität und Leistung beeinflussen. Im Folgenden sind die häufigsten Fehlertypen, die Gründe dafür und Optimierungen aufgeführt, die vorgenommen werden können.

## Fehlermeldungen

Häufige Fehlermeldungen, die bei der Verwendung von Analysis Workspace möglicherweise angezeigt werden:

| Fehlermeldung | Fehlerursache | Optimierung |
| --- | --- | --- |
| [!UICONTROL Die Report Suite weist derzeit ein ungewöhnlich hohes Berichtvolumen auf. Bitte später erneut versuchen.] | Ihr Unternehmen versucht, zu viele Anfragen gleichzeitig für eine bestimmte Report Suite auszuführen. Zu diesem Fehler gehören API-Anfragen, geplante Projekte, terminierte Berichte, terminierte Warnhinweise und gleichzeitige Benutzer, die Reporting-Anfragen ausführen. | Verteilen Sie Ihre Anfragen und Zeitpläne für die Report Suite gleichmäßig über den Tag.<p>Admins können den [Berichterstellungsaktivitäts-Manager verwenden, um Anfragen zu identifizieren und abzubrechen](/help/admin/tools/reporting-activity-manager/reporting-activity-overview.md), die Berichtskapazität verbrauchen.</p> |
| [!UICONTROL Dieser Bericht ist zu komplex. Beachten Sie die Best Practices für die Erstellung von Analysis Workspace-Berichten.] | Ihre Reporting-Anfrage ist zu groß und kann nicht ausgeführt werden. Gründe für diesen Fehler sind Zeitüberschreitungen aufgrund der Komplexität der Anfrage. | Vereinfachen Sie die Anfrage. Verkürzen Sie beispielsweise den Datumsbereich, vereinfachen Sie die Segmentkriterien oder entfernen Sie einige Spalten oder Zeilen aus der Tabelle. Sie können die Tabelle ggf. auch in separate Anfragen aufteilen. |
| [!UICONTROL Die Report Suite überschreitet derzeit die Berichtskapazitäten. Bitte vereinfachen Sie die Anfrage oder versuchen Sie es später erneut.] | Ihr Unternehmen versucht, zu viele Anfragen gleichzeitig für eine bestimmte Report Suite auszuführen. Dieser Fehler kann etwa ausgelöst werden durch API-Anfragen, geplante Projekte und die gleichzeitige Ausführung von Reporting-Anfragen durch mehrere Benutzende. | Verteilen Sie Ihre Anfragen und Zeitpläne für die Report Suite gleichmäßig über den Tag. |
| [!UICONTROL Es ist ein Systemfehler aufgetreten. Melden Sie eine Anfrage an die Kundenunterstützung unter **[!UICONTROL Hilfe > senden Sie ein Support-Ticket]** und geben Sie Ihren Fehler-Code an.] | Adobe hat ein Problem, das behoben werden muss. | Senden Sie den Fehler-Code an die Kundenunterstützung. |
| [!UICONTROL Fehler 500: Seite konnte nicht geladen werden] | Probleme mit Ihrem lokalen Netzwerk, wie z. B. die [Firewall-Einstellungen](/help/technotes/ip-addresses.md) der Firma, tragen zu diesem Fehler bei. Darüber hinaus tritt bei Adobe möglicherweise ein Problem auf, das behoben werden muss. | Versuchen Sie nach einigen Minuten erneut sich anzumelden. Wenn das Problem weiterhin besteht, senden Sie den EIM-Instanz-ID-Code an die Kundenunterstützung. |
| [!UICONTROL Ihre Anfrage schlug aufgrund zu vieler Spalten oder vorkonfigurierter Zeilen fehl.] | Ihre Tabelle enthält zu viele Freiformzellen (Zeile * Spalten). | Entfernen Sie Spalten oder Zeilen in der Tabelle oder erwägen Sie, die Tabelle in separate Anfragen zu unterteilen. |


## Fehlerbehebung

Bei Verwendung von Analysis Workspace können Sie die folgenden Informationen verwenden, um einige häufige Probleme zu beheben.

| Problem | Fehlerbehebung |
|---|---|
| Wenn ich eine Metrik per Drag-and-Drop ziehe, wird die Meldung *Ungültige Daten* angezeigt. | „Ungültige Daten“ bedeuten, dass Adobe keine Daten mit der Kombination von Dimensionen und Metriken zurückgeben kann, die im Bericht verwendet werden. Beispielsweise können zwei Metriken, die übereinander gestapelt sind, nicht als Daten zurückgegeben werden, da es nicht möglich ist, zwei Metriken in dieser Weise anzuzeigen. Platzieren Sie die Metriken stattdessen nebeneinander. |
| Wenn ich eine Metrik per Drag-and-Drop ziehe, sehe ich keine tatsächlichen Daten, sondern nur Nullen. | Wenn Sie einen Workspace-Bericht erfolgreich erstellt haben, aber keine Daten vorhanden sind, können Sie einige der folgenden Dinge überprüfen:<ul><li>Wenn Sie ein Segment in Ihrem Bericht angewendet haben, stimmen die Segmentkriterien möglicherweise nicht mit den Daten überein. Versuchen Sie, das Segment zu entfernen oder die Segmentdefinition anzupassen.</li><li>Überprüfen Sie den Datumsbereich oben rechts und stellen Sie sicher, dass er auf einen erwarteten Wert eingestellt ist.</li><li>Navigieren Sie zu Ihrer Website und verwenden Sie die [Adobe Experience Platform Debugger](https://experienceleague.adobe.com/de/docs/experience-platform/debugger/home), um zu überprüfen, ob Daten erfasst werden.</li></ul> |
