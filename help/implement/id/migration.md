---
title: Überlegungen zur Migration des Besucher-ID-Service für Adobe Analytics
description: Ein Überblick darüber, wie Adobe Analytics mit dem Besucher-ID-Service verbunden ist.
exl-id: da1f9917-5254-41fb-9e2c-c94f66a22360
TQID: https://experienceleague.adobe.com/NnZ-Vv2M5cWkfekbVX1B-dFesdtxy50fMdTlwPYviYQ
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7aid: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: c8add8f2-4250-4fd9-9cde-9707036c567d
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: a947d2d7f45d4155a61cbfe0f8110851cca32e60
workflow-type: tm+mt
source-wordcount: 678
ht-degree: 2%

---

# Überlegungen zur Migration des Besucher-ID-Service für Adobe Analytics

Wenn Ihr Unternehmen plant, mit einer bestehenden Analytics-Implementierung zum Besucher-ID-Service zu wechseln, sind einige wichtige Themen zu beachten. Anhand dieser Überlegungen können Sie die Integrität der Besucheridentifizierung wahren und verstehen, wie der Besucher-ID-Service bei einer vorhandenen Analytics-Implementierung funktioniert.

>[!TIP]
>
>Diese Seite gilt nur für bestehende AppMeasurement- oder Analytics-Erweiterungsimplementierungen, bei denen der Besucher-ID-Service hinzugefügt oder ein Upgrade auf eine Web SDK-Implementierung durchgeführt wird. Anders ausgedrückt: Ihre Implementierung verwendet eine veraltete Analytics-ID (`aid`) und geht zur Verwendung einer ECID (`mid`) über. Alle Web SDK-Implementierungen verwenden den [Experience Platform Identity Service](https://experienceleague.adobe.com/de/docs/experience-platform/identity/home), der standardmäßig eine ECID (`mid`) verwendet.

## Schnittstellen zwischen dem Besucher-ID-Dienst und älteren Analytics-Besucher-Cookies

Da AppMeasurement über eine eigene veraltete Methode zur Besucheridentifizierung verfügt, verfügen manche Besucher möglicherweise über Analytics-Cookies, wenn ein Unternehmen den Besucher-ID-Dienst bereitstellt. In der folgenden Liste wird beschrieben, wie ein Besucher unter verschiedenen Umständen identifiziert wird.

* **Keine Besucher-Cookies vorhanden**: Der Besucher-ID-Dienst weist eine ECID zu (`mid`).
* **Ein `s_vi` Cookie ist vorhanden**: Der Besucher-ID-Dienst schreibt zusätzlich zu einer ECID (`mid`) die vorhandene veraltete Analytics-ID (`aid`) in das `AMCV`-Cookie. Da `aid` in der Reihenfolge [ Vorgänge höher liegt, ](overview.md) die alte Analytics-ID die Besucherkennung, bis das `AMCV`-Cookie abläuft oder gelöscht wird. Wenn eine Übergangsphase aktiviert ist, enthält der Besucher-ID-Dienst in seiner Antwort sowohl die `mid` als auch die `aid`.
* **Es ist ein Ausweich-Cookie**: Der Besucher-ID-Dienst schreibt das Ausweich-Cookie (`fid`) nicht in das `AMCV`-Cookie. Stattdessen erhalten Besucher eine ECID (`mid`), als ob sie ein neuer Besucher wären.

## Übergangsphase für den Besucher-ID-Service

Wenn Sie über mehrere Implementierungen verfügen, die Daten an dieselbe Report Suite senden, und Sie den Besucher-ID-Service nur für einige Implementierungen implementieren können, empfiehlt Adobe, eine Übergangsphase zu konfigurieren. Wenn beispielsweise der Support-Bereich Ihrer Site von einer separaten Tagging-Lösung verwaltet wird, kann der Besucher-ID-Service auf dem Rest Ihrer Site bereitgestellt werden, bevor der Support-Bereich aufgerufen wird. Ohne eine Übergangsphase erhalten neue Besucher, die den Abschnitt „Support“ anzeigen, eine alte Analytics-Besucher-ID, wodurch zwei separate Besucher gezählt werden. Bei einer Übergangsphase stellt der Besucher-ID-Dienst sowohl eine ECID (`mid`) als auch eine ältere Analytics-Besucher-ID (`aid`) bereit, damit Bereiche Ihrer Site ohne den Besucher-ID-Dienst bei der Besucheridentifizierung konsistent bleiben.

Wenn Sie die Bereitstellung des Besucher-ID-Service für alle Bereiche Ihrer Site koordinieren, benötigen Sie keine Übergangsphase. Wenden Sie sich zur Konfiguration einer Übergangsphase an die [Adobe-Kundenunterstützung](https://helpx.adobe.com/de/marketing-cloud/contact-support.html). Übergangsphasen können für bis zu 180 Tage konfiguriert und erneuert werden. Adobe empfiehlt, die Übergangsphase einzustellen, sobald Ihre gesamte Eigenschaft für die Verwendung des Besucher-ID-Service konfiguriert ist.

## Domain-übergreifendes Tracking

Einige ältere Implementierungen der Analytics-Besucher-ID verwenden möglicherweise „benutzerfreundliche Drittanbieter-Cookies“, bei denen zwei Domains dasselbe Besucher-Cookie in einer gemeinsamen Domain wie `data.example.com` teilen. Da es sich bei benutzerfreundlichen Third-Party-Cookies weiterhin um Third-Party-Cookies handelt, werden sie von vielen modernen Browsern zurückgewiesen, sodass Analytics zur Besucheridentifizierung eine Fallback-ID (`fid`) verwenden muss. Der Wechsel zum Besucher-ID-Dienst ermöglicht es allen Domains, das `AMCV`-Cookie in einem First-Party-Kontext zu setzen, was ihre Lebensfähigkeit zur Beibehaltung einer Besucher-ID erhöht.

Während der Besucher-ID-Dienst versucht, ein Drittanbieter-Cookie für domänenübergreifendes Tracking (das [`demdex`-Cookie) ](https://experienceleague.adobe.com/en/docs/id-service/using/intro/cookies) setzen, wird es von modernen Browsern häufig abgelehnt. Erwägen Sie die Verwendung der [`appendVisitorIDsTo`](https://experienceleague.adobe.com/en/docs/id-service/using/id-service-api/methods/appendvisitorid) Methode zum Übergeben der ECID (`mid`) eines Besuchers zwischen Domains, deren Inhaber Sie sind.

## Server-seitiges Tracking

Sie können [`getMarketingCloudVisitorID`](https://experienceleague.adobe.com/en/docs/id-service/using/id-service-api/methods/getmcvid) aufrufen, um die ECID (`mid`) und [`getAnalyticsVisitorID`](https://experienceleague.adobe.com/en/docs/id-service/using/id-service-api/methods/getanalyticsvisitorid), um die Legacy-Analytics-ID (`aid`) zu erhalten. Adobe empfiehlt, nach beiden zu suchen, um die Logik der Besucheridentifizierung beizubehalten.
