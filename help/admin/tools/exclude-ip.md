---
title: Nach IP-Adresse ausschließen
description: Verhindern, dass von bestimmten IP-Adressen generierte Daten in Berichten angezeigt werden.
exl-id: 315a3000-f043-434b-a677-d111aeed7971
feature: Admin Tools
role: Admin
source-git-commit: 4b4febd839682d88164b2f505245441d18ef2543
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 28%

---

# Nach IP-Adresse ausschließen

Daten von bestimmten IP-Adressen, z. B. von internen Websiteaktivitäten, Websitetests und der Verwendung durch Mitarbeiter, können aus Berichten ausgeschlossen werden. Das Ausschließen von Daten verbessert die Genauigkeit des Berichts, indem IP-Adressdaten ausgeschlossen werden. Darüber hinaus können Sie Daten aus DoS-Angriffen oder anderen böswilligen Ereignissen entfernen, die Berichtsdaten verfälschen können.

Um Daten nach IP-Adresse auszuschließen, können Sie Ausschlüsse wie unten beschrieben konfigurieren oder [Firewall konfigurieren](/help/technotes/ip-addresses.md).

## Ausschlüsse nach IP-Adresse konfigurieren

>[!NOTE]
>
>Beachten Sie beim Konfigurieren von Ausschlüssen nach IP-Adresse Folgendes:
>
>* Treffer, die nach IP-Adresse ausgeschlossen sind, werden als [Server-Aufrufe](/help/technotes/terms.md) in Rechnung gestellt.
>* Private IP-Adressen müssen nicht ausgeschlossen werden. Nur externe IP-Adressen gelangen zu den Adobe-Datenerfassungs-Servern. Private Adressen enthalten `10.*.*.*`, `192.168.*.*`, `172.[16-31].*.*` und `169.254.*.*`.
>* Sie können Platzhalterindikatoren (&#42;) verwenden, um einen Adressbereich auszuschließen. Zum Beispiel würde `[!DNL 0.0.*.0]` sämtliche IP-Adressen zwischen `[!DNL 0.0.0.0]` und `[!DNL 0.0.255.0]` ausschließen. Sie können bis zu 50 verschiedene IP-Adressen ausschließen.
>* Daten von einer ausgeschlossenen IP-Adresse werden für alle neuen Treffer, die innerhalb von 5 Minuten nach dem Festlegen des Ausschlusses in das System gelangen, ausgeschlossen.
>* Daten zu Treffern, die vor dem Zeitpunkt erfasst wurden, zu dem Änderungen an der IP-Adresse vorgenommen wurden, sind davon nicht betroffen. Der IP-Ausschluss gilt nur für Daten, die in Zukunft berücksichtigt werden.
>* Ausgeschlossene Treffer sind weiterhin in [Daten-Feeds](/help/export/analytics-data-feed/data-feed-overview.md) sichtbar (als `exclude_hit = 4` gekennzeichnet).

So konfigurieren Sie Ausschlüsse nach IP-Adresse:

1. Wählen Sie in Adobe Analytics **[!UICONTROL Admin]** > **[!UICONTROL Alle Administratoren]** aus.

1. Wählen Sie auf der Seite Admin die Option **[!UICONTROL Nach IP ausschließen]** aus.

## Auswirkungen der Verwendung von IP-Verschleierung mit IP-Ausschluss

Die Auswirkungen der Verwendung [IP-Verschleierung](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md) zusammen mit dem IP-Ausschluss hängen von den IP-Verschleierungseinstellungen der einzelnen Report Suites ab:

* **IP-Verschleierung (letztes Oktett)**: IP wird teilweise verschleiert, BEVOR der IP-Ausschluss ausgeführt wird. Stellen Sie sicher, dass die IP-Ausschlussregeln immer eine `0` als letztes Oktett erwarten (Platzhalter sind gültig, da sie `0` enthalten).
* **IP-Verschleierung (IP entfernen)**: IP wird nach Ausführung des IP-Ausschlusses vollständig verschleiert. Es sind keine Anpassungen der IP-Ausschlussregel erforderlich.
