---
title: Adobe Analytics in einer Entwicklungsumgebung bereitstellen
description: Hier erfahren Sie, wie Sie Tags verwenden, um Adobe Analytics in Ihrer Entwicklungsumgebung bereitzustellen.
feature: Tags
exl-id: 324943db-cb0b-40b1-8884-56bb3f608278
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 48%

---

# Analytics-Implementierung in einer Entwicklungsumgebung bereitstellen

Nachdem Sie eine Tag-Eigenschaft erstellt und konfiguriert haben, können die Bibliotheken bereitgestellt und Code auf Ihrer Site implementiert werden.

## Voraussetzungen

[Erstellen und konfigurieren einer Tag-Eigenschaft für Adobe Analytics](create-analytics-property.md): Greifen Sie auf das Werkzeug zu und erstellen Sie einen Raum für Ihre Analytics-Implementierung.

## Erstellen von Adaptern und Umgebungen

Tags ermöglichen durch die Bereitstellung von Code zahlreiche betriebliche Arbeitsabläufe. Führen Sie die folgenden Schritte aus, um die erforderlichen Mindestkomponenten für eine Analytics-Implementierung zu erstellen. Als Tag-Administrator können Sie innerhalb Ihres Unternehmens den richtigen Arbeitsablauf für die Bereitstellung von Adobe-Lösungen einrichten.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) an.
2. Klicken Sie auf die Tag-Eigenschaft, die Sie auf Ihrer Site implementieren möchten.
3. Klicken Sie auf **[!UICONTROL Hosts]** und dann auf **[!UICONTROL Host hinzufügen]**.
4. Benennen Sie ihn mit &quot;`"Adobe managed"`&quot;und wählen Sie &quot;**[!UICONTROL Verwaltet von Adobe]**&quot;in der Typ-Dropdownliste aus. Klicken Sie auf „Speichern“.
5. Navigieren Sie zu **[!UICONTROL Umgebungen]** und klicken Sie dann auf **[!UICONTROL Umgebung hinzufügen]**.
6. Wählen Sie **[!UICONTROL Entwicklung]** aus, geben Sie ihr den Namen `"Dev Environment"` und wählen Sie dann den vom Adobe verwalteten Host aus der Dropdownliste aus. Klicken Sie auf **[!UICONTROL Speichern]**.
7. Ein modales Fenster mit Anweisungen zur Web-Installation wird angezeigt. Wir kehren zu einem späteren Zeitpunkt zu diesem Fenster zurück. Klicken Sie zunächst auf **[!UICONTROL Schließen]** .
8. Klicken Sie auf &quot;**[!UICONTROL Umgebung hinzufügen]**&quot;, wählen Sie &quot;**[!UICONTROL Staging]**&quot;, geben Sie ihr den Namen &quot;`"Staging Environment"`&quot;ein und wählen Sie dann den vom Adobe verwalteten Host aus. Klicken Sie auf **[!UICONTROL Erstellen]** und schließen Sie dann das modale Fenster mit den Installationsanweisungen.
9. Klicken Sie erneut auf **[!UICONTROL Umgebung hinzufügen]** , wählen Sie **[!UICONTROL Produktion]**, geben Sie ihr den Namen `"Production Environment"` und wählen Sie dann den vom Adobe verwalteten Host aus. Klicken Sie auf **[!UICONTROL Erstellen]** und schließen Sie dann das modale Fenster mit den Installationsanweisungen.

## Erstellen einer Dev-Bibliothek

Trotz aller bisherigen Änderungen und Konfigurationen wurde kein Code veröffentlicht. Wenn Sie eine Bibliothek erstellen, also eine Sammlung von Änderungen, können Sie Code auf Ihrer Website veröffentlichen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) an.
2. Klicken Sie auf die Tag-Eigenschaft, die Sie auf Ihrer Site implementieren möchten.
3. Klicken Sie auf die Registerkarte **[!UICONTROL Veröffentlichungsfluss]** und dann auf **[!UICONTROL Bibliothek hinzufügen]**. Weitere Informationen zu dieser Seite finden Sie unter [Veröffentlichungsübersicht](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/overview.html?lang=de) in der Dokumentation zu Tags .
4. Benennen Sie die Bibliothek mit &quot;`'Initial changes'`&quot;und wählen Sie Ihre Entwicklungsumgebung aus.
5. Klicken Sie auf &quot;**[!UICONTROL Alle geänderten Ressourcen hinzufügen&quot;]**&quot;, in dem Adobe Analytics, der Identitätsdienst und der Core automatisch aufgeführt werden.
6. Klicken Sie auf **[!UICONTROL Speichern]**.
7. Klicken Sie im Bildschirm des Veröffentlichungs-Workflows auf die Dropdownliste neben Ihrer neuen Bibliothek und klicken Sie auf **[!UICONTROL Für Entwicklung erstellen]**. Nach einigen Sekunden wird der gelbe Punkt in der Bibliothek grün, was darauf hinweist, dass der Build erfolgreich war.
8. Navigieren Sie zu **[!UICONTROL Umgebungen]** und klicken Sie dann auf das Installationssymbol rechts neben Ihrer Entwicklungsumgebung. Durch diese Aktion wird das modale Fenster Web-Installationsanweisungen erneut angezeigt.
9. Kopieren Sie die Codeblöcke und stellen Sie sie den Website-Eigentümern Ihrer Organisation zur Verfügung.

## Installieren von Tags in der Entwicklungsumgebung Ihrer Website

Wenn Sie den Code Ihrer Website steuern, implementieren Sie die einzelnen Codeblöcke an ihrem jeweiligen Speicherort:

* Das Haupt-Tag gehört zum Tag `<head>` auf Ihrer Site.
* Wenn Sie Tags synchron laden möchten, müssen Sie auch einen zweiten Codeblock direkt unterhalb des schließenden `</body>` -Tags auf Ihrer Site einfügen. Sie können Bibliotheks-Tags synchron laden, indem Sie in den Web-Installationsanweisungen die Option **[!UICONTROL Bibliothek asynchron laden]** aktivieren.

Tag-Code wird normalerweise in der übergreifenden Vorlage der Site platziert. Eine leere Seite, die nur Implementierungscode enthält, würde wie folgt aussehen:

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
