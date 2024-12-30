---
description: Antworten auf Fragen, die Sie unter Umständen bei der Implementierung von Audience Analytics haben.
solution: Experience Cloud
title: Häufig gestellte Fragen zu Audience Analytics
feature: Audience Analytics
exl-id: 86e7967c-030c-44d6-8294-e7e6d41f6fc3
source-git-commit: 750c4b0ffb52c3f2cf25abcd76ef149a4521109e
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 31%

---

# Häufig gestellte Fragen

Antworten auf Fragen, die Sie unter Umständen bei der Implementierung von Audience Analytics haben.

## FAQs zu rechtlichen Fragen {#legal}

+++ Woher weiß ich, ob meine Analytics-Daten personenbezogene Daten (PII) enthalten? Und wenn ja, was mache ich dagegen?

Wenn E-Mails/Adressen/etc. in einer Prop oder eVar vorhanden sind, sollten Sie die Daten während der Erfassung hashen. Wenn Ihr Land IP-Adressen als personenbezogene Daten einstuft ([ Sie die IP-Verschleierung ein](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/exclude-ip.html?lang=de). Wenden Sie sich an Ihren Analytics-Administrator, um zu erfahren, was Sie erfassen. Sprechen Sie mit Ihrer Rechtsabteilung, um zu erfahren, was sie als personenbezogene Daten erachtet.

+++

+++ Woher weiß ich, ob meine Report Suites eine Onsite-Personalisierung oder ein Offsite-/Onsite-Targeting durchführen?

Diese gelten nicht für das Senden von Adobe Analytics-Daten an Adobe Audience Manager. Fragen Sie sich:

* Wird ein von Analytics freigegebenes Segment mit einer MCA-Dimension wieder für die Experience Cloud freigegeben?

* Exportieren Sie (z. B. über Datenfeeds) in ein Business Intelligence-System (BI), das für diese Zwecke verwendet wird?

+++

## Adobe Audience Manager-spezifische FAQs {#aam-specific}

+++ Wie erstelle ich ein Analytics-Ziel in Audience Manager?

Siehe [Konfigurieren eines Analytics-Ziels in Adobe Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/experience-cloud-destinations/create-analytics-destination.html?lang=de).

+++

+++ Wie lange dauert es nach dem Erstellen und Speichern eines Analytics-Ziels, bis die Daten in meinen ausgewählten Report Suites angezeigt werden?

Es kann einige Stunden dauern, Ihre Report Suites mit neuen Daten zu füllen.

+++

+++ Ich habe ein neues Analytics-Ziel erstellt, sehe es jedoch nicht im Abschnitt „Zielzuordnungen“ meiner verfügbaren Segmente. Wo ist dieses Ziel hingegangen oder wie finde ich es?

Ein Analytics-Ziel verschwindet aus dem Abschnitt „Zielzuordnungen“ eines Segments, wenn Sie die Option **[!UICONTROL Alle aktuellen und zukünftigen Segmente automatisch zuordnen]** in &quot;**[!UICONTROL &quot;]**. Um das zu vermeiden, wählen Sie statt der automatischen Option **[!UICONTROL Segmente manuell zuweisen]** aus.

+++

Erhalte ich dadurch alle Informationen aus Adobe Audience Manager, in Analytics?

Nein, nur Daten, die sich auf Personen beziehen, die während oder nach der Aktivierung von Audience Manager-Zielgruppen und während oder nach der Qualifizierung des Segments auf Ihre Site kommen.

+++

+++ Erhalte ich so eine für jedes Segment adressierbare Zielgruppe?

Nicht ganz. Sie erfahren die Anzahl der Besucher in diesem Segment, die während oder nach der Qualifizierung des Segments auf Ihre Site kamen.

+++

+++ Wie unterscheidet sich dies vom alten Cookie-Ziel von Analytics?

Segmente werden für qualifiziert und in Echtzeit zurückgegeben - zum selben Treffer. Die Anzeigenamen werden automatisch angezeigt.

+++

+++ Was passiert, wenn einige meiner Report Suites personenbezogene Daten enthalten und andere nicht?&lt;

Tipp: Erstellen Sie zwei Ziele – Fügen Sie die Report Suites mit persönlichen Daten zu einem Ziel hinzu und die Report Suites ohne persönliche Daten zum anderen.

+++

## Analytics-spezifische FAQs {#aa-specific}

+++ Wird diese Integration als Dimension oder Segment in Analytics angezeigt?

Als Dimensionen: Zielgruppen-ID und Zielgruppenname.

+++

+++Wo kann ich diese Dimensionen in Analytics verwenden?

Überall werden sie wie jede andere Dimension behandelt, die in Analytics erfasst wird.

+++

+++ Warum sehe ich keine Daten in Analytics?

Wahrscheinlich gibt es widersprüchliche Adobe Audience Manager-Datenschutzsteuerelemente zwischen Datenquelle und Ziel.

+++

+++ Warum fehlen einige meiner Segmente in Analytics, obwohl ich alle Segmente gesendet habe?&lt;

* Die Adobe Audience Manager-Datenexportsteuerelemente für das Ziel und in den Datenquellen der Segmente kollidieren möglicherweise, sodass bestimmte Segmente nicht gesendet werden können.

* Wenn Sie Eigenschaften mit Drittpartei-Daten in Ihren Segmenten verwenden, können diese Segmente nicht an ein Ziel (einen Satz von Report Suites) weitergeleitet werden, das persönliche Daten enthält.

+++

+++ Warum wird in meinem Analytics-Bericht „Zielgruppenlimit erreicht“ angezeigt? (Hinweis: Dies wird auch als Zielgruppen-ID = -1 und `::max_audiences_exceeded::` in Data Warehouse dargestellt.)

Standardmäßig sendet die Audience Analytics-Integration für Adobe Audience Manager alle Segmente, für die sich eine Besucherin oder ein Besucher qualifiziert, pro Treffer an Analytics. Wenn ein Besucher zu mehr als 150 Adobe Audience Manager-Segmenten auf einmal gehört, werden die **150 zuletzt qualifizierten Segmente** an Analytics gesendet, während die restliche Liste abgeschnitten wird. Es wird ein zusätzliches Warnsignal an Analytics gesendet, das anzeigt, dass die Segmentliste gekürzt wurde. Dieses Warnsignal wird in der Dimension „Zielgruppendimension“ als „Zielgruppenlimit erreicht“ und in der Dimension „Zielgruppen-ID“ als „-1“ dargestellt.

Es ist zwar unwahrscheinlich, dass sich ein Besucher bei einem bestimmten Treffer für mehr als 150 Segmente qualifiziert, aber es kann in seltenen Fällen vorkommen. Wenn Ihnen in Ihrer Berichterstellung die Meldung „Zielgruppenlimit erreicht“ angezeigt wird, haben Sie zwei Optionen:

* Option 1: Lassen Sie die Integration weiterhin im vorkonfigurierten Zustand funktionieren, indem Sie die 150 zuletzt qualifizierten Segmente für einen bestimmten Besucher senden.

* Option 2: Wählen Sie in Adobe Audience Manager die 150 Segmente aus, die für Ihr Unternehmen bei der Integration am wichtigsten sind. Adobe Audience Manager vergleicht dann Besucher nur mit diesen 150 Segmenten. Der Nachteil dieser Vorgehensweise ist, dass Sie bei allen Besuchern nur noch diese 150 Segmente erhalten. Dahingegen liefert die Vorgehensweise in Option 1 dadurch, dass die Integration pro Treffer Segmente sendet, eine unbegrenzte Anzahl an Segmenten.

+++

+++ Werden für diese Integration zusätzliche Server-Aufrufe an Analytics in Rechnung gestellt?

Nein. Adobe Audience Manager-Zielgruppen werden Server-seitig in den Analytics-Treffer integriert. Dabei fallen keine zusätzlichen Server-Aufrufe für Analytics an (primär oder sekundär).

+++

## FAQs zur serverseitigen Weiterleitung {#SSF}

+++ Muss ich, wenn ich ältere SSF implementiert habe, auch zu Analytics Admin gehen und Report Suite SSF aktivieren?

Ja. Im Adobe Audience Manager-Ziel-Setup werden nur Report Suites angezeigt, für die SSF aktiviert ist.

+++

+++ Warum kann ich bestimmte Report Suites für SSF nicht in Analytics Admin aktivieren?

Es können nur Suites aktiviert werden, die Ihrer Experience Cloud-Org zugeordnet sind.

Weitere häufig gestellte Fragen zu diesem Thema finden Sie unter [FAQs zur serverseitigen Weiterleitung](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-faq.md).

+++

## Allgemeine FAQs {#section_E55410BBFB624AAFB87ADCF7F036DDA3}

+++ Warum unterscheiden sich die Segmentbesucherzahlen zwischen Audience Manager und Analytics?

Siehe [Unterschiede in der Besucherzahl](/help/integrate/c-audience-analytics/visitor-count-reconciliation.md).

+++

+++ Was ist der Unterschied zwischen „Zielgruppen“ in Adobe Audience Manager und „Segmenten“ in Analytics?

Siehe [Grundlegendes zu Segmenten in Analytics und Audience Manager](/help/integrate/c-audience-analytics/aam-analytics-segments.md). Adobe Audience Manager-Zielgruppen werden gesendet und als „Dimensionskomponenten“ freigegeben, die in Analytics verwendet werden können. Sie werden nicht als Segmente z. B. im Segment Builder angezeigt, sondern als Dimensionen, mit denen Sie Segmente erstellen können.

+++

+++ Was ist der Unterschied zwischen Kundenattributen und aus Adobe Audience Manager integrierten Kundendaten?

Kundenattribute sind nicht zeitbasiert, sondern gelten rückwirkend und können weiterverwendet werden. Die integrierten Daten von Adobe Audience Manager sind nur zeitbasiert und für die Zukunft vorgesehen. Darüber hinaus sind Kundenattribute eine Suchtabelle für das Experience Cloud von Besucher-IDs, während die Adobe Audience Manager-Integrationsdaten bei jedem Treffer für einen Besucher zugeordnet werden.

+++

+++ Was ist mit alten Ansätzen zu diesem Problem, z. B. den alten Beta- oder Consulting-Plug-in-Cookie-Zielen?

Wir empfehlen Ihnen, die neue Integration zu implementieren und alte Ziele zu entfernen.

+++
