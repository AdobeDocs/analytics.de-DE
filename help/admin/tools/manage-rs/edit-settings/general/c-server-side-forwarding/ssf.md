---
description: Die Server-seitige Weiterleitung wurde für Kunden entwickelt, die Daten aus Analytics in Echtzeit für andere CX Enterprise-Lösungen freigeben möchten. Wenn diese Option aktiviert ist, ermöglicht die Server-seitige Weiterleitung während des Datenerfassungsprozesses Analytics das Pushen von Daten an andere CX Enterprise-Lösungen und diese Lösungen das Pushen von Daten an Analytics.
solution: Analytics
title: Übersicht über die Server-seitige Weiterleitung
feature: Report Suite Settings
exl-id: e3cd72d2-9588-4770-a7c2-64b13a1e9519
role: Admin
TQID: 'https://experienceleague.adobe.com/3Jing56TCBeoAFOXowaXAXoTDkXgQB0-j5jFmVOTsrw'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
subfeature_v2:
  - id: c354699e-6555-4397-8706-1a9a89984069
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 301a0341e725ca15f1700046528ea5f42969add4
workflow-type: tm+mt
source-wordcount: 887
ht-degree: 60%

---

# Übersicht über die Server-seitige Weiterleitung

Die Server-seitige Weiterleitung wurde für Kunden entwickelt, die Daten aus Analytics in Echtzeit für andere CX Enterprise-Lösungen freigeben möchten. Wenn diese Option aktiviert ist, ermöglicht die Server-seitige Weiterleitung während des Datenerfassungsprozesses Analytics das Pushen von Daten an andere CX Enterprise-Lösungen und diese Lösungen das Pushen von Daten an Analytics.

Die Server-seitige Weiterleitung verbessert die Datenerfassung, da sie:

* Reduziert Aufrufe von der Seite. Mit der serverseitigen Weiterleitung müssen Kunden von [!DNL Audience Manager] für die Datenerfassung nicht mehr DIL verwenden, weil die Weiterleitung über Analytics erfolgt. Das Entfernen von DIL bedeutet, einen `"/event"`-Aufruf zu entfernen. Weniger Aufrufe helfen, die Seitenladezeiten zu verbessern, was zu einem besseren Kundenerlebnis auf Ihrer Site führt.
* Ermöglicht die gemeinsame Nutzung von Daten zwischen CX Enterprise-Lösungen.
* Konformität mit unseren Best Practices für die Implementierung und Bereitstellung von Audience Manager-Code.

>[!TIP]
>
>Audience Manager-Bestandskunden, die Analytics verwenden, sollten auf die serverseitige Weiterleitung migrieren. Neukunden von Adobe Analytics und Audience Manager sollten die serverseitige Weiterleitung (anstelle von DIL) als Standardmethode zur Datenerfassung und -übertragung implementieren.

>[!IMPORTANT]
>Gemäß den Anforderungen des sogenannten EU-Cookie-Gesetzes haben Datenverantwortliche (Analytics-Kundinnen und -Kunden) nun die Möglichkeit, bislang noch nicht bewilligte Daten auf Adobe Analytics zu beschränken und zu verhindern, dass sie Server-seitig an Adobe Audience Manager (AAM) weitergeleitet werden. Eine neue Variable im Implementierungskontext ermöglicht es, die Treffer zu kennzeichnen, bei denen noch keine Zustimmung erfolgt ist. Diese Variable verhindert, sofern festgelegt, dass diese Treffer vor einer Einwilligung an Adobe Audience Manager weitergeleitet werden. Weitere Informationen finden Sie unter [DSGVO_ePrivacy - Einhaltung und Server-seitige Weiterleitung](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf-gdpr.md).

Wenn Sie nachvollziehen möchten, wo sich Ihre Organisation bezüglich der Implementierung der serverseitigen Weiterleitung befindet, führen Sie die folgenden Validierungsschritte durch:

## ![Grafik step1_icon.png](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/assets/step1_icon.png) ECID-Dienstimplementierung überprüfen

Überprüfen Sie, ob der Experience Cloud ID-(ECID-)Service implementiert wurde, indem Sie die [Analytics-Tracking-Anfrage](https://experienceleague.adobe.com/docs/id-service/using/implementation/test-verify.html?lang=de) prüfen.

Stellen Sie auf der Registerkarte „Anfrage“ sicher, dass ein ECID-Wert festgelegt wurde. Dies gibt darüber Auskunft, dass der Identity Service korrekt implementiert wurde. Dies ist eine Voraussetzung für die serverseitige Weiterleitung.

* Wenn ein ECID-Wert angezeigt wird, fahren Sie mit Schritt 2 fort.
* Wenn kein ECID-Wert angezeigt wird, [implementieren Sie den Identity Service](https://experienceleague.adobe.com/docs/id-service/using/implementation/implementation-guides.html?lang=de), bevor Sie den Vorgang bei Schritt 2 fortsetzen.

## ![Grafik step2_icon.png](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/assets/step2_icon.png) Implementierungsversion der serverseitigen Weiterleitung überprüfen

Überprüfen Sie, ob bereits eine Version der serverseitigen Weiterleitung implementiert ist, indem Sie die [Analytics-Tracking-Anforderung prüfen](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf-verify.md).

Überprüfen Sie auf der Registerkarte „Antwort“, ob die Antwort Audience Manager-Daten umfasst. Bei Anzeige des Folgenden gilt das Nachstehende:

* Eine **JSON-Antwort von Audience Manager mit Elementen wie „postbacks“ oder „dcs_region“**: Es ist bereits eine Form der serverseitigen Weiterleitung aktiviert. Fahren Sie mit Schritt 3 fort.
* **&quot;status&quot;:&quot;SUCCESS&quot;**: Das Zielgruppen-Management-Modul ist zwar implementiert, die serverseitige Weiterleitung ist jedoch nicht ordnungsgemäß konfiguriert. Fahren Sie mit Schritt 3 fort.
* Ein **2 x 2-Bild**: Sie haben keine Server-seitige Weiterleitung oder das Audience Management-Modul implementiert. So korrigieren Sie dies:

   * **Adobe Audience Manager-Kundinnen und -Kunden mit DIL**: Koordinieren Sie die folgenden beiden Elemente in enger Verbindung:

      1. Entfernen Sie den DIL-Code und installieren Sie den [Audience Management-Modul](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/audience-management-module.html?lang=de)-Seitencode.
      1. Aktivieren Sie die Server-seitige Weiterleitung in der Admin-Benutzeroberfläche von Analytics, wie in Schritt 3 beschrieben. Wenn Sie diese Einstellung vor dem Entfernen des DIL-Codes aktivieren, werden Daten dupliziert und zusätzliche in Rechnung gestellte Server-Aufrufe an Audience Manager erstellt.

   * **Neue Adobe Audience Manager-Kundinnen und -Kunden**: Installieren Sie den Seiten-Code für das [Zielgruppen-Management-Modul](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/audience-management-module.html?lang=de) und fahren Sie mit Schritt 3 fort. Es werden erst Daten an Audience Manager gesendet, nachdem die Server-seitige Weiterleitung in Schritt 3 aktiviert wurde.

## ![Grafik step3_icon.png](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/assets/step3_icon.png) Implementierung der serverseitigen Weiterleitung der Report Suite überprüfen

Überprüfen Sie, ob die Server-seitige Weiterleitung auf der Report Suite-Ebene implementiert wurde, anstatt des alten Tracking-Server-Ansatzes.

Die Server-seitige Weiterleitung auf Report Suite-Ebene wird gegenüber dem alten Tracking-Server-Ansatz empfohlen, da Sie detaillierter steuern können, welche Daten von Analytics freigegeben werden. Sie ist auch eine Voraussetzung für diese Audience Analytics-Integration.

Gehen Sie zu **Analytics** > **Admin** > **Report Suites** > (**Report Suites** auswählen) > **Einstellungen bearbeiten** > **Allgemein** > **Serverseitige Weiterleitung**. Wenn das Kontrollkästchen folgenden Zustand aufweist, gilt das Nachfolgende:

* **Inaktiv** (Sie können keine Auswahl treffen oder das Menü existiert nicht): Die ausgewählten Report Suites sind keiner Organisations-ID zugewiesen. Wenden Sie sich an die Kundenunterstützung, um sicherzustellen, dass die Report Suite korrekt zugeordnet ist.
* **Deaktiviert**: Die neue Server-seitige Weiterleitung ist nicht aktiviert. Lesen Sie den Inhalt der Seite und aktivieren Sie dann die Funktion.
* **Aktiviert**: Sie wurden für die neue Server-seitige Weiterleitung bereitgestellt. Sie können diese Audience Analytics-Integration auch einrichten.

>[!NOTE]
>
>Daten werden erst dann in anderen CX Enterprise-Lösungen wie [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html?lang=de) oder [Audiences](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=de) angezeigt, wenn alle drei Schritte abgeschlossen sind. Nach der Aktivierung dauert es mehrere Stunden, bis diese Einstellungen wirksam werden.
