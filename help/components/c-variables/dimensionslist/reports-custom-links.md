---
description: Zeigt die Links, die die Besucher Ihrer Site gern aufrufen. Die Homepage Ihrer Website hat vermutlich mehrere Links, die zur selben Seite führen. Möglicherweise gibt es einen Grafik- und Text-Link, die beide zur selben Seite führen. Dieser Bericht zeigt den Prozentsatz der Besucher, die den Grafik-Link im Vergleich zum Text-Link verwenden.
solution: Analytics
title: Anwenderspezifischer Link
topic: Reports
uuid: 2e0d0175-d5e4-4919-b601-3f488ef3e090
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Anwenderspezifischer Link

Zeigt die Links, die die Besucher Ihrer Site gern aufrufen. Die Homepage Ihrer Website hat vermutlich mehrere Links, die zur selben Seite führen. Möglicherweise gibt es einen Grafik- und Text-Link, die beide zur selben Seite führen. Dieser Bericht zeigt den Prozentsatz der Besucher, die den Grafik-Link im Vergleich zum Text-Link verwenden.

Die spezifischen Links, die verfolgt werden sollen, müssen mit speziellen Tags modifiziert werden, siehe [Linktracking](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linktrackvars.html).

Den [!UICONTROL Bericht „Benutzerspezifische Links“] können Sie zu folgenden Zwecken einsetzen:

* Ihren Site-Entwurf zu optimieren, durch die Erkenntnis, welche Links von Besuchern bevorzugt werden
* den Bedarf an redundanten Links zu Einzelseiten zu bestätigen

## Mobile SDK-Link-Namen {#section_70C91FE794104B5FBF289B19CC02EA8E}

The [mobile SDKs](https://marketing.adobe.com/resources/help/en_US/mobile/home.html) use custom links to track actions and lifecycle metrics. In Report Suites, die verwendet werden, um mobile Anwendungen zu messen, werden möglicherweise die folgenden vom SDK festgelegten Link-Namen angezeigt:

| ADBINTERNAL:Lifecycle | Gesendet vom Lebenszyklus-Aufruf in den 4.x SDKs. |
|---|---|
| AMACTION:[action name] | Gesendet von der Methode trackAction() in den 4.x SDKs, wobei „Aktionsname“ der bei Aufruf der Methode festgelegte Name ist. |
| ADMS BP-Ereignis | Gesendet vom Lebenszyklus-Aufruf in den 3.x SDKs. |

