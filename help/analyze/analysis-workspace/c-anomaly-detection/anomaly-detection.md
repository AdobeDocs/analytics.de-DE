---
description: Erfahren Sie, wie Sie Datenanomalien in Analysis Workspace kontextuell anzeigen und analysieren können.
title: Übersicht über die Anomalieerkennung
feature: Anomaly Detection
role: User, Admin
exl-id: b1625206-c774-40ef-9d92-25ee8ff1478d
source-git-commit: d37fa0aff0b1bbe196b943bc26e86b1e79936184
workflow-type: tm+mt
source-wordcount: '1300'
ht-degree: 68%

---

# Übersicht über die Anomalieerkennung

Datenanomalien können kontextbezogen in Analysis Workspace angezeigt und analysiert werden. Die Beitragsanalyse verwendet die Anomalieerkennung, um den Grund für die Anomalie zu ermitteln.


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Anomalieerkennung](https://video.tv.adobe.com/v/40727?quality=12&learn=on&captions=ger){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Kunden von Adobe Analytics Select und Adobe Analytics Foundation haben nur Zugriff auf die *tägliche Granularität* Anomalieerkennung in Workspace. Weitere Informationen finden Sie unter [Anomalieerkennung und Beitragsanalyse – Berechtigungen](#anomaly-detection-and-contribution-analysis-entitlements).

## Anomalieerkennung

Die Anomalieerkennung bietet eine statistische Methode, mit der festgestellt wird, wie sich eine bestimmte Metrik in Bezug auf frühere Daten verändert hat.

Die Anomalieerkennung ermöglicht es Ihnen, „echte Signale“ von „Rauschen“ zu unterscheiden. Zudem hilft sie Ihnen anschließend dabei, potenzielle Faktoren zu bestimmen, die zu diesen Signalen oder Anomalien beigesteuert haben. Auf diese Weise können Sie feststellen, welche statistischen Schwankungen relevant sind, und anschließend die Ursache eines echten Fehlers feststellen. Zudem erhalten Sie eine zuverlässige Metrikvorhersage (KPI).

Zu Beispielen von Fehlern, die ein Eingreifen Ihrerseits erfordern, zählen:

* Erhebliche Verwerfungen im durchschnittlichen Bestellwert
* Spitzen in Bestellungen mit geringem Umsatz
* Spitzen oder Verwerfungen in Testprogrammregistrierungen
* Verwerfungen bei Landingpage-Aufrufen
* Spitzen in Videopufferereignissen
* Spitzen in niedrigen Video-Bitraten

Sowohl die Anomalieerkennung als auch die [Beitragsanalyse](https://experienceleague.adobe.com/de/docs/analytics/analyze/analysis-workspace/anomaly-detection/anomaly-detection) sind zentrale Workflows in Analysis Workspace. Sie können Beitragsanalysen zu jeder beliebigen täglichen Anomalie ausführen und das Ergebnis in Ihr Analysis Workspace-Projekt einbetten.

Der Algorithmus der Analysis Workspace-Anomalieerkennung umfasst:

* Unterstützung für die Einstellungen „Stündlich“, „Wöchentlich“ und „Monatlich“ (zusätzlich zur vorhandenen Einstellung „Täglich“)
* Berücksichtigung von besonderen Tagen (wie z. B. Black Friday) und Feiertagen

## Beitragsanalyse

Die Beitragsanalyse erkennt verborgene Muster in Ihren Daten, um statistische Anomalien zu erklären und Korrelationen dahinter zu identifizieren

* unerwartete Kundenaktionen,
* Out-of-bound-Werte und
* plötzliche Spitzen oder Tiefpunkte

für ausgewählte Metriken über konvergente Zielgruppensegmente hinweg.


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Beitragsanalyse](https://video.tv.adobe.com/v/40759?quality=12&learn=on&captions=ger){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]


Etwas ist passiert. Warum? Ihr Anomalieerkennungsbericht zeigt einen ungewöhnlichen Anstieg bei Bestellungen und Sie möchten wissen, wie es dazu kommt. Was ist Außergewöhnliches passiert? Wer reagiert auf welche Kampagne oder welchen Verweis? Hat sich etwas viral verbreitet? Welche spezifischen Faktoren haben zu dieser Anomalie beigetragen? Und womöglich die wichtigste Frage: Wie kann ich wichtige Informationen zu meinem Kunden erfassen und diese Performance wiederholen? (Oder: Wie kann ich in Zukunft einen Rückgang bei einer Metrik oder einen Anstieg bei einer negativen Metrik vermeiden?)

Mithilfe der Beitragsanalyse können Sie Ihre Daten umgehend analysieren und so herausfinden, wie es zu einer Anomalie kam. Die Analyse ermittelt die beitragenden Faktoren zu einer Anomalie innerhalb weniger Sekunden anstatt in Wochen und stellt Ihnen Muster für Zielgruppensegmente bereit, sodass Sie die Interaktionen von Kunden besser nachvollziehen können. Sie können die Beitragsanalyse strategisch einsetzen, um aussagekräftige Verknüpfungen zu identifizieren und zu erfassen. Verwenden Sie diese Verknüpfungen dann strategisch, um neue Zielgruppensegmente zu entwickeln, oder taktisch, um nicht gebundene oder betrügerische Aktivitäten zu identifizieren, die einen Warnhinweis Trigger haben.

Die [Anomalieerkennung](#anomaly-detection) identifiziert Datenspitzen und extreme statistische Rückgänge, basierend auf ausgewählten Metriken und Zielgruppensegmenten. Die Anomalieerkennung legt eine historische Norm auf der Grundlage eines Trainingszeitraums fest und stellt dann extreme Versätze dar, die mit bestimmten Ereignissen korrelieren. Die Anomalieerkennung kann einen steilen Anstieg einer positiven Orders-Metrik oder einen Anstieg einer negativen Bounces-Metrik oder einen Rückgang beider Metriken melden und statistisch relevante Datenpunkte erfassen, die von der Beitragsanalyse ausgewertet werden. Wenn eine statistische Anomalie identifiziert wurde, können Sie mit der Beitragsanalyse für alle abweichenden Datenpunkte relevante Marketing- und Kampagnenvariablen einsehen und auswerten. Für die Auswertung von Verbindungen, die zu einer deutlichen Spitze bzw. einem deutlichen Tiefpunkt beigetragen haben, kommen fortschrittliche Algorithmen und maschinelles Lernen zum Einsatz. Diese Berechnungen werden dann in interaktiven Darstellungen angezeigt, die Ihnen unterschiedliche Perspektiven auf den Sachverhalt bieten. Auf diese Weise können Sie erkennen, warum etwas passiert ist und was dagegen unternommen werden kann.

Mithilfe der Beitragsanalyse können Sie eine Erzählung entwickeln, um zu beschreiben, warum eine Anomalie aufgetreten ist. Erfahren Sie, wie Sie auf Anomalien reagieren, relevante Metriken erfassen und versteckte Punkte identifizieren können, die Ihnen einen Gesamtgrund für Zielgruppeninteraktionen und Trends bei den Kundeninteressen liefern. Manchmal lässt sich eine Anomalie leicht erkennen und korrigieren. Das ist beispielsweise bei einer irrtümlichen Bestellung von 2000 Kajaks der Fall. Manchmal ist die Erkennung einer Anomalie dagegen recht schwierig, zum Beispiel bei einem aufkommenden Trend in einem bestimmten Zeitraum in einer Region, der nur in Reaktion auf eine spezifische zielgerichtete Kampagne erfolgt. Die Zusammenstellung beitragender Elemente in Metriken für unterschiedliche Dimensionen und ihre Verbindungen verschafft Ihnen einen allgemeinen Überblick über die Interaktionen Ihrer Zielgruppen und liefert wichtigen Kontext für abweichende Datenpunkte.

Im Folgenden finden Sie einige Anwendungsfälle:

* Identifizierung des Weitervermarktungspotenzials durch die Überwachung von Veränderungen bei der Produktnachfrage
* Optimierung des Kundenerlebnisses durch Reaktion auf spezifische Zielgruppeninteressen
* Frühe Identifizierung betrügerischer Bestellungen dank Anomalieberichten
* Schutz vor Industriespionage durch Identifikation hoher Auslastung und einer großen Anzahl an Downloads
* Überwachen von Vorgängen wie der Berichterstellung für fehlende JavaScript-Tags

Nach der umfassenden Analyse einer Anomalie wird eine Beitragszusammenfassung für die wichtigsten Elemente erstellt. Die Elemente werden darin in einer Rangfolge angeordnet, die auf der Gesamtzahl der Vorkommen und dem Prozentsatz des Elements an den beitragenden Faktoren basiert. Anhand der normalisierten Beitragsbewertung können Sie einen beitragenden Faktor ganz unkompliziert mit anderen wichtigen Dimensionselementen vergleichen und verbinden.

## Beitragsanalyse-Token

Sämtliche Kunden mit einer Berechtigung für Beitragsanalysen können in Analysis Workspace pro Monat eine begrenzte Anzahl vollständiger Beitragsanalysen ausführen. Beitragsanalyse **schließt Kunden von** (SiteCatalyst 15), Analytics Foundation-Kunden und Analytics Select-Kunden aus, die keine Berechtigung für die Beitragsanalyse haben.

Die Anzahl von Ausführungen pro Unternehmen ist durch monatliche Token beschränkt, die auf der Basis des von Ihrem Unternehmen gekauften Adobe Analytics-Produkts zugeteilt werden. Die Anzahl der Ausführungen pro Unternehmen beinhaltet die Möglichkeit, den Zugriff auf die Beitragsanalyse einzuschränken, um einen Token-Missbrauch zu vermeiden.

## Häufig gestellte Fragen

| Frage | Antwort |
| --- | --- |
| Warum hat Adobe Token eingeführt? | Die Beitragsanalyse ist eine der beliebtesten Funktionen in Adobe Analytics. Durch eine geringe Anzahl vollständiger Ausführungen pro Monat (statt nur 3 Dimensionen für einige Analytics-Produkte) können Sie sehen, was die vollständige Beitragsanalyse für Sie leisten kann. |
| Wie funktionieren Token in der Beitragsanalyse? Kostet es ein Token, ein Projekt mit einer vorhandenen Beitragsanalyse zu laden, oder gilt dies nur für neue Ausführungen? | Jedes Anmeldeunternehmen (nicht jeder Benutzer) erhält eine bestimmte Anzahl an Token pro Monat, mit denen Sie eine „vollständige“ Beitragsanalyse in Analysis Workspace durchführen können.  Jedes Mal, wenn Sie eine neue Beitragsanalyse erstellen, bezahlen Sie ein Token. Das Laden von Projekten mit bereits ausgeführten Beitragsanalysen kostet kein Token. |
| Was kann ich tun, wenn mein Unternehmen keine Token mehr hat und zusätzliche Beitragsanalysen durchführen möchte? | Sie können ein Upgrade auf ein anderes Adobe Analytics-Produkt durchführen, z. B. von Standard (2 Token/Monat) auf Ultimate (20 Token/Monat). Man kann keine weiteren Token kaufen. Sie müssen das Upgrade innerhalb des vorhandenen Paketierungs-Frameworks durchführen. |
| Wie kann ich den Zugriff auf die Beitragsanalyse beschränken? | Standardmäßig haben nur Administratoren Zugriff auf die Ausführung von Beitragsanalysen. Administratoren können anderen Benutzern jedoch Zugriff gewähren, indem sie eine Berechtigungsgruppe in der [Adobe Admin Console](https://experienceleague.adobe.com/de/docs/analytics/admin/admin-console/home) erstellen. Erteilen Sie die Berechtigung zur Verwendung der Beitragsanalyse nur Benutzern, die einen legitimen Grund zu ihrer Verwendung haben und sich darauf verlassen können, dass sie ihren Zugriff nicht missbrauchen. Die Berechtigung lautet [!UICONTROL Beitragsanalyse] unter [!UICONTROL Report Suite-Werkzeuge]. [Weitere Infos](https://experienceleague.adobe.com/de/docs/analytics/admin/admin-console/permissions/report-suite-tools) |
| Wie weiß ich, wie viele Token mein Unternehmen pro Monat erhält und wie viele Token mein Unternehmen im aktuellen Monat verwendet hat? | Gehen Sie zu [!UICONTROL Admin] > [!UICONTROL Alle Administratoren] > [!UICONTROL Unternehmenseinstellungen] > [!UICONTROL Funktionszugriffsebenen anzeigen]. Schauen Sie unter<ul><li>Beitragsanalyse: Anzahl der monatlichen Nutzungs-Token</li><li>Beitragsanalyse: Anzahl der diesen Monat verwendeten Nutzungs-Token</li></ul> |

## Anomalieerkennung und Beitragsanalyse – Berechtigungen

Weiter unten finden Sie eine ausführliche Liste der Berechtigungen für die Anomalieerkennung und Beitragsanalyse in Analysis Workspace.

<table id="table_5C9B7E4AE82640B5A913519E576889B5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Adobe Analytics-Berechtigung </th> 
   <th colname="col2" class="entry"> Anomalieerkennung </th> 
   <th colname="col3" class="entry"> Beitragsanalyse </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Foundation </p> </td> 
   <td colname="col2"> <p>Nur nach Tagen </p> </td> 
   <td colname="col3" colsep="1"> <p>Keine Token </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://business.adobe.com/products/analytics/compare-adobe-analytics-packages.html?promoid=B4XQ3X7G&amp;mv=other"  >Select</a> </p> </td> 
   <td colname="col2"> <p>Nur nach Tagen </p> </td> 
   <td colname="col3"> <p>Keine Token </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://business.adobe.com/products/analytics/compare-adobe-analytics-packages.html?promoid=91BF51TR&amp;mv=other"  >Prime</a> </p> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>10 Token/Monat </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://business.adobe.com/products/analytics/compare-adobe-analytics-packages.html?promoid=8N4B5F1V&amp;mv=other"  > Ultimate</a> </p> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>20 Token/Monat </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Predictive Workbench-Add-on </p> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>Unbegrenzte Token </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Standard </p> 
    <ul id="ul_73D52020793B44868C9CE0F90893075D"> 
     <li id="li_21EE0871C87E43C8B781219B2BA0FA74">Adobe Analytics Core </li> 
     <li id="li_AB3593200F33439BAEE8FEB13CAE57F4">Adobe Analytics OD </li> 
     <li id="li_2B7D625519BC4A4CB598C95F15D3029B">Adobe Analytics MA </li> 
    </ul> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>2 Token/Monat </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Premium (360, Attribution) </p> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>2 Token/Monat </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Premium (Complete, <a href="https://business.adobe.com/products/analytics/predictive-analytics.html"  >Predictive Intelligence</a>) </p> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>Unbegrenzte Token </p> </td> 
  </tr> 
 </tbody> 
</table>
