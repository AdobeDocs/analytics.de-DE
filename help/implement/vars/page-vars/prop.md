---
title: prop
description: Benutzerdefinierte Variablen, die Sie in Ihrer Implementierung verwenden können.
feature: Appmeasurement Implementation
exl-id: 0d0ff8cd-1d8c-4263-866d-e51ad66148b0
role: Admin, Developer
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 85%

---

# prop

*Auf dieser Hilfeseite wird die Implementierung von Props beschrieben. Informationen dazu, wie Props als Dimension funktionieren, finden Sie unter [Props](/help/components/dimensions/prop.md) im Komponenten-Benutzerhandbuch.*

Props sind benutzerdefinierte Variablen, die Sie beliebig verwenden können. Sie bleiben nicht über den von ihnen festgelegten Treffer hinaus bestehen.

>[!TIP]
>
>Adobe empfiehlt in den meisten Fällen die Verwendung von [eVars](evar.md). In früheren Versionen von Adobe Analytics hatten Props und eVars Vorteile und Nachteile. Adobe hat eVars jedoch so weit verbessert, dass sie jetzt fast alle Anwendungsfälle für Props erfüllen.

Wenn Sie über ein [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) verfügen, können Sie diese benutzerspezifischen Dimensionen den unternehmensspezifischen Werten zuordnen. Die Anzahl der verfügbaren Props hängt von Ihrem Vertrag mit Adobe ab. Es sind bis zu 75 Props verfügbar, wenn Ihr Vertrag mit Adobe dies unterstützt.

## Props, die das Web SDK verwenden

Props sind den folgenden Variablen zugeordnet:

* [XDM-](/help/implement/aep-edge/xdm-var-mapping.md): `xdm._experience.analytics.customDimensions.props.prop1` - `xdm._experience.analytics.customDimensions.props.prop75` - Listen-Props werden in einem [separaten Satz von Feldern) &#x200B;](#list-props-web-sdk).
* [Datenobjekt](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.prop1` - `data.__adobe.analytics.prop75`; oder `data.__adobe.analytics.c1` - `data.__adobe.analytics.c75` - Listen-Props sind in diesen Feldern enthalten.

## Props, die die Adobe Analytics-Erweiterung verwenden

Sie können Props entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Legen Sie [!UICONTROL &#x200B; Dropdown]Liste „Erweiterung“ auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen] fest.
6. Suchen Sie den Abschnitt [!UICONTROL Props].

Sie können eine Prop auf einen Wert oder ein Datenelement festlegen. Sie können den Wert auch aus einer anderen Analytics-Variablen kopieren.

## s.prop1 – s.prop75 in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Jede Prop-Variable ist eine Zeichenfolge, die für Ihr Unternehmen spezifische benutzerdefinierte Werte enthält. Die maximale Länge beträgt 100 Byte. Werte, die länger als 100 Byte sind, werden beim Senden an Adobe automatisch abgeschnitten.

```js
s.prop1 = "Example custom value";
```

## Listen-Props

Listen-Props sind eine Einstellung, die auf Props angewendet wird, mit denen die Variable mehrere Werte im selben Treffer enthalten kann. Wenn diese Einstellung nicht aktiviert ist oder das falsche Trennzeichen verwendet wird, wird die Variable als einzelner Wert behandelt.

### Konfigurieren von Listen-Props

Aktivieren Sie Listen-Props in [Traffic-Variablen](/help/admin/tools/manage-rs/edit-settings/c-traffic-variables/traffic-var.md) unter den Report Suite-Einstellungen. Vergewissern Sie sich, dass das gewünschte Trennzeichen richtig konfiguriert ist. Adobe stellt kein Standardtrennzeichen bereit.

>[!TIP]
>
>Bei Implementierungen werden häufig Trennzeichen wie Komma (`,`), Doppelpunkt (`:`), Semikolon (`;`) oder der senkrechte Strich (`|`) verwendet. Sie können jedes beliebige nicht-erweiterte ASCII-Trennzeichen verwenden, das am besten zu Ihrer Implementierung passt.

### Festlegen von Listen-Props mit dem Web SDK {#list-props-web-sdk}

Bei Verwendung des [**XDM-**](/help/implement/aep-edge/xdm-var-mapping.md)) werden Listen-Props `xdm._experience.analytics.customDimensions.listProps.prop1.values[]` - `xdm._experience.analytics.customDimensions.listProps.prop75.values[]` zugeordnet. Das Web SDK verwendet automatisch das richtige Trennzeichen, das unter den Report Suite-Einstellungen aufgeführt ist. Wenn Sie das Trennzeichen im XDM-Feld festlegen (z. B. `xdm._experience.analytics.customDimensions.props.prop1.delimiter`), wird das Trennzeichen überschrieben, das automatisch aus den Report Suite-Einstellungen abgerufen wird, was zu einer falschen Analyse der Listen-Prop-Zeichenfolge führen kann.

Bei Verwendung des [**Datenobjekts**](/help/implement/aep-edge/data-var-mapping.md) verwenden Listen-Props dieselben Felder wie Standard-Props und folgen der AppMeasurement-Syntax.

### Festlegen von Listen-Props mit der Adobe Analytics-Erweiterung und AppMeasurement

Sobald Sie Listen-Props in den Report Suite-Einstellungen mit dem gewünschten Trennzeichen konfigurieren, gibt es außer der Verwendung des Trennzeichens keine weiteren Implementierungsunterschiede.

```js
// List prop delimited with a comma
s.prop1 = "value1,value2,value3";
```

>[!IMPORTANT]
>
>Listen-Props unterliegen weiterhin der maximalen Länge von 100 Byte. Listen-Props können diese Grenze leichter erreichen und abgeschnitten werden, da sie mehrere Werte enthalten können. Erwägen Sie die Verwendung von Abkürzungen oder die Verkürzung von Werten, wenn Sie diesen Grenzwert von 100 Byte erreichen.

Wenn Sie denselben Wert mehr als einmal in einer Listen-Prop festlegen, werden diese Werte in Berichten dedupliziert. Analysis Workspace zählt die Anzahl der Treffer, bei denen ein Wert angezeigt wird, und nicht, wie oft ein Wert in Daten vorhanden ist.
