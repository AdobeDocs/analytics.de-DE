---
title: Einrichten von Report Builder
description: Eine vollständige Anleitung zum Installieren und Konfigurieren von Adobe Analytics Report Builder for Excel. Schrittweise Einrichtungsanweisungen für eine nahtlose Integration.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: 9d0161a9-ee7b-43a9-92ad-4079cf4b9c6c
source-git-commit: 1e893ce94ee3da46bbf22d7a90573681950d1135
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 39%

---

# Einrichten von Report Builder

In diesem Artikel werden die Anforderungen für die Verwendung von Report Builder for Adobe Analytics in [!DNL Microsoft] [!DNL Excel] beschrieben. und wie das Add-In installiert und eingerichtet wird.

## Voraussetzungen

Report Builder für Adobe Analytics wird von den folgenden Betriebssystemen und Webbrowsern unterstützt.

### macOS

- macOS-Version 10.x oder höher
- Alle [!DNL Microsoft] [!DNL Excel] Versionen

### Windows

- Windows 10 Version 1904 oder höher
- [!DNL Excel] Version 2106 oder höher

  Alle Benutzer von Windows Desktop [!DNL Excel] müssen Microsoft Edge Webview2 installieren, um das Add-In verwenden zu können. So installieren Sie den Controller:

   1. Öffnen von <https://aka.ms/webview2installer>.
   1. Wählen Sie das Evergreen Standalone-Installationsprogramm aus und laden Sie es herunter.
   1. Folgen Sie den Anweisungen bei der Installation.

### Web Office

- Unterstützt alle Browser und Versionen


## Report Builder Excel-Add-in

Sie müssen das Report Builder [!DNL Excel]-Add-in installieren, um [!DNL Report Builder] für Adobe Analytics verwenden zu können. Nachdem Sie das Report Builder [!DNL Excel]-Add-in installiert haben, können Sie von einer geöffneten [!DNL Excel] aus auf Report Builder zugreifen.

### Herunterladen und Installieren des Report Builder-Add-ins

So laden Sie das Report Builder-Add-in herunter und installieren es

1. Starten Sie [!DNL Excel] und öffnen Sie eine neue Arbeitsmappe.

1. Wählen **[!UICONTROL Einfügen]** > **[!UICONTROL Add-Ins abrufen]**.

1. Wählen Sie im Dialogfeld „Office-Add-ins“ die Registerkarte „Store“ aus.

1. Suchen Sie nach &quot;Report Builder&quot; und klicken Sie auf **[!UICONTROL Hinzufügen]**.

1. Klicken Sie im Dialogfeld Lizenzbedingungen und Datenschutzrichtlinien auf **[!UICONTROL Weiter]**.

**Wenn die Registerkarte „Store“ nicht angezeigt wird**

1. Wählen Sie [!DNL Excel] Datei > Konto > Einstellungen verwalten aus.

1. Aktivieren Sie das Kontrollkästchen neben „Optionale verbundene Erlebnisse aktivieren“

1. [!DNL Excel] neu starten.

**Wenn Ihre Organisation den Zugriff auf den Microsoft Store blockiert**

- Wenden Sie sich an Ihre IT- oder Sicherheitsabteilung, um eine Genehmigung für das Report Builder-Add-in anzufordern. Nachdem die Genehmigung erteilt wurde, wählen Sie im Dialogfeld „Office-Add-Ins“ die Registerkarte **[!UICONTROL Admin Managed]** aus.

  ![Die Registerkarte „Admin Managed“ im Dialogfeld „Office-Add-Ins“.](./assets/image1.png)

- Alternativ können Sie die [Manifestdatei) manuell abrufen &#x200B;](https://reportbuilder.an.adobe.com/manifest.xml) die Datei in Ihrer eigenen IT-Infrastruktur hosten. <br/>Anweisungen zum Installieren einer Excel-Manifestdatei, die nicht [&#x200B; Microsoft Store bereitgestellt wird, finden Sie in der Dokumentation zu Microsoft Office &#x200B;](https://learn.microsoft.com/en-us/office/dev/add-ins/publish/publish)Online).

Nach der Installation des Report Builder-Add-ins wird das Report Builder-Symbol im [!DNL Excel] unter der Registerkarte Startseite angezeigt.

![Das Report Builder-Symbol in Excel](/help/analyze/report-builder/assets/rb_app_icon.png)

## Anmelden bei Report Builder

Nachdem Sie das Report Builder for Excel-Add-in für Ihre Betriebsplattform oder Ihren Browser installiert haben, führen Sie die folgenden Schritte aus, um sich bei Report Builder anzumelden.

1. Öffnen Sie eine Excel-Arbeitsmappe.

1. Klicken Sie auf das Report Builder-Symbol, um Report Builder zu starten.

1. Klicken Sie in der Adobe Report Builder-Symbolleiste auf **[!UICONTROL Anmelden]**.

   ![Klicken Sie auf die Schaltfläche Report Builder-Anmeldung.](/help/analyze/report-builder/assets/rb_login.png)

1. Geben Sie Ihre Adobe Experience ID-Kontoinformationen ein. Ihre Kontoinformationen sollten mit Ihren Adobe Analytics-Anmeldeinformationen übereinstimmen.

   ![Ihr Anmeldesymbol und Ihre Organisation.](/help/analyze/report-builder/assets/image4.png)

Nach der Anmeldung werden Ihr Anmeldesymbol und Ihre Organisation oben im Bedienfeld angezeigt

## Wechseln von Organisationen

Bei der ersten Anmeldung werden Sie bei der Ihrem Profil zugewiesenen Standardorganisation angemeldet.

1. Klicken Sie auf den Namen der Organisation, die bei der Anmeldung angezeigt wird.

1. Wählen Sie eine Organisation aus der Liste der verfügbaren Organisationen aus. Es werden nur Organisationen aufgelistet, auf die Sie Zugriff haben.

   ![Die Liste der Organisationen, auf die Sie zugreifen können.](/help/analyze/report-builder/assets/image5.png)

## Abmelden

Sie können sich über das Benutzerprofil von Report Builder abmelden.

1. Speichern Sie die Änderungen in allen geöffneten Arbeitsmappen.

1. Klicken Sie auf das Avatar-Symbol, um Ihr Benutzerprofil anzuzeigen.

   ![Ihr Benutzerprofilavatar und die Schaltfläche Abmelden.](/help/analyze/report-builder/assets/image6.png)

1. Klicken Sie auf **Abmelden**.
