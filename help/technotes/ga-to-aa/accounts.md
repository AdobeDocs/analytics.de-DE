---
title: Konten und Report Suites
description: Erfahren Sie, wie Sie mit einem Anmeldeunternehmen und einer Report Suite Datensilos in Adobe Analytics organisieren können.
exl-id: f4cf2a77-30c1-40f8-ba18-e4d71e170831
source-git-commit: f9b5380cfb2cdfe1827b8ee70f60c65ff5004b48
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 100%

---

# Konten und Report Suites

In Adobe Analytics gibt es zwei Ebenen, auf denen Datensilos organisiert werden:

* Ein **Anmeldeunternehmen** ist eine übergreifende Organisation, die eine oder mehrere Report Suites enthält. Ein Anmeldeunternehmen ähnelt *Konten* in anderen Analyse-Tools wie Google Analytics. Berater, die mit mehreren Unternehmen zusammenarbeiten, haben normalerweise Zugriff auf mehrere Anmeldeunternehmen.
* Eine **Report Suite** ist ein Repository, über das Sie Daten senden und Berichte abrufen. Eine Report Suite enthält in der Regel Daten von einer Website, dies liegt jedoch im Ermessen der Implementierung des jeweiligen Unternehmens. Eine Report Suite ähnelt einer *Ansicht* in anderen Analyse-Tools.

Größere Unternehmen verfügen in der Regel über mehrere Report Suites – eine für jede Website oder App. Wenden Sie sich an einen Administrator in Ihrem Unternehmen, wenn Sie nicht sicher sind, welche Report Suite Sie zum Abrufen der Daten verwenden sollten.

Ein wichtiger Unterschied zwischen der Datenerfassungsmethode von Adobe und vielen anderen Tools besteht darin, dass Sie angeben, an welche Report Suites Daten in Ihrer Implementierung gesendet werden sollen. Das unterscheidet sich von anderen Werkzeugen, die normalerweise alle Daten an einen Erfassungsort senden und diese dann nach Ansichten oder Profilen filtern.

[!UICONTROL Virtual Report Suites] stehen auch in Adobe Analytics zur Verfügung. Sie ermöglichen eine gefilterte Ansicht einer Report Suite ohne Änderung der Datenerfassung oder der Verlaufsdaten. Sie können beispielsweise eine [!UICONTROL Virtual Report Suite] verwenden, um Bot-Traffic zu eliminieren, der zuvor nicht erfasst wurde, oder um betrügerische/ausreißende Umsätze auszuschließen. Weitere Informationen finden Sie unter [Virtual Report Suites](/help/components/vrs/vrs-about.md) im Benutzerhandbuch zu Komponenten.
