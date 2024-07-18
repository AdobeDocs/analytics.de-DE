---
title: Util.getQueryParam
description: Gibt den Wert eines Abfragezeichenfolgenparameters zurück.
feature: Variables
exl-id: d29d6cd9-f85f-475b-a7a8-73785aa4ae7b
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 79%

---

# Util.getQueryParam

Abfragezeichenfolgenparameter in einer Browser-URL enthalten häufig wichtige Daten für Analytics. Verwenden Sie die `Util.getQueryParam()`-Methode, um Daten aus der Abfragezeichenfolge abzurufen.

## Abrufen von Abfragezeichenfolgenparameterdaten mithilfe der Adobe Analytics-Erweiterung und der Web SDK-Erweiterung

Sie können Abfragezeichenfolgenparameterdaten abrufen, indem Sie Werte in Datenelementen festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Datenelemente] und klicken Sie dann auf das gewünschte Datenelement (oder erstellen Sie ein Datenelement).
4. Setzen Sie die Dropdownliste [!UICONTROL Erweiterung] auf **[!UICONTROL Core]** und den Datenelementtyp [!UICONTROL  auf **[!UICONTROL Abfragezeichenfolgenparameter]**.]
5. Geben Sie den Abfragezeichenfolgenparameter in das Textfeld ein.

Der Wert des Abfragezeichenfolgenparameters wird im Datenelement gespeichert. Anschließend können Sie das Datenelement in Regeln referenzieren, um die gewünschten Variablen zuzuweisen.

## s.Util.getQueryParam() in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Rufen Sie die `s.Util.getQueryParam()`-Methode auf, um einen Abfragezeichenfolgenwert aus der Browser-URL abzurufen. Das Zeichenfolgenargument, das einen Abfragezeichenfolgenparameter enthält, ist erforderlich. Diese Methode gibt eine Zeichenfolge zurück, die Sie Analytics-Variablen zuweisen können:

```js
s.eVar1 = s.Util.getQueryParam("cid");
```

Ein zweites optionales Argument ermöglicht es Ihnen, die Zeichenfolge anzugeben, die auf Abfragezeichenfolgenparameter überprüft werden soll. Standardmäßig überprüft das Dienstprogramm die Browser-URL.

```js
// Search a custom string for query string parameter
var customString = "https://example.com?q=search";

// eVar1 is set to "search"
s.eVar1 = s.Util.getQueryParam("q",customString);
```

Ein drittes optionales Argument ermöglicht es Ihnen, das Trennzeichen für die Abfragezeichenfolge anzupassen. Der Standardwert lautet `&`. Sie können diesen Wert ändern, wenn Ihre Abfragezeichenfolge ein anderes Trennzeichen verwendet.

```js
var customString = "https://example.com?q1=value1;q2=value2;q3=value3";

// eVar1 is set to "value2"
s.eVar1 = s.Util.getQueryParam("q2",customString,";");
```

>[!TIP]
>
>Ein ähnliches Plug-in namens [`s.getQueryParam`](../plugins/getqueryparam.md) ist verfügbar. Dieses Plug-in enthält erweiterte Funktionen, ist aber auch komplexer und standardmäßig nicht in AppMeasurement enthalten.
