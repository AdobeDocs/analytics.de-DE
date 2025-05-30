---
description: Erfahren Sie mehr über die Feldbeschreibungen für den Manager für geplante Aufgaben.
title: Über den Manager für geplante Aufgaben
feature: Report Builder
role: User, Admin
exl-id: 8bacd7e4-ab50-4b36-842c-a8b6130a58d9
source-git-commit: fcecc8a493852f5682fd7fbd5b9bb484a850922c
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 86%

---

# Manager für geplante Aufgaben

{{legacy-arb}}

Im [!UICONTROL Manager für geplante Aufgaben] finden Sie eine Liste mit den vorhandenen terminierten Berichten, ihren Empfängern, Zeitplandetails und Dateiformaten. Sie können außerdem geplante Arbeitsmappen, deren Ausführung fehlgeschlagen ist, reaktivieren.

## Anhalten älterer geplanter Aufgaben

Am 21. April 2022 haben wir im Rahmen unserer Leistungs- und Versandoptimierungsbemühungen in Report Builder Änderungen an terminierten Aufgaben durchgeführt. Zu diesen Änderungen gehörte auch das Entfernen der Möglichkeit, dass geplante Sendungen „nach x Ereignissen beendet werden“. Als Reaktion auf mehrere Kundenanfragen, die mehr Zeit für die Erkundung und Implementierung von Alternativen benötigen, haben wir beschlossen, diese Option in begrenztem Umfang wieder einzuführen und bis zum **31. Januar 2023** aufrecht zu erhalten.

Sie können weiterhin stündliche Report Builder-Aufgaben planen und diese nach maximal 99 Vorfällen beenden lassen. Bitte beachten Sie, dass das Rollback nur für stündliche Aufgaben gilt. Die Option „Nach x Ereignissen beenden“ bleibt für alle anderen Versandintervalle (täglich, wöchentlich, monatlich und jährlich) weiterhin nicht verfügbar.

Beachten Sie, dass diese Option zum 31. Januar 2023 eingestellt wurde.
Bei weiteren Fragen oder bezüglich Support wenden Sie sich bitte an die Adobe-Kundenunterstützung.

Diese Pause gilt insbesondere für **vor dem 31. Januar 2020 erstellte Aufgaben**. Es werden keine Aufgaben, Arbeitsmappen oder Daten gelöscht. Aufgaben, die älter als zwei Jahre sind, werden angehalten und es werden keine weiteren geplanten Aufgaben gesendet.

Alle Aufgaben, die fortgesetzt werden sollen, können reaktiviert werden. Melden Sie sich bei Report Builder an und starten Sie den [!UICONTROL Manager für geplante Aufgaben]. Klicken Sie auf **[!UICONTROL Reaktivieren]** für die geplante Aufgabe, für die Sie den Versand fortsetzen möchten. Die Gültigkeit von reaktivierten Aufgaben beträgt standardmäßig 18 Monate – es sei denn, es wird ein kürzeres Ablaufdatum ausgewählt.

Darüber hinaus gilt für alle Aufgaben mit einem Erstellungsdatum von weniger als zwei Jahren ohne aktuelles Ablaufdatum (oder mit einem Ablaufdatum von mehr als zwei Jahren) das standardmäßige Ablaufdatum von 18 Monaten. Das neue Ablaufdatum ist der 15. Oktober 2023. Sie können dieses Ablaufdatum auf weniger als 18 Monate ändern, es kann jedoch nicht länger sein. Zum Zeitpunkt des Ablaufs wird die Aufgabe angehalten. Sie können die Aufgabe jedoch mit einem neuen Ablaufdatum von 18 Monaten erneut aktivieren. Es werden keine Aufgaben, Arbeitsmappen oder Daten gelöscht.

Ziel dieser Pause ist es, unsere Datenbank geplanter Aufgaben effektiv zu verwalten und zu pflegen, um eine optimale Leistung und Bereitstellung für alle nötigen Aufgaben und Arbeitsmappen sicherzustellen. Dies wird künftig unsere neue Governance-Richtlinie sein. Nach dem 31. Januar 2023 haben alle Aufgaben ein maximales Ablaufdatum von 18 Monaten. Nach 18 Monaten werden abgelaufene Aufgaben angehalten und können bei Bedarf reaktiviert werden.

## Geplante Aufgaben konfigurieren

| Feld | Beschreibung |
| --- | --- |
| **[!UICONTROL Registerkarte „Geplante Berichte“]** | |
| [!UICONTROL Berichtsname] | Dies ist der Name der geplanten Aufgabe. |
| [!UICONTROL E-Mail/FTP] | Die E-Mail- oder FTP-Adresse des Empfängers. **Hinweis:** Wenn E-Mail ausgewählt ist, werden Berichte, die größer als 1 MB sind, automatisch als ZIP-Datei an die E-Mail angehängt. Dank dieser Funktion bleibt die Größe der angehängten Dateien klein. Diese Funktion kann nicht deaktiviert werden. |
| [!UICONTROL Veröffentlichungsoptionen] | In dieser Spalte wird Power BI aufgeführt, wenn eine der [Veröffentlichungsoptionen für Power BI](https://experienceleague.adobe.com/docs/analytics/analyze/legacy-report-builder/publish-powerbi/power-bi.html?lang=de) ausgewählt ist. |
| [!UICONTROL Zeitplan] | Der Typ der geplanten Bereitstellung. |
| [!UICONTROL Dateiformat] | Das Bereitstellungsformat des Berichts, z. B. Excel, PDF, HTML usw. |
| [!UICONTROL Reaktivieren] | Wenn eine geplante Arbeitsmappe nicht ausgeführt werden kann, unternimmt Report Builder in jeweils 15 Minuten Abstand zwei weitere Ausführungsversuche. Nach drei fehlgeschlagenen Versuchen deaktiviert Report Builder den Zeitplan und die Schaltfläche „Reaktivieren“ wird angezeigt. Wenn Sie eine Arbeitsmappe reaktivieren, wird die geplante Bereitstellung ab dem Zeitpunkt wiederaufgenommen, an dem die Deaktivierung erfolgte.<p>Wenn eine geplante Arbeitsmappe beispielsweise vor 14 Tagen deaktiviert wurde und Sie sie heute reaktivieren, wird sie für jeden fehlenden Tag, also 14-mal ausgeliefert. Wenn die Arbeitsmappe für die fehlenden Tage nicht ausgeliefert werden soll, können Sie die geplante Arbeitsmappe löschen und eine neue geplante Arbeitsmappe unter Verwendung derselben Planungsparameter erstellen.<p>**Hinweis:** Reaktivieren Sie eine Arbeitsmappe erst wieder, wenn Sie die Ursache der Deaktivierung durch das System kennen. Laden Sie zur Fehlerbehebung eine deaktivierte Arbeitsmappe herunter und aktualisieren Sie sie auf der Client-Seite. Wenn keine Fehlermeldung erfolgt, sollte die Arbeitsmappe reaktiviert werden können. |
| [!UICONTROL Zuletzt gesendet] | Das Datum und die Uhrzeit, an denen der Bericht zuletzt gesendet wurde. |
| **Registerkarte „Empfänger“** | |
| [!UICONTROL E-Mail-Adresse des Empfängers] | Die E-Mail-Adresse des Berichtempfängers. |
| [!UICONTROL Berichte] | Die Berichte, die an die einzelnen Empfänger gesendet wurden. |
| **Registerkarte „Berichte – Verlauf“** | |
| [!UICONTROL Dateiname] | Dies ist der Name der geplanten Aufgabe. |
| [!UICONTROL Datum] | Das Datum und die Uhrzeit, an denen der Bericht zuletzt gesendet wurde. |
| [!UICONTROL Status] | Der Status gibt an, ob der Bericht gesendet oder nicht gesendet wurde. |
| [!UICONTROL E-Mail/FTP] | Die E-Mail- oder FTP-Adresse des Empfängers des Berichts. |
| [!UICONTROL Dateiformat] | Das Bereitstellungsformat des Berichts, z. B. Excel, PDF, HTML usw. |
