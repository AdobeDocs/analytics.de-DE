---
title: linkLeaveQueryString
description: Ermöglicht die Beibehaltung von Abfragezeichenfolgen in Linktracking-Dimensionen.
feature: Variables
exl-id: 266f7d9c-803d-4dbe-95a1-282230012878
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '328'
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

## s.linkLeaveQueryString im AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

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
