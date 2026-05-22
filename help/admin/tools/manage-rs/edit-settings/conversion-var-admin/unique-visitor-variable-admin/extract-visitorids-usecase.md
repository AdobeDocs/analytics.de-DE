---
description: Data Warehouse bietet eine Funktion, mit der Sie eine Liste von Besucher-IDs extrahieren können. Bei diesen IDs handelt es sich nicht um Cookie-IDs, sondern um IDs, die Sie in einer Ihrer Konversionsvariablen erfassen. Obwohl es andere Möglichkeiten gibt, diese Informationen abzurufen, ist das folgende Beispiel eine Abkürzung zum Generieren einer Data Warehouse-Anfrage.
title: Verwendungsfall – Extrahieren von Besucher-IDs
feature: Admin Tools
role: Admin
exl-id: b1fc41af-31c7-42cd-aab7-0c659577781d
TQID: 'https://experienceleague.adobe.com/CUpKcu-jVNn77bkWM2mJvlLxYMyvfpRt4o-maC7tUBA'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: ff9b434a-2221-4df7-81d1-5bcbf5f80bceid: b8734a57-d5fb-44a8-8ee1-65225cecaeae
subfeature_v2: id: f47edbe0-f963-46ff-a667-71011396f5f3
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 399
ht-degree: 2%

---

# Verwendungsfall – Extrahieren von Besucher-IDs

Data Warehouse bietet eine Funktion, mit der Sie eine Liste von Besucher-IDs extrahieren können. Bei diesen IDs handelt es sich nicht um Cookie-IDs, sondern um IDs, die Sie in einer Ihrer Konversionsvariablen erfassen. Obwohl es andere Möglichkeiten gibt, diese Informationen abzurufen, ist das folgende Beispiel eine Abkürzung zum Generieren einer Data Warehouse-Anfrage.

Angenommen, Ihr Unternehmen sendet Marketing-E-Mails an Kunden und potenzielle Kunden. Jeder dieser E-Mail-Empfänger verfügt über eine eindeutige ID in Ihrem E-Mail-System (z. B. *`EMAIL Contact ID`*). Sie richten Ihre E-Mails so ein, dass Kontakte, die eine E-Mail erhalten und auf einen ihrer Links klicken, mit einer Kampagnen-ID und einer eindeutigen E-Mail-Kontakt-ID zu Ihrer Website gelangen. Ihr E-Mail-Link kann beispielsweise wie folgt aufgelöst werden:

```js
https://www.example.com/?cid=springmailblast&mid=1363660158
```

Durch das Festlegen dieser Variablen in Konversionsvariablen (eVars) können Sie sehen, wie jede E-Mail ausgeführt wurde (über die Kampagnen-ID) und wie oft jeder E-Mail-Empfänger die Website besucht hat (über die E-Mail-Kontakt-ID).

Angenommen, Sie erfassen diese IDs. Die meisten Marketing-Fachleute möchten ihr Website-Verhalten segmentieren und dann prüfen, ob sie an diejenigen weitervermarkten können, die bestimmte Kriterien erfüllen. Beispielsweise können Sie eine Remarketing-E-Mail an alle E-Mail-Empfänger senden, die von der E-Mail zu Ihrer Website gekommen sind und ein Website-Formular angezeigt (oder ausgefüllt) haben. Finden Sie dazu eine Möglichkeit, die E-Mail-Kontakt-IDs derjenigen zu identifizieren, die das spezifische Formular ausfüllen.

Eine Möglichkeit, dies zu tun, besteht darin, einen Konversions-Unterbeziehungsbericht zu verwenden, um den Wert der Formular-ID eVar nach der E-Mail-Kontakt-ID eVar aufzuschlüsseln. Dafür ist jedoch eine vorkonfigurierte Funktion mit Data Warehouse verfügbar. Mit dieser Funktion können Sie festlegen, welche eVar Ihre Unique User IDs speichert (in diesem Fall E-Mail-Kontakt-ID), und diese IDs mithilfe von Data Warehouse einfach extrahieren. Mithilfe dieser Funktion können Sie automatisch eine Data Warehouse-Anfrage erstellen, die die Unique-Visitor-IDs abruft, für die Sie Interesse haben.
