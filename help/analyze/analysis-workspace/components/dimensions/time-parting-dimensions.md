---
description: Erfahren Sie, wie Zeitunterteilungsdimensionen den Zeitstempel erfasster Ereignisse in aussagekräftigere Dimensionen wie „Stunde des Tages“ oder „Tag der Woche“ unterteilen.
title: Dimensionen für die Zeitunterteilung
feature: Dimensions
role: User, Admin
exl-id: 92fbcc1e-1f7f-405a-8ad1-199fb7ba505e
TQID: https://experienceleague.adobe.com/bQVBmv3KhaDZtmUXSOY3UsustpCZKAwJ8rH9Qv49Rfw
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2:
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 266
ht-degree: 18%

---

# Dimensionen für die Zeitunterteilung

Bei der Zeitunterteilung wird der Zeitstempel erfasster Treffer in aussagekräftigere Dimensionen wie **Stunde des Tages** oder **Tag der Woche** unterteilt.


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Dimensionen für die Zeitunterteilung](https://experienceleague.adobe.com/de/docs/analytics-learn/tutorials/analysis-workspace/building-freeform-tables/time-parting-dimensions-in-analysis-workspace){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]


Zeitunterteilungsdimensionen basieren auf der Zeitzone der Report Suite oder Virtual Report Suite. Diese Dimensionen sind in Analysis Workspace verfügbar und können bei der Beantwortung der folgenden Fragen helfen:

* Welcher Tageszeit können Besucher über einen großen Datumsbereich hinweg am häufigsten auf meine Site oder mein Programm zugreifen?
* Gibt es Tage der Woche oder Stunden des Tages, an denen die Konversion auf meiner Site oder in meiner App höher ist?
* Wie hoch sind meine Wochenendverkäufe im Vergleich zu meinen Wochenendverkäufen?
* Führt eine bestimmte Marketing-Kampagne zu höheren Konversionen am Morgen oder am Nachmittag?

>[!NOTE]
>
>Die Dimensionen für die Zeitunterteilung sind nur in Analysis Workspace verfügbar. Um Zeitunterteilungsdimensionen in anderen Analytics-Lösungen zu verwenden, können Sie das Plug-in [getTimeParting“ &#x200B;](/help/implement/vars/plugins/gettimeparting.md).

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
