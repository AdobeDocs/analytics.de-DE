---
description: Erfahren Sie mehr zu häufig gestellte Fragen zu Report Builder.
title: Häufig gestellte Fragen zu Report Builder
feature: Report Builder
role: User, Admin
exl-id: 86604d39-2965-45a5-98ab-3ee4adcb7f97
TQID: https://experienceleague.adobe.com/vFQWGX3ojl070mQIg7GXhY87kxC-7d0dlYl-0rFU9Uk
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: ac8a38fa-dec3-4581-8f64-178fde9f64e8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 474
ht-degree: 100%

---

# Häufig gestellte Fragen zu Report Builder

{{legacy-arb}}

Häufig gestellte Fragen rund um Report Builder.

## Kann ich die Funktion `TODAY()` oder `DATERANGE()` in Arbeitsmappen verwenden? {#today}

Die [`TODAY()`-Funktion](https://support.microsoft.com/de-de/office/today-function-5eb3078d-a82c-4736-8930-2f51a028fdd9) in Excel gibt den aktuellen Tag zurück. Die [`DATEVALUE()`-Funktion](https://support.microsoft.com/de-de/office/datevalue-function-df8b07d4-7761-4a93-bc33-b7471bbff252) wandelt eine Datumszeichenfolge in einen seriellen Wert um. Obwohl diese Funktionen für viele Funktionalitäten in Excel hilfreich sind, empfiehlt Adobe dringend, diese Funktionen nicht als Teil geplanter Report Builder-Anfragen zu verwenden. Die Adobe-Kundenunterstützung unterstützt keine Anfragen zur Fehlerbehebung mit einer dieser Funktionen.

Terminierte Berichte werden auf Servern verarbeitet, die wahrscheinlich nicht die gleichen Zeitzonen haben wie die Report Suite. Die Funktion `TODAY()`, die ein Benutzer erwartet, und die Funktion `TODAY()`, die der Verarbeitungs-Server verwendet, können häufig unterschiedlich sein. Außerdem basiert das verwendete Datum auf dem Beginn der Verarbeitung. Wenn mehrere Berichte gleichzeitig ausgeführt werden, kann sich aufgrund von Verzögerungen das Datum zwischen der angeforderten Zeit und dem Beginn der Verarbeitung ändern. Dieses Problem tritt auf, wenn die geplante Zeit nahe um Mitternacht liegt.

Terminierte Berichte werden auch auf Servern verarbeitet, die wahrscheinlich keine Datumssyntax verwenden. Zum Beispiel kann `7/1/YYYY` je nach Land oder Region auf den 1. Juli oder den 7. Januar verweisen. Die Anwendung der Funktion `DATEVALUE()` auf dieses Datum würde zu unterschiedlichen seriellen Werten führen, je nachdem, welcher Computer die Funktion ausführt.

Als Alternative zu diesen Excel-Funktionen empfiehlt Adobe dringend die Verwendung von Datumsbereichen innerhalb von Report Builder-Anfragen. Wählen Sie auf der ersten Seite des Anfrage-Assistenten in der Dropdown-Liste **[!UICONTROL Vordefinierte Datumswerte]** und dann unter „Häufig verwendete Datumswerte“ die Option **[!UICONTROL Heute]** oder einen anderen gewünschten Datumsbereich aus. Bei dieser Einstellung wird die Zeit der Report Suite zum Zeitpunkt der Ausführung berücksichtigt und nicht die Zeit, zu der der Server die Anforderung verarbeitet.

## Wie groß und komplex kann ich meine Arbeitsmappen machen? {#complexity}

Report Builder unterstützt Arbeitsmappen bis zu den folgenden Grenzen:

* **1.000 Anfragen**: Eine einzelne Arbeitsmappe kann bis zu 1.000 Datenanfragen enthalten. Wenn Sie Berichte oder Projekte haben, für die mehr als 1000 Anforderungen erforderlich sind, empfiehlt Adobe, diese in mehrere Arbeitsmappen aufzuteilen.
* **20.000 Anfragen pro Stunde und Firma**: Report Builder verwendet die Analytics-Reporting-API zum Abrufen von Daten. Jede einzelne Anfrage verwendet einen API-Aufruf, wenn sie erstellt oder aktualisiert wird. Wenn sich für Ihr Unternehmen mehr als 20.000 API-Aufrufe in einer bestimmten Stunde ansammeln, müssen Sie bis zur nächsten Stunde warten, um die Daten erneut abzurufen.
* **Vierstündige Verarbeitungszeit**: Terminierte Berichte werden beendet, wenn deren Verarbeitung mehr als vier Stunden dauert. Wenn Ihre Arbeitsmappe viele komplexe Anfragen mit großen Datensätzen enthält, kann der terminierte Bericht fehlschlagen.

## Woher weiß ich, ob ich Zugriff auf Report Builder habe? {#access}

Ihre bzw. Ihr Adobe Analytics-Admin muss Ihnen Zugriff auf Report Builder gewähren. Die oder der Admin richtet Produktprofile in [Adobe Admin Console](/help/admin/admin-console/home.md) ein. Bitten Sie die oder den Admin, Ihnen Zugriff zu erteilen.
