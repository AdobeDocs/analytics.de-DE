---
title: Entwicklungsimplementierung validieren und in der Produktion veröffentlichen
description: Hier erfahren Sie, wie Sie Tags in Adobe Experience Platform verwenden, um Adobe Analytics in Ihrer Produktionsumgebung bereitzustellen.
feature: Tags
exl-id: 2f5bcfee-d75e-4dac-bea9-91c6cc545173
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/FpJRwRs9GXGTzUY52vWqC5Ddej-I3mh2ASC6YKphNRI'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: c153fd90-23e1-4614-81d3-3cc7571227f7id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: df312454-73c4-43f6-a90e-18f5043f074c
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 301a0341e725ca15f1700046528ea5f42969add4
workflow-type: tm+mt
source-wordcount: 635
ht-degree: 65%

---

# Entwicklungsimplementierung validieren und in der Produktion veröffentlichen

Sobald Ihre Tag-Bibliothek in die Produktion verschoben wurde, kann Ihr Unternehmen Adobe Analytics verwenden, um grundlegende Berichte abzurufen.

## Voraussetzungen

[Stellen Sie Ihre Analytics-Implementierung in Ihrer Entwicklungsumgebung bereit](deploy-dev.md): Eine Analytics-Implementierung muss in Ihrer Entwicklungsumgebung veröffentlicht werden, um dieser Seite zu folgen.

## Validieren der Entwicklungsimplementierung mit dem CX Enterprise-Debugger

Der CX Enterprise-Debugger ist eine Erweiterung, die alle auf einer Seite vorhandenen CX Enterprise-Tags anzeigt.

1. Installieren Sie die Erweiterung für [Chrome](https://chromewebstore.google.com/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob) oder Firefox.
2. Navigieren Sie zu Ihrer Entwicklungs-Website, auf der Sie Tags implementiert haben.
3. Klicken Sie in Ihrem Browser auf das Symbol Adobe CX Enterprise Debugger .
4. Wenn alles ordnungsgemäß implementiert ist, sollten Inhalte in Adobe Analytics, Tags und der Besucher-ID-Dienst von Adobe Experience Cloud angezeigt werden.

## Bereitstellen der Dev-Implementierung für Staging/Produktion.

Nachdem Sie überprüft haben, ob Daten angezeigt werden, können Sie Ihre Implementierung an die Live-Version Ihrer Site pushen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) an.
1. Klicken Sie auf die Tag-Eigenschaft, die Sie auf Ihrer Site implementieren möchten.
1. Klicken Sie auf die Registerkarte **[!UICONTROL Publishing]** und suchen Sie die Bibliothek in der Spalte „Entwicklung“.
1. Klicken Sie in der Bibliothek auf die Dropdown-Liste und wählen Sie **[!UICONTROL Zur Genehmigung einreichen]**. Klicken Sie im modalen Fenster auf **[!UICONTROL Senden]**.
1. Klicken Sie erneut auf die Dropdown-Liste der Bibliothek (jetzt in der Spalte „Gesendet„) und wählen Sie **[!UICONTROL Für Staging erstellen]**.
1. Nach einigen Augenblicken wird das gelbe Licht der Bibliothek grün, was auf eine erfolgreiche Erstellung hinweist.
1. Klicken Sie erneut auf die Dropdown-Liste der Bibliothek und wählen Sie **[!UICONTROL Für Veröffentlichung genehmigen]**.
1. Klicken Sie erneut auf die Dropdown-Liste der Bibliothek (jetzt in der Spalte [!UICONTROL Genehmigt] und wählen Sie **[!UICONTROL Erstellen und in Produktion veröffentlichen]**.
1. Klicken Sie auf der Registerkarte „Umgebungen“ auf **[!UICONTROL Produktionsumgebung]**.
1. Kopieren Sie den Produktions-Installations-Code und stellen Sie ihn Ihren Website-Inhabern bereit. Fordern Sie an, diesen Code in der Produktionsumgebung Ihrer Site zu implementieren.

## Überprüfen der Produktionsimplementierung

Vergewissern Sie sich, dass Sie Daten zur Live-Version Ihrer Site sehen, und beginnen Sie mit der offiziellen Datenerfassung für Adobe Analytics.

1. Nachdem Sie sich von Ihren Website-Verantwortlichen bestätigen haben lassen, dass diese den Tag-Code in die Produktionsumgebung verschoben haben, navigieren Sie in Chrome zur Homepage Ihrer Website und öffnen Sie den Adobe CX Enterprise-Debugger.
2. Wenn alles funktioniert, sollten Sie ähnliche Daten wie Ihre Tests in Ihrer Entwicklungsumgebung sehen. Zu diesem Zeitpunkt erfassen Sie jetzt Daten auf Ihrer Site und können nun Adobe Analytics für die Berichterstellung verwenden.

## Fehlerbehebung

**Im Debugger werden keine Daten angezeigt.**

Öffnen Sie auf Ihrer Site die Entwicklerkonsole des Browsers (normalerweise F12). Sehen Sie sich den Quellcode der Seite an und stellen Sie sicher, dass Folgendes erfüllt ist:

* Es gibt keine JavaScript-Fehler in der Konsole. Wenden Sie sich an die Website-Inhaber Ihres Unternehmens, um sicherzustellen, dass alle JS-Fehler behoben sind.
* Der Kopfzeilencode ist ordnungsgemäß implementiert: Stellen Sie sicher, dass sich der Kopfzeilencode innerhalb des `<head>`-Tags befindet und dass die Datei vorhanden ist.
* AppMeasurement-Bibliothek vorhanden: Navigieren Sie direkt zur JS-Quelle, um sicherzustellen, dass die JS-Datei Code enthält. Ist dies nicht der Fall, stellen Sie sicher, dass jede Umgebung erstellt und die Bibliothek in der entsprechenden Umgebung veröffentlicht wurde.
* Überlagernde Erweiterungen: Einige Erweiterungen, wie z. B. Anzeigenblocker, können das Auslösen von Bildanforderungen verhindern. Deaktivieren Sie alle Erweiterungen, die das Senden von Daten an Adobe verhindern könnten.

## Nächste Schritte

Nachdem eine Basisimplementierung eingerichtet wurde, kann Ihre Rolle innerhalb Ihres Unternehmens beeinflussen, über welchen Pfad Sie mehr erfahren möchten:

* [Erstellen Sie ein Lösungsdesigndokument](../prepare/solution-design.md): Planen Sie, wie Sie benutzerdefinierte Variablen verwenden möchten, und schließen Sie sie dann in Ihre Implementierung ein
* [Erste Schritte mit Analysis Workspace](/help/analyze/analysis-workspace/home.md): Tauchen Sie mit der Flagship-Funktion des Tools direkt in Adobe Analytics ein.
