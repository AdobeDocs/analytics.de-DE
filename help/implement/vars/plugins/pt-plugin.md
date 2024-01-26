---
title: pt
description: Führt eine Funktion für eine Liste von Variablen aus.
feature: Variables
exl-id: 2ab24a8e-ced3-43ea-bdb5-7c39810e4102
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 88%

---

# Adobe-Plug-in: pt

{{plug-in}}

Das `pt`-Plug-in führt eine Funktion oder Methode für eine Liste von Analytics-Variablen aus. Beispielsweise können Sie die [`clearVars`](../functions/clearvars.md)-Methode selektiv für mehrere Variablen ausführen, ohne die Methode jedes Mal manuell aufzurufen. Mehrere andere Plug-ins sind auf diesen Code angewiesen, um korrekt zu funktionieren. Dieses Plug-in ist nicht erforderlich, wenn Sie nicht gleichzeitig eine bestimmte Funktion für mehrere Analytics-Variablen ausführen müssen oder wenn Sie keine abhängigen Plug-ins verwenden.

## Installieren des Plug-ins mit der Web SDK- oder Web SDK-Erweiterung

Dieses Plug-in wird noch nicht für die Verwendung im Web SDK unterstützt.

## Installieren des Plug-ins mit der Adobe Analytics-Erweiterung

Adobe bietet eine Erweiterung, mit der Sie am häufigsten verwendete Plug-ins mit Adobe Analytics verwenden können.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann auf die Schaltfläche [!UICONTROL Katalog].
1. Installieren und Veröffentlichen der Erweiterung [!UICONTROL Common Analytics Plugins].
1. Wenn Sie dies noch nicht getan haben, erstellen Sie eine Regel mit der Bezeichnung „Plug-ins initialisieren“ mit der folgenden Konfiguration:
   * Bedingung: Keine
   * Ereignis: Core – Bibliothek geladen (Seitenanfang)
1. Fügen Sie der obenstehenden Regel eine Aktion mit der folgenden Konfiguration hinzu:
   * Erweiterung: Common Analytics Plugins
   * Aktionstyp: pt initialisieren
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor

Wenn Sie die Plug-in-Erweiterung &quot;Common Analytics Plugins&quot;nicht verwenden möchten, können Sie den Editor für benutzerdefinierten Code verwenden.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter der Erweiterung „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
1. Erweitern Sie das Akkordeon [!UICONTROL Tracking mit benutzerdefiniertem Code konfigurieren], wodurch die Schaltfläche [!UICONTROL Editor öffnen] angezeigt wird.
1. Öffnen Sie den Editor für benutzerdefinierten Code und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen an der Analytics-Erweiterung.

## Installieren des Plug-ins mit AppMeasurement

Kopieren Sie den folgenden Code und fügen Sie ihn an beliebiger Stelle in der AppMeasurement Datei ein, nachdem das Analytics-Tracking-Objekt instanziiert wurde (unter Verwendung von [`s_gi`](../functions/s-gi.md)). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: pt v3.0 */
function pt(l,de,cf,fa){var b=l,d=de,f=cf,g=fa;if("-v"===b)return{plugin:"pt",version:"3.0"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var c;a<window.s_c_il.length;a++)if(c=window.s_c_il[a],c._c&&"s_c"===c._c){a=c;break a}}a=void 0}if("undefined"!==typeof a&&(a.contextData.pt="3.0",b&&a[f])){b=b.split(d||",");d=b.length;for(var e=0;e<d;e++)if(c=a[f](b[e],g))return c}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `pt`-Methode verwendet die folgenden Argumente:

* **`l`** (erforderlich, Zeichenfolge): Eine Liste von Variablen, für die die im `cf`-Argument enthaltene Funktion ausgeführt werden kann.
* **`de`** (optional, Zeichenfolge): Das Trennzeichen, das die Liste der Variablen im `l`-Argument trennt. Der Standardwert ist ein Komma (`,`).
* **`cf`** (erforderlich, Zeichenfolge): Der Name der Callback-Funktion im AppMeasurement-Objekt, die für jede der im `l`-Argument enthaltenen Variablen aufgerufen werden soll.
* **`fa`** (optional, Zeichenfolge): Wenn die Funktion im `cf`-Argument bei Ausführung zusätzliche Argumente benötigt, schließen Sie sie hier ein. Die Standardeinstellung ist `undefined`.

Der Aufruf dieser Methode gibt einen Wert zurück, wenn die Callback-Funktion (im `cf`-Argument) einen Wert zurückgibt.

## Beispielaufrufe

### Beispiel 1

Der folgende Code ist Teil des Plug-ins getQueryParam.  Es wird die Hilfefunktion getParameterValue für alle Schlüssel-Wert-Paare ausgeführt, die in der Abfragezeichenfolge (fullQueryString) der URL enthalten sind.  Um jedes Schlüssel-Wert-Paar zu extrahieren, muss die Zeichenfolge (fullQueryString) durch ein kaufmännisches Und (&amp;) getrennt und geteilt werden. parameterKey bezieht sich auf den Abfragezeichenfolgenparameter, den das Plug-in speziell aus der Abfragezeichenfolge extrahieren möchte.

```js
returnValue = pt(fullQueryString, "&", "getParameterValue", parameterKey)
```

Die obige Zeile ist eine Verknüpfung zum Ausführen von Code, der wie folgt aussieht:

```js
var returnValue = "",
  parameters = fullQueryString.split("&"),
  parametersLength = parameters.length;
for(var i = 0; i < parametersLength; i++)
{
  returnValue = getParameterValue(parameters[i], parameterKey);
  if(returnValue !== "") break;
}
```

## Versionsverlauf

### 3.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 2.01 (24. September 2019)

* Geringfügige Codeänderungen zur Reduzierung der Gesamtgröße.

### 2.0 (17. April 2018)

* Zwischenversion (neu kompiliert, kleinere Code-Größe).
* Unterstützung für H-Code und AppMeasurement hinzugefügt.

### 1.0 (23. September 2013)

* Erste Version.
