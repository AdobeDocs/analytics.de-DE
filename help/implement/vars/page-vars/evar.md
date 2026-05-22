---
title: eVar (Variable)
description: Benutzerdefinierte Variablen, die Sie in Ihrer Implementierung verwenden können.
feature: Appmeasurement Implementation
exl-id: f89457b2-4186-4276-8637-9992070e3a73
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/7GS-wW0K3hh-uZ4fTi8yajH9wgFGBW-BQjT9m1mhXuU'
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
source-wordcount: 409
ht-degree: 96%

---

# eVar

*Auf dieser Hilfeseite wird die Implementierung von eVars beschrieben. Informationen dazu, wie eVars als Dimension funktionieren, finden Sie unter [eVars](/help/components/dimensions/evar.md) im Komponenten-Benutzerhandbuch.*

eVars sind benutzerdefinierte Variablen, die Sie beliebig verwenden können. Wenn Sie über ein [Lösungsdesigndokument](/help/implement/prepare/solution-design.md) verfügen, werden die meisten für Ihr Unternehmen spezifischen Dimensionen als eVars angezeigt. Standardmäßig bleiben eVars über den Treffer hinaus bestehen, auf den sie gesetzt wurden. Sie können ihre Gültigkeit und Zuordnung unter [Konversionsvariablen](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/conversion-var-admin.md) in den Report Suite-Einstellungen anpassen.

Die Anzahl der verfügbaren eVars hängt von Ihrem Vertrag mit Adobe ab. Es sind bis zu 250 eVars verfügbar, wenn Ihr Vertrag mit Adobe dies unterstützt.

## Einrichten von eVars in den Report Suite-Einstellungen

Bevor Sie eVars in Ihrer Implementierung verwenden, stellen Sie sicher, dass Sie jede eVar in den Report Suite-Einstellungen konfigurieren. Weitere Informationen finden Sie im Admin-Handbuch unter [Konversionsvariablen](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/conversion-var-admin.md).

## eVars, die das Web SDK verwenden

eVars werden den folgenden Variablen zugeordnet:

* [XDM-Objekt](/help/implement/aep-edge/xdm-var-mapping.md): `xdm._experience.analytics.customDimensions.eVars.eVar1` zu `xdm._experience.analytics.customDimensions.eVars.eVar250`
* [Datenobjekt](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.eVar1` zu `data.__adobe.analytics.eVar250` oder `data.__adobe.analytics.v1` zu `data.__adobe.analytics.v250`

## eVars, die die Adobe Analytics-Erweiterung verwenden

Sie können eVars entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und legen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen] fest.
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
>Bevor Sie Zähler-eVars verwenden können, müssen Sie eVars in der Admin Console zuerst in „Zähler“ konfigurieren. Weitere Informationen finden Sie im Admin-Handbuch unter [Konversionsvariablen](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/conversion-var-admin.md).
