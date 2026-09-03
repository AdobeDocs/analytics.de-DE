---
description: Erfahren Sie, wie Sie Berichte planen.
title: Planen einer Datenanfrage
uuid: f6d8c90f-e185-4d60-8035-f20f74bfcd89
feature: Report Builder
role: User, Admin
exl-id: 6aaadaa8-d68f-4a03-8838-53a61b152e31
TQID: https://experienceleague.adobe.com/CPg94k8G-tLWRvgdYHLz1UP2p1gJ7ad1g39rFtMWAG4
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2:
  - id: ac8a38fa-dec3-4581-8f64-178fde9f64e8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 972
ht-degree: 77%

---

# Arbeitsmappen planen

{{legacy-arb}}

Sie können Arbeitsmappen planen, erweiterte Bereitstellungsoptionen festlegen, Empfänger definieren und sich frühere Zeitpläne ansehen. Erweiterte Bereitstellungsoptionen ermöglichen die Konfigurierung von Arbeitsmappen, die Sie zu einem bestimmten Zeitpunkt oder in regelmäßigen Abständen senden möchten. Sie können außerdem das Dateiformat der Arbeitsmappe festlegen.

Beispielsweise können Sie unter [!DNL Advanced Delivery Options] Arbeitsmappen so planen, dass sie umgehend oder in regelmäßigen Zeitintervallen gesendet werden, und das Dateiformat angeben. Die Dateigröße ist für einen Arbeitsmappen-Upload auf 5 MB begrenzt.

>[!NOTE]
>
>Sie müssen über Excel 2007 verfügen oder das Compatibility Pack installieren, um eine Arbeitsmappe planen zu können. Sie können pro Report Builder-Lizenz über maximal 10 geplante Arbeitsmappen verfügen. Jedoch können Sie diese Zahl erhöhen, indem Sie bei anderen Lizenzen die benötigte Menge an Arbeitsmappen wegnehmen. Gehen Sie dazu zu **[!UICONTROL Admin]** > **[!UICONTROL Alle Administratoren]** > **[!UICONTROL Unternehmenseinstellungen]** > **[!UICONTROL Report Builder-Berichte]**. Eine Arbeitsmappe, die geplant (oder in die Arbeitsmappen-Bibliothek hochgeladen) wurde und innerhalb von 28 Monaten nicht weiterverwendet (aktualisiert, ersetzt) wurde, wird gelöscht.

>[!NOTE]
>
>Der vom Benutzer eingegebene Wert „Zeitpunkt der Auslieferung“/„Uhrzeit“ gibt den Zeitpunkt an, zu dem die Verarbeitung der Arbeitsmappe beginnt, und nicht den Zeitpunkt, zu dem sie tatsächlich bereitgestellt wird. Die tatsächliche Bereitstellungszeit der Arbeitsmappe hängt in erster Linie davon ab, wie lange die Verarbeitung dauert (bei komplexen und großen Arbeitsmappen dauert die Verarbeitung länger als bei einfacheren Arbeitsmappen). Wenn die Verarbeitung einer Arbeitsmappe z. B. 15 Minuten dauert, ist die tatsächliche Auslieferungszeit frühestens 15 Minuten nach dem ursprünglich angegebenen „Zeitpunkt der Auslieferung“/„Uhrzeit“.
>Darüber hinaus gibt es weitere Faktoren, die die Verzögerung vor der tatsächlichen Auslieferung der Arbeitsmappe weiter erhöhen können:
>
> * **Das gleichzeitige Ausführen vieler verschiedener Zeitpläne desselben Typs** kann das System überlasten. Das Planungssystem erlaubt nur die gleichzeitige Ausführung einiger (5–10) Arbeitsmappen eines Typs. Wenn also mehr als 5–10 gleichzeitig geplant sind, müssen einige warten, bis andere Arbeitsmappen fertig sind, bevor mit deren Verarbeitung begonnen werden kann. Dieses Problem kann behoben werden, indem die Arbeitsmappen eines Unternehmens über den ganzen Tag oder eine Stunde hinweg gestaffelt und nicht gleichzeitig ausgeführt werden.
> * Neben dem Arbeitsmappentyp liegen Arbeitsmappen auch dann in der Warteschlange, wenn das Unternehmen **mehr als 15–20 Arbeitsmappen einer Art gleichzeitig geplant hat (alle Arbeitsmappentypen)**. Dieses Problem kann durch gestaffelte Zeitpläne gelöst werden, sodass nicht viele gleichzeitig ausgeführt werden.
> * **Probleme bei den nachgelagerten Diensten**, auf denen die Planung basiert, können sich auch auf die Bereitstellung von Arbeitsmappen auswirken. Wenn Sie beispielsweise unabhängig voneinander die APIs zum Ausführen von Arbeitsmappen und zum Füllen der API-Anforderungswarteschlange verwenden, werden Ihre geplanten Arbeitsmappen möglicherweise langsam bereitgestellt, da Sie diese Ressource mit einer anderen Funktion teilen.
> * **Die Report Suite-Latenz** (Verzögerung bei der Datenerfassung) kann auch eine Verzögerung bei geplanten Arbeitsmappen bewirken.

## Arbeitsmappe planen

1. Erzeugen Sie eine Arbeitsmappe und speichern Sie ihn.
1. Klicken Sie auf der Report Builder-Symbolleiste auf **[!UICONTROL Plan]**.

   Die Registerkarte [!UICONTROL Terminierte Berichte] enthält eine Zusammenfassung aller von Ihnen erstellten Aufgaben sowie die Anzahl der verbleibenden Aufgaben.
1. Klicken Sie auf **[!UICONTROL Registerkarte]** Geplante Berichte“ auf **[!UICONTROL Neu]**. Der Assistent Einfache Planung zeigt die Optionen an, die zum Definieren des terminierten Berichts verwendet werden.

   ![Screenshot mit dem Assistenten für die allgemeine Planung.](assets/simple-schedule-wizard.png)

1. Konfigurieren Sie im Fenster [!UICONTROL Planungs-Assistent – Grundlegend] die folgenden Optionen:

| Feld | Beschreibung |
|--- |--- |
| Bericht auswählen | Der Name der Arbeitsmappe. Bei neuen terminierten Berichten wird dieses Feld mit dem Namen der aktiven Arbeitsmappe ausgefüllt. |
| Auswählen | Hierdurch wird die Seite „Bericht auswählen“ angezeigt. Sie können einen Bericht vom Server (wo alle früher geplanten Arbeitsmappen gespeichert sind) oder von Ihrem lokalen Computer auswählen. Wenn Sie eine Arbeitsmappe von der lokalen Festplatte im .xls-Format auswählen, wandelt das System sie in eine .xlsx-Datei um. Im Rahmen der Konversion wird die Datei in Excel geöffnet und aktiviert. Wenn die ausgewählte Arbeitsmappe für den terminierten Bericht denselben Dateinamen wie die derzeit in Excel geöffnete Arbeitsmappe hat, wählt das System die lokale Datei anstelle der zuvor hochgeladenen Datei aus. Wenn Sie einen Bericht aus dem Zeitplan-Repository auswählen, wird eine Kopie der Arbeitsmappe auf dem Server erstellt, wobei ihr Dateiname mit 1 aktualisiert wird. Der neu erstellte terminierte Bericht verwendet die kopierte Arbeitsmappe. |
| Anpassen | Ermöglicht die Anpassung des Datumsformats. |
| An | Zeigt Ihr Outlook-Adressbuch an, falls zutreffend. |
| Senden an: E-Mail | Die E-Mail-Adresse des Empfängers der Arbeitsmappe. |
| Power BI | Weitere [&#x200B; finden Sie unter „Veröffentlichen von Arbeitsmappen &#x200B;](/help/analyze/legacy-report-builder/c-publish-power-bi/integration-power-bi.md) Microsoft Power BI&quot;. |
| Betreff | Eine benutzerdefinierte Beschreibung. |
| Zeitplan | Hier können Sie angeben, wann die Arbeitsmappe gesendet werden soll (sofort, stündlich, täglich, wöchentlich oder jährlich). |

## Erweiterte Bereitstellungsoptionen

1. Klicken Sie auf **[!UICONTROL Erweiterte Bereitstellungsoptionen]**, um Datei- und Veröffentlichungsoptionen zu konfigurieren:

| Feld | Beschreibung |
|--- |--- |
| Registerkarte **Zeitplan** |  |
| Zeitpunkt der Bereitstellung | Hier können Sie eine sofortige oder spätere Auslieferung der Arbeitsmappe planen. Die Tageszeit bezieht sich auf die auf dem Computer angegebene Zeitzone. |
| Wiederholungsmuster | Hiermit wird die Arbeitsmappe entsprechend Ihrer Auswahl gesendet. |
| Bereich des Intervalls | Hier geben Sie an, wann der Empfang der Arbeitsmappe beginnen und stoppen soll.   Hinweis: Wenn Sie eine Arbeitsmappe für den ersten Tag eines bestimmten Zeitraums (Woche, Monat, Quartal oder Jahr) planen, werden nur Daten für den ersten Tag zurückgegeben. |
| Registerkarte **Dateioptionen** |  |
| Dateiformat | Hier können Sie als Bereitstellungsformat Excel 2007 (.xlsx) oder 2003 (.xls), .pdf, .csv, .mht, .txt oder .xml auswählen. |
| Dateiziel | Gibt E-Mail oder FTP an. Die verfügbaren Optionen wechseln ja nach der bisherigen Auswahl. Bei FTP müssen Sie sicherstellen, dass der Host extern verfügbar ist. |
| Sprache des Dateiinhalts | Gibt die Sprache an, die für das Anschreiben verwendet werden soll. Sie können Chinesisch (vereinfacht oder traditionell), Deutsch, Französisch, Japanisch, Koreanisch, Portugiesisch (Brasilien) oder Spanisch auswählen. |
| Registerkarte **Veröffentlichungsoptionen** |  |
| In Power BI veröffentlichen | <ul><li>Arbeitsmappe in Power BI veröffentlichen</li><li>Alle Report Builder-Anforderungen als Power BI-Datensätze veröffentlichen</li><li>Alle formatierten Tabellen als Power BI-Datensätze veröffentlichen</li></ul> |
| Diesen Power BI-Bericht kennzeichnen als | Kennzeichnungsdetails |

1. Klicken Sie auf **[!UICONTROL OK]** und dann auf **[!UICONTROL Beenden]**.

   Report Builder zeigt die terminierte Arbeitsmappe im [Manager für geplante Aufgaben](/help/analyze/legacy-report-builder/r-arb-scheduled-reports.md) an.
