---
title: Nach IP-Adresse ausschließen
description: Verhindern, dass von bestimmten IP-Adressen generierte Daten in Berichten angezeigt werden.
exl-id: 315a3000-f043-434b-a677-d111aeed7971
feature: Admin Tools
role: Admin
source-git-commit: d642bf8703d7c4c1545bfd9763c70ed8b1237eac
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 62%

---

# Nach IP-Adresse ausschließen

Daten von bestimmten IP-Adressen, z. B. von internen Websiteaktivitäten, Websitetests und der Verwendung durch Mitarbeiter, können aus Berichten ausgeschlossen werden. Durch das Ausschließen von Daten nach der IP-Adresse wird die Genauigkeit der Berichte erhöht. Zudem können Sie Daten entfernen, die auf DoS-Angriffen oder anderen böswilligen Ereignissen beruhen und Ihre Berichte verfälschen könnten.

Um Daten nach IP-Adresse auszuschließen, können Sie Ausschlüsse wie unten beschrieben konfigurieren oder [Firewall konfigurieren](/help/technotes/ip-addresses.md).

## Ausschlüsse nach IP-Adresse konfigurieren

>[!NOTE]
>
>Beachten Sie beim Konfigurieren von Ausschlüssen nach IP-Adresse Folgendes:
>
>* Treffer, die nach IP-Adresse ausgeschlossen sind, werden als [Server-Aufrufe](https://experienceleague.adobe.com/docs/analytics/technotes/terms.html?lang=de) in Rechnung gestellt.
>* Private IP-Adressen müssen nicht ausgeschlossen werden. Nur externe IP-Adressen gelangen zu den Adobe-Datenerfassungs-Servern. Private Adressen enthalten `10.*.*.*`, `192.168.*.*`, `172.[16-31].*.*` und `169.254.*.*`.
>* Sie können Platzhalterindikatoren (&#42;) verwenden, um einen Adressbereich auszuschließen. Zum Beispiel würde `[!DNL 0.0.*.0]` sämtliche IP-Adressen zwischen `[!DNL 0.0.0.0]` und `[!DNL 0.0.255.0]` ausschließen. Sie können bis zu 50 verschiedene IP-Adressen ausschließen.
* Daten von einer ausgeschlossenen IP-Adresse werden für alle neuen Treffer, die innerhalb von 5 Minuten nach dem Festlegen des Ausschlusses in das System gelangen, ausgeschlossen.
* Daten zu Treffern, die vor dem Zeitpunkt erfasst wurden, zu dem Änderungen an der IP-Adresse vorgenommen wurden, sind davon nicht betroffen.
>

So konfigurieren Sie Ausschlüsse nach IP-Adresse:

1. Wählen Sie in Adobe Analytics **[!UICONTROL Admin]** > **[!UICONTROL Alle Administratoren]** aus.

1. Wählen Sie auf der Seite Admin die Option **[!UICONTROL Nach IP ausschließen]** aus.




## Auswirkung der IP-Verschleierung {#section_51B7529FFF16449CA016FDC51D87E2CA}

Wenn die IP-Verschleierung aktiviert ist, wird der IP-Ausschluss durchgeführt, bevor die IP verschleiert wird. Kunden müssen also keine Änderungen vornehmen, wenn sie die IP-Verschleierung aktivieren.

Wenn das letzte Oktett entfernt wird, geschieht dies vor der IP-Filterung. Dabei wird das letzte Oktett mit „0“ ersetzt und die Regeln für den IP-Ausschluss sollten aktualisiert werden, sodass sie IP-Adressen mit einer Null am Ende berücksichtigen. Übereinstimmende &#42; sollten 0 entsprechen.
