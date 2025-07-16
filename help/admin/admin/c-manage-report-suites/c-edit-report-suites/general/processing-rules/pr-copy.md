---
title: Kopieren von Verarbeitungsregeln
description: Erfahren Sie, wie Sie Verarbeitungsregeln von einer Report Suite in eine andere kopieren.
feature: Processing Rules
role: Admin
source-git-commit: 0bed2622f54bf2f46aa57dbfad7bd55a61d6c7d0
workflow-type: tm+mt
source-wordcount: '253'
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
