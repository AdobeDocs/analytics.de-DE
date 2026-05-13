---
title: Util.getQueryParam
description: Gibt den Wert eines Abfragezeichenfolgenparameters zurück.
feature: Appmeasurement Implementation
exl-id: d29d6cd9-f85f-475b-a7a8-73785aa4ae7b
role: Admin, Developer
TQID: https://experienceleague.adobe.com/hPNA1jq7fyFOlvqNJ3dVZeSvBeCCfWzyH5BdhQDRZV8
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 274
ht-degree: 79%

---

# Util.getQueryParam

Abfragezeichenfolgenparameter in einer Browser-URL enthalten häufig wichtige Daten für Analytics. Verwenden Sie die `Util.getQueryParam()`-Methode, um Daten aus der Abfragezeichenfolge abzurufen.

## Abrufen von Abfragezeichenfolgenparameterdaten mithilfe der Adobe Analytics-Erweiterung und der Web SDK-Erweiterung

Sie können Abfragezeichenfolgenparameterdaten abrufen, indem Sie Werte in Datenelementen festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Datenelemente] und klicken Sie dann auf das gewünschte Datenelement (oder erstellen Sie ein Datenelement).
4. Legen Sie [!UICONTROL  Dropdown]Liste „Erweiterung“ auf **[!UICONTROL Core]** und den [!UICONTROL Datenelementtyp] auf **[!UICONTROL Abfragezeichenfolgenparameter]**.
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
