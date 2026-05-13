---
title: VISTA-Regeln in Adobe Analytics
description: Erfahren Sie mehr über VISTA-Regeln und ihre Funktionen.
exl-id: fab2acc3-b037-48f9-bb20-625ccb75b4cc
feature: Analytics Basics
TQID: https://experienceleague.adobe.com/x3pRtt4sTKGPnD30xXJWIX6OEjaDWHED-S2-0BXCcDg
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: a421fb65-2c82-457a-921c-28c46b697a39
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 354
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
