---
title: useLinkTrackSessionStorage
description: Speichern von Linktracking-Daten im Sitzungsspeicher statt in einem Cookie.
feature: Appmeasurement Implementation
exl-id: 3295195d-bfd6-4af9-9487-dc1ea6c3da23
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/JQc7Ii-LrL8k0KIttWFuowJCASGK2e75exSbjhG347s'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 283
ht-degree: 86%

---

# useLinkTrackSessionStorage

Wenn Ihr Unternehmen Linktracking verwendet, nutzt AppMeasurement das Cookie `s_sq`, um Informationen zwischen Treffern weiterzugeben. Manche Website-Konfigurationen stehen in Konflikt mit diesem Cookie. Wenn Sie zum Linktracking die Browser-Sitzungsspeicherung und Activity Map-Daten anstelle eines Cookies verwenden möchten, aktivieren Sie diese Variable.

Die Verwendung der Sitzungsspeicherung eines Browsers für Linktracking unterliegt einigen Einschränkungen:

* Die Sitzungsspeicherung funktioniert nicht zwischen unterschiedlichen Protokollen. Dies ist der Fall, wenn beispielsweise eine Seite über HTTP und die nächste über HTTPS bereitgestellt wird. AppMeasurement kann aufgrund von unterschiedlichen Protokollen nicht auf Linktracking-Daten in der Sitzungsspeicherung zugreifen.
* Die Sitzungsspeicherung funktioniert nicht Subdomain-übergreifend. Beispielsweise könnte ein Besucher zu `store.example.com` und dann zu `toys.example.com` navigieren. AppMeasurement kann aufgrund verschiedener Subdomains nicht auf Linktracking-Daten in der Sitzungsspeicherung zugreifen.

>[!TIP]
>
>Die zuverlässigste Implementierung ist die, die mithilfe der Sitzungsspeicherung zum Linktracking alle Inhalte über HTTPS in einer einzigen Subdomain bereitstellt.

AppMeasurement entfernt die Sitzungsspeicherungs-Linktracking-Daten, nachdem ein Treffer an Adobe gesendet wurde. Die Speicherung wird auch automatisch eingestellt, wenn die Browser-Registerkarte geschlossen wird.

## Verwenden der Speicherung von Linktracking-Sitzungen mit der Web-SDK

Web SDK unterstützt diese Funktion nicht.

## Verwenden der Linktracking-Sitzungsspeicherung mit der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.useLinkTrackSessionStorage in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die Variable `s.useLinkTrackSessionStorage` ist ein boolescher Wert, der bestimmt, ob AppMeasurement die Sitzungsspeicherung anstelle des `s_sq`-Cookies für die Linktracking-Daten verwendet. Der Standardwert lautet `false`. Legen Sie diese Variable auf `true` fest, wenn Sie möchten, dass AppMeasurement die Sitzungsspeicherung anstelle des `s_sq`-Cookies für Linktracking und Activity Map verwendet.

```js
s.useLinkTrackSessionStorage = true;
```
