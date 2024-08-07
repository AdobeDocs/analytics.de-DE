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

## Umgang mit Report Suites mit dem Web SDK

Das Web SDK sendet Daten an einen bestimmten Datastream, der Daten an die gewünschten Analytics Report Suites weiterleitet. Ein einzelner Datastream kann Daten an mehrere Report Suites weiterleiten. Dieser Abschnitt gilt sowohl für die Web SDK-Erweiterung als auch für die manuelle Implementierung des Web SDK.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie links auf **[!UICONTROL Datastreams]**.
1. Klicken Sie auf den gewünschten Datastream oder klicken Sie auf **[!UICONTROL Neuer Datastream]**.
1. Klicken Sie auf **[!UICONTROL Dienst hinzufügen]** und wählen Sie dann **[!UICONTROL Adobe Analytics]** aus.
1. Geben Sie die gewünschte Report Suite-ID ein. Wenn Sie dieselben Daten an mehrere Report Suites senden möchten, klicken Sie auf **[!UICONTROL Report Suite hinzufügen]**.
1. Sobald alle gewünschten Report Suites eingegeben wurden, klicken Sie auf **[!UICONTROL Speichern]**.

## Festlegen des gewünschten Datenspeichers mithilfe der Web SDK-Erweiterung

Die Web SDK-Erweiterung stellt für jede Umgebung eine Dropdown-Liste für Datastream bereit. Alternativ können Sie die Datastream-ID manuell eingeben.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter [!UICONTROL Adobe Experience Platform Web SDK] auf die Schaltfläche **[!UICONTROL Konfigurieren]** .
1. Wählen Sie unter [!UICONTROL Datastreams] den gewünschten Datastream in der Dropdown-Liste für jede Umgebung aus.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Festlegen des gewünschten Datastreams zur manuellen Implementierung des Web SDK

Stellen Sie die Konfigurationsvariable `datastreamId` auf die Datastream-ID ein. Die Datastream-ID befindet sich rechts beim Anzeigen eines Datastreams in der Adobe Experience Platform-Datenerfassung.

```js
alloy("configure", {
  datastreamId: "example-a01f-4458-8cec-ef61de241c93",
  orgId: "ADB3LETTERSANDNUMBERS@AdobeOrg"
});
```

Weitere Informationen finden Sie unter [Web SDK konfigurieren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=de) in der Web SDK-Dokumentation.

## Report Suite mithilfe der Adobe Analytics-Erweiterung ändern

Es gibt keine flexible Möglichkeit, die Report Suite in der Oberfläche zu ändern. Sie können die Report Suite bei der Konfiguration der Adobe Analytics-Erweiterung unter dem Akkordeon [!UICONTROL Bibliotheksverwaltung] festlegen. Sie können die Report Suite jedoch nicht mithilfe von Regeln ändern oder aktualisieren. Wenn Sie die Report Suite-Werte nach dem Festlegen aktualisieren möchten, verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.sa() in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Rufen Sie die `s.sa()`-Methode auf, um die Ziel-Report Suite zu ändern. Das einzige Argument ist eine Zeichenfolge, die eine Report Suite-ID oder mehrere durch ein Komma getrennte Report Suite-IDs enthält. Das Argument der Report Suite-ID ist erforderlich. Verwenden Sie keine Leerzeichen im Zeichenfolgenargument.

```js
s.sa("examplersid");
```

Sie können beispielsweise die Report Suite ändern, wenn der Benutzer eine bestimmte Aktion auf Ihrer Site ausführt.

```js
// Instantiate the tracking object
var s = s_gi("examplersid");

// If the visitor plays a video, you can add a video report suite
s.sa("examplersid,videorsid");

// Then send an image request
s.t();
```
