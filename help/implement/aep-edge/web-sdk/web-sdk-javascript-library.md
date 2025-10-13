---
title: Senden von Daten an Adobe Analytics mithilfe der Web SDK JavaScript-Bibliothek
description: Beginnen Sie mit einer sauberen Web-SDK-Implementierung, um Daten mithilfe der JavaScript-Bibliothek an Adobe Analytics zu senden.
exl-id: 593b63ac-e411-4f88-af7e-78f026269ec0
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '1070'
ht-degree: 18%

---

# Senden von Daten an Adobe Analytics mithilfe der Web SDK JavaScript-Bibliothek

Dieser Implementierungspfad umfasst eine Neuinstallation von Web SDK mithilfe der Web SDK JavaScript-Bibliothek. Andere Implementierungspfade werden auf separaten Seiten behandelt:

* [Web SDK-Tag-Erweiterung](web-sdk-tag-extension.md): Eine neue Web SDK-Installation unter Verwendung der Web SDK-Tag-Erweiterung. Ähnelt dem Ansatz mit der Web SDK JavaScript-Bibliothek (diese Seite), mit der Ausnahme, dass Sie die Implementierung mithilfe von Tags in der Adobe Experience Platform-Datenerfassung verwalten. Dazu muss die Adobe Analytics ExperienceEvent-Feldergruppe, die typische Analytics-Variablen enthält, in Ihr XDM-Schema aufgenommen werden.
* [Analytics-Erweiterung zur Web SDK-Erweiterung](analytics-extension-to-web-sdk.md): Verwenden Sie einen reibungslosen und methodischen Ansatz, um von der Adobe Analytics-Tag-Erweiterung zur Web SDK-Tag-Erweiterung zu wechseln. Durch diesen Ansatz entfällt die Notwendigkeit, XDM zu verwenden, bis Ihr Unternehmen bereit ist, Adobe Experience Platform-Services wie Customer Journey Analytics zu verwenden. Verwenden Sie das `data`-Objekt anstelle des `xdm`-Objekts, um Daten an Adobe zu senden.
* [AppMeasurement to Web SDK JavaScript Library](appmeasurement-to-web-sdk.md): Ein reibungsloser und methodischer Ansatz für die Migration zum Web SDK, außer es werden keine Tags verwendet. Stattdessen können Sie die Adobe Analytics-Datenerfassungsbibliothek (`AppMeasurement.js`) manuell entfernen und durch die Web-SDK-JavaScript-Bibliothek (`alloy.js`) ersetzen.

## Vor- und Nachteile dieses Implementierungspfads

Die Verwendung der Web SDK JavaScript-Bibliothek zum Senden von Daten an Adobe Analytics hat Vor- und Nachteile. Wägen Sie jede Option sorgfältig ab, um zu entscheiden, welcher Ansatz für Ihr Unternehmen am besten geeignet ist.

| Vorteile | Nachteile |
| --- | --- |
| <ul><li>**Direkter Ansatz**: Dieser Implementierungspfad ist einfacher als Ansätze, die bestehende Adobe Analytics-Implementierungen verschieben. Wenn Sie derzeit keine Adobe Analytics-Implementierung haben, um die Sie sich Sorgen machen müssen, füllen Sie die entsprechenden XDM-Felder für Web SDK aus.</li><li>**Vordefiniertes Schema**: Wenn Ihr Unternehmen kein eigenes Schema benötigt, können Sie einfach das Schema verwenden, das auf Adobe Analytics ausgerichtet ist. Dieses Konzept gilt auch dann, wenn Sie sich Customer Journey Analytics nähern. Das Konzept der Props und eVars gilt nicht für Customer Journey Analytics, Sie können aber weiterhin Props und eVars als einfache benutzerdefinierte Dimensionen verwenden.</li></ul> | <ul><li>**Implementierungsänderungen erfordern**: Wenn Sie Änderungen an Ihrer Web SDK-Implementierung vornehmen möchten, müssen Sie mit Ihrem Entwicklungs-Team zusammenarbeiten, um den Code auf Ihrer Site zu bearbeiten. Der Ansatz, bei dem die Tag[Erweiterung „Web SDK&quot; verwendet wird](web-sdk-tag-extension.md) vermeidet diesen Nachteil.</li><li>**Mit einem bestimmten Schema verknüpft**: Wenn Ihr Unternehmen zu Customer Journey Analytics wechselt, müssen Sie entweder das Adobe Analytics-Schema weiter verwenden oder zum Schema Ihres eigenen Unternehmens migrieren (was ein separater Datensatz wäre). Wenn Ihr Unternehmen beim Wechsel zu Customer Journey Analytics sowohl das Adobe Analytics-Schema als auch die Migration zu einem separaten Datensatz vermeiden möchte, empfiehlt Adobe eine der beiden folgenden Methoden:</li><ul><li>Verwenden des `data`: Mit dem `data` können Sie Daten an Adobe Analytics senden, ohne einem XDM-Schema zu entsprechen. Nachdem das Schema Ihres Unternehmens erstellt wurde, können Sie die Datenstromzuordnung verwenden, um `data` Objektfelder XDM zuzuordnen. Sowohl [Analytics-Erweiterung zur Web SDK-Erweiterung](analytics-extension-to-web-sdk.md) als auch [AppMeasurement zur Web SDK JavaScript](appmeasurement-to-web-sdk.md)Bibliothek verwenden dieses `data`.</li><li>Adobe Analytics ganz überspringen: Wenn Sie die Web-SDK implementieren, können Sie diese Daten zur Verwendung in Customer Journey Analytics an einen Datensatz in Adobe Experience Platform senden. Sie können ein beliebiges Schema verwenden. Adobe Analytics ist an diesem Workflow überhaupt nicht beteiligt und erfordert daher keine Adobe Analytics ExperienceEvent-Feldergruppe. Diese Methode ist technisch am wenigsten verschuldet, lässt Adobe Analytics aber völlig außen vor.</li></ul></ul> |

>[!IMPORTANT]
>
>Diese Implementierungsmethode erfordert die Verwendung eines für Adobe Analytics konfigurierten Schemas. Wenn Ihr Unternehmen beabsichtigt, in Zukunft Ihr eigenes Schema mit Customer Journey Analytics zu verwenden, kann die Verwendung des Adobe Analytics-Schemas für Datenadministratoren oder -architekten zu Verwirrung führen. Es gibt mehrere Optionen, um dieses Hindernis zu beheben:
>
>* Sie können das Adobe Analytics-Schema in CJA verwenden. Beachten Sie, dass CJA kein Props- oder eVar-Konzept hat; sie werden wie jedes andere Schemafeld behandelt. Beachten Sie außerdem, dass die Verwendung des Adobe Analytics-Schemas in CJA die Verwendung anderer Platform-Services wie Adobe Journey Optimizer oder Real-Time Customer Data Platform erschweren kann.
>* Sie können das Datenobjekt verwenden, ähnlich wie bei einem Migrations-Workflow. Beachten Sie, dass Sie zur Verwendung des Datenobjekts jedes Datenobjektfeld einem XDM-Schemafeld zuordnen müssen.
>* Sie können die Adobe Analytics-Implementierung vollständig überspringen und Daten mithilfe Ihres eigenen Schemas an Adobe Experience Platform senden. Dieser Ansatz ist langfristig optimal und ermöglicht Ihrem Unternehmen, mit der Verwendung von Customer Journey Analytics zu beginnen.

## Zur Implementierung der Web SDK JavaScript-Bibliothek erforderliche Schritte

Ein allgemeiner Überblick über die Implementierungsaufgaben:

![Implementieren von Adobe Analytics mithilfe des Web-SDK-Workflows, wie in diesem Abschnitt beschrieben.](../../assets/websdk-annotated.png)

<table style="width:100%">

<tr>
<th style="width:5%"></th><th style="width:60%"><b>Aufgabe</b></th><th style="width:35%"><b>Weitere Informationen</b></th>
</tr>

<tr>
<td>1</td>
<td>Stellen Sie sicher, dass Sie <b>eine Report Suite definiert haben</b>.</td>
<td><a href="/help/admin/tools/manage-rs/report-suites-admin.md">Report Suite Manager</a></td>
</tr>

<tr>
<td>2</td>
<td><b>Schemata einrichten</b>. Um die Datenerfassung für die Verwendung in allen Anwendungen zu standardisieren, die Adobe Experience Platform nutzen, hat Adobe das offene und öffentlich dokumentierte Standard Experience-Datenmodell (XDM) erstellt.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=de">Übersicht über die Benutzeroberfläche von Schemata</a></td>
</tr>

<tr>
<td>3</td>
<td><b>Erstellen Sie eine Datenschicht</b>, um das Tracking der Daten auf Ihrer Website zu verwalten.</td>
<td><a href="../../prepare/data-layer.md">Datenschicht erstellen</a></td>
</tr>

<tr>
<td> 4</td>
<td><b>Installieren Sie die vordefinierte eigenständige Version</b>. Sie können direkt auf Ihrer Seite auf die Bibliothek (<code>alloy.js</code>) im CDN verweisen oder sie herunterladen und in Ihrer eigenen Infrastruktur hosten. Alternativ können Sie das NPM-Paket verwenden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/web-sdk/install/library.html">Installieren der vordefinierten eigenständigen Version</a> und <a href="https://experienceleague.adobe.com/docs/experience-platform/web-sdk/install/npm.html">Verwenden des NPM-Pakets</a></td>
</tr>

<tr>
<td>5</td>
<td><b>Konfigurieren eines Datenstroms</b>. Ein Datenstrom stellt die Server-seitige Konfiguration bei der Implementierung des Adobe Experience Platform Web SDK dar.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=de">Konfigurieren eines Datenstroms<a></td> 
</tr>

<td>6</td>
<td><b>Fügen Sie einen Adobe Analytics-Service</b> in Ihrem Datenstrom hinzu. Dieser Service steuert, ob und wie Daten an Adobe Analytics gesendet werden und an welche Report Suite(s).</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html#analytics">Hinzufügen des Adobe Analytics-Service zu einem Datenstrom</a></td>
</tr>

<tr>
<td>7</td>
<td><b>Konfigurieren des Web SDKs</b>. Stellen Sie sicher, dass die Bibliothek, die Sie in Schritt 4 installiert haben, ordnungsgemäß mit der Datenstrom-ID (ehemals Edge-Konfigurations-ID (<code>datastreamId</code>)), der Organisations-ID (<code>orgId</code>) und anderen verfügbaren Optionen konfiguriert ist. Sicherstellen einer ordnungsgemäßen Zuordnung von Variablen. </td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/web-sdk/commands/configure/overview.html">Konfigurieren der Web SDK</a><br/><a href="../xdm-var-mapping.md">XDM-Objektvariablenzuordnung</a></td>
</tr>

<tr>
<td>8</td>
<td><b>Führen Sie Befehle aus</b> und/oder <b>verfolgen Sie Ereignisse</b>. Nachdem der Basis-Code auf Ihrer Web-Seite implementiert wurde, können Sie mit der Ausführung von Befehlen und dem Nachverfolgen von Ereignissen mit dem SDK beginnen.
</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/web-sdk/commands/sendevent/overview.html">Ereignisse senden</a></td>
</tr>

<tr>
<td>9</td><td><b>Erweitern und validieren Sie die Implementierung</b>, bevor Sie sie in die Produktion verschieben.</td><td></td> 
</tr>
</table>
