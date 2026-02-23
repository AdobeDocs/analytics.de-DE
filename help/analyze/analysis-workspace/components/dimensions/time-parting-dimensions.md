---
description: Erfahren Sie, wie Zeitunterteilungsdimensionen den Zeitstempel erfasster Ereignisse in aussagekräftigere Dimensionen wie „Stunde des Tages“ oder „Tag der Woche“ unterteilen.
title: Dimensionen für die Zeitunterteilung
feature: Dimensions
role: User, Admin
exl-id: 92fbcc1e-1f7f-405a-8ad1-199fb7ba505e
source-git-commit: 8b1e25b9633b6db3e49da079f7014e6b7b595474
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 20%

---

# Dimensionen für die Zeitunterteilung

Bei der Zeitunterteilung wird der Zeitstempel erfasster Treffer in aussagekräftigere Dimensionen wie **Stunde des Tages** oder **Tag der Woche** unterteilt.


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Dimensionen für die Zeitunterteilung](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/analysis-workspace/building-freeform-tables/time-parting-dimensions-in-analysis-workspace){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]


Zeitunterteilungsdimensionen basieren auf der Zeitzone der Report Suite oder Virtual Report Suite. Diese Dimensionen sind in Analysis Workspace verfügbar und können bei der Beantwortung der folgenden Fragen helfen:

* Welcher Tageszeit können Besucher über einen großen Datumsbereich hinweg am häufigsten auf meine Site oder mein Programm zugreifen?
* Gibt es Tage der Woche oder Stunden des Tages, an denen die Konversion auf meiner Site oder in meiner App höher ist?
* Wie hoch sind meine Wochenendverkäufe im Vergleich zu meinen Wochenendverkäufen?
* Führt eine bestimmte Marketing-Kampagne zu höheren Konversionen am Morgen oder am Nachmittag?

>[!NOTE]
>
>Die Dimensionen für die Zeitunterteilung sind nur in Analysis Workspace verfügbar. Um Zeitunterteilungsdimensionen in anderen Analytics-Lösungen zu verwenden, können Sie das Plug-in [getTimeParting“ ](/help/implement/vars/plugins/gettimeparting.md).

Zu den Zeitunterteilungsdimensionen in Analysis Workspace gehören:

| Dimension | Beispielwerte |
| --- | --- |
| Stunde des Tages | 0–23 |
| Vormittag/Nachmittag | VORMITTAG, VORMITTAG |
| Wochentag | Montag, Dienstag, Mittwoch, Donnerstag, Freitag, Samstag, Sonntag |
| Wochenende/Wochentag | Wochenende, Wochentag |
| Tag des Monats | 1–31 |
| Monat des Jahres | Januar-Dezember |
| Tag des Jahres | 1–366 |
| Quartal des Jahres | Q1, Q2, Q3, Q4 |
