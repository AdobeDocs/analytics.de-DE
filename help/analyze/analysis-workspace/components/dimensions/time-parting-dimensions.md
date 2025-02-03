---
description: Bei einer Zeitunterteilung wird der Zeitstempel erfasster Hits in aussagekräftigere Dimensionen wie „Stunde des Tages“ oder „Tag der Woche“ unterteilt.
title: Dimensionen für die Zeitunterteilung
feature: Dimensions
role: User, Admin
exl-id: 92fbcc1e-1f7f-405a-8ad1-199fb7ba505e
source-git-commit: d7a6867796f97f8a14cd8a3cfad115923b329c7c
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 96%

---

# Dimensionen für die Zeitunterteilung

Bei einer Zeitunterteilung wird der Zeitstempel erfasster Hits in aussagekräftigere Dimensionen wie „Stunde des Tages“ oder „Tag der Woche“ unterteilt.


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Time=Parting Dimensions](https://video.tv.adobe.com/v/23727?quality=12&learn=on){target="_blank"} für ein Demo-Video.

>[!ENDSHADEBOX]


Die Dimensionen für die Zeitunterteilung basieren auf der Zeitzone der Report Suite bzw. der virtuellen Report Suite. Diese Dimensionen sind in Analysis Workspace verfügbar und können bei der Beantwortung der folgenden Fragen hilfreich sein:

* Welches ist in einem umfangreichen Datumsbereich die bevorzugte Tageszeit, zu der Besucher meine Site oder Anwendung aufrufen?
* Gibt es Wochentage oder Zeiten, an bzw. zu denen auf meiner Site oder in meiner Anwendung mehr Konversionen erfolgen?
* Wie verhalten sich Verkäufe am Wochenende in Bezug auf Verkäufe während der Woche?
* Führt eine bestimmte Marketing-Kampagne eher am Morgen oder am Nachmittag zu einer höheren Konversionsrate?

>[!NOTE]
>
>Die Dimensionen für die Zeitunterteilung sind nur in Analysis Workspace verfügbar. Wenn Sie Dimensionen für die Zeitunterteilung in anderen Analytics-Lösungen verwenden möchten, können Sie das [getTimeParting-Plug-in](https://experienceleague.adobe.com/docs/analytics/implementation/vars/plugins/gettimeparting.html?lang=de) implementieren.

Zu den Dimensionen für die Zeitunterteilung in Analysis Workspace zählen:

| Dimension | Beispielwerte |
| --- | --- |
| Stunde des Tages | 0–23 |
| Vormittag/Nachmittag | Vormittag (AM), Nachmittag (PM) |
| Wochentag | Montag, Dienstag, Mittwoch, Donnerstag, Freitag, Samstag, Sonntag |
| Wochenende/Wochentag | Wochenende, Wochentag |
| Tag des Monats | 1–31 |
| Monat des Jahres | Januar bis Dezember |
| Tag des Jahres | 1–366 |
| Quartal des Jahres | Q1, Q2, Q3, Q4 |
