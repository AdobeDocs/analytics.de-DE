---
description: Sie können eine neue Report Suite erstellen, indem Sie eine vordefinierte Vorlage auswählen oder eine Ihrer vorhandenen Report Suites als Modell verwenden.
title: Neue Report Suite – Einstellungen
feature: Report Suite Settings
uuid: 3508f684-11a3-4c8f-a233-bea6bafd57c0
exl-id: ea5f8543-058d-4e08-bc66-575e3a7460c2
source-git-commit: 8c0e88a22928d79599ab0a0ad3efc8159712d739
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 94%

---

# Neue Report Suite – Einstellungen

Sie können eine neue Report Suite erstellen, indem Sie eine vordefinierte Vorlage auswählen oder eine Ihrer vorhandenen Report Suites als Modell verwenden.

Im Folgenden werden die beim [Erstellen einer Report Suite](/help/admin/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md) verwendeten Elemente beschrieben.

>[!NOTE]
>
>In der [Dokumentation zu Virtual Report Suites](/help/components/vrs/c-workflow-vrs/vrs-create.md) erfahren Sie, wie Sie Virtual Report Suites erstellen.

| Element | Beschreibung |
| --- | --- |
| Report Suite-ID | Gibt eine eindeutige ID an, die nur alphanumerische Zeichen enthalten darf. Diese ID kann nach dem Erstellen nicht mehr geändert werden. Adobe legt das erforderliche ID-Präfix fest, das ebenfalls nicht geändert werden kann.  Achten Sie beim Erstellen mehrerer Report Suites darauf, dass die von Ihnen verwendeten Benennungsregeln eindeutige Report Suite-IDs ergeben. |
| Website-Titel | Gibt die Report Suite in den Admin Tools an. Der Titel wird ebenfalls in der Dropdown-Liste der Report Suites in der Kopfzeile der Suite verwendet. |
| Zeitzone | Wird zur Planung von Ereignissen und für Zeitstempeldaten verwendet. |
| Basis-URL | (Optional) Definiert die Basisdomäne für die Report Suite. Diese URL-Adresse fungiert als interner URL-Filter, wenn Sie nicht explizit interne URL-Filter für die Report Suite definiert haben. |
| Standardseite | (Optional) Bereinigt Vorkommnisse des Werts „Standardseite“ von den dabei auftretenden URL-Adressen. Wenn der Bericht zu den beliebtesten Seiten URLs statt Seitennamen enthält, verhindert diese Einstellung, dass für eine Web-Seite mehrere URLs angegeben werden.  Beispielsweise sind die URLs `https://example.com` und `https://example.com/index.html` normalerweise dieselben Seiten.<p> Sie können irrelevante Dateinamen entfernen, sodass beide URL-Adressen in den Berichten als `https://example.com` angezeigt werden. Wenn Sie diesen Wert nicht angeben, entfernt Analytics automatisch die folgenden Dateinamen aus den URLs: `index.htm`, `index.html`, `index.cgi`, `index.asp`, `default.htm`, `default.html`, `default.cgi`, `default.asp`, `home.htm`, `home.html`, `home.cgi` und `home.asp`. Wenn Sie die Bereinigung von Dateinamen deaktivieren möchten, geben Sie einen Wert für „Standardseite“ an, der in keiner URL-Adresse vorkommt. |
| Aufschaltdatum | Informiert Adobe über das Datum, ab dem diese Report Suite aktiv sein soll. Wenn sich der Bereitstellungsplan ändert, müssen Sie in der Traffic-Verwaltung mithilfe des Tools für dauerhaft erwarteten Traffic eine aktualisierte Traffic-Schätzung eingeben. |
| Geschätzte Seitenansichten pro Tag | Gibt an, wie viele Seitenaufrufe diese Report Suite pro Tag unterstützen soll. Ein großes Traffic-Volumen beansprucht mehr Zeit im Genehmigungsprozess. Die Schätzung sollte möglichst genau ausfallen, damit es nicht zu Verzögerungen bei der Verarbeitung kommt. |
| Basiswährung | Gibt die Standardwährung für die Speicherung sämtlicher Geldbeträge an. In der Analytics-Berichterstellung werden Transaktionen in anderen Währungen zum aktuellen Konversionskurs (d. h. zum Zeitpunkt des Eingangs der Daten) in die Basiswährung umgerechnet. Die Währung einer Transaktion wird in Analytics-Berichten mit der JavaScript-Variable „currencyCode“ erkannt. |
| Verarbeitung japanischer Keywords aktivieren | Aktiviert die Multi-Byte-Zeichenunterstützung für die Report Suite. Wenn Sie die Multi-Byte-Zeichenunterstützung deaktivieren, geht das System davon aus, dass die Daten im Format `ISO-8859-1` vorliegen. Auf Web-Seiten muss der Zeichensatz in der JavaScript-Variablen „charSet“ angegeben werden. <p>Bei der Multi-Byte-Zeichenunterstützung werden Zeichen der Report Suite als UTF-8 gespeichert. Beim Empfang der Daten konvertiert das System die Daten aus dem Zeichensatz der Web-Seite in den UTF-8-Zeichensatz, damit Sie in Ihren Marketing-Berichten eine beliebige Sprache verwenden können.  Wenden Sie sich an Ihr Adobe-Accountteam oder die Kundenunterstützung, wenn die Multi-Byte-Zeichenunterstützung für eine vorhandene Report Suite geändert werden soll. |
| Vereinfachtes Navigationsmenü verwenden | Diese Funktion war Teil von [Reports &amp; Analytics](https://new.express.adobe.com/webpage/WFCyq7w8kijmB?), die nicht mehr unterstützt wird. |

{style="table-layout:auto"}
