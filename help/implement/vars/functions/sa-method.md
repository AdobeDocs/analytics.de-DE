---
title: sa
description: Ändern Sie die Report Suite jederzeit in Ihrer Implementierung.
feature: Variables
exl-id: 524857a7-c820-4985-86c7-fcf21a0809bd
role: Admin, Developer
source-git-commit: bfafc1f8eddf82b34fb45e3d6197213f0cee0d97
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 42%

---

# sa

Mit der `sa()`-Methode können Sie eine Report Suite jederzeit auf der Seite dynamisch ändern. Wenn Sie Daten ohne Seitenneuladung an andere Report Suites senden möchten, können Sie diese Methode verwenden.

## Umgang mit Report Suites mit der Web-SDK

Web SDK sendet Daten an einen bestimmten Datenstrom, der Daten an die gewünschte(n) Analytics Report Suite(s) weiterleitet. Ein einzelner Datenstrom kann Daten an mehrere Report Suites weiterleiten. Dieser Abschnitt gilt sowohl für die Web SDK-Erweiterung als auch für die manuelle Implementierung der Web SDK.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken **[!UICONTROL links auf]** Datenströme“.
1. Klicken Sie auf den gewünschten Datenstrom oder klicken Sie auf **[!UICONTROL Neuer Datenstrom]**.
1. Klicken Sie **[!UICONTROL Service hinzufügen]** und wählen Sie dann **[!UICONTROL Adobe Analytics]** aus.
1. Geben Sie die gewünschte Report Suite-ID ein. Wenn Sie dieselben Daten an mehrere Report Suites senden möchten, klicken Sie auf **[!UICONTROL Report Suite hinzufügen]**.
1. Nachdem alle gewünschten Report Suites eingegeben wurden, klicken Sie auf **[!UICONTROL Speichern]**.

## Festlegen des gewünschten Datenstroms mithilfe der Web SDK-Erweiterung

Die Web SDK-Erweiterung bietet eine Dropdown-Liste für jeden Datenstrom für jede Umgebung. Alternativ können Sie die Datenstrom-ID manuell eingeben.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Wechseln Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter &lbrace;4 **[!UICONTROL Adobe Experience Platform Web SDK]** auf die Schaltfläche Konfigurieren.
1. Wählen [!UICONTROL &#x200B; unter &#x200B;] den gewünschten Datenstrom in der Dropdown-Liste für jede Umgebung aus.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Manuelles Festlegen des gewünschten Datenstroms durch Implementieren der Web-SDK

Legen Sie die `datastreamId`-Konfigurationsvariable auf die Datenstrom-ID fest. Die Datenstrom-ID befindet sich auf der rechten Seite, wenn Sie einen Datenstrom in der Datenerfassung von Adobe Experience Platform anzeigen.

```js
alloy("configure", {
  datastreamId: "example-a01f-4458-8cec-ef61de241c93",
  orgId: "ADB3LETTERSANDNUMBERS@AdobeOrg"
});
```

Weitere Informationen [ Sie in der ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=de) zu Web SDK unter „Konfigurieren der Web-SDK&quot;.

## Ändern der Report Suite mithilfe der Adobe Analytics-Erweiterung

Es gibt keine flexible Möglichkeit, die Report Suite in der Oberfläche zu ändern. Sie können die Report Suite bei der Konfiguration der Adobe Analytics-Erweiterung unter dem Akkordeon [!UICONTROL Bibliotheksverwaltung] festlegen. Sie können die Report Suite jedoch nicht mithilfe von Regeln ändern oder aktualisieren. Wenn Sie die Report Suite-Werte nach dem Festlegen aktualisieren möchten, verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.sa() in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Rufen Sie die `s.sa()`-Methode auf, um die Ziel-Report Suite zu ändern. Das einzige Argument ist eine Zeichenfolge, die eine Report Suite-ID oder mehrere durch ein Komma getrennte Report Suite-IDs enthält. Das Argument der Report Suite-ID ist erforderlich. Verwenden Sie keine Leerzeichen im Zeichenfolgenargument.

```js
s.sa("examplersid");
```

Sie können beispielsweise die Report Suite ändern, wenn der Benutzer eine bestimmte Aktion auf Ihrer Site durchführt.

```js
// Instantiate the tracking object
var s = s_gi("examplersid");

// If the visitor plays a video, you can add a video report suite
s.sa("examplersid,videorsid");

// Then send an image request
s.t();
```
