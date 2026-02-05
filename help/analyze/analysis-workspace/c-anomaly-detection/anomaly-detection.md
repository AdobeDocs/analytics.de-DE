---
description: Erfahren Sie mehr über die Erkennung von Datenanomalien in Analysis Workspace.
title: Anomalieerkennung – Überblick
feature: Anomaly Detection
role: User, Admin
exl-id: b1625206-c774-40ef-9d92-25ee8ff1478d
source-git-commit: fcc165536d77284e002cb2ba6b7856be1fdb3e14
workflow-type: ht
source-wordcount: '1292'
ht-degree: 100%

---

# Anomalieerkennung – Überblick

Datenanomalien können kontextbezogen in Analysis Workspace angezeigt und analysiert werden. Die Beitragsanalyse arbeitet in Verbindung mit der Anomalieerkennung, um herauszufinden, was zur Anomalie beigetragen hat.


>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Anomalieerkennung](https://video.tv.adobe.com/v/25444?quality=12&learn=on){target="_blank"} finden Sie ein Demovideo.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Kundinnen und Kunden von Adobe Analytics Select und Adobe Analytics Foundation haben in Workspace nur Zugriff auf die Anomalieerkennung mit *täglicher Granularität*. Weitere Informationen finden Sie unter [Anomalieerkennung und Beitragsanalyse – Berechtigungen](#anomaly-detection-and-contribution-analysis-entitlements).

## Anomalieerkennung

Die Anomalieerkennung bietet eine statistische Methode, mit der festgestellt wird, wie sich eine bestimmte Metrik in Bezug auf frühere Daten verändert hat.

Die Anomalieerkennung ermöglicht es Ihnen, „echte Signale“ von „Rauschen“ zu trennen und potenzielle Faktoren zu identifizieren, die zu diesen Signalen oder Anomalien beigetragen haben. Mit anderen Worten, sie hilft Ihnen zu unterscheiden, welche statistischen Schwankungen relevant sind und welche nicht. So können Sie dann die Ursache einer echten Anomalie identifizieren. Darüber hinaus können Sie zuverlässige Prognosen für Ihre Metrik (KPI) erhalten.

Beispiele für Anomalien, die Sie untersuchen können:

* Drastische Rückgänge beim durchschnittlichen Bestellwert
* Spitzen bei Bestellungen mit niedrigem Umsatz
* Spitzen oder Rückgänge bei Testregistrierungen
* Rückgänge bei Landingpage-Ansichten
* Spitzen bei Video-Pufferereignissen
* Spitzen bei niedrigen Video-Bitraten

Sowohl die Anomalieerkennung als auch die [Beitragsanalyse](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) sind Kern-Workflows in Analysis Workspace. Sie können die Beitragsanalyse für jede tägliche Anomalie ausführen und das Ergebnis in Ihr Analysis Workspace-Projekt einbetten.

Der Algorithmus zur Anomalieerkennung in Analysis Workspace umfasst

* Unterstützung für stündliche, wöchentliche und monatliche Granularität zusätzlich zur bestehenden täglichen Granularität.
* Berücksichtigung von Saisonalität (wie „Black Friday“) und Feiertagen.

## Beitragsanalyse

Die Beitragsanalyse erkennt versteckte Muster in Ihren Daten, mit denen sich statistische Anomalien erklären und Korrelationen

* für nicht erwartete Kundenaktionen,
* Wertbereichsüberschreitungen und
* plötzliche Spitzen oder Rückgänge

für ausgewählte Metriken in konvergenten Zielgruppensegmenten feststellen lassen.


>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Beitragsanalyse](https://video.tv.adobe.com/v/25443?quality=12&learn=on){target="_blank"} finden Sie ein Demovideo.

>[!ENDSHADEBOX]


Etwas ist passiert. Warum? Ihr Anomalieerkennungsbericht zeigt einen ungewöhnlichen Anstieg bei Bestellungen und Sie möchten wissen, wie es dazu kommt. Was ist Außergewöhnliches passiert? Wer reagiert auf welche Kampagne oder Empfehlung? Ist etwas viral gegangen? Welche spezifischen Faktoren haben zu dieser Anomalie beigetragen? Und womöglich die wichtigste Frage: Wie kann ich wichtige Informationen zu meinem Kunden erfassen und diese Performance wiederholen? (Oder: Wie kann ich in Zukunft einen Rückgang bei einer Metrik oder einen Anstieg bei einer negativen Metrik vermeiden?)

Mithilfe der Beitragsanalyse können Sie Ihre Daten umgehend analysieren und so herausfinden, wie es zu einer Anomalie kam. Sie schlüsselt die Faktoren, die zu einer Anomalie beigetragen haben, in Sekundenschnelle auf, was früher Wochen gedauert hätte, stellt Muster für Zielgruppensegmente bereit und hilft Ihnen, eine schlüssige Erzählweise für Kundeninteraktionen zu entwickeln. Sie können die Beitragsanalyse strategisch einsetzen, um aussagekräftige Zusammenhänge zu identifizieren und zu erfassen. Verwenden Sie diese Erkenntnisse anschließend strategisch für die Entwicklung neuer Zielgruppensegmente oder taktisch zur Identifizierung von Überschreitungen oder betrügerischen Aktivitäten, die einen Warnhinweis auslösen.

Die [Anomalieerkennung](#anomaly-detection) identifiziert Datenspitzen und extreme statistische Rückgänge basierend auf ausgewählten Metriken und Zielgruppensegmenten. Die Anomalieerkennung ermittelt eine historische Norm basierend auf einem Trainings-Zeitraum und stellt dann extreme Abweichungen dar, die mit spezifischen Ereignissen korrelieren. Die Anomalieerkennung kann einen rasanten Anstieg einer positiven Metrik „Bestellungen“ oder den Anstieg einer negativen Metrik „Bounces“ sowie Rückgänge bei beiden melden. Dabei werden statistisch relevante Datenpunkte für die Auswertung durch die Beitragsanalyse erfasst. Sobald eine statistische Anomalie identifiziert wurde, können Sie mit der Beitragsanalyse einen gezielten Drilldown durchführen und relevante Marketing- und Kampagnenvariablen über alle anomalen Datenpunkte hinweg bewerten. Dabei kommen erweiterte Algorithmen und maschinelle Lernprozesse zum Einsatz, um Zusammenhänge zu bewerten, die zu einer signifikanten Spitze oder einem Rückgang beigetragen haben. Diese Berechnungen werden dann in interaktiven Darstellungen angezeigt, die Ihnen unterschiedliche Perspektiven auf den Sachverhalt bieten. Auf diese Weise können Sie erkennen, warum etwas passiert ist und was dagegen unternommen werden kann.

Mithilfe der Beitragsanalyse können Sie eine schlüssige Erzählweise entwickeln, um zu beschreiben, warum eine Anomalie aufgetreten ist. Zudem erfahren Sie, wie Sie auf Anomalien reagieren können, indem Sie relevante Metriken erfassen und versteckte Faktoren identifizieren, die Ihnen ein Gesamtbild der Interaktionen der Zielgruppe und Trends bei Kundeninteressen vermitteln. Manchmal ist eine Anomalie leicht zu erkennen und zu korrigieren, wie zum Beispiel eine fehlerhafte Bestellung von 2.000 Kajaks. Manchmal ist dies komplex, z. B. wenn es darum geht, einen neuen Trend über einen bestimmten Zeitraum in einer Region zu identifizieren, der nur auf eine spezifische zielgerichtete Kampagne reagiert. Durch das Zusammenfügen von beitragenden Elementen aus verschiedenen Metriken für unterschiedliche Dimensionen und deren Zusammenhänge erhalten Sie einen Überblick über die Interaktionen Ihrer Zielgruppe und können Kontext für anomale Datenpunkte schaffen.

Im Folgenden finden Sie einige Anwendungsfälle:

* Identifizierung des Weitervermarktungspotenzials durch die Überwachung von Veränderungen bei der Produktnachfrage
* Optimierung des Kundenerlebnisses durch Reaktion auf spezifische Zielgruppeninteressen
* Frühe Identifizierung betrügerischer Bestellungen dank Anomalieberichten
* Schutz vor Industriespionage durch Identifikation hoher Auslastung und einer großen Anzahl an Downloads
* Überwachung von Vorgängen, z. B. Berichte zu fehlenden JavaScript-Tags.

Nach der umfassenden Analyse einer Anomalie wird eine Beitragszusammenfassung für die wichtigsten Elemente erstellt. Die Elemente werden darin in einer Rangfolge angeordnet, die auf der Gesamtzahl der Vorkommen und dem Prozentsatz des Elements an den beitragenden Faktoren basiert. Anhand der normalisierten Beitragsbewertung können Sie einen beitragenden Faktor ganz unkompliziert mit anderen wichtigen Dimensionselementen vergleichen und verbinden.

## Token für Beitragsanalyse

Alle Kundinnen und Kunden mit der Berechtigung für die Beitragsanalyse können eine vollständige Beitragsanalyse eine begrenzte Anzahl von Malen pro Monat in Analysis Workspace durchführen. Die Beitragsanalyse **schließt Folgendes aus:** Kundinnen und Kunden von Point Products (SiteCatalyst 15), Analytics Foundation und Analytics Select, die keine Berechtigung für die Beitragsanalyse haben.

Die Anzahl der Ausführungen pro Unternehmen ist durch monatliche Token begrenzt, die basierend auf dem von Ihrem Unternehmen erworbenen Adobe Analytics-Produkt gewährt werden. Die Anzahl der Ausführungen pro Unternehmen beinhaltet die Möglichkeit, den Zugriff auf die Beitragsanalyse einzuschränken, um Token-Missbrauch zu vermeiden.

## Häufig gestellte Fragen

| Frage | Antwort |
| --- | --- |
| Warum hat Adobe Token eingeführt? | Die Beitragsanalyse ist eine der beliebtesten Funktionen in Adobe Analytics. Indem Ihnen eine geringe Anzahl vollständiger Ausführungen pro Monat zur Verfügung steht (statt nur 3 Dimensionen bei einigen Analytics-Produkten), können Sie erleben, was die uneingeschränkte vollständige Beitragsanalyse für Sie leisten kann. |
| Wie funktionieren Token in der Beitragsanalyse? Kostet es ein Token, ein Projekt mit einer vorhandenen Beitragsanalyse zu laden, oder gilt dies nur für neue Ausführungen? | Jedes Anmeldeunternehmen (nicht jeder Benutzer) erhält eine bestimmte Anzahl an Token pro Monat, mit denen Sie eine „vollständige“ Beitragsanalyse in Analysis Workspace durchführen können.  Jedes Mal, wenn Sie eine neue Beitragsanalyse erstellen, bezahlen Sie ein Token. Das Laden von Projekten mit bereits ausgeführten Beitragsanalysen verbraucht keine Token. |
| Was kann ich tun, wenn mein Unternehmen keine Token mehr hat, aber zusätzliche Beitragsanalysen durchführen möchte? | Sie können auf ein anderes Adobe Analytics-Produkt aktualisieren, z. B. von Standard (2 Token/Monat) auf Ultimate (20 Token/Monat). Sie können keine weiteren Token kaufen. Eine Aktualisierung muss innerhalb der bestehenden Paketstruktur erfolgen. |
| Wie kann ich den Zugriff auf die Beitragsanalyse beschränken? | Standardmäßig haben nur Administratoren Zugriff auf die Ausführung von Beitragsanalysen. Administratoren können anderen Benutzern jedoch Zugriff gewähren, indem sie eine Berechtigungsgruppe in der [Adobe Admin Console](/help/admin/admin-console/home.md) erstellen. Erteilen Sie die Berechtigung zur Verwendung der Beitragsanalyse nur denjenigen Benutzenden, die einen legitimen Grund für die Verwendung haben und bei denen darauf vertraut werden kann, dass sie ihren Zugriff nicht missbräuchlich verwenden. Die Berechtigung lautet [!UICONTROL Beitragsanalyse] unter [!UICONTROL Report Suite-Werkzeuge]. [Weitere Infos](/help/admin/admin-console/permissions/report-suite-tools.md) |
| Woher weiß ich, auf wie viele Token mein Unternehmen pro Monat Anspruch hat und wie viele Token wir im laufenden Monat bereits verbraucht haben? | Gehen Sie zu [!UICONTROL Admin] > [!UICONTROL Alle Administratoren] > [!UICONTROL Unternehmenseinstellungen] > [!UICONTROL Funktionszugriffsebenen anzeigen]. Schauen Sie unter<ul><li>Beitragsanalyse: Anzahl der monatlichen Nutzungs-Token</li><li>Beitragsanalyse: Anzahl der diesen Monat verwendeten Nutzungs-Token</li></ul> |

## Anomalieerkennung und Beitragsanalyse – Berechtigungen

Weiter unten finden Sie eine ausführliche Liste der Berechtigungen für die Anomalieerkennung und Beitragsanalyse in Analysis Workspace.

<table id="table_5C9B7E4AE82640B5A913519E576889B5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Berechtigung für Adobe Analytics </th> 
   <th colname="col2" class="entry"> Anomalieerkennung </th> 
   <th colname="col3" class="entry"> Beitragsanalyse </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Foundation </p> </td> 
   <td colname="col2"> <p>Nur tägliche Granularität </p> </td> 
   <td colname="col3" colsep="1"> <p>Keine Token </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://business.adobe.com/products/analytics/compare-adobe-analytics-packages.html?lang=depromoid=B4XQ3X7G&amp;mv=other"  >Select</a> </p> </td> 
   <td colname="col2"> <p>Nur tägliche Granularität </p> </td> 
   <td colname="col3"> <p>Keine Token </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://business.adobe.com/products/analytics/compare-adobe-analytics-packages.html?lang=depromoid=91BF51TR&amp;mv=other"  >Prime</a> </p> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>10 Token pro Monat </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://business.adobe.com/products/analytics/compare-adobe-analytics-packages.html?lang=depromoid=8N4B5F1V&amp;mv=other"  > Ultimate</a> </p> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>20 Token pro Monat </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Add-on für Predictive Workbench </p> </td> 
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
   <td colname="col3"> <p>2 Token pro Monat </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Premium (360, Attribution) </p> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>2 Token pro Monat </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Premium (Complete, <a href="https://business.adobe.com/products/analytics/predictive-analytics.html?lang=de"  >Predictive Intelligence</a>) </p> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>Unbegrenzte Token </p> </td> 
  </tr> 
 </tbody> 
</table>
