---
title: Adobe Analytics in einer Entwicklungsumgebung bereitstellen
description: Hier erfahren Sie, wie Sie Tags verwenden, um Adobe Analytics in Ihrer Entwicklungsumgebung bereitzustellen.
feature: Tags
exl-id: 324943db-cb0b-40b1-8884-56bb3f608278
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/2wGsyulntC5-iSfcM9HEWXqBCAL-SUXWHM2r-4ylITg'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: df312454-73c4-43f6-a90e-18f5043f074c
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 603
ht-degree: 48%

---

# Analytics-Implementierung in einer Entwicklungsumgebung bereitstellen

Nachdem Sie eine Tag-Eigenschaft erstellt und konfiguriert haben, können die Bibliotheken bereitgestellt und Code auf Ihrer Site implementiert werden.

## Voraussetzungen

[Erstellen und konfigurieren einer Tag-Eigenschaft für Adobe Analytics](create-analytics-property.md): Greifen Sie auf das Werkzeug zu und erstellen Sie einen Raum für Ihre Analytics-Implementierung.

## Erstellen von Adaptern und Umgebungen

Tags ermöglichen durch die Bereitstellung von Code zahlreiche betriebliche Workflows. Führen Sie die folgenden Schritte aus, um die erforderlichen Mindestkomponenten für eine Analytics-Implementierung zu erstellen. Als Tag-Administrator können Sie innerhalb Ihres Unternehmens den richtigen Workflow für die Bereitstellung von Adobe-Lösungen einrichten.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) an.
2. Klicken Sie auf die Tag-Eigenschaft, die Sie auf Ihrer Site implementieren möchten.
3. Klicken Sie auf **[!UICONTROL Hosts]** und dann auf **[!UICONTROL Host hinzufügen]**.
4. Benennen Sie ihn `"Adobe managed"` und wählen Sie **[!UICONTROL Verwaltet von Adobe]** in der Dropdown-Liste Typ aus. Klicken Sie auf „Speichern“.
5. Navigieren Sie zu **[!UICONTROL Umgebungen]** und klicken Sie dann auf **[!UICONTROL Umgebung hinzufügen]**.
6. Wählen Sie **[!UICONTROL Entwicklung]**, benennen Sie ihn `"Dev Environment"`, und wählen Sie dann den verwalteten Adobe-Host aus der Dropdown-Liste aus. Klicken Sie auf **[!UICONTROL Speichern]**.
7. Ein modales Fenster mit Web-Installationsanweisungen wird angezeigt. Wir werden zu einem späteren Zeitpunkt zu diesem Fenster zurückkehren. Klicken Sie **[!UICONTROL auf]**.
8. Klicken Sie auf **[!UICONTROL Umgebung hinzufügen]**, wählen Sie **[!UICONTROL Staging]** aus, benennen Sie sie `"Staging Environment"` und wählen Sie dann den von Adobe verwalteten Host aus. Klicken Sie **[!UICONTROL Erstellen]** und schließen Sie dann das modale Fenster mit den Installationsanweisungen.
9. Klicken Sie erneut **[!UICONTROL Umgebung hinzufügen]**, wählen Sie **[!UICONTROL Produktion]**, benennen Sie sie `"Production Environment"` und wählen Sie dann den von Adobe verwalteten Host aus. Klicken Sie **[!UICONTROL Erstellen]** und schließen Sie dann das modale Fenster mit den Installationsanweisungen.

## Erstellen einer Dev-Bibliothek

Trotz aller bisherigen Änderungen und Konfigurationen wurde kein Code veröffentlicht. Wenn Sie eine Bibliothek erstellen, also eine Sammlung von Änderungen, können Sie Code auf Ihrer Website veröffentlichen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) an.
2. Klicken Sie auf die Tag-Eigenschaft, die Sie auf Ihrer Site implementieren möchten.
3. Klicken Sie auf die **[!UICONTROL Veröffentlichungsfluss]** und dann auf **[!UICONTROL Bibliothek hinzufügen]**. Weitere Informationen [&#x200B; dieser Seite finden Sie &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/overview.html?lang=de) der Tags-Dokumentation unter „Publishing-Übersicht“.
4. Benennen Sie die `'Initial changes'` und wählen Sie Ihre Entwicklungsumgebung aus.
5. Klicken Sie **[!UICONTROL Alle geänderten Ressourcen hinzufügen]**, wodurch Adobe Analytics, Identity Service und Core automatisch aufgelistet werden.
6. Klicken Sie auf **[!UICONTROL Speichern]**.
7. Klicken Sie auf dem Bildschirm Veröffentlichungs-Workflow auf die Dropdown-Liste neben Ihrer neuen Bibliothek und klicken Sie auf **[!UICONTROL Für Entwicklung erstellen]**. Nach einigen Sekunden wird der gelbe Punkt in der Bibliothek grün, was darauf hinweist, dass der Build erfolgreich war.
8. Navigieren Sie **[!UICONTROL Umgebungen]** und klicken Sie dann auf das Installationssymbol rechts neben Ihrer Entwicklungsumgebung. Durch diese Aktion wird das modale Fenster Web-Installationsanweisungen erneut angezeigt.
9. Kopieren Sie die Code-Blöcke und stellen Sie sie den Besitzern der Website Ihres Unternehmens zur Verfügung.

## Installieren von Tags in der Entwicklungsumgebung Ihrer Website

Wenn Sie den Code Ihrer Website steuern, implementieren Sie jeden Codeblock an seinem jeweiligen Speicherort:

* Das Haupt-Tag gehört zum `<head>`-Tag auf Ihrer Site.
* Wenn Sie Tags synchron laden möchten, müssen Sie auch einen zweiten Code-Block direkt unter dem schließenden `</body>`-Tag auf Ihrer Site einfügen. Sie können Bibliotheks-Tags synchron laden, indem Sie in den Web **[!UICONTROL Installationsanweisungen die Option „Bibliothek asynchron laden]** aktivieren.

Tag-Code wird normalerweise in der übergeordneten Vorlage der Site platziert. Eine leere Seite, die nur Implementierungscode enthält, würde wie folgt aussehen:

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Example page</title>
  <script src="//assets.adobedtm.com/launch-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx-development.min.js"></script>
</head>
<body>
   <p>This is a test page.</p>
   <!-- Only include this extra code if you load tags synchronously -->
   <script type="text/javascript">_satellite.pageBottom();</script>
</body>
</html>
```

## Fehlerbehebung

**Der Build-Versuch schlägt fehl.**

Ein häufiger Grund dafür ist, dass Elemente bereits in anderen Bibliotheken vorhanden sind, die in die Staging- oder Produktionsumgebung verschoben werden. Stellen Sie beim Erstellen von Bibliotheken sicher, dass der Bibliothek nur geänderte Ressourcen hinzugefügt werden.

## Nächste Schritte

[Validieren Sie Ihre Analytics-Implementierung und veröffentlichen Sie sie für die Produktion](validate-publish-prod.md): Mehrwert schaffen mit Adobe Analytics.
