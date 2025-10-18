---
title: Überlegungen zur Migration des Besucher-ID-Service für Adobe Analytics
description: Ein Überblick darüber, wie Adobe Analytics mit dem Besucher-ID-Service verbunden ist.
source-git-commit: 3055a76f797438be71e82ea8f73800dc82ff4805
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 0%

---

# Überlegungen zur Migration des Besucher-ID-Service für Adobe Analytics

Wenn Ihr Unternehmen plant, mit einer bestehenden Analytics-Implementierung zum Besucher-ID-Service zu wechseln, sind einige wichtige Themen zu beachten. Diese Überlegungen sind wichtig, um die Integrität der Besucheridentifizierung beizubehalten und zu verstehen, wie der ID-Service in Anwesenheit einer vorhandenen Analytics-Implementierung funktioniert.

## Schnittstellen zwischen dem Besucher-ID-Dienst und älteren Analytics-Besucher-Cookies

Da AppMeasurement über eine eigene Methode zur Besucheridentifizierung verfügt, verfügen manche Besucher möglicherweise über veraltete Analytics-Cookies, wenn ein Unternehmen den Besucher-ID-Dienst bereitstellt. In der folgenden Liste wird beschrieben, wie ein Besucher unter verschiedenen Umständen identifiziert wird.

* **Keine Besucher-Cookies vorhanden**: Der ID-Service weist eine Experience Cloud-ID zu (`mid`).
* **Ein `s_vi` Cookie ist vorhanden**: Der ID-Service schreibt zusätzlich zu einer Experience Cloud-ID (`aid`) die vorhandene veraltete Analytics-ID (`AMCV`) in das `mid`-Cookie. Da `aid` in der Reihenfolge [&#x200B; Vorgänge höher liegt, &#x200B;](overview.md) die alte Analytics-ID die Besucherkennung, bis das `AMCV`-Cookie abläuft oder gelöscht wird. Wenn eine Nachfrist aktiviert ist, enthält der ID-Service in seiner Antwort sowohl die `mid` als auch die `aid`.
* **Es ist ein Ausweich-Cookie vorhanden**: Der ID-Service schreibt das Ausweich-Cookie (`fid`) nicht in das `AMCV`-Cookie. Stattdessen erhalten Besuchende eine Experience Cloud-ID (`mid`), als ob sie neue Besuchende wären.

## Übergangsphase für den Besucher-ID-Service

Wenn Sie über mehrere Implementierungen verfügen, die Daten an dieselbe Report Suite senden, und Sie den Besucher-ID-Service nur für einige Implementierungen implementieren können, empfiehlt Adobe, eine Übergangsphase zu konfigurieren. Wenn beispielsweise der Support-Bereich Ihrer Site von einer separaten Tagging-Lösung verwaltet wird, kann der Besucher-ID-Service auf dem Rest Ihrer Site bereitgestellt werden, bevor der Support-Bereich aufgerufen wird. Ohne eine Übergangsphase erhalten neue Besucher, die den Abschnitt „Support“ anzeigen, eine alte Analytics-Besucher-ID, wodurch zwei separate Besucher gezählt werden. Bei einer Übergangsphase stellt der Besucher-ID-Dienst sowohl eine Experience Cloud-ID (`mid`) als auch eine ältere Analytics-Besucher-ID (`aid`) bereit, damit Bereiche Ihrer Site ohne den ID-Dienst bei der Besucheridentifizierung konsistent bleiben.

Wenn Sie die Bereitstellung des Besucher-ID-Service für alle Bereiche Ihrer Site koordinieren, benötigen Sie keine Übergangsphase. Wenden Sie sich zur Konfiguration einer Übergangsphase an die [Adobe-Kundenunterstützung](https://helpx.adobe.com/de/marketing-cloud/contact-support.html).

## Domain-übergreifendes Tracking

Einige ältere Implementierungen der Analytics-Besucher-ID verwenden möglicherweise „benutzerfreundliche Drittanbieter-Cookies“, bei denen zwei Domains dasselbe Besucher-Cookie in einer gemeinsamen Domain wie `data.example.com` teilen. Da es sich bei benutzerfreundlichen Third-Party-Cookies weiterhin um Third-Party-Cookies handelt, werden sie von den meisten modernen Browsern abgelehnt, sodass Analytics zur Besucheridentifizierung eine Fallback-ID (`fid`) verwenden muss. Der Wechsel zum ID-Service ermöglicht es allen Domains, das `AMCV`-Cookie in einem First-Party-Kontext zu setzen, was ihre Lebensfähigkeit zur Beibehaltung einer Besucher-ID erhöht.

Während der Besucher-ID-Dienst versucht, ein Drittanbieter-Cookie für domänenübergreifendes Tracking (das [`demdex`-Cookie) &#x200B;](https://experienceleague.adobe.com/de/docs/id-service/using/intro/cookies) setzen, wird es von den meisten modernen Browsern häufig abgelehnt. Erwägen Sie die Verwendung der [`appendVisitorIDsTo`](https://experienceleague.adobe.com/de/docs/id-service/using/id-service-api/methods/appendvisitorid)-Methode, um die Experience Cloud-IDs zwischen den Domains zu übergeben, deren Inhaber Sie sind.

## Server-seitiges Tracking

Sie können [`getMarketingCloudVisitorID`](https://experienceleague.adobe.com/de/docs/id-service/using/id-service-api/methods/getmcvid) aufrufen, um die Experience Cloud-ID (`mid`) und [`getAnalyticsVisitorID`](https://experienceleague.adobe.com/de/docs/id-service/using/id-service-api/methods/getanalyticsvisitorid), um die Legacy-Analytics-ID (`aid`) zu erhalten. Adobe empfiehlt, nach beiden zu suchen, um die Logik der Besucheridentifizierung beizubehalten.
