---
title: Globale Report Suites in Adobe Analytics
description: Machen Sie sich mit den Vorteilen und Anforderungen einer globalen Report Suite vertraut.
feature: Implementation Basics
exl-id: fa949b1e-80bd-41cf-a294-c840503b568f
role: Admin, Developer, Leader
TQID: https://experienceleague.adobe.com/Y96K5iwjDCqXBzMeYVGJA06e115acL3aZOJl8oCBBEs
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b0ca67c6-0a35-482c-ad91-baac1bcb26d6id: b3f03848-ae12-48b2-8aab-cad18567eb32id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7aid: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: c8add8f2-4250-4fd9-9cde-9707036c567did: df312454-73c4-43f6-a90e-18f5043f074cid: e7d92df1-c5ba-4e93-85df-f83171b889beid: f1f1a2d4-0976-4881-b091-c2bb8de7ffacid: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: a947d2d7f45d4155a61cbfe0f8110851cca32e60
workflow-type: tm+mt
source-wordcount: 885
ht-degree: 95%

---

# Überlegungen zur globalen Report Suite

Bei einer globalen Report Suite handelt es sich um eine Report Suite, die Daten aus allen Domänen und Apps sammelt, deren Inhaber Ihre Organisation ist. Diese Datenerfassungstechnik erfordert Vorbereitung und unter Umständen eine Koordinierung zwischen Teams in Ihrer Organisation.

## Vorteile

Adobe empfiehlt in den meisten Fällen die Implementierung einer globalen Report Suite.

* **Aggregierte Daten:** Globale Report Suites ermöglichen es Ihnen, KPIs und Erfolgsereignisse über Ihre eigenen Sites hinweg anzuzeigen. Mithilfe von Segmentierung und Virtual Report Suites können Site-spezifische Daten angezeigt werden.
* **Unterstützung für Cross-Device Analytics:** Cross-Device Analytics erfordert eine Report Suite, die Daten von mehreren Stellen sammelt, z. B. von Ihrer Website und Ihrer Mobile App. Separate Geräte können bei korrekter Implementierung Daten zuordnen. Weitere Informationen finden Sie unter [Cross-Device Analytics](../../components/cda/overview.md) im Benutzerhandbuch zu den Komponenten.
* **Nicht mehr als eine Report Suite erforderlich:** Alle Daten können in einer einzigen Report Suite gesammelt werden. So ist es weniger wahrscheinlich, dass ein Entwickler fälschlicherweise Daten an die falsche Report Suite sendet.
* **Keine Datenaggregation erforderlich:** Datenaggregationen sind eine ziemlich veraltete Funktion, mit der individuelle Report Suite-Daten täglich aggregiert werden. Datenaggregationen deduplizieren keine Besuchs- oder Besucherdaten, was zu verfälschten Zahlen führen kann. Weitere Informationen finden Sie unter [Datenaggregationen](../../admin/tools/manage-rs/rollup-report-suite.md) im Admin-Benutzerhandbuch.
* **Zeit sparen:** Workspace-Projekte, Klassifizierungen, Segmente und berechnete Metriken sind mit derselben globalen Report Suite verknüpft. Administratoren verbringen weniger Zeit mit der Verwaltung dieser Komponenten und der Data Governance.
* **Präzisere markenübergreifende Attribution:** Wenn ein Besuch auf einer Site beginnt und der Besucher dann auf eine andere Ihrer eigenen Sites klickt, bevor ein Erfolgsereignis ausgelöst wird, wird die Attribution genau erfasst. Beispiel: Ein Besucher klickt auf einen Paid Search-Link und landet auf Site A. Anschließend klickt er auf einen Link zu Site B und tätigt dort einen Kauf. Eine globale Report Suite ordnet die erworbenen Produkte korrekt der Paid Search zu.
* **Vereinfachte Implementierung:** Da alle Marken/Sites Daten an dieselbe Report Suite senden, sind Ihre Implementierungen auf jeder Site aufeinander abgestimmt. Diese erzwungene Verwaltung stellt sicher, dass eine bestimmte Dimension oder Metrik in derselben eVar oder demselben Ereignis gespeichert wird. Administratoren, Tester, Tag-Management-Inhaber und Analysten profitieren von dieser Vereinfachung.

>[!NOTE]
>
>Die Koordination einer globalen Report Suite-Implementierung ist ein großes Projekt. Adobe empfiehlt, mit einem Berater zusammenzuarbeiten, um Komplikationen und auftretende Probleme zu reduzieren.

## Starten einer neuen Implementierung mit einer globalen Report Suite

Befolgen Sie die folgenden allgemeinen Richtlinien, um die Implementierung einer globalen Report Suite zu verstehen.

1. Erstellen Sie die globale Report Suite in Adobe Analytics. Weitere Informationen finden Sie unter [Erstellen einer Report Suite](/help/admin/tools/manage-rs/new-rs/t-create-a-report-suite.md) im Admin-Benutzerhandbuch.
1. Arbeiten Sie mit Teams in Ihrer Organisation zusammen, die für die jeweilige Domain zuständig sind. Viele Teams verfügen über Reporting-Anforderungen, die sich auf ihren Geschäftsbereich beziehen.
1. Erfassen und aggregieren Sie alle diese Anforderungen in einem [Lösungsdesigndokument](solution-design.md). Wenn Teams ähnliche Anforderungen an eine Dimension haben, können sie dieselbe benutzerdefinierte Variable verwenden. Wenn beispielsweise sowohl Site A als auch Site B eine Breadcrumb-Dimension erfordern, können Implementierungen für beide Sites diese Daten über eVar1 senden.

   >[!IMPORTANT]
   >
   >Achten Sie darauf, dass jede benutzerdefinierte Variable domänenübergreifend gleich verwendet wird. Verwenden Sie nicht dieselbe eVar oder dasselbe Ereignis zu verschiedenen Zwecken auf Ihren Sites.
1. Stellen Sie sicher, dass jede Domain über eine Datenschicht verfügt, um die Datenerfassung zu vereinfachen. Daten können weiterhin ohne Datenschicht erfasst werden, doch die Zuverlässigkeit und Langlebigkeit Ihrer Implementierung nimmt dann ab, insbesondere wenn Ihre Site neu gestaltet wird.
1. Verwenden Sie Tags in Adobe Experience Platform, um Analytics zu implementieren. Verschiedene Sites erfordern wahrscheinlich unterschiedliche Datenelemente. Verwenden Sie für jede Domain spezifische Regeln, um sicherzustellen, dass jedes Datenelement korrekt ausgefüllt wird, und weisen Sie diese Datenelemente dann ihren jeweiligen eVars und Ereignissen zu. Siehe [Tags – Übersicht](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=de).
1. Schließen Sie den [Adobe-Besucher-ID](https://experienceleague.adobe.com/de/docs/id-service/using/home)Service ein und verwenden Sie die [`appendVisitorIDsTo`](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/methods/appendvisitorid.html?lang=de). Diese Funktion führt Besucherdaten zusammen, wenn Benutzer von einer Domain auf eine andere klicken.

## Ändern einer bestehenden Implementierung mit einer globalen Report Suite

Der Prozess der Umstellung einer vorhandenen Implementierung über mehrere Sites hinweg auf eine einzige globale Report Suite erfordert mehr Zeit und Koordination zwischen Teams in Ihrer Organisation.

1. Bestimmen Sie, ob Sie eine Ihrer vorhandenen Report Suites oder eine neue Report Suite verwenden möchten. Wenn Sie die Verwendungszwecke vorhandener Variablen in Ihrer Implementierung ändern möchten, wird empfohlen, mit einer neuen Report Suite zu beginnen.
2. Legen Sie ein Umstellungsdatum fest, an dem Sie zu einer globalen Report Suite wechseln möchten. Der beste Zeitpunkt für eine Umstellung ist zwischen zwei wichtigen Reporting-Zeiträumen oder in Kombination mit größeren Änderungen an Ihrer Site. Beispiele sind der Beginn eines Geschäftsquartals oder -jahres, während einer Site-Aktualisierung oder beim Wechsel zu einem neuen Tag-Management-System.
3. Gehen Sie wie oben beschrieben vor (erstellen Sie eine Report Suite, erfassen Sie Reporting-Anforderungen in einem Lösungsdesigndokument und richten Sie auf jeder Site eine Datenschicht ein). Wenn Sie Tags in Adobe Experience Platform implementieren, validieren Sie Ihre Implementierung mithilfe einer Entwicklungsversion Ihrer Website.
4. Sobald Sie sich vergewissert haben, dass Ihre Implementierung in der Entwicklung funktioniert, veröffentlichen Sie Ihre Tags-Implementierung am Umstellungsdatum.

>[!MORELIKETHIS]
>
>[Wechsel vom Multi-Suite-Tagging zu einer globalen Report Suite und zu Virtual Report SuitesVergleichen von Datenaggregationen und globalen Report Suites](../../admin/tools/manage-rs/rollup-report-suite.md)
