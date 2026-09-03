---
title: Util.cookieRead
description: Ruft den Wert aus einem Cookie ab.
feature: Appmeasurement Implementation
exl-id: b05b628c-bae6-4dba-bc1d-6a1ab56e3660
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/puEimpy5b-hdgo186YqHzsgxC-LGKPluxN5mVdxFer4'
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
source-wordcount: 184
ht-degree: 72%

---

# Util.cookieRead

Cookies können Informationen über Seiten in derselben Domain hinweg speichern und abrufen. Verwenden Sie die `Util.cookieRead()`-Methode, um einen Wert aus einem Cookie abzurufen.

## Lesen von Cookies mithilfe der Adobe Analytics-Erweiterung und der Web SDK-Erweiterung

Sie können Cookies lesen, indem Sie Werte in Datenelementen festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Datenelemente] und klicken Sie dann auf das gewünschte Datenelement (oder erstellen Sie ein Datenelement).
4. Legen Sie [!UICONTROL &#x200B; Dropdown]Liste Erweiterung auf **[!UICONTROL Core]** und den [!UICONTROL Datenelementtyp] auf **[!UICONTROL Cookie]** fest.
5. Geben Sie den Namen des Cookies in das Textfeld ein.

Der Wert des Cookies wird im Datenelement gespeichert. Anschließend können Sie das Datenelement in Regeln referenzieren, um die gewünschten Variablen zuzuweisen.

## s.Util.cookieRead() in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Rufen Sie die `s.Util.cookieRead()`-Methode auf, um einen gewünschten Cookie-Wert zu lesen. Das einzige Argument ist eine Zeichenfolge, die erforderlich ist. Diese Methode gibt eine Zeichenfolge zurück, die den Cookie-Wert enthält. Wenn die Cookies nicht vorhanden sind, wird eine leere Zeichenfolge zurückgegeben.

```js
// Reads the value set in the cookie named 'example' and assigns the value to eVar1
s.eVar1 = s.Util.cookieRead("example");
```
