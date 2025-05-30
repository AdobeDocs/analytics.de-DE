---
title: Implementieren von Adobe Analytics mit der Analytics-Erweiterung
description: Erfahren Sie, wie Sie Adobe Analytics mithilfe von Tags und der Analytics-Erweiterung implementieren
feature: Tags
exl-id: 52990731-8a68-4779-ad42-6ec94b0aabd1
role: Admin, Developer
source-git-commit: 43c39b99cbae3e714b7f017dec14dd02fa350790
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 83%

---

# Implementieren von Adobe Analytics mit der Analytics-Erweiterung

Seit dem Bestehen von Adobe Analytics hat Adobe verschiedene Methoden zur Implementierung von Code für die Datenerfassung auf Ihrer Website angeboten. Die derzeit empfohlene Methode für die Adobe ist [Tags](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=de) in Adobe Experience Platform.

Tags in Adobe Experience Platform ist eine Tag-Management-Lösung, mit der Sie Analytics-Code bereitstellen und weitere Tagging-Vorgaben erfüllen können. Adobe bietet Integrationen mit anderen Lösungen und Produkten und ermöglicht die Bereitstellung von benutzerdefiniertem Code. Alle diese Aufgaben können ausgeführt werden, ohne dass Entwicklungsteams in Ihrer Organisation Code auf Ihrer Website aktualisieren müssen.

Alle Kunden mit einem aktiven Adobe Experience Cloud-Vertrag können Tags verwenden. Wenn Sie sich wissen, ob Sie Zugriff haben, wenden Sie sich an einen Systemadministrator bzw. eine Systemadministratorin für Experience Cloud in Ihrem Unternehmen.

Ein allgemeiner Überblick über die Implementierungsaufgaben:



![Implementieren von Adobe Analytics mithilfe des Workflows der Analytics-Erweiterung, wie in diesem Abschnitt beschrieben.](../assets/analytics-extension-annotated.png)

<table style="width:100%">

<tr>
<th style="width:5%"></th><th style="width:60%"><b>Aufgabe</b></th><th style="width:35%"><b>Weitere Informationen</b></th>
</tr>

<tr>
<td> 1</td>
<td>Stellen Sie sicher, dass Sie <b>eine Report Suite definiert haben</b>.</td>
<td><a href="../../admin/admin/c-manage-report-suites/report-suites-admin.md">Report Suite Manager</a></td>
</tr>

<tr>
<td>2</td>
<td><b>Erstellen Sie eine Datenschicht</b>, um das Tracking der Daten auf Ihrer Website zu verwalten.</td>
<td>
<a href="../prepare/data-layer.md">Datenschicht erstellen</a>
</td>
</tr>

<tr>
<td>3</td>
<td><b><b>Erstellen Sie eine Tag-Eigenschaft</b>. Eigenschaften sind übergreifende Container, die für Verweise auf Tag-Management-Daten verwendet werden.</td>
<td><a href="../launch/create-analytics-property.md">Erstellen einer Tag-Eigenschaft in Adobe Analytics</a></td>
</tr>

<tr>
<td>4</td><td><b>Installieren Sie die Analytics-Erweiterung</b> in der Tag-Eigenschaft. Konfigurieren Sie die Analytics-Erweiterung, um Daten an Adobe Analytics zu senden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html?lang=de">Adobe Analytics-Erweiterung – Übersicht</a></td>
</tr>

<tr>
<td>5</td>
<td><b>Bereitstellung in einer Entwicklungsumgebung</b>. Verwenden Sie eine Umgebung, in der Sie die Entwicklung von Tags iterieren können.</td>
<td><a href="./deploy-dev.md">Analytics-Implementierung in einer Entwicklungsumgebung bereitstellen</td>
</tr>

<tr>
<td>6</td> 
<td><b>Validieren und Veröffentlichen in der Produktionsumgebung</b>. Betten Sie Code ein, um Ihre Tag-Eigenschaft in die Seiten Ihrer Website einzuschließen. Verwenden Sie dann Datenelemente, Regeln usw., um Ihre Implementierung anzupassen.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/publish/environments/environments.html?lang=de#embed-code">Einbettungs-Code</a><br/><a href="./validate-publish-prod.md">Validieren Sie eine Entwicklungsimplementierung und veröffentlichen Sie sie in der Produktionsumgebung</a></td>
</tr>

</table>

## Zusätzliche Ressourcen

Tags können in hohem Maße angepasst werden. Erfahren Sie, wie Sie Adobe Analytics optimal nutzen können, indem Sie die richtigen Daten in Ihre Implementierung aufnehmen.

- [Tags-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=de#): Hier erfahren Sie, wie die Benutzeroberfläche funktioniert und welche Erweiterungen verfügbar sind.

- [Implementierungsvariablen](../vars/overview.md): Legen Sie fest, welche Variablen Sie an Datenerfassungs-Server senden möchten.
