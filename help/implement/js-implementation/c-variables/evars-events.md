---
description: 'Wenn Sie zusätzliche Informationen verfolgen möchten, aber nicht genügend Variablen zur Verfügung haben, können Sie jetzt auf zusätzliche eVars und Erfolgsereignisse zugreifen '
keywords: Analytics-Implementierung;eVars;Ereignisse;eVar-Anzahl;wie viele eVars;wie viele Ereignisse
seo-description: 'Wenn Sie zusätzliche Informationen verfolgen möchten, aber nicht genügend Variablen zur Verfügung haben, können Sie jetzt auf zusätzliche eVars und Erfolgsereignisse zugreifen '
seo-title: Zusätzliche eVars und Ereignisse
solution: Analytics
title: Zusätzliche eVars und Ereignisse
topic: Entwickler und Implementierung
uuid: 6f53069b-6941-40f1-9db6-2d1839822b8f
translation-type: ht
source-git-commit: 76d0ce11d9b560e0df866be9e753804b6fa4bb3d

---


# Zusätzliche eVars und Ereignisse

Wenn Sie zusätzliche Informationen verfolgen möchten, aber nicht genügend Variablen zur Verfügung haben, können Sie jetzt auf zusätzliche eVars und Erfolgsereignisse zugreifen:

>[!NOTE]
>
>JavaScript-H-Code unterstützt diese zusätzlichen eVars und Ereignisse nicht.

## Berechtigungen für benutzerdefinierte Dimensionen und Ereignisse {#section_869EC3D8A5614036A9C586F2B74FA7DC}

| Adobe Analytics-Produkt |  |  |  |
|---|---|---|---|
| Adobe Analytics – Foundation | 75 Eigenschaftsvariablen | 200 eVars | 1000 Ereignisse |
| Adobe Analytics – [Select](https://www.adobe.com/data-analytics-cloud/analytics/select.html) | 75 Eigenschaftsvariablen | 200 eVars | 1000 Ereignisse |
| Adobe Analytics – [Prime](https://www.adobe.com/data-analytics-cloud/analytics/prime.html) | 75 Eigenschaftsvariablen | 200 eVars | 1000 Ereignisse |
| Adobe Analytics – [Ultimate](https://www.adobe.com/data-analytics-cloud/analytics/ultimate.html) | 75 Eigenschaftsvariablen | 250 eVars | 1000 Ereignisse |

## Befüllen von Variablen und Ereignissen {#section_DEA51A22BCBB4B92BDD25814AAD296E4}

* Wenn Sie die folgenden Versionen von [!DNL AppMeasurement] verwenden, können die Variablen in der Datenerfassungsbibliothek befüllt werden:

   * AppMeasurement für JavaScript, Version 1.4+
   * AppMeasurement für Flash, Version 3.9+
   * AppMeasurement für Java, Version 1.2.8+
   * AppMeasurement für Silverlight/.NET, Version 1.4.2+
   * AppMeasurement für PHP, Version 1.2.2+

* Wenn Sie eine frühere Version von Code oder JavaScript H.* verwenden, können Sie Textdaten befüllen und Verarbeitungsregeln verwenden, um die Variablen zu befüllen.
* Alle Version des Datenerfassungscodes können die Ereignisse 101–1000 befüllen.
* Verarbeitungsregeln können verwendet werden, um eVars 76–250 basierend auf Kontextdaten oder anderen Variablen zu befüllen.

## Häufig gestellte Fragen {#section_E915B03236BD47DCA065F1FC5A6E30C6}

* **Haben Adobe Analytics-Schnittstellen sofort Zugriff auf diese neuen Variablen?** Diese Schnittstellen haben sofort Zugriff: [!UICONTROL Analysis Workspace], [!UICONTROL Reports &amp; Analytics], [!UICONTROL Report Builder], [!UICONTROL Ad Hoc Analysis], APIs und [!UICONTROL Data Workbench].

* **Werden diese zusätzlichen eVars und Ereignisse automatisch in meinen Data Feeds angezeigt?** Sobald die neuen Variablen aktiviert sind, können Data Feeds darauf zugreifen. Neue eVar-Spalten werden erst dann angezeigt, wenn Sie sie einschließen. Neue Ereignisse werden jedoch in der event_list-Spalte angezeigt, sobald sie aktiviert wurden. Die Suchtabelle für Ereignisse enthält die Ereignisnamen für diese Ereignis-IDs. Aktivieren Sie keine neuen Ereignisse, wenn Sie sie noch nicht in den Data Feeds verwenden möchten.

* **Wie fordere ich neue Data Feed-Spalten an?** Informationen zum Anfordern neuer Spalten finden Sie unter [Konfigurieren von Datenfeeds](https://marketing.adobe.com/resources/help/de_DE/sc/clickstream/datafeeds_configure.html).

* **Angenommen, ich bin Analytics Ultimate-Kunde und möchte wieder zu Analytics Prime zurückkehren, habe aber derzeit mehr als 200 eVars aktiviert. Was muss ich tun?** Adobe deaktiviert keine Ihrer vorhandenen eVars, Sie können jedoch keine weiteren eVars aktivieren. Wenn Sie eVars deaktivieren, können Sie sie erst wieder aktivieren, wenn Sie weniger als die für Analytics Prime zulässige Höchstzahl von 200 eVars aktiviert haben.

