---
title: Klassifizierungssätze – Übersicht
description: Verwenden Sie Klassifizierungssätze zum Verwalten von Klassifizierungsdaten.
exl-id: a139b298-1188-42ce-b52f-c71e0ff7c4e3
source-git-commit: 34ba0e09cd909951a777b0ad3da080958633f97e
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 100%

---

# Klassifizierungssätze – Übersicht

Klassifizierungssätze bieten eine einzige Oberfläche zum Verwalten von Klassifizierungen und Regeln. Dieser Workflow kombiniert das Konzept der Erstellung von Klassifizierungen in den Report Suite-Einstellungen mit dem Konzept des Classification Importer, um eine intuitivere Benutzeroberfläche zum Erstellen und Verwalten von Klassifizierungsdaten zu bieten.

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]**

Die Backend-Architektur, die mit Klassifizierungs-Sets veröffentlicht wurde, enthält einige wichtige Verbesserungen:

* deutlich verkürzte Verarbeitungszeit (72 Stunden → 24 Stunden)
* Möglichkeit zur Verwendung der Benutzeroberfläche für Klassifizierungs-Sets
* Die Option, Klassifizierungsdaten in Adobe Experience Platform künftig über den [Adobe Analytics-Quell-Connector für Klassifizierungsdaten](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/classifications.html?lang=de) zu verwenden

Die Backend-Architektur, die mit Klassifizierungs-Sets veröffentlicht wurde, enthält auch einige wichtige Änderungen:

* Bei Verwendung des Browsers oder FTP-Imports ist [!UICONTROL Bei Konflikt überschreiben] immer aktiviert.
* Bei Verwendung des Browser- oder FTP-Imports wird die Option zum sofortigen Export nach dem Import nicht mehr unterstützt. Exporte müssen separat initiiert werden.
* Die Analytics 2.0-API `GetDimensions`-Endpunkt gibt jetzt Zeichenfolgenkennungen für Klassifizierungen anstelle numerischer Kennungen zurück. Numerische Kennungen können zwar weiterhin verwendet werden, Adobe empfiehlt jedoch, nach Möglichkeit die neuen Zeichenfolgenkennungen zu verwenden. Numerische Kennungen können mithilfe der `?expansion=hidden` Abfragezeichenfolgen-Parameter abgerufen werden.


Klassifizierungssätze bestehen aus zwei Hauptbereichen:

* [**[!UICONTROL Classification Sets Manager]**](set-manager.md): Erstellen, bearbeiten und löschen von Klassifizierungssätze.
* [**[!UICONTROL Auftrags-Manager für Klassifizierungssätze]**](job-manager.md): Zeigt den Status der Klassifizierungssatz-Aufträge an und ermöglicht, die Exportdateien herunterzuladen.
