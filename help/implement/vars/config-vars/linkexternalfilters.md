---
title: linkExternalFilters
description: Verwenden Sie die Variable „linkExternalFilters“, um das automatische Tracking von Exitlinks zu unterstützen.
feature: Appmeasurement Implementation
exl-id: 7d4e8d96-17ee-4a04-9a57-37d2056ee9a7
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 91%

---

# linkExternalFilters

AppMeasurement bietet die Möglichkeit, Links, die auf eine Stelle außerhalb Ihrer Website verweisen, automatisch zu verfolgen. Wenn [`trackExternalLinks`](trackexternallinks.md) (AppMeasurement) oder [`clickCollectionEnabled`](trackexternallinks.md) (Web SDK) aktiviert ist, wird eine Bildanfrage an Adobe geschickt, wenn ein Besucher bzw. eine Besucherin auf einen Link klickt, um Ihre Website zu verlassen. Die Variablen `linkExternalFilters` und [`linkInternalFilters`](linkinternalfilters.md) bestimmen, welche Links als intern/extern betrachtet werden.

Wenn diese Variable einen Wert enthält, verhält sich das automatische Tracking von Exitlinks wie eine Zulassungsliste. Wenn ein Link-Klick keinem `linkExternalFilters`-Wert entspricht, wird er nicht als Exitlink betrachtet. Die gesamte URL wird mit dieser Variablen verglichen. Wenn [`linkLeaveQueryString`](linkleavequerystring.md) aktiviert ist, wird auch die Abfragezeichenfolge geprüft.

>[!TIP]
>
>Verwenden Sie diese Variable nur, wenn Sie genau wissen, welche Domains Sie als Exitlinks betrachten möchten. Viele Unternehmen stellen fest, dass die Verwendung von `linkInternalFilters` für das Tracking von Exitlinks ausreicht, und verwenden `linkExternalFilters` nicht.

Wenn Sie sowohl `linkInternalFilters` als auch `linkExternalFilters` gleichzeitig verwenden, muss der geklickte Link mit `linkExternalFilters` übereinstimmen **und** darf nicht mit `linkInternalFilters` überstimmen, um als Exitlink betrachtet zu werden. Wenn ein geklickter Link sowohl den Kriterien für Exitlinks als auch für Downloadlinks entspricht, hat der Downloadlink-Typ Priorität.

## Exitlinks im Web SDK

Links qualifizieren sich automatisch als Exitlink, wenn sich die Ziel-Domain des Links vom aktuellen `window.location.hostname` unterscheidet. Das Web SDK bietet keine Konfigurationsvariablen, um die automatische Exitlink-Erkennung zu ändern. Wenn Sie die Domains, die als Exitlink gelten, anpassen müssen, können Sie die benutzerdefinierte Logik im `onBeforeEventSend`-Callback verwenden.

Weitere Informationen finden Sie in der Web-SDK-Dokumentation im Abschnitt [Automatisches Linktracking](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/track-links.html?lang=de#automaticLinkTracking).

## Ausgehende Links - Tracking mithilfe der Adobe Analytics-Erweiterung

Das Feld „Verfolgen“ ist eine kommagetrennte Liste von Filtern (üblicherweise Domains) unter dem Akkordeon [!UICONTROL Linktracking] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
4. Erweitern Sie das Akkordeon [!UICONTROL Linktracking], wodurch das Feld [!UICONTROL Ausgehende Links – Verfolgen] angezeigt wird.

Platzieren Sie Filter, die Sie immer als extern betrachten wollen, in diesem Feld. Trennen Sie mehrere Domänen durch ein Komma ohne Leerzeichen.

## s.linkExternalFilters in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.linkExternalFilters`-Variable ist eine Zeichenfolge mit Filtern (z. B. Domänen), die Sie als Exitlinks betrachten. Trennen Sie mehrere Domänen durch ein Komma ohne Leerzeichen.

```js
s.linkExternalFilters = "example.com,example.net,example.org";
```

Betrachten Sie das folgende Implementierungsbeispiel, als ob es auf `adobe.com` wäre:

```html
<script>
  s.trackExternalLinks = true;
  s.linkExternalFilters = "example.com,example.net";
</script>

<!-- The following link is NOT considered an exit link, even though the link is outside adobe.com -->
<a href = "example.org">Example link 1</a>

<!-- The following link is an exit link because it matches the linkExternalFilters allowlist -->
<a href = "example.com">Example link 2</a>
```
