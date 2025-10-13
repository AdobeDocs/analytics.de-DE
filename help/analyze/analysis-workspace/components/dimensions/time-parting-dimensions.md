---
description: Erfahren Sie, wie Zeitunterteilungsdimensionen den Zeitstempel erfasster Ereignisse in aussagekräftigere Dimensionen wie „Stunde des Tages“ oder „Tag der Woche“ unterteilen.
title: Dimensionen für die Zeitunterteilung
feature: Dimensions
role: User, Admin
exl-id: 92fbcc1e-1f7f-405a-8ad1-199fb7ba505e
source-git-commit: fcc165536d77284e002cb2ba6b7856be1fdb3e14
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 74%

---

# Dimensionen für die Zeitunterteilung

Bei der Zeitunterteilung wird der Zeitstempel erfasster Treffer in aussagekräftigere Dimensionen wie **Stunde des Tages** oder **Tag der Woche** unterteilt.


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Dimensionen für die Zeitunterteilung](https://video.tv.adobe.com/v/23727?quality=12&learn=on){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]


Die Dimensionen für die Zeitunterteilung basieren auf der Zeitzone der Report Suite bzw. der virtuellen Report Suite. Diese Dimensionen sind in Analysis Workspace verfügbar und können bei der Beantwortung der folgenden Fragen hilfreich sein:

* Welches ist in einem umfangreichen Datumsbereich die bevorzugte Tageszeit, zu der Besucher meine Site oder Anwendung aufrufen?
* Gibt es Wochentage oder Zeiten, an bzw. zu denen auf meiner Site oder in meiner Anwendung mehr Konversionen erfolgen?
* Wie verhalten sich Verkäufe am Wochenende in Bezug auf Verkäufe während der Woche?
* Führt eine bestimmte Marketing-Kampagne eher am Morgen oder am Nachmittag zu einer höheren Konversionsrate?

>[!NOTE]
>
>Die Dimensionen für die Zeitunterteilung sind nur in Analysis Workspace verfügbar. Wenn Sie Dimensionen für die Zeitunterteilung in anderen Analytics-Lösungen verwenden möchten, können Sie das [getTimeParting-Plug-in](/help/implement/vars/plugins/gettimeparting.md) implementieren.

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
