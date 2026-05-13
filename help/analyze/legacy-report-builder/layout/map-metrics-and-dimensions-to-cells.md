---
description: Erfahren Sie, wie Sie einen Zellenbereich auswählen, wie Sie Zellen auswählen und Probleme mit der Zuordnung beheben.
title: Erfahren Sie mehr über die Zuordnung von Metriken und Dimensionen zu Zellen
uuid: 50893e1c-5f2c-4558-8001-41e70d74d6e7
feature: Report Builder
role: User, Admin
exl-id: e63fc679-39eb-417b-9a2b-6620db63a824
TQID: https://experienceleague.adobe.com/yeU4gugMR2nSKwjo4LuX79spXIaD4UtuaTQ52bZwGrU
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2: id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 676
ht-degree: 26%

---

# Metriken und Dimensionen Zellen zuordnen

{{legacy-arb}}

Bevor Sie damit beginnen, einem Arbeitsblatt Elemente zuzuordnen, stellen Sie sicher, dass das Arbeitsblatt nicht schreibgeschützt ist. Wenn ein bestehender Schutz für das Arbeitsblatt die Benutzerinteraktion verhindert, können Sie keine Zellen darin auswählen. Heben Sie zunächst den Schutz des Arbeitsblatts auf und fügen Sie dann Zellenzuordnungen hinzu.

Die Anzahl der Bereiche und Zellen, die zugeordnet werden sollen, hängt von der ausgewählten Metrik, der Granularität, dem Datumsbereich und den von Ihnen festgelegten Filtern ab. Wenn Sie beispielsweise [!UICONTROL Site-Metrik] > [!UICONTROL Traffic-Bericht] auswählen, die [!UICONTROL Woche]-Granularität festlegen und den Datumsbereich für die [!UICONTROL Letzte 2 Wochen] festlegen, werden Sie aufgefordert, drei Zellen (bei Verwendung von [!UICONTROL Benutzerdefiniertes Layout]) im [!UICONTROL -Anforderungs-Assistenten zuzuordnen: Schritt 2]. Die Anfrage ruft Daten für die erste Woche und Daten für die zweite Woche ab, wobei jeder Datenpunktwert dem Wert einer Seitenansicht entspricht. Die dritte Zelle dient als Zeilenüberschrift, die Sie mit „Formatoptionen[!UICONTROL  konfigurieren ].

Wenn Sie versehentlich inkompatible Speicherorte auf dem Arbeitsblatt zuordnen, gibt Report Builder einen Fehler aus.

Weitere Informationen finden Sie in den folgenden Abschnitten:

* [Auswahl eines Zellenbereiches ](/help/analyze/legacy-report-builder/layout/map-metrics-and-dimensions-to-cells.md#section_1E37FB46DA194FB7A1050B8833A48AC6)
* [Methoden für die Auswahl von Zellen ](/help/analyze/legacy-report-builder/layout/map-metrics-and-dimensions-to-cells.md#section_760421C3D7F84D67A639174710C93B22)
* [Probleme beim Zuordnen](/help/analyze/legacy-report-builder/layout/map-metrics-and-dimensions-to-cells.md#section_CC1BCF841291447EB3A994EB08F3A099)

## Einen Zellenbereich auswählen {#section_1E37FB46DA194FB7A1050B8833A48AC6}

Wenn Sie in [!UICONTROL Anforderungs-Assistent: Schritt 2] die Option [!UICONTROL Benutzerdefiniertes Layout] für eine Trendanforderung verwenden, können Sie die Anforderung einem Bereich von Zellen zuordnen.

Klicken Sie auf **[!UICONTROL Bereichsauswahl]** ![select_cell_icon.png](assets/select_cell_icon.png) neben dem Element, das Sie zuordnen möchten.

* **Alle Zellen im Bereich:** Dies erfordert die Auswahl einer Gruppe von Zellen für eine Anforderung mit [!UICONTROL benutzerdefiniertem Layout].
* **Erste Zelle des Bereichs:** Hierdurch wird die Zelle links oben im Zellbereich ausgewählt und die Option [!UICONTROL Bereichausrichtung] angezeigt, mit der Sie festlegen können, ob die Eingabe- und Ausgabezellen horizontal (Zeile) oder vertikal (Spalte) angeordnet werden sollen. Verwenden Sie diese Option, damit Report Builder Zellen für Sie auswählt.
* **Bereichsausrichtung:** Wahlweise Orientierung des Zellenbereichs als Spalten oder Zeilen.
* **Position der obersten Zelle des Bereichs auswählen:** Zeigt die Zellreferenzen an.

## Verfahren zur Auswahl von Zellen {#section_760421C3D7F84D67A639174710C93B22}

Sie können die Daten durch Klicken auf das Symbol **[!UICONTROL Bereichsauswahl]** auswählen ![select_cell_icon.png](assets/select_cell_icon.png)

und die Maus bei gedrückter Taste über den gewünschten Zellbereich im Arbeitsblatt ziehen. Eine durchgehende Auswahl wird durch einen schwarzen Rahmen gekennzeichnet.

![](assets/twenty_cells.gif)

Separate ausgewählte Zeilen haben einen dünnen weißen Rahmen um jede Zeile.

![](assets/twoXten_cells_highlighted.gif)

Um einzelne Zeilen in einer Anfrage zuzuordnen, verwenden Sie die [!UICONTROL Strg]-Taste und klicken und ziehen Sie den Cursor über die gewünschten Zellen. Dies wäre sinnvoll, wenn Ihre Anfrage vier Bereiche mit jeweils zehn Zellen statt eines zusammenhängenden Bereichs mit 40 Zellen zusammen erfordert.

![](assets/map4.png)

Nachdem Sie Zellen ausgewählt haben, klicken Sie auf die **[!UICONTROL Bereichsauswahl]** erneut auf dem Formular [!UICONTROL Bereichsauswahl], um zum [!UICONTROL Anforderungs-Assistenten: Schritt 2) ].

## Fehlerbehebung bei Zuordnungsproblemen{#section_CC1BCF841291447EB3A994EB08F3A099}

Wenn Sie versehentlich eine Zuordnung zu einer Zelle auswählen, die bereits über eine aktive Zuordnung verfügt, wird im Textfeld neben dem Bereichsauswahlsymbol kein Zellverweis angezeigt. Wenn Sie auf [!UICONTROL OK] klicken, zeigt Report Builder den Fehler an *Der ausgewählte Bereich überschneidet sich mit dem Bereich einer anderen Anfrage. Ändern Sie Ihre Auswahl.*

* Wenn Sie die Zelle weiterhin verwenden müssen, klicken Sie mit der rechten Maustaste auf die gewünschten Zellen und wählen Sie **[!UICONTROL Löschanfrage]**.

Wenn Sie diese Meldung vermeiden möchten, können Sie zwei Ansätze verfolgen:

* Planen Sie das Berichtsformat, indem Sie den Zellen mit Anfragen und Zuordnungen Formatierungen hinzufügen
* Testen auf Bereiche des Arbeitsblatts, die Zuordnungen enthalten

Um Bereiche mit eingebetteten Anfragen zu testen, haben Sie folgende Möglichkeiten:

* Starten Sie den [!UICONTROL Anforderungs-Manager] und klicken Sie auf die einzelnen Anforderungen, die in der Tabelle aufgeführt sind. Durch Klicken auf die Anfrage werden die Zellen des Arbeitsblatts hervorgehoben, in denen die Anfrage zugeordnet ist.
* Wählen Sie Zellen im Arbeitsblatt aus, die Sie für eine neue Zuordnung verwenden möchten, und klicken Sie auf [!UICONTROL Aus Blatt]. Der [!UICONTROL Anforderungs-Manager] wählt die Anforderung in der Liste aus, die über ein Ausgabeelement verfügt, das die ausgewählte Zelle schneidet. Wenn keine Anfrage ausgewählt ist, ist die Zelle verfügbar.
* Wählen Sie Zellen in der Tabelle aus, klicken Sie mit der rechten Maustaste in das Kontextmenü und überprüfen Sie, ob [!UICONTROL Anforderung bearbeiten] verfügbar ist. Wenn ja, ist mit diesen Zellen eine Anfrage verknüpft.
