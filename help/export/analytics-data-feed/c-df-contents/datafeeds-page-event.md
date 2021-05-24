---
description: Suchtabelle zur Bestimmung der Art eines Treffers auf der Grundlage des Werts „page_event“.
keywords: Daten-Feed, Seite, Ereignis, „page_event“, „post_page_event“
title: Seitenereignissuche
feature: Grundlagen zu Reports & Analytics
uuid: 73af597c-5560-466e-94b2-ddd1d64797c8
exl-id: ef0467df-b94b-4cec-b312-96d8f42c23b0
source-git-commit: cddf2a76ca36914f133379959b7cbb5246bdd695
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 100%

---

# Seitenereignissuche

Suchtabelle zur Bestimmung der Art eines Treffers auf der Grundlage des Werts „page_event“.

| Treffertyp | Wert `page_event` | Wert `post_page_event` |
| --- | --- | --- |
| Seitenansichten | 0: Alle Seitenansichtsaufrufe und `trackState`-Aufrufe von mobilen SDKs | Gleicher Wert wie `post_page_event` |
| Linktracking | 10: Benutzerspezifische Links und `trackAction`-Aufrufe in mobilen SDKs<br>11: Downloadlinks<br>12: Exitlinks | 100: Benutzerspezifische Links und `trackAction`-Aufrufe in mobilen SDKs<br>101: Downloadlinks<br>102: Exitlinks |
| Meilenstein-Video | 31: Medienstart<br>32: Medienaktualisierungen (keine andere Variablenverarbeitung)<br>33: Medienaktualisierungen (mit anderen Variablen) | 76: Medienstart<br>77: Medienaktualisierungen (keine andere Variablenverarbeitung)<br>78: Medienaktualisierungen (mit anderen Variablen) |
| Heartbeat-Video | 50: Medien-Stream-Start (nicht Primetime)<br>51: Medien-Stream-Beendigung (nicht Primetime)<br>52: Medien-Stream-Scrubbing (nicht Primetime)<br>53: Medien-Stream-Fortsetzung (nicht Primetime)<br>54: Medien-Stream-Anzeigenstart (nicht Primetime)<br>55: Medien-Stream-Anzeigenbeendigung (nicht Primetime)<br>56: Medien-Stream-Anzeigen-Scrubbing (nicht Primetime)<br>60: Medien-Stream-Start (Primetime)<br>61: Medien-Stream-Beendigung (Primetime)<br>62: Medien-Stream-Scrubbing (Primetime)<br>63: Medien-Stream-Fortsetzung (Primetime)<br>64: Medien-Stream-Anzeigenstart (Primetime)<br>65: Medien-Stream-Anzeigenbeendigung (Primetime)<br>66: Medien-Stream-Anzeigen-Scrubbing (Primetime) | Gleicher Wert wie `post_page_event` |
| Umfrage | 40: Jeder Aufruf, der aus der Umfrage generiert wurde | 80: Jeder Aufruf, der aus der Umfrage generiert wurde |
| Analytics for Target | 70: Treffer enthält Target-Aktivitätsdaten | Gleicher Wert wie `post_page_event` |
