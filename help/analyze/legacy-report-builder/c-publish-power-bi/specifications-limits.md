---
description: Einschränkungen bei der Verwendung von Report Builder und Microsoft Power BI.
title: Einschränkungen und Spezifikationen
feature: Report Builder
role: User, Admin
exl-id: 4bbeec5b-64bc-4285-9f13-33b223b88834
TQID: https://experienceleague.adobe.com/L3R3ufcclrTpw-fKoFLD8Y-v56rTm4tXlXqjaTdmdoQ
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 631
ht-degree: 34%

---

# Einschränkungen und Spezifikationen

{{legacy-arb}}

## Einschränkungen für Power BI-Veröffentlichungen {#section_D4BDD70B20F94A0FAE53531CA528AE42}

>[!NOTE]
>
>Diese Einschränkungen gelten nur für die Option „Report Builder-Anforderungen als Power BI-Datensatztabellen veröffentlichen“.

* Maximal 100 Report Builder-Anforderungen pro Arbeitsmappe können nach Power BI exportiert werden.
* Der Planungsprozess stoppt den Export von Anfragen, wenn die 101. Anfrage erreicht ist.
* Pro Report Builder-Anforderung werden nur die Analytics-Daten in den ersten 10.000 Zeilen an Power BI gesendet. Die verbleibenden Zeilen werden ignoriert.

## Bearbeiten einer Report Builder-Anforderung nach der Veröffentlichung in Power BI {#section_6989E74F68DD43F08D37C36B6777DB50}

>[!NOTE]
>
>Diese Angaben gelten für die Optionen „Alle Report Builder-Anforderungen als Power BI-Datensatztabellen veröffentlichen“ und „Alle formatierten Tabellen der Arbeitsmappe als Power BI-Datensatztabellen veröffentlichen“.

Bearbeiten einer Report Builder-Anforderung nach der Veröffentlichung in Power BI kann zu Problemen führen.

* **1.**: Sie veröffentlichen eine Arbeitsmappe in Power BI und erstellen eine Visualisierung basierend auf ihren Daten. Als Nächstes nehmen Sie Änderungen an der Arbeitsmappe vor, wodurch eine der Spalten des Datensatzes, auf den sie verweist, verschwindet. Dann wird erneut veröffentlicht. Dadurch wird die Visualisierung in Power BI unterbrochen.

  **Hier ist ein Beispiel dafür, wie die Visualisierung funktioniert:**

   1. Erstellen Sie in Report Builder eine Arbeitsmappe mit einer Anforderung, indem Sie die Dimension „Seite“ und die Metrik „Seitenansichten“ verwenden.
   2. Planen Sie die Veröffentlichung dieser Anforderung in Power BI.
   3. Erstellen Sie in Power BI eine Visualisierung für Seiten- und Seitenansichten.
   4. Bearbeiten Sie nun die Arbeitsmappe, indem Sie Seitenansichten aus der Anfrage entfernen.
   5. Bearbeiten Sie den Zeitplan mit der aktualisierten Arbeitsmappe und veröffentlichen Sie die Anfrage erneut in Power BI.
   6. Sobald die neue Arbeitsmappe an Power BI gesendet wurde

      1. Stellen Sie sicher, dass der vorhandene Datensatz, der bei der ersten Veröffentlichung erstellt wurde, überschrieben wurde.
      2. Überprüfen Sie, ob die Tabelle page_1 ordnungsgemäß mit den Spalten Seite und Besuche aktualisiert wurde.
      3. Stellen Sie sicher, dass Ihre Visualisierung fehlerhaft ist, da sie auf die Spalte Seitenansichten verweist, die nicht mehr in der Tabelle page_1 vorhanden ist.

  **Im Folgenden finden Sie ein Beispiel dafür, wie die Visualisierung NICHT beschädigt wird:**

   1. Erstellen Sie in Report Builder eine Arbeitsmappe mit einer Anforderung, indem Sie die Dimension „Seite“ und die Metrik „Seitenansichten“ verwenden.
   2. Planen Sie die Veröffentlichung dieser Anforderung in Power BI.
   3. Erstellen Sie in Power BI eine Visualisierung für Seiten- und Seitenansichten.
   4. Bearbeiten Sie die Arbeitsmappe in Report Builder, indem Sie die Metrik für Besuche hinzufügen und „Seite“ sowie „Seitenansichten“ beibehalten.
   5. Bearbeiten Sie den Zeitplan mit der aktualisierten Arbeitsmappe und veröffentlichen Sie die Anfrage erneut in Power BI.
   6. Sobald die neue Arbeitsmappe an Power BI gesendet wurde

      1. Stellen Sie sicher, dass der vorhandene Datensatz, der bei der ersten Veröffentlichung erstellt wurde, überschrieben wurde.
      2. Überprüfen Sie, ob die Tabelle page_1 ordnungsgemäß mit den Spalten Seite, Seitenansichten und Besuche aktualisiert wurde.
      3. Stellen Sie sicher, dass Ihre Visualisierung weiterhin ordnungsgemäß funktioniert, da sie auf zwei Spalten verweist, die noch in der Tabelle page_1 vorhanden sind.

* **Fall 2**: Sie heften einen Abschnitt Ihrer Arbeitsmappe an ein Dashboard in Power BI und entfernen später diesen angehefteten Abschnitt (z. B. ein Diagramm oder eine Tabelle) aus der Arbeitsmappe. Dadurch wird die Visualisierung unterbrochen.

## Ändern des Namens eines Power BI-Berichts {#section_2E7893A78B914EBFACB2B08CBD9E472E}

Standardmäßig wird der Name aus dem Dateinamen der Arbeitsmappe (ohne die Erweiterung .xlsx) gefüllt, mit der Ausnahme, dass Leerzeichen durch Unterstriche ersetzt werden.

Bedenken Sie Folgendes

* Bei der Bezeichnung darf es sich nicht um eine Kombination aus Buchstaben und Zahlen handeln, die mit einer Zeilen- und Spaltenadresse verwechselt werden könnte. Beispielsweise kann A100 keine Beschriftung sein, da es sich um die Adresse einer Zelle in einem Arbeitsblatt handelt.
* Die folgenden Zeichen sind für eine Bezeichnung nicht gültig: `'#', '@', '!', '$', '^', '&', '&#42;', '` und `'~', ' '` . Sie werden durch einen Unterstrich ersetzt.
* Wenn Sie einen ungültigen Namen eingeben, wird eine Warnmeldung angezeigt, die einen automatisch generierten Namen vorschlägt. Wenn Sie auf **[!UICONTROL Ja]** klicken, wird dieser Name verwendet. Wenn Sie auf **[!UICONTROL Nein]** klicken, können Sie in der Benutzeroberfläche des erweiterten Assistenten den neuen Namen eingeben.
