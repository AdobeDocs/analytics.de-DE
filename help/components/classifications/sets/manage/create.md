---
title: Erstellen eines Klassifizierungssatzes
description: Verfügbare Felder und Beschreibungen beim Erstellen eines Klassifizierungssatzes.
exl-id: 6d692d90-8cc7-4306-a780-58d03db45be8
feature: Classifications
source-git-commit: a40f30bbe8fdbf98862c4c9a05341fb63962cdd1
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 8%

---

# Erstellen eines Klassifizierungssatzes

Sie können den Classification Set Manager verwenden, um einen Klassifizierungssatz zu erstellen.

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]** > **[!UICONTROL Sets]** > **[!UICONTROL Hinzufügen]**

Beim Erstellen eines Klassifizierungssatzes sind die folgenden Felder verfügbar.

* **[!UICONTROL Name]**: Ein Textfeld, mit dem der Klassifizierungssatz identifiziert wird. Dieses Feld kann bei seiner Erstellung nicht bearbeitet werden, kann aber später umbenannt werden.
* **[!UICONTROL Spaltenname]**: Der Name der ersten Klassifizierungsdimension, die Sie erstellen möchten. Dieses Feld ist der in Analysis Workspace verwendete Dimensionsname und der Spaltenname beim Exportieren von Klassifizierungsdaten. Sie können weitere Spaltennamen hinzufügen, nachdem der Klassifizierungssatz erstellt wurde.
* **[!UICONTROL Type]**: Optionsfelder, die den Typ der Klassifizierung angeben.
   * **[!UICONTROL Primär]**: Auf in Analytics erfasste Dimensionen anwenden. Sie bieten die Möglichkeit, granulare Dimensionswerte in aussagekräftigere Datenebenen zu gruppieren (zu klassifizieren). Beispielsweise können Sie interne Suchbegriffe in internen Suchkategorien gruppieren, um Themen in Ihren Suchdaten besser zu verstehen.
   * **[!UICONTROL Lookup]**: Eine Lookup-Tabelle, häufig als untergeordnete Klassifizierungen oder Unterklassifizierungen bezeichnet, ist eine Klassifizierung einer primären Klassifizierung. Es handelt sich um Metadaten über einen Klassifizierungswert und nicht um die ursprüngliche Dimension. Die Variable „Product“ könnte beispielsweise die primäre Classification „Farbcode“ aufweisen. Eine Lookup-Tabelle mit „Farbname“ könnte dann an „Farbcode“ angehängt werden, um die Bedeutung der einzelnen Codes näher zu erklären.
* **[!UICONTROL Abonnements]** Die Report Suites und Dimensionen, für die dieser Klassifizierungssatz gilt. Sie können mehrere Report Suite- und Dimensionskombinationen zu einem Klassifizierungssatz hinzufügen.

![Erstellen eines Klassifizierungssatzes](../../assets/classification-set-create.png)

Wenn für eine bestimmte Report Suite und Variable ein Klassifizierungssatz vorhanden ist, wird stattdessen die Klassifizierung zum Schema hinzugefügt. Eine bestimmte Kombination aus Report Suite und Variable kann nicht zu mehreren Klassifizierungssätzen gehören.
