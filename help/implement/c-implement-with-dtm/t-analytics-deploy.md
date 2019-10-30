---
description: Erstellen Sie ein Adobe Analytics-Tool für die Implementierung mithilfe des Dynamic Tag Managements. Diese Anleitung beschreibt eine manuelle Implementierung (alte Methode).
keywords: Dynamic Tag Management
seo-description: Erstellen Sie ein Adobe Analytics-Tool für die Implementierung mithilfe des Dynamic Tag Managements. Diese Anleitung beschreibt eine manuelle Implementierung (alte Methode).
seo-title: Adobe Analytics manuell implementieren (alt)
solution: Experience Cloud, Analytics, Target, Dynamic Tag Management
title: Adobe Analytics manuell implementieren (alt)
uuid: d3ad2035-393d-4a77-81f6-e749ee717c09
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Adobe Analytics manuell implementieren (alt)

Erstellen Sie ein Adobe Analytics-Tool für die Implementierung mithilfe des [!UICONTROL Dynamic Tag Managements]. Diese Anleitung beschreibt eine manuelle Implementierung (alte Methode).

Informationen zur automatischen Implementierungsverwaltung finden Sie unter [Adobe Analytics-Tool hinzufügen](../../implement/c-implement-with-dtm/c-aa-tool/analytics-dtm.md#concept_FBA6679A0B79490F8296437F11E5E4F8).

Wenn Sie eine manuelle Konfiguration auf automatisch umstellen möchten, bearbeiten Sie ein Tool und klicken Sie auf **[!UICONTROL Automatische Konfiguration aktivieren]**.

1. Laden Sie den Analytics-Messungscode herunter:
   1. Klicken Sie in Analytics auf **[!UICONTROL Admin**] &gt; **[!UICONTROL Code-Manager]**.
   1. Klicken Sie auf **[!UICONTROL JavaScript (neu)]**, um den Code lokal herunterzuladen.
1. In [!UICONTROL Dynamic Tag Management] [erstellen Sie eine Webeigenschaft](../../implement/c-implement-with-dtm/t-create-web-property.md#task_960467FBB7A54499AC228CB3AA3C4123).

   ![](assets/dtm-property.png)

   Nachdem Sie die Webeigenschaft erstellt haben, ist diese auf der Registerkarte [!UICONTROL Webeigenschaften] im [!UICONTROL Dashboard] zur Bearbeitung verfügbar. Es ist nicht erforderlich, die Webeigenschaft zu aktivieren..

1. Fügen Sie der Eigenschaft ein Analytics-Tool hinzu:
   1. Klicken Sie dazu auf der Registerkarte **[!UICONTROL Webeigenschaften]** auf die Eigenschaft.
   1. Klicken Sie auf der Registerkarte **[!UICONTROL Übersicht]** auf **[!UICONTROL Tool hinzufügen]**.
   1. Wählen Sie im Menü **[!UICONTROL Tool-Typ]** die Option **[!UICONTROL Adobe Analytics]** aus.

      ![](assets/dtm-add-analytics-tool.png)

   1. Konfigurieren Sie die folgenden Felder:

      | Element | Beschreibung |
      |---|---|
      | Tool-Typ | Experience Cloud-Lösung, z. B. Analytics, Target, Social usw. |
      | Tool-Name | Der Werkzeugname. Dieser Name wird auf der Registerkarte [!UICONTROL Übersicht] unter [!UICONTROL Installierte Tools] angezeigt. |
      | Produktions-Konto-ID | Eine ID für Ihr Produktions-Konto zur Datensammlung. Das Dynamic Tag Management installiert automatisch das richtige Konto in der Produktions- und Staging-Umgebung. |
      | Staging-Konto-ID | Eine ID, die für Ihre Entwicklungs- oder Testumgebung verwendet wird. Mit dem Staging-Konto werden Ihre Testdaten von der Produktion getrennt gehalten. |

1. Klicken Sie auf **[!UICONTROL Tool erstellen]**.

   Auf der Registerkarte [!UICONTROL Übersicht] wird das installierte Tool angezeigt.

1. Klicken Sie zur Konfiguration des Codes auf **[!UICONTROL Einstellungen]** ![](assets/settings_gear.png).

   Klicken Sie mindestens auf **[!UICONTROL Cookies]und konfigurieren Sie Ihren Tracking-Server und den SSL-Tracking-Server.**

1. Klicken Sie auf **[!UICONTROL Allgemein]** und [fügen Sie den AppMeasurement-Kern-Code](../../implement/c-implement-with-dtm/c-aa-tool/t-appmeasurement-code.md#task_068D72664B2743359A64ADB8692D3658) ein.
1. Definieren Sie eine [Seitenladeregel](../../implement/c-implement-with-dtm/c-rules/t-rules-create.md#task_B7FB5ED415AF430C952265AC2835C0DB), um [!DNL Analytics]-Daten zu erfassen.

   Sie können nun Regeln zum Sammeln von Analysedaten definieren. Möglicherweise möchten Sie zuerst einige Datenelemente definieren. Mithilfe von Datenelementen können Sie Daten aus der Seite extrahieren, die Sie verwenden können, um Ihre Regel zu konfigurieren. Sie können zu Beginn eine Seitenladeregel definieren, die keine Bedingungen zum Sammeln von [!DNL Analytics]-Daten auf den einzelnen Seiten enthält.
1. [Fügen Sie auf der Registerkarte „Einbettung“ den Kopf- und Fußzeilencode hinzu.](../../implement/c-implement-with-dtm/c-headers-footers/t-header-footer-code.md#task_43C8DD699A514638B0620775C06423E5)

   Für die Staging-Umgebung können Sie die Standard-Hostingoption Amazon beibehalten. Sie können diese Option bei Bedarf vor der Implementierung in der Produktionsumgebung ändern.
1. (Optional) Klicken Sie auf der Registerkarte „Optionen“ auf **[!UICONTROL Einstellungen]** (![](assets/settings_gear.png)) und konfigurieren Sie den Adobe Analytics-Code.

   >[!NOTE]
   >
   >Die Einstellungen auf der Seite [!UICONTROL Adobe Analytics] („Allgemein“, „Cookies“ usw.) heben Einstellungen in Ihrem `s_code` auf. Wenn diese Einstellungen in Ihrem `s_code` vorhanden sind, müssen sie an dieser Stelle nicht wiederholt werden.

