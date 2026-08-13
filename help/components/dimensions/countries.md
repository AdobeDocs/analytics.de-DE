---
title: Länder
description: Das Land, aus dem der Treffer stammt.
feature: Dimensions
exl-id: 47704b08-215d-4d2d-bcd4-1789e308c1c6
TQID: https://experienceleague.adobe.com/qEG8tKa7eEuYV6XgYSlf4Y8FPaCiyWxPmdtL6KkKm94
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 324
ht-degree: 65%

---

# Länder

Die Dimension „Länder[&#x200B; gibt &#x200B;](overview.md) Land an, aus dem der Treffer stammt. Diese Dimension ist nützlich, um die beliebtesten Länder zu ermitteln, aus denen die Besucher beim Besuch Ihrer Website stammen. Sie können diese Daten verwenden, um sich auf die Marketing-Maßnahmen in diesen Ländern zu konzentrieren, oder sicherstellen, dass Ihr Site-Erlebnis in Ländern mit unterschiedlichen Primärsprachen optimal ist.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf interne Suchregeln von Adobe. Der Suchwert basiert auf der mit dem Treffer gesendeten IP-Adresse. Adobe arbeitet mit [Digital Element](https://www.digitalelement.com/) zusammen, um die Suche zwischen IP-Adresse und Land zu unterstützen.

* Bei AppMeasurement-Implementierungen ist diese Dimension vorkonfiguriert.
* Aktivieren Sie für Web SDK-Implementierungen [!UICONTROL Geo-Suche] beim [Konfigurieren eines Datenstroms](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de).

## Dimensionselemente

Zu den Dimensionselementen gehören Länder auf der ganzen Welt. Zu den Beispielwerten gehören `"United States"`, `"United Kingdom"` oder `"India"`.

## Unterschiede zwischen gemeldetem und tatsächlichem Standort

Da diese Dimension auf der IP-Adresse basiert, kann in einigen Szenarien ein Unterschied zwischen dem gemeldeten und dem tatsächlichen Standort anzeigt werden:

* **IP-Adressen, die Unternehmensproxys darstellen**: Diese Besucher können als Traffic erscheinen, der über das Unternehmensnetzwerk des Benutzers kommt. Dies kann ein anderer Standort sein, wenn der Benutzer remote arbeitet.
* **Mobile IP-Adressen**: Die mobile IP-Zielerfassung funktioniert auf unterschiedlichen Ebenen, je nach Standort und Netzwerk. Einige Fluggesellschaften befördern den IP-Verkehr über zentrale oder regionale Anlaufstellen.
* **Satelliten-ISP-Benutzer**: Es ist schwierig, den spezifischen Standort dieser Benutzer zu identifizieren, da sie in der Regel vom Uplink-Standort zu stammen scheinen.
* **Militärische und staatliche IPs**: Die Mitarbeiter sind weltweit unterwegs und der Zugriff erfolgt eher über ihren Heimatstandort als von der Basis oder der Behörde aus, in der sie gegenwärtig beschäftigt sind.
* **Proxys, die IP-Adressen aus Datenschutzgründen verdecken**: Services wie das Private Relay von Apple verbergen die wahre IP-Adresse, indem sie zufällig Daten über einen Vermittler oder Proxy senden. Dieser Proxy ersetzt dann eine andere IP-Adresse, bevor er an Adobe weitergeleitet wird.
