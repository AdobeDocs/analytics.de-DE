---
title: Ausschließen von Daten in Adobe Analytics
description: Lernen Sie verschiedene Methoden kennen, wie Sie Daten sowohl vor als auch nach der Datenerfassung ausschließen können.
exl-id: dee5bf3b-8bb3-48eb-908d-b4a981f17bfb
feature: Data Configuration and Collection
role: Admin
TQID: https://experienceleague.adobe.com/EVXvZGgeAPTcUUd035DgBAyU38hKNh8xU7nX3g7aY7o
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 356
ht-degree: 96%

---

# Ausschließen von Daten in Adobe Analytics

Das Ausschließen von Daten wird häufig verwendet, um zu verhindern, dass die Testaktivitäten Ihres Unternehmens in die Produktionsdaten einfließen, oder um zu verhindern, dass unerwünschte Daten die Berichte fälschlicherweise aufblähen. Verwenden Sie eine der folgenden Methoden, um Daten aus Adobe Analytics je nach Anwendungsfall auszuschließen.

## Daten nach der Datenerfassung ausschließen

Mit den folgenden Methoden können Sie Daten im Analytics-Reporting ausschließen, nachdem die Datenerfassungs-Server von Adobe Bildanforderungen empfangen haben. Daten, die mit diesen Methoden ausgeschlossen wurden, werden weiterhin für abrechnungsfähige Server-Aufrufe gezählt.

* **Nach IP ausschließen**: Adobe Analytics bietet grundlegende Funktionen zum Ausschließen von Daten für IP-Adressen oder Bereiche in einer Report Suite. Siehe [Nach IP ausschließen](/help/admin/tools/exclude-ip.md) im Admin-Benutzerhandbuch.
* **Bot-Regeln**: Bot-Regeln nehmen Traffic, der zu bekannten Zeichenfolgen von Bot-Benutzeragenten gehört, und schließen ihn aus Analytics-Berichten aus. Daten, die über Bot-Regeln ausgeschlossen werden, werden im Bots-Bericht platziert. Es können benutzerdefinierte Bot-Regeln erstellt werden, um zusätzliche Daten auszuschließen. Weitere Informationen finden Sie im Admin-Benutzerhandbuch unter [Bot-Regeln](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md).
* **VISTA-Regeln**: Je nach Bedarf Ihres Unternehmens werden Treffer, die Ihren Anforderungen entsprechen, an eine andere Report Suite gesendet, die speziell zum Empfang ausgeschlossener Daten verwendet wird. VISTA-Regeln werden häufig in Bezug auf IP-Adressen verwendet, sind jedoch nicht auf sie beschränkt. Sie können beliebige Dimensionen verwenden, um Daten in Report Suites ein- oder auszuschließen. VISTA-Regeln verursachen zusätzliche Kosten. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.
* **Ausschluss-Cookies**: Alle Besucher Ihrer Site können sich freiwillig gegen das Tracking in Adobe Analytics entscheiden, indem sie eine für Ihren Tracking-Server spezifische Seite besuchen. Siehe [Implementieren von Abmelde-Links](/help/implement/js/opt-out.md) im Implementierungs-Benutzerhandbuch.

>[!TIP]
>
>Verarbeitungsregeln können keine Daten ausschließen oder Daten an eine andere Report Suite senden. Bestimmte Variablen können jedoch bedingt festgelegt werden und ein Segment kann verwendet werden, um diese Daten vom Reporting auszuschließen.

## Daten vor der Datenerfassung ausschließen

Wenn Sie verhindern möchten, dass bestimmte Treffer die Datenerfassungs-Server von Analytics erreichen, verwenden Sie die Variable [`abort`](/help/implement/vars/config-vars/abort.md). Diese Kennzeichnung verhindert, dass die Bildanforderung gesendet wird. Abrechnungsfähige Server-Aufrufe werden für abgebrochene Bildanforderungen nicht mitgerechnet, da sie keine Datenerfassungs-Server von Adobe erreichen.
