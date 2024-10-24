---
title: Was ist die neue Adobe Report Builder?
description: Beschreibt die neue Report Builder-Funktion
role: User
feature: Report Builder
type: Documentation
solution: Analytics
source-git-commit: 7e8a25381f2eadafc5dc22a0991060ea475b5d43
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 27%

---

# Über die neue Adobe Report Builder

Das neue JavaScript-Report Builder-Add-in, das ursprünglich nur auf Customer Journey Analytics verfügbar war, wird jetzt auch in Adobe Analytics eingeführt. Diese neue Version bietet mehrere Vorteile:

- Mit verbesserten Workflows für die Erstellung und Verwaltung von Datenblöcken, einschließlich höherer Flexibilität bei Datenblöcken, können Sie Einblicke in Excel schneller und einfacher finden.
- Plattformübergreifend: Melden Sie sich nicht mehr bei Ihrer VM an, um Report Builder zu verwenden, da wir jetzt PC, Mac und Excel Online unterstützen
- Weniger Wartezeit für die Rückgabe von Datenblöcken dank API 2.0-Upgrade
- Verbesserte Geschwindigkeit.

>[!NOTE]
>
>Die Arbeitsmappen-Planung für diese Version von Report Builder auf Adobe Analytics wurde noch nicht veröffentlicht, wird aber Anfang 2025 verfügbar sein. Sie können jetzt mit Arbeitsmappen beginnen, die keine Planung erfordern.

Benutzer des Tools &quot;Legacy Report Builder&quot;können [alte Arbeitsmappen](/help/analyze/report-builder/convert-workbooks.md) in den neuen Report Builder konvertieren.

Mit Report Builder können Sie benutzerspezifische Berichte einfach mit Adobe Analytics-Daten erstellen, bearbeiten und aktualisieren. Mithilfe der einfachen und flexiblen Drag &amp; Drop-Benutzeroberfläche von Report Builder können Sie komplexe Datenabfragen und benutzerspezifische Berichte aus Adobe Analytics-Daten erstellen, die alle in Excel verfügbar sind.

Mit Report Builder können Sie:

- Referenzieren vorhandener Arbeitsblattzellen zur Erstellung der gewünschten Zeilenreihenfolge sowie des entsprechenden Datumsbereichs oder Filters
- Erstellen von benutzerdefinierten Datumsangaben mithilfe von Kalendern, Zellbezügen oder mathematischen Berechnungen
- Gestalten Ihrer Tabellen und Visualisierungen mit den bekannten Excel-Formatierungswerkzeugen

## Verwenden des alten Report Builders und des neuen Report Builders nebeneinander

Sie können beide Versionen von Report Builder mit folgenden Einschränkungen verwenden:

- Verwenden Sie nicht beide Report Builder-Versionen gleichzeitig in derselben Datei. Sie schließen sich gegenseitig aus.
- Sie können weiterhin den alten Report Builder für alte Arbeitsmappen und den neuen Report Builder für neue Arbeitsmappen verwenden.
- Darüber hinaus können Sie alte Arbeitsmappen automatisch mit [1 in das neue Report Builder-Format konvertieren. ](/help/analyze/report-builder/convert-workbooks.md) Duplizieren Sie zuvor die Datei und benennen Sie sie um.

## In New Report Builder nicht unterstützte ältere Report Builder-Funktionen

Beim Vergleich der Funktionalität von Legacy Report Builder mit dem neuen Report Builder-Add-in sind einige ältere Funktionen nicht mehr verfügbar:

- Echtzeitanforderungen

- Pfad-/Fallout-Reporting

- FTP-Option für terminierte Berichte

- Besuchermetriken. Die folgenden Metriken werden in &quot;Unique Visitors&quot;konvertiert, auch wenn das Berichterstellungsergebnis möglicherweise nicht exakt übereinstimmt: `visitorshourly`, `visitorsdaily`, `visitorsweekly`, `visitorsmonthly`, `visitorsquarterly` und `visitorsyearly`. Dies gilt auch für `mobilevisitorshourly`, `mobilevisitorsdaily`, `mobilevisitorsweekly`, `mobilevisitorsmonthly`, `mobilevisitorsquarterly` und `mobilevisitorsyearly`.

## Häufige Anwendungsfälle

- **Datenextrahierung**: Mit Adobe Report Builder können Sie Daten aus Adobe Analytics in Excel extrahieren. Sie können benutzerdefinierte Berichte und Abfragen erstellen, um bestimmte Datenpunkte abzurufen, die für Ihre Analyse relevant sind.

- **Benutzerdefinierte Berichterstellung**: Sie können benutzerdefinierte Berichte in Excel entsprechend Ihren spezifischen Berichtsanforderungen entwerfen und formatieren. Dies ist besonders nützlich, um Berichte an verschiedene Stakeholder anzupassen.

- **Ad-Hoc-Analysen**: Benutzende können schnell Ad-Hoc-Berichte erstellen, um bestimmte Fragen zu beantworten oder Daten-Trends zu untersuchen, ohne einen langwierigen Prozess der Berichterstellung durchlaufen zu müssen.

- **Dashboarding**: Aus CJA extrahierte Daten können zur Erstellung von Excel-basierten Dashboards und Visualisierungen verwendet werden, um einen allgemeinen Überblick über die wichtigsten Leistungsindikatoren (KPIs) zu erhalten.

- **Freigeben von Erkenntnissen**: Sie können Excel-Berichte und -Erkenntnisse für Team-Mitglieder oder Stakeholder freigeben, die möglicherweise keinen direkten Zugriff auf CJA haben.

## Übersichtsvideo

>[!IMPORTANT]
>
>In diesem Übersichtsvideo wird die Benutzeroberfläche des Report Builders im Customer Journey Analytics dargestellt. Die Benutzeroberfläche und die Terminologie unterscheiden sich in einigen Punkten. Andernfalls ist das Benutzererlebnis identisch.

>[!VIDEO](https://video.tv.adobe.com/v/337569/?quality=12&learn=on)

Sie können Report Builder aus dem [Microsoft Store](https://appsource.microsoft.com/en-us/product/office/WA200003101?tab=Overview) herunterladen.
