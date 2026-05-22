---
title: Kopieren von Verarbeitungsregeln
description: Erfahren Sie, wie Sie Verarbeitungsregeln von einer Report Suite in eine andere kopieren.
feature: Processing Rules
role: Admin
exl-id: bb34ecac-0512-4cff-9ef0-72db2dcabc03
TQID: 'https://experienceleague.adobe.com/x7mG1fjpNiPn0x6No0RtEz4aJLcN2t7wpUkJ-0LQxII'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
subfeature_v2:
  - id: fbaf7f9a-8341-44f6-aa57-6c8d50741804
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b4dd41a7-ccf8-4e9d-918e-acaab534a307
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 253
ht-degree: 0%

---

# Kopieren von Verarbeitungsregeln zwischen Report Suites

Durch Kopieren von Verarbeitungsregeln können Sie dieselbe Logik nicht manuell in mehreren Report Suites neu erstellen. Mit der Kopierfunktion können Sie Verarbeitungsregeln problemlos für viele Report Suites freigeben oder getestete Funktionen von einer Entwicklungs-Report Suite in eine Produktions-Report Suite kopieren.

**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Report Suite auswählen > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Verarbeitungsregeln]** > **[!UICONTROL Verarbeitungsregeln kopieren]**

Diese Schnittstelle bietet zwei Optionen:

* **Alle Verarbeitungsregeln ersetzen**: Diese Option löscht alle Verarbeitungsregeln aus der Ziel-Report Suite und fügt dann alle Verarbeitungsregeln in derselben Reihenfolge zur Ziel-Report Suite hinzu. Es kann keine begrenzte Anzahl von Verarbeitungsregeln zum Ersetzen ausgewählt werden.
* **Spezifische Verarbeitungsregeln anhängen**: Mit dieser Option können Sie eine oder mehrere Verarbeitungsregeln auswählen. Angefügte Regeln werden in jeder Ziel-Report Suite am Ende der Liste der Verarbeitungsregeln hinzugefügt. Erwägen Sie die Reihenfolge der Verarbeitungsregeln und die bereits vorhandenen Regeln, wenn Sie Regeln an jede Ziel-Report Suite anhängen.

Bei der Auswahl von Verarbeitungsregeln, an die angehängt werden soll, oder Report Suites, an die kopiert werden soll, können Sie mit `Ctrl`/`Cmd` + `Click` mehrere Verarbeitungsregeln oder Report Suites auswählen. Nachdem Sie die gewünschten Report Suites zum Kopieren ausgewählt haben, klicken Sie auf **[!UICONTROL Kopieren]** und bestätigen Sie das angezeigte modale Fenster.

>[!WARNING]
>
>Verarbeitungsregeln wirken sich direkt auf die Datenerfassung aus und können bei falscher Verwendung zu Datenverlust führen. Testen Sie Verarbeitungsregeln immer in einer Entwicklungs-Report Suite, bevor Sie sie in eine Produktions-Report Suite kopieren, um Datenqualitätsprobleme zu minimieren.
