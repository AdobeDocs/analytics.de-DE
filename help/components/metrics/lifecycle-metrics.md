---
title: Lebenszyklusmetriken für Mobile
description: Metriken basierend auf Daten, die mit dem Mobile SDK erfasst wurden.
feature: Metrics
exl-id: 64af4942-d249-47a5-a62f-6051f4c44ee3
TQID: 'https://experienceleague.adobe.com/Y1IigGbQygTsS9UD3WEp9z8rLTqkeDuhZZ83AJQMa3o'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: 6fd4400b33fcfc8bc3cd3ffc54fa738fef3441ef
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 10%
---
# Lebenszyklusmetriken für Mobile

>[!BEGINSHADEBOX]

*Diese Seite verweist auf Daten, die häufig über die Adobe Experience Platform Mobile SDK verfolgt werden. Informationen zu Dimensionen, die mit der Mobile SDK verfolgt werden, finden Sie unter [Mobile-Lebenszyklusdimensionen](../dimensions/lifecycle-dimensions.md). Informationen zu Mobilgeräten mit dem Benutzeragenten finden Sie unter [Dimensionen für die mobile Suche](../dimensions/mobile-dimensions.md).*

>[!ENDSHADEBOX]

| Name der Lebenszyklusmetrik | Beschreibung | Kontextdatenvariable |
| --- | --- | --- |
| **[!UICONTROL Erste Starts]** | Die Häufigkeit, mit der die App zum ersten Mal ausgeführt wurde, nachdem sie installiert oder neu installiert wurde. | `a.InstallEvent` |
| **[!UICONTROL Upgrades]** | Die Häufigkeit, mit der die App zum ersten Mal nach einem Upgrade oder nach einer Änderung der Versionsnummer ausgeführt wurde. | `a.UpgradeEvent` |
| **[!UICONTROL Launches]** | Die Häufigkeit, mit der die App ausgeführt wurde, einschließlich Ausführungen nach Abstürzen und Installationen. Ein Launch wird auch gezählt, wenn die App nach Überschreiten des Lebenszyklussitzungs-Timeouts aus dem Hintergrund fortgesetzt wird. | `a.LaunchEvent` |
| **[!UICONTROL Abstürze]** | Die Häufigkeit, mit der die App abgestürzt ist, bevor sie geschlossen wurde. Der Absturz wird beim nächsten Start der App gemeldet. | `a.CrashEvent` |
| **[!UICONTROL Gesamtsitzungslänge]** | Die Gesamtzahl der Sekunden, die App-Sitzungen dauerten, basierend auf der Dauer der App und im Vordergrund. Jeder Launch zeigt die Länge der vorherigen Sitzung an. Diese Metrik ist die Summe dieser Werte. | `a.PrevSessionLength` |
| **[!UICONTROL Aktionsdauer insgesamt]** | Die Gesamtzahl der Sekunden (Uhrzeit) zwischen dem Start und dem Ende einer zeitgesteuerten Aktion in allen Sitzungen. Wird mit den `trackTimedAction` Methoden in der veralteten Mobile Services-SDK (4.x) gefüllt. | `a.action.time.total` |
| **[!UICONTROL Aktionsdauer in Anwendung]** | Die Anzahl der Sekunden, die in der App zwischen dem Start und dem Ende einer zeitgesteuerten Aktion sitzungsübergreifend verbracht wurden. Wird mit den `trackTimedAction` Methoden in der veralteten Mobile Services-SDK (4.x) gefüllt. | `a.action.time.inapp` |
| **[!UICONTROL Lebenszeitwert (event)]** | Der Lebenszeitwert eines Benutzers, z. B. Käufe über die gesamte Lebensdauer, Anzeigen-Ansichten, abgeschlossene Videos oder Social Shares. Wird durch die `trackLifetimeValueIncrease` in der veralteten Mobile Services-SDK (4.x) aufgefüllt. | `a.ltv.amount` |

>[!NOTE]
>
>Die Metriken [!UICONTROL Aktionszeit insgesamt], [!UICONTROL Aktionszeit in der App] und [!UICONTROL Lebenszeitwert (Ereignis)] werden mit Methoden aus der veralteten Mobile Services SDK (4.x) ausgefüllt, die nicht mehr unterstützt wird. Adobe Experience Platform Mobile SDK füllt diese Metriken nicht automatisch aus. Unter [Migration von Adobe Mobile Library (v4) zu Experience Platform Analytics](https://developer.adobe.com/client-sdks/resources/upgrade-platform-sdks/analytics/) finden Sie Alternativen zu zeitgesteuerten Aktionen und zur Nachverfolgung von Lebensdauerwerten.
