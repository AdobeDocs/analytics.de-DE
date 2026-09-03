---
description: In diesen Schritten wird beschrieben, wie Sie Classification-Daten löschen oder entfernen.
title: Löschen von Classification-Daten
feature: Classifications
exl-id: 2b156e66-3090-4048-8192-a412320e3be3
TQID: https://experienceleague.adobe.com/NZhXTXSwpA-E-6JaGRInMf3TMwHp5A1uMSjaAU1whts
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 366
ht-degree: 88%

---

# Löschen von Classification-Daten

{{classification-importer-deprecation}}

In einigen Fällen müssen Classification-Daten nach dem Hochladen entfernt werden. Verwenden Sie entweder `~empty~` oder `~deletekey~`, je nachdem, was Sie entfernen möchten.

## Schritte zum Entfernen von Classification-Daten

Das Entfernen von Classification-Daten umfasst das Hochladen einer Classification-Datei, mit `~empty~` oder `~deletekey~` in den entsprechenden Zellen.

1. Klicken Sie auf **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Klicken Sie auf **[!UICONTROL Browser-Export]**.
1. Wählen Sie die Report Suite und den Datensatz aus, aus denen Classification-Daten entfernt werden sollen.
1. Passen Sie die optionalen Einstellungen zum Filtern der gesuchten Daten an und klicken Sie auf **[!UICONTROL Datei exportieren]**.
1. Nachdem die Datei heruntergeladen wurde, öffnen Sie die Datei und ersetzen Sie alle Classification-Werte durch `~empty~` oder `~deletekey~`.
1. Speichern Sie die Datei als tabulatorgetrennte Textdatei.
1. Klicken Sie auf **[!UICONTROL Datei importieren]** und laden Sie die gespeicherte Classification-Datei erneut in Adobe Analytics hoch.

## Löschen eines einzelnen Classification-Werts

Mehrere Klassifizierungen können zur gleichen Variable gehören. Sie können beispielsweise zwei verschiedene Klassifizierungen von eVar1 haben. Wenn Sie nur einen einzelnen klassifizierten Wert entfernen möchten, ersetzen Sie den Classification-Wert durch `~empty~`. Beispiel:

| Inventar-SKU (eVar8) | Inventarname | Inventarkategorie |
| --- | --- | --- |
| 857467 | Pullover mit V-Ausschnitt | Damenbekleidung |
| 948203 | Fußkettchen | Schmuck |
| 174391 | Weiße Kordhose | `~empty~` |

Die Verwendung von `~empty~` unter der Classification „Inventarkategorie“ behält weiterhin Daten für die Classification „Inventarname“ bei. Der `~empty~`-Wert löscht nur die Classification-Daten für diese Zelle.

## Löschen einer gesamten Classification-Zeile

Verwenden Sie `~deletekey~` in einer beliebigen Spalte, um die gesamte Classification-Zeile zu löschen. Beispiel:

| Inventar-SKU (eVar8) | Inventarname | Inventarkategorie |
| --- | --- | --- |
| 857467 | Pullover mit V-Ausschnitt | Damenbekleidung |
| 948203 | Fußkettchen | Schmuck |
| 174391 | Weiße Kordhose | `~deletekey~` |

Durch Verwendung von `~deletekey~` unter der Classification „Inventarkategorie“ werden alle Classification-Daten für den Schlüsselwert `174391` gelöscht. Es wirkt dann so, als ob die Zeile nie klassifiziert wurde.

## Fallstricke und Tipps

* Bei der Verwendung von `~deletekey~` benötigen Sie nur eine Zeile in einer Classification-Datei.
* `~empty~` und `~deletekey~` müssen *exakt* übereinstimmen. Leerzeichen oder Groß-/Kleinschreibung sind nicht zulässig.
* Werte in der Schlüsselspalte können nicht gelöscht werden. Diese Werte werden direkt in die Variable übergeben und sind dauerhaft.
* Wenn Sie einen Klassifizierungswert entfernen, der Unterklassifizierungen enthält, werden diese Unterklassifizierungen ebenfalls entfernt. Klassifizierungen können nicht ohne Schlüsselwert vorhanden sein, und das übergeordnete Element einer Unterklassifizierung ist ihr Schlüsselwert.
* Es ist möglich, Unterklassifizierungsdaten zu entfernen, während die übergeordnete Klassifizierung intakt bleibt.
