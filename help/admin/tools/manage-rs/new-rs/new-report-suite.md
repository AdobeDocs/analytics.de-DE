---
description: Sie können eine neue Report Suite erstellen, indem Sie eine vordefinierte Vorlage auswählen oder eine Ihrer vorhandenen Report Suites als Modell verwenden.
title: Neue Report Suite – Einstellungen
feature: Report Suite Settings
uuid: 3508f684-11a3-4c8f-a233-bea6bafd57c0
exl-id: ea5f8543-058d-4e08-bc66-575e3a7460c2
TQID: https://experienceleague.adobe.com/9wZ2rIgzZtJduhFAx6XcD53H2qzB2SZMr0pbxCopBvk
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
subfeature_v2:
  - id: c4cb071e-4667-4fb1-b1f1-d8994549cfb2
  - id: f52db89b-2666-4cad-9c50-9da4d3ffcfd0
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 541
ht-degree: 73%

---

# Neue Report Suite – Einstellungen

Sie können eine neue Report Suite erstellen, indem Sie eine vordefinierte Vorlage auswählen oder eine Ihrer vorhandenen Report Suites als Modell verwenden.

Im Folgenden werden die beim [Erstellen einer Report Suite](/help/admin/tools/manage-rs/new-rs/t-create-a-report-suite.md) verwendeten Elemente beschrieben.

>[!NOTE]
>
>In der [Dokumentation zu Virtual Report Suites](/help/components/vrs/c-workflow-vrs/vrs-create.md) erfahren Sie, wie Sie Virtual Report Suites erstellen.

| Element | Beschreibung |
| --- | --- |
| Report Suite-ID | Gibt eine eindeutige ID an, die nur alphanumerische Zeichen enthalten darf. Diese ID kann nach ihrer Erstellung nicht mehr geändert werden. Adobe legt das erforderliche ID-Präfix fest, das ebenfalls nicht geändert werden kann.  Achten Sie beim Erstellen mehrerer Report Suites darauf, dass die von Ihnen verwendeten Benennungsregeln eindeutige Report Suite-IDs ergeben. |
| Website-Titel | Gibt die Report Suite in den Admin Tools an. Der Titel wird ebenfalls in der Dropdown-Liste der Report Suites in der Kopfzeile der Suite verwendet. |
| Zeitzone | Wird zur Planung von Ereignissen und für Zeitstempeldaten verwendet. |
| Basis-URL | (Optional) Definiert die Basis-Domain für die Report Suite. Diese URL fungiert als interner URL-Filter, wenn Sie keine expliziten internen URL-Filter für die Report Suite definieren. |
| Standardseite | (Optional) Bereinigt Vorkommnisse des Werts „Standardseite“ von den dabei auftretenden URL-Adressen. Wenn der Bericht zu den beliebtesten Seiten URLs statt Seitennamen enthält, verhindert diese Einstellung, dass für eine Web-Seite mehrere URLs angegeben werden.  Beispielsweise sind die URLs `https://example.com` und `https://example.com/index.html` normalerweise dieselben Seiten.<p> Sie können irrelevante Dateinamen entfernen, sodass beide URL-Adressen in den Berichten als `https://example.com` angezeigt werden. Wenn Sie diesen Wert nicht angeben, entfernt Analytics automatisch die folgenden Dateinamen aus den URLs: `index.htm`, `index.html`, `index.cgi`, `index.asp`, `default.htm`, `default.html`, `default.cgi`, `default.asp`, `home.htm`, `home.html`, `home.cgi` und `home.asp`. Um das Ausblenden von Dateinamen zu deaktivieren, geben Sie einen Wert für die Standardseite an, der in Ihren URLs nie auftritt. |
| Tag der Live-Schaltung | Informiert Adobe über das Datum, an dem diese Report Suite voraussichtlich aktiviert wird. Wenn sich der Bereitstellungsplan ändert, müssen Sie in der Traffic-Verwaltung mithilfe des Tools für dauerhaft erwarteten Traffic eine aktualisierte Traffic-Schätzung eingeben. |
| Geschätzte Seitenansichten pro Tag | Gibt an, wie viele Seitenansichten diese Report Suite voraussichtlich in einem Tag unterstützen wird. Große Traffic-Volumina erfordern einen längeren Genehmigungsprozess. Um Verzögerungen bei der Verarbeitung zu vermeiden, sollten Sie diese Schätzung so genau wie möglich verwenden. |
| Basiswährung | Gibt die Standardwährung für die Speicherung sämtlicher Geldbeträge an. In der Analytics-Berichterstellung werden Transaktionen in anderen Währungen zum aktuellen Konversionskurs (d. h. zum Zeitpunkt des Eingangs der Daten) in die Basiswährung umgerechnet. Die Währung einer Transaktion wird in Analytics-Berichten mit der JavaScript-Variable „currencyCode“ erkannt. |
| Verarbeitung japanischer Keywords aktivieren | Aktiviert die Multi-Byte-Zeichenunterstützung für die Report Suite. Wenn Sie die Multi-Byte-Zeichenunterstützung deaktivieren, geht das System davon aus, dass die Daten im Format `ISO-8859-1` vorliegen. Auf Web-Seiten muss der Zeichensatz in der JavaScript-Variablen „charSet“ angegeben werden. <p>Bei der Multi-Byte-Zeichenunterstützung werden Zeichen der Report Suite als UTF-8 gespeichert. Beim Empfang der Daten konvertiert das System die Daten aus dem Zeichensatz der Web-Seite in den UTF-8-Zeichensatz, damit Sie in Ihren Marketing-Berichten eine beliebige Sprache verwenden können.  Wenden Sie sich an Ihr Adobe-Accountteam oder die Kundenunterstützung, wenn die Multi-Byte-Zeichenunterstützung für eine vorhandene Report Suite geändert werden soll. |
| Vereinfachtes Navigationsmenü verwenden | Diese Funktion war Teil von [Reports &amp; Analytics](https://new.express.adobe.com/webpage/WFCyq7w8kijmB?), die nicht mehr unterstützt wird. |

{style="table-layout:auto"}
