---
title: dynamicVariablePrefix
description: Ermöglicht die Anpassung der Zeichenfolge zur Identifizierung dynamischer Variablen.
feature: Variables
exl-id: fe208723-0cf2-4899-be7a-8f23c6501c11
role: Admin, Developer
source-git-commit: 12347957a7a51dc1f8dfb46d489b59a450c2745a
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 70%

---

# dynamicVariablePrefix

Dynamische Variablen sind ein Kurzkonzept, mit dem Sie Werte von einer Variablen in eine andere kopieren können. Sie sind für lange Variablenwerte nützlich, da sie dazu beitragen, die URL-Länge einer Bildanforderung zu verkürzen. Weitere Informationen zu diesem Konzept finden Sie unter [Dynamische Variablen](../page-vars/dynamic-variables.md).

Dynamische Variablen verwenden standardmäßig das Präfix `D=`. Mit der `dynamicVariablePrefix`-Variablen können Sie die Zeichenfolge zur Identifizierung dynamischer Variablen anpassen. Dabei ist die Groß-/Kleinschreibung zu beachten.

## Dynamisches Variablenpräfix mit dem Web SDK

Das Web SDK verwendet keine dynamische Variablenformatierung. Stattdessen können Sie die Datastream-Zuordnung verwenden, um mehrere Zielfelder mit einem einzigen Quellfeld zu füllen. Siehe [Dynamische Variablen mit dem Web SDK](../page-vars/dynamic-variables.md#dynamic-variables-using-the-web-sdk) für weitere Informationen.

Wenn Sie Daten direkt an Adobe Analytics senden, ohne einem Schema zu entsprechen, wird die folgende Variable verwendet:

* [Datenobjekt](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.dynamicVariablePrefix`

## Dynamisches Variablenpräfix mit der Adobe Analytics-Erweiterung

„Dynamisches Variablenpräfix“ ist ein Feld unter dem Akkordeon [!UICONTROL Globale Variablen] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
1. Erweitern Sie das Akkordeon [!UICONTROL Globale Variablen], wodurch das Feld [!UICONTROL Dynamisches Variablenpräfix] angezeigt wird.

Dieses Feld enthält standardmäßig `D=`. Sie können den Wert ändern, wenn Sie ein anderes Präfix für dynamische Variablen verwenden möchten. Sie können jeden gewünschten Wert verwenden, sofern er mit der Zeichencodierung auf Ihrer Website übereinstimmt.

## s.dynamicVariablePrefix in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.dynamicVariablePrefix`-Variable ist eine Zeichenfolge, die eine beliebige Folge von Zeichen enthalten kann. Wenn diese Variable nicht definiert ist, verwendet AppMeasurement standardmäßig die Zeichenfolge `D=`.

```js
// An example that changes the dynamic variable prefix
s.dynamicVariablePrefix="..";

// This eVar uses the above customized dynamic variable prefix to set eVar to page URL
s.eVar1="..g";
```
