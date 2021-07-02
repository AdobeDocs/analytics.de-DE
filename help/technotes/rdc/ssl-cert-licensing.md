---
title: SSL-Zertifikatslizenzierung
description: Zertifizierungsverfahren für kundenverwaltete Zertifikate
exl-id: 7d1373c8-6f7b-4ce7-a555-d3d506e08d17
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: ht
source-wordcount: '256'
ht-degree: 100%

---

# SSL-/TLS-Zertifikatlizenzierung

Adobe empfiehlt, dass Sie Ihr Zertifikat ohne zusätzliche Kosten im Rahmen des [Adobe-Programms für verwaltete Zertifikate](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html?lang=de) verwalten. Das Adobe-Programm für verwaltete Zertifikate ist vollständig automatisiert und stellt sicher, dass Zertifikate zeitnah erneuert werden, sodass abgelaufene Zertifikate keine Auswirkungen haben.

Wenn Sie das [Adobe-Programm für verwaltete Zertifikate](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html?lang=de) nicht verwenden möchten, sind Sie für die Bereitstellung eines SSL-/TLS-Zertifikats für Erstanbieter-Cookies verantwortlich.

Bei Bereitstellung Ihres eigenen Zertifikats sind Sie dafür verantwortlich, diese SSL-Zertifikate zu kaufen und zu verwalten.  Ihr SSL-/TLS-Zertifikat muss eine unbegrenzte Server-Lizenz enthalten.

Um die Zertifikatsicherheit zu gewährleisten, fordern Sie bei Adobe eine [CSR]-Anfrage (Certificate Signing Request) für die Zertifikatsignierung an und stellen Sie bei Ihrer zuständigen Zertifizierungsstelle sicher, dass das Zertifikat signiert wird.  Stellen Sie Adobe das signierte Zertifikat zur Implementierung zur Verfügung.  Bei diesem Vorgang wird die Sicherheit des Zertifikatschlüssels beibehalten.  Die Adobe-Kundenunterstützung unterstützt diesen Prozess.

Stellen Sie im Rahmen der Zertifikatverwaltung mindestens einen Monat vor Ablauf Ihres Zertifikats bei Ihrer gewünschten Zertifizierungsstelle sicher, dass Sie ein neues Zertifikat erhalten und dies Adobe zur Verfügung stellen.  Dieses Zertifikat sollte dieselbe CSR verwenden wie zuvor.  Wenden Sie sich an Adobe, wenn Sie eine Kopie der CSR benötigen oder eine neue CSR mit einem neuen Schlüssel erstellen möchten.

Die Kundenunterstützung ist unter customercare@adobe.com oder 1-800-497-0335 erreichbar.

Häufig verwendete Zertifizierungsstellen sind DigiCert, Comodo und GeoTrust.
