---
title: VISTA-Regeln in Adobe Analytics
description: Erfahren Sie mehr über VISTA-Regeln und ihre Funktionen.
exl-id: fab2acc3-b037-48f9-bb20-625ccb75b4cc
feature: Analytics Basics
source-git-commit: b1c22031b9254ff077dfdc04ab90ab231b504299
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 57%

---

# VISTA-Regeln in Adobe Analytics

VISTA-Regeln sind eine alternative Form der benutzerdefinierten Datenänderung, die Sie zwischen der Datenerfassung und -verarbeitung anwenden können. Weitere Informationen zu der Phase in der Daten-Pipeline, für die die VISTA-Regeln angewendet werden, finden Sie unter [Verarbeitungsreihenfolge](processing-order.md). VISTA-Regeln wirken sich nur auf aktuelle Daten zum Zeitpunkt ihrer Erfassung aus. Vorhandene Daten werden durch sie nicht geändert.

Typische Anwendungsfälle von VISTA-Regeln sind etwa:

* Kopieren eines Analytics-Treffers zwischen Report Suites mit möglicher Datenänderung in der kopierten Report Suite
* Benutzerdefinierter IP-Ausschluss, der über die möglichen Anwendungsfälle von [Nach IP ausschließen](/help/admin/tools/exclude-ip.md) hinausgeht
* Bedingte oder globale Änderung eines Variablenwerts
* Duplizieren von Variablenwerten in andere Variablen
* Hochladen von Dateien auf eine Adobe-FTP-Site mit möglichen Auswirkungen auf Variablenwerte

Viele Anwendungsfälle für VISTA-Regeln werden bereits von [Verarbeitungsregeln](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md), [Bot-Regeln](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md), [Virtual Report Suites](/help/components/vrs/vrs-about.md) oder einfach durch eine Aktualisierung Ihrer Adobe Analytics-Implementierung abgedeckt. Adobe empfiehlt VISTA-Regeln nur als letztes Mittel.

>[!IMPORTANT]
>
>Die Implementierung und Konfiguration von VISTA-Regeln erfordert eine kostenpflichtige Vereinbarung zwischen Ihrem Unternehmen und Adobe Professional Services. Wenden Sie sich an Ihr Adobe-Konto-Team, wenn Sie eine VISTA-Regel erstellen oder aktualisieren möchten.
>
>Bitte beachten Sie:
>
>* Die Erstellung von VISTA-Regeln umfasst nur die anfängliche Implementierung. Laufende Wartungs- oder VISTA-Regelaktualisierungen erfordern ein separates gebührenpflichtiges Engagement.
>
>* VISTA-Regeln sind auf bestimmte Bedingungen in Ihren Daten angewiesen. Änderungen an Ihrer Adobe Analytics-Implementierung, den Datentypen oder Zeichenfolgenlängen, die erfasst werden, Änderungen an den für DB VISTA verwendeten Tabellen oder andere Änderungen an den Eingabedatenmustern können beispielsweise dazu führen, dass eine VISTA-Regel nicht mehr wie erwartet funktioniert. Adobe empfiehlt, Ihre VISTA-Regeln regelmäßig zu überprüfen, um festzustellen, ob Aktualisierungen oder Entfernungen erforderlich sind.

## Erstellen einer VISTA-Regel {#create}

Sie müssen mit Adobe Professional Services zusammenarbeiten, um eine VISTA-Regel zu erstellen. Wenden Sie sich an Ihr Adobe-Konto-Team, wenn Sie eine VISTA-Regel erstellen möchten.

## Anzeigen vorhandener VISTA-Regeln. {#see}

Adobe bietet keine Benutzeroberfläche zum Anzeigen vorhandener VISTA-Regeln. Wenden Sie sich mit der gewünschten Report Suite an Ihr Adobe-Konto-Team oder die Kundenunterstützung, um eine Liste der vorhandenen VISTA-Regeln abzurufen.
