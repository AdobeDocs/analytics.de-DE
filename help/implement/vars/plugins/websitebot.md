---
title: websiteBot
description: Identifizieren Sie Bots dynamisch durch Mausbewegungen.
feature: Variables
exl-id: de997254-c604-4ca0-bdda-5920f3a4fa57
source-git-commit: b8640d1387a475e2a9dd082759f0514bd18c1b6e
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 100%

---

# Adobe Plug-in: websiteBot

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Mit dem `websiteBot`-Plug-in können Sie dynamisch identifizieren, ob Desktop-Besucher Bots sind. Mithilfe dieser Daten können Sie eine höhere Genauigkeit bei allen Arten von Berichten erzielen. Dadurch verfügen Sie über eine bessere Möglichkeit, legitimen Sitetraffic zu messen.

Dieses Plug-in führt zwei Prüfungen durch:

* Zunächst wird bei einem Desktop-Gerät ein Ereignis-Listener für die Mausbewegung hinzugefügt.
* Danach wird anhand der Variablen `navigator.UserAgent` ermittelt, ob es sich bei dem Gerät um ein Desktop-Gerät oder ein Smartphone bzw. Tablet handelt. Smartphones und Tablets werden ignoriert.

Wenn sich der Benutzeragent auf einem Desktop befindet und keine Mausbewegung erkannt wird, kann das Plug-in 

* Führen Sie entweder einen Aufruf für eine Direktaufrufregel mit dem Web SDK oder der Adobe Analytics-Erweiterung aus oder
* Führen Sie einen Linktracking-Aufruf aus, um anzugeben, dass der Besucher kein Bot ist.

## Voraussetzungen

Adobe empfiehlt vor der Verwendung dieses Plug-ins Folgendes:

* **eVar-Einstellungen konfigurieren**: Richten Sie in den Report Suite-Einstellungen eine eVar unter [Konversionsvariablen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-var-admin.md) ein. Legen Sie den Ablauf auf **Niemals** oder **Visit** und die Zuordnung auf **Ausgangswert (Erster)** fest. Diese eVar sollte in den beiden folgenden Fällen festgelegt werden: wenn entweder die Regel [!UICONTROL Direktaufruf] oder der Aufruf `s.tl` ausgelöst wird.
* **Benutzeragent in einer separaten Variablen** erfassen: Erfassen Sie die Benutzeragenten-Zeichenfolge in einer separaten Variablen, um die Wirksamkeit dieses Plug-ins zu überwachen. Legen Sie bei jedem Treffer eine eVar auf `navigator.UserAgent` fest, um diese Daten zu erfassen.

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor

1. Fügen Sie eine neue Regel `websiteBot` hinzu.
1. Fügen Sie der Regel `websiteBot` ein **Mausbewegung-Listener**-Ereignis mit diesem benutzerdefinierten Code hinzu:

   ```js
   trigger(document.addEventListener('mousemove', function detectMouseMove() {   
    document.removeEventListener('mousemove', detectMouseMove, false);   
    if (!
      /(android|bb\d+|meego).+mobile|avantgo|bada\/|blackberry|blazer|compal|elaine|fennec|hiptop|iemobile|
      ip(hone|od)|ipad|iris|kindle|Android|Silk|lge |maemo|midp|mmp|netfront|opera m(ob|in)i|palm( os)?|
      phone|p(ixi|re)\/|plucker|pocket|psp|series(4|6)0|symbian|treo|up\.(browser|link)|vodafone|wap|
      windows (ce|phone)|xda|xiino/i
         .test(navigator.userAgent) ||
      /1207|6310|6590|3gso|4thp|50[1-6]i|770s|802s|a wa|abac|ac(er|oo|s\-)|ai(ko|rn)|al(av|ca|co)|
      amoi|an(ex|ny|yw)|aptu|ar(ch|go)|as(te|us)|attw|au(di|\-m|r |s )|avan|be(ck|ll|nq)|bi(lb|rd)|
      bl(ac|az)|br(e|v)w|bumb|bw\-(n|u)|c55\/|capi|ccwa|cdm\-|cell|chtm|cldc|cmd\-|co(mp|nd)|craw|
      da(it|ll|ng)|dbte|dc\-s|devi|dica|dmob|do(c|p)o|ds(12|\-d)|el(49|ai)|em(l2|ul)|er(ic|k0)|esl8|
      ez([4-7]0|os|wa|ze)|fetc|fly(\-|_)|g1 u|g560|gene|gf\-5|g\-mo|go(\.w|od)|gr(ad|un)|haie|hcit|
      hd\-(m|p|t)|hei\-|hi(pt|ta)|hp( i|ip)|hs\-c|ht(c(\-| |_|a|g|p|s|t)|tp)|hu(aw|tc)|i\-(20|go|ma)|
      i230|iac( |\-|\/)|ibro|idea|ig01|ikom|im1k|inno|ipaq|iris|ja(t|v)a|jbro|jemu|jigs|kddi|keji|
      kgt( |\/)|klon|kpt |kwc\-|kyo(c|k)|le(no|xi)|lg( g|\/(k|l|u)|50|54|\-[a-w])|libw|lynx|m1\-w|
      m3ga|m50\/|ma(te|ui|xo)|mc(01|21|ca)|m\-cr|me(rc|ri)|mi(o8|oa|ts)|mmef|mo(01|02|bi|de|do|t(\-| 
      |o|v)|zz)|mt(50|p1|v )|mwbp|mywa|n10[0-2]|n20[2-3]|n30(0|2)|n50(0|2|5)|n7(0(0|1)|10)|ne((c|m)\-|
      on|tf|wf|wg|wt)|nok(6|i)|nzph|o2im|op(ti|wv)|oran|owg1|p800|pan(a|d|t)|pdxg|pg(13|\-([1-8]|c))|
      phil|pire|pl(ay|uc)|pn\-2|po(ck|rt|se)|prox|psio|pt\-g|qa\-a|qc(07|12|21|32|60|\-[2-7]|i\-)|
      qtek|r380|r600|raks|rim9|ro(ve|zo)|s55\/|sa(ge|ma|mm|ms|ny|va)|sc(01|h\-|oo|p\-)|sdk\/|
      se(c(\-|0|1)|47|mc|nd|ri)|sgh\-|shar|sie(\-|m)|sk\-0|sl(45|id)|sm(al|ar|b3|it|t5)|so(ft|ny)|
      sp(01|h\-|v\-|v )|sy(01|mb)|t2(18|50)|t6(00|10|18)|ta(gt|lk)|tcl\-|tdg\-|tel(i|m)|tim\-|t\-mo|
      to(pl|sh)|ts(70|m\-|m3|m5)|tx\-9|up(\.b|g1|si)|utst|v400|v750|veri|vi(rg|te)|vk(40|5[0-3]|\-v)|
      vm40|voda|vulc|vx(52|53|60|61|70|80|81|83|85|98)|w3c(\-| )|webc|whit|wi(g |nc|nw)|wmlb|wonu|
      x700|yas\-|your|zeto|zte\-/i
      .test(navigator.userAgent.substr(0, 4))) {       
      _satellite.track('websiteBot')
         }
      }))
   ```

1. Fügen Sie eine Regel [!UICONTROL Direktaufruf] hinzu, die ein Analytics-Beacon auslöst, wobei `websiteBot` als Kennung verwendet wird. In diesem Beispiel wird ein `s.tl`-Aufruf verwendet:

   ![websiteBot-Kennung](assets/websitebot.png)

1. Lösen Sie die Aktionen „Adobe Analytics - Variablen festlegen“ und „Adobe Analytics - Beacon senden“ in der Regel [!UICONTROL Direktaufruf] aus. Eine Möglichkeit hierzu finden Sie im folgenden Beispiel:

   ![Aktionen „Beacon senden“](assets/websitebot2.png)


## Installieren des Plug-ins mit AppMeasurement

Kopieren Sie den folgenden Code und fügen Sie ihn an beliebiger Stelle in der AppMeasurement Datei ein, nachdem das Analytics-Tracking-Objekt instanziiert wurde (unter Verwendung von [`s_gi`](../functions/s-gi.md)). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: websiteBot BETA v0.12 */
/(android|bb\d+|meego).+mobile|avantgo|bada\/|blackberry|blazer|compal|elaine|fennec|hiptop|iemobile|ip(hone|od)|ipad|iris|kindle|Android|Silk|lge |maemo|midp|mmp|netfront|opera m(ob|in)i|palm( os)?|phone|p(ixi|re)\/|plucker|pocket|psp|series(4|6)0|symbian|treo|up\.(browser|link)|vodafone|wap|windows (ce|phone)|xda|xiino/i.test(navigator.userAgent)&&!/1207|6310|6590|3gso|4thp|50[1-6]i|770s|802s|a wa|abac|ac(er|oo|s\-)|ai(ko|rn)|al(av|ca|co)|amoi|an(ex|ny|yw)|aptu|ar(ch|go)|as(te|us)|attw|au(di|\-m|r |s )|avan|be(ck|ll|nq)|bi(lb|rd)|bl(ac|az)|br(e|v)w|bumb|bw\-(n|u)|c55\/|capi|ccwa|cdm\-|cell|chtm|cldc|cmd\-|co(mp|nd)|craw|da(it|ll|ng)|dbte|dc\-s|devi|dica|dmob|do(c|p)o|ds(12|\-d)|el(49|ai)|em(l2|ul)|er(ic|k0)|esl8|ez([4-7]0|os|wa|ze)|fetc|fly(\-|_)|g1 u|g560|gene|gf\-5|g\-mo|go(\.w|od)|gr(ad|un)|haie|hcit|hd\-(m|p|t)|hei\-|hi(pt|ta)|hp( i|ip)|hs\-c|ht(c(\-| |_|a|g|p|s|t)|tp)|hu(aw|tc)|i\-(20|go|ma)|i230|iac( |\-|\/)|ibro|idea|ig01|ikom|im1k|inno|ipaq|iris|ja(t|v)a|jbro|jemu|jigs|kddi|keji|kgt( |\/)|klon|kpt |kwc\-|kyo(c|k)|le(no|xi)|lg( g|\/(k|l|u)|50|54|\-[a-w])|libw|lynx|m1\-w|m3ga|m50\/|ma(te|ui|xo)|mc(01|21|ca)|m\-cr|me(rc|ri)|mi(o8|oa|ts)|mmef|mo(01|02|bi|de|do|t(\-| |o|v)|zz)|mt(50|p1|v )|mwbp|mywa|n10[0-2]|n20[2-3]|n30(0|2)|n50(0|2|5)|n7(0(0|1)|10)|ne((c|m)\-|on|tf|wf|wg|wt)|nok(6|i)|nzph|o2im|op(ti|wv)|oran|owg1|p800|pan(a|d|t)|pdxg|pg(13|\-([1-8]|c))|phil|pire|pl(ay|uc)|pn\-2|po(ck|rt|se)|prox|psio|pt\-g|qa\-a|qc(07|12|21|32|60|\-[2-7]|i\-)|qtek|r380|r600|raks|rim9|ro(ve|zo)|s55\/|sa(ge|ma|mm|ms|ny|va)|sc(01|h\-|oo|p\-)|sdk\/|se(c(\-|0|1)|47|mc|nd|ri)|sgh\-|shar|sie(\-|m)|sk\-0|sl(45|id)|sm(al|ar|b3|it|t5)|so(ft|ny)|sp(01|h\-|v\-|v )|sy(01|mb)|t2(18|50)|t6(00|10|18)|ta(gt|lk)|tcl\-|tdg\-|tel(i|m)|tim\-|t\-mo|to(pl|sh)|ts(70|m\-|m3|m5)|tx\-9|up(\.b|g1|si)|utst|v400|v750|veri|vi(rg|te)|vk(40|5[0-3]|\-v)|vm40|voda|vulc|vx(52|53|60|61|70|80|81|83|85|98)|w3c(\-| )|webc|whit|wi(g |nc|nw)|wmlb|wonu|x700|yas\-|your|zeto|zte\-/i.test(navigator.userAgent.substr(0,4))||document.addEventListener("mousemove",function e(){document.removeEventListener("mousemove",e,!1),s.tl(!0,"o","Not a bot")});
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Das Plug-in `websiteBot` löst einen `s.tl`-Aufruf aus, wenn Nicht-Bot-Traffic erkannt wird.

## Beispiele

```js
// Set eVar1 to detect bots. Dimension items in reporting are "true" or "false"
s.eVar1 = websiteBot;

// Use a ternary operator to set eVar values
s.eVar1 = websiteBot ? "Bot detected" : "Not a bot";
```

## Versionsverlauf

### 0.1 (19. Januar 2021)

* Beta-Version

### 0.11 (3. Juni 2021)

* Aktualisierter AppMeasurement-Plug-in-Code
* Der Abschnitt zum benutzerdefinierten Code-Editor wurde durch Anweisungen ergänzt.
* Der Abschnitt „Verwenden des Plug-ins“ wurde aktualisiert.
