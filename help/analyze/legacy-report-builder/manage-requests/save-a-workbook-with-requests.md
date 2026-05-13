---
description: Erfahren Sie mehr über das Speichern von Berichten mit eingebetteten Anfragen.
title: Informationen zum Speichern einer Arbeitsmappe mit Anfragen
uuid: 31611031-0982-4124-9fc7-7888124aa603
feature: Report Builder
role: User, Admin
exl-id: 192ac2f6-cfb8-447b-8fc1-19ad786ef924
TQID: https://experienceleague.adobe.com/0UMDDWbeilsUp-yB-tzMVcWkGfUXtf4lh2ciaAg4AEk
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2:
  - id: ac8a38fa-dec3-4581-8f64-178fde9f64e8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 276
ht-degree: 39%

---

# Arbeitsmappe mit Anforderungen speichern

{{legacy-arb}}

Wenn Sie Berichte mit eingebetteten Anfragen erstellen, können Sie sie mithilfe von **Datei** > **Speichern** oder **Datei** > **Speichern unter** in Excel speichern. Report Builder erkennt, ob der Bericht Anforderungen enthält. Wenn Sie eine der Speicheroptionen auswählen, füllen Sie das Formular **Arbeitsmappe speichern unter** aus.

* Als Best Practice für umfangreiche Arbeiten mit Windows-Anwendungen empfiehlt Adobe, Ihre Anfragen oft und regelmäßig in der Tabelle zu speichern, um einen unerwarteten Verlust von Anfragen in Ihrem Arbeitsblatt zu vermeiden.
* Erwägen Sie beim Benennen Ihrer Arbeitsmappe, eine Versionsnummer im Dateinamen zu verwenden, damit Sie einen Arbeitsverlauf beibehalten können. Nennen Sie beispielsweise Ihre erste Arbeitsmappe [!DNL web_forecast_01_01.xlsx].
* Wenn Sie den Bericht bereits gespeichert haben, wird [!UICONTROL &#x200B; Formular „Vorlage speichern] beim erneuten Speichern des Berichts nicht angezeigt. Wenn der Bericht keine Anforderungen enthält, wird dieses Dialogfeld nicht angezeigt. Stattdessen wird das standardmäßige Excel[!UICONTROL Formular „Speichern unter] angezeigt.

## Dateinamen und Speicherort {#section_2406629E9B644CE08430826948977D5D}

Das Dialogfeld [!UICONTROL Vorlage speichern] ähnelt in einigen Punkten dem Excel-Standarddialogfeld [!UICONTROL Datei] > [!UICONTROL Speichern unter]. Beispielsweise gibt es ein Textfeld für die Eingabe des Dateinamens für die Arbeitsmappe, bei dem die herkömmliche Dateiendung [!DNL .xls] verwendet wird.

Jeder Dateiname darf höchstens 255 Zeichen enthalten. Darüber hinaus darf der Dateiname die folgenden Zeichen nicht enthalten:

\ ? | > &lt; : / &#42; &#39; &quot;

Außerdem ist die Verwendung von Unicode-Zeichen über den erweiterten ASCII-Zeichensatz hinaus nicht möglich.

Wenn Sie eine Datei an einem Speicherort auf der lokalen Festplatte oder im Netzwerk speichern, können Sie den vollständigen Pfad im Textfeld angeben oder auf die Schaltfläche „Durchsuchen“ ![browse_button.gif](assets/browse_button.gif) neben dem Textfeld [!UICONTROL Speichern unter] klicken.
