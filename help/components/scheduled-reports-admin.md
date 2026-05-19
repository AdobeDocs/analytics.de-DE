---
description: Damit können Administratoren terminierte Berichte für die ganze Organisation anzeigen und verwalten.
title: Warteschlange für terminierte Berichte
feature: Admin Tools
uuid: 3fcf92d3-a472-465f-ad7a-c48cd9a8238b
exl-id: 7287e6c7-e354-48a0-9343-35dccfc46e63
role: Admin
TQID: https://experienceleague.adobe.com/HL78cbB5NqKCjv4NvZ5OiqjfbwBjI0KAC8hEr8Afd2U
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
subfeature_v2:
  - id: c80b99d6-98b9-4aeb-b5c4-933ef2ef705c
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 319
ht-degree: 53%

---

# Warteschlange für terminierte Berichte

Damit können Administratoren terminierte Berichte für die ganze Organisation anzeigen und verwalten.

**[!UICONTROL Analytics]** > **[!UICONTROL Komponenten]** > **[!UICONTROL Alle Komponenten]** > **[!UICONTROL Geplante Berichte]**

Zu den Admin-spezifischen Fähigkeiten des Managers für terminierte Berichte gehören:

* Die Option [Alle terminierten Berichte anzeigen](/help/components/scheduled-reports-admin.md#section_3F167CAAEEC24140B476CF95B7402690) in Ihrer Organisation.
* [Erweiterte Filterfunktionen](/help/components/scheduled-reports-admin.md#section_206A52A85DE84947AAB3AD082FBF6275) in Ihrer gesamten Organisation.
* Die neue Registerkarte [Berichtswarteschlange](/help/components/scheduled-reports-admin.md#section_03C866115D354BB182E90BF4D52F1E0B) mit allen Berichten, die auf Reporting-Servern zur Ausführung in die Warteschlange gestellt werden.
* Anzeigen der [Zeitplan-ID](/help/components/scheduled-reports-admin.md#section_568B70F4228C4229977CB85D2DCD53A1) in der Benutzeroberfläche der Berichtwarteschlange.

## Alle terminierten Berichte anzeigen {#section_3F167CAAEEC24140B476CF95B7402690}

Auf der Registerkarte **[!UICONTROL Berichtsliste]** können Sie neben den von Ihnen terminierten Berichten mit der Option **[!UICONTROL Alle terminierten Berichte anzeigen]** alle terminierten Berichte in Ihrer Organisation anzeigen.

>[!NOTE]
>
>Die Spalte **[!UICONTROL Berichtsname]** zeigt den Namen des terminierten Berichts an, und die Spalte **[!UICONTROL Dateiname]** zeigt benutzerdefinierte Dateinamen an, die Sie unter „Erweiterte Bereitstellungsoptionen“ festgelegt haben. Wenn Sie also mehrere Berichte desselben Berichtstyps planen und für jeden Bericht benutzerdefinierte Namen angeben, zeigt der Manager für terminierte Berichte mehrere Einträge mit demselben Berichtsnamen, aber mit unterschiedlichen Dateinamen an. Dies liegt daran, dass der geplante Back-End-Bericht identisch ist, sodass die Spalte Berichtsname für alle außer den benutzerdefinierten Dateinamen (als festgelegt) dieselben Berichtsnamen enthält.

![](assets/show_all_scheduled_reports.png)

## Erweiterte Filterfunktionen {#section_206A52A85DE84947AAB3AD082FBF6275}

Beispiel: Wenn Sie nach allen Berichten filtern möchten, die für die stündliche Ausführung geplant sind, geben Sie **[!UICONTROL Häufigkeit = Stündlich]** in den Filter **[!UICONTROL Erweitert]** ein und klicken Sie auf **[!UICONTROL Übernehmen]**:

![](assets/advanced_filtering_schedl_reports.png)

## Berichtwarteschlange {#section_03C866115D354BB182E90BF4D52F1E0B}

Mit dieser Warteschlange können Sie alle terminierten Berichte verwalten und möglicherweise löschen, die die Warteschlange „verstopfen“. (In der Regel tritt bei Berichten eine Zeitüberschreitung nach 4 Stunden auf.)

![](assets/scheduled_reports_2.png)

Die Berichtswarteschlange bietet außerdem die Möglichkeit, „einen terminierten Bericht einmal zu überspringen“. Klicken Sie einfach auf das blaue Symbol in der Spalte **[!UICONTROL Verwalten]**.

## Zeitplan-ID {#section_568B70F4228C4229977CB85D2DCD53A1}

Die **[!UICONTROL Zeitplan-ID]** wird in der Benutzeroberfläche der Berichtwarteschlange angezeigt, falls Sie die Kundenunterstützung von Adobe kontaktieren müssen, um ein Problem mit terminierten Berichten zu lösen.

![](assets/schedule_id.png)
