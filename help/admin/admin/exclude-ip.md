---
title: Nach IP-Adresse ausschließen
description: Verhindern, dass von bestimmten IP-Adressen generierte Daten in Berichten angezeigt werden.
exl-id: 315a3000-f043-434b-a677-d111aeed7971
feature: Admin Tools
role: Admin
source-git-commit: 938795c7378cb1f0537ff84eddeab3feddf8d073
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 94%

---

# Nach IP-Adresse ausschließen

Daten von bestimmten IP-Adressen, z. B. von internen Websiteaktivitäten, Websitetests und der Verwendung durch Mitarbeiter, können aus Berichten ausgeschlossen werden. Durch das Ausschließen von Daten nach der IP-Adresse wird die Genauigkeit der Berichte erhöht. Zudem können Sie Daten entfernen, die auf DoS-Angriffen oder anderen böswilligen Ereignissen beruhen und Ihre Berichte verfälschen könnten. Die Ausschlüsse lassen sich wahlweise oder über die Firewall konfigurieren.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Alle Administratoren]** > **[!UICONTROL Nach IP ausschließen]**

>[!NOTE]
>
>Treffer, die nach IP-Adresse ausgeschlossen sind, werden als [Server-Aufrufe](https://experienceleague.adobe.com/docs/analytics/technotes/latency.html?lang=de) in Rechnung gestellt.

Sie können Platzhalterindikatoren (&#42;) verwenden, um einen Adressbereich auszuschließen. Zum Beispiel würde `[!DNL 0.0.*.0]` sämtliche IP-Adressen zwischen `[!DNL 0.0.0.0]` und `[!DNL 0.0.255.0]` ausschließen. Sie können bis zu 50 verschiedene IP-Adressen ausschließen.

>[!TIP]
>
>Private IP-Adressen müssen nicht ausgeschlossen werden. Nur externe IP-Adressen gelangen zu den Adobe-Datenerfassungs-Servern. Private Adressen enthalten `10.*.*.*`, `192.168.*.*`, `172.[16-31].*.*` und `169.254.*.*`.

## Auswirkung der IP-Verschleierung  {#section_51B7529FFF16449CA016FDC51D87E2CA}

Wenn die IP-Verschleierung aktiviert ist, wird der IP-Ausschluss durchgeführt, bevor die IP verschleiert wird. Kunden müssen also keine Änderungen vornehmen, wenn sie die IP-Verschleierung aktivieren.

Wenn das letzte Oktett entfernt wird, geschieht dies vor der IP-Filterung. Dabei wird das letzte Oktett mit „0“ ersetzt und die Regeln für den IP-Ausschluss sollten aktualisiert werden, sodass sie IP-Adressen mit einer Null am Ende berücksichtigen. Übereinstimmende &#42; sollten 0 entsprechen.
