---
title: Häufig gestellte Fragen zu Klassifizierungen
description: Häufig gestellte Fragen zur Verwendung von Klassifizierungen
feature: Classifications
exl-id: e929d7cb-0bfd-46de-88d1-aea2b4b91911
TQID: https://experienceleague.adobe.com/pIwAdewnHA4AB9hyRDRkH6xXvyxx-BceWvDXMydX-ew
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 420
ht-degree: 86%

---

# Häufig gestellte Fragen zum Classification Importer

{{classification-importer-deprecation}}

Häufig gestellte Fragen zur Verwendung des Classification Importer.

## Wie klassifiziere ich das Dimensionselement „0“?

Klassifizierungsdateien, die mit einem Schlüsselwert oder einem Klassifizierungswert von null hochgeladen wurden (`0`), führen zu einem Fehler. Dies schließt alle Werte ein, die nur Nullen (`00`, `000` usw.) enthalten. Es gibt mehrere Methoden, um dieses Problem zu beheben:

* **Alternative Werte implementieren**: Die Verwendung eines anderen Textwerts als `"0"` ist der beste und einfachste Weg, dieses Problem zu lösen. Ändern Sie zum Beispiel `s.campaign = "0";` in Ihrer Implementierung in `s.campaign = "Zero";`.

* **Verarbeitungsregeln verwenden**: Sie können Dimensionselemente zwischen der Datenerfassung und ihrer Datenspeicherung in einer Report Suite ändern. Erstellen Sie die folgende Verarbeitungsregel:

  *Wenn die [Dimension] gleich `0` ist, überschreiben Sie den Wert der [Dimension] mit dem benutzerdefinierten Wert `Zero`.*

* **Eine VISTA-Regel anfordern**: Ein Engineering Services-Berater richtet gegen Aufpreis eine Server-seitige Regel für Sie ein. Wenden Sie sich an Ihr Adobe-Acountteam, um eine VISTA-Regel anzufordern.

## Kann ich mit Classification Importer Dimensionselemente klassifizieren, die noch nicht vorhanden sind?

Ja, dabei wird *jedoch jedes Dimensionselement als abrechnungsfähiger Server-Aufruf gezählt.*

* Dimensionen, die bereits vorhanden sind, verursachen keine zusätzlichen Kosten.
* Die Verwendung des Classification Rule Builders klassifiziert nicht vorhandene Elemente nicht und verursacht daher keine zusätzlichen Kosten.

## Wie klassifiziere ich Werte, die Sonderzeichen enthalten?

Die Verwendung von Leerzeichen am Anfang und Ende in Classification-Daten und Trefferdaten wird nicht unterstützt, da Adobe Analytics Leerzeichen automatisch abschneidet.

Die Verwendung von Sonderzeichen wie Kommas oder doppelten Anführungszeichen im Reporting wird normalerweise nicht empfohlen. In einigen Fällen ist ihre Verwendung jedoch erforderlich. Wenn Ihre Reporting-Werte solche Zeichen enthalten, die Sie klassifizieren möchten, gehen Sie wie folgt vor:

1. Melden Sie sich bei Adobe Analytics an und navigieren Sie dann zu **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
2. Klicken Sie auf die Registerkarte **[!UICONTROL Browser-Export]**.
3. Konfigurieren Sie die Exporteinstellungen und stellen Sie sicher, dass „Anführungszeichenausgabe“ NICHT aktiviert ist.
4. Klicken Sie auf **[!UICONTROL Datei exportieren]** und öffnen Sie die heruntergeladene Datei in einem Tabellen-Editor.
5. Suchen Sie in Zeile 1 die Zelle C1, die den Wert `v:2.0` enthält. Ändern Sie den Wert in `v:2.1` und wenden Sie die gewünschten Klassifizierungen auf die Arbeitsmappe an.
6. Laden Sie die Datei wie jede andere Classification hoch.

## Was sind Nummerisch-2-Klassifizierungen?

Mit Nummerisch-2-Klassifizierungen können Sie Dimensionselemente als zeitbasierte Metriken klassifizieren. Sie wurden im Juli 2019 aus der Benutzeroberfläche von Adobe Analytics entfernt.

## Wie kann ich Daten in einer Classification-Datei mit Escape-Zeichen versehen?

Umschließen Sie das Feld mit Sonderzeichen in doppelten Anführungszeichen (`"`). Ein doppeltes Anführungszeichen kann in einer maskierten Zelle enthalten sein, wenn Sie es durch zwei doppelte Anführungszeichen ersetzen (`" "`). Zum Beispiel:

```
My String "of data"
```

Mit Escape-Zeichen versehen:

```
"My String ""of data"""
```
