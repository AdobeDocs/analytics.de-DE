---
title: eVar (Variable)
description: Benutzerdefinierte Variablen, die Sie in Ihrer Implementierung verwenden können.
feature: Variables
exl-id: f89457b2-4186-4276-8637-9992070e3a73
role: Admin, Developer
source-git-commit: 12347957a7a51dc1f8dfb46d489b59a450c2745a
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 92%

---

# eVar

*Auf dieser Hilfeseite wird die Implementierung von eVars beschrieben. Informationen dazu, wie eVars als Dimension funktionieren, finden Sie unter [eVars](/help/components/dimensions/evar.md) im Komponenten-Benutzerhandbuch.*

eVars sind benutzerdefinierte Variablen, die Sie beliebig verwenden können. Wenn Sie über ein [Lösungsdesigndokument](/help/implement/prepare/solution-design.md) verfügen, werden die meisten für Ihr Unternehmen spezifischen Dimensionen als eVars angezeigt. Standardmäßig bleiben eVars über den Treffer hinaus bestehen, auf den sie gesetzt wurden. Sie können ihre Gültigkeit und Zuordnung unter [Konversionsvariablen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-var-admin.md) in den Report Suite-Einstellungen anpassen.

Die Anzahl der verfügbaren eVars hängt von Ihrem Vertrag mit Adobe ab. Es sind bis zu 250 eVars verfügbar, wenn Ihr Vertrag mit Adobe dies unterstützt.

## Einrichten von eVars in den Report Suite-Einstellungen

Bevor Sie eVars in Ihrer Implementierung verwenden, stellen Sie sicher, dass Sie jede eVar in den Report Suite-Einstellungen konfigurieren. Weitere Informationen finden Sie im Admin-Handbuch unter [Konversionsvariablen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-var-admin.md).

## eVars, die das Web SDK verwenden

eVars werden den folgenden Variablen zugeordnet:

* [XDM-Objekt](/help/implement/aep-edge/xdm-var-mapping.md): `xdm._experience.analytics.customDimensions.eVars.eVar1` bis `xdm._experience.analytics.customDimensions.eVars.eVar250`
* [Datenobjekt](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.eVar1` bis `data.__adobe.analytics.eVar250` oder `data.__adobe.analytics.v1` bis `data.__adobe.analytics.v250`

## eVars, die die Adobe Analytics-Erweiterung verwenden

Sie können eVars entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Setzen Sie die Dropdownliste [!UICONTROL Erweiterung] auf Adobe Analytics und den Aktionstyp [!UICONTROL 3} auf [!UICONTROL Variablen festlegen].]
6. Suchen Sie den Abschnitt [!UICONTROL eVars].

Sie können eine eVar auf einen Wert oder ein Datenelement festlegen. Sie können den Wert auch aus einer anderen Analytics-Variablen kopieren.

## s.eVar1 – s.eVar250 in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Jede eVar ist eine Zeichenfolge, die für Ihr Unternehmen spezifische benutzerdefinierte Werte enthält. Die maximale Länge beträgt 255 Byte. Werte, die länger als 255 Byte sind, werden beim Senden an Adobe automatisch abgeschnitten.

```js
s.eVar1 = "Example custom value";
```

## Zähler-eVars

eVar-Werte enthalten normalerweise einen Zeichenfolgenwert. Sie können eVars jedoch so konfigurieren, dass sie stattdessen einen Zähler enthalten. Sie möchten beispielsweise die Anzahl der internen Suchen zählen, die vor einem Kauf durchgeführt wurden. Anstatt einen Textwert festzulegen, verwenden Sie folgende Syntax:

```js
// Increment a counter eVar by 1
s.eVar1 = "+1";

// Increment a counter eVar by 12.49
s.eVar1 = "+12.49";
```

Wenn mehr als zwei Dezimalstellen angegeben sind, wird die Zähler-eVar auf zwei Dezimalstellen gerundet. Ein eVar-Zähler kann keine negativen Zahlen enthalten.

>[!IMPORTANT]
>
>Bevor Sie Zähler-eVars verwenden können, müssen Sie eVars in der Admin Console zuerst in „Zähler“ konfigurieren. Weitere Informationen finden Sie im Admin-Handbuch unter [Konversionsvariablen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-var-admin.md).
