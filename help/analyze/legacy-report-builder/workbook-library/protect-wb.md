---
description: Erfahren Sie, wie Sie alle Anforderungen in einer Arbeitsmappe vor dem Hinzufügen und Bearbeiten von Anforderungen schützen können, indem Sie die Arbeitsmappe sperren.
title: Sperren und Entsperren von Arbeitsmappen
uuid: ef5c276c-5f74-4741-b6fa-4c79eda29f62
feature: Report Builder
role: User, Admin
exl-id: b5a83532-9fa7-4f1f-b744-e5d74781fffb
TQID: https://experienceleague.adobe.com/0UyYFqVn5qAIimI3obHdsBbTsRirLl6llZf8Y3endLo
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 475
ht-degree: 19%

---

# Arbeitsmappen sperren und entsperren

{{legacy-arb}}

Sie können alle Anforderungen in einer Arbeitsmappe vor dem Hinzufügen und Bearbeiten von Anforderungen schützen, indem Sie die Arbeitsmappe sperren. Dies ermöglicht die Offline-Bearbeitung von Arbeitsmappen, indem alle Berichtsanfragen angehalten werden, um eine effizientere Bearbeitung zu ermöglichen.

Wenn Sie als Analyst eine Arbeitsmappe sperren, können Sie Ihre Arbeitsmappen-Anfragen vor Manipulationen durch andere Benutzer in Ihrer Organisation schützen. Gleichzeitig können diese Benutzer die Anfragen in der Arbeitsmappe immer noch aktualisieren.

Um eine Arbeitsmappe vor Bearbeitung zu schützen, klicken Sie in der **[!UICONTROL -Symbolleiste]** Sperren“ (![](assets/locked_icon.png)).

Um den Schutz einer Arbeitsmappe aufzuheben, klicken Sie auf **[!UICONTROL Entsperrt]** ( ![](assets/unlocked_icon.png)).

Sie können eine Arbeitsmappe entsperren, wenn Sie über eine der folgenden Berechtigungen verfügen:

* Sie sind ein Administrator oder
* Sie sind die Person, die die Arbeitsmappe ursprünglich gesperrt hat. In diesem Fall müssen Sie kein Administrator sein.

>[!NOTE]
>
>Sie können eine Anfrage nur dann zu einer geschützten Arbeitsmappe hinzufügen, wenn Sie über die Berechtigungen zum Entsperren der Arbeitsmappe verfügen.

Wenn eine Arbeitsmappe für die Bearbeitung von Anfragen gesperrt ist,

* Benutzende können keine Anfragen erstellen und hinzufügen.
* Benutzende können Anfragen nicht über den Anforderungs-Assistenten bearbeiten.
* Benutzende können Anfragen nicht über die Funktionen „Mehrere Anfragen bearbeiten“ bearbeiten.
* Benutzende können Anfragen nicht ausschneiden, kopieren oder einfügen. Benutzer können jedoch weiterhin das native Excel-Kontextmenü „Ausschneiden/Kopieren/Einfügen“ verwenden, um den Inhalt der Anfrage(n) auszuschneiden/zu kopieren/einzufügen.
* Benutzer können Anfragen entweder einzeln oder als Teil einer Gruppe aktualisieren.
* Wenn die Anfrage Eingabewerte aus Zellen verwendet (Datumsbereich, Segment, Filter), können Benutzende diese Werte in den Zellen ändern und so die Anfragen indirekt bearbeiten, indem sie sie aktualisieren.

Wenn Sie versuchen, eine geschützte Arbeitsmappe über das Kontextmenü, den **[!UICONTROL Anforderungs-Manager]** oder **[!UICONTROL Mehrere Anforderungen bearbeiten]** zu bearbeiten, können Sie dies tun oder nicht:

* Wenn Sie nicht über die Berechtigung zum Entsperren einer Anfrage verfügen, wird eine Meldung angezeigt, die Sie darauf hinweist, dass Sie nicht über die Berechtigungen zum Entsperren und Bearbeiten der Arbeitsmappe verfügen.

  ![Screenshot, der die Fehlermeldung anzeigt, wenn Sie nicht über die Berechtigung zum Entsperren einer Anfrage verfügen.](assets/locked_workbook_error.png)

## Workflow {#section_260D05FF632B41DB97DB43E2ADBE2E75}

Nehmen wir an, dass Arbeitsmappe A über eine Anforderung verfügt, die gesperrt ist und von Benutzer A erstellt wurde.

**Beispiel 1: Benutzer A mit Administratorrechten (Benutzer A)**

1. Der Benutzer meldet sich bei Report Builder an und öffnet Arbeitsmappe A.
1. Arbeitsmappe A ist gesperrt, sodass auf der Symbolleiste die Schaltfläche „Anforderung erstellen“ deaktiviert ist. Auch andere Schaltflächen sind aufgrund der Sperre deaktiviert.
1. Wenn der/die Benutzende versucht, eine der deaktivierten Schaltflächen zu verwenden, wird eine Meldung angezeigt, dass die Arbeitsmappe derzeit gesperrt ist.
1. Der Benutzer kann die Arbeitsmappe entsperren, was eine vollständige Bearbeitungsfunktion ermöglicht.
1. Nach dem Entsperren bleibt die Arbeitsmappe entsperrt, bis sie explizit erneut gesperrt wird.

**Beispiel 2: Benutzer ohne Administratorrechte (Benutzer B)**

1. Der Benutzer meldet sich bei Report Builder an und öffnet Arbeitsmappe A.
1. Benutzende können die Anfrage nicht hinzufügen/bearbeiten.
1. Benutzer kann die Arbeitsmappe nicht entsperren.
