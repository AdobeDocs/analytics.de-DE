---
title: linkInternalFilters
description: Verwenden Sie die Variable „linkInternalFilters“, um das automatische Tracking von Exitlinks zu unterstützen.
feature: Variables
exl-id: eaa6e64a-ebd5-4e6b-913f-1a6c315579c8
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 100%

---

# linkInternalFilters

AppMeasurement bietet die Möglichkeit, Links, die auf eine Stelle außerhalb Ihrer Website verweisen, automatisch zu verfolgen. Wenn [`trackExternalLinks`](trackexternallinks.md) aktiviert ist, wird eine Bildanfrage an Adobe geschickt, wenn ein Besucher auf einen Link klickt, um Ihre Website zu verlassen. Die Variablen [`linkExternalFilters`](linkexternalfilters.md) und `linkInternalFilters` bestimmen, welche Links als intern/extern betrachtet werden.

Wenn diese Variable einen Wert enthält, verhält sich das automatische Tracking von Exitlinks wie eine Blockierungsliste. Wenn ein Link-Klick keinem `linkInternalFilters`-Wert entspricht, wird er als Exitlink betrachtet. Die gesamte URL wird mit dieser Variablen verglichen. Wenn [`linkLeaveQueryString`](linkleavequerystring.md) aktiviert ist, wird auch die Abfragezeichenfolge geprüft.

Wenn Sie sowohl `linkInternalFilters` als auch `linkExternalFilters` gleichzeitig verwenden, muss der geklickte Link mit `linkExternalFilters` übereinstimmen **und** darf nicht mit `linkInternalFilters` überstimmen, um als Exitlink betrachtet zu werden. Wenn ein geklickter Link sowohl den Kriterien für Exitlinks als auch für Downloadlinks entspricht, hat der Downloadlink-Typ Priorität.

Activity Map verwendet diese Variable, um zu ermitteln, welche Links interne Links Ihrer Website sind. Adobe empfiehlt, diese Variable für Implementierungen festzulegen, die Activity Map verwenden.

>[!NOTE]
>
>`linkInternalFilters` und [interne URL-Filter](/help/admin/admin/internal-url-filter-admin.md) sind separate Funktionen, die unterschiedliche Zwecke erfüllen. Die `linkInternalFilters`-Variable wird speziell für das Tracking von Exitlinks verwendet. Interne URL-Filter sind eine Admin-Einstellung, die bei Traffic-Quellendimensionen (wie z. B. verweisende Domain) hilfreich ist.

## Ausgehende Links – „Niemals verfolgen“ bei Verwendung von Tags in Adobe Experience Platform

Das Feld „Niemals verfolgen“ ist eine kommagetrennte Liste von Filtern (üblicherweise Domains) unter dem Akkordeon [!UICONTROL Linktracking] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
4. Erweitern Sie das Akkordeon [!UICONTROL Linktracking], wodurch das Feld [!UICONTROL Ausgehende Links – Niemals verfolgen] angezeigt wird.

Platzieren Sie Filter, die Sie nie als Exitlinks verfolgen möchten, in diesem Feld. Trennen Sie mehrere Domänen durch ein Komma ohne Leerzeichen.

## s.linkInternalFilters in AppMeasurement und im benutzerdefinierten Code-Editor

Die `s.linkInternalFilters`-Variable ist eine Zeichenfolge mit Filtern (z. B. Domänen), die Sie als intern für Ihre Website betrachten. Trennen Sie mehrere Filter durch ein Komma ohne Leerzeichen.

```js
s.linkInternalFilters = "example.com,example.net";
```

Betrachten Sie das folgende Implementierungsbeispiel, als ob es auf `adobe.com` wäre:

```html
<script>
  s.trackExternalLinks = true;
  s.linkInternalFilters = "adobe.com";
</script>

<!-- The following link is an exit link because it does not match the anything under linkInternalFilters -->
<a href = "example.org">Example link 2</a>
```
