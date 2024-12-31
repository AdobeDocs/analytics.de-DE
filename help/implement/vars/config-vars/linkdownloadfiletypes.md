---
title: linkDownloadFileTypes
description: Legen Sie Dateierweiterungen fest, die automatisch als Downloadlinks verfolgt werden.
feature: Variables
exl-id: 5089571a-d387-4ac7-838f-8bc95b2856fb
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 55%

---

# linkDownloadFileTypes

Wenn [`trackDownloadLinks`](trackdownloadlinks.md) (AppMeasurement) oder [`clickCollectionEnabled`](trackdownloadlinks.md) (Web SDK) aktiviert ist und ein Besucher auf einen Link klickt, prüft AppMeasurement die URL des Links auf Dateityperweiterungen. Wenn die Link-URL einen übereinstimmenden Dateityp enthält, wird automatisch eine Bildanforderung für einen Download-Link gesendet.

Verwenden Sie `linkDownloadFileTypes`, um anzupassen, welche Dateierweiterungen Sie als Download-Links zählen möchten.

>[!NOTE]
>
>Nur tatsächliche Klicks werden automatisch verfolgt. Die folgenden Link-Typen werden nicht automatisch verfolgt:
>
>* Datei-Downloads, die beim Laden einer Seite automatisch eingeleitet werden
>* Downloads, die nach einer Umleitung ausgelöst werden
>* Mit der rechten Maustaste klicken und „Ziel speichern unter...“ auswählen
>* Links, die JavaScript verwenden, wie z. B. `javascript:openLink()`
>
>Für diese Download-Typen können Sie manuell einen [`link tracking`](../functions/tl-method.md)-Aufruf senden.

Wenn ein geklickter Link sowohl den Kriterien für Exitlinks als auch für Downloadlinks entspricht, hat der Downloadlink-Typ Priorität.

## Herunterladen des Link-Qualifizierers mithilfe der Web-SDK-Erweiterung

Das Textfeld [!UICONTROL Downloadlink]Qualifizierer“ verwendet Regex, um zu bestimmen, ob ein geklickter Link als Download-Link gilt.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Wechseln Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter {4 **[!UICONTROL Adobe Experience Platform Web SDK]** auf die Schaltfläche Konfigurieren].[!UICONTROL 
1. Legen [!UICONTROL  unter „Datenerfassung] den gewünschten Wert im Textfeld **[!UICONTROL Link-Qualifizierer herunterladen]** fest.

## Download-Link-Qualifizierer bei der manuellen Implementierung der Web-SDK

[Konfigurieren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=de) der SDK mithilfe von [`downloadLinkQualifier`](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/track-links.html?lang=de#automaticLinkTracking). Das Feld verwendet Regex für die angeklickte URL, um zu ermitteln, ob es sich um einen gültigen Download-Link handelt. Wenn `downloadLinkQualifier` nicht definiert ist, wird der Standardwert auf `\\.(exe|zip|wav|mp3|mov|mpg|avi|wmv|pdf|doc|docx|xls|xlsx|ppt|pptx)$` festgelegt.

```json
alloy("configure", {
  "downloadLinkQualifier": "\\.(exe|zip|wav|mp3|mov|mpg|avi|wmv|pdf|doc|docx|xls|xlsx|ppt|pptx)$"
});
```

## Herunterladen von Erweiterungen mit der Adobe Analytics-Erweiterung

Download-Erweiterungen sind eine Liste von Dateierweiterungen, in der Sie bei der Konfiguration der Adobe Analytics-Erweiterung in einem Feld unter dem Akkordeon [!UICONTROL Linktracking] weitere Erweiterungen hinzufügen können.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
4. Erweitern Sie das Akkordeon [!UICONTROL Linktracking], wodurch das Feld **[!UICONTROL Download-Erweiterungen]** angezeigt wird.

Fügen Sie der Liste Dateierweiterungen hinzu, indem Sie Text in das Feld eingeben und auf **[!UICONTROL Hinzufügen]** klicken. Entfernen Sie Dateierweiterungen aus der Liste, indem Sie auf das entsprechende **X“**.

## s.linkDownloadFileTypes auf AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.linkDownloadFileTypes`-Variable ist eine Zeichenfolge aus kommagetrennten Dateierweiterungen. Verwenden Sie keine Leerzeichen.

Wenn diese Variable nicht definiert ist, funktioniert das automatische Tracking von Downloadlinks nicht (auch wenn [`trackDownloadLinks`](trackdownloadlinks.md) den Wert `true` aufweist).

```js
s.linkDownloadFileTypes = "doc,docx,eps,jpg,png,svg,xls,ppt,pptx,pdf,xlsx,tab,csv,zip,txt,vsd,vxd,xml,js,css,rar,exe,wma,mov,avi,wmv,mp3,wav,m4v";
```
