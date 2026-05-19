---
title: Lösungsdesigndokument erstellen
description: Erfahren Sie, was ein Lösungsdesigndokument ist und wie Sie es in Ihrem Unternehmen verwenden können.
feature: Implementation Basics
exl-id: 0b5c5ddd-5f53-4790-a649-1381135dacda
role: Admin, Developer, Leader
TQID: https://experienceleague.adobe.com/OLSxdEz9--Xe8bCRH6-TimsPloUUdesg4-wrBNL3uPU
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 698
ht-degree: 76%

---

# Lösungsdesigndokument erstellen

Ein Dokument zum Lösungsentwurf (auch als Referenz zum Lösungsentwurf oder als Dokument zu Geschäftsanforderungen bezeichnet) ist im Wesentlichen der Entwurf Ihrer Analytics-Implementierung. Es definiert Kriterien, die von Interessenträgern in Ihrer gesamten Organisation identifiziert werden, und übersetzt diese in Variablen in Adobe Analytics. Ohne eine Lösung haben Unternehmen Schwierigkeiten, die Berichtserfordernisse zu koordinieren, und neigen dazu, das Erfassen wichtiger Daten zu übersehen.

## Voraussetzungen

[Überprüfen Sie Ihre Analytics-Implementierung und veröffentlichen Sie sie in der Produktion](../launch/validate-publish-prod.md) - Adobe empfiehlt, eine Basisimplementierung einzurichten, damit wichtige Daten gesammelt werden, während zusätzliche Geschäftsanforderungen festgelegt und implementiert werden.

## Eigentum und Speicherort des Entwurfspapiers

* **Legen Sie fest, wer in Ihrem Unternehmen für die Pflege des Lösungs-Design-Dokuments verantwortlich ist.** Diese Rolle kann entweder eine Einzelperson oder ein Team sein. Stellen Sie sicher, dass der Lösungsentwurf auch durch Rollenänderungen oder Organisationsänderungen erhalten bleibt. Es handelt sich um ein lebendiges Dokument, das ordnungsgemäß aufbewahrt werden muss.
* **Bestimmen Sie, wo sich Ihr Lösungsdokument befinden wird.** Es gibt keinen optimalen Ort für Lösungs-Design-Dokumente, aber sie leben normalerweise an einem weit zugänglichen internen Ort. Beispiele sind eine freigegebene Tabelle oder ein gemeinsamer Arbeitsbereich wie SharePoint oder ein internes Wiki. Sie müssen nicht für jeden bearbeitbar sein, aber es ist hilfreich, wenn zumindest die Anzeige möglich ist,

## Geschäftsanforderungen definieren

Bei der Ermittlung der zu erfassenden Daten ist es leicht, „alles“ zu sagen, was jedoch schnell schwer zu handhaben sein kann und sogar weniger Wert bieten kann als die Erfassung präziserer Datenmengen.

1. **Bestimmen der wichtigsten Leistungsindikatoren.** Was möchten Sie letztendlich von den Besuchern? Die Antwort auf diese Frage variiert je nach Branche und kann mehrere Dinge umfassen. Beispiele sind Käufe, Registrierungen oder Anzeigenklicks.
1. **Finden Sie die wichtigsten zu erfassenden Daten heraus.** Stellen Sie Geschäftsfragen, auf die Sie spezifische Antworten wünschen. Antworten auf diese Fragen würden Einblicke in die Verbesserung der KPIs geben.
1. **Stellen Sie sich diese Fragen und ermitteln Sie Ihre Tracking-Anforderungen.** Gruppieren Sie sie in Dimensionen und Metriken.
   * Dimensionen sind Variablen, die Text enthalten. Beispiele wären der interne Suchbegriff, die Produktkategorie oder der Name eines Bereichs, auf den ein Besucher geklickt hat.
   * Metriken sind spezifische Ereignisse, die ein Besucher ausführen soll - wenn er eine gewünschte Aktion durchführt, steigt die Zahl um 1. Beispiele wären das Senden einer Bestellung, das Abonnieren eines Newsletters oder das Senden einer Umfrageantwort.
1. **Ordnen Sie Dimensionen und Metriken einer Seite oder einem Arbeitsblatt zu.** Diese Seite oder Tabelle wird letztendlich zu Ihrem Lösungs-Design-Dokument. Einige hilfreiche Spalten oder Aufzählungspunkte, die eingeschlossen werden sollen:
   * Implementierungsstatus: Geplant, aktiv, inaktiv, Probleme usw. Dies würde die Betrachter des Dokuments über den Status der Variablen informieren, wenn sie implementiert wurde oder Probleme mit der Datenerfassung auftreten.
   * Variablenname: Beispiel: „Interne Suchbegriffe“. Dieser Wert ist der Wert, den Analysten bei der Arbeit in Analytics sehen.
   * Zugeordnete Analytics-Variable: welcher standardmäßigen oder benutzerdefinierten Analytics-Variable Werte zugewiesen werden sollen. Dimensionen fallen normalerweise unter eVars, während Metriken unter Ereignisse fallen.
   * Logik: Eine Beschreibung, wie die Variable festgelegt wird und was deren Wert bestimmt. Beispiel: „Nur auf internen Suchseiten eingestellt. Übernimmt den Wert des Abfragezeichenfolgenparameters q.“
   * Sonstige Hinweise zur Variablen.

## Zusätzliche Ressourcen

Die Definition eines Lösungsdesigndokuments ist ein ziemlich komplexes Projekt, besonders für Unternehmen, die noch kein Projekt erstellt haben. Wenn Sie weitere Unterstützung benötigen, bietet Adobe eine spezielle Beratung an, um Ihr Unternehmen bei der Einführung von Adobe Analytics zu unterstützen. Wenden Sie sich an Ihr Adobe Account Team, wenn Sie professionelle Services von Adobe in Anspruch nehmen möchten. Es kann ein [technischer Fragenkatalog](assets/technical-pre-implementation-questionnaire.pdf) zur Implementierung ausgefüllt werden, damit Adobe anhand der Anforderungen Ihres Unternehmens genau weiß, wie Sie dabei unterstützt werden können.

Es gibt auch mehrere Adobe-Partner, die sich auf die Unterstützung bei der Erstellung eines Lösungsdesigndokuments sowie die Implementierung von Adobe Analytics auf Ihrer Site spezialisiert haben.

## Nächste Schritte

Implementieren Sie die Variablen in Ihr Lösungsdesigndokument.

[Erstellen Sie eine Datenschicht](data-layer.md): Übersetzen Sie Variablen in Ihrem Design-Dokument in JavaScript-Variablen auf Ihrer Site.
