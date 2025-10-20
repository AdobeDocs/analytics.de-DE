---
title: Besucheridentifizierung in Adobe Analytics
description: Erfahren Sie, wie Sie in Adobe Analytics Besuchende mithilfe der neuesten Best Practices identifizieren.
source-git-commit: 779ba5b0a1d71467aaaf3872fd707cc323ae8af2
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 12%

---

# Besucheridentifizierung in Adobe Analytics

Die Besucheridentifizierung spielt eine zentrale Rolle für den Wert, den Adobe Analytics für das Verständnis des Online-Benutzerverhaltens bietet. Dazu gehört die Verknüpfung von Treffern mit derselben Person im Laufe der Zeit mithilfe einer gemeinsamen Kennung. Eine genaue Besucheridentifizierung stellt zuverlässige Metriken sicher und unterstützt eine sinnvolle Implementierungsstrategie. Adobe empfiehlt Unternehmen, modernen Identitätsdiensten für Konsistenz und Datenintegrität plattformübergreifend Priorität einzuräumen.

Die Besucheridentifizierung in Adobe Analytics besteht aus den folgenden Komponenten:

* Client-seitige Kennung: Wird normalerweise in einem Erstanbieter-Cookie gespeichert. Implementierungen, die auf Drittanbieter-Cookies angewiesen sind, sind aufgrund moderner Browser-Datenschutzstandards weniger konsistent mit der Besucheridentifizierung.
* Server-seitige Kennung: Jede Analytics-Besucher-ID ist mit einem Profil auf den Servern von Adobe verknüpft. Diese Besucherprofile ermöglichen die Persistenz für Variablen wie [eVars](/help/components/dimensions/evar.md). Profile werden nach mindestens 13 Monaten Inaktivität gelöscht, unabhängig vom Ablauf von Besucher-ID-Cookies.

## Adobe Analytics-Identifizierungsreihenfolge der Vorgänge

Wenn Adobe einen Treffer erhält, werden die folgenden Prüfungen der Reihe nach durchgeführt. Wenn eine bestimmte Eigenschaft vorhanden ist, verwendet Adobe diese Kennung für den Treffer. Wenn mehrere Kennungen in einem Treffer vorhanden sind, wird nur die erste Methode verwendet.

| Verwendete Reihenfolge | Abfrageparameter | Vorhanden, wenn |
|---|---|---|
| **1<sup>st</sup>** | `vid` | Die [`visitorID`](/help/implement/vars/config-vars/visitorid.md)-Variable ist gesetzt. |
| **2<sup>nd</sup>** | `aid` | Der Besucher verfügt über ein vorhandenes [`s_vi`](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/cookies/analytics)-Cookie. Wird bei Implementierungen ohne oder vor der Implementierung des Besucher-Identity Service gesetzt. |
| **3<sup>rd</sup>** | `mid` | Der Besucher verfügt über ein vorhandenes [`s_ecid`](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/cookies/analytics)-Cookie. Festlegen bei Implementierungen mit dem [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de). Adobe empfiehlt, nach Möglichkeit für alle Implementierungen den ID-Service zu verwenden. |
| **4<sup>th</sup>** | `fid` | Der Besucher verfügt über ein vorhandenes [`s_fid`](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/cookies/analytics)-Cookie oder wenn `aid` und `mid` aus irgendeinem Grund nicht festgelegt werden konnten. |
| **5<sup>th</sup>** | IP-Adresse, Benutzeragent, Gateway-IP-Adresse | Wird als letztes Mittel verwendet, um einen Unique Visitor zu identifizieren, wenn der Browser des Besuchers keine Cookies akzeptiert. |

## Verhalten, das sich auf die Zahl der Unique Visitors auswirkt

Unique-Visitor-IDs werden in der Regel in einem Browser-Cookie gespeichert. Ein neuer Unique Visitor wird gezählt, wenn ein Besucher eine der folgenden Aktionen ausführt:

* Löscht die Cookies jederzeit. Ein Unique Visitor wird für einen Treffer gezählt, nachdem jeder Cache geleert wurde.
* Besucher-ID-Cookies laufen aufgrund der Datenschutzeinstellungen ihres Browsers ab. Einige Browser beinhalten Tracking-Präventionsmethoden, die die Lebensdauer von Cookies begrenzen.
* Öffnet einen anderen Browser auf demselben Computer. Pro Browser wird ein Unique Visitor gezählt.
* Öffnet eine private Browser-Sitzung (z. B. die Chrome-Registerkarte Inkognito ). Pro Browser-Sitzung wird ein Unique Visitor gezählt, nachdem alle Registerkarten geschlossen wurden.
* Besucht Ihre Site auf verschiedenen Geräten. Pro Gerät wird ein Unique Visitor gezählt.
* Besucht Ihre Site nach mehr als 13 Monaten Inaktivität.

Erwägen Sie [ Verwendung von ](https://experienceleague.adobe.com/de/docs/analytics-platform/using/stitching/overview) in Customer Journey Analytics, um dieselbe Person mithilfe mehrerer Browser oder Geräte zu identifizieren.

## Verhalten, das sich nicht auf die Anzahl der Unique Visitors auswirkt

Ein neuer Unique Visitor *nicht* gezählt, solange die Besucher-ID beibehalten wird:

* Schließt den Browser (für weniger als 13 Monate)
* Aktualisiert den Browser auf die neueste Version.
* Startet den Computer neu.
