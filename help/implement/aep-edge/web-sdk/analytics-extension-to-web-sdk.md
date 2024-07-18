---
title: Migration von der Adobe Analytics-Tag-Erweiterung zur Web SDK-Tag-Erweiterung
description: Aktualisieren Sie Ihre Analytics-Implementierung auf Adobe Experience Platform-Datenerfassungs-Tags, um die Web SDK-Erweiterung zu verwenden.
exl-id: 691c29ca-d169-4ef8-9f91-d0375166796d
source-git-commit: 7bd4a188e5a2171260f1f0696d8bebad854dba4a
workflow-type: tm+mt
source-wordcount: '1706'
ht-degree: 5%

---

# Migration von der Adobe Analytics-Tag-Erweiterung zur Web SDK-Tag-Erweiterung

Dieser Implementierungspfad umfasst einen methodischen Migrationsprozess, um von der Adobe Analytics-Tag-Erweiterung zur Web SDK-Tag-Erweiterung zu wechseln. Andere Implementierungspfade werden auf separaten Seiten behandelt:

* [AppMeasurement in die JavaScript-Bibliothek des Web SDK](appmeasurement-to-web-sdk.md): Ein reibungsloser und methodischer Ansatz für die Migration zum Web SDK, allerdings werden keine Tags verwendet. Stattdessen entfernen Sie die Adobe Analytics-Datenerfassungsbibliothek (`AppMeasurement.js`) manuell und ersetzen Sie sie durch die Web SDK JavaScript-Bibliothek (`alloy.js`).
* [Web SDK tag extension](web-sdk-tag-extension.md): Eine neue Web SDK-Installation, bei der Sie die Implementierung mithilfe von Tags in der Adobe Experience Platform-Datenerfassung verwalten. Dazu ist die Adobe Analytics ExperienceEvent-Feldergruppe erforderlich, die typische Analytics-Variablen enthält, die in Ihr XDM-Schema aufgenommen werden sollen.
* [Web SDK JavaScript Library](web-sdk-javascript-library.md): Eine neue Web SDK-Installation mit der Web SDK JavaScript Library (`alloy.js`). Verwalten Sie die Implementierung selbst, anstatt die Tags-Benutzeroberfläche zu verwenden. Dazu ist die Adobe Analytics ExperienceEvent-Feldergruppe erforderlich, die typische Analytics-Variablen enthält, die in Ihr XDM-Schema aufgenommen werden sollen.

## Vorteile und Nachteile dieses Implementierungspfads

Die Verwendung dieses Migrationsansatzes hat sowohl Vor- als auch Nachteile. Legen Sie bei jeder Option sorgfältig ab, welcher Ansatz für Ihr Unternehmen am besten geeignet ist.

| Vorteile | Nachteile |
| --- | --- |
| <ul><li>**Keine Codeänderungen auf Ihrer Site**: Da Ihre Implementierung bereits Tags installiert hat, können alle Migrationsaktualisierungen auf der Tag-Oberfläche vorgenommen werden.</li><li>**Verwendet Ihre vorhandene Implementierung**: Für diesen Ansatz ist keine neue Implementierung erforderlich. Sie benötigen zwar neue Regelaktionen, können aber Ihre vorhandenen Datenelemente und Regelbedingungen mit minimalen Änderungen wiederverwenden.</li><li>**Kein Schema erforderlich**: Für diese Phase der Migration zum Web SDK benötigen Sie kein XDM-Schema. Stattdessen können Sie das Objekt `data` ausfüllen, das Daten direkt an Adobe Analytics sendet. Nachdem die Migration zum Web SDK abgeschlossen ist, können Sie ein Schema für Ihre Organisation erstellen und die Datastraam-Zuordnung verwenden, um die entsprechenden XDM-Felder auszufüllen. Wenn in dieser Phase des Migrationsprozesses ein Schema erforderlich ist, muss Ihr Unternehmen ein Adobe Analytics-XDM-Schema verwenden. Die Verwendung dieses Schemas erschwert es Ihrem Unternehmen, in Zukunft Ihr eigenes Schema zu verwenden.</li></ul> | <ul><li>**Technische Schulden bei der Implementierung**: Da dieser Ansatz eine modifizierte Form Ihrer vorhandenen Implementierung verwendet, kann es schwieriger sein, die Implementierungslogik zu verfolgen und bei Bedarf Änderungen vorzunehmen. Das Debuggen von benutzerspezifischem Code kann besonders schwierig sein.</li><li>**Erfordert eine Zuordnung zum Senden von Daten an Platform**: Wenn Ihre Organisation für die Verwendung von Customer Journey Analytics bereit ist, müssen Sie Daten an einen Datensatz in Adobe Experience Platform senden. Diese Aktion erfordert, dass jedes Feld im `data` -Objekt ein Eintrag im Tool für die Datenasterzuordnung ist, der ihn einem XDM-Schemafeld zuordnet. Die Zuordnung muss nur einmal für diesen Workflow durchgeführt werden. Implementierungsänderungen sind nicht erforderlich. Es handelt sich jedoch um einen zusätzlichen Schritt, der beim Senden von Daten in ein XDM-Objekt nicht erforderlich ist.</li></ul> |

Adobe empfiehlt, diesem Implementierungspfad in den folgenden Szenarien zu folgen:

* Sie verfügen über eine vorhandene Implementierung mit der Adobe Analytics-Tag-Erweiterung. Wenn Sie über eine Implementierung mit AppMeasurement verfügen, folgen Sie stattdessen dem Befehl [Migration von AppMeasurement zum Web SDK](appmeasurement-to-web-sdk.md) .
* Sie beabsichtigen in Zukunft Customer Journey Analytics zu verwenden, möchten Ihre Analytics-Implementierung jedoch nicht von Grund auf durch eine Web SDK-Implementierung ersetzen. Die Ersetzung Ihrer Implementierung durch das Web SDK erfordert den größten Aufwand, bietet aber auch die praktikabelste langfristige Implementierungsarchitektur. Wenn Ihr Unternehmen bereit ist, die Implementierung eines sauberen Web SDK durchzuführen, finden Sie weitere Informationen unter [Aufnehmen von Daten über das Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk) im Customer Journey Analytics-Benutzerhandbuch.

## Schritte für die Migration zum Web SDK

Die folgenden Schritte enthalten konkrete Ziele, auf die wir hinarbeiten müssen. Klicken Sie auf jeden Schritt, um detaillierte Anweisungen dazu zu erhalten.

+++**1. Erstellen und Konfigurieren eines Datastreams**

Erstellen Sie einen Datenspeicher in der Adobe Experience Platform-Datenerfassung. Wenn Sie Daten an diesen Datastream senden, leitet er Daten an Adobe Analytics weiter. Künftig leitet derselbe Datenspeicher Daten an Customer Journey Analytics weiter.

1. Navigieren Sie zu [experience.adobe.com](https://experience.adobe.com) und melden Sie sich mit Ihren Anmeldedaten an.
1. Verwenden Sie die Startseite oder die Produktselektor oben rechts, um zur **[!UICONTROL Datenerfassung]** zu navigieren.
1. Wählen Sie im linken Navigationsbereich **[!UICONTROL Datenspeicher]** aus.
1. Wählen Sie **[!UICONTROL Neuer Datenstrom]** aus.
1. Geben Sie den gewünschten Namen ein und wählen Sie dann **[!UICONTROL Speichern]** aus.
1. Nachdem der Datastream erstellt wurde, wählen Sie **[!UICONTROL Dienst hinzufügen]** aus.
1. Wählen Sie im Dropdown-Menü &quot;Dienst&quot;die Option **[!UICONTROL Adobe Analytics]**.
1. Geben Sie dieselbe Report Suite-ID ein wie die Site, an die Sie derzeit Analysedaten senden. Klicken Sie auf **[!UICONTROL Speichern]**.

![Hinzufügen des Adobe Analytics-Dienstes](assets/datastream-rsid.png) {style="border:1px solid lightslategray"}

Ihr Datastream kann jetzt Daten empfangen und an Adobe Analytics weitergeben.

+++

+++**2. Fügen Sie Ihrer Tag-Eigenschaft die Web SDK-Erweiterung hinzu**

In diesem Abschnitt wird Ihr -Tag für den Großteil der Migrationsschritte vorbereitet, die im nächsten Schritt unternommen werden.

1. Klicken Sie oben links in der Adobe Experience Platform-Benutzeroberfläche auf das Hamburger-Symbol und wählen Sie dann **[!UICONTROL Tags]** aus.
1. Wählen Sie die gewünschte Tag-Eigenschaft aus.
1. Wählen Sie im linken Navigationsbereich der Tag-Eigenschaft **[!UICONTROL Erweiterungen]** aus.
1. Wählen Sie oben **[!UICONTROL Katalog]** aus, um eine Liste aller verfügbaren Erweiterungen anzuzeigen.
1. Suchen Sie nach der Erweiterung **[!UICONTROL Adobe Experience Platform Web SDK]** und wählen Sie sie aus. Klicken Sie dann rechts auf **[!UICONTROL Installieren]** .

   ![Katalog](assets/catalog.png) {style="border:1px solid lightslategray"}

1. Die Erweiterungskonfigurationseinstellungen werden angezeigt. Suchen Sie den Abschnitt &quot;Datenspeicher&quot;und wählen Sie den Datenspeicher aus, den Sie im vorherigen Schritt erstellt haben.

   ![Auswahl des Datenspeichers](assets/datastream-select.png) {style="border:1px solid lightslategray"}

1. Wählen Sie **[!UICONTROL Speichern]** aus.

Für Ihre Tag-Eigenschaft ist jetzt das Web SDK installiert.

+++

+++**3. Datenobjektdatenelement** erstellen

Das Datenobjekt-Datenelement bietet ein intuitives Framework zum Konfigurieren einer Payload, die das Web SDK zum Senden an einen Datastream verwendet. Die meisten Regeln, die Sie im folgenden Schritt aktualisieren, interagieren mit diesem Datenelement.

1. Wählen Sie im linken Navigationsbereich der Tags-Oberfläche **[!UICONTROL Datenelemente]** aus.
1. Wählen Sie **[!UICONTROL Datenelement hinzufügen]** aus.
1. Legen Sie für das Datenelement die folgenden Einstellungen fest:
   * [!UICONTROL Name]: Alles, was Sie möchten, wie &quot;Datenschicht&quot;oder &quot;Datenobjekt&quot;
   * [!UICONTROL Erweiterung]: [!UICONTROL Adobe Experience Platform Web SDK]
   * [!UICONTROL Datenelementtyp]: [!UICONTROL Variable]
   * Kontrollkästchen können unverändert bleiben
1. Wählen Sie rechts die folgenden Einstellungen aus:
   * Optionsfeld &quot;Eigenschaft&quot;: [!UICONTROL Daten]
   * Lösung: [!UICONTROL Adobe Analytics]
1. Wählen Sie **[!UICONTROL Speichern]** aus.

![Datenelement erstellen](assets/create-data-element.png) {style="border:1px solid lightslategray"}

Ihre Tag-Eigenschaft verfügt jetzt über alles, was zum Aktualisieren der einzelnen Regeln erforderlich ist.

+++

+++**4. Aktualisieren Sie Regeln, um die Web SDK-Erweiterung anstelle der Analytics-Erweiterung zu verwenden**

Dieser Schritt enthält den Großteil des für die Migration zum Web SDK erforderlichen Aufwands und erfordert Kenntnisse darüber, wie Ihre Implementierung funktioniert. Im Folgenden finden Sie ein Beispiel für die Bearbeitung einer typischen Tag-Regel. Aktualisieren Sie alle Tag-Regeln in Ihrer Implementierung, um alle Verweise auf die Adobe Analytics-Erweiterung durch die Web SDK-Erweiterung zu ersetzen.

1. Wählen Sie im linken Navigationsbereich der Tags-Oberfläche **[!UICONTROL Regeln]** aus.
1. Wählen Sie eine zu bearbeitende Regel aus.
1. Wählen Sie die Aktion **[!UICONTROL Adobe Analytics - Variablen festlegen]** aus.
1. Beachten Sie alle in dieser Regel festgelegten Analytics-Variablen. Schließen Sie beide in den Dropdown-Menüs festgelegten Variablen und die in benutzerdefiniertem Code festgelegten Variablen ein.
1. Ändern Sie die [!UICONTROL Aktionskonfiguration] in die folgenden Einstellungen:
   * [!UICONTROL Erweiterung]: [!UICONTROL Adobe Experience Platform Web SDK]
   * [!UICONTROL Aktionstyp]: Variable aktualisieren
1. Stellen Sie sicher, dass Ihr Datenobjekt in der Dropdown-Liste auf der rechten Seite ausgewählt ist.
1. Legen Sie die Analytics-Variablen auf die gleichen Werte fest wie in der Analytics-Erweiterung konfiguriert.
   * Variablen, die in der Tag-Oberfläche festgelegt werden, können direkt in dieselben Werte übersetzt werden.
   * Zeichenfolgenvariablen, die in benutzerdefiniertem Code festgelegt werden, erfordern minimale Anpassungen. Verwenden Sie stattdessen `data.__adobe.analytics`, anstatt das Objekt `s` zu verwenden. Beispielsweise würde `s.eVar1` in `data.__adobe.analytics.eVar1` übersetzen.
   * Analytics-Konfigurationsvariablen und Methodenaufrufe in benutzerdefiniertem Code können eine geänderte Implementierungslogik erfordern. Sehen Sie sich die jeweiligen [Variablen](/help/implement/vars/overview.md) an, um zu bestimmen, wie die entsprechende Entsprechung mit dem Web SDK erreicht wird.
1. Nachdem alle Regellogik mit der Web SDK-Erweiterung repliziert wurde, wählen Sie **[!UICONTROL Änderungen beibehalten]** aus.
1. Wiederholen Sie diese Schritte für jede Aktionskonfiguration, in der die Adobe Analytics-Erweiterung zum Festlegen von Werten verwendet wird. Dieser Schritt umfasst sowohl Variablen, die mithilfe der Tag-Oberfläche festgelegt werden, als auch Variablen, die mithilfe von benutzerdefiniertem Code festgelegt werden. Benutzerdefinierte Codeblöcke können nirgends auf das Objekt `s` verweisen.

Die obigen Schritte gelten nur für Regeln, die Werte festlegen. Die folgenden Schritte ersetzen alle Aktionen, die die [!UICONTROL Aktionskonfiguration] [!UICONTROL Beacon senden] verwenden.

1. Wählen Sie eine Regel aus, die ein Beacon sendet.
1. Wählen Sie die Aktion **[!UICONTROL Adobe Analytics - Beacon senden]** aus.
1. Notieren Sie den aktuellen Wert der Optionsschaltfläche [!UICONTROL Tracking] auf der rechten Seite ([`s.t()`](../../vars/functions/t-method.md) oder [`s.tl()`](../../vars/functions/tl-method.md)).
1. Ändern Sie die [!UICONTROL Aktionskonfiguration] in die folgenden Einstellungen:
   * [!UICONTROL Erweiterung]: [!UICONTROL Adobe Experience Platform Web SDK]
   * [!UICONTROL Aktionstyp]: [!UICONTROL Ereignis senden]
1. Ändern Sie rechts die Aktionseinstellungen in Folgendes:
   * [!UICONTROL Typ]: Verwenden Sie für `s.t()` **[!UICONTROL Seitenansichten der Web-SeiteDetails]**. Verwenden Sie für `s.tl()` **[!UICONTROL Klicks auf Web-Webinteraction-Links]**. Wenn Sie [`s.tl()`](../../vars/functions/tl-method.md) verwenden, müssen Sie auch die folgenden Felder in Ihr Datenobjekt einschließen. Diese Felder werden bei der Ausführung der Aktionskonfiguration [!UICONTROL Variable aktualisieren] unter [!UICONTROL Zusätzliche Eigenschaften] aufgeführt:
      * [Link-Name](../../vars/functions/tl-method.md)
      * [Link-Typ ](../../vars/functions/tl-method.md)
      * [Link-URL](../../vars/config-vars/linkurl.md)
1. Wählen Sie **[!UICONTROL Änderungen beibehalten]** aus.
1. Wiederholen Sie diese Schritte für jede Aktionskonfiguration, bei der Adobe Analytics zum Senden eines Beacons verwendet wird.

+++

+++**5. Publish - aktualisierte Regeln**

Das Veröffentlichen aktualisierter Regeln folgt demselben Workflow wie jede andere Änderung an der Tag-Konfiguration.

1. Wählen Sie im linken Navigationsbereich der Tags-Benutzeroberfläche die Option **[!UICONTROL Veröffentlichungsfluss]**.
1. Wählen Sie **[!UICONTROL Bibliothek hinzufügen]** aus.
1. Geben Sie diesem Tag einen Namen, z. B. &quot;Aktualisierung auf Web SDK&quot;.
1. Wählen Sie **[!UICONTROL Alle geänderten Ressourcen hinzufügen]** aus.
1. Wählen Sie **[!UICONTROL Speichern]** aus.
1. Der Veröffentlichungs-Workflow zeigt einen orangefarbenen Punkt an, der angibt, dass er erstellt wird. Sobald der Punkt grün wird, sind Ihre Änderungen in Ihrer Entwicklungsumgebung verfügbar.
1. Testen Sie Ihre Änderungen in Ihrer Entwicklungsumgebung, um sicherzustellen, dass alle Regeln ordnungsgemäß ausgelöst werden und dass das Datenobjekt mit den erwarteten Werten gefüllt wird.
1. Wenn die Bibliothek fertig ist, senden Sie sie zur Genehmigung, erstellen Sie sie zum Staging, genehmigen Sie sie schließlich und veröffentlichen Sie sie in der Produktion.

![Veröffentlichungsfluss](assets/publishing-flow.png) {style="border:1px solid lightslategray"}

+++

+++**6. Analytics-Erweiterung deaktivieren**

Sobald Ihre Tag-Implementierung vollständig im Web SDK vorhanden ist, können Sie die Adobe Analytics-Erweiterung deaktivieren.

1. Wählen Sie im linken Navigationsbereich der Tags-Oberfläche **[!UICONTROL Erweiterungen]** aus.
1. Suchen und wählen Sie die Erweiterung [!UICONTROL Adobe Analytics] aus. Wählen Sie rechts **[!UICONTROL Deaktivieren]** aus.
1. Führen Sie denselben obigen Veröffentlichungsarbeitsablauf aus, um das Entfernen der Erweiterung [!UICONTROL Adobe Analytics] zu veröffentlichen.
1. Nachdem die Erweiterung in der Produktion deaktiviert wurde, können Sie sie vollständig deinstallieren. Wählen Sie die Erweiterung aus, wählen Sie das Menü mit den drei Punkten auf der rechten Seite aus und klicken Sie dann auf **[!UICONTROL Deinstallieren]**.
1. Führen Sie denselben obigen Veröffentlichungsarbeitsablauf aus, um diese Änderungen in der Produktion zu veröffentlichen.

+++

Zu diesem Zeitpunkt befindet sich Ihre Analytics-Implementierung vollständig im Web SDK und ist angemessen darauf vorbereitet, in Zukunft zu Customer Journey Analytics zu wechseln.
