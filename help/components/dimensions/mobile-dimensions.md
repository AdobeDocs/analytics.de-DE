---
title: Lookup-Dimensionen für Mobile
description: Dimensionen basierend auf der IP-Adresse und dem Benutzeragenten des Geräts.
feature: Dimensions
exl-id: fa460888-513d-4d14-93b1-33d308e0758a
TQID: https://experienceleague.adobe.com/X80x0MIx5gd16J20VU37fNSExDO2NSXPrHR8EKqsMqw
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: c77ba355-6681-41fe-b719-563d3f507fdbid: d2311670-43bd-4c2e-bc98-1da2aaba9cefid: e7d92df1-c5ba-4e93-85df-f83171b889beid: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 961
ht-degree: 95%

---

# Lookup-Dimensionen für Mobile

*Auf dieser Seite werden die Eigenschaften von Mobilgeräten aufgeführt, die auf Ihre Website zugreifen. Siehe [Lebenszyklusdimensionen für Mobile](lifecycle-dimensions.md) oder [Lebenszyklusmetriken für Mobile](../metrics/lifecycle-metrics.md) für das Tracking in einer mobilen App.*

Lookup-[Dimensionen](overview.md) für Mobile bieten Einblicke in die Eigenschaften von Mobilgeräten, die Ihre Site besuchen. Diese Eigenschaften basieren auf dem Benutzeragenten und der IP-Adresse des Treffers. Anhand dieser Dimensionen können Sie erkennen, welche Funktionen ein Mobilgerät unterstützt.

## Füllen dieser Dimensionen mit Daten

Diese Dimensionen verweisen auf interne Suchregeln von Adobe.

* Für die Dimension [!UICONTROL Mobilnetzbetreiber] arbeitet Adobe mit [Digital Element](https://www.digitalelement.com/) zusammen und nutzt NetAcuity, um Suchen zwischen IP-Adresse und Mobilnetzbetreiber zu erhalten.
* Für alle anderen Mobilgeräte-Dimensionen arbeitet Adobe mit [DeviceAtlas](https://deviceatlas.com/) zusammen, um Suchen zwischen dem Benutzeragenten und den jeweiligen Mobilgeräte-Dimensionen zu erhalten.

Die Verfügbarkeit dieser Dimensionen hängt vom Implementierungstyp ab:

* Bei AppMeasurement-Implementierungen sind diese Dimensionen vorkonfiguriert.
* Aktivieren Sie für Web SDK-Implementierungen die [!UICONTROL Geo-Suche] (für Mobilnetzbetreiber) oder die [!UICONTROL Gerätesuche] (für alle anderen Dimensionen), wenn Sie einen [Datenstrom konfigurieren](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de).

## Beschreibung der Mobilgerätedimensionen

>[!NOTE]
>
>Mit `"None"` gekennzeichnete Dimensionselemente sind keine Mobilgeräte. Wenn Sie einen Bericht wünschen, der nur Mobilgeräte enthält, ziehen Sie die Dimension „Mobilgerät“ in den Segmentbereich der Arbeitsfläche von Workspace.

* **[!UICONTROL Mobilgerät – Audio-Unterstützung]**: Stellt die Dateiformate fest, die vom Gerät wiedergegeben werden können. Zu den Beispielwerten gehören `"MP3"`, `"AAC"` und `"MIDI Monophonic"`. Die Werte in dieser Dimension schließen sich nicht gegenseitig aus. Ein einzelner Treffer kann mehreren Dimensionselementen zugeordnet werden.
* **[!UICONTROL Mobilnetzbetreiber]**: Der Telefon- oder Datenanbieter für das Gerät. Zu den Beispielwerten gehören `"Reliance Jio"`, `"Airtel"`, `"Vodafone"` und `"Verizon"`.
* **[!UICONTROL Mobilgerät – Farbtiefe]**: Die Farbtiefe des Mobilgeräts in Bit.
* **[!UICONTROL Mobilgerät – Cookie-Unterstützung]**: Stellt fest, ob das Mobilgerät Cookies unterstützt. Diese Dimension gibt nicht an, ob der Browser Cookies akzeptiert. Zu den Dimensionselementen gehören `"Supported"`, `"Not supported"` und `"Unknown"`.
* **[!UICONTROL Mobilgerät]**: Das Mobilgerät, das der Besucher verwendet.
* **[!UICONTROL Mobilgerätenummer]**: Stellt fest, ob das Mobilgerät seine Nummer übermittelt. Diese Dimension stellt nicht die Mobiltelefonnummer selbst bereit. Zu den Dimensionselementen gehören `"Supported"`, `"Not supported"` und `"Unknown"`.
* **[!UICONTROL Mobilgerätetyp]**: Der Typ des Mobilgeräts. Zu den Beispielwerten gehören `"Mobile phone"`, `"Tablet"`, `"Media player"` und `"Gaming console"`.
* **[!UICONTROL Mobil-DRM]**: Der DRM-Typ, den das Mobilgerät unterstützt. Zu den Beispielwerten gehören `"DRM OMA forward"`, `"DRM OMA combined delivery"` und `"DRM OMA separate delivery"`.
* **[!UICONTROL Mobilgerät – Bildunterstützung]**: Die Bildtypen, die vom Mobilgerät unterstützt werden. Zu den Beispielwerten gehören `"PNG"`, `"JPEG"` und `"GIF 87"`. Die Werte in dieser Dimension schließen sich nicht gegenseitig aus. Ein einzelner Treffer kann mehreren Dimensionselementen zugeordnet werden.
* **[!UICONTROL Mobile Informationsdienste]**: Die vom Gerät unterstützten Arten von Nachrichtendiensten. Moderne Geräte melden diese Informationen normalerweise nicht.
* **[!UICONTROL Mobile Java-VM]**: Die Java-Versionen, die das Gerät unterstützt.
* **[!UICONTROL Mobiles Mail-Design]**: Legt fest, ob das Gerät [Decome](https://en.wikipedia.org/wiki/Decome) unterstützt, eine Funktion, die auf japanischen Geräten bereits verwendet wird.
* **[!UICONTROL Mobilgerätehersteller]**: Klassifiziert Mobilgeräte nach Hersteller. Zu den Beispielwerten gehören `"Apple"`, `"Samsung"`, `"Huawei"` und `"Motorola"`.
* **[!UICONTROL Maximale mobile Lesezeichenlänge]**: Die maximale Anzahl von Byte, die das Mobilgerät in mit Lesezeichen versehenen URLs unterstützt. Für moderne Geräte gibt es in der Regel keine Beschränkung.
* **[!UICONTROL Maximale mobile Browser-URL-Länge]**: Die maximale Anzahl von Byte, die das Mobilgerät in URLs unterstützt. Für moderne Geräte gibt es in der Regel keine Beschränkung.
* **[!UICONTROL Maximale mobile E-Mail-Länge]**: Die maximale Anzahl von Byte, die das Mobilgerät in E-Mails unterstützt. Für moderne Geräte gibt es in der Regel keine Beschränkung.
* **[!UICONTROL Mobile Netzprotokolle]**: Die Protokolltypen, die das Gerät beim Zugriff auf das Internet unterstützt. Zu den Beispielwerten gehören `"EDGE"`, `"GPRS"`, `"UMTS"` und `"LTE"`.
* **[!UICONTROL Mobiles Betriebssystem (veraltet)]**: Verwenden Sie stattdessen die Dimension [Betriebssystem](operating-systems.md).
* **[!UICONTROL Mobiles PTT]**: Stellt fest, ob das Gerät PTT (Push to Talk) unterstützt, wodurch das Mobilgerät sich ähnlich wie ein Funkgerät verhalten kann. Modernere Geräte melden diese Funktion normalerweise nicht.
* **[!UICONTROL Mobilgerät – Bildschirmhöhe]**: Die Höhe des Bildschirms in Pixel. iPhones melden immer `"480"`, da die iPhone-Geräteversion nicht ermittelt werden kann. Informationen zum Bestimmen der Geräteversion eines iPhones finden Sie im folgenden Abschnitt.
* **[!UICONTROL Mobilgerät – Bildschirmgröße]**: Die vollständigen Abmessungen des Mobilgeräts in Pixel. Die angezeigte Bildschirmgröße gibt nicht die Ausrichtung des Geräts an. Unabhängig von der Bildschirmausrichtung verfügt jedes Gerät über eine feste Bildschirmauflösung im Bericht. Diese Größe basiert auf Untersuchungen, die bestimmen, welche Ausrichtung wahrscheinlicher ist. Sie können Größen wie `"768x1024"` und `"1024x768"` im selben Bericht sehen, wobei jede Größe ein oder mehrere verschiedene Geräte repräsentiert.
* **[!UICONTROL Mobilgerät – Bildschirmbreite]**: Die Breite des Bildschirms in Pixel.
* **[!UICONTROL Mobilgerät – Video-Unterstützung]**: Die Videodateiformate und Codecs, die vom Mobilgerät unterstützt werden. Für verschiedene Codecs von MP4- und 3GPP-Dateien existieren verschiedene Dimensionselemente. Die Werte in dieser Dimension schließen sich nicht gegenseitig aus. Ein einzelner Treffer kann mehreren Dimensionselementen zugeordnet werden.

## Aufteilen von iPhone-Geräten nach Modell oder Version

Mobilgeräte melden ihre Firmware-Version in ihrer Benutzeragenten-Zeichenfolge, nicht die Geräteversion. Beispielsweise enthält ein iPhone der aktuellen Generation einen identischen Benutzeragenten wie das iPhone der letzten Generation, wenn sie dieselbe Firmware-Version verwenden. Da es nicht möglich ist, die Geräteversion eines iPhone mit JavaScript zu bestimmen, gehören alle iPhones in denselben Behälter. Die Mobilgerätedimensionen basieren ausschließlich auf Suchvorgängen, die auf den Benutzeragenten verweisen. Sie werden also feststellen, dass alle iPhone-Geräte eine Bildschirmgröße von `320 x 480` angeben.

Wenn Sie die Geräteversion eines iPhones erfassen möchten, gibt es zwei Möglichkeiten, diese Einschränkung zu umgehen.

* **Verwenden des Mobile SDK**: Das Mobile SDK enthält Dimensionen, die die Geräteversion für die Verwendung beim Reporting verfügbar machen. Diese Methode eignet sich besser für Mobile Apps als für Websites.
* **Verwenden andere Variablen, die über JavaScript verfügbar sind**: Einige Variablen, wie `screen.height` und `screen.width`, können verwendet werden, um die Geräteversion abzuleiten. Sie könnten beispielsweise den folgenden Code-Ausschnitt auf Ihrer Site verwenden:

  ```js
  if (navigator.userAgent.indexOf('iPhone') > -1) {
    s.eVarXX = screen.width + "x" + screen.height;
    }
  ```

  Dieser Code-Block erkennt zunächst, ob es sich bei dem Gerät um ein iPhone handelt. Ist dies der Fall, verwendet der Code JavaScript, um die Bildschirmauflösung in eine eVar zu ziehen. Mit dieser Methode können Sie die Geräteversion in etwa erkennen, wenn die Bildschirmauflösungen eindeutig sind.
