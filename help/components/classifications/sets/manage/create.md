---
title: Erstellen eines Klassifizierungssatzes
description: Verfügbare Felder und Beschreibungen beim Erstellen eines Klassifizierungssatzes.
exl-id: 6d692d90-8cc7-4306-a780-58d03db45be8
feature: Classifications
source-git-commit: 811e321ce96aaefaeff691ed5969981a048d2c31
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 22%

---

# Erstellen eines Klassifizierungssatzes

Sie können den Classification Set Manager verwenden, um einen Klassifizierungssatz zu erstellen.

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]** > **[!UICONTROL Sets]** > **[!UICONTROL Hinzufügen]**

Beim Erstellen eines Klassifizierungssatzes sind die folgenden Felder verfügbar.

* **[!UICONTROL Name]**: Ein Textfeld, mit dem der Klassifizierungssatz identifiziert wird. Dieses Feld kann bei seiner Erstellung nicht bearbeitet werden, kann aber später umbenannt werden.
* **[!UICONTROL Spaltenname]**: Der Name der ersten Klassifizierungsdimension, die Sie erstellen möchten. Dieses Feld ist der in Analysis Workspace verwendete Dimensionsname und der Spaltenname beim Exportieren von Klassifizierungsdaten. Sie können weitere Spaltennamen hinzufügen, nachdem der Klassifizierungssatz erstellt wurde.
* **[!UICONTROL Typ]**: Optionsfelder, die den Typ der Klassifizierung angeben. Normalerweise werden primäre Klassifizierungen verwendet. Suchklassifizierungen stellen [Unterklassifizierungen](../../c-sub-classifications.md) dar.
* **[!UICONTROL Abonnements]** Die Report Suites und Dimensionen, für die dieser Klassifizierungssatz gilt. Sie können mehrere Report Suite- und Dimensionskombinationen zu einem Klassifizierungssatz hinzufügen.

![Erstellen eines Klassifizierungssatzes](../../assets/classification-set-create.png)

Wenn für eine bestimmte Report Suite und Variable ein Klassifizierungssatz vorhanden ist, wird stattdessen die Klassifizierung zum Schema hinzugefügt. Eine bestimmte Kombination aus Report Suite und Variable kann nicht zu mehreren Klassifizierungssätzen gehören.
