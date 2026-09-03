---
description: Details zur Analysis Workspace-Vorlage und zum Reporting in Report Builder.
title: Berichte zu Werbedaten in Adobe Analytics
feature: Advertising Analytics
exl-id: bbc830d9-e168-471d-a1ba-308277aab415
TQID: https://experienceleague.adobe.com/BOly6gaT1ybHWDppJzhi9ILClvJ9UoLzkGFua1gS1lo
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
subfeature_v2:
  - id: a9364d69-0c51-44bf-8b5f-6d99c04493b8
  - id: ac8a38fa-dec3-4581-8f64-178fde9f64e8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 350
ht-degree: 9%

---

# Bericht zu Werbedaten

Dieser Artikel enthält Details zum Analysis Workspace-Bericht und zum Reporting in Report Builder.

>[!NOTE]
>
>Rechnen Sie damit, dass Sie mindestens 24 Stunden warten müssen, bevor die Suchmaschinendaten in Analytics-Berichte aufgenommen werden. Die Analytics-Berichterstellung gibt keine Daten mit stündlicher Granularität zurück, da Adobe Advertising-Daten keine stündliche Granularität unterstützen.

## Paid Search-Bericht {#section_8173F42B2C784F41B9FD82CBB66F9ADF}

Dieser Bericht ermöglicht allen Personen, die die Suchmaschinenintegration implementieren, den Zugriff auf Suchmaschinendaten in Analytics. Sie können darauf über **[!UICONTROL Workspace]** > **[!UICONTROL Berichte]** > **[!UICONTROL Akquise]** > **[!UICONTROL Advertising Analytics: Paid Search zugreifen]**

>[!NOTE]
>
>Der Paid Search-Bericht ist für alle Kunden sichtbar, auch wenn Sie keine Advertising-Konten implementiert haben. Wenn Sie versuchen, den Paid-Search-Bericht für ein Unternehmen zu öffnen, das nicht bereitgestellt wurde, wird eine Fehlermeldung angezeigt, die besagt, dass Sie kein Suchmaschinenkonto konfiguriert haben. Wählen Sie **[!UICONTROL Jetzt konfigurieren]** aus, um zum Bildschirm [Advertising-Konto-Einrichtung](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-create-ad-account.md) zu gelangen.

![](assets/aa_aw.png)  ![](assets/aa_aw2.png) ![](assets/aa_aw3.png) ![](assets/aa_aw4.png)  ![](assets/aa_aw5.png) ![](assets/aa_aw6.png)

| Tabelle/Visualisierung | Beschreibung |
|--- |--- |
| Werbetrends | Tägliche Trend-Übersicht für AMO-Impressionen, AMO-Klicks und AMO-Kosten. |
| Werbeplattformen | Ringdiagramm für die Kosten der zwei wichtigsten Plattformen (Google Ads, Microsoft Advertising). |
| Anzeigenplattform gesamt | Freiformtabelle der Top-Plattformen, aufgeschlüsselt nach AMO-Impressionen, AMO-Klicks, AMO-Kosten, AMO-Durchschnitt. Position, AMO-Durchschnitt Qualitätsbewertung. |
| Konten | Gestapelter Kostenbereich. |
| Konto gesamt: | Freiformtabelle der Top-Konten, aufgeschlüsselt nach den zugehörigen Metriken. |
| Kampagnen | Balkendiagramm der Kampagnenkosten. |
| Kampagne gesamt | Freiformtabelle der Top-Kampagnen, aufgeschlüsselt nach den zugehörigen Metriken. |
| Gruppen | Baumdiagramm der Kosten. |
| Gruppe gesamt | Freiformtabelle der Top-Werbegruppen, aufgeschlüsselt nach den zugehörigen Metriken. |
| Werbeanzeigen | Horizontales Balkendiagramm mit Impressionen, Klicks und Kosten. |
| Anzeige gesamt: | Freiformtabelle der Top-Anzeigen, unterteilt nach den zugehörigen Metriken. |
| Suchbegriffe | Streudiagramm der Impressionen, Klicks und Kosten für alle Keyword-/Übereinstimmungstyp-Kombinationen. |
| Keywords gesamt | Freiformtabelle der wichtigsten Kombinationen aus Keyword- und Übereinstimmungstyp, aufgeschlüsselt nach den zugehörigen Metriken. |

## Report Builder {#section_8E0371CF81144C33990D909685D1726E}

Sobald Sie ein Advertising Analytics-Konto eingerichtet haben, wird der Advertising Analytics-Bericht bereitgestellt.
