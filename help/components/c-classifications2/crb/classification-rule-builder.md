---
description: Statt Classifications bei jeder Trackingcode-Änderung zu verwalten und hochzuladen, können Sie automatische, regelbasierte Classifications erstellen und diese auf mehrere Report Suites anwenden. Regeln werden in kurzen Intervallen verarbeitet, die sich nach Ihrem Classification-Bezogenen Trafficvolumen richten.
subtopic: Classifications
title: Classification Rule Builder-Workflow
topic: Admin tools
uuid: edb1f07e-fa86-4055-8f4b-cce2d370edbb
translation-type: tm+mt
source-git-commit: ad991b8fcc309d1f3aae01d472683927a447ab4d
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 92%

---


# Classification Rule Builder-Workflow

Statt Classifications bei jeder Trackingcode-Änderung zu verwalten und hochzuladen, können Sie automatische, regelbasierte Classifications erstellen und diese auf mehrere Report Suites anwenden. Regeln werden in kurzen Intervallen verarbeitet, die sich nach Ihrem Classification-Bezogenen Trafficvolumen richten.

## Wichtiger Hinweis vor Beginn

Beachten Sie Folgendes, bevor Sie mit der Verwendung von Klassifizierungsregeln beginnen:

* Unter-Classifications werden nicht von Classification Rule Builder (CRB) unterstützt.
* Unser aktuelles Klassifizierungssystem kann bis zu 10 Millionen Zeilen gleichzeitig exportieren.
* Wenn CRB einen Export anfordert, zieht es sowohl klassifizierte als auch nicht klassifizierte Werte, wobei nicht klassifizierte Werte am Ende des Exports durchlaufen werden. Das bedeutet, dass man im Laufe der Zeit 10 Millionen klassifizierte Werte auflisten könnte, ohne jemals zu den nicht klassifizierten Werten zu gelangen.
* Da die Architektur so eingerichtet ist, dass der CRB Werte von Servern mit der Anzahl „n“ abrufen kann, kann dies zu Inkonsistenzen dahingehend führen, welche Server aufgenommen werden und in welcher Reihenfolge. Aus diesem Grund ist es sehr schwierig, nicht klassifizierte Werte zu erhalten.

Hier finden Sie die **Lösung** für diejenigen, die mehr als 10 Millionen klassifizierte Werte für eine Dimension haben: Sie müssen nicht klassifizierte Werte per FTP in 10 Millionen Stapel exportieren und manuell klassifizieren.

## Erste Schritte mit Classification-Regeln {#section_3FF666EF9D5B4E37A23B3FB400CDA2E6}

**[!UICONTROL Admin]** > **[!UICONTROL Classification Rule Builder]**

Für die Implementierung von Klassifizierungsregeln gelten die nachfolgenden allgemeinen Schritte:

| Schritt | Wo | Beschreibung |
|--- |--- |--- |
| Schritt 1 (Voraussetzung): [Klassifizierungsschema einrichten](https://docs.adobe.com/content/help/en/analytics/components/classifications/c-classifications.html). | [!UICONTROL Admin] > [!UICONTROL Report Suites] > [!UICONTROL Einstellungen bearbeiten] > &lt;Traffic-Klassifizierungen oder Konversionsklassifizierungen> | Wählen Sie eine Variable aus und definieren Sie die für die Variable zu verwendenden Classifications. <br>Für Variablen muss mindestens eine Classification-Spalte erstellt werden, bevor sie in Regeln genutzt werden können.<br>Sobald Classifications aktiviert sind, können Sie den Importeur und den Rule Builder verwenden, um bestimmte Werte zu klassifizieren. |
| Schritt 2: [Regelsatz erstellen](/help/components/c-classifications2/crb/classification-rule-set.md). | [!UICONTROL Admin] > [!UICONTROL Classification Rule Builder] > [!UICONTROL Regelsatz hinzufügen] | Ein Regelsatz ist eine Gruppe von Classification-Regeln für eine bestimmte Variable. |
| Schritt 3: Report Suites und Variablen konfigurieren. | [!UICONTROL Classification Rule Builder] >  &lt;Ihr Regelsatz> | Wenden Sie den Regelsatz auf Report Suites und Variablen an. |
| Schritt 4: [Klassifizierungsregeln zum Satz hinzufügen](/help/components/c-classifications2/crb/classification-quickstart-rules.md). | [!UICONTROL Classification Rule Builder] >  &lt;Ihr Regelsatz> | Ordnen Sie einer Classification eine Bedingung zu, und legen Sie die Aktion fest, die für die Regel ausgeführt werden soll.  Machen Sie sich mit den Informationen unter [Verarbeitung der Regeln](/help/components/c-classifications2/crb/classification-quickstart-rules.md) vertraut. |
| Schritt 5: [Testen eines Klassifizierungsregelsatzes](/help/components/c-classifications2/crb/classification-quickstart-rules.md) | [!DNL Testing Page] | Zum Testen der Regeln im Rahmen der Validierung bearbeiten Sie die Regeln im Entwurfsmodus. Im Entwurfsmodus können keine Regeln ausgeführt werden.<br>Dieser Schritt ist bei der Verwendung [regulärer Ausdrücke](/help/components/c-classifications2/crb/classification-quickstart-rules.md) wichtig. |
| Schritt 6: [Gültige Regeln aktivieren](/help/components/c-classifications2/crb/classification-rule-definitions.md). | [!DNL Rules Page] | Sobald die Regeln gültig sind, aktivieren Sie den Regelsatz.  Bei Bedarf können Sie vorhandene Schlüssel überschreiben. Siehe [Verarbeitung der Regeln](/help/components/c-classifications2/crb/classification-quickstart-rules.md). |
| Schritt 7 (Optional): [Unerwünschte Regeln löschen](/help/components/c-classifications2/crb/classification-rule-definitions.md). | [!DNL Rules Page] | Löschen Sie die unerwünschten Regeln aus dem Satz.<br>Hinweis: Beim Löschen von Regeln werden die hochgeladenen klassifizierten Daten nicht gelöscht.  Informationen zum Löschen klassifizierter Daten finden Sie unter [Löschen von Klassifizierungsdaten](/help/components/c-classifications2/c-classifications-importer/t-delete-classification-data.md). |

>[!NOTE]
>
>Gruppen mit der Berechtigung zum Nutzen des Klassifizierungsimport-Werkzeugs können Klassifizierungsregeln verwenden. Wichtige Verarbeitungsinformationen finden Sie unter [Verarbeitung der Regeln](/help/components/c-classifications2/crb/classification-quickstart-rules.md).

**Zusätzliche Ressourcen**

**Blog**: Weitere Informationen zu dieser Funktion finden Sie im Digital Marketing Blog: [Regelbasierte Klassifizierungen](https://theblog.adobe.com/rule-based-classifications-part-1-making-classifications-easier/).

**Video**: Auf [YouTube](https://www.youtube.com/watch?v=6laI5SBXY-I) können Sie sich das Video [!UICONTROL Klassifizierungsübersicht] ansehen.
