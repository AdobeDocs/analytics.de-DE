---
title: Util.cookieRead
description: Ruft den Wert aus einem Cookie ab.
feature: Appmeasurement Implementation
exl-id: b05b628c-bae6-4dba-bc1d-6a1ab56e3660
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 72%

---

# Util.cookieRead

Cookies können Informationen über Seiten in derselben Domain hinweg speichern und abrufen. Verwenden Sie die `Util.cookieRead()`-Methode, um einen Wert aus einem Cookie abzurufen.

## Lesen von Cookies mithilfe der Adobe Analytics-Erweiterung und der Web SDK-Erweiterung

Sie können Cookies lesen, indem Sie Werte in Datenelementen festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Datenelemente] und klicken Sie dann auf das gewünschte Datenelement (oder erstellen Sie ein Datenelement).
4. Legen Sie [!UICONTROL  Dropdown]Liste Erweiterung auf **[!UICONTROL Core]** und den [!UICONTROL Datenelementtyp] auf **[!UICONTROL Cookie]** fest.
5. Geben Sie den Namen des Cookies in das Textfeld ein.

Der Wert des Cookies wird im Datenelement gespeichert. Anschließend können Sie das Datenelement in Regeln referenzieren, um die gewünschten Variablen zuzuweisen.

## s.Util.cookieRead() in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Rufen Sie die `s.Util.cookieRead()`-Methode auf, um einen gewünschten Cookie-Wert zu lesen. Das einzige Argument ist eine Zeichenfolge, die erforderlich ist. Diese Methode gibt eine Zeichenfolge zurück, die den Cookie-Wert enthält. Wenn die Cookies nicht vorhanden sind, wird eine leere Zeichenfolge zurückgegeben.

```js
// Reads the value set in the cookie named 'example' and assigns the value to eVar1
s.eVar1 = s.Util.cookieRead("example");
```
