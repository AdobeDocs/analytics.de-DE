---
description: Erfahren Sie, wie Sie Metriken in einer bereits vorhandenen Anfrage oder über eine Gruppe von Anfragen hinweg hinzufügen, entfernen oder ersetzen.
title: Bearbeiten von Metriken über mehrere Anfragen hinweg
feature: Report Builder
role: User, Admin
exl-id: e537b67a-aa07-4acd-a476-7497426e2f7d
TQID: https://experienceleague.adobe.com/epK-BLSIpnZV1-0eqPxb2aGXSbon4Oc1mRDnRljpCxI
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 598
ht-degree: 18%

---

# Metriken mit Mehrfachanforderungen bearbeiten

{{legacy-arb}}

Metriken in einer bereits vorhandenen Anfrage oder über eine Gruppe von Anfragen hinweg hinzufügen, entfernen oder ersetzen.

## Kennzahlen hinzufügen {#section_3FBDA9668039404895059618D70FCBCD}

Beachten Sie beim Hinzufügen von Metriken die folgenden Richtlinien:

* Metriken können nur zu Pivot-Layout-Anfragen hinzugefügt werden.
Wenn einige der ausgewählten Anforderungen benutzerdefinierte Layouts sind, können keine Metriken hinzugefügt werden. Wenn das Layout angepasst ist, weiß Report Builder nicht, wo die neue Metrik in der Tabelle platziert werden soll.
* Wenn Sie nur benutzerdefinierte Layout-Anfragen auswählen, ist die Option **[!UICONTROL Metriken hinzufügen]** nicht verfügbar.
* Das Hinzufügen von Metriken erhöht die Größe einer Anfrage und kann dazu führen, dass sie sich mit einer anderen Anfrage überschneidet. Stellen Sie sicher, dass Ihre Anfrage rundherum ausreichend Platz zum Hinzufügen von Metriken hat.
* Wenn die hinzugefügte Metrik bereits in einer der ausgewählten Anfragen vorhanden ist, wird sie dieser Anfrage nicht hinzugefügt.

So fügen Sie eine oder mehrere Metriken hinzu

1. Wählen Sie mindestens eine Anforderung in Excel aus, klicken Sie mit der rechten Maustaste darauf und wählen Sie **[!UICONTROL Metriken bearbeiten]** aus. (Oder klicken Sie auf **[!UICONTROL Verwalten]** > **[!UICONTROL Mehrere bearbeiten]** > `<choose metric>` > **[!UICONTROL Gruppe bearbeiten]**, um die zu ändernde Anforderungsgruppe auszuwählen.)
1. Wählen Sie **[!UICONTROL Metrik(en) hinzufügen]** und danach die entsprechenden Metriken aus.

   ![Screenshot, der die ausgewählte Option „Anfrage bearbeiten“, „Metriken hinzufügen“ zeigt.](assets/add_metric.png)

1. Aktualisieren Sie die Anforderung, um die tatsächlichen Daten anzuzeigen. Offline-Daten werden angezeigt, bis Sie die Daten aktualisieren.

## Metriken ersetzen

Beachten Sie beim Ersetzen von Metriken die folgenden Richtlinien:

* Es :1 nur 1 Ersetzungen zulässig. 1:many oder viele:1 sind nicht zulässig.
* Wenn die ausgewählte Metrik in einer der ausgewählten Anfragen nicht vorhanden ist, bleibt die Anfrage unverändert.
* Die neue Metrik wird an derselben Stelle platziert wie die ersetzte Metrik.

   * **Wenn in einem Pivot** Layout eine Pivot-Layout-Anfrage Datum, Besuch, Besucher, tägliche Unique Visitors und *Visitors* durch *Umsatz* ersetzt, lautet das aktualisierte Anfrage-Layout: Datum, Besuch, Umsatz und täglich eindeutig.
   * **Wenn bei einem benutzerdefinierten Layout** die Metrik *Besucher* in Zelle F11 ausgegeben wurde, zeigt das aktualisierte Anfrage-Layout *Umsatz* in derselben Zelle F11 an.

* Wenn auf die ersetzte Metrik ein Vorgang angewendet wurde (durchschnittlicher, vorangestellter Text, Text nach dem Anfügen, Microchart), werden diese Vorgänge auch auf die neue Metrik angewendet.

So ersetzen Sie eine Metrik

1. Wählen Sie mindestens eine Anforderung in Excel aus, klicken Sie mit der rechten Maustaste darauf und wählen Sie **[!UICONTROL Metriken bearbeiten]** aus. Alternativ können Sie auf **[!UICONTROL Verwalten]** > **[!UICONTROL Mehrere bearbeiten]** > **`<choose metric>`** > **[!UICONTROL Gruppe bearbeiten]** klicken, um die Gruppe der zu ändernden Anfragen auszuwählen.

1. Wählen Sie **[!UICONTROL Metrik ersetzen]** aus.

   ![Screenshot des Bildschirms „Gruppe bearbeiten“ mit ausgewählter Option „Metrik ersetzen“](assets/replace_metric.png)

1. Wählen Sie die Metrik aus, die Sie ersetzen möchten, und die Ersatzmetrik.
1. Aktualisieren Sie die Anforderung. Offline-Daten werden angezeigt, bis Sie die Daten aktualisieren.

## Kennzahlen entfernen {#section_D3CD5BAC7670416593B633B2B8423C60}

Beachten Sie beim Entfernen von Metriken die folgenden Richtlinien:

* Wenn eine der Metriken, die Sie zum Entfernen auswählen, in einer der ausgewählten Anfragen nicht vorhanden ist, wird die Anfrage unverändert gelassen.
* Wenn Sie in einem Pivot-Layout eine Metrik entfernen, ändert sich das Layout bei Metriken, die sich nach der entfernten Metrik befinden. Wenn beispielsweise eine Pivot-Layout-Anfrage ein Datum, Besuche, Besucher und tägliche eindeutige Daten ausgibt und Sie *Besuche* entfernen, wird das aktualisierte Layout für die Anfrage angezeigt: Datum, Besucher und tägliche eindeutige Daten.

So entfernen Sie Metriken

1. Wählen Sie mindestens eine Anforderung in Excel aus, klicken Sie mit der rechten Maustaste darauf und wählen Sie **[!UICONTROL Metriken bearbeiten]** aus. Klicken Sie alternativ auf **[!UICONTROL Verwalten]** > **[!UICONTROL Mehrere bearbeiten]** > **`<choose metric>`** > **[!UICONTROL Gruppe bearbeiten]**, um die Gruppe der zu ändernden Anfragen auszuwählen.

1. Wählen Sie **[!UICONTROL Metrik(en) entfernen]**.

   ![Screenshot, der die ausgewählte Option „Gruppe bearbeiten“ und „Metrik(en) entfernen“ zeigt.](assets/remove_metric.png)

1. Wählen Sie eine oder mehrere Metriken aus, die aus der Anfrage entfernt werden sollen.
1. Aktualisieren Sie die Anforderung. Bis zur Aktualisierung werden Offline-Daten angezeigt.
