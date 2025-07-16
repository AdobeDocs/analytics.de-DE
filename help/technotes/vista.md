---
title: VISTA-Regeln in Adobe Analytics
description: Erfahren Sie mehr über VISTA-Regeln und ihre Funktionen.
exl-id: fab2acc3-b037-48f9-bb20-625ccb75b4cc
feature: Analytics Basics
source-git-commit: c2adf6d2e328378332cc290ba2dfd75ee6587ef6
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 81%

---

# VISTA-Regeln in Adobe Analytics

VISTA-Regeln sind eine alternative Form der benutzerdefinierten Datenänderung, die Sie zwischen der Datenerfassung und -verarbeitung anwenden können. Weitere Informationen zu der Phase in der Daten-Pipeline, für die die VISTA-Regeln angewendet werden, finden Sie unter [Verarbeitungsreihenfolge](processing-order.md). VISTA-Regeln wirken sich nur auf aktuelle Daten zum Zeitpunkt ihrer Erfassung aus. Vorhandene Daten werden durch sie nicht geändert.

Typische Anwendungsfälle von VISTA-Regeln sind etwa:

* Kopieren eines Analytics-Treffers zwischen Report Suites mit möglicher Datenänderung in der kopierten Report Suite
* Benutzerdefinierter IP-Ausschluss, der über die möglichen Anwendungsfälle von [Nach IP ausschließen](/help/admin/admin/exclude-ip.md) hinausgeht
* Bedingte oder globale Änderung eines Variablenwerts
* Duplizieren von Variablenwerten in andere Variablen
* Hochladen von Dateien auf eine Adobe-FTP-Site mit möglichen Auswirkungen auf Variablenwerte

Viele Anwendungsfälle für VISTA-Regeln werden bereits von [Verarbeitungsregeln](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-overview.md), [Bot-Regeln](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md), [Virtual Report Suites](/help/components/vrs/vrs-about.md) oder einfach durch eine Aktualisierung Ihrer Adobe Analytics-Implementierung abgedeckt. Adobe empfiehlt VISTA-Regeln nur als letztes Mittel.

>[!IMPORTANT]
>
>VISTA-Regeln erfordern eine entgeltliche Vereinbarung zwischen Ihrem Unternehmen und Adobe Professional Services. Wenden Sie sich an Ihr Adobe-Konto-Team, wenn Sie eine VISTA-Regel erstellen oder aktualisieren möchten.

## Erstellen einer VISTA-Regel {#create}

Sie müssen mit Adobe Professional Services zusammenarbeiten, um eine VISTA-Regel zu erstellen. Wenden Sie sich an Ihr Adobe-Konto-Team, wenn Sie eine VISTA-Regel erstellen möchten.

## Anzeigen vorhandener VISTA-Regeln. {#see}

Adobe bietet keine Benutzeroberfläche zum Anzeigen vorhandener VISTA-Regeln. Wenden Sie sich mit der gewünschten Report Suite an Ihr Adobe-Konto-Team oder die Kundenunterstützung, um eine Liste der vorhandenen VISTA-Regeln abzurufen.
