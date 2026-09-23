---
title: Postleitzahl
description: Die Postleitzahl des Besuchers.
feature: Dimensions
exl-id: 597619f8-a581-4491-beb2-c14b1f7b7bec
TQID: https://experienceleague.adobe.com/XHrUXKHrXiH0wsUr0klmPmA-DEq5T5yu18KLNT7oYeo
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
subfeature_v2:
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
    internal-label: Appmeasurement implementation
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 61%
---
# Postleitzahl

Die Dimension „Postleitzahl[&#x200B; gibt &#x200B;](overview.md) Postleitzahl des Besuchers an. Sie können diese Dimension verwenden, um mehr über den Erfolg lokaler Werbung zu erfahren oder zu sehen, wo Ihre Site weltweit am besten abschneidet.

## Füllen dieser Dimension mit Daten

Diese Dimension ist insofern einzigartig, als sie mehrere Möglichkeiten enthält, sie mit Daten zu füllen. Sie können entweder eine oder eine Kombination aus beiden verwenden:

* Legen Sie die Postleitzahl direkt mithilfe der Variablen [`zip`](/help/implement/vars/page-vars/zip.md) fest.
* Konfigurieren Sie es so, dass es aus den Geolokalisierungsdaten abgerufen wird. Wenn Geo-ZIP verwendet wird, wird keine Variable festgelegt. Bei AppMeasurement-Implementierungen ist diese Dimension vorkonfiguriert. Aktivieren Sie für Web SDK-Implementierungen [!UICONTROL Geo-Suche] beim [Konfigurieren eines Datenstroms](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de).

Die [!UICONTROL Postleitzahlenoption] unter [Allgemeine Kontoeinstellungen](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md) steuert, wie Sie diese Dimension füllen möchten. Die nachstehende Referenztabelle gilt, wenn Sie die Variable `zip` direkt festlegen.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | [`zip`](/help/implement/vars/page-vars/zip.md) |
| **Feld Web SDK/XDM** | [`placeContext.geo.postalCode`](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/data-types/geo) |
| **Abfrageparameter** | [`zip`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<zip>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Byte-Grenze** | 50 Byte |
| **Persistenz** | Treffer |

## Dimensionselemente

Die Dimensionselemente beinhalten die Postleitzahl des Besuchers.

## Länder mit unterstützten Postleitzahlen

* Aland-Inseln
* Albanien
* Algerien
* Argentinien
* Armenien
* Österreich
* Australien
* Bangladesch
* Barbados
* Belgien
* Brasilien
* Bulgarien
* Kanada
* Chile
* China
* Kolumbien
* Costa Rica
* Kroatien
* Tschechische Republik
* Dänemark
* Ecuador
* Ägypten
* Estland
* Finnland
* Frankreich
* Georgien
* Deutschland
* Gibraltar
* Griechenland
* Grenada
* Guatemala
* Sonderverwaltungsregion Hongkong der Volksrepublik China
* Ungarn
* Indien
* Indonesien
* Irland
* Israel
* Italien
* Japan
* Jordanien
* Kasachstan
* Kirgisistan
* Lettland
* Libanon
* Litauen
* Luxemburg
* Malaysia
* Malta
* Mauritius
* Mexiko
* Marokko
* Mosambik
* Nepal
* Niederlande
* Neuseeland
* Norwegen
* Pakistan
* Panama
* Peru
* Philippinen
* Polen
* Portugal
* Puerto Rico
* Katar
* Rumänien
* Russische Föderation
* Saudi-Arabien
* Senegal
* Serbien
* Singapur
* Slowenien
* Südafrika
* Südkorea
* Spanien
* Sri Lanka
* Schweden
* Schweiz
* Region Taiwan
* Thailand
* Tunesien
* Türkei
* Ukraine
* Vereinigte Arabische Emirate
* Vereinigtes Königreich
* Vereinigte Staaten
* Uruguay
* Usbekistan
* Venezuela
* Vietnam
