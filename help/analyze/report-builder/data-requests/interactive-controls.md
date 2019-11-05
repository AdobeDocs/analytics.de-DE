---
description: Mit interaktiven Steuerelementen können Sie direkt im Arbeitsblatt Segmente und Datumsbereiche für eine oder mehrere Anforderungen bearbeiten. Dadurch erhalten Sie beim Aktualisieren von ReportBuilder-Anforderungen mehr Flexibilität.
seo-description: Mit interaktiven Steuerelementen können Sie direkt im Arbeitsblatt Segmente und Datumsbereiche für eine oder mehrere Anforderungen bearbeiten. Dadurch erhalten Sie beim Aktualisieren von ReportBuilder-Anforderungen mehr Flexibilität.
seo-title: interaktive Steuerelemente
solution: Analytics
title: interaktive Steuerelemente
topic: ReportBuilder
uuid: 5f324b61-e032-455e-9947-5037f013e0fa
translation-type: tm+mt
source-git-commit: 8c4c368a84ba5499d85f0b7512c99de47ddb14c2

---


# interaktive Steuerelemente

Mit interaktiven Steuerelementen können Sie direkt im Arbeitsblatt Segmente und Datumsbereiche für eine oder mehrere Anforderungen bearbeiten. Dadurch erhalten Sie beim Aktualisieren von ReportBuilder-Anforderungen mehr Flexibilität.

Interaktive Steuerelemente wurden als Antwort auf einen gemeinsamen Workflow erstellt, bei dem Analysten Arbeitsmappen erstellen und diese mit der Marketingorganisation teilen. Mit interaktiven Steuerelementen können Marketingexperten Anforderungen anpassen und aktualisieren, ohne dabei die Funktionsweise von ReportBuilder genau kennen zu müssen. (Beachten Sie, dass der Arbeitsmappenempfänger ein ReportBuilder-Benutzer sein muss, um eine Anforderung aktualisieren zu können.) Diese Steuerelemente funktionieren innerhalb geplanter Arbeitsmappen. Derzeit sind zwei Arten interaktiver Steuerelemente verfügbar:

* Rollierender Datumsbereich
* Segmente

>[!IMPORTANT]
>
>Damit die interaktiven Steuerelemente funktionieren, muss ReportBuilder Version 5.0 installiert sein. &gt;
>* Wenn Sie Microsoft Excel unter Windows ausführen, aber eine niedrigere Version von ReportBuilder ausführen oder wenn ReportBuilder nicht installiert ist: Sie können den Wert im interaktiven Steuerelement ändern. Die zugehörige Anforderung wird jedoch nicht aktualisiert und die zugehörigen Parameter der Anforderung werden auch nicht aktualisiert.
>* Wenn Sie Excel unter Mac ausführen, wird beim Ändern des Werts im Steuerelement die folgende Meldung angezeigt: "Das Makro 'Adobe.ReportBuilder.Bridge.FormControlClick.Event' kann nicht gefunden werden."
>



>[!IMPORTANT]
>
>Ändern Sie nicht den Namen des Steuerelements. (Zum Anzeigen des Namens fokussieren Sie das Steuerelement. Der Name des Steuerelements wird dann direkt über dem Excel-Raster in der oberen linken Ecke angezeigt.)

## Implement interactive date range control {#section_39B228F2D2C44985863D31424C953280}

1. Wählen Sie in Schritt 1 des Anforderungs-Assistenten zum Beispiel den Bericht **[!UICONTROL Seite]aus.**
1. Klicken Sie neben dem Dropdown-Menü **[!UICONTROL Häufig verwendete Datumsangaben]** auf das Symbol **Steuerungseinstellungen[!UICONTROL :]**

   ![](assets/date_range_control.png)

1. Wählen Sie im Dialogfeld „Steuerungseinstellungen“ alle Datumsbereichselemente aus, die im interaktiven Steuerelement angezeigt werden sollen. Legen Sie außerdem den oberen linken Zellenstandort des Steuerelements fest.

   ![](assets/control_settings.png)

1. Beachten Sie die Option "Verknüpfte Anforderungen bei Elementauswahl automatisch aktualisieren".

   * Wenn diese aktiviert ist, werden alle Anforderungen aktualisiert, die dieses Steuerelement verwenden.
   * Wenn sie nicht aktiviert ist, werden zwar die verknüpften Anforderungsparameter aktualisiert, jedoch nicht die Anforderung selbst.

1. Klicken Sie auf **[!UICONTROL OK]**. Das Steuerelement wird in dem von Ihnen festgelegten Zellenstandort angezeigt:

   ![](assets/date_range_control_interactive.png)

1. Nun können Sie den Datumsbereich ändern und die Anforderung wird mit diesem Datumsbereich aktualisiert.
1. Sie können die Anforderung auch kopieren und mit der rechten Maustaste darauf klicken, um eine der zwei Optionen zum Einfügen von Anforderungen zu verwenden:

   * **[!UICONTROL Anforderung]** einfügen &gt; **[!UICONTROL Absolute Eingabezelle]** verwenden. Das bedeutet, dass die kopierte Anforderung zu demselben interaktiven Steuerelement für Datumsbereiche verweist wie die ursprüngliche Anforderung.

   * **[!UICONTROL Anforderung]** einfügen &gt; Relative Eingabezelle **[!UICONTROL verwenden]**. Das bedeutet, dass die kopierte Anforderung zum eigenen Steuerelement verweist.

      >[!NOTE]
      >
      >Sie können die native Microsoft Excel-Steuerungsfunktion zum Ausschneiden/Kopieren/Einfügen verwenden. ReportBuilder erkennt die neu hinzugefügten Steuerelemente automatisch.

## Implement interactive segment control {#section_5003D3F724644280BF1BCD6E1B0CB784}

Das Implementieren interaktiver Steuerelemente für Segmente ähnelt dem Implementieren des Steuerelements für Datumsbereiche.

1. Wählen Sie in Schritt 1 des Anforderungs-Assistenten neben dem Dropdown-Menü **[!UICONTROL Segment]das Symbol für die Segmentsteuerungseinstellungen:**

   ![](assets/segment_interactive_1.png)

1. Wählen Sie im Dialogfeld für die Segmentsteuerungseinstellungen die Segmente aus, die im Dropdown-Menü enthalten sein sollen. Legen Sie außerdem den oberen linken Zellenstandort des Steuerelements fest.

   ![](assets/segment_drop_down_properties.png)

1. Das neue interaktive Steuerelement wird nun in der Arbeitsmappe angezeigt:

   ![](assets/segment_interactive_3.png)

