---
description: Erfahren Sie, wie Sie veraltete Segmente verwalten.
title: Häufig gestellte Fragen zu Legacy-Segmenten
feature: Segmentation
exl-id: 316e2a2e-55d3-4c23-9985-9a6d90390e86
TQID: https://experienceleague.adobe.com/P1EFVQMiTkCoZd-rak9jJgNz-AbgjnhMd6sWlIAKhsk
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2: id: a544b409-2610-410d-a842-474ac1d0d54eid: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: ef60b66e-5984-4336-ba72-6d978b1b6f87id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 1440
ht-degree: 24%

---

# Legacy-Segmente

In diesem Artikel werden häufig gestellte Fragen zu Best Practices für die Verwaltung veralteter Segmente beantwortet. Legacy-Segmente sind Segmente, die vor 2014 erstellt wurden.

## Verwalten veralteter Segmente {#legacy}

+++ **Was ist mit meinen vorhandenen Segmenten passiert?**

Die vorhandenen Segmente funktionieren weiterhin wie zuvor. Alle Berichte, auf die diese Segmente angewendet werden, funktionieren weiterhin ordnungsgemäß.

Die meisten vorherigen vordefinierten Segmente und Suite-Segmente werden als Segmentvorlagen in Segment Builder migriert. Segmentvorlagen werden verwendet, um schnell benutzerdefinierte Segmente mit gemeinsamen Zielgruppen zu erstellen. Segmentvorlagen können nicht direkt auf einen Bericht angewendet werden, sie können jedoch einfach in einem benutzerdefinierten Segment gespeichert werden.

Segmentvorlagen sind im Segment Builder mit einem speziellen Symbol ![AdobeLogoSmall](/help/assets/icons/AdobeLogoSmall.svg) gekennzeichnet.



+++

+++ **Was ist mit terminierten Berichten passiert, auf die Segmente angewendet sind?**

Terminierte Berichte werden weiterhin ordnungsgemäß mit den von Ihnen definierten Segmenten ausgeführt.

Wenn Sie ein Segment löschen, funktionieren terminierte Berichte und Dashboards, auf die dieses Segment angewendet wird, weiterhin normal. Das Segment oder Dashboard verwendet also weiterhin das gelöschte Segment.

Terminierte Berichte werden nicht aktualisiert, wenn Sie ein Segment mit demselben Namen bearbeiten. Im Folgenden finden Sie ein Beispiel: Angenommen, Sie haben zwei Segmente mit demselben Namen in verschiedenen Report Suites:

![](assets/duplicate_seg_names.png)

Sie verfügen über eine Visualisierung, die auf das Segment für die Report Suite **[!UICONTROL mainprod]** verweist. Dann löschen Sie das Segment, weil es sich um ein Duplikat handelt. Die Visualisierung wird fortgesetzt und verweist auf die Definition des gelöschten Segments. Wenn Sie die Segmentdefinition für das Hauptsegment ändern, um Catalina Island und Tijuana, Mexiko, einzuschließen, ändert sich das auf die Visualisierung angewendete Segment nicht und verwendet die alte Definition. Um die neue Definition zu verwenden, aktualisieren Sie die Visualisierung, um auf die neue Definition zu verweisen. Wenn Sie sich nicht sicher sind, ob eine Visualisierung, ein Projekt oder ein terminierter Bericht ein gelöschtes Segment verwendet, ändern Sie den Namen des verbleibenden Segments, um anzuzeigen, ob die Visualisierung das verbleibende Segment verwendet.

+++

+++ **Was ist mit Data Warehouse-Segmenten passiert?**

Alle vorhandenen Data Warehouse-Segmente funktionieren weiterhin in Data Warehouse. Die meisten Data Warehouse-Segmente funktionieren auch in anderen Komponenten wie Analysis Workspace.

Sie können neue Data Warehouse-Segmente im Segment Builder/Manager erstellen oder bearbeiten. Der Produktkompatibilitätsmechanismus in Segment Builder bestimmt automatisch, ob ein Segment mit Data Warehouse kompatibel ist.

+++

+++ **Was ist mit vorkonfigurierten Segmenten passiert?**

* **Einzelseitenbesuche**
* **Besuche von Mobilgeräten**
* **Besuche über eine kostenlose Suche**
* **Besuche über eine gebührenpflichtige Suche**
* **Besuche mit Besucher-ID-Cookie**

Diese Segmente werden als Segmentvorlagen in den Segment Builder migriert. Vorhandene Berichte, auf die diese Segmente angewendet wurden, funktionieren weiterhin fehlerfrei.

+++

+++ **Was ist mit Experience Cloud (Suite)-Segmenten passiert?**

* Nichtkaufende
* Kaufende
* Erstbesuche
* Besuche von Social Media aus
* Besuche von mehr als 10 Minuten*
* Besuche mit mehr als 5 vorherigen Besuchen*
* Besuche von Facebook*

Die meisten dieser Segmente (bis auf die mit einem Sternchen „*“ markierten) werden als Segmentvorlagen in Segment Builder migriert. Darüber hinaus wurden einige neue Segmente hinzugefügt.

Vorhandene Berichte, auf die diese Segmente angewendet wurden, funktionieren weiterhin fehlerfrei.

+++

+++ **Was ist mit Admin-Segmenten (auch bekannt als „globale“ Segmente) passiert?**

**Admin**-Segmente werden in die neue Segmentoberfläche migriert und als Segmente angezeigt, die für alle freigegeben sind.

Der Eigentümer dieser Segmente wird auf den Administrator mit dem ältesten Konto von Admin-Benutzern festgelegt. Alle Administratoren können diese Segmente jedoch löschen, bearbeiten und freigeben.

Die Benutzeroberfläche für das Segmentmanagement in der Admin Console, in der Administratoren diese globalen Segmente erstellt und verwaltet haben, ist nicht mehr verfügbar. Administratoren sollten jetzt den neuen Segment Builder verwenden, um Segmente zu erstellen und sie für entsprechende Gruppen oder Einzelpersonen oder für alle freizugeben.

Vorhandene Segmente, die eine geänderte Logik wie in diesem Dokument beschrieben verwenden, funktionieren weiterhin ordnungsgemäß, obwohl die Segmente aktualisiert werden müssen, bevor sie erneut gespeichert werden können. Wenn Sie beispielsweise über ein vorhandenes Segment verfügen, in dem **[!UICONTROL US]** **[!UICONTROL enthält]** `New York`, funktioniert dieses Segment weiterhin ordnungsgemäß. Wenn Sie das nächste Mal das Segment bearbeiten, müssen Sie das Segment aktualisieren, um den Aufzählungstyp mit einer **[!UICONTROL gleich]**-Bedingung zu verwenden.

+++

+++ **Was sollte ich mit doppelten Segmenten tun, die denselben Namen, aber möglicherweise unterschiedliche Definitionen haben?** 
Nachdem Segmente jetzt von unterschiedlichen Report-Suites genutzt werden können, kann es vorkommen, dass Sie mehrere Segmente mit demselben Namen haben. Sie sollten:

* Segmente umbenennen, die denselben Namen, aber unterschiedliche Definitionen aufweisen, oder
* Segmente löschen, die nicht mehr benötigt werden.

+++

+++ **Was empfiehlt Adobe im Hinblick auf die Bereinigung von Segmenten?**

* Taggen Sie alle Segmente mit dem Legacy-Tag.
* Überprüfen Sie die vorhandenen Segmente.
* Fügen Sie sie gegebenenfalls zur Segmentbibliothek hinzu.
* Genehmigen von kanonischen Segmenten.
* Markieren Sie Segmente gemäß den [Best Practices](/help/components/segmentation/segmentation-workflow/seg-workflow.md).

+++

### Tipps zur Migration

Die folgenden Tipps helfen Ihnen bei der Migration allgemeiner Dimensionen:

* Geo-Stadt/Region/Land – Suche nach und Auswahl bestimmter Städte, Regionen oder Länder, anstelle einer teilweisen Übereinstimmung.
* Browser - Verwenden Sie die Dimension Browser-Typen , um alle Browser in einen Typ zu bekommen, z. B. Google Chrome
* Betriebssysteme : Verwenden Sie die Dimensionen „Betriebssystemtypen“, um alle Betriebssysteme in einen Typ zu bekommen, z. B. Microsoft Windows.
* Siehe „Neue und umbenannte Dimensionen“ (siehe unten).

## Neue und umbenannte Dimensionen {#renamed}

Die folgende Tabelle enthält eine Liste der Dimensionen, die in Segment Builder umbenannt wurden.

| Neuer Dimensionsname | Vorheriger Name | Hinweise |
|--- |--- |--- |
| Betriebssystemtypen | Neu | Im Frühjahr 2015 hinzugefügt. |
| Browser-Breite – zusammengefasst | Browser-Breite | Diese Dimension ist mit allen Schnittstellen kompatibel und wird in eine Aufzählungsliste von Bereichen anstelle von bestimmten ganzzahligen Werten aufgeteilt. Wenn Sie bestimmte Werte segmentieren müssen, verwenden Sie die granulare Version dieser Dimension in einem Data Warehouse-Segment. |
| Browser-Höhe – zusammengefasst | Browser-Höhe | Diese Dimension ist mit allen Schnittstellen kompatibel und wird in eine Aufzählungsliste von Bereichen anstelle von bestimmten ganzzahligen Werten aufgeteilt. Wenn Sie bestimmte Werte segmentieren müssen, verwenden Sie die granulare Version dieser Dimension in einem Data Warehouse-Segment. |
| Browser-Breite – Präzise | Browser-Breite | Diese Dimension wurde umbenannt und ist jetzt nur noch mit Data Warehouse kompatibel. Verwenden Sie beim Definieren von Segmenten, die mit allen Schnittstellen kompatibel sind, den Aufzählungstyp „Browser Width - Bucketed“. |
| Browser-Höhe – Präzise | Browser-Höhe | Diese Dimension wurde umbenannt und ist jetzt nur noch mit Data Warehouse kompatibel. Verwenden Sie beim Definieren von Segmenten, die mit allen Schnittstellen kompatibel sind, den Aufzählungstyp „Browser Height - Bucketed“. |
| Cookie-Unterstützung | Cookies | – |
| Farbtiefe | Bildschirmfarbtiefe | – |
| – | „Programm - *&quot; | Die Präfixe „App -&quot; wurden aus einer Reihe von Dimensionstypen entfernt. Da Mobile-App-Daten normalerweise in einer Report Suite erfasst werden, die keine Web-Daten enthält, waren diese Präfixe nicht erforderlich. |
| Ursprüngliche Entrypage | Ursprüngliche Einstiegsseite | – |
| Java aktiviert | Java | – |
| Maximale mobile Browser-URL-Länge | Länge der mobilen Browser-URL | – |
| Mobilgerät – Mail-Design | Mobile Design-Mail-Unterstützung | – |
| Mobilgerät | Mobilgerätename | – |
| Maximale mobile Lesezeichenlänge | Mobil Max. Lesezeichen URL-Länge | – |
| Maximale mobile E-Mail-Länge | Mobil Max. Mail URL-Länge | – |
| Betriebssystem für Mobilgeräte (veraltet) | Mobilbetriebssystem | Verwenden Sie stattdessen die Dimension Betriebssystem und wenden Sie Besuche von Segmenten mobiler Geräte an. |
| Mobiles PTT | Mobile PTT | – |
| Umfrageansichten | Gesamtaufrufe der Umfrage | – |
| Umfrageantworten | Gesamtzahl der Umfrageantworten | – |
| Besuchstiefe | Path Length | – |
| Postleitzahl | Postleitzahl | – |

{style="table-layout:auto"}

## Änderungen an zeichenfolgenbasierten Dimensionen mit bekannten Werten {#string-based-dims}

Zeichenfolgenbasierte Dimensionen mit einem bekannten Wertesatz wurden in Aufzählungstypen geändert. Beim Erstellen eines Segments mit diesen Dimensionen wird die Liste mit allen bekannten Werten vorab ausgefüllt und der einzige unterstützte Operator ist **[!UICONTROL Gleich]**. Mit dieser Wertepopulation können Sie die gesuchten Werte schnell segmentieren, ohne unbeabsichtigte Werte bei weniger restriktiven Übereinstimmungen auszuwählen.

Die folgenden Dimensionen wurden in Aufzählungslisten geändert:

| Name der Dimension | Name der Dimension | Name der Dimension |
| --- | --- | --- |
| Mobilgerätehersteller | Länge der mobilen E-Mail | Farbtiefe |
| Mobilgerät - Bildschirmgröße | Mobilgerätenummer | Bildschirmauflösung |
| Mobilgerät - Bildschirmhöhe | Gebührenpflichtige Suche | Plug-in |
| Unterstützung mobiler Cookies | Mobile-Mail-Dekoration | Betriebssystem |
| Bildunterstützung für Mobilgeräte | Mobile Informationsdienste | Empfehlungstyp |
| Mobilgerät - Farbtiefe | Mobilgerätetyp | Suchmaschine |
| Mobilgerät – Audio-Unterstützung | Browser-Typ | state |
| Mobilgerät – Video-Unterstützung | browser | Geo-Land |
| Mobiles DRM | Verbindungstyp | Geo-Region |
| mobile Netzprotokolle | Mobilnetzbetreiber | Geo-Stadt |
| Mobile Betriebssystem | Cookie | Geo-DMA |
| Mobile Java-VM | Kundentreue | Persistentes Cookie |
| Länge des mobilen Lesezeichens | Java aktiviert | Paid Search |
| Länge der mobilen URL | Sprache |  |

## Änderungen an auf Ganzzahlen basierenden Dimensionen mit bekannten Werten {#integer-based-dims}

Ganzzahlige Dimensionen (z. B. die Browser-Breite) mit einem bekannten Satz von Werten werden in Aufzählungsbereiche aufgeteilt, sodass Sie schnell Segmente für einen bestimmten Bereich definieren können. Diese Aufzählungslisten werden mit &quot;- Bucketed“ nach dem Dimensionsnamen angehängt. Der folgende Bildschirm zeigt, wie diese Dimensionen mit der früheren und der neuen Segment Builder-Oberfläche segmentiert werden:

![](assets/seg_browser_dimension.png)

Die Operatoren „kleiner als“, „größer als“ und „ähnlich“ sind jetzt nur noch mit Data Warehouse-Segmenten kompatibel. Segmente, die mit allen Reporting-Schnittstellen kompatibel sein sollen, sollten die „Bucketed“-Version der Metrik mit dem Operator **[!UICONTROL Gleich]** verwenden.
