---
title: linkLeaveQueryString
description: Ermöglicht die Beibehaltung von Abfragezeichenfolgen in Linktracking-Dimensionen.
feature: Appmeasurement Implementation
exl-id: 266f7d9c-803d-4dbe-95a1-282230012878
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/HI9yasKxMWctqoHOlZfkvMEWo1tDa3UWuWo22Bl3jFM'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 331
ht-degree: 84%

---

# linkLeaveQueryString

AppMeasurement entfernt Abfragezeichenfolgen standardmäßig aus Linktracking-URLs. Verwenden Sie die Variable `linkLeaveQueryString`, um Abfragezeichenfolgen in den Linktracking-Dimensionen beizubehalten.

Bei einigen Exitlinks und Downloadlinks kann sich der wichtige Teil der URL in der Abfragezeichenfolge befinden. Beispielsweise enthält ein Downloadlink wie `https://example.com/download.asp?filename=myfile.exe` wichtige Link-Informationen in der Abfragezeichenfolge.

Wenn die Linktracking-Informationen nicht in den URLs Ihrer Website enthalten sind, ist die Verwendung dieser Variablen nicht erforderlich. Das Entfernen von Abfragezeichenfolgen aus Linktracking-URLs hilft, die Anzahl der eindeutigen Werte zu begrenzen, die die Dimension enthält.

Die Aktivierung von `linkLeaveQueryString` gilt für alle Linktracking-Dimensionen (einschließlich benutzerspezifischer Links, Exitlinks und Downloadlinks).

>[!TIP]
>
>Diese Variable hat keine Auswirkungen auf Dimensionen außerhalb des Linktrackings. Sie betrifft nur benutzerspezifische Links, Exitlinks und Downloadlinks.

## Verarbeiten von Link-Abfragezeichenfolgen mit der Web-SDK

Abfragezeichenfolgen werden nicht aus dem XDM-`web.webInteraction.URL` entfernt. Wenn Sie Abfragezeichenfolgen aus diesem XDM-Feld entfernen möchten, können Sie sie mit `onBeforeEventSend` bearbeiten.

## Beibehalten von URL-Parametern mithilfe der Adobe Analytics-Erweiterung

[!UICONTROL URL-Parameter beibehalten] ist ein Kontrollkästchen unter dem Akkordeon [!UICONTROL Linktracking] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
4. Erweitern Sie das Akkordeon [!UICONTROL Linktracking], wodurch das Kontrollkästchen [!UICONTROL URL-Parameter beibehalten] angezeigt wird.

Aktivieren Sie dieses Kontrollkästchen, wenn Sie Abfragezeichenfolgen in die Linktracking-Dimensionen einbeziehen möchten.

## s.linkLeaveQueryString in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.linkLeaveQueryString`-Variable ist ein boolescher Wert. Der Standardwert lautet `false`.

* Wenn diese Variable auf `true` festgelegt ist, werden Abfragezeichenfolgen in Linktracking-URLs beibehalten.
* Wenn diese Variable auf `false` festgelegt oder nicht definiert ist, werden Abfragezeichenfolgen aus den Linktracking-URLs entfernt.

```js
s.linkLeaveQueryString = true;
```

## Beispiel

Seien Sie vorsichtig, wenn Sie diese Variable auf „true“ setzen, da dies Auswirkungen auf Linktracking-Filter wie [`linkInternalFilters`](linkinternalfilters.md), [`linkExternalFilters`](linkexternalfilters.md) und [`linkDownloadFiletypes`](linkdownloadfiletypes.md) haben kann.

Betrachten Sie das folgende Beispiel, als ob es auf `adobe.com` wäre:

```html
<script>
  s.linkInternalFilters = "adobe.com";
  s.linkLeaveQueryString = true;
</script>

<!--This link is not an exit link because the internal filter matches part of the query string -->
<a href = "example.com?r=adobe.com">Example link</a>
```
