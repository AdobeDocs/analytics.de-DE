---
description: Erläutert, wie in Report Builder veröffentlichte Assets in Power BI Desktop abgerufen werden
title: Veröffentlichte Assets in Power BI Desktop abrufen
feature: Report Builder
role: User, Admin
exl-id: ce6020df-caf4-4cd2-8086-4357309e5bbb
TQID: https://experienceleague.adobe.com/fS1xnUciNh8LdPw2ENYMJTDGLqo3C8u4lu39X-GYuZE
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2: id: ac8a38fa-dec3-4581-8f64-178fde9f64e8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 222
ht-degree: 69%

---

# Veröffentlichte Assets in Power BI Desktop abrufen

{{legacy-arb}}

Erläutert, wie in Report Builder veröffentlichte Assets in Power BI Desktop abgerufen werden

## Voraussetzungen {#section_BDFDAE1E300B429FB6EBCB21AD1383A0}

* Sie müssen die neueste Power BI Desktop-Version installiert haben (Version April 2017)
* In dieser Vorgehensweise wird davon ausgegangen, dass Sie bereits formatierte Report Builder-Tabellen oder Anforderungen für den Power BI-Dienst veröffentlicht haben.

## Prozess {#section_CB03E6E1B066457EA0F6FC08FFF5EFDD}

In der Power BI-Desktop-Aktualisierung vom April 2017 hat Microsoft die Möglichkeit veröffentlicht, eine Verbindung zu Datensätzen im Power BI-Service herzustellen. Mit dieser Funktion können Sie neue Berichte zu vorhandenen Datensätzen erstellen, die Sie bereits in der Cloud veröffentlicht haben. Sie können diese Funktion nutzen, um die Zusammenarbeit in Ihrem gesamten Team zu verbessern und Doppelarbeit zu reduzieren.

1. Gehen Sie in Power BI Desktop zu **[!UICONTROL Datei]** > **[!UICONTROL Optionen und Einstellungen]** > **[!UICONTROL Optionen]** > **[!UICONTROL Vorschaufeatures.]**
1. Aktivieren Sie **[!UICONTROL Live-Verbindung mit Power BI-Dienst]** und klicken Sie auf **[!UICONTROL OK]**. ![Klicken Sie auf „Live-Verbindung mit Power BI-Dienst“ und dann auf „OK“. ](assets/bi-preview-features.png)

1. Starten Sie Power BI Desktop neu.
1. Sobald Sie Desktop neu gestartet haben, wechseln Sie zu **[!UICONTROL Start]** > **[!UICONTROL Daten abrufen]** > **[!UICONTROL Mehr...]**.
1. Suchen Sie nach **[!UICONTROL Power BI-Dienst]** und wählen Sie ihn aus.
1. Wählen Sie unter **[!UICONTROL Microsoft Power BI-Dienst]** > **[!UICONTROL Arbeitsbereich]** den zuvor in Report Builder veröffentlichten Datensatz aus.

Weitere Informationen finden Sie in diesem [Microsoft-Blogpost](https://powerbi.microsoft.com/en-us/blog/connecting-to-datasets-in-the-power-bi-service-from-desktop/).
