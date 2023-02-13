---
description: Mit internen URL-Filtern werden die Referrer, die Sie als seitenintern betrachten, gekennzeichnet. Dies hilft, Berichte zu Traffic-Quellen mit Daten zu füllen und internen Traffic zu filtern.
title: Interne URL-Filter
feature: Admin Tools
uuid: 70868edb-208d-4dad-9401-70967468d40c
exl-id: fa387da2-e9be-47c0-9c4e-edd75af1f05a
source-git-commit: 71ff81a0ae67c6f4cc9a8df567e27223cc63f18c
workflow-type: ht
source-wordcount: '212'
ht-degree: 100%

---


# Interne URL-Filter

Mit internen URL-Filtern werden die Referrer, die Sie als seitenintern betrachten, gekennzeichnet. Dies hilft, Berichte zu Traffic-Quellen mit Daten zu füllen und internen Traffic zu filtern.

**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Interne URL-Filter]**

Ein Referrer oder eine verweisende Seite ist normalerweise die Seite, von der aus Besucher Ihre Website aufgerufen haben. Um Datenverzerrungen zu vermeiden, können Sie interne Seiten als Referrer herausfiltern. Berichte schließen gefilterte Referrer aus   der Dimension [Referrers](/help/components/dimensions/referrer.md), der Dimension [Referrerdomänen](/help/components/dimensions/referring-domain.md) und anderen Traffic-Quellendimensionen aus.

Der häufigste Grund, aus dem Berichte zu Traffic-Quellen keine Daten enthalten, besteht darin, dass keine interne URL-Filterliste definiert ist. Gehen Sie wie folgt vor, um zu prüfen, welche internen URL-Filter für eine Report Suite festgelegt wurden. Entfernen Sie, um dies zu vermeiden, die Regel, die einen Punkt (.) als Filter enthält und fügen Sie Ihre eigene Site hinzu.

Ein Punkt ist der standardmäßige interne URL-Filter, damit Daten im Bericht „Seiten“ erfasst werden können. Wenn Treffer nicht mit den internen URL-Filtern übereinstimmen, werden alle Seiten als „Sonstige“ eingestuft. Ein Punkt befindet sich immer in der URL und garantiert daher, dass der Bericht „Seiten“ ausgefüllt wird.
