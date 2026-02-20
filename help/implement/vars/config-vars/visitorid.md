---
title: visitorID
description: Verwenden Sie eine benutzerdefinierte Besucher-ID.
feature: Appmeasurement Implementation
exl-id: cb336042-01a1-4a66-a947-a221a7919c1b
role: Admin, Developer
source-git-commit: de98bf68c57f5453b6662f6e6e57312d8fd3e642
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 19%

---

# visitorID

Adobe verwendet mehrere verschiedene Methoden zum [Identifizieren von Besuchern](../../id/overview.md) auf Ihrer Site. **Die Variable `visitorID` überschreibt alle anderen Methoden der Besucheridentifizierung.**

>[!IMPORTANT]
>
>Adobe empfiehlt, diese Variable nicht zu verwenden. Verwenden Sie stattdessen den [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de).

## Verwendung von `visitorID` durch Analytics

Diese Variable ist eine manuelle Überschreibung der Besucher-ID, die alle anderen Formen der Besucheridentifizierung ersetzt. Um als einzelner Besucher gezählt zu werden, muss jeder Treffer für eine Person denselben `visitorID` verwenden.

* Treffer, bei denen `visitorID` auf eine andere Besucheridentifizierungsmethode zurückgreifen und die als separater Besucher behandelt werden.
* Treffer, die mehr als einen `visitorID` verwenden, werden als separate Besucher behandelt.
* Adobe ordnet keine Treffer zu, die unterschiedliche Besucher-IDs verwenden.

Siehe [Besucheridentifizierung in Adobe Analytics](../../id/overview.md) für Details zur Identifizierungspriorität und dazu, warum das Mischen von Identifikatoren die Besucherzahlen in die Höhe treiben kann.

>[!WARNING]
>
>Legen Sie `visitorID` nur fest, wenn Sie garantieren können, dass es bei jedem Treffer für diese Person festgelegt wird und dass sich der Wert nie ändert. Wenn Sie sie nur für einige Treffer festlegen, sie teilweise durch einen Besuch einführen (z. B. bei der Authentifizierung) oder sie zwischen Treffern ändern, wird die Aktivität eines einzelnen Besuchers in mehrere Besucher aufgeteilt.

>[!CAUTION]
>
>Ungültige benutzerdefinierte Besucher-ID-Werte können zu falschen Daten und schlechter Berichtsleistung führen. Wenn diese Variable einen Standard- oder Platzhalterwert enthält (z. B. `"0"` oder `"NULL"`), behandelt Adobe diese Treffer so, als wären sie ein und derselbe Besucher. Dies führt zu falschen Daten, wobei künstlich niedrige Besucherzahlen und Segmente auf Besucherebene nicht wie erwartet funktionieren. Falsch implementierte benutzerdefinierte Besucher-IDs können auch die Verarbeitungs-Server stark belasten, die [Latenz](/help/technotes/latency.md) erhöhen und die Berichtsleistung verringern.

## Besucher-ID bei Verwendung der Adobe Analytics-Erweiterung

[!UICONTROL Besucher-ID] ist ein Feld unter dem Akkordeon [!UICONTROL Cookies] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Wählen Sie die gewünschte Tag-Eigenschaft aus.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter &quot;Adobe Analytics **[!UICONTROL auf]** Konfigurieren“.
4. Erweitern Sie das Akkordeon [!UICONTROL Cookies], wodurch das Feld [!UICONTROL Besucher-ID] angezeigt wird.

Weisen Sie dieses Feld dem Datenelement zu, das Ihre benutzerdefinierte Besucher-ID enthält. **Legen Sie für dieses Feld nicht einen einzigen statischen Wert für alle Besucher fest.** Verwenden Sie ein Datenelement, das pro Besucher aufgelöst wird und über alle Treffer hinweg konstant bleibt.

## s.visitorID in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.visitorID`-Variable ist eine Zeichenfolge, die eine benutzerdefinierte eindeutige Kennung für den Besucher enthält. Gültige Werte sind alphanumerische Zeichen bis zu 100 Byte. Verwenden Sie in dieser Variablen keine Bindestriche, Leerzeichen, Unterstriche oder Symbole.

```js
s.visitorID = "abc123";
```

## Besucher-ID bei Verwendung der Web-SDK

Mit Adobe Experience Platform Edge Network können Sie mehrere Kennungen mithilfe der XDM-Identitätszuordnung [Identity Map) &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/identity/overview.html?lang=de#using-identitymap). Jede Identität in einer Identitätszuordnung hat einen anderen Namespace. Sie können angeben, welcher Namespace für die Besucher-ID als Teil der [Datenstromkonfiguration“ verwendet werden &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de#analytics). Nachdem dieses Feld konfiguriert wurde, wird es automatisch als Besucher-ID in Analytics verwendet, wenn Sie ein Ereignis senden, für das ein Wert für diesen Namespace angegeben ist.
