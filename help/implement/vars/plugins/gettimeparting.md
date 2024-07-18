---
title: getTimeParting
description: Messen Sie die Zeit, zu der eine bestimmte Aktion stattfindet.
feature: Variables
exl-id: 3fab36c8-a006-405a-9ef1-2547c2b36b0d
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '801'
ht-degree: 77%

---

# Adobe-Plug-in: getTimeParting

{{plug-in}}

Mit dem `getTimeParting`-Plug-in können Sie die Details zu dem Zeitpunkt erfassen, zu dem eine beliebige messbare Aktivität auf Ihrer Website stattfindet. Dieses Plug-in ist nützlich, wenn Sie Metriken nach wiederholbarer Zeitteilung über einen bestimmten Datumsbereich aufschlüsseln möchten. Sie können beispielsweise die Konversionsraten zwischen zwei verschiedenen Wochentagen vergleichen, z. B. alle Sonntage im Vergleich zu allen Donnerstagen. Sie können auch Tageszeiträume vergleichen, z. B. alle Morgen im Vergleich zu allen Abenden.

Analysis Workspace bietet ähnliche vordefinierte Dimensionen, die etwas anders formatiert sind als dieses Plug-in. Weitere Informationen finden Sie unter [Dimensionen für die Zeitunterteilung](/help/analyze/analysis-workspace/components/dimensions/time-parting-dimensions.md) im Analysebenutzerhandbuch. Für einige Unternehmen sind die vordefinierten Dimensionen von Analysis Workspace ausreichend.

>[!IMPORTANT]
>
>Version 4.0+ dieses Plug-ins unterscheidet sich deutlich von früheren Versionen. Adobe empfiehlt dringend, dieses Plug-in von Grund auf neu zu implementieren. Code, der auf das Plug-in vor Version 4.0 verweist, ist nicht mit der aktuellen Version dieses Plug-ins kompatibel.

## Installieren des Plug-ins mit der Web SDK-Erweiterung

Adobe bietet eine Erweiterung, mit der Sie am häufigsten verwendete Plug-ins mit dem Web SDK verwenden können.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie links auf **[!UICONTROL Tags]** und dann auf die gewünschte Tag-Eigenschaft.
1. Klicken Sie links auf **[!UICONTROL Erweiterungen]** und dann auf die Registerkarte **[!UICONTROL Katalog]** .
1. Suchen und installieren Sie die Erweiterung **[!UICONTROL Common Web SDK Plugins]** .
1. Klicken Sie links auf **[!UICONTROL Datenelemente]** und dann auf das gewünschte Datenelement.
1. Legen Sie den gewünschten Datenelementnamen mit der folgenden Konfiguration fest:
   * Erweiterung: Allgemeine Web SDK-Plugins
   * Datenelement: `getTimeParting`
1. Legen Sie den Parameter `Time Zone` auf der rechten Seite fest.
1. Speichern und veröffentlichen Sie die Änderungen am Datenelement.

## Installieren Sie das Plug-in manuell für die Implementierung des Web SDK

Dieses Plug-in wird noch nicht für die Verwendung in einer manuellen Implementierung des Web SDK unterstützt.

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
   * Aktionstyp: getTimeParting initialisieren
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
/* Adobe Consulting Plugin: getTimeParting v6.3 (No Prerequisites Needed) */
function getTimeParting(t){var c=t;if("-v"===t)return{plugin:"getTimeParting",version:"6.3"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var b;a<window.s_c_il.length;a++)if(b=window.s_c_il[a],b._c&&"s_c"===b._c){a=b;break a}}a=void 0}"undefined"!==typeof a&&(a.contextData.getTimeParting="6.3");c=document.documentMode?void 0:c||"Etc/GMT";a=(new Date).toLocaleDateString("en-US",{timeZone:c,minute:"numeric",hour:"numeric",weekday:"long",day:"numeric",year:"numeric",month:"long"});a=/([a-zA-Z]+).*?([a-zA-Z]+).*?([0-9]+).*?([0-9]+)(.*?)([0-9])(.*)/.exec(a);return"year="+a[4]+" | month="+a[2]+" | date="+a[3]+" | day="+a[1]+" | time="+(a[6]+a[7])};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getTimeParting`-Funktion verwendet das folgende Argument:

**`t`** (Optional, aber empfohlen, Zeichenfolge): Der Name der Zeitzone, in die die Ortszeit des Besuchers umgerechnet werden soll.  Die Standardeinstellung ist die UTC/GMT-Zeit. Eine vollständige Liste der gültigen Werte finden Sie unter [List of tz database time zones (Liste der Zeitzonen der Zeitzonen-Datenbank)](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) auf Wikipedia.

Zu den üblichen gültigen Werten gehören:

* `"America/New_York"` für Eastern Time (EST)
* `"America/Chicago"` für Central Time (CST)
* `"America/Denver"` für Mountain Time (MST)
* `"America/Los_Angeles"` für Pacific Time (PST)

Beim Aufrufen dieser Funktion wird eine Zeichenfolge zurückgegeben, die die folgenden durch einen senkrechten Strich (`|`) getrennten Zeichen enthält:

* Das aktuelle Jahr
* Der aktuelle Monat
* Der Tag des Monats
* Der Tag des Woche
* Die aktuelle Zeit

## Beispiele

```js
// Use the following code if the visitor resides in Paris, France
s.eVar8 = getTimeParting("Europe/Paris");

// Use the following code if the visitor resides in San Jose, California
s.eVar17 = getTimeParting("America/Los_Angeles");

// Use the following code if the visitor resides in Ghana.
// Note that Ghana is in GMT time, the default time zone that the plug-in uses with no argument
s.eVar22 = getTimeParting();

// Internet Explorer only returns the visitor's local time. Use this conditional statement to accommodate IE visitors
if(!document.documentMode) s.eVar39 = getTimeParting("America/New_York");
else s.eVarX = "Internet Explorer Visitors";

// Given a visitor from Denver Colorado visits a site on August 31, 2020 at 9:15 AM
// Returns the string value "year=2020 | month=August | date=31 | day=Friday | time=6:15 PM"
s.eVar10 = getTimeParting("Europe/Athens");

// Returns the string value "year=2020 | month=August | date=31 | day=Friday | time=6:15 AM"
s.eVar11 = getTimeParting("America/Nome");

// Returns the string value "year=2020 | month=August | date=31 | day=Friday | time=8:45 PM"
s.eVar12 = getTimeParting("Asia/Calcutta");

// Returns the string value "year=2020 | month=September | date=1 | day=Saturday | time=1:15 AM"
s.eVar13 = getTimeParting("Australia/Sydney");
```

## Versionsverlauf

### 6.3 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 6.2 (5. November 2019)

* Kleine Fehlerbehebungen
* Reduzierte Gesamt-Code-Größe

### 6.1 (26. November 2018)

* Korrektur für Internet Explorer-Browser. Sie können die Zeit zurückgeben, jedoch nur in der Ortszeit des Besuchers.

### 6.0 (14. August 2018)

* Vollständige Neufassung zur Anpassung an internationale Standards. Die Sommerzeit und alle Zeitzonen werden jetzt richtig konvertiert.

### 5.0 (17. April 2018)

* Zwischenversion (neu kompiliert, kleinere Code-Größe)
* Der `tpDST`-Parameter ist nicht mehr erforderlich, da das Start-/Enddatum der Sommerzeit jetzt automatisch erkannt wird.

>[!CAUTION]
>
>Frühere Versionen dieses Plug-Ins konnten nicht für alle zukünftigen Jahre verwendet werden. Wenn Sie eine frühere Version dieses Plug-Ins verwenden, empfiehlt Adobe dringend, ein Upgrade auf die neueste Version durchzuführen, um JavaScript-Fehler und Datenverluste zu vermeiden. Wenn eine Aktualisierung dieses Plug-Ins nicht möglich ist, stellen Sie sicher, dass die Variable `s._tpdst` im Plug-in-Code die entsprechenden Jahre in der Zukunft enthält.

### 4.0 (22. August 2016)

* Bietet eine brandneue Lösung und enthält jetzt Informationen zu Jahr, Monat und Datum.
